---
title: Создание и обработка несоответствий
description: В этой теме рассматривается порядок управления несоответствием на основании существующего заказа контроля качества.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956214"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="ac64b-103">Создание и обработка несоответствий</span><span class="sxs-lookup"><span data-stu-id="ac64b-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac64b-104">В этой теме рассматривается порядок управления несоответствием на основании существующего заказа контроля качества.</span><span class="sxs-lookup"><span data-stu-id="ac64b-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="ac64b-105">Обычно управление несоответствиями выполняется сотрудником отдела контроля качества.</span><span class="sxs-lookup"><span data-stu-id="ac64b-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="ac64b-106">В качестве обязательного условия должен быть доступен заказ для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="ac64b-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="ac64b-107">(Дополнительные сведения о порядке создания заказа для контроля качества см. в разделе [Контроль качества товаров](inspect-quality-goods.md).)</span><span class="sxs-lookup"><span data-stu-id="ac64b-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="ac64b-108">Прежде чем пользователь сможет обработать утверждение несоответствия, работнику необходимо назначить его в поле **Сотрудник** на странице **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="ac64b-109">Кроме того, прежде чем пользователь сможет использовать примечания к документу, параметр **Разрешить работу с документами** должен быть задан как *Да* в параметрах пользователя.</span><span class="sxs-lookup"><span data-stu-id="ac64b-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="ac64b-110">Создание несоответствия</span><span class="sxs-lookup"><span data-stu-id="ac64b-110">Create a nonconformance</span></span>

<span data-ttu-id="ac64b-111">Чтобы создать несоответствие, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="ac64b-112">Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="ac64b-113">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="ac64b-114">В диалоговом окне **Создание несоответствия** в поле **Тип проблемы** выберите тип проблемы, которая была обнаружена во время процесса проверки.</span><span class="sxs-lookup"><span data-stu-id="ac64b-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="ac64b-115">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="ac64b-116">Утверждение или отклонение несоответствия</span><span class="sxs-lookup"><span data-stu-id="ac64b-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="ac64b-117">Для утверждения или отклонения несоответствия выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="ac64b-118">Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="ac64b-119">В списке выберите несоответствие, которое необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac64b-120">Исправление можно добавлять только для несоответствий, которые утверждены.</span><span class="sxs-lookup"><span data-stu-id="ac64b-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="ac64b-121">В области действий выберите **Функции \> Утвердить несоответствие** для утверждения несоответствия или **Функции \> Отклонить несоответствие** для отклонения.</span><span class="sxs-lookup"><span data-stu-id="ac64b-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="ac64b-122">Утвержденные несоответствия можно связать с [соответствующими операциями](../quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="ac64b-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="ac64b-123">Таким образом можно записать работу, которая выполняется как часть обработки несоответствия и обработку исправления.</span><span class="sxs-lookup"><span data-stu-id="ac64b-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="ac64b-124">Выводится запрос на подтверждение выбора.</span><span class="sxs-lookup"><span data-stu-id="ac64b-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="ac64b-125">Выберите **Да** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="ac64b-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="ac64b-126">Добавьте операции и другие сведения в несоответствия</span><span class="sxs-lookup"><span data-stu-id="ac64b-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="ac64b-127">После создания несоответствия можно начать добавлять связанные операции и указывать дополнительные сведения об этих операциях.</span><span class="sxs-lookup"><span data-stu-id="ac64b-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="ac64b-128">Связанные операции можно добавлять только для несоответствий, которые утверждены.</span><span class="sxs-lookup"><span data-stu-id="ac64b-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="ac64b-129">Кроме основной информации, в операцию можно добавить следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="ac64b-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="ac64b-130">**Номенклатуры** — можно создать список номенклатур, которые потребляются для выполнения исправления.</span><span class="sxs-lookup"><span data-stu-id="ac64b-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="ac64b-131">Например, номенклатуры могут быть продуктами, необходимыми для ремонта оборудования или составляющими, которые необходимы для повторной работы готового продукта.</span><span class="sxs-lookup"><span data-stu-id="ac64b-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="ac64b-132">**Расходы по контролю качества** — можно создать список накладных расходов, которые были понесены или выставляются во внешние источники.</span><span class="sxs-lookup"><span data-stu-id="ac64b-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="ac64b-133">**Табель учета рабочего времени** — можно создать журнал времени, которое каждый работник тратит на операцию.</span><span class="sxs-lookup"><span data-stu-id="ac64b-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="ac64b-134">Остальные параметры необязательные.</span><span class="sxs-lookup"><span data-stu-id="ac64b-134">The remaining settings are optional.</span></span> <span data-ttu-id="ac64b-135">Затраты для каждой номенклатуры, расходы по контролю качества и табели учета рабочего времени суммируются и отображаются в операции.</span><span class="sxs-lookup"><span data-stu-id="ac64b-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="ac64b-136">Невозможно непосредственно изменить поле **Затраты** для операции.</span><span class="sxs-lookup"><span data-stu-id="ac64b-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="ac64b-137">Создание операции для несоответствия</span><span class="sxs-lookup"><span data-stu-id="ac64b-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="ac64b-138">Чтобы создать операцию для несоответствия, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="ac64b-139">Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="ac64b-140">В списке выберите несоответствие, которое необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac64b-141">Операции можно добавлять или обновлять только для несоответствий, которые утверждены.</span><span class="sxs-lookup"><span data-stu-id="ac64b-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="ac64b-142">В области операций выберите **Связанные операции**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="ac64b-143">На странице **Связанные операции** в области действий выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="ac64b-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ac64b-144">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="ac64b-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ac64b-145">**Операция** — выберите код операции, которая будет выполнена для несоответствия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="ac64b-146">**Причина** — введите подробное описание, объясняющее, почему необходимо выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="ac64b-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="ac64b-147">**Заказ на продажу** — если выбран код операции, связанный с типом заказа на продажу, выберите заказ на продажу, с которым связана выполняемая операция.</span><span class="sxs-lookup"><span data-stu-id="ac64b-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="ac64b-148">**Заказ на покупку** — если выбран код операции, связанный с типом заказа на покупку, выберите заказ на покупку, с которым связана выполняемая операция.</span><span class="sxs-lookup"><span data-stu-id="ac64b-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="ac64b-149">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="ac64b-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="ac64b-150">Добавление номенклатур в операцию</span><span class="sxs-lookup"><span data-stu-id="ac64b-150">Add items to an operation</span></span>

