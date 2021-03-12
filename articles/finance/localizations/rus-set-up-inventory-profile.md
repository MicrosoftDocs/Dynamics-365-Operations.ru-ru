---
title: Настройка профиля учета
description: В данном разделе содержится общая информация о настройке профиля учета.
author: v-nadyuz
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: kfend
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 62ea28da11cd3480f501ae6ba1e9767ad97a4b48
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997471"
---
# <a name="set-up-an-inventory-profile"></a><span data-ttu-id="19065-103">Настройка профиля учета</span><span class="sxs-lookup"><span data-stu-id="19065-103">Set up an inventory profile</span></span> 
[!include [banner](../includes/banner.md)]

## <a name="create-an-inventory-profile"></a><span data-ttu-id="19065-104">Создание профиля учета</span><span class="sxs-lookup"><span data-stu-id="19065-104">Create an inventory profile</span></span>

1. <span data-ttu-id="19065-105">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Аналитики** \> **Профили учета**.</span><span class="sxs-lookup"><span data-stu-id="19065-105">Go to **Inventory management** \> **Setup** \> **Dimensions** \> **Inventory profiles**.</span></span>
2. <span data-ttu-id="19065-106">Выберите **Создать**, чтобы создать новый профиль учета.</span><span class="sxs-lookup"><span data-stu-id="19065-106">Select **New** to create a new inventory profile.</span></span>
3. <span data-ttu-id="19065-107">В поле **Профиль учета** введите идентификатор профиля учета.</span><span class="sxs-lookup"><span data-stu-id="19065-107">In the **Inventory profile** field, enter the identifier of the inventory profile.</span></span>
4. <span data-ttu-id="19065-108">В поле **Имя** введите описание профиля учета.</span><span class="sxs-lookup"><span data-stu-id="19065-108">In the **Name** field, enter a description of the inventory profile.</span></span>
5. <span data-ttu-id="19065-109">На Экспресс-вкладке **настройки** в поле **вид деятельности** выберите вид деятельности для профиля учета.</span><span class="sxs-lookup"><span data-stu-id="19065-109">On the **Setup** FastTab, in the **Kind of activity** field, select the kind of activity for the inventory profile.</span></span>
6. <span data-ttu-id="19065-110">Установите для параметра **Не подбирать** значение **Да**, если профиль учета не обязательно должен участвовать в автоматическом выборе профилей учета из запасов в наличии при создании строк заказа на продажу посредством выбора пункта **создать строки**.</span><span class="sxs-lookup"><span data-stu-id="19065-110">Set the **Don't match** option to **Yes** if the inventory profile doesn't have to participate in the automatic selection of inventory profiles from on-hand inventory when you create sales order lines by selecting **Create lines**.</span></span>
7. <span data-ttu-id="19065-111">На экспресс-вкладке **Приоритет подбора** используйте кнопки **вверх** и **вниз**, чтобы задать порядок автоматического выбора профилей учета при создании строк заказа на продажу, выбрав **Добавить строки**.</span><span class="sxs-lookup"><span data-stu-id="19065-111">On the **Matching priority** FastTab, use the **Up** and **Down** buttons to set the order that inventory profiles are automatically selected in when you create sales order lines by selecting **Add lines**.</span></span>

    ![Страница профилей учета, экспресс-вкладка "Приоритет подбора"](media/1_Inventory_profiles.png)

8. <span data-ttu-id="19065-113">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="19065-113">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="19065-114">Удалить профиль учета можно только в том случае, если в нем нет сальдо.</span><span class="sxs-lookup"><span data-stu-id="19065-114">You can delete an inventory profile only if there are no balances on it.</span></span>

## <a name="set-up-compatible-inventory-profiles"></a><span data-ttu-id="19065-115">Настройка совместимых профилей учета</span><span class="sxs-lookup"><span data-stu-id="19065-115">Set up compatible inventory profiles</span></span>

1. <span data-ttu-id="19065-116">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Аналитики** \> **Профили учета**.</span><span class="sxs-lookup"><span data-stu-id="19065-116">Go to **Inventory management** \> **Setup** \> **Dimensions** \> **Inventory profiles**.</span></span>
2. <span data-ttu-id="19065-117">Выберите профиль учета, для которого необходимо настроить совместимые профили учета.</span><span class="sxs-lookup"><span data-stu-id="19065-117">Select the inventory profile that you want to set up compatible inventory profiles for.</span></span>

    - <span data-ttu-id="19065-118">На экспресс-вкладке **совместимые профили учета** в списке **Совместимые** отображаются профили учета, совместимые с выбранным профилем учета.</span><span class="sxs-lookup"><span data-stu-id="19065-118">On the **Compatible inventory profiles** FastTab, the **Compatible** list shows the inventory profiles that are compatible with the selected inventory profile.</span></span> <span data-ttu-id="19065-119">В списке **Прочие** перечислены другие профили учета.</span><span class="sxs-lookup"><span data-stu-id="19065-119">The **Other** list shows other inventory profiles.</span></span>

