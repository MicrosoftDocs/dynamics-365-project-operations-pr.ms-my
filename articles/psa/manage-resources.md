---
title: Urus sumber
description: Topik ini memberikan maklumat tentang cara anda boleh mengurus sumber.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b067f900fa49bba04536b49600dbe80a2167f707
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997837"
---
# <a name="manage-resources"></a><span data-ttu-id="8c6c3-103">Urus sumber</span><span class="sxs-lookup"><span data-stu-id="8c6c3-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8c6c3-104">Dynamics 365 Project Service Automation memasukkan papan pemuka pengurus sumber yang memberikan gambaran keseluruhan visual bagi permintaan dan penggunaan sumber di seluruh organisasi.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="8c6c3-105">Anda boleh menggunaan carta pada papan pemuka ini untuk visualisasikan maklumat berikut:</span><span class="sxs-lookup"><span data-stu-id="8c6c3-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="8c6c3-106">**Permintaan sumber** – Carta **Permintaan Sumber Aktif** menunjukkan sumber yang telah diserahkan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="8c6c3-107">Sumber diagregatkan sama ada melalui peranan atau projek.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="8c6c3-108">**Permintaan sumber belum diserahkan** – Carta **Permintaan Sumber Belum Ditugaskan** menunjukkan semua keperluan sumber yang belum diserahkan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="8c6c3-109">Ia membantu pengurus sumber melihat permintaan yang tidak tegas dan mungkin menyerahkan melalui permintaan sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="8c6c3-110">**Penggunaan boleh bil untuk minggu lepas** – Carta **Penggunaan mengikut Peranan** menunjukkan peratusan penggunaan boleh bil aktual organisasi oleh peranan dengan penggunaan boleh bil sasaran mengikut peranannya.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8c6c3-111">Untuk menjadikan carta **Penggunaan mengikut Peranan** tersedia, cipta kerja yang menjalankan aliran kerja UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="8c6c3-112">Peranan berulang ini berjalan setiap tujuh hari untuk mengira penggunaan boleh bil untuk tujuh hari sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="8c6c3-113">Keputusan diagregatkan mengikut peranan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="8c6c3-114">Urus ahli pasukan projek</span><span class="sxs-lookup"><span data-stu-id="8c6c3-114">Manage project team members</span></span>

<span data-ttu-id="8c6c3-115">Pengurus projek boleh menggunakan papan pemuka pengurus sumber untuk mengurus sumber pada projek.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="8c6c3-116">Contohnya, mereka boleh menambah ahli pasukan secara terus untuk projek dan menempah ahli pasukan untuk mengisi keperluan sumber yang direkod oleh sumber generik.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="8c6c3-117">Tambah ahli pasukan secara terus kepada projek</span><span class="sxs-lookup"><span data-stu-id="8c6c3-117">Add a team member directly to a project</span></span>

<span data-ttu-id="8c6c3-118">Untuk menambah ahli pasukan secara terus kepada projek, pada halaman **Projek**, pada tab **Pasukan**, pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="8c6c3-119">Kotak dialog **Cipta Pantas: Ahli Pasukan Projek** muncul.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="8c6c3-120">Dalam kotak dialog ini, anda boleh menjalankan tugas ini:</span><span class="sxs-lookup"><span data-stu-id="8c6c3-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="8c6c3-121">**Tempah sumber bernama** – Dalam medan **Sumber Boleh Tempah**, pilih nama sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="8c6c3-122">Kemudian pilih sumber, tetapkan tempoh, kemudian pilih kaedah peruntukan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="8c6c3-123">Sumber bernama yang anda pilih ditambah pada projek menggunakan kaedah peruntukan dipilih dan kalendar sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="8c6c3-124">**Tambah sumber generik** – Biarkan medan **Sumber boleh tempah** kosong, kemudian pilih peranan, tetapkan period, dan pilih kaedah peruntukkan pilihan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="8c6c3-125">Sumber generik ditambah pada pasukan sebagai pemegang ruang untuk memegang corak permintaan yang digunakan untuk menempah sumber bernama pada pasukan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="8c6c3-126">Keperluan dibuat mengikut kalendar projek.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="8c6c3-127">**Tambah sumber bernama pada pasukan tanpa menggunakan kapasiti sumber** – Dalam medan **Sumber Boleh Tempah**, pilih sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="8c6c3-128">Kemudian pilih tempoh, dan pilih **Tiada** sebagai kaedah peruntukan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="8c6c3-129">Sumber ditambah pada pasukan, tetapi kapasiti sumber tidak digunakan melalui tempahan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="8c6c3-130">Tempah ahli pasukan untuk mengisi keperluan sumber untuk sumber generik</span><span class="sxs-lookup"><span data-stu-id="8c6c3-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="8c6c3-131">Dalam PSA, anda boleh menempah sumber generik pada pasukan projek, dan boleh menyatakan peranan, kapasiti diperlukan, dan cara kapasiti tersebut diagihkan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="8c6c3-132">Anda boleh menempah sumber bernama untuk menggantikan sumber generik yang mempunyai keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="8c6c3-133">Atirbut ini termasuklah kemahiran yang diperlukan, unit organisasi pilihan, dan sumber pilihan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="8c6c3-134">Ikuti langkah-langkah ini untuk menyatakan kemahiran yang diperlukan pada sumber generik untuk pembangun.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="8c6c3-135">Pada halaman **Projek**, pada tab **Pasukan**, pilih **Baharu** untuk menempah sumber generik.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Sumber generik ditempah pada pasukan](media/Resource-Management-image9.png)