<span data-ttu-id="ac64b-151">Чтобы добавить номенклатуры в операцию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="ac64b-152">Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="ac64b-153">В списке выберите несоответствие, которое необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac64b-154">Операции можно добавлять или обновлять только для несоответствий, которые утверждены.</span><span class="sxs-lookup"><span data-stu-id="ac64b-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="ac64b-155">В области операций выберите **Связанные операции**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="ac64b-156">На странице **Связанные операции** выберите операцию, в которую необходимо добавить номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="ac64b-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="ac64b-157">В области действий выберите **Номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="ac64b-158">На странице **Связанные операции** в области действий выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="ac64b-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ac64b-159">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="ac64b-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="ac64b-160">**Код номенклатуры** — выберите продукт, который будет потреблен как часть выбранной операции.</span><span class="sxs-lookup"><span data-stu-id="ac64b-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="ac64b-161">**Количество** — введите количество номенклатур, которое будет потреблено.</span><span class="sxs-lookup"><span data-stu-id="ac64b-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac64b-162">Затраты для номенклатуры можно просмотреть в поле **Затраты** на вкладке **Общее**. Отображаемые затраты поступают из затрат, настроенных на странице **Выпущенный продукт**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="ac64b-163">Затраты не могут быть обновлены непосредственно на странице **Номенклатура связанной операции**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="ac64b-164">Затраты на все номенклатуры, добавленные на странице **Номенклатуры связанной операции**, автоматически добавляются в поле **Затраты** на странице **Связанные операции**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="ac64b-165">Повторите предыдущий шаг для каждой дополнительной номенклатуры, которую необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="ac64b-166">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="ac64b-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="ac64b-167">Добавление расходов по контролю качества в операцию</span><span class="sxs-lookup"><span data-stu-id="ac64b-167">Add quality charges to an operation</span></span>

