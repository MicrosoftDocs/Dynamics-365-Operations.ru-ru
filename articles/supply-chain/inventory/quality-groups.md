---
title: Группы контроля качества номенклатуры
description: В этой теме описывается, как использовать и создавать группы контроля качества номенклатур, чтобы логически сгруппировать продукты, чтобы они могли быть назначены для сопоставлений контроля качества для автоматического создания заказов контроля качества.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022260"
---
# <a name="item-quality-groups"></a><span data-ttu-id="c4754-103">Группы контроля качества номенклатуры</span><span class="sxs-lookup"><span data-stu-id="c4754-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4754-104">Группа контроля качества определяет общие требования к проверке номенклатур.</span><span class="sxs-lookup"><span data-stu-id="c4754-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="c4754-105">В этой теме описывается, как использовать и создавать группы контроля качества номенклатур, чтобы логически сгруппировать продукты, чтобы они могли быть назначены для сопоставлений контроля качества для автоматического создания заказов контроля качества.</span><span class="sxs-lookup"><span data-stu-id="c4754-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="c4754-106">Для настройки, изменения и просмотра номенклатур, назначенных группе контроля качества, или групп контроля качества, назначенных номенклатуре, перейдите **Управление запасами \> Настройка \> Группы контроля качества**.</span><span class="sxs-lookup"><span data-stu-id="c4754-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="c4754-107">После определения требованиям к испытанию на странице **Группы проверки** вы можете определить правила для автоматического создания заказов для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="c4754-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="c4754-108">Для того, чтобы упростить процесс, вы не определяете правила для индивидуальных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="c4754-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="c4754-109">Вместо этого вы определяете правила для группы качества путем использования страницы **Сопоставления контроля качества**.</span><span class="sxs-lookup"><span data-stu-id="c4754-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="c4754-110">Пример группы контроля качества номенклатуры</span><span class="sxs-lookup"><span data-stu-id="c4754-110">Example of an item quality group</span></span>

<span data-ttu-id="c4754-111">Производственная компания приобретает различные виды сырья, для которых действуют одинаковые требования по проверке во время входного контроля.</span><span class="sxs-lookup"><span data-stu-id="c4754-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="c4754-112">Поэтому компания определяет группу качества, и после этого назначает коды номенклатур, которые связаны с сырьем, для этой группы.</span><span class="sxs-lookup"><span data-stu-id="c4754-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="c4754-113">Позднее компания покупает новый тип сырья, которое имеет такие же требования к испытаниям.</span><span class="sxs-lookup"><span data-stu-id="c4754-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="c4754-114">Вместо настройки новых требований к испытаниям для нового материала компания добавляет код номенклатуры для нового материала к существующей группе качества.</span><span class="sxs-lookup"><span data-stu-id="c4754-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="c4754-115">Эта же компания также производит номенклатуры, которые имеют одинаковые требования в отношении производственных испытаний и одинаковые требования в отношении проведения испытаний перед отгрузкой.</span><span class="sxs-lookup"><span data-stu-id="c4754-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="c4754-116">Поэтому компания определяет две дополнительные группы контроля качества и назначает соответствующие коды номенклатур каждой группе.</span><span class="sxs-lookup"><span data-stu-id="c4754-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="c4754-117">Создание группы контроля качества</span><span class="sxs-lookup"><span data-stu-id="c4754-117">Create a quality group</span></span>

<span data-ttu-id="c4754-118">Чтобы создать группу контроля качества, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c4754-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="c4754-119">Перейдите в раздел **Управление запасами \> Настройка \> Контроль качества \> Группы контроля качества**.</span><span class="sxs-lookup"><span data-stu-id="c4754-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="c4754-120">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="c4754-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c4754-121">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="c4754-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c4754-122">**Группа контроля качества** — введите уникальный код или имя группы контроля качества.</span><span class="sxs-lookup"><span data-stu-id="c4754-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="c4754-123">**Описание** — введите подробное описание группы контроля качества.</span><span class="sxs-lookup"><span data-stu-id="c4754-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="c4754-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c4754-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="c4754-125">Добавление номенклатур в группу контроля качества вручную</span><span class="sxs-lookup"><span data-stu-id="c4754-125">Manually add items to a quality group</span></span>