2. <span data-ttu-id="8c6c3-137">Dalam pandangan **Semua Ahli Pasukan**, dalam lajur **Keperluan Sumber**, pilih pautan untuk menambah kemahiran diperlukan untuk sumber generik.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Pautan keperluan](media/Resource-Management-image10.png)

3. <span data-ttu-id="8c6c3-139">Pada halaman **Keperluan Sumber** yang muncul, dalam grid **Kemahiran**, pilih elipsis (**...**) kemudian pilih **Tambah Sifat Keperluan Baharu** untuk menambah kemahiran yang diperlukan untuk pembangun anda.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Tambah perintah Sifat Keperluan Baharu](media/Resource-Management-image11.png)

4. <span data-ttu-id="8c6c3-141">Dalam kotak dialog **Cipta Pantas: Sifat Keperluan** yang muncul, dalam medan **Sifat**, pilih kemahiran diperlukan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="8c6c3-142">Kemudian dalam medan **Nilai Penarafan**, pilih tahap kecekapan untuk kemahiran tersebut.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="8c6c3-143">Akhir sekali, dalam medan **Keperluan Sumber**, tetapkan keperluan untuk sumber sumber daripada unit organiasi atau bahkan sumber bernama.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="8c6c3-144">Apabila anda telah selesai, pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-144">When you've finished, select **Save**.</span></span>

    ![Cari Cepat: kotak dialog Sifat Keperluan](media/Resource-Management-image12.png)

5. <span data-ttu-id="8c6c3-146">Pada halaman **Keperluan Sumber**, pilih **Tempah** untuk memenuhi keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Butang tempah pada halaman Keperluan Sumber](media/Resource-Management-image13.png)

    <span data-ttu-id="8c6c3-148">Anda juga boleh memilih sumber generik dalam grid **Semua Ahli Pasukan** dan kemudian pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Butang tempah di atas grid Semua Ahli Pasukan](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="8c6c3-150">Dalam contoh ini, terdapat 40 jam diperlukan tetapi tiada jam ditempah aktual, kerana sumber generik tidak mempunyai tempahan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="8c6c3-151">Selain itu, tiada jam ditugaskan, kerana sumber generik ditambah terus kepada pasukan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="8c6c3-152">Ia tidak ditambah menggunakan tugasan tugas.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="8c6c3-153">Pada halaman **Menjadualkan Pembantu**, anda boleh menapis sumber tersedia melalui keperluan yang dinyatakan dalam keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="8c6c3-154">Sumber diisih mengikut parameter pengisihan yang dinyatakan dalam papan Jadual.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Halaman Menjadualkan Pembantu](media/Resource-Management-image15.png)

    <span data-ttu-id="8c6c3-156">Berikut adalah beberapa penapis yang sering digunakan:</span><span class="sxs-lookup"><span data-stu-id="8c6c3-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="8c6c3-157">**Ciri berserta dengan penarafan** – Tapis mengikut kemahiran, pensijilan, kualiti sumber lain, selain daripada penarafan kecekapan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="8c6c3-158">**Peranan** – Tapis mengikut peranan lalai yang ditugaskan untuk sumber boleh tempah.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="8c6c3-159">**Unit organisasi** – Tapis sumber boleh tempah mengikut unit organisasi yang ditugaskan mereka.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="8c6c3-160">Jika anda tidak berpuas hati dengan kepurusan carian keperluan awal, anda boleh mengubah kriteria penapis.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="8c6c3-161">Kembangkan anak tetingkap **Pandangan Penapis** di sebelah kiri, kemudian pilih **Cari** untuk mencari sumber tambahan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Anak tetingkap Pandangan Penapis](media/Resource-Management-image16.png)

