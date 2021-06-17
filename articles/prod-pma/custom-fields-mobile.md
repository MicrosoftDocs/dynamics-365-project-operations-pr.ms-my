---
title: Mengimplemen medan tersuai untuk aplikasi mudah alih Microsoft Dynamics 365 Project Timesheet pada iOS dan Android
description: Topik ini menyediakan corak lazim yang menggunakan sambungan untuk mengimplemen medan tersuai.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003054"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="651a7-103">Mengimplemen medan tersuai untuk aplikasi mudah alih Microsoft Dynamics 365 Project Timesheet pada iOS dan Android</span><span class="sxs-lookup"><span data-stu-id="651a7-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="651a7-104">Topik ini menyediakan corak lazim yang menggunakan sambungan untuk mengimplemen medan tersuai.</span><span class="sxs-lookup"><span data-stu-id="651a7-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="651a7-105">Topik berikut dirangkumi:</span><span class="sxs-lookup"><span data-stu-id="651a7-105">The following topics are covered:</span></span>

- <span data-ttu-id="651a7-106">Jenis data pelbagai yang disokong oleh kerangka kerja medan tersuai</span><span class="sxs-lookup"><span data-stu-id="651a7-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="651a7-107">Cara untuk menunjukkan medan baca sahaja atau boleh diedit pada entiti lembaran masa dan menyimpan semula nilai yang diberikan pengguna ke dalam pangkalan data</span><span class="sxs-lookup"><span data-stu-id="651a7-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="651a7-108">Cara untuk menunjukkan medan baca sahaja pada pengepala lembaran masa</span><span class="sxs-lookup"><span data-stu-id="651a7-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="651a7-109">Cara mengintegrasikan logik perniagaan tersuai yang lain untuk memasukkan nilai dalam medan dan melakukan pengesahan tambahan</span><span class="sxs-lookup"><span data-stu-id="651a7-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="651a7-110">Hadirin</span><span class="sxs-lookup"><span data-stu-id="651a7-110">Audience</span></span>