3. <span data-ttu-id="19065-120">Настройка списка совместимых профилей учета.</span><span class="sxs-lookup"><span data-stu-id="19065-120">Set up the list of compatible inventory profiles.</span></span>

    - <span data-ttu-id="19065-121">Выберите →, чтобы переместить выбранный профиль учета из списка **Прочие** в список **совместимые**.</span><span class="sxs-lookup"><span data-stu-id="19065-121">Select → to move a selected inventory profile from the **Other** list to the **Compatible** list.</span></span> <span data-ttu-id="19065-122">Профиль учета добавляется в конец списка **совместимые**.</span><span class="sxs-lookup"><span data-stu-id="19065-122">The inventory profile is added to the end of the **Compatible** list.</span></span>
    - <span data-ttu-id="19065-123">Выберите →, чтобы удалить выбранный профиль учета из списка **Совместимые** и добавить его в список **Прочие**.</span><span class="sxs-lookup"><span data-stu-id="19065-123">Select ← to remove a selected inventory profile from the **Compatible** list and add it to the **Other** list.</span></span>
    - <span data-ttu-id="19065-124">Выберите ⊞→, чтобы переместить все профили учета из списка **Прочие** в список **совместимые**.</span><span class="sxs-lookup"><span data-stu-id="19065-124">Select ⊞→ to move all the inventory profiles from the **Other** list to the **Compatible** list.</span></span> <span data-ttu-id="19065-125">Профили последовательно добавляются в конец списка **совместимые**.</span><span class="sxs-lookup"><span data-stu-id="19065-125">The profiles are consistently added to the end of the **Compatible** list.</span></span>
    - <span data-ttu-id="19065-126">Выберите ←⊞, чтобы удалить все профили учета из списка **Совместимые** и добавить их в список **Прочие**.</span><span class="sxs-lookup"><span data-stu-id="19065-126">Select ←⊞ to remove all the inventory profiles from the **Compatible** list and add them to the **Other** list.</span></span>
    - <span data-ttu-id="19065-127">Используйте **вверх** или **вниз** для задания порядка сопоставления, который используется для профилей учета, совместимых с выбранным профилем учета, когда профили учета в наличии автоматически выбираются из запасов в наличии в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="19065-127">Use **Up** and **Down** to set the matching order that is used for inventory profiles that are compatible with the selected inventory profile when inventory profiles are automatically selected from the on-hand inventory in the sales order.</span></span>

4. <span data-ttu-id="19065-128">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="19065-128">Select **Save**.</span></span>

![Страница "профиль учета", экспресс-вкладка "совместимые профили учета"](media/2_Inventory_profiles.png)

## <a name="set-up-an-inventory-profile-in-tracking-dimension-groups"></a><span data-ttu-id="19065-130">Настройка профиля учета в группах аналитика отслеживания</span><span class="sxs-lookup"><span data-stu-id="19065-130">Set up an inventory profile in tracking dimension groups</span></span>

1. <span data-ttu-id="19065-131">Откройте **Управление сведениями о продукте \> Настройка \> Группы аналитик и вариантов \> Группы аналитик отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="19065-131">Go to **Product information management \> Setup \> Dimension and variant groups \> Tracking dimension groups**.</span></span>
2. <span data-ttu-id="19065-132">В левой области выберите группу аналитик или выберите **создать**, чтобы создать новую группу аналитик.</span><span class="sxs-lookup"><span data-stu-id="19065-132">In the left pane, select a dimension group, or select **New** to create a new dimension group.</span></span>
3. <span data-ttu-id="19065-133">В поле **Имя** введите полное имя группы аналитик.</span><span class="sxs-lookup"><span data-stu-id="19065-133">In the **Name** field, enter the name of the dimension group.</span></span>
4. <span data-ttu-id="19065-134">В поле **Описание** введите описание группы аналитик.</span><span class="sxs-lookup"><span data-stu-id="19065-134">In the **Description** field, enter a description of the dimension group.</span></span>
5. <span data-ttu-id="19065-135">На экспресс-вкладке **аналитики отслеживания** в строке **профиля учета** установите флажок **активно**, чтобы активировать профиль учета.</span><span class="sxs-lookup"><span data-stu-id="19065-135">On the **Tracking dimensions** FastTab, on the **Inventory profile** line, select the **Active** check box to activate the inventory profile.</span></span>

    <span data-ttu-id="19065-136">Флажки **Первичная аналитика хранения**, **Физические запасы**, **Финансовые запасы** и **Перемещение** установлены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19065-136">The **Primary stocking**, **Physical inventory**, **Financial inventory**, and **Transfer** check boxes are selected by default.</span></span>

6. <span data-ttu-id="19065-137">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="19065-137">Select **Save**.</span></span>

![Страница Аналитики отслеживания](media/3_Tracking_dimension_groups.png)

## <a name="activate-transaction-combinations-for-inventory-profiles"></a><span data-ttu-id="19065-139">Активация сочетаний проводок для профилей учета.</span><span class="sxs-lookup"><span data-stu-id="19065-139">Activate transaction combinations for inventory profiles</span></span>

1. <span data-ttu-id="19065-140">Выберите **Управление запасами \> Настройка \> Разноска \> Комбинации проводок**.</span><span class="sxs-lookup"><span data-stu-id="19065-140">Go to **Inventory management \> Setup \> Posting \> Transaction combinations**.</span></span>
2. <span data-ttu-id="19065-141">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="19065-141">Select **Edit**.</span></span>
3. <span data-ttu-id="19065-142">В разделе **отношение профиля учета** настройте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="19065-142">In the **Inventory profile relation** section, set the following values:</span></span>

    - <span data-ttu-id="19065-143">Установите флажок **Активировать отношение профиля учета Все**, если необходимо, чтобы можно было настроить разноску запасов, не указывая профиль учета.</span><span class="sxs-lookup"><span data-stu-id="19065-143">Select the **Activate inventory profile relation All** check box if you want to be able to set up inventory posting without specifying an inventory profile.</span></span>
    - <span data-ttu-id="19065-144">Установите флажок **Активировать отношение профиля учета Группы**, если необходимо, чтобы можно было настроить разноску запасов для видов деятельности.</span><span class="sxs-lookup"><span data-stu-id="19065-144">Select the **Activate inventory profile relation Group** check box if you want to be able to set up inventory posting for kinds of activity.</span></span>
    - <span data-ttu-id="19065-145">Установите флажок **Активировать отношение профиля учета Таблица**, если необходимо, чтобы можно было настроить разноску запасов для профилей учета.</span><span class="sxs-lookup"><span data-stu-id="19065-145">Select the **Activate inventory profile relation Table** check box if you want to be able to set up inventory posting for inventory profiles.</span></span>