7. <span data-ttu-id="8c6c3-163">Untuk mengubah cara hasil diisih, pilih **Isih**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Isih perintah](media/Resource-Management-image17.png)

8. <span data-ttu-id="8c6c3-165">Pilih sumber mengikut permintaan yang dinyatakan dalam keperluan, seperti dinyakan di bahagian atas grid.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="8c6c3-166">Anda boleh mengosongkan pilihan sel dalam grid dan membiarkan kapasiti sumber terbuka.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="8c6c3-167">Hanya satu sumber pada satu masa boleh dipilih sebagai ditempah.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="8c6c3-168">Pilih **Tempah** untuk menempah sumber dipilih dan biarkan Papan Jadual dibuka, agar anda boleh memilih sumber tambahan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="8c6c3-169">Secara alternatif, pilih **Tempah & Keluar** untuk menampah sumber dipilih dan tutup Papan Jadual.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Sumber untuk ditempah](media/Resource-Management-image19.png)

    <span data-ttu-id="8c6c3-171">Anda terima pemberitahuan tentang jam ditempah.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="8c6c3-172">Penunjuk permintaan menunjukkan bilangan keperluan tempahan dipenuhi dan bilangan yang dikekalkan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="8c6c3-173">Anda juga boleh melihat berapa banyak kapasiti sumber dipilih telah digunakan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="8c6c3-174">Pilih **Kembangkan** untuk melihat lebih lanjut tentang tempahan sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="8c6c3-175">Kembali ke pandangan **Semua Ahli Pasukan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="8c6c3-176">Dalam grid, sila maklum bahawa sumber generik telah digantikan oleh sumber bernama dan 40 jam disenaraikan sebagai ditempah untuk sumber tersebut.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Gris Semua Ahli Pasukan yang Dikemas Kini](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="8c6c3-178">Tiada jam ditugaskan ditunjukkan kerana ia telah ditempah secara terus pada pasukan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="8c6c3-179">Ia tidak ditempah menggunakan tugasan tugas.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="8c6c3-180">Tugaskan sumber generik untuk tugas dan jana tugasan sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="8c6c3-181">Dalam PSA, anda boleh mencipta tugas, kemudian tugaskan sumber generik kepada mereka.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="8c6c3-182">Dengan cara ini, permintaan sumber boleh diwakili oleh pemegang ruang sementara anda menganggarkan jadual dan angka kewangan anda.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="8c6c3-183">Anda kemudian boleh menjana keperluan sumber untuk sumber generik dan memenuhinya.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="8c6c3-184">Pada halaman **Projek**, pada tab **Jadual**, pilih **Tambah** untuk mencipta tugas.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Tugas baharu dicipta](media/Resource-Management-image21.png)

2. <span data-ttu-id="8c6c3-186">Dalam medan **Sumber**, pilih simbol **Pemilih Sumber**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="8c6c3-187">Pemilih Sumber muncul dan menunjukkan ahli pasukan sedia ada untuk projek.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Pemilih Sumber](media/Resource-Management-image22.png)

3. <span data-ttu-id="8c6c3-189">Masukkan nama sumber generik baharu dan pilih **Cipta**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Nama sumber generik baharu dimasukkan](media/Resource-Management-image23.png)

4. <span data-ttu-id="8c6c3-191">Dalam kotak dialog **Cipta Pantas: Ahli Pasukan Projek** yang muncul, dalam medan **Peranan**, pilih peranan untuk sumber generik.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="8c6c3-192">Dalam medan **Unit Penyumberan**, pilih unit organisasi untuk sumber generik.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="8c6c3-193">Kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-193">Then select **Save**.</span></span>

    ![Kotak dialog Cipta Pantas: Ahli Pasukan Projek](media/Resource-Management-image24.png)

    <span data-ttu-id="8c6c3-195">Ahli pasukan generik kini ditugaskan kepada tugas.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-195">The generic team member is now assigned to the task.</span></span>

    ![Ahli pasukan generik ditugaskan kepada tugas](media/Resource-Management-image25.png)

    <span data-ttu-id="8c6c3-197">Pada tab **Pasukan**, anda akan melihat ahli pasukan generik baharu.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="8c6c3-198">Sila maklum bahawa ia hanya mempunyai jam ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="8c6c3-199">Jam ini adalah jumlah semua tugas yang ditugaskan kepada ahli pasukan generik.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="8c6c3-200">Ahli pasukan generik belum lagi mempunyai jam diperlukan atau keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Ahli pasukan generik pada tab Pasukan](media/Resource-Management-image26.png)