<span data-ttu-id="ac64b-168">Чтобы добавить расходы по контролю качества в операцию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="ac64b-169">Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="ac64b-170">В списке выберите несоответствие, которое необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac64b-171">Операции можно добавлять или обновлять только для несоответствий, которые утверждены.</span><span class="sxs-lookup"><span data-stu-id="ac64b-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="ac64b-172">В области операций выберите **Связанные операции**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="ac64b-173">На странице **Связанные операции** выберите операцию, в которую необходимо добавить расходы по контролю качества.</span><span class="sxs-lookup"><span data-stu-id="ac64b-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="ac64b-174">В области операций выберите **Расходы по контролю качества**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="ac64b-175">На странице **Расходы связанной операции** в области действий выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="ac64b-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ac64b-176">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="ac64b-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ac64b-177">**Код накладных расходов** — выберите расходы по контролю качества, которые требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="ac64b-178">**Описание** — введите подробное описание накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="ac64b-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="ac64b-179">**Значение расходов** — вводится сумма накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="ac64b-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="ac64b-180">Повторите предыдущий шаг для каждого дополнительного накладного расхода, который необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="ac64b-181">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="ac64b-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="ac64b-182">Сумма в поле **Значение накладных расходов** автоматически суммируется для всех расходов по контролю качества и добавляется ко всем другим суммам в поле **Затраты** на странице **Связанные операции**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="ac64b-183">Создание табеля учета рабочего времени для операции</span><span class="sxs-lookup"><span data-stu-id="ac64b-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="ac64b-184">Чтобы добавить табель учета рабочего времени в операцию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="ac64b-185">Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="ac64b-186">В списке выберите несоответствие, которое необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac64b-187">Операции можно добавлять или обновлять только для несоответствий, которые утверждены.</span><span class="sxs-lookup"><span data-stu-id="ac64b-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="ac64b-188">В области операций выберите **Связанные операции**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="ac64b-189">На странице **Связанные операции** выберите операцию, в которую необходимо добавить табель учета рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="ac64b-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="ac64b-190">В области действий выберите **Табель учета рабочего времени**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="ac64b-191">На странице **Табели учета рабочего времени связанной операции** в области действий выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="ac64b-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ac64b-192">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="ac64b-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ac64b-193">**Дата** — укажите дату завершения работы.</span><span class="sxs-lookup"><span data-stu-id="ac64b-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="ac64b-194">По умолчанию для этого поля задана текущая дата.</span><span class="sxs-lookup"><span data-stu-id="ac64b-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="ac64b-195">**Работник** — выберите работника, который выполнил работу.</span><span class="sxs-lookup"><span data-stu-id="ac64b-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="ac64b-196">По умолчанию в этом поле задается работник, назначенный текущему пользователю.</span><span class="sxs-lookup"><span data-stu-id="ac64b-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="ac64b-197">**Часы работы** — ввод количества часов, отработанных по выбранной операции.</span><span class="sxs-lookup"><span data-stu-id="ac64b-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="ac64b-198">**Выставлено накладных** — этот флажок устанавливается, если по времени была выставлена оплата для клиента или поставщика по накладной.</span><span class="sxs-lookup"><span data-stu-id="ac64b-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac64b-199">Можно просмотреть затраты в поле **Затраты** на вкладке **Общее**. Затраты рассчитываются с использованием ставки, определенной на странице **Параметры управления запасами**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="ac64b-200">Повторите предыдущий шаг для каждого дополнительного табеля учета рабочего времени, который необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="ac64b-201">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="ac64b-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="ac64b-202">Сумма в поле **Затраты** суммируется для всех строк табеля учета рабочего времени и добавляется ко всем другим суммам в поле **Затраты** на странице **Связанные операции**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="ac64b-203">Добавление исправления для несоответствия</span><span class="sxs-lookup"><span data-stu-id="ac64b-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="ac64b-204">Чтобы добавить исправление для несоответствия, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="ac64b-205">Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="ac64b-206">В списке выберите несоответствие, которое необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac64b-207">Исправление можно добавлять только для несоответствий, которые утверждены.</span><span class="sxs-lookup"><span data-stu-id="ac64b-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="ac64b-208">В области действий выберите **Корректировки**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="ac64b-209">На странице **Корректировки** на панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="ac64b-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ac64b-210">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="ac64b-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ac64b-211">**Диагностика** — выберите тип диагностики, определяющий тип создаваемой корректировки.</span><span class="sxs-lookup"><span data-stu-id="ac64b-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="ac64b-212">**Работник** — выберите лицо, несущее ответственность за корректировку.</span><span class="sxs-lookup"><span data-stu-id="ac64b-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="ac64b-213">**Приоритет корректировки** — выберите параметр, чтобы указать приоритет корректировки (*низкий*, *нормальный* или *высокий*).</span><span class="sxs-lookup"><span data-stu-id="ac64b-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="ac64b-214">**Запрошенная дата** — введите дату запроса корректирующего действия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="ac64b-215">**Спланированная дата** — введите дату, в которую ожидается завершение корректировки.</span><span class="sxs-lookup"><span data-stu-id="ac64b-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="ac64b-216">**Краткосрочное решение** — установите этот флажок, если корректирующее действие исправляет несоответствие только на короткое время.</span><span class="sxs-lookup"><span data-stu-id="ac64b-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="ac64b-217">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="ac64b-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="ac64b-218">Отметка корректировки как завершенной</span><span class="sxs-lookup"><span data-stu-id="ac64b-218">Mark a correction as completed</span></span>