<span data-ttu-id="c4754-126">Чтобы вручную добавить номенклатуры в группу качества, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c4754-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="c4754-127">Перейдите в раздел **Управление запасами \> Настройка \> Контроль качества \> Группы контроля качества**.</span><span class="sxs-lookup"><span data-stu-id="c4754-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="c4754-128">Выберите группу контроля качества, в которую необходимо добавить номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c4754-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="c4754-129">В области действий выберите **Номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="c4754-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="c4754-130">На странице **Номенклатуры в группе контроля качества** в области действий выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="c4754-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c4754-131">Затем для новой строки задайте в поле **Код номенклатуры** код номенклатуры, которую требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="c4754-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="c4754-132">Повторите предыдущий шаг для каждой дополнительной номенклатуры, которую необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="c4754-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="c4754-133">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="c4754-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="c4754-134">Добавление нескольких номенклатур в группу контроля качества</span><span class="sxs-lookup"><span data-stu-id="c4754-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="c4754-135">Чтобы добавить несколько номенклатур в группу качества, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c4754-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="c4754-136">Перейдите в раздел **Управление запасами \> Настройка \> Контроль качества \> Группы контроля качества**.</span><span class="sxs-lookup"><span data-stu-id="c4754-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="c4754-137">Создайте или выберите группу контроля качества, в которую необходимо добавить номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c4754-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="c4754-138">В области действий выберите **Добавить номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="c4754-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="c4754-139">В диалоговом окне **Запрос** введите критерии фильтрации для добавляемых номенклатур.</span><span class="sxs-lookup"><span data-stu-id="c4754-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="c4754-140">Например, можно отфильтровать все номенклатуры в определенной группе номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c4754-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="c4754-141">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c4754-141">Select **OK**.</span></span>
1. <span data-ttu-id="c4754-142">В диалоговом окне **Добавление номенклатур** в сетке отображаются все номенклатуры, соответствующие запросу.</span><span class="sxs-lookup"><span data-stu-id="c4754-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="c4754-143">Проверка результатов.</span><span class="sxs-lookup"><span data-stu-id="c4754-143">Review the results.</span></span>

    <span data-ttu-id="c4754-144">Если требуется внести изменения, выберите **Выбрать**, чтобы вернуться в диалоговое окно **Запрос**, и настройте запрос.</span><span class="sxs-lookup"><span data-stu-id="c4754-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="c4754-145">Когда в результаты включены все номенклатуры, которые требуется добавить, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c4754-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="c4754-146">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c4754-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="c4754-147">Связывание номенклатуры с группой контроля качества вручную</span><span class="sxs-lookup"><span data-stu-id="c4754-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="c4754-148">Чтобы вручную связать номенклатуру с группой качества, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c4754-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="c4754-149">Перейдите в раздел **Управление запасами \> Настройка \> Контроль качества \> Группы контроля качества номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="c4754-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="c4754-150">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="c4754-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c4754-151">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="c4754-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c4754-152">**Код номенклатуры** — выберите код добавляемой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c4754-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="c4754-153">**Группа контроля качества** — выберите группу контроля качества, которая будет назначена номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="c4754-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="c4754-154">Повторите предыдущий шаг для всех дополнительных комбинаций номенклатуры и группы контроля качества, которые необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="c4754-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="c4754-155">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="c4754-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="c4754-156">Добавление группы контроля качества со страницы выпущенных продуктов вручную</span><span class="sxs-lookup"><span data-stu-id="c4754-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="c4754-157">Чтобы вручную добавить группу контроля качества со страницы **Выпущенные продукты**, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c4754-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="c4754-158">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="c4754-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="c4754-159">Выберите продукты, которым необходимо назначить группу контроля качества.</span><span class="sxs-lookup"><span data-stu-id="c4754-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="c4754-160">На панели действий на вкладке **Управление складскими запасами** в группе **Качество** выберите **Группы контроля качества номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="c4754-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="c4754-161">На странице **Номенклатуры в группе контроля качества** в области действий выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="c4754-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c4754-162">Затем для новой строки задайте поле **Группа контроля качества** для группы контроля качества, которую необходимо назначить продукту.</span><span class="sxs-lookup"><span data-stu-id="c4754-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="c4754-163">Повторите предыдущий шаг для каждой дополнительной группы контроля качества, которую необходимо назначить продукту.</span><span class="sxs-lookup"><span data-stu-id="c4754-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="c4754-164">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="c4754-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4754-165">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c4754-165">Additional resources</span></span>

- [<span data-ttu-id="c4754-166">Инструменты проверки управления качеством</span><span class="sxs-lookup"><span data-stu-id="c4754-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="c4754-167">Проверки управления качеством</span><span class="sxs-lookup"><span data-stu-id="c4754-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="c4754-168">Группы проверки контроля качества</span><span class="sxs-lookup"><span data-stu-id="c4754-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="c4754-169">Переменные управления качеством</span><span class="sxs-lookup"><span data-stu-id="c4754-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="c4754-170">Сопоставления контроля качества</span><span class="sxs-lookup"><span data-stu-id="c4754-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
