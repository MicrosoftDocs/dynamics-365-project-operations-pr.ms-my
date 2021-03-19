---
title: Mengimplemen medan tersuai untuk aplikasi mudah alih Microsoft Dynamics 365 Project Timesheet pada iOS dan Android
description: Topik ini menyediakan corak lazim yang menggunakan sambungan untuk mengimplemen medan tersuai.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271004"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Mengimplemen medan tersuai untuk aplikasi mudah alih Microsoft Dynamics 365 Project Timesheet pada iOS dan Android

[!include [banner](../includes/banner.md)]

Topik ini menyediakan corak lazim yang menggunakan sambungan untuk mengimplemen medan tersuai. Topik berikut dirangkumi:

- Jenis data pelbagai yang disokong oleh kerangka kerja medan tersuai
- Cara untuk menunjukkan medan baca sahaja atau boleh diedit pada entiti lembaran masa dan menyimpan semula nilai yang diberikan pengguna ke dalam pangkalan data
- Cara untuk menunjukkan medan baca sahaja pada pengepala lembaran masa
- Cara mengintegrasikan logik perniagaan tersuai yang lain untuk memasukkan nilai dalam medan dan melakukan pengesahan tambahan

## <a name="audience"></a>Hadirin

Topik ini bertujuan untuk pembangun yang mengintegrasikan medan tersuai mereka ke dalam aplikasi mudah alih Microsoft Dynamics 365 Project Timesheet yang tersedia untuk Apple iOS dan Google Android. Anggapannya adalah pembaca yang terbiasa dengan pembangunan X++ dan kefungsian lembaran masa projek.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Kontrak data – kelas TSTimesheetCustomField X++

Kelas **TSTimesheetCustomField** adalah kelas data kontrak X++ yang mewakili maklumat tentang medan tersuai untuk kefungsian lembaran masa. Senarai objek medan tersuai diserahkan pada kedua-dua kontrak data TSTimesheetDetails dan kontrak data TSTimesheetEntry untuk menunjukkan medan tersuai dalam aplikasi mudah alih.

- **TSTimesheetDetails** - Kontrak pengepala lembaran masa.
- **TSTimesheetEntry** - Kontrak transaksi lembaran masa. Kumpulan objek ini yang mempunyai maklumat projek yang sama dan nilai **timesheetLineRecId** yang membentuk garisan.

### <a name="fieldbasetype-types"></a>fieldBaseType (Jenis)

Sifat **FieldBaseType** pada objek **TsTimesheetCustom** menentukan jenis medan yang dipaparkan dalam aplikasi. Nilai **Jenis** yang disokong.

| Nilai jenis | Jenis              | Nota |
|-------------|-------------------|-------|
| 0           | Rentetan (dan Enum) | Medan dipaparkan sebagai medan teks. |
| 1           | Integer           | Nilai ditunjukkan sebagai nombor tanpa tempat perpuluhan. |
| 2           | Nyata              | Nilai ditunjukkan sebagai nombor yang mempunyai tempat perpuluhan.<p>Untuk menunjukkan nilai nyata sebagai mata wang dalam aplikasi, gunakan sifat **fieldExtenededType**. Anda boleh menggunakan sifat **numberOfDecimals** untuk menetapkan nombor tempat perpuluhan yang ditunjukkan.</p> |
| 3           | Tarikh              | Format tarikh ditentukan oleh tetapan **Tarikh, masa dan format nombor** pengguna yang dikhususkan di bawah **Keutamaan bahasa dan negara/rantau** dalam **Pilihan pengguna**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Jika sifat **stringOptions** disediakan pada objek **TSTimesheetCustomField**, medan teks bebas disediakan kepada pengguna.

    Sifat **stringLength** boleh digunakan untuk menetapkan panjang rentetan maksimum yang boleh dimasukkan oleh pengguna.