<span data-ttu-id="ac64b-219">Чтобы отметить корректировку несоответствия как завершенную, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="ac64b-220">Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="ac64b-221">В списке выберите несоответствие, которое необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac64b-222">Исправление можно добавлять только для несоответствий, которые утверждены.</span><span class="sxs-lookup"><span data-stu-id="ac64b-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="ac64b-223">В области действий выберите **Корректировки**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="ac64b-224">На странице **Корректировки** в сетке выберите корректировку, которое необходимо отметить как завершенную.</span><span class="sxs-lookup"><span data-stu-id="ac64b-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="ac64b-225">На панели операций выберите **Отметить как завершенное**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="ac64b-226">Выводится запрос на подтверждение выбора.</span><span class="sxs-lookup"><span data-stu-id="ac64b-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="ac64b-227">Нажмите **ОК**, чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-227">Select **OK** to continue.</span></span> <span data-ttu-id="ac64b-228">В поле **Дата и время завершения** устанавливается значение текущих даты и времени, и выбран флажок **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="ac64b-229">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ac64b-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="ac64b-230">Повторное открытие завершенной корректировки</span><span class="sxs-lookup"><span data-stu-id="ac64b-230">Reopen a completed correction</span></span>

<span data-ttu-id="ac64b-231">Чтобы поврано открыть завершенную корректировку, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="ac64b-232">Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="ac64b-233">В списке выберите несоответствие, которое необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="ac64b-234">В области действий выберите **Корректировки**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="ac64b-235">На странице **Корректировки** в сетке выберите корректировку, которую необходимо снова открыть.</span><span class="sxs-lookup"><span data-stu-id="ac64b-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="ac64b-236">В области действий выберите **Открыть повторно**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="ac64b-237">Выводится запрос на подтверждение выбора.</span><span class="sxs-lookup"><span data-stu-id="ac64b-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="ac64b-238">Нажмите **ОК**, чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="ac64b-238">Select **OK** to continue.</span></span> <span data-ttu-id="ac64b-239">Значение удаляется из поля **Дата и время завершения**, флажок **Завершено** снимается.</span><span class="sxs-lookup"><span data-stu-id="ac64b-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="ac64b-240">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ac64b-240">Close the page.</span></span>

<span data-ttu-id="ac64b-241">Теперь можно внести дополнительные изменения или обновления для корректировки.</span><span class="sxs-lookup"><span data-stu-id="ac64b-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="ac64b-242">После завершения можно снова отметить корректировку как завершенную.</span><span class="sxs-lookup"><span data-stu-id="ac64b-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="ac64b-243">Закрытие несоответствия</span><span class="sxs-lookup"><span data-stu-id="ac64b-243">Close a nonconformance</span></span>

<span data-ttu-id="ac64b-244">Чтобы закрыть несоответствие, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac64b-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="ac64b-245">Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Заказы для контроля качества**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="ac64b-246">Выберите заказа для контроля качества в сетке.</span><span class="sxs-lookup"><span data-stu-id="ac64b-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="ac64b-247">В области действий выберите **Запросы \> Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="ac64b-248">На странице **Несоответствии** выберите целевое несоответствие в сетке.</span><span class="sxs-lookup"><span data-stu-id="ac64b-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="ac64b-249">В области действий выберите **Функции \> Закрыть несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="ac64b-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="ac64b-250">Выводится запрос на подтверждение выбора.</span><span class="sxs-lookup"><span data-stu-id="ac64b-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="ac64b-251">Выберите **Да** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="ac64b-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="ac64b-252">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="ac64b-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac64b-253">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ac64b-253">Additional resources</span></span>

- [<span data-ttu-id="ac64b-254">Обзор управления качеством</span><span class="sxs-lookup"><span data-stu-id="ac64b-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="ac64b-255">Включение управления качеством и несоответствием</span><span class="sxs-lookup"><span data-stu-id="ac64b-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="ac64b-256">Работники, ответственные за утверждение несоответствий</span><span class="sxs-lookup"><span data-stu-id="ac64b-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="ac64b-257">Карантинные зоны для несоответствий</span><span class="sxs-lookup"><span data-stu-id="ac64b-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="ac64b-258">Типы диагностики для несоответствий</span><span class="sxs-lookup"><span data-stu-id="ac64b-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="ac64b-259">Расходы по контролю качества для несоответствий</span><span class="sxs-lookup"><span data-stu-id="ac64b-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="ac64b-260">Операции для несоответствий</span><span class="sxs-lookup"><span data-stu-id="ac64b-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="ac64b-261">Управление качеством для складских процессов</span><span class="sxs-lookup"><span data-stu-id="ac64b-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
