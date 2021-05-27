---
title: Прикрепление налоговых кодов TDS к налоговым группам TDS и определение формулы для расчета TDS
description: В этой теме объясняется, как настроить налоговые группы для налога, удержанного в источнике (TDS), и привязать налоговые коды TDS к налоговым группам TDS. Чтобы рассчитать TDS для налоговой группы TDS, необходимо определить формулу для приложенных к ней кодов налога TDS.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023547"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="d60aa-104">Прикрепление налоговых кодов TDS к налоговым группам TDS и определение формулы для расчета TDS</span><span class="sxs-lookup"><span data-stu-id="d60aa-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d60aa-105">В этой теме объясняется, как настроить налоговые группы для налога, удержанного в источнике (TDS), и привязать налоговые коды TDS к налоговым группам TDS.</span><span class="sxs-lookup"><span data-stu-id="d60aa-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="d60aa-106">Чтобы рассчитать TDS для налоговой группы TDS, необходимо определить формулу для приложенных к ней кодов налога TDS.</span><span class="sxs-lookup"><span data-stu-id="d60aa-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="d60aa-107">Выполните следующие действия, чтобы настроить налоговую группу TDS, приложите к ней налоговые коды TDS и определите формулу для расчета TDS.</span><span class="sxs-lookup"><span data-stu-id="d60aa-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="d60aa-108">Перейдите в раздел **Налог \> Косвенные налоги \> Подоходный налог \> Группы подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="d60aa-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="d60aa-109">[![Страница групп подоходного налога](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="d60aa-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="d60aa-110">В области действий выберите **Создать**, чтобы создать группу подоходного налога для TDS, и введите требуемые сведения.</span><span class="sxs-lookup"><span data-stu-id="d60aa-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="d60aa-111">В поле **Тип налога** выберите **TDS**.</span><span class="sxs-lookup"><span data-stu-id="d60aa-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="d60aa-112">На экспресс-вкладке **Настройка** выберите **Добавить**, чтобы создать новую строку.</span><span class="sxs-lookup"><span data-stu-id="d60aa-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="d60aa-113">В поле **Код подоходного налога** выберите код налога TDS для налоговой группы TDS.</span><span class="sxs-lookup"><span data-stu-id="d60aa-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="d60aa-114">В поле **Имя подоходного налога** отображается имя налогового кода (TDS), а в поле **Значение** указано значение.</span><span class="sxs-lookup"><span data-stu-id="d60aa-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="d60aa-115">Чтобы игнорировать предел порогового значения и предельный порог исключений, которые определены для компонента налога TDS, присоединенного к налоговому коду TDS в проводках TDS, установите флажок **Пропустить порог**.</span><span class="sxs-lookup"><span data-stu-id="d60aa-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="d60aa-116">Чтобы запретить расчет налоговой группы в проводках, установите флажок **Освобождается**.</span><span class="sxs-lookup"><span data-stu-id="d60aa-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="d60aa-117">В области действий выберите **Конструктор**, чтобы открыть конструктор формул, чтобы можно было определить формулу для расчета TDS для налоговой группы TDS.</span><span class="sxs-lookup"><span data-stu-id="d60aa-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="d60aa-118">На странице **Конструктор** на вкладке **Налоги** отображаются налоговые коды TDS, которые были выбраны для налоговой группы TDS.</span><span class="sxs-lookup"><span data-stu-id="d60aa-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="d60aa-119">[![Страница конструктора](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="d60aa-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="d60aa-120">На вкладке **Расчет** нажмите сочетание клавиш **ALT+N**, чтобы создать строку.</span><span class="sxs-lookup"><span data-stu-id="d60aa-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="d60aa-121">Поле **Код** содержит автоматически созданный код приоритета для расчета TDS.</span><span class="sxs-lookup"><span data-stu-id="d60aa-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="d60aa-122">В поле **Налоговый код** выберите налоговый код TDS, для которого определяется формула.</span><span class="sxs-lookup"><span data-stu-id="d60aa-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="d60aa-123">Все налоговые коды TDS, которые были выбраны для налоговой группы TDS, доступны для выбора в этом поле.</span><span class="sxs-lookup"><span data-stu-id="d60aa-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="d60aa-124">В поле **Налогооблагаемая база** выберите основу для расчета TDS:</span><span class="sxs-lookup"><span data-stu-id="d60aa-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="d60aa-125">**Валовая сумма** — расчет TDS на основе валовой суммы проводки (то есть, суммы накладной) с помощью расчетного выражения, которое определено для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="d60aa-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="d60aa-126">**Без валовой суммы** — расчет TDS на основе расчетного выражения, определенного для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="d60aa-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d60aa-127">Поле **Налогооблагаемая база** не может иметь значение **Без валовой суммы** для налогового кода TDS с кодом приоритета **1**.</span><span class="sxs-lookup"><span data-stu-id="d60aa-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="d60aa-128">Расчет TDS базируется на формуле, которая определена в поле **Выражение для расчета** для каждого налогового кода, присоединенного к налоговой группе TDS.</span><span class="sxs-lookup"><span data-stu-id="d60aa-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="d60aa-129">Выберите знак "плюс" (**+**), минус (**-**), знак умножения (**\**_) или знак деления (_*/**), чтобы ввести выражение для расчета для выбранного налогового кода в формате TDS в поле **Выражение для расчета**.</span><span class="sxs-lookup"><span data-stu-id="d60aa-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d60aa-130">Для налогового кода TDS с кодом приоритета **1** не может быть определено выражение для расчета.</span><span class="sxs-lookup"><span data-stu-id="d60aa-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="d60aa-131">Для определения выражения для расчета для налогового кода в формате TDS в поле **Выражение для расчета** добавьте налоговые коды TDS, доступные на вкладке **Налоги**. Чтобы добавить налоговые коды TDS в поле **Выражение для расчета**, можно использовать любой из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="d60aa-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="d60aa-132">Перетащите требуемый налоговый код из вкладки **Налоги** в поле **Выражение для расчета**.</span><span class="sxs-lookup"><span data-stu-id="d60aa-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="d60aa-133">Дважды коснитесь (или дважды щелкните) требуемый налоговый код на вкладке **Налоги**.</span><span class="sxs-lookup"><span data-stu-id="d60aa-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="d60aa-134">Выберите и удерживайте (или щелкните правой кнопкой мыши) требуемый налоговый код на вкладке **Налоги**, а затем выберите **Добавить налоговый код**.</span><span class="sxs-lookup"><span data-stu-id="d60aa-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d60aa-135">Вставьте выражение для расчета перед каждым налоговым кодом TDS.</span><span class="sxs-lookup"><span data-stu-id="d60aa-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="d60aa-136">Налоговые коды TDS, добавленные в выражение для расчета, отображаются в квадратных скобках (\[...\]).</span><span class="sxs-lookup"><span data-stu-id="d60aa-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="d60aa-137">Чтобы удалить выражение для расчета, которое определено для налогового кода в поле **Выражение для расчета**, нажмите кнопку **C**.</span><span class="sxs-lookup"><span data-stu-id="d60aa-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="d60aa-138">Чтобы удалить запись на вкладке **Расчет**, выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="d60aa-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="d60aa-139">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d60aa-139">Close the page.</span></span>
