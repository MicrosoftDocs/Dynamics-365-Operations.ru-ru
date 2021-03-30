---
title: Настройка должностных лиц (Россия)
description: В этой теме поясняется, как производится настройка должностных лиц в Microsoft Dynamics 365 Finance в России.
author: ShylaThompson
manager: AnnBe
ms.date: 07/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OfficialsTable_RU
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 64d127364b279f24bbdbebfaf53afa2348ffd8d0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219843"
---
# <a name="set-up-officials-russia"></a><span data-ttu-id="b727c-103">Настройка должностных лиц (Россия)</span><span class="sxs-lookup"><span data-stu-id="b727c-103">Set up officials (Russia)</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="b727c-104">В этой теме описывается порядок настройки должностных лиц в России, которые занимаются созданием транспортных накладных и заказ-нарядов, а также фигурирующих в различных отчетах.</span><span class="sxs-lookup"><span data-stu-id="b727c-104">This topic explains how to set up officials in Russia who generate transportation invoices and job tickets and who are involved in various reports.</span></span>

## <a name="set-up-officials-who-generate-transportation-invoices-and-job-tickets"></a><span data-ttu-id="b727c-105">Настройка должностных лиц, которые занимаются созданием транспортных накладных и заказ-нарядов</span><span class="sxs-lookup"><span data-stu-id="b727c-105">Set up officials who generate transportation invoices and job tickets</span></span>

<span data-ttu-id="b727c-106">Эта процедура относится к функциям в модуле **Управление запасами**.</span><span class="sxs-lookup"><span data-stu-id="b727c-106">This procedure applies to features in the **Inventory management** module.</span></span> <span data-ttu-id="b727c-107">К функциям в модуле [Обзор управления складом](../../supply-chain/warehousing/warehouse-management-overview.md) она неприменима.</span><span class="sxs-lookup"><span data-stu-id="b727c-107">It doesn't apply to features in [Warehouse management overview](../../supply-chain/warehousing/warehouse-management-overview.md).</span></span>

<span data-ttu-id="b727c-108">Используйте страницу **Должностные лица** для настройки должностных лиц, которые участвуют в транспортировке грузов.</span><span class="sxs-lookup"><span data-stu-id="b727c-108">Use the **Officials** page to set up the officials who are involved in the transportation of cargo.</span></span> <span data-ttu-id="b727c-109">Можно выбрать должностных лиц, ответственных за внутрихолдинговые и межхолдинговые проводки.</span><span class="sxs-lookup"><span data-stu-id="b727c-109">You can select the officials who are responsible for intercompany and intracompany transactions.</span></span>

<span data-ttu-id="b727c-110">Необходимо настроить записи для должностных лиц, ответственных за транспортировку с обеих сторон проводок.</span><span class="sxs-lookup"><span data-stu-id="b727c-110">You must set up records for the officials who are responsible for transportation on both sides of the transactions.</span></span> <span data-ttu-id="b727c-111">Следовательно, необходимо настроить записи для должностных лиц и на стороне клиента или поставщика, и на стороне поставщика.</span><span class="sxs-lookup"><span data-stu-id="b727c-111">Therefore, you must set up records for the officials both on the customer or vendor side, and on the company side.</span></span> <span data-ttu-id="b727c-112">Эти данные требуются при создании и печати транспортной накладной и заказ-наряда на основе транспортной накладной.</span><span class="sxs-lookup"><span data-stu-id="b727c-112">This information is required when you generate and print a transportation invoice and a job ticket that are based on a bill of lading.</span></span>