5. <span data-ttu-id="8c6c3-202">Anda kini boleh menugaskan ahli pasukan generik kepada tugas lain dengan menggunakan Pemilih Sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Ahli pasukan generik dalam Pemilih Sumber](media/Resource-Management-image27.png)

    <span data-ttu-id="8c6c3-204">Apabila anda selesai menugaskan sumber generik kepada tugas, anda boleh menjana keperluan sumber untuk sumber generik.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="8c6c3-205">Pada tab **Pasukan**, pilih sumber generik dan kemudian pilih **Jana Keperluan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Jana perintah Keperluan](media/Resource-Management-image28.png)

    <span data-ttu-id="8c6c3-207">Apabila keperluan dijana, ahli pasukan generik akan mempunyai jam diperlukan dan pautan untuk keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Pautan keperluan sumber](media/Resource-Management-image29.png)

    <span data-ttu-id="8c6c3-209">Selepas anda menempah sumber bernama, sumber generik dialih keluardaripada pasukan dan digantikan oleh sumber bernama.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Sumber generik digantikan oleh sumber bernama](media/Resource-Management-image30.png)

    <span data-ttu-id="8c6c3-211">Pada tab **Jadual**, tugasan sumber generik dialih keluar dan digantikan dengan sumber bernama.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Tugasan sumber generik digantikan dengan sumber bernama pada tab Jadual](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="8c6c3-213">Tingkah laku ini berlaku hanya apabila sumber bernama ditempah penuh untuk keperluan sumber generik.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="8c6c3-214">Apabila sama ada sumber bernama menggantikan separuh keperluan sumber generik atau berbilang sumber bernama menggantikan keperluan sumber generik, sumber generik kekal ditugaskan kepada tugas.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="8c6c3-215">Dalam ilustrasi berikut, 80 jam tugas telah dirancang selama tempoh limat hari (16 jam setiap hari selama lima hari) dan ditugaskan kepada sumber generi bernama **Fungsi**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Tugas 80 jam, lima hari ditugaskan kepada sumber generi Fungsi](media/Resource-Management-image32.png)

    <span data-ttu-id="8c6c3-217">Apabila anda menjana keperluan, ia untuk 80 jam selama lima hari.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Keperluan dijana untuk 80 jam selama lima hari](media/Resource-Management-image33.png)

    <span data-ttu-id="8c6c3-219">Disebabkan sumber tersedia hanya bekerja lapan jam setiap hari, dua sumber diperlukan untuk memenuhi keperluan ini.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Sumber kedua](media/Resource-Management-image35.png)

    <span data-ttu-id="8c6c3-221">Pada tab **Pasukan**, anda kini boleh melihat sumber generik tiada jam diperlukan, tetapi jam ditugaskan masih muncul bersama dengan dua sumber bernama yang mengisi keperluan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dua sumber bernama pada tab Pasukan](media/Resource-Management-image36.png)

    <span data-ttu-id="8c6c3-223">Pada tab **Jadual**, sumber generik kekal ditugaskan kepada tugas.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Sumber generik pada tab Jadual](media/Resource-Management-image37.png)

<span data-ttu-id="8c6c3-225">PSA tidak menyokong kedua-dua sumber kepada tugas, kerana tingkah laku tersebut akan kurang menghasilkan jadual boleh diramalkan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="8c6c3-226">Dalam contoh mudah ini, mudah untuk membahagian jam sama rata antara dua sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="8c6c3-227">Nmaun, dalam senario lebih rumit yang melibatkan berbilang tugas dan berbilang sumber, PSA perlu membuat anggapan tentang cara ia perlu memperuntukkan tempahan yang diterima untuk berbilang sumber pada semua berbilang tugas.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="8c6c3-228">Maka, dalam senario ini, pengurus projek bertanggungjawab menghuraikan berbilang tempahan dan menugaskan sebagaimana perlu.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="8c6c3-229">Untuk memperuntukkan tempahan, pengurus projek menugaskan tugasan daripada sumber generik kepada sumber bernama dan menggunakan pandangan **Pelarasan** untuk memastikan peruntukan berfungsi dengan tempahan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="8c6c3-230">Edit keperluan sumber</span><span class="sxs-lookup"><span data-stu-id="8c6c3-230">Edit a resource requirement</span></span>

<span data-ttu-id="8c6c3-231">Selepas keperluan sumber dicipta, pengurus projek atau pengurus sumber mungkin mahu mengedit butiran untuk menghalusi kriteria carian apabila Papan Jadual digunakan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="8c6c3-232">Untuk mengedit keperluan sumber, ikut langkah ini.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="8c6c3-233">Pada halaman **Projek**, pada tab **Pasukan**, pilih pautan ke mana-mana keperluan pada sumber generik.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="8c6c3-234">Pada halaman **Keperluan Sumber** yang muncul, anda boleh mengemas kini beberapa atribut.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="8c6c3-235">Berikut adalah beberapa contoh:</span><span class="sxs-lookup"><span data-stu-id="8c6c3-235">Here are some examples:</span></span>

    - <span data-ttu-id="8c6c3-236">Nama</span><span class="sxs-lookup"><span data-stu-id="8c6c3-236">Name</span></span>
    - <span data-ttu-id="8c6c3-237">Tarikh Dari</span><span class="sxs-lookup"><span data-stu-id="8c6c3-237">From Date</span></span>
    - <span data-ttu-id="8c6c3-238">Tarikh Sehingga</span><span class="sxs-lookup"><span data-stu-id="8c6c3-238">To Date</span></span>
    - <span data-ttu-id="8c6c3-239">Tempoh</span><span class="sxs-lookup"><span data-stu-id="8c6c3-239">Duration</span></span>
    - <span data-ttu-id="8c6c3-240">Jenis Sumber</span><span class="sxs-lookup"><span data-stu-id="8c6c3-240">Resource Type</span></span>

<span data-ttu-id="8c6c3-241">Pada halaman **Keperluan Sumber**, pengurus projek atau pengurus sumber boleh juga mentakrifkan maklumat berikut:</span><span class="sxs-lookup"><span data-stu-id="8c6c3-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="8c6c3-242">Kemahiran</span><span class="sxs-lookup"><span data-stu-id="8c6c3-242">Skills</span></span>
- <span data-ttu-id="8c6c3-243">Peranan</span><span class="sxs-lookup"><span data-stu-id="8c6c3-243">Roles</span></span>
- <span data-ttu-id="8c6c3-244">Keutamaan sumber</span><span class="sxs-lookup"><span data-stu-id="8c6c3-244">Resource preferences</span></span>
- <span data-ttu-id="8c6c3-245">Unit organisasi diutamakan</span><span class="sxs-lookup"><span data-stu-id="8c6c3-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="8c6c3-246">Kemas kini tempahan sumber selepas ia ditempah pada projek</span><span class="sxs-lookup"><span data-stu-id="8c6c3-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="8c6c3-247">Selepas anda menambah sumber generik atau bernama kepada pasukan projek, anda boleh mengubah tempahan sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="8c6c3-248">Pada halaman **Projek**, pada tab **Pasukan**, pilih ahli pasukan kemudian pilih **Kekalkan Tempahan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Papan Jadual dibuka untuk ahli pasukan terpilih](media/Resource-Management-image40.png)

    <span data-ttu-id="8c6c3-250">Papan Jadual muncul dan menunjukkan tempahan ahli pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="8c6c3-251">Kembangkan rekod ahli pasukan untuk melihat jam yang telah ditempah terhadap projek ini dan projek lain yang menggunakan kapasiti ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="8c6c3-252">Pilih dan seret tempahan untuk melanjutkan atau memendekkannya.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="8c6c3-253">Kotak dialog **Cipta Tempaham Sumber** muncul yang membolehkan anda melaraskan tempahan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Kotak dialog Cipta Tempahan Sumber](media/Resource-Management-image41.png)

3. <span data-ttu-id="8c6c3-255">Klik kanan tempahan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-255">Right-click the booking.</span></span> <span data-ttu-id="8c6c3-256">Anda kemudian boleh menggunakan menu pintasan untuk melengkapkan tindakan berikut:</span><span class="sxs-lookup"><span data-stu-id="8c6c3-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="8c6c3-257">Ubah status tempahan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-257">Change the booking status.</span></span>
    - <span data-ttu-id="8c6c3-258">Edit tempahan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-258">Edit the booking.</span></span>
    - <span data-ttu-id="8c6c3-259">Gantikan sumber pada pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="8c6c3-260">Ubah status tempahan</span><span class="sxs-lookup"><span data-stu-id="8c6c3-260">Change the booking status</span></span>

<span data-ttu-id="8c6c3-261">Anda boleh mengubah status tempahan lalai atau tersuai.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-261">You can change any default or custom booking status.</span></span>

![Ubah Perintah Status](media/Resource-Management-image42.png)

<span data-ttu-id="8c6c3-263">Status berikut dimasukkan dalam PSA:</span><span class="sxs-lookup"><span data-stu-id="8c6c3-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="8c6c3-264">**Dibatalkan** – Status ini membatalkan tempahan sumber dan mengosongkan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="8c6c3-265">**Tempah Keras** – Status ini menggunakan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="8c6c3-266">Tempahan lazimnya mempunyai status ini apabila anda membuka **Kekalkan Tempahan** dari grid **Semua Ahli Pasukan** pada halaman **Projek**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="8c6c3-267">**Tempah Lembut** – Status ini menambah sumber kepada pasukan tetapi tidak menggunakan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="8c6c3-268">Ini menunjukkan sumber telah disimpan untuk potensi kerja tetapi masih mempunyai kapasiti jika diperlukan untuk kerja lain.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="8c6c3-269">Dalam pandangan keseluruhan ketersediaan sumber, tempahan lembut mempunyai status berbeza daripada tempahan keras.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="8c6c3-270">**Dicadangkan** – Status ini mewakili cadangan pengurus projek atau pengurus sumber untuk sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="8c6c3-271">Cadangan tidak menggunakan kapasiti sumber dan sumber tidak ditambah pada pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="8c6c3-272">Untuk tempah keras sumber dalam pasukan, pengurus projek mestilah menerima cadangan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="8c6c3-273">Serahkan permintaan sumber</span><span class="sxs-lookup"><span data-stu-id="8c6c3-273">Submit resource requests</span></span>

<span data-ttu-id="8c6c3-274">Permintaan sumber digunakan untuk menjalankan permintaan (keperluan sumber) yang mesti diisi oleh pengurus sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="8c6c3-275">Untuk sumber generik yang telah ada dalam pasukan, anda boleh menyerahkan permintaan sumber secara terus.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="8c6c3-276">Permintaan sumber boleh diisi dalam dua cara:</span><span class="sxs-lookup"><span data-stu-id="8c6c3-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="8c6c3-277">Pengurus sumber mengisi permintaan secara terus.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="8c6c3-278">Dalam situasi ini, sumber generik digantikan oleh tempahan keras yang ada sumber bernama.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="8c6c3-279">Sumber pengurus mencadangkan sumber kepada pengurus projek, dan pengurus projek meluluskan atau menolak cadangan sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="8c6c3-280">Memenuhi keperluan sumber secara terus</span><span class="sxs-lookup"><span data-stu-id="8c6c3-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="8c6c3-281">Apabila keperluan sumber dijana, pengurus projek boleh menyerahkan permintaan sumber untuk sumber generik dengan memilih sumber dan kemudian memilih **Serah Permintaan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Butang Serah Permintaan](media/Resource-Management-image45.png)

<span data-ttu-id="8c6c3-283">Komen tentang sumber boleh diberikan kepada pengurus sumber yang mengisi permintaan tersebut.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="8c6c3-284">Selepas permintaan diserahkan, medan **Status** untuk ahli pasukan diubah kepada **Diserahkan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Memasukkan komen pilihan](media/Resource-Management-image46.png)

<span data-ttu-id="8c6c3-286">Apabila pengurus sumber mengisi keperluan, ahli pasukan generik digantikan dengan sumber bernama dalam grid **Semua Ahli Pasukan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Ahli pasukan generik digantikan dengan sumber bernama dalam grid Semua Ahli Pasukan](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="8c6c3-288">Gunakan cadangan sumber untuk permintaan sumber</span><span class="sxs-lookup"><span data-stu-id="8c6c3-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="8c6c3-289">Daripada menempah terus sumber dalam permintaan sumber, pengurus sumber boleh mencadangkan sumber kepada pengurus projek.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="8c6c3-290">Pengurus projek mungkin menggunakan pilihan ini apabila padanan betul untuk keperluan tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="8c6c3-291">Apabila pengurus sumber mencadangkan sumber, pengurus projek melihat bahawa medan **Status** untuk ahli pasukan generik diubah kepada **Memerlukan Semakan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Status ahli pasukan generik diubah kepada Memerlukan Ulasan](media/Resource-Management-image48.png)

<span data-ttu-id="8c6c3-293">Untuk melihat cadangan sumber berserta dengan visualisasi kesan tempahan cadangan, klik dua kali ahli pasukan yang mempunyai status **Memerlukan Semakan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="8c6c3-294">Kemudian pilih tab **Sumber Dicadangkan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-294">Then select the **Proposed Resources** tab.</span></span>

![Tab Sumber Dicadangkan](media/Resource-Management-image49.png)

<span data-ttu-id="8c6c3-296">Pilih **Terima Semua Cadangan** untuk menerima semua sumber dicadangkan atau **Tolak Semua Cadangan** untuk menolaknya.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="8c6c3-297">Jika anda menerima sumber dicadangkan, ia ditempah keras dalam projek sebagai ahli pasukan dan menggantikan sumber generik.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="8c6c3-298">Anda mesti sama ada menerima atau menolak semua sumber dicadangkan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="8c6c3-299">Anda boleh terima atau menolak separuh.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="8c6c3-300">Gantikan sumber pada pasukan projek</span><span class="sxs-lookup"><span data-stu-id="8c6c3-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="8c6c3-301">Kadangkala, pengurus projek mestilah menggantikan ahli pasukan ditempah dalam projek.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="8c6c3-302">Pada halaman **Projek**, pada tab **Pasukan**, pilih sumber yang perlu diganti, kemudian pilih **Kekalkan Tempahan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="8c6c3-303">Kembangkan sumber untuk melihat projek yang ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Sumber dikembangkan untuk menunjukkan projek yang ditugaskan](media/Resource-Management-image50.png)

3. <span data-ttu-id="8c6c3-305">Klik kanan projek, kemudian pilih **Gantikan Sumber**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="8c6c3-306">Jika anda tahu sumber yang anda mahu gantikan untuk sumber semasa, pilih atau taip nama, kemudian pilih **Tugaskan semula**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Menentukan sumber gantian](media/Resource-Management-image51.png)

    <span data-ttu-id="8c6c3-308">Secara alternatif, ikuti langkah-langkah ini untuk mencari sumber:</span><span class="sxs-lookup"><span data-stu-id="8c6c3-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="8c6c3-309">Pilih **Cari Penggantian**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-309">Select **Find Substitution**.</span></span>

        ![Mencari sumber gantian](media/Resource-Management-image52.png)

        <span data-ttu-id="8c6c3-311">Pembantu Jadual mengembalikan senarai gantian tersedia.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="8c6c3-312">Dalam Pembantu Jadual, anda boleh menapis sumber tersedia untuk mencari gantian sesuai.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Senarai gantian tersedia](media/Resource-Management-image53.png)

    2. <span data-ttu-id="8c6c3-314">Untuk menggantikan sumber, pilih sumber yang anda mahu, dan pilih **Gantikan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Sumber gantian dipilih](media/Resource-Management-image54.png)

    <span data-ttu-id="8c6c3-316">Tempahan dan tugasan digantikan dengan sumber baharu.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Tempahan dan tugasan digantikan dengan sumber baharu](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="8c6c3-318">Sesuaikan tempahan dan tugasan ahli pasukan</span><span class="sxs-lookup"><span data-stu-id="8c6c3-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="8c6c3-319">Untuk ahli pasukan, tempahan dan tugasan tidak begitu digandingkan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="8c6c3-320">Dengan kata lain, sumber boleh mempunyai tugasan tapi tidak tempahan, atau mereka boleh ada tempahan tetapi tidak tugasan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="8c6c3-321">Tempahan dan tugasan hendaklah sejajar, agar sumber ada kapasiti komited untuk melaksanakan tugasan tugas.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="8c6c3-322">Namun, tempahan mungkin berdasarkan ketersediaan, dan pemasaan tugas mungkin berubah seiring projek diteruskan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="8c6c3-323">Makan, gandingan longgar tempahan dan tugasan memberikan kefleksibelan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="8c6c3-324">PSA mempunyai tab **Pelarasan** yang membolehkan pengurus projek menyesuaikan tempahan dan tugasan ahli pasukan mereka untuk pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Tab Penyelarasan](media/Resource-Management-image56.png)

<span data-ttu-id="8c6c3-326">Tab **Penyelarasan** menunjukkan tempahan dan tugasan sehingga ke tahap tugasan tugas individu untuk setiap ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="8c6c3-327">Ia menunjukkan jam dalam sel yang mewakili tempoh masa dari bulan sehingga hari.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="8c6c3-328">Tab juga menunjukkan keseluruhan jumlah bersih untuk projek, berserta lajur jumlah.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="8c6c3-329">Untuk setiap sumber, tab mengira perbezaan antara tempahan dan gulung atas ahli pasukan bagi tugasan tugas ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="8c6c3-330">Perbezaan ini hendaklah 0 (sifar).</span><span class="sxs-lookup"><span data-stu-id="8c6c3-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="8c6c3-331">Dengan kata lain, tiada perbezaan antara tempahan dan tugasan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="8c6c3-332">Perbezaan diwarnai dan dibayangi untuk menarik perhatian kepada dua keadaan:</span><span class="sxs-lookup"><span data-stu-id="8c6c3-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="8c6c3-333">**Kekurangan tempahan** – Kekurangan tempahan berlaku apabila sumber ada lebih tugasan berbanding tempahan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="8c6c3-334">Disebabkan kapasiti ini telah disimpan, pengurus projek mungkin mahu membetulkan keadaan ini dengan melanjutkan tempahan sumber untuk menampung desifit.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="8c6c3-335">**Tempahan berlebihan** – Tempahan berlebihan berlaku apabila sumber telah ditempah kepada projek tetapi belum ditugaskan kepada tugas.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="8c6c3-336">Keadaan ini mungkin boleh diterima dalam situasi di mana sumber ditempah untuk projek sebelum tugasan tugas berlaku.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="8c6c3-337">Namun, dalam situasi lain, sumber tidak dirandang ditugaskan kepada tugas.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="8c6c3-338">Dalam kes ini, pengurus projek perlu mempertimbangkan untuk membatalkan penempahan sumber, supaya kapasiti boleh digunakan untuk projek lain.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="8c6c3-339">Dalam situasi tertentu, apabila anda melihat masa pada tahap lebih tingi daripada tahap hari (contohnya, tahap bulan), anda mungkin melihat perbezaan bersih sifar untuk sumber (dengan kata lain, tempahan = tugasan).</span><span class="sxs-lookup"><span data-stu-id="8c6c3-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="8c6c3-340">Namun, jika anda melihat masa pada tahap minggu, anda mungkin melihat tugasan sifat jam dan tempahan 40 jam dalam minggu pertama, tetapi tugasan 40 jam dan tempahan sifar jam dalam minggu kedua.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="8c6c3-341">Keseluruhannya, tempahan dan tugasan diselaraskan, tetapi berbeza dari satu minggu ke minggu seterusnya.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="8c6c3-342">Apabila anda melihat masa pada tahap lebih tinggi, sel dalam tab **Penyelarasan** mempunyai penunjuk untuk memaklumkan anda terdapat perbezaan pada tahap lebih rendah.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="8c6c3-343">Dengan mengklik dua kali dalam sel, anda boleh zum dekat untuk melihat perbezaan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="8c6c3-344">Anda kemudian boleh klik kanan untuk zum jauh. Dengan memilih sumber dan menggunakan kawalan **Perbezaan seterusnya** pada bar alat grid, anda boleh pergi ke perbezaan seterusnya antara tempahan dan tugasan untuk sumber tersebut.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="8c6c3-345">Anda kemudian boleh menggunakan kawalan **Perbezaan sebelumnya** untuk kembali.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="8c6c3-346">Anda juga boleh mematikan penunjuk perbezaan dan tingkah laku navigasi di bawah **Tetapan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Penunjuk perbezaan](media/Resource-Management-image57.png)

<span data-ttu-id="8c6c3-348">Jika anda ada tugasan tugas untuk sumber tetapi tiada tempahan, pada halaman **Projek**, pada tab **Penyelarasan**, pilih kekurangan tempahan dan kemudian pilih **Lanjutkan Tempahan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="8c6c3-349">Kotak dialog **Lanjutkan Tempahan** muncul dan menunjukkan tempahan yang diperlukan untuk menyelesaikan kekurangan sumber.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="8c6c3-350">Ia juga menunjukkan tempahan sedia ada sumber dalam semua projek atau entiti boleh dijadual lain.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="8c6c3-351">Jika anda pilih **OK** untuk mencipta tempahan untuk sumber, tanpa mengira ketersediaan sumber tersebut, anda mungkin menyebabkan tempahan berlebihan.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Kotak dialog Lanjutkan Tempahan](media/Resource-Management-image58.png)

<span data-ttu-id="8c6c3-353">Pengurus projek atau pengurus sumber kemudian boleh menggunakan Papan Jadual untuk mengurus sebarang situasi di mana sumber ditempah berlebihan di luar kapasitinya.</span><span class="sxs-lookup"><span data-stu-id="8c6c3-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]