4. <span data-ttu-id="19065-146">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="19065-146">Select **Save**.</span></span>

![Страница Комбинации проводок](media/4_Transaction_combinations.png)

## <a name="set-up-inventory-posting-in-the-context-of-an-inventory-profile"></a><span data-ttu-id="19065-148">Настройка профиля учета в контексте профиля учета.</span><span class="sxs-lookup"><span data-stu-id="19065-148">Set up inventory posting in the context of an inventory profile</span></span>

1. <span data-ttu-id="19065-149">Выберите **Управление запасами** \> **Настройка** \> **Разноска** \> **Разноска**.</span><span class="sxs-lookup"><span data-stu-id="19065-149">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
2. <span data-ttu-id="19065-150">В левой области выберите тип разноски и создайте новую строку.</span><span class="sxs-lookup"><span data-stu-id="19065-150">In the left pane, select the posting type, and create a new line.</span></span>
3. <span data-ttu-id="19065-151">В поле **отношение профиля учета** выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="19065-151">In the **Inventory profile relation** field, select one of the following values:</span></span>

    - <span data-ttu-id="19065-152">**Профиль** — Настройка разноски запасов для определенного профиля учета.</span><span class="sxs-lookup"><span data-stu-id="19065-152">**Profile** – Set up inventory posting for a specific inventory profile.</span></span>
    - <span data-ttu-id="19065-153">**Тип** — Настройка разноски запасов для определенного вид деятельности.</span><span class="sxs-lookup"><span data-stu-id="19065-153">**Type** – Set up inventory posting for a specific kind of activity.</span></span>
    - <span data-ttu-id="19065-154">**Все** — Настройка разноски запасов без указания вида деятельности или профиля учета.</span><span class="sxs-lookup"><span data-stu-id="19065-154">**All** – Set up inventory posting without specifying a kind of activity or an inventory profile.</span></span>

4. <span data-ttu-id="19065-155">В поле **вид деятельности** выберите вид деятельности, для которого необходимо настроить разноску запасов.</span><span class="sxs-lookup"><span data-stu-id="19065-155">In the **Kind of activity** field, select the kind of activity that you want to set up inventory posting for.</span></span> <span data-ttu-id="19065-156">Это поле доступно, только если выбран вариант **Тип** в поле **отношение профиля учета**.</span><span class="sxs-lookup"><span data-stu-id="19065-156">This field is available only if you selected **Type** in the **Inventory profile relation** field.</span></span>
5. <span data-ttu-id="19065-157">В поле **Профиль учета** выберите профиль учета, для которого необходимо настроить разноску запасов.</span><span class="sxs-lookup"><span data-stu-id="19065-157">In the **Inventory profile** field, select the inventory profile that you want to set up inventory posting for.</span></span> <span data-ttu-id="19065-158">Это поле доступно, только если выбран вариант **Профиль** в поле **отношение профиля учета**.</span><span class="sxs-lookup"><span data-stu-id="19065-158">This field is available only if you selected **Profile** in the **Inventory profile relation** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19065-159">Параметры профиля учета в настройке разноски запасов имеют приоритет над другими настройками.</span><span class="sxs-lookup"><span data-stu-id="19065-159">The inventory profile settings in the inventory posting setup have priority over the other settings.</span></span> <span data-ttu-id="19065-160">Например, имеется два набора параметров разноски:</span><span class="sxs-lookup"><span data-stu-id="19065-160">For example, you have two sets of posting  settings:</span></span>
>   
>   - <span data-ttu-id="19065-161">Параметры для определенной номенклатуры и любого профиля учета</span><span class="sxs-lookup"><span data-stu-id="19065-161">Settings for a specific item and any inventory profile</span></span>
>   - <span data-ttu-id="19065-162">Параметры для определенного профиля учета и всех номенклатур</span><span class="sxs-lookup"><span data-stu-id="19065-162">Settings for a specific inventory profile and all items</span></span>
>   
>   <span data-ttu-id="19065-163">В этом случае система выберет второй набор параметров.</span><span class="sxs-lookup"><span data-stu-id="19065-163">In this case, the system will select the second set of settings.</span></span>

## <a name="set-up-a-relation-between-inventory-profiles-and-customer-and-vendor-posting-profiles"></a><span data-ttu-id="19065-164">Настройте связь между профилями учета и профилями разноски клиента и поставщика</span><span class="sxs-lookup"><span data-stu-id="19065-164">Set up a relation between inventory profiles and customer and vendor posting profiles</span></span>

1. <span data-ttu-id="19065-165">Выберите **Управление запасами** \> **Настройка** \> **Разноска** \> **Профиль учета – профиль разноски**.</span><span class="sxs-lookup"><span data-stu-id="19065-165">Go to **Inventory management** \> **Setup** \> **Posting** \> **Inventory profile – posting profile**.</span></span>
2. <span data-ttu-id="19065-166">Выберите **Создать** для создания новой строки.</span><span class="sxs-lookup"><span data-stu-id="19065-166">Select **New** to create a new line.</span></span>
3. <span data-ttu-id="19065-167">В поле **отношение профиля учета** выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="19065-167">In the **Inventory profile relation** field, select one of the following values:</span></span>

    - <span data-ttu-id="19065-168">**Профиль** — Настройка профилей разноски по клиенту и поставщику для определенного профиля учета.</span><span class="sxs-lookup"><span data-stu-id="19065-168">**Profile** – Set up customer and vendor posting profiles for a specific inventory profile.</span></span>
    - <span data-ttu-id="19065-169">**Тип** — Настройка профилей разноски по клиенту и поставщику для определенного вид деятельности.</span><span class="sxs-lookup"><span data-stu-id="19065-169">**Type** – Set up customer and vendor posting profiles for a specific kind of activity.</span></span>
    - <span data-ttu-id="19065-170">**Все** — Настройка профилей разноски по клиенту и поставщику без указания вида деятельности или профиля учета.</span><span class="sxs-lookup"><span data-stu-id="19065-170">**All** – Set up customer and vendor posting profiles without specifying a kind of activity or an inventory profile.</span></span>