<span data-ttu-id="651a7-111">Topik ini bertujuan untuk pembangun yang mengintegrasikan medan tersuai mereka ke dalam aplikasi mudah alih Microsoft Dynamics 365 Project Timesheet yang tersedia untuk Apple iOS dan Google Android.</span><span class="sxs-lookup"><span data-stu-id="651a7-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="651a7-112">Anggapannya adalah pembaca yang terbiasa dengan pembangunan X++ dan kefungsian lembaran masa projek.</span><span class="sxs-lookup"><span data-stu-id="651a7-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="651a7-113">Kontrak data – kelas TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="651a7-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="651a7-114">Kelas **TSTimesheetCustomField** adalah kelas data kontrak X++ yang mewakili maklumat tentang medan tersuai untuk kefungsian lembaran masa.</span><span class="sxs-lookup"><span data-stu-id="651a7-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="651a7-115">Senarai objek medan tersuai diserahkan pada kedua-dua kontrak data TSTimesheetDetails dan kontrak data TSTimesheetEntry untuk menunjukkan medan tersuai dalam aplikasi mudah alih.</span><span class="sxs-lookup"><span data-stu-id="651a7-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="651a7-116">**TSTimesheetDetails** - Kontrak pengepala lembaran masa.</span><span class="sxs-lookup"><span data-stu-id="651a7-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="651a7-117">**TSTimesheetEntry** - Kontrak transaksi lembaran masa.</span><span class="sxs-lookup"><span data-stu-id="651a7-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="651a7-118">Kumpulan objek ini yang mempunyai maklumat projek yang sama dan nilai **timesheetLineRecId** yang membentuk garisan.</span><span class="sxs-lookup"><span data-stu-id="651a7-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="651a7-119">fieldBaseType (Jenis)</span><span class="sxs-lookup"><span data-stu-id="651a7-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="651a7-120">Sifat **FieldBaseType** pada objek **TsTimesheetCustom** menentukan jenis medan yang dipaparkan dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="651a7-121">Nilai **Jenis** yang disokong.</span><span class="sxs-lookup"><span data-stu-id="651a7-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="651a7-122">Nilai jenis</span><span class="sxs-lookup"><span data-stu-id="651a7-122">Types value</span></span> | <span data-ttu-id="651a7-123">Jenis</span><span class="sxs-lookup"><span data-stu-id="651a7-123">Type</span></span>              | <span data-ttu-id="651a7-124">Nota</span><span class="sxs-lookup"><span data-stu-id="651a7-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="651a7-125">0</span><span class="sxs-lookup"><span data-stu-id="651a7-125">0</span></span>           | <span data-ttu-id="651a7-126">Rentetan (dan Enum)</span><span class="sxs-lookup"><span data-stu-id="651a7-126">String (and Enum)</span></span> | <span data-ttu-id="651a7-127">Medan dipaparkan sebagai medan teks.</span><span class="sxs-lookup"><span data-stu-id="651a7-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="651a7-128">1</span><span class="sxs-lookup"><span data-stu-id="651a7-128">1</span></span>           | <span data-ttu-id="651a7-129">Integer</span><span class="sxs-lookup"><span data-stu-id="651a7-129">Integer</span></span>           | <span data-ttu-id="651a7-130">Nilai ditunjukkan sebagai nombor tanpa tempat perpuluhan.</span><span class="sxs-lookup"><span data-stu-id="651a7-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="651a7-131">2</span><span class="sxs-lookup"><span data-stu-id="651a7-131">2</span></span>           | <span data-ttu-id="651a7-132">Nyata</span><span class="sxs-lookup"><span data-stu-id="651a7-132">Real</span></span>              | <span data-ttu-id="651a7-133">Nilai ditunjukkan sebagai nombor yang mempunyai tempat perpuluhan.</span><span class="sxs-lookup"><span data-stu-id="651a7-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="651a7-134">Untuk menunjukkan nilai nyata sebagai mata wang dalam aplikasi, gunakan sifat **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="651a7-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="651a7-135">Anda boleh menggunakan sifat **numberOfDecimals** untuk menetapkan nombor tempat perpuluhan yang ditunjukkan.</span><span class="sxs-lookup"><span data-stu-id="651a7-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="651a7-136">3</span><span class="sxs-lookup"><span data-stu-id="651a7-136">3</span></span>           | <span data-ttu-id="651a7-137">Tarikh</span><span class="sxs-lookup"><span data-stu-id="651a7-137">Date</span></span>              | <span data-ttu-id="651a7-138">Format tarikh ditentukan oleh tetapan **Tarikh, masa dan format nombor** pengguna yang dikhususkan di bawah **Keutamaan bahasa dan negara/rantau** dalam **Pilihan pengguna**.</span><span class="sxs-lookup"><span data-stu-id="651a7-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="651a7-139">4</span><span class="sxs-lookup"><span data-stu-id="651a7-139">4</span></span>           | <span data-ttu-id="651a7-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="651a7-140">Boolean</span></span>           | |
| <span data-ttu-id="651a7-141">15</span><span class="sxs-lookup"><span data-stu-id="651a7-141">15</span></span>          | <span data-ttu-id="651a7-142">GUID</span><span class="sxs-lookup"><span data-stu-id="651a7-142">GUID</span></span>              | |
| <span data-ttu-id="651a7-143">16</span><span class="sxs-lookup"><span data-stu-id="651a7-143">16</span></span>          | <span data-ttu-id="651a7-144">Int64</span><span class="sxs-lookup"><span data-stu-id="651a7-144">Int64</span></span>             | |