- Jika sifat **stringOptions** disediakan pada objek **TSTimesheetCustomField**, elemen senarai itu adalah hanya nilai yang boleh dipilih oleh pengguna dengan menggunakan butang pilihan (butang radio).

    Dalam kes ini, medan rentetan boleh bertindak sebagai nilai enum untuk tujuan entri pengguna. Untuk menyimpan nilai ke pangkalan data sebagai enum, petakan nilai rentetan secara manual sebelum anda menyimpan ke pangkalan data dengan menggunakan rantaian perintah (lihat bahagian “Gunakan rantaian perintah pada kelas TSTimesheetEntryService untuk menyimpan semula entri lembaran masa daripada aplikasi ke pangkalan data” kemudian dalam topik ini sebagai contoh).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Anda boleh menggunakan sifat ini untuk memformat nilai nyata sebagai mata wang. Pendekatan ini terpakai hanya apabila nilai **fieldBaseType** adalah **Nyata**.

- **TSCustomFieldExtendedType:None** – Tiada pemformatan digunakan.
- **TSCustomFieldExtendedType::Mata wang** – Format nilai sebagai mata wang.

    Apabila pemformatan mata wang adalah aktif, medan **stringValue** boleh digunakan untuk meluluskan kod mata wang yang perlu ditunjukkan dalam aplikasi. Nilai adalah nilai baca sahaja.

    Medan **realValue** mengandungi jumlah wang yang perlu disimpan ke pangkalan data.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Anda boleh menggunakan sifat ini untuk menentukan di mana medan tersuai hendak dipaparkan dalam aplikasi.

- **TSCustomFieldSection::Pengepala** – Medan akan dipaparkan dalam bahagian **Lihat butiran lanjut** dalam aplikasi. Medan ini sentiasa baca sahaja.
- **TSCustomFieldSection::Line** – Medan ini akan dipaparkan selepas semua medan garisan di luar kotak pada entri lembaran masa. Medan ini boleh sama ada boleh diedit atau baca sahaja.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Sifat ini mengenal pasti medan apabila nilai yang disediakan oleh aplikasi disimpan semula ke pangkalan data.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Sifat ini mengenal pasti medan apabila nilai yang disediakan oleh aplikasi disimpan semula ke pangkalan data.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Tetapkan sifat ini kepada **Ya** untuk menentukan medan dalam bahagian entri lembaran masa perlu boleh diedit oleh pengguna. Tetapkan sifat ke **Tidak** untuk menjadikan medan baca sahaja.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Tetapkan sifat ini kepada **Ya** untuk menentukan medan dalam bahagian entri lembaran masa perlu mandatori.

### <a name="label-str"></a>label (str)

Sifat ini menentukan label yang menunjukkan medan seterusnya dalam aplikasi.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Senarai Rentetan)

Sifat ini terpakai hanya apabila **fieldBaseType** ditetapkan kepada **Rentetan**. Jika **stringOptions** ditetapkan, nilai rentetan yang tersedia untuk pemilihan melalui butang pilihan (butang radio) ditentukan oleh rentetan dalam senarai. Jika tiada rentetan disediakan, entri teks bebas dalam medan rentetan dibenarkan (lihat bahagian “Gunakan rantaian perintah pada kelas TSTimesheetEntryService untuk menyimpan semula entri lembaran masa daripada aplikasi ke pangkalan data” kemudian dalam topik ini sebagai contoh).

### <a name="stringlength-int"></a>stringLength (int)

Sifat ini menentukan panjang maksimum untuk medan rentetan. Ianya terpakai hanya apabila **fieldBaseType** ditetapkan ke **Rentetan**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Sifat ini menentukan nombor tempat perpuluhan yang ditunjukkan untuk medan nyata. Ianya terpakai hanya apabila **fieldBaseType** ditetapkan ke **Nyata**.

### <a name="ordersequence-int"></a>orderSequence (int)

Sifat ini mengawal pesanan bagi medan tersuai yang ditunjukkan dalam aplikasi apabila lebih daripada satu medan tersuai ditentukan. Medan yang mempunyai nombor rendah ditunjukkan dahulu.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Untuk medan jenis **Boolean**, sifat ini menyerahkan nilai Boolean medan antara pelayan dan aplikasi.

### <a name="guidvalue-guid"></a>guidValue (guid)

Untuk medan jenis **GUID**, sifat ini menyerahkan nilai pengecam unik sejagat (GUID) medan antara pelayan dan aplikasi.

### <a name="int64value-int64"></a>int64Value (int64)

Untuk medan jenis **Int64**, sifat ini menyerahkan nilai Int64 medan antara pelayan dan aplikasi.

### <a name="intvalue-int"></a>intValue (int)

Untuk medan jenis **Int**, sifat ini menyerahkan nilai Int medan antara pelayan dan aplikasi.

### <a name="realvalue-real"></a>realValue (real)

Untuk medan jenis **Nyata**, sifat ini menyerahkan nilai nyata medan antara pelayan dan aplikasi.

### <a name="stringvalue-str"></a>stringValue (str)

Untuk medan jenis **Rentetan**, sifat ini menyerahkan nilai rentetan medan antara pelayan dan aplikasi. Ianya juga digunakan untuk medan jenis **Nyata** diformat sebagai mata wang. Untuk medan itu, sifat digunakan untuk menyerahkan kod mata wang ke aplikasi.

### <a name="datevalue-date"></a>dateValue (tarikh)

Untuk medan jenis **Tarikh**, sifat ini menyerahkan nilai tarikh medan antara pelayan dan aplikasi.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Tunjukkan dan simpan medan tersuai dalam bahagian entri lembaran masa

Di bawah adalah syot skrin daripada aplikasi mudah alih bagi penciptaan entri lembaran masa. Ianya menunjukkan medan di luar kotak dan medan tersuai dalam bahagian "Entri masa" dipanggil "Rentetan ujian" dengan nilai enum "Pilihan kedua" tetal ditetapkan.

![Uji rentetan medan tersuai dalam aplikasi](media/timesheet-entry.jpg)



Di bawah adalah syot skrin daripada aplikasi mudah alih pengguna memilih satu daripada pilihan enum yang tersedia untuk medan tersuai "Rentetan ujian".  Kedua-dua pilihan adalah "Pilihan pertama" dan "Pilihan kedua" ditunjukkan sebagai butang radio. Pilihan kedua pada masa ini dipilih.

![Pilihan butang (butang radio) untuk medan tersuai rentetan Ujian](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Lanjutkan jadual TSTimesheetLine supaya ianya mempunyai medan tersuai

Dalam senario biasa, berkemungkinan data untuk medan tersuai dalam bahagian entri lembaran masa akan disimpan ke jadual TSTimesheetLine. Walau bagaimanapun, jadual lain boleh digunakan jika data boleh diambil berasaskan pada rekod TSTimesheetTrans yang disediakan atau jika ianya tidak mempunyai rekod tertentu (contohnya, jika medan ditetapkan sebagai baca sahaja dalam parameter projek).

Ambil perhatian bahawa medan tersuai tidak mempunyai sebarang rekod pangkalan data sandaran. Ianya boleh dijana secara dinamik berasaskan pada logik X++. Pendekatan ini berguna dalam senario baca sahaja (lihat bahagian “Gunakan rantaian perintah pada kelas TSTimesheetDetails, kaedah buildCustomFieldListForHeader untuk diisi dalam bahagian butiran” sebagai contoh nilai medan tersuai yang dijana secara dinamik.)

Di bawah adalah syot skrin daripada Visual Studio Application Object Tree. Ianya menunjukkan lanjutan jadual TSTimesheetLine dengan medan TestLineString ditambah sebagai medan tersuai.

![Rentetan baris](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Gunakan rantaian perintah pada kaedah buildCustomFieldList bagi kelas TSTimesheetSettings untuk menunjukkan medan dalam bahagian entri lembaran masa

Kod ini mengawal tetapan paparan untuk medan dalam aplikasi. Contohnya, ia mengawal jenis medan, label sama ada medan adalah mandatori dan bahagian yang memaparkan medan.

Contoh berikut menunjukkan medan rentetan pada entri masa. Medan ini mempunyai dua pilihan, **Pilihan pertama** dan **Pilihan kedua** yang tersedia melalui butang pilihan (butang radio). Medan dalam aplikasi berkaitan dengan medan **TestLineString** yang ditambahkan kepada jadual TSTimesheetLine.

Ambil perhatian bahawa penggunaan kaedah **TSTimesheetCustomField::newFromMetatdata()** adalah untuk memudahkan permulaan sifat medan tersuai: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, dan **numberOfDecimals**. Anda juga boleh menetapkan parameter secara manual mengikut kemahuan anda.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Gunakan rantaian perintah pada kaedah buildCustomFieldListForEntry bagi kelas TSTimesheetEntry untuk memasukkan nilai dalam entri lembaran masa

Kaedah **buildCustomFieldListForEntry** digunakan untuk memasukkan nilai pada baris lembaran masa yang disimpan dalam aplikasi mudah alih. Ianya mengambil rekod TSTimesheetTrans sebagai parameter. Medan daripada rekod boleh digunakan untuk mengisi dalam nilai medan tersuai dalam aplikasi.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Gunakan rantaian perintah pada kelas TSTimesheetEntryService untuk menyimpan entri lembaran masa daripada aplikasi kembali ke pangkalan data

Untuk menyimpan semula medan tersuai ke pangkalan data dalam penggunaan biasa, anda mesti melanjutkan berbilang kaedah:

- Kaedah **timesheetLineNeedsUpdating** digunakan untuk menentukan sama ada baris rekod telah diubah oleh pengguna dalam aplikasi dan mesti disimpan ke pangkalan data. Jika prestasi tidak diambil kira, kaedah ini boleh dipermudahkan supaya ianya sentiasa mengembalikan **benar**.
- Kaedah **populateTimesheetLineFromEntryDuringCreate** dan **populateTimesheetLineFromEntryDuringUpdate** boleh dilanjutkan supaya mereka memasukkan nilai dalam rekod pangkalan data TSTimesheetLine daripada rekod kontrak data TSTimesheetEntry yang disediakan. Dalam contoh yang berikut, perhatikan cara pemetaan antara medan pangkalan data dan medan entri dilakukan secara manual melalui kod X++.
- Kaedah **populateTimesheetWeekFromEntry** boleh juga dilanjutkan jika medan tersuai dipetakan ke objek **TSTimesheetEntry** mesti ditulis semula ke jadual pangkalan data TSTimesheetLineweek.

> [!NOTE]
> Contoh berikut menyimpan nilai **firstOption** atau **secondOption** yang dipilih oleh pengguna ke pangkalan data sebagai nilai rentetan mentah. Jika medan pangkalan data adalah medan jenis **Enum**, nilai itu boleh dipetakan secara manual kepada nilai enum dan kemudian disimpan ke medan enum pada jadual pangkalan data.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Tunjukkan dan simpan medan tersuai dalam bahagian entri pengepala lembaran masa

Di bawah adalah syot skrin daripada aplikasi mudah alih bagi pengguna yang melihat lembaran masa. Butang "Maklumat lanjut" telah dipilih di sudut kanan atas untuk menunjukkan pilihan Lihat butiran lanjut".  

![Lihat lebih lanjut perintah](media/show-more.png)

Di bawah adalah syot skrin daripada aplikasi mudah alih menunjukkan “Lebih” bahagian lembaran masa. Medan tersuai dipanggil “Kadar penggunaan lembaran masa ini (medan tersuai dikira)” telah ditambah ke bahagian pengepala lembaran masa. Nilai dibaca sahaja "0.667" ditetapkan pada medan tersuai.

![Lebih banyak bahagian](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Lanjutkan jadual TSTimesheetTable supaya ianya mempunyai medan tersuai

Dalam senario biasa, berkemungkinan data untuk medan tersuai dalam bahagian pengepala akan ditarik daripada jadual TSTimesheetHeader. Walau bagaimanapun, jadual lain boleh digunakan jika data boleh diambil berasaskan pada rekod TSTimesheetTable yang disediakan atau jika ianya tidak mempunyai konteks rekod tertentu (contohnya, jika medan ditetapkan sebagai baca sahaja dalam parameter projek).

Ambil perhatian bahawa medan tersuai tidak mempunyai sebarang rekod pangkalan data sandaran. Ianya boleh dijana secara dinamik berasaskan pada logik X++. Contoh berikut menunjukkan pendekatan ini.

Medan dalam bahagian pengepala sentiasa baca sahaja dalam aplikasi.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Gunakan rantaian perintah pada kaedah buildCustomFieldList bagi kelas TSTimesheetSettings untuk menunjukkan medan dalam bahagian pengepala

Kod ini mengawal tetapan paparan untuk medan dalam aplikasi. Contohnya, ia mengawal jenis medan, label sama ada medan adalah mandatori dan bahagian yang memaparkan medan.

Contoh berikut menunjukkan nilai dikira dalam bahagian pengepala dalam aplikasi.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Gunakan rantaian perintah pada kaedah buildCustomFieldListForHeader bagi kelas TSTimesheetDetails untuk mengisi butiran lembaran masa

Kaedah **buildCustomFieldListForHeader** digunakan untuk mengisi butiran pengepala lembaran masa dalam aplikasi mudah alih. Ianya mengambil rekod TSTimesheetTable sebagai parameter. Medan daripada rekod boleh digunakan untuk mengisi dalam nilai medan tersuai dalam aplikasi. Contoh berikut tidak membaca sebarang nilai daripada pangkalan data. Sebaliknya, ia menggunakan logik X++ untuk menjana nilai dikira yang kemudiannya ditunjukkan dalam aplikasi.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Peluang yang boleh dikonfigurasi/boleh dilanjutkan yang lain

### <a name="adding-additional-validation-for-the-app"></a>Menambah pengesahan tambahan untuk aplikasi

Logik sedia ada untuk kefungsian lembaran masa pada peringkat pangkalan data akan masih berfungsi seperti yang dijangkakan. Untuk mengganggu penyempurnaan operasi simpan atau serah dan menunjukkan message ralat tertentu, anda boleh menambah **buang ralat("message kepada pengguna")** ke kod melalui lanjutan rantaian perintah. Berikut adalah tiga contoh kaedah boleh dilanjutkan yang berguna:

- Jika **validateWrite** pada jadual TSTimesheetLine mengembalikan **palsu** semasa operasi simpan untuk baris lembaran masa, message ralat ditunjukkan dalam aplikasi mudah alih.
- Jika **validateSubmit** pada jadual TSTimesheetTable mengembalikan **palsu** semasa operasi penyerahan dalam aplikasi, message ralat ditunjukkan kepada pengguna.
- Logik yang diisi dalam medan (contohnya, **Sifat Baris**) semasa kaedah **sisip** pada jadual TSTimesheetLine akan masih berjalan.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Menyembunyi dan menanda medan di luar kotak sebagai baca sahaja melalui konfigurasi

Daripada parameter projek, anda boleh menjadikan medan di luar kota baca sahaja atau tersembunyi dalam aplikasi mudah alih. Tetapkan pilihan dalam bahagian **Lembaran masa mudah alih** pada tab **Lembaran masa** bagi halaman **Parameter pengurusan projek dan perakaunan**.

![Parameter projek](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Mengubah aktiviti yang tersedia untuk pemilihan melalui sambungan

Aktiviti yang tersedia untuk pemilihan projek diisi melalui kaedah **getActivitiesForProject()** dan **getActivityQuery()** dalam kelas **TsTimesheetProjectService**. Anda boleh menggunakan rantaian perintah untuk mengubah tingkah laku ini bagi memadankan senario perniagaan anda untuk aktiviti yang tersedia bagi pemilihan projek tertentu.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Memasukkan kategori projek lalai pada entri lembaran masa

Entri bagi kategori projek lalai pada entri lembaran masa berlaku pada tiga peringkat. Anda boleh menggunakan rantaian perintah untuk melanjutkan tingkah laku pada mana-mana atau semua peringkat ini untuk mencapai tingkah laku yang diinginkan. Hierarki berikut digunakan:

1. Aplikasi cuba meletakkan kategori lalai daripada sumber projek. Kategori lalai ditetapkan dalam kaedah **getCurrentUserResource** dan **getDelegatedResourcesForCurrentUser** dalam kelas **TSTimesheetSettingsService**.
2. Jika kategori lalai tidak disediakan pada peringkat sumber projek, aplikasi cuba menariknya daripada aktiviti projek. Kategori lalai ditetapkan dalam kaedah **getActivitiesForProject** dalam kelas **TSTimesheetProjectService**.
3. Jika kategori lalai tidak disediakan pada peringkat aktiviti projek, kategori lalai diambil daripada parameter projek. Kategori lalai ditetapkan dalam kaedah **getProjectDetailsbyRule** dalam kelas **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]