4. <span data-ttu-id="19065-171">В поле **вид деятельности** выберите вид деятельности, для которого необходимо настроить профили разноски.</span><span class="sxs-lookup"><span data-stu-id="19065-171">In the **Kind of activity** field, select the kind of activity that you want to set up posting profiles for.</span></span> <span data-ttu-id="19065-172">Это поле доступно, только если выбран вариант **Тип** в поле **отношение профиля учета**.</span><span class="sxs-lookup"><span data-stu-id="19065-172">This field is available only if you selected **Type** in the **Inventory profile relation** field.</span></span>
5. <span data-ttu-id="19065-173">В поле **Профиль учета** выберите профиль учета, для которого необходимо настроить профили разноски.</span><span class="sxs-lookup"><span data-stu-id="19065-173">In the **Inventory profile** field, select the inventory profile that you want to set up posting profiles for.</span></span> <span data-ttu-id="19065-174">Это поле доступно, только если выбран вариант **Профиль** в поле **отношение профиля учета**.</span><span class="sxs-lookup"><span data-stu-id="19065-174">This field is available only if you selected **Profile** in the **Inventory profile relation** field.</span></span> <span data-ttu-id="19065-175">При выборе определенного профиля учета поле **вид деятельности** автоматически устанавливается на соответствующий вид деятельности.</span><span class="sxs-lookup"><span data-stu-id="19065-175">When you select a specific inventory profile, the **Kind of activity** field is automatically set to the corresponding kind of activity.</span></span>
6. <span data-ttu-id="19065-176">Настройка полей **Профиль разноски по поставщику** и **Профиль разноски по клиенту**.</span><span class="sxs-lookup"><span data-stu-id="19065-176">Set the **Vendor posting profile** and **Customer posting profile** fields.</span></span>
7. <span data-ttu-id="19065-177">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="19065-177">Select **Save**.</span></span>

![Страница Профиль учета-профиль разноски](media/5_Inventory_profile_-_posting_profile.png)

## <a name="set-up-a-default-kind-of-activity-and-inventory-profile-for-vendors-customers-agreements-and-warehouses"></a><span data-ttu-id="19065-179">Настройка вида деятельности и профиля учета по умолчанию для поставщиков, клиентов, договоров и складов</span><span class="sxs-lookup"><span data-stu-id="19065-179">Set up a default kind of activity and inventory profile for vendors, customers, agreements, and warehouses</span></span>

<span data-ttu-id="19065-180">Можно указать вид деятельности и профиль учета по умолчанию в основной записи поставщика, клиента, соглашения или склада.</span><span class="sxs-lookup"><span data-stu-id="19065-180">You can specify the default kind of activity and inventory profile in a vendor, customer, agreement, or warehouse master record.</span></span> <span data-ttu-id="19065-181">На странице **все поставщики**, **все клиенты**, **Договоры покупки**, **Договоры продажи** или **склады** установите следующие поля.</span><span class="sxs-lookup"><span data-stu-id="19065-181">On the **All vendors**, **All customers**, **Purchase agreements**, **Sales agreements**, or **Warehouses** page, set the following fields.</span></span>