- <span data-ttu-id="651a7-145">Jika sifat **stringOptions** disediakan pada objek **TSTimesheetCustomField**, medan teks bebas disediakan kepada pengguna.</span><span class="sxs-lookup"><span data-stu-id="651a7-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="651a7-146">Sifat **stringLength** boleh digunakan untuk menetapkan panjang rentetan maksimum yang boleh dimasukkan oleh pengguna.</span><span class="sxs-lookup"><span data-stu-id="651a7-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="651a7-147">Jika sifat **stringOptions** disediakan pada objek **TSTimesheetCustomField**, elemen senarai itu adalah hanya nilai yang boleh dipilih oleh pengguna dengan menggunakan butang pilihan (butang radio).</span><span class="sxs-lookup"><span data-stu-id="651a7-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="651a7-148">Dalam kes ini, medan rentetan boleh bertindak sebagai nilai enum untuk tujuan entri pengguna.</span><span class="sxs-lookup"><span data-stu-id="651a7-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="651a7-149">Untuk menyimpan nilai ke pangkalan data sebagai enum, petakan nilai rentetan secara manual sebelum anda menyimpan ke pangkalan data dengan menggunakan rantaian perintah (lihat bahagian “Gunakan rantaian perintah pada kelas TSTimesheetEntryService untuk menyimpan semula entri lembaran masa daripada aplikasi ke pangkalan data” kemudian dalam topik ini sebagai contoh).</span><span class="sxs-lookup"><span data-stu-id="651a7-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="651a7-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="651a7-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="651a7-151">Anda boleh menggunakan sifat ini untuk memformat nilai nyata sebagai mata wang.</span><span class="sxs-lookup"><span data-stu-id="651a7-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="651a7-152">Pendekatan ini terpakai hanya apabila nilai **fieldBaseType** adalah **Nyata**.</span><span class="sxs-lookup"><span data-stu-id="651a7-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="651a7-153">**TSCustomFieldExtendedType:None** – Tiada pemformatan digunakan.</span><span class="sxs-lookup"><span data-stu-id="651a7-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="651a7-154">**TSCustomFieldExtendedType::Mata wang** – Format nilai sebagai mata wang.</span><span class="sxs-lookup"><span data-stu-id="651a7-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="651a7-155">Apabila pemformatan mata wang adalah aktif, medan **stringValue** boleh digunakan untuk meluluskan kod mata wang yang perlu ditunjukkan dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="651a7-156">Nilai adalah nilai baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="651a7-156">The value is a read-only value.</span></span>

    <span data-ttu-id="651a7-157">Medan **realValue** mengandungi jumlah wang yang perlu disimpan ke pangkalan data.</span><span class="sxs-lookup"><span data-stu-id="651a7-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="651a7-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="651a7-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="651a7-159">Anda boleh menggunakan sifat ini untuk menentukan di mana medan tersuai hendak dipaparkan dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="651a7-160">**TSCustomFieldSection::Pengepala** – Medan akan dipaparkan dalam bahagian **Lihat butiran lanjut** dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="651a7-161">Medan ini sentiasa baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="651a7-161">These fields are always read-only.</span></span>
- <span data-ttu-id="651a7-162">**TSCustomFieldSection::Line** – Medan ini akan dipaparkan selepas semua medan garisan di luar kotak pada entri lembaran masa.</span><span class="sxs-lookup"><span data-stu-id="651a7-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="651a7-163">Medan ini boleh sama ada boleh diedit atau baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="651a7-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="651a7-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="651a7-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="651a7-165">Sifat ini mengenal pasti medan apabila nilai yang disediakan oleh aplikasi disimpan semula ke pangkalan data.</span><span class="sxs-lookup"><span data-stu-id="651a7-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="651a7-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="651a7-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="651a7-167">Sifat ini mengenal pasti medan apabila nilai yang disediakan oleh aplikasi disimpan semula ke pangkalan data.</span><span class="sxs-lookup"><span data-stu-id="651a7-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="651a7-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="651a7-168">isEditable (NoYes)</span></span>

<span data-ttu-id="651a7-169">Tetapkan sifat ini kepada **Ya** untuk menentukan medan dalam bahagian entri lembaran masa perlu boleh diedit oleh pengguna.</span><span class="sxs-lookup"><span data-stu-id="651a7-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="651a7-170">Tetapkan sifat ke **Tidak** untuk menjadikan medan baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="651a7-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="651a7-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="651a7-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="651a7-172">Tetapkan sifat ini kepada **Ya** untuk menentukan medan dalam bahagian entri lembaran masa perlu mandatori.</span><span class="sxs-lookup"><span data-stu-id="651a7-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="651a7-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="651a7-173">label (str)</span></span>

<span data-ttu-id="651a7-174">Sifat ini menentukan label yang menunjukkan medan seterusnya dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="651a7-175">stringOptions (Senarai Rentetan)</span><span class="sxs-lookup"><span data-stu-id="651a7-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="651a7-176">Sifat ini terpakai hanya apabila **fieldBaseType** ditetapkan kepada **Rentetan**.</span><span class="sxs-lookup"><span data-stu-id="651a7-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="651a7-177">Jika **stringOptions** ditetapkan, nilai rentetan yang tersedia untuk pemilihan melalui butang pilihan (butang radio) ditentukan oleh rentetan dalam senarai.</span><span class="sxs-lookup"><span data-stu-id="651a7-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="651a7-178">Jika tiada rentetan disediakan, entri teks bebas dalam medan rentetan dibenarkan (lihat bahagian “Gunakan rantaian perintah pada kelas TSTimesheetEntryService untuk menyimpan semula entri lembaran masa daripada aplikasi ke pangkalan data” kemudian dalam topik ini sebagai contoh).</span><span class="sxs-lookup"><span data-stu-id="651a7-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="651a7-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="651a7-179">stringLength (int)</span></span>

<span data-ttu-id="651a7-180">Sifat ini menentukan panjang maksimum untuk medan rentetan.</span><span class="sxs-lookup"><span data-stu-id="651a7-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="651a7-181">Ianya terpakai hanya apabila **fieldBaseType** ditetapkan ke **Rentetan**.</span><span class="sxs-lookup"><span data-stu-id="651a7-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="651a7-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="651a7-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="651a7-183">Sifat ini menentukan nombor tempat perpuluhan yang ditunjukkan untuk medan nyata.</span><span class="sxs-lookup"><span data-stu-id="651a7-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="651a7-184">Ianya terpakai hanya apabila **fieldBaseType** ditetapkan ke **Nyata**.</span><span class="sxs-lookup"><span data-stu-id="651a7-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="651a7-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="651a7-185">orderSequence (int)</span></span>

<span data-ttu-id="651a7-186">Sifat ini mengawal pesanan bagi medan tersuai yang ditunjukkan dalam aplikasi apabila lebih daripada satu medan tersuai ditentukan.</span><span class="sxs-lookup"><span data-stu-id="651a7-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="651a7-187">Medan yang mempunyai nombor rendah ditunjukkan dahulu.</span><span class="sxs-lookup"><span data-stu-id="651a7-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="651a7-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="651a7-188">booleanValue (boolean)</span></span>

<span data-ttu-id="651a7-189">Untuk medan jenis **Boolean**, sifat ini menyerahkan nilai Boolean medan antara pelayan dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="651a7-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="651a7-190">guidValue (guid)</span></span>

<span data-ttu-id="651a7-191">Untuk medan jenis **GUID**, sifat ini menyerahkan nilai pengecam unik sejagat (GUID) medan antara pelayan dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="651a7-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="651a7-192">int64Value (int64)</span></span>

<span data-ttu-id="651a7-193">Untuk medan jenis **Int64**, sifat ini menyerahkan nilai Int64 medan antara pelayan dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="651a7-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="651a7-194">intValue (int)</span></span>

<span data-ttu-id="651a7-195">Untuk medan jenis **Int**, sifat ini menyerahkan nilai Int medan antara pelayan dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="651a7-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="651a7-196">realValue (real)</span></span>

<span data-ttu-id="651a7-197">Untuk medan jenis **Nyata**, sifat ini menyerahkan nilai nyata medan antara pelayan dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="651a7-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="651a7-198">stringValue (str)</span></span>

<span data-ttu-id="651a7-199">Untuk medan jenis **Rentetan**, sifat ini menyerahkan nilai rentetan medan antara pelayan dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="651a7-200">Ianya juga digunakan untuk medan jenis **Nyata** diformat sebagai mata wang.</span><span class="sxs-lookup"><span data-stu-id="651a7-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="651a7-201">Untuk medan itu, sifat digunakan untuk menyerahkan kod mata wang ke aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="651a7-202">dateValue (tarikh)</span><span class="sxs-lookup"><span data-stu-id="651a7-202">dateValue (date)</span></span>

<span data-ttu-id="651a7-203">Untuk medan jenis **Tarikh**, sifat ini menyerahkan nilai tarikh medan antara pelayan dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="651a7-204">Tunjukkan dan simpan medan tersuai dalam bahagian entri lembaran masa</span><span class="sxs-lookup"><span data-stu-id="651a7-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="651a7-205">Di bawah adalah syot skrin daripada aplikasi mudah alih bagi penciptaan entri lembaran masa.</span><span class="sxs-lookup"><span data-stu-id="651a7-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="651a7-206">Ianya menunjukkan medan di luar kotak dan medan tersuai dalam bahagian "Entri masa" dipanggil "Rentetan ujian" dengan nilai enum "Pilihan kedua" tetal ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="651a7-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Uji rentetan medan tersuai dalam aplikasi](media/timesheet-entry.jpg)



<span data-ttu-id="651a7-208">Di bawah adalah syot skrin daripada aplikasi mudah alih pengguna memilih satu daripada pilihan enum yang tersedia untuk medan tersuai "Rentetan ujian".</span><span class="sxs-lookup"><span data-stu-id="651a7-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="651a7-209">Kedua-dua pilihan adalah "Pilihan pertama" dan "Pilihan kedua" ditunjukkan sebagai butang radio.</span><span class="sxs-lookup"><span data-stu-id="651a7-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="651a7-210">Pilihan kedua pada masa ini dipilih.</span><span class="sxs-lookup"><span data-stu-id="651a7-210">The second option is currently selected.</span></span>

![Pilihan butang (butang radio) untuk medan tersuai rentetan Ujian](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="651a7-212">Lanjutkan jadual TSTimesheetLine supaya ianya mempunyai medan tersuai</span><span class="sxs-lookup"><span data-stu-id="651a7-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="651a7-213">Dalam senario biasa, berkemungkinan data untuk medan tersuai dalam bahagian entri lembaran masa akan disimpan ke jadual TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="651a7-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="651a7-214">Walau bagaimanapun, jadual lain boleh digunakan jika data boleh diambil berasaskan pada rekod TSTimesheetTrans yang disediakan atau jika ianya tidak mempunyai rekod tertentu (contohnya, jika medan ditetapkan sebagai baca sahaja dalam parameter projek).</span><span class="sxs-lookup"><span data-stu-id="651a7-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="651a7-215">Ambil perhatian bahawa medan tersuai tidak mempunyai sebarang rekod pangkalan data sandaran.</span><span class="sxs-lookup"><span data-stu-id="651a7-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="651a7-216">Ianya boleh dijana secara dinamik berasaskan pada logik X++.</span><span class="sxs-lookup"><span data-stu-id="651a7-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="651a7-217">Pendekatan ini berguna dalam senario baca sahaja (lihat bahagian “Gunakan rantaian perintah pada kelas TSTimesheetDetails, kaedah buildCustomFieldListForHeader untuk diisi dalam bahagian butiran” sebagai contoh nilai medan tersuai yang dijana secara dinamik.)</span><span class="sxs-lookup"><span data-stu-id="651a7-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="651a7-218">Di bawah adalah syot skrin daripada Visual Studio Application Object Tree.</span><span class="sxs-lookup"><span data-stu-id="651a7-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="651a7-219">Ianya menunjukkan lanjutan jadual TSTimesheetLine dengan medan TestLineString ditambah sebagai medan tersuai.</span><span class="sxs-lookup"><span data-stu-id="651a7-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Rentetan baris](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="651a7-221">Gunakan rantaian perintah pada kaedah buildCustomFieldList bagi kelas TSTimesheetSettings untuk menunjukkan medan dalam bahagian entri lembaran masa</span><span class="sxs-lookup"><span data-stu-id="651a7-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="651a7-222">Kod ini mengawal tetapan paparan untuk medan dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="651a7-223">Contohnya, ia mengawal jenis medan, label sama ada medan adalah mandatori dan bahagian yang memaparkan medan.</span><span class="sxs-lookup"><span data-stu-id="651a7-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="651a7-224">Contoh berikut menunjukkan medan rentetan pada entri masa.</span><span class="sxs-lookup"><span data-stu-id="651a7-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="651a7-225">Medan ini mempunyai dua pilihan, **Pilihan pertama** dan **Pilihan kedua** yang tersedia melalui butang pilihan (butang radio).</span><span class="sxs-lookup"><span data-stu-id="651a7-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="651a7-226">Medan dalam aplikasi berkaitan dengan medan **TestLineString** yang ditambahkan kepada jadual TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="651a7-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="651a7-227">Ambil perhatian bahawa penggunaan kaedah **TSTimesheetCustomField::newFromMetatdata()** adalah untuk memudahkan permulaan sifat medan tersuai: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, dan **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="651a7-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="651a7-228">Anda juga boleh menetapkan parameter secara manual mengikut kemahuan anda.</span><span class="sxs-lookup"><span data-stu-id="651a7-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="651a7-229">Gunakan rantaian perintah pada kaedah buildCustomFieldListForEntry bagi kelas TSTimesheetEntry untuk memasukkan nilai dalam entri lembaran masa</span><span class="sxs-lookup"><span data-stu-id="651a7-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="651a7-230">Kaedah **buildCustomFieldListForEntry** digunakan untuk memasukkan nilai pada baris lembaran masa yang disimpan dalam aplikasi mudah alih.</span><span class="sxs-lookup"><span data-stu-id="651a7-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="651a7-231">Ianya mengambil rekod TSTimesheetTrans sebagai parameter.</span><span class="sxs-lookup"><span data-stu-id="651a7-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="651a7-232">Medan daripada rekod boleh digunakan untuk mengisi dalam nilai medan tersuai dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="651a7-233">Gunakan rantaian perintah pada kelas TSTimesheetEntryService untuk menyimpan entri lembaran masa daripada aplikasi kembali ke pangkalan data</span><span class="sxs-lookup"><span data-stu-id="651a7-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="651a7-234">Untuk menyimpan semula medan tersuai ke pangkalan data dalam penggunaan biasa, anda mesti melanjutkan berbilang kaedah:</span><span class="sxs-lookup"><span data-stu-id="651a7-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="651a7-235">Kaedah **timesheetLineNeedsUpdating** digunakan untuk menentukan sama ada baris rekod telah diubah oleh pengguna dalam aplikasi dan mesti disimpan ke pangkalan data.</span><span class="sxs-lookup"><span data-stu-id="651a7-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="651a7-236">Jika prestasi tidak diambil kira, kaedah ini boleh dipermudahkan supaya ianya sentiasa mengembalikan **benar**.</span><span class="sxs-lookup"><span data-stu-id="651a7-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="651a7-237">Kaedah **populateTimesheetLineFromEntryDuringCreate** dan **populateTimesheetLineFromEntryDuringUpdate** boleh dilanjutkan supaya mereka memasukkan nilai dalam rekod pangkalan data TSTimesheetLine daripada rekod kontrak data TSTimesheetEntry yang disediakan.</span><span class="sxs-lookup"><span data-stu-id="651a7-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="651a7-238">Dalam contoh yang berikut, perhatikan cara pemetaan antara medan pangkalan data dan medan entri dilakukan secara manual melalui kod X++.</span><span class="sxs-lookup"><span data-stu-id="651a7-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="651a7-239">Kaedah **populateTimesheetWeekFromEntry** boleh juga dilanjutkan jika medan tersuai dipetakan ke objek **TSTimesheetEntry** mesti ditulis semula ke jadual pangkalan data TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="651a7-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="651a7-240">Contoh berikut menyimpan nilai **firstOption** atau **secondOption** yang dipilih oleh pengguna ke pangkalan data sebagai nilai rentetan mentah.</span><span class="sxs-lookup"><span data-stu-id="651a7-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="651a7-241">Jika medan pangkalan data adalah medan jenis **Enum**, nilai itu boleh dipetakan secara manual kepada nilai enum dan kemudian disimpan ke medan enum pada jadual pangkalan data.</span><span class="sxs-lookup"><span data-stu-id="651a7-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="651a7-242">Tunjukkan dan simpan medan tersuai dalam bahagian entri pengepala lembaran masa</span><span class="sxs-lookup"><span data-stu-id="651a7-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="651a7-243">Di bawah adalah syot skrin daripada aplikasi mudah alih bagi pengguna yang melihat lembaran masa.</span><span class="sxs-lookup"><span data-stu-id="651a7-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="651a7-244">Butang "Maklumat lanjut" telah dipilih di sudut kanan atas untuk menunjukkan pilihan Lihat butiran lanjut".</span><span class="sxs-lookup"><span data-stu-id="651a7-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Lihat lebih lanjut perintah](media/show-more.png)

<span data-ttu-id="651a7-246">Di bawah adalah syot skrin daripada aplikasi mudah alih menunjukkan “Lebih” bahagian lembaran masa.</span><span class="sxs-lookup"><span data-stu-id="651a7-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="651a7-247">Medan tersuai dipanggil “Kadar penggunaan lembaran masa ini (medan tersuai dikira)” telah ditambah ke bahagian pengepala lembaran masa.</span><span class="sxs-lookup"><span data-stu-id="651a7-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="651a7-248">Nilai dibaca sahaja "0.667" ditetapkan pada medan tersuai.</span><span class="sxs-lookup"><span data-stu-id="651a7-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Lebih banyak bahagian](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="651a7-250">Lanjutkan jadual TSTimesheetTable supaya ianya mempunyai medan tersuai</span><span class="sxs-lookup"><span data-stu-id="651a7-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="651a7-251">Dalam senario biasa, berkemungkinan data untuk medan tersuai dalam bahagian pengepala akan ditarik daripada jadual TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="651a7-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="651a7-252">Walau bagaimanapun, jadual lain boleh digunakan jika data boleh diambil berasaskan pada rekod TSTimesheetTable yang disediakan atau jika ianya tidak mempunyai konteks rekod tertentu (contohnya, jika medan ditetapkan sebagai baca sahaja dalam parameter projek).</span><span class="sxs-lookup"><span data-stu-id="651a7-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="651a7-253">Ambil perhatian bahawa medan tersuai tidak mempunyai sebarang rekod pangkalan data sandaran.</span><span class="sxs-lookup"><span data-stu-id="651a7-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="651a7-254">Ianya boleh dijana secara dinamik berasaskan pada logik X++.</span><span class="sxs-lookup"><span data-stu-id="651a7-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="651a7-255">Contoh berikut menunjukkan pendekatan ini.</span><span class="sxs-lookup"><span data-stu-id="651a7-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="651a7-256">Medan dalam bahagian pengepala sentiasa baca sahaja dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="651a7-257">Gunakan rantaian perintah pada kaedah buildCustomFieldList bagi kelas TSTimesheetSettings untuk menunjukkan medan dalam bahagian pengepala</span><span class="sxs-lookup"><span data-stu-id="651a7-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="651a7-258">Kod ini mengawal tetapan paparan untuk medan dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="651a7-259">Contohnya, ia mengawal jenis medan, label sama ada medan adalah mandatori dan bahagian yang memaparkan medan.</span><span class="sxs-lookup"><span data-stu-id="651a7-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="651a7-260">Contoh berikut menunjukkan nilai dikira dalam bahagian pengepala dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="651a7-261">Gunakan rantaian perintah pada kaedah buildCustomFieldListForHeader bagi kelas TSTimesheetDetails untuk mengisi butiran lembaran masa</span><span class="sxs-lookup"><span data-stu-id="651a7-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="651a7-262">Kaedah **buildCustomFieldListForHeader** digunakan untuk mengisi butiran pengepala lembaran masa dalam aplikasi mudah alih.</span><span class="sxs-lookup"><span data-stu-id="651a7-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="651a7-263">Ianya mengambil rekod TSTimesheetTable sebagai parameter.</span><span class="sxs-lookup"><span data-stu-id="651a7-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="651a7-264">Medan daripada rekod boleh digunakan untuk mengisi dalam nilai medan tersuai dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="651a7-265">Contoh berikut tidak membaca sebarang nilai daripada pangkalan data.</span><span class="sxs-lookup"><span data-stu-id="651a7-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="651a7-266">Sebaliknya, ia menggunakan logik X++ untuk menjana nilai dikira yang kemudiannya ditunjukkan dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="651a7-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="651a7-267">Peluang yang boleh dikonfigurasi/boleh dilanjutkan yang lain</span><span class="sxs-lookup"><span data-stu-id="651a7-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="651a7-268">Menambah pengesahan tambahan untuk aplikasi</span><span class="sxs-lookup"><span data-stu-id="651a7-268">Adding additional validation for the app</span></span>

<span data-ttu-id="651a7-269">Logik sedia ada untuk kefungsian lembaran masa pada peringkat pangkalan data akan masih berfungsi seperti yang dijangkakan.</span><span class="sxs-lookup"><span data-stu-id="651a7-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="651a7-270">Untuk mengganggu penyempurnaan operasi simpan atau serah dan menunjukkan message ralat tertentu, anda boleh menambah **buang ralat("message kepada pengguna")** ke kod melalui lanjutan rantaian perintah.</span><span class="sxs-lookup"><span data-stu-id="651a7-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="651a7-271">Berikut adalah tiga contoh kaedah boleh dilanjutkan yang berguna:</span><span class="sxs-lookup"><span data-stu-id="651a7-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="651a7-272">Jika **validateWrite** pada jadual TSTimesheetLine mengembalikan **palsu** semasa operasi simpan untuk baris lembaran masa, message ralat ditunjukkan dalam aplikasi mudah alih.</span><span class="sxs-lookup"><span data-stu-id="651a7-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="651a7-273">Jika **validateSubmit** pada jadual TSTimesheetTable mengembalikan **palsu** semasa operasi penyerahan dalam aplikasi, message ralat ditunjukkan kepada pengguna.</span><span class="sxs-lookup"><span data-stu-id="651a7-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="651a7-274">Logik yang diisi dalam medan (contohnya, **Sifat Baris**) semasa kaedah **sisip** pada jadual TSTimesheetLine akan masih berjalan.</span><span class="sxs-lookup"><span data-stu-id="651a7-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="651a7-275">Menyembunyi dan menanda medan di luar kotak sebagai baca sahaja melalui konfigurasi</span><span class="sxs-lookup"><span data-stu-id="651a7-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="651a7-276">Daripada parameter projek, anda boleh menjadikan medan di luar kota baca sahaja atau tersembunyi dalam aplikasi mudah alih.</span><span class="sxs-lookup"><span data-stu-id="651a7-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="651a7-277">Tetapkan pilihan dalam bahagian **Lembaran masa mudah alih** pada tab **Lembaran masa** bagi halaman **Parameter pengurusan projek dan perakaunan**.</span><span class="sxs-lookup"><span data-stu-id="651a7-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parameter projek](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="651a7-279">Mengubah aktiviti yang tersedia untuk pemilihan melalui sambungan</span><span class="sxs-lookup"><span data-stu-id="651a7-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="651a7-280">Aktiviti yang tersedia untuk pemilihan projek diisi melalui kaedah **getActivitiesForProject()** dan **getActivityQuery()** dalam kelas **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="651a7-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="651a7-281">Anda boleh menggunakan rantaian perintah untuk mengubah tingkah laku ini bagi memadankan senario perniagaan anda untuk aktiviti yang tersedia bagi pemilihan projek tertentu.</span><span class="sxs-lookup"><span data-stu-id="651a7-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="651a7-282">Memasukkan kategori projek lalai pada entri lembaran masa</span><span class="sxs-lookup"><span data-stu-id="651a7-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="651a7-283">Entri bagi kategori projek lalai pada entri lembaran masa berlaku pada tiga peringkat.</span><span class="sxs-lookup"><span data-stu-id="651a7-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="651a7-284">Anda boleh menggunakan rantaian perintah untuk melanjutkan tingkah laku pada mana-mana atau semua peringkat ini untuk mencapai tingkah laku yang diinginkan.</span><span class="sxs-lookup"><span data-stu-id="651a7-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="651a7-285">Hierarki berikut digunakan:</span><span class="sxs-lookup"><span data-stu-id="651a7-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="651a7-286">Aplikasi cuba meletakkan kategori lalai daripada sumber projek.</span><span class="sxs-lookup"><span data-stu-id="651a7-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="651a7-287">Kategori lalai ditetapkan dalam kaedah **getCurrentUserResource** dan **getDelegatedResourcesForCurrentUser** dalam kelas **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="651a7-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="651a7-288">Jika kategori lalai tidak disediakan pada peringkat sumber projek, aplikasi cuba menariknya daripada aktiviti projek.</span><span class="sxs-lookup"><span data-stu-id="651a7-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="651a7-289">Kategori lalai ditetapkan dalam kaedah **getActivitiesForProject** dalam kelas **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="651a7-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="651a7-290">Jika kategori lalai tidak disediakan pada peringkat aktiviti projek, kategori lalai diambil daripada parameter projek.</span><span class="sxs-lookup"><span data-stu-id="651a7-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="651a7-291">Kategori lalai ditetapkan dalam kaedah **getProjectDetailsbyRule** dalam kelas **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="651a7-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]