1. <span data-ttu-id="b727c-113">Выберите **Управление организацией** \> **Настройка** \> **Контакты** \> **Должностные лица**.</span><span class="sxs-lookup"><span data-stu-id="b727c-113">Select **Organization administration** \> **Setup** \> **Contacts** \> **Officials**.</span></span>
2. <span data-ttu-id="b727c-114">Для настройки записей должностных лиц, ответственных за транспортировку исходящих документов для клиентов, на вкладке **Заказы на продажу** выберите **Накладная** или **Накладная - Кредит-нота**, а затем выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b727c-114">To set up records for the officials who are responsible for transportation on outgoing documents for customers, on the **Sales orders** tab, select either **Invoice** or **Invoice - credit-note**, and then follow these steps:</span></span>

    1. <span data-ttu-id="b727c-115">Создайте запись для должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-115">Create a record for an official.</span></span> <span data-ttu-id="b727c-116">В поле **Должность** выберите **Отв. за перевозку от клиента**.</span><span class="sxs-lookup"><span data-stu-id="b727c-116">In the **Position** field, select **Customer transportation responsible**.</span></span>
    2. <span data-ttu-id="b727c-117">В поле **Имя** выберите контактное лицо клиента, ответственное за транспортировку.</span><span class="sxs-lookup"><span data-stu-id="b727c-117">In the **Name** field, select the customer contact who is responsible for transportation.</span></span>
    3. <span data-ttu-id="b727c-118">Создайте запись для должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-118">Create a record for an official.</span></span> <span data-ttu-id="b727c-119">В поле **Должность** выберите **Отв. за перевозку**.</span><span class="sxs-lookup"><span data-stu-id="b727c-119">In the **Position** field, select **Transportation responsible**.</span></span>
    4. <span data-ttu-id="b727c-120">В поле **Имя** выберите контактное лицо компании, ответственное за транспортировку.</span><span class="sxs-lookup"><span data-stu-id="b727c-120">In the **Name** field, select the company contact who is responsible for transportation.</span></span>

3. <span data-ttu-id="b727c-121">Для настройки записей должностных лиц, ответственных за транспортировку входящих документов для поставщиков, на вкладке **Заказы на покупку** выберите **Накладная** или **Накладная - Кредит-нота**, а затем выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b727c-121">To set up records for the officials who are responsible for transportation on incoming documents for vendors, on the **Purchase orders** tab, select either **Invoice** or **Invoice - credit-note**, and then follow these steps:</span></span>

    1. <span data-ttu-id="b727c-122">Создайте запись для должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-122">Create a record for an official.</span></span> <span data-ttu-id="b727c-123">В поле **Должность** выберите **Отв. за перевозку от поставщика**.</span><span class="sxs-lookup"><span data-stu-id="b727c-123">In the **Position** field, select **Vendor transportation responsible**.</span></span>
    2. <span data-ttu-id="b727c-124">В поле **Имя** выберите контактное лицо поставщика, ответственное за транспортировку.</span><span class="sxs-lookup"><span data-stu-id="b727c-124">In the **Name** field, select the vendor contact who is responsible for transportation.</span></span>
    3. <span data-ttu-id="b727c-125">Создайте запись для должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-125">Create a record for an official.</span></span> <span data-ttu-id="b727c-126">В поле **Должность** выберите **Отв. за перевозку**.</span><span class="sxs-lookup"><span data-stu-id="b727c-126">In the **Position** field, select **Transportation responsible**.</span></span>
    4. <span data-ttu-id="b727c-127">В поле **Имя** выберите контактное лицо компании, ответственное за транспортировку.</span><span class="sxs-lookup"><span data-stu-id="b727c-127">In the **Name** field, select the company contact who is responsible for transportation.</span></span>

4. <span data-ttu-id="b727c-128">Для настройки записей должностных лиц, ответственных за транспортировку по входящим или исходящим складским документам, на вкладке **Учет МЦ** выберите либо **Накладная на отпуск по заказу на продажу (М-15)** или **Накладная на отпуск по заказу на перемещение (М-15)**, а затем выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b727c-128">To set up records for the officials who are responsible for transportation on incoming or outgoing warehouse documents, on the **Inventory item management** tab, select either **Issue slip for sales order (M-15)** or **Issue slip for transfer order (M-15)**, and then follow these steps:</span></span>

    1. <span data-ttu-id="b727c-129">Создайте запись для должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-129">Create a record for an official.</span></span> <span data-ttu-id="b727c-130">В поле **Должность** выберите **Отв. за перевозку от клиента**.</span><span class="sxs-lookup"><span data-stu-id="b727c-130">In the **Position** field, select **Customer transportation responsible**.</span></span>
    2. <span data-ttu-id="b727c-131">В поле **Имя** выберите контактное лицо клиента, ответственное за транспортировку.</span><span class="sxs-lookup"><span data-stu-id="b727c-131">In the **Name** field, select the customer contact who is responsible for transportation.</span></span>
    3. <span data-ttu-id="b727c-132">Создайте запись для должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-132">Create a record for an official.</span></span> <span data-ttu-id="b727c-133">В поле **Должность** выберите **Отв. за перевозку**.</span><span class="sxs-lookup"><span data-stu-id="b727c-133">In the **Position** field, select **Transportation responsible**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b727c-134">Настроить запись для должностного лица **Отв. за перевозку** можно только при выборе варианта **Накладная на отпуск по заказу на перемещение (М-15)**.</span><span class="sxs-lookup"><span data-stu-id="b727c-134">You can set up a record for a **Transportation responsible** official only if you selected **Issue slip for transfer order (M-15)**.</span></span>

    4. <span data-ttu-id="b727c-135">В поле **Имя** выберите контактное лицо компании, ответственное за транспортировку.</span><span class="sxs-lookup"><span data-stu-id="b727c-135">In the **Name** field, select the company contact who is responsible for transportation.</span></span>

## <a name="set-up-officials-for-the-counting-list-inv-5-report"></a><span data-ttu-id="b727c-136">Настройка должностных лиц для отчета "Инвентаризационная опись (ИНВ-5)"</span><span class="sxs-lookup"><span data-stu-id="b727c-136">Set up officials for the counting list (INV-5) report</span></span>

<span data-ttu-id="b727c-137">Эта процедура относится к функциям в модуле **Управление запасами**.</span><span class="sxs-lookup"><span data-stu-id="b727c-137">This procedure applies to features in the **Inventory management** module.</span></span> <span data-ttu-id="b727c-138">К функциям в модуле [Обзор управления складом](../../supply-chain/warehousing/warehouse-management-overview.md) она неприменима.</span><span class="sxs-lookup"><span data-stu-id="b727c-138">It doesn't apply to features in [Warehouse management overview](../../supply-chain/warehousing/warehouse-management-overview.md).</span></span>

<span data-ttu-id="b727c-139">Используйте страницу **Должностные лица** для настройки должностных лиц, участвующих в процессе инвентаризации для отчета **Инвентаризационная опись (ИНВ-5)**.</span><span class="sxs-lookup"><span data-stu-id="b727c-139">Use the **Officials** page to set up the officials who are involved in the item counting process for the **Counting list (INV-5)** report.</span></span>

1. <span data-ttu-id="b727c-140">Выберите **Управление организацией** \> **Настройка** \> **Контакты** \> **Должностные лица**.</span><span class="sxs-lookup"><span data-stu-id="b727c-140">Select **Organization administration** \> **Setup** \> **Contacts** \> **Officials**.</span></span>
2. <span data-ttu-id="b727c-141">На вкладке **Запасы** в левой области выберите **Инвентаризационная опись (ИНВ-5)**.</span><span class="sxs-lookup"><span data-stu-id="b727c-141">On the **Inventory** tab, in the left pane, select **Counting list (INV-5)**.</span></span>
3. <span data-ttu-id="b727c-142">В правой области нажмите CTRL+N, чтобы создать должностное лицо.</span><span class="sxs-lookup"><span data-stu-id="b727c-142">In the right pane, press Ctrl+N to create an official.</span></span>
4. <span data-ttu-id="b727c-143">В поле **Должность** выберите назначение должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-143">In the **Position** field, select the designation for the official.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b727c-144">Вы можете указать не более одного председателя и одного ответственного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-144">You can set up a maximum of one chair and one person who is in charge.</span></span>

5. <span data-ttu-id="b727c-145">В поле **Имя** введите имя должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-145">In the **Name** field, enter the name of the official.</span></span>
6. <span data-ttu-id="b727c-146">В поле **Название должности** выберите для должностного лица псевдоним для названия должности.</span><span class="sxs-lookup"><span data-stu-id="b727c-146">In the **Job title** field, select the alias for the job title of the official.</span></span>

## <a name="set-up-officials-for-the-counting-act-inv-6-report"></a><span data-ttu-id="b727c-147">Настройка должностных лиц для отчета "Акт инвентаризации ИНВ-6"</span><span class="sxs-lookup"><span data-stu-id="b727c-147">Set up officials for the Counting act INV-6 report</span></span>

<span data-ttu-id="b727c-148">Эта процедура относится к функциям в модуле **Управление запасами**.</span><span class="sxs-lookup"><span data-stu-id="b727c-148">This procedure applies to features in the **Inventory management** module.</span></span> <span data-ttu-id="b727c-149">К функциям в модуле [Обзор управления складом](../../supply-chain/warehousing/warehouse-management-overview.md) она неприменима.</span><span class="sxs-lookup"><span data-stu-id="b727c-149">It doesn't apply to features in [Warehouse management overview](../../supply-chain/warehousing/warehouse-management-overview.md).</span></span>

<span data-ttu-id="b727c-150">Используйте страницу **Должностные лица** для настройки должностных лиц для отчета **Акт инвентаризации ИНВ-6**.</span><span class="sxs-lookup"><span data-stu-id="b727c-150">Use the **Officials** page to set up officials for the **Counting act (INV-6)** report.</span></span> <span data-ttu-id="b727c-151">Можно определить должностных лиц компании, участвующих в процессе инвентаризации номенклатур для отчета.</span><span class="sxs-lookup"><span data-stu-id="b727c-151">You can identify the company officials who are involved in the item counting process for the report.</span></span>

1. <span data-ttu-id="b727c-152">Выберите **Управление организацией** \> **Настройка** \> **Контакты** \> **Должностные лица**.</span><span class="sxs-lookup"><span data-stu-id="b727c-152">Select **Organization administration** \> **Setup** \> **Contacts** \> **Officials**.</span></span>
2. <span data-ttu-id="b727c-153">На вкладке **Запасы** в левой области выберите **Акт инвентаризации (ИНВ-6)**.</span><span class="sxs-lookup"><span data-stu-id="b727c-153">On the **Inventory** tab, in the left pane, select **Counting act (INV-6)**.</span></span>
3. <span data-ttu-id="b727c-154">Выберите **Добавить**, чтобы создать должностное лицо для отчета **Акт инвентаризации (ИНВ-6)**.</span><span class="sxs-lookup"><span data-stu-id="b727c-154">Select **Add** to create an official for the **Counting act (INV-6)** report.</span></span>
4. <span data-ttu-id="b727c-155">В поле **Должность** выберите назначение должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-155">In the **Position** field, select the designation for the official.</span></span>
5. <span data-ttu-id="b727c-156">В поле **Имя** введите имя должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-156">In the **Name** field, enter the name of the official.</span></span>
6. <span data-ttu-id="b727c-157">В поле **Название должности** выберите название должности должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-157">In the **Job title** field, select the job title of the official.</span></span>

## <a name="set-up-officials-for-the-nvfa-statement-of-writing-off-no-mb-8-report"></a><span data-ttu-id="b727c-158">Настройка должностных лиц для отчета "Акт на списание МОС (номер</span><span class="sxs-lookup"><span data-stu-id="b727c-158">Set up officials for the NVFA statement of writing-off (No.</span></span> <span data-ttu-id="b727c-159">МБ-8)"</span><span class="sxs-lookup"><span data-stu-id="b727c-159">MB-8) report</span></span>

<span data-ttu-id="b727c-160">Используйте страницу **Должностные лица** для настройки членов и председателя комиссии, ответственных за отчет "Акт на списание МОС (номер</span><span class="sxs-lookup"><span data-stu-id="b727c-160">Use the **Officials** page to set up the members and chair of the commission that is responsible for the NVFA Statement of writing-off (No.</span></span> <span data-ttu-id="b727c-161">МБ-8)".</span><span class="sxs-lookup"><span data-stu-id="b727c-161">MB-8) report.</span></span>

1. <span data-ttu-id="b727c-162">Выберите **Управление организацией** \> **Настройка** \> **Контакты** \> **Должностные лица**.</span><span class="sxs-lookup"><span data-stu-id="b727c-162">Select **Organization administration** \> **Setup** \> **Contacts** \> **Officials**.</span></span>
2. <span data-ttu-id="b727c-163">На вкладке **Основные средства** выберите **Акт на списание МОС (МБ-8)**.</span><span class="sxs-lookup"><span data-stu-id="b727c-163">On the **Fixed assets** tab, select **NVFA Statement of writing-off (No. MB-8)**.</span></span>
3. <span data-ttu-id="b727c-164">Выберите **Добавить**, чтобы создать запись.</span><span class="sxs-lookup"><span data-stu-id="b727c-164">Select **Add** to create a record.</span></span>
4. <span data-ttu-id="b727c-165">В поле **Должность** выберите **Член комиссии** или **Председатель комиссии**, чтобы указать, является выбранный сотрудник членом комиссии или ее председателем.</span><span class="sxs-lookup"><span data-stu-id="b727c-165">In the **Position** field, select **Member** or **Chairman** to indicate whether the selected employee is a commission member or the chair.</span></span> <span data-ttu-id="b727c-166">В качестве председателя можно выбрать только одного сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b727c-166">You can select only one employee as the chair.</span></span>
5. <span data-ttu-id="b727c-167">В поле **Имя** выберите имя сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b727c-167">In the **Name** field, select the name of the employee.</span></span>

## <a name="set-up-officials-for-the-issue-slip-m-15-report"></a><span data-ttu-id="b727c-168">Настройка должностных лиц для отчета "Накладная на отпуск (М-15)"</span><span class="sxs-lookup"><span data-stu-id="b727c-168">Set up officials for the Issue slip (M-15) report</span></span>

<span data-ttu-id="b727c-169">Используйте страницу **Отгрузка** для настройки должностных лиц для отчета **Накладная на отпуск (М-15)**, создаваемого для ответственного хранения.</span><span class="sxs-lookup"><span data-stu-id="b727c-169">Use the **Shipment** page to set up officials for the **Issue slip (M-15)** report that is generated for bailment.</span></span>

1. <span data-ttu-id="b727c-170">Выберите **Управление запасами** \> **Периодические операции** \> **Заказы на перемещение**.</span><span class="sxs-lookup"><span data-stu-id="b727c-170">Select **Inventory management** \> **Periodic** \> **Transfer orders**.</span></span>
2. <span data-ttu-id="b727c-171">В форме **Заказы на перемещение** выберите заказ на перемещение для ответственного хранения.</span><span class="sxs-lookup"><span data-stu-id="b727c-171">On the **Transfer orders** form, select a transfer order for bailment.</span></span>
3. <span data-ttu-id="b727c-172">Выберите **Разноска** \> **Отгрузить заказ на перемещение**.</span><span class="sxs-lookup"><span data-stu-id="b727c-172">Select **Posting** \> **Ship transfer order**.</span></span>
4. <span data-ttu-id="b727c-173">На странице **Отгрузка** на вкладке **Должностные лица** выберите название должности контактного должностного лица.</span><span class="sxs-lookup"><span data-stu-id="b727c-173">On the **Shipment** page, on the **Officials** tab, select the job title of the contact official.</span></span>
5. <span data-ttu-id="b727c-174">Выберите **ОК**, чтобы разнести отгрузки заказа на перемещение с информацией о должностных лицах.</span><span class="sxs-lookup"><span data-stu-id="b727c-174">Select **OK** to post the transfer order shipments that include information about officials.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b727c-175">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b727c-175">Additional resources</span></span>

- [<span data-ttu-id="b727c-176">Настройка подписывающих лиц для печатных форм</span><span class="sxs-lookup"><span data-stu-id="b727c-176">Set up signers for print forms</span></span>](emea-set-up-signers-for-printing-forms.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]