<table>
<thead>
<tr>
<td width="123">
<p><span data-ttu-id="19065-182"><strong>Страница</strong></span><span class="sxs-lookup"><span data-stu-id="19065-182"><strong>Page</strong></span></span></p>
</td>
<td width="123">
<p><span data-ttu-id="19065-183"><strong>Экспресс-вкладка</strong></span><span class="sxs-lookup"><span data-stu-id="19065-183"><strong>FastTab</strong></span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="19065-184"><strong>Секция</strong></span><span class="sxs-lookup"><span data-stu-id="19065-184"><strong>Section</strong></span></span></p>
</td>
<td width="369">
<p><span data-ttu-id="19065-185"><strong>Поля</strong></span><span class="sxs-lookup"><span data-stu-id="19065-185"><strong>Fields</strong></span></span></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td width="123">
<p><span data-ttu-id="19065-186">Все поставщики</span><span class="sxs-lookup"><span data-stu-id="19065-186">All vendors</span></span></p>
</td>
<td width="123">
<p><span data-ttu-id="19065-187">Значения заказа на покупку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="19065-187">Purchase order defaults</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="19065-188">Профиль учета</span><span class="sxs-lookup"><span data-stu-id="19065-188">Inventory profile</span></span></p>
</td>
<td width="369">
<p><span data-ttu-id="19065-189">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Вид деятельности</strong> &ndash; Выбор вида деятельности, который должен быть введен по умолчанию в заказах на покупку от поставщика.</span><span class="sxs-lookup"><span data-stu-id="19065-189">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Kind of activity</strong> &ndash; Select the kind of activity that should be entered by default in purchase orders from the vendor.</span></span></p>
<p><span data-ttu-id="19065-190">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Профиль учета</strong> &ndash; Выбор профиль учета, который должен быть введен по умолчанию в заказах на покупку от поставщика.</span><span class="sxs-lookup"><span data-stu-id="19065-190">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Inventory profile</strong> &ndash; Select the inventory profile that should be entered by default in purchase orders from the vendor.</span></span></p>
</td>
</tr>
<tr>
<td width="123">
<p><span data-ttu-id="19065-191">Все клиенты</span><span class="sxs-lookup"><span data-stu-id="19065-191">All customers</span></span></p>
</td>
<td width="123">
<p><span data-ttu-id="19065-192">Значения заказов на продажу по умолчанию</span><span class="sxs-lookup"><span data-stu-id="19065-192">Sales order defaults</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="19065-193">Профиль учета</span><span class="sxs-lookup"><span data-stu-id="19065-193">Inventory profile</span></span></p>
</td>
<td width="369">
<p><span data-ttu-id="19065-194">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Вид деятельности</strong> &ndash; Выбор вида деятельности, который должен быть введен по умолчанию в заказах на продажу от клиента.</span><span class="sxs-lookup"><span data-stu-id="19065-194">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Kind of activity</strong> &ndash; Select the kind of activity that should be entered by default in sales orders from the customer.</span></span></p>
<p><span data-ttu-id="19065-195">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Профиль учета</strong> &ndash; Выбор профиль учета, который должен быть введен по умолчанию в заказах на продажу от клиента.</span><span class="sxs-lookup"><span data-stu-id="19065-195">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Inventory profile</strong> &ndash; Select the inventory profile that should be entered by default in sales orders from the customer.</span></span></p>
</td>
</tr>
<tr>
<td width="123">
<p><span data-ttu-id="19065-196">Договоры покупки</span><span class="sxs-lookup"><span data-stu-id="19065-196">Purchase agreements</span></span></p>
</td>
<td width="123">
<p><span data-ttu-id="19065-197">Финансы (в представлении <strong>Заголовок</strong>)</span><span class="sxs-lookup"><span data-stu-id="19065-197">Financial (in the <strong>Header</strong> view)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="19065-198">Профиль учета</span><span class="sxs-lookup"><span data-stu-id="19065-198">Inventory profile</span></span></p>
</td>
<td width="369">
<p><span data-ttu-id="19065-199">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Вид деятельности</strong> &ndash; Выбор вида деятельности, который должен быть введен по умолчанию в заказах на покупку из договора покупки.</span><span class="sxs-lookup"><span data-stu-id="19065-199">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Kind of activity</strong> &ndash; Select the kind of activity that should be entered by default in purchase orders from the purchase agreement.</span></span></p>
<p><span data-ttu-id="19065-200">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Профиль учета</strong> &ndash; Выбор профиль учета, который должен быть введен по умолчанию в заказах на покупку из договора покупки.</span><span class="sxs-lookup"><span data-stu-id="19065-200">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Inventory profile</strong> &ndash; Select the inventory profile that should be entered by default in purchase orders from the purchase agreement.</span></span></p>
<p><span data-ttu-id="19065-201">При создании нового договора покупки с поставщиком поля <strong>Вид деятельности</strong> и <strong>профиль учета</strong> автоматически заполняются поставщиком.</span><span class="sxs-lookup"><span data-stu-id="19065-201">When you create a new purchase agreement with a vendor, the <strong>Kind of activity</strong> and <strong>Inventory profile</strong> fields are automatically filled in from the vendor.</span></span></p>
</td>
</tr>
<tr>
<td width="123">
<p><span data-ttu-id="19065-202">Договоры продажи</span><span class="sxs-lookup"><span data-stu-id="19065-202">Sales agreements</span></span></p>
</td>
<td width="123">
<p><span data-ttu-id="19065-203">Финансы (в представлении <strong>Заголовок</strong>)</span><span class="sxs-lookup"><span data-stu-id="19065-203">Financial (in the <strong>Header</strong> view)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="19065-204">Профиль учета</span><span class="sxs-lookup"><span data-stu-id="19065-204">Inventory profile</span></span></p>
</td>
<td width="369">
<p><span data-ttu-id="19065-205">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;<strong>Вид деятельности</strong> &ndash; Выбор вида деятельности, который должен автоматически использоваться в заказах на продажу, которые используют договор продажи.</span><span class="sxs-lookup"><span data-stu-id="19065-205">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;<strong>Kind of activity</strong> &ndash; Select the kind of activity that should automatically be used in sales orders that use the sales agreement.</span></span></p>
<p><span data-ttu-id="19065-206">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Профиль учета</strong> &ndash; Выбор профиля учета, который должен автоматически использоваться в заказах на продажу, которые используют договор продажи.</span><span class="sxs-lookup"><span data-stu-id="19065-206">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Inventory profile</strong> &ndash; Select the inventory profile that should automatically be used in sales orders that use the sales agreement.</span></span></p>
<p><span data-ttu-id="19065-207">При создании нового договора продажи с клиентом поля <strong>Вид деятельности</strong> и <strong>профиль учета</strong> автоматически заполняются из записи клиента.</span><span class="sxs-lookup"><span data-stu-id="19065-207">When you create a new sales agreement with a customer, the <strong>Kind of activity</strong> and <strong>Inventory profile</strong> fields are automatically filled in from the customer record.</span></span></p>
</td>
</tr>
<tr>
<td width="123">
<p><span data-ttu-id="19065-208">Склады</span><span class="sxs-lookup"><span data-stu-id="19065-208">Warehouses</span></span></p>
</td>
<td width="123">
<p><span data-ttu-id="19065-209">Общее</span><span class="sxs-lookup"><span data-stu-id="19065-209">General</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="19065-210">Профиль учета</span><span class="sxs-lookup"><span data-stu-id="19065-210">Inventory profile</span></span></p>
</td>
<td width="369">
<p><span data-ttu-id="19065-211">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Вид деятельности</strong> &ndash; Выбор вида деятельности, который должен быть введен по умолчанию в заказах на перемещение со склада.</span><span class="sxs-lookup"><span data-stu-id="19065-211">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Kind of activity</strong> &ndash; Select the kind of activity that should be entered by default in transfer orders from the warehouse.</span></span></p>
<p><span data-ttu-id="19065-212">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Профиль учета</strong> поле, выберите профиль учета, который должен быть введен по умолчанию в заказах на перемещение со склада.</span><span class="sxs-lookup"><span data-stu-id="19065-212">&middot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>Inventory profile</strong> field, select the inventory profile that should be entered by default in transfer orders from the warehouse.</span></span></p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>

> [!NOTE]
> <span data-ttu-id="19065-213">При выборе определенного профиля учета поле **вид деятельности** автоматически устанавливается на соответствующий вид деятельности.</span><span class="sxs-lookup"><span data-stu-id="19065-213">When you select a specific inventory profile, the **Kind of activity** field is automatically set to the corresponding kind of activity.</span></span>

## <a name="set-up-a-default-inventory-profile-for-boms"></a><span data-ttu-id="19065-214">Настройка профиля учета по умолчанию для спецификаций.</span><span class="sxs-lookup"><span data-stu-id="19065-214">Set up a default inventory profile for BOMs</span></span>

1. <span data-ttu-id="19065-215">Перейдите **Управление запасами \> Записи журнала \> Номенклатуры \> Спецификации**.</span><span class="sxs-lookup"><span data-stu-id="19065-215">Go to **Inventory management \> Journal entries \> Items \> Bills of materials**.</span></span>
2. <span data-ttu-id="19065-216">Выберите журнал спецификации и создайте строку.</span><span class="sxs-lookup"><span data-stu-id="19065-216">Select a BOM journal and its line.</span></span>
3. <span data-ttu-id="19065-217">На экспресс-вкладке **Сведения о строке** на вкладке **Складские аналитики** в поле **Профиль учета** выберите профиль учета.</span><span class="sxs-lookup"><span data-stu-id="19065-217">On the **Line details** FastTab, on the **Inventory dimensions** tab, in the **Inventory profile** field, select an inventory profile.</span></span>

> [!NOTE]
> <span data-ttu-id="19065-218">Невозможно развернуть или принять спецификацию или создать производственный заказ, если выполняются все следующие условия:</span><span class="sxs-lookup"><span data-stu-id="19065-218">You can't explode or accept the BOM, or create a production order, if all the following conditions are met:</span></span>
>
>   - <span data-ttu-id="19065-219">Для номенклатуры в строке спецификации активен профиль учета.</span><span class="sxs-lookup"><span data-stu-id="19065-219">The inventory profile is active for the item on the BOM line.</span></span>
>   - <span data-ttu-id="19065-220">В строке спецификации не указана аналитика **профиля запасов**.</span><span class="sxs-lookup"><span data-stu-id="19065-220">The BOM line doesn't specify the **Inventory profile** dimension.</span></span>
>   - <span data-ttu-id="19065-221">Поле **Профиль запасов** на вкладке **спецификации** модуля **Управление запасами и складами** пусто.</span><span class="sxs-lookup"><span data-stu-id="19065-221">The **Inventory profile** field on the **Bills of materials** tab of the **Inventory and warehouse management parameters** page is blank.</span></span>

## <a name="set-up-a-default-inventory-profile-for-purchase-orders"></a><span data-ttu-id="19065-222">Настройка профиля учета по умолчанию для заказов на покупку</span><span class="sxs-lookup"><span data-stu-id="19065-222">Set up a default inventory profile for purchase orders</span></span>

<span data-ttu-id="19065-223">На странице **Параметры модуля "Закупки и источники"** можно выбрать профиль учета по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19065-223">On the **Procurement and sourcing parameters** page, you can select a default inventory profile.</span></span> <span data-ttu-id="19065-224">Этот профиль учета будет затем автоматически вводиться в заказы на покупку, если не выбраны профили учета по умолчанию и виды деятельности для записи поставщика и записи договора покупки.</span><span class="sxs-lookup"><span data-stu-id="19065-224">That inventory profile will then automatically be entered in purchase orders if default inventory profiles and kinds of activity aren't selected for the vendor record and purchase agreement record.</span></span>

1. <span data-ttu-id="19065-225">Выберите **Закупки и источники \> Настройка \> Параметры модуля "Закупки и источники"**.</span><span class="sxs-lookup"><span data-stu-id="19065-225">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
2. <span data-ttu-id="19065-226">На вкладке **Общие** на экспресс-вкладке **значения и параметры по умолчанию** в поле **Профиль учета** выберите профиль учета, который должен использоваться автоматически в заказах на покупку.</span><span class="sxs-lookup"><span data-stu-id="19065-226">On the **General** tab, on the **Default values and parameters** FastTab, in the **Inventory profile** field, select the inventory profile that should automatically be used in purchase orders.</span></span>

    ![Страница Параметры модуля "Закупки и источники", вкладка Общие](media/6_Procurement_and_sourcing_parameters.png)

3. <span data-ttu-id="19065-228">Выберите **Обновление строк заказа**, чтобы открыть диалоговое окно **Обновление строк заказа**.</span><span class="sxs-lookup"><span data-stu-id="19065-228">Select **Update order lines** to open the **Update order lines** dialog box.</span></span>

    ![Диалоговое окно Обновление строк заказа](media/7_Update_order_lines.png)

4. <span data-ttu-id="19065-230">В разделе **Профиль учета** в поле **Обновить профиль учета** выберите одно из следующих значений для настройки правил, используемых для обновления поля **профиль учета** в строках заказа на покупку при изменении соответствующего поля в заголовке заказа на покупку:</span><span class="sxs-lookup"><span data-stu-id="19065-230">In the **Inventory profile** section, in the **Updating Inventory profile** field, select one of the following values to set up the rules that are used to update the **Inventory profile** field on purchase order lines when the corresponding field in the purchase order header is changed:</span></span>

    - <span data-ttu-id="19065-231">**Никогда** — профиль учета в строках заказа не должен обновляться автоматически при изменении профиля учета в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="19065-231">**Never** – The inventory profile on the order lines should not automatically be updated when the inventory profile in the order header is changed.</span></span>
    - <span data-ttu-id="19065-232">**Всегда** — профиль учета в строках заказа должны всегда обновляться автоматически при изменении профиля учета в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="19065-232">**Always** – The inventory profile on the order lines should always automatically be updated when the inventory profile in the order header is changed.</span></span>
    - <span data-ttu-id="19065-233">**Запрос** — система должна предложить вам обновить профиль учета в строках заказа при изменении профиля учета в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="19065-233">**Prompt** – The system should prompt you to update the inventory profile on the order lines when you change the inventory profile in the order header.</span></span>

5. <span data-ttu-id="19065-234">Закройте диалоговое окно **Обновление строк заказа**.</span><span class="sxs-lookup"><span data-stu-id="19065-234">Close the **Update order lines** dialog box.</span></span>
6. <span data-ttu-id="19065-235">На странице **Параметры модуля "Закупки и источники"** на вкладке **Сводное обновление** в разделе **Разделение на основании** установите два варианта **Поступление продуктов**:</span><span class="sxs-lookup"><span data-stu-id="19065-235">On the **Procurement and sourcing parameters** page, on the **Summary update** tab, in the **Split based on** section, set the two **Product receipt** options:</span></span>

    - <span data-ttu-id="19065-236">Установите для параметра в столбце **профиль разноски** значение **Да**, если требуется разбиение поступления продуктов заказа на покупку по профилям разноски по поставщикам, указанным в строках заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="19065-236">Set the option in the **Posting profile** column to **Yes** if you want to split purchase order product receipts by the vendor posting profiles that are specified on the purchase order lines.</span></span>
    - <span data-ttu-id="19065-237">Установите параметр в столбце **Вид деятельности** в значение **Да**, если требуется разбиение отборочных накладных по заказу на покупку на виды деятельности, которые включают профили учета, указанные в строках заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="19065-237">Set the option in the **Kind of activity** column to **Yes** if you want to split purchase order packing slips by the kinds of activity that include the inventory profiles that are specified on the purchase order lines.</span></span>

![Страница Параметры модуля "Закупки и источники", вкладка Сводное обновление](media/8_Procurement_and_sourcing_parameters.png)

> [!NOTE]
> <span data-ttu-id="19065-239">Параметр **Накладная** в обоих столбцах **профиль разноски** и столбца **Вид деятельности** всегда имеет значение **Да** и не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="19065-239">The **Invoice** option in both the **Posting profile** column and the **Kind of activity** column is always set to **Yes** and can't be changed.</span></span> <span data-ttu-id="19065-240">Таким образом, накладные, связанные с заказом на покупку всегда разбиваются на профили разноски по поставщику и виды деятельности.</span><span class="sxs-lookup"><span data-stu-id="19065-240">Therefore, purchase order invoices are always split by vendor posting profiles and kinds of activity.</span></span>

## <a name="set-up-a-default-inventory-profile-for-sales-orders"></a><span data-ttu-id="19065-241">Настройка профиля учета по умолчанию для заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="19065-241">Set up a default inventory profile for sales orders</span></span>

<span data-ttu-id="19065-242">На странице **Параметры модуля расчетов с клиентами** можно выбрать профиль учета по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19065-242">On the **Accounts receivable parameters** page, you can select a default inventory profile.</span></span> <span data-ttu-id="19065-243">Этот профиль учета будет затем автоматически выбран в заказах на продажу, если не выбраны профили учета по умолчанию и виды деятельности для записи клиента и записи договора продажи.</span><span class="sxs-lookup"><span data-stu-id="19065-243">That inventory profile will then automatically be selected in sales orders if default inventory profiles and kinds of activity for the customer record and sales agreement record aren't selected.</span></span>

1. <span data-ttu-id="19065-244">Перейдите в раздел **Расчеты с клиентами** \> **Настройка** \> **Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="19065-244">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="19065-245">На вкладке **Общие** на экспресс-вкладке **Настройка продаж** в поле **Профиль учета** выберите профиль учета, который должен использоваться автоматически в заказах на продажу.</span><span class="sxs-lookup"><span data-stu-id="19065-245">On the **General** tab, on the **Sales setup** FastTab, in the **Inventory profile** field, select the inventory profile that should automatically be used in sales orders.</span></span>
3. <span data-ttu-id="19065-246">Установите параметр **использовать совместимые профили учета** на **Да**, если в заказах на продажу должны автоматически использоваться совместимые профили учета.</span><span class="sxs-lookup"><span data-stu-id="19065-246">Set the **Use compatible inventory profiles** option to **Yes** if compatible inventory profiles should automatically be used in sales orders.</span></span>
4. <span data-ttu-id="19065-247">Установите параметр **разбивка строк заказа по профилям учета** на **Да**, чтобы автоматически разбить строки заказа на продажу по профилям учета при использовании **Создать строки** из доступного физического количества.</span><span class="sxs-lookup"><span data-stu-id="19065-247">Set the **Split order lines by inventory profiles** option to **Yes** to automatically split sales order lines by the inventory profiles when **Create lines** is used from the available physical quantity.</span></span>

    ![Страница Параметры расчетов с клиентами, вкладка "Общие"](media/9_Accounts_receivable_parameters.png)

5. <span data-ttu-id="19065-249">На вкладке **Сводное обновление** на экспресс-вкладке **Разделение на основании** установите параметр **Профиль разноски** в столбце **Отборочная накладная** на **Да** для разбиения отборочных накладных заказа на продажу по профилям разноски по клиенту, указанным в строках заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="19065-249">On the **Summary update** tab, on the **Split based on** FastTab, set the **Posting profile** option in the **Packing slip** column to **Yes** to split sales order packing slips by the customer posting profiles that are specified on the sales order lines.</span></span>
6. <span data-ttu-id="19065-250">Установите параметр **Вид деятельности** в столбце **отборочная накладная** на **Да**, если требуется разбиение отборочных накладных по заказу на покупку на виды деятельности, которые включают профили учета, указанные в строках заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="19065-250">Set the **Kind of activity** option in the **Packing slip** column to **Yes** to split sales order packing slips by the kinds of activity that the inventory profiles that are specified on the sales order lines correspond to.</span></span>

    ![<span data-ttu-id="19065-251">Страница "Параметры модуля расчетов с клиентами", вкладка Сводное обновление</span><span class="sxs-lookup"><span data-stu-id="19065-251">Accounts receivable parameters page, Summary update tab</span></span> ](media/10_Accounts_receivable_parameters.png)

    > [!NOTE]
    > <span data-ttu-id="19065-252">В столбце **Накладная** параметры **профиль разноски** и **Вид деятельности** всегда имеют значение **Да** и не могут быть изменено.</span><span class="sxs-lookup"><span data-stu-id="19065-252">In the **Invoice** column, the **Posting profile** and **Kind of activity** options are always set to **Yes** and can't be changed.</span></span> <span data-ttu-id="19065-253">Таким образом, накладные по заказам на продажу всегда разбиваются на профили разноски по клиенту и виды деятельности.</span><span class="sxs-lookup"><span data-stu-id="19065-253">Therefore, sales order invoices are always split by customer posting profiles and kinds of activity.</span></span>

7. <span data-ttu-id="19065-254">На вкладке **обновления** на Экспресс-вкладке **строки заказа** выберите **Обновление строк заказа**, чтобы открыть диалоговое окно **Обновление строк заказа**.</span><span class="sxs-lookup"><span data-stu-id="19065-254">On the **Updates** tab, on the **Order lines** FastTab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
8. <span data-ttu-id="19065-255">В разделе **Режим доставки** в поле **Обновить профиль учета** выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="19065-255">In the **Mode of delivery** section, in the **Updating Inventory profile** field, select one of the following values:</span></span>

    - <span data-ttu-id="19065-256">**Никогда** — профиль учета в строках заказа не должен обновляться автоматически при изменении профиля учета в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="19065-256">**Never** – The inventory profile on the order lines should not automatically be updated when the inventory profile in the order header is changed.</span></span>
    - <span data-ttu-id="19065-257">**Всегда** — профиль учета в строках заказа должны всегда обновляться автоматически при изменении профиля учета в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="19065-257">**Always** – The inventory profile on the order lines should always automatically be updated when the inventory profile in the order header is changed.</span></span>
    - <span data-ttu-id="19065-258">**Запрос** — система должна предложить вам обновить профиль учета в строках заказа при изменении профиля учета в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="19065-258">**Prompt** – The system should prompt you to update the inventory profile on the order lines when you change the inventory profile in the order header.</span></span>

![Страница Обновление строк заказа](media/11_Update_order_lines.png)

## <a name="set-up-a-default-inventory-profile-for-transfer-orders"></a><span data-ttu-id="19065-260">Настройка профиля учета по умолчанию для заказов на перемещение</span><span class="sxs-lookup"><span data-stu-id="19065-260">Set up a default inventory profile for transfer orders</span></span>

<span data-ttu-id="19065-261">На странице **Параметры модуля "Управление запасами и складами"** можно выбрать профиль учета по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19065-261">On the **Inventory and warehouse management parameters** page, you can select a default inventory profile.</span></span> <span data-ttu-id="19065-262">Этот профиль учета будет затем автоматически выбран в заказах на перемещение, если не выбраны профиль учета по умолчанию и вид деятельности для записи склада.</span><span class="sxs-lookup"><span data-stu-id="19065-262">That inventory profile will then automatically be selected in transfer orders if a default inventory profile and kind of activity for the warehouse record aren't selected.</span></span>

1. <span data-ttu-id="19065-263">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Параметры управления запасами и складами**.</span><span class="sxs-lookup"><span data-stu-id="19065-263">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="19065-264">На вкладке **Общие** в разделе **Профиль учета** в поле **Профиль учета** выберите профиль учета, который должен использоваться автоматически в заказах на перемещение.</span><span class="sxs-lookup"><span data-stu-id="19065-264">On the **General** tab, in the **Inventory profile** section, in the **Inventory profile** field, select the inventory profile that should automatically be used in transfer orders.</span></span>
3. <span data-ttu-id="19065-265">Установите параметр **использовать совместимые профили учета** на **Да**, если параметр **использовать совместимые профили учета** в заказах на перемещение должен быть установлен на **Да** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19065-265">Set the **Use compatible inventory profiles** option to **Yes** if the **Use compatible inventory profiles** option in transfer orders should be set to **Yes** by default.</span></span>

    ![Страница Параметры управления запасами и складами, вкладка Общие](media/12_Inventory_and_warehouse_management_parameters.png)

4. <span data-ttu-id="19065-267">На вкладке **спецификации** в поле **Профиль учета** выберите профиль учета, который должен использоваться по умолчанию при создании и развертывании спецификаций, и когда обрабатывается как готовое, если в строках спецификации не указан профиль учета.</span><span class="sxs-lookup"><span data-stu-id="19065-267">On the **Bills of materials** tab, in the **Inventory profile** field, select the inventory profile that should be used by default when BOMs are created and exploded, and when reporting as finished is processed, if an inventory profile isn't specified on the BOM lines.</span></span>

<span data-ttu-id="19065-268">![Страница параметров модуля "Управление запасами и складами", вкладка Спецификации](media/13_Inventory_and_warehouse_management_parameters.png)</span><span class="sxs-lookup"><span data-stu-id="19065-268">!Inventory and warehouse management parameters page, Bills of materials tab](media/13_Inventory_and_warehouse_management_parameters.png)</span></span>

<span data-ttu-id="19065-269">Более подробную информацию см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="19065-269">Find more details in the following topics:</span></span>

- [<span data-ttu-id="19065-270">Обзор профиля учета</span><span class="sxs-lookup"><span data-stu-id="19065-270">Inventory profile overview</span></span>](rus-inventory-profile-overview.md)
- [<span data-ttu-id="19065-271">Использование профиля учета в документах и запросах</span><span class="sxs-lookup"><span data-stu-id="19065-271">Use an inventory profile in documents and queries</span></span>](rus-use-inventory-profile-documents-queries.md)
