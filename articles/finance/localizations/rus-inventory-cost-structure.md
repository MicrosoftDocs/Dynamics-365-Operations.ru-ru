---
title: Структура стоимости запасов
description: В этой теме приводятся сведения о структуре стоимости запасов для накладных расходов в складских проводках.
author: v-nadyuz
manager: AnnBe
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a10fe09d0dda892d3679aee71f2bab40205f385d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408558"
---
# <a name="inventory-cost-structure"></a><span data-ttu-id="c2e0a-103">Структура стоимости запасов</span><span class="sxs-lookup"><span data-stu-id="c2e0a-103">Inventory cost structure</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2e0a-104">Структуру затрат на номенклатуру можно сохранить в складских проводках в качестве накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-104">You can save the item cost structure in inventory transactions as miscellaneous charges.</span></span> <span data-ttu-id="c2e0a-105">После этого можно просмотреть структуру затрат на странице **Анализатор себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-105">You can then review the cost structure on the **Cost explorer** page.</span></span> <span data-ttu-id="c2e0a-106">Можно изменить стоимость складских проводок, используя следующие функции:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-106">You can change the cost of inventory transactions by using the following functionality:</span></span>

- <span data-ttu-id="c2e0a-107">Распределите накладные расходы из заказов на покупку и заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-107">Allocate miscellaneous charges from purchase orders and sales orders.</span></span>
- <span data-ttu-id="c2e0a-108">Настройте затраты на поступление на склад, используя периодическую операцию **Закрытие и коррекция**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-108">Adjust the cost of inventory receipts by using the **Closing and adjustment** periodic operation.</span></span>

<span data-ttu-id="c2e0a-109">При распределении накладных расходов по заказу на покупку создаются сопоставления запасов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-109">When you allocate miscellaneous charges on a purchase order, inventory settlements are generated.</span></span> <span data-ttu-id="c2e0a-110">Затем можно просмотреть складские проводки прихода в виде кодов накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-110">You can then explore receipt inventory transactions in terms of miscellaneous charges codes.</span></span> <span data-ttu-id="c2e0a-111">Для работы со стоимостью складских проводок необходимо создать код накладных расходов для складских проводок расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-111">To work with the cost of inventory transactions, you must create a miscellaneous charges code for expense inventory transactions.</span></span> <span data-ttu-id="c2e0a-112">Для этой цели доступны следующие функции системы:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-112">The following system features are available for this purpose:</span></span>

- <span data-ttu-id="c2e0a-113">Настройка параметра **Структура накладных расходов**, чтобы разрешить или запретить создание сопоставлений запасов в виде кодов накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-113">Set the **Misc. charges structure** parameter to allow or disallow the creation of inventory settlements in terms of miscellaneous charges codes.</span></span>
- <span data-ttu-id="c2e0a-114">Периодическая операция **Закрытие и коррекция** используется для регистрации корректировки затрат по складским проводкам или по запасам в наличии, которые имеют коды накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-114">Use the **Closing and adjustment** periodic operation to register a cost adjustment on inventory transactions or on-hand inventory that has miscellaneous charges codes.</span></span>
- <span data-ttu-id="c2e0a-115">Страница **Анализатор себестоимости** предназначена для просмотра и изучения структуры затрат в виде кодов накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-115">Use the **Cost explorer** page to view and explore a cost structure in terms of miscellaneous charges codes.</span></span>

## <a name="preliminary-setup"></a><span data-ttu-id="c2e0a-116">Предварительная настройка</span><span class="sxs-lookup"><span data-stu-id="c2e0a-116">Preliminary setup</span></span>

### <a name="set-up-the-miscellaneous-charges-structure"></a><span data-ttu-id="c2e0a-117">Настройка структуры накладных расходов</span><span class="sxs-lookup"><span data-stu-id="c2e0a-117">Set up the miscellaneous charges structure</span></span>

1. <span data-ttu-id="c2e0a-118">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Параметры управления запасами и складами**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-118">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="c2e0a-119">На вкладке **Общие** в разделе **Корректировка** задайте параметр **Структура накладных расходов**:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-119">On the **General** tab, in the **Correction** section, set the **Misc. charges structure** option:</span></span>

    - <span data-ttu-id="c2e0a-120">Если для этого параметра установить значение **Нет**, одна проводка сопоставления для общей суммы создается для каждой проводки прихода.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-120">If you set this option to **No**, one settlement transaction, for the total amount, is generated for each receipt transaction.</span></span> <span data-ttu-id="c2e0a-121">Код накладных расходов не введен в сопоставление запасов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-121">The miscellaneous charges code isn't entered in the inventory settlement.</span></span>
    - <span data-ttu-id="c2e0a-122">При выборе значения **Да** сопоставления запасов создаются как коды накладных расходов при разноске накладной по покупке.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-122">If you set this option to **Yes**, inventory settlements are generated as miscellaneous charges codes when you post a purchase invoice.</span></span>

### <a name="set-up-a-charges-code-in-inventory-management"></a><span data-ttu-id="c2e0a-123">Настройка кода расходов в управлении запасами</span><span class="sxs-lookup"><span data-stu-id="c2e0a-123">Set up a charges code in Inventory management</span></span>

1. <span data-ttu-id="c2e0a-124">Перейдите **Управление запасами** \> **Настройка** \> **Накладные расходы** \> **Коды накладных расходов**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-124">Go to **Inventory management** \> **Setup** \> **Charges** \> **Charges codes**.</span></span>
2. <span data-ttu-id="c2e0a-125">Создание кода расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-125">Create a charges code.</span></span> <span data-ttu-id="c2e0a-126">Коды накладных расходов, которые создаются в модуле **Управление запасами**, имеют следующие ограничения по конфигурации:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-126">Charges codes that you create in the **Inventory management** module have the following configuration limitations:</span></span>

    - <span data-ttu-id="c2e0a-127">В поле **Тип** в разделе **Дебет** можно выбрать только **Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-127">In the **Type** field in the **Debit** section, you can select only **Item**.</span></span>
    - <span data-ttu-id="c2e0a-128">В поле **Тип** в разделе **Кредит** можно выбрать только **Счет ГК**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-128">In the **Type** field in the **Credit** section, you can select only **Ledger account**.</span></span>

![Страница накладных расходов](media/1_Charges_codes.png)

## <a name="adjustment-of-item-cost-in-terms-of-miscellaneous-charges-codes"></a><span data-ttu-id="c2e0a-130">Корректировка затрат по номенклатуре в виде кодов накладных расходов</span><span class="sxs-lookup"><span data-stu-id="c2e0a-130">Adjustment of item cost in terms of miscellaneous charges codes</span></span>

<span data-ttu-id="c2e0a-131">В модуле **Управление запасами** накладные расходы могут распределяться несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-131">In the **Inventory management** module, miscellaneous charges can be allocated in several ways:</span></span>

- <span data-ttu-id="c2e0a-132">Коррекция запасов в наличии вручную.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-132">Manually adjust on-hand inventory.</span></span>
- <span data-ttu-id="c2e0a-133">Корректировка проводок вручную.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-133">Manually adjust transactions.</span></span>
- <span data-ttu-id="c2e0a-134">Корректировка запасов в наличии или проводок с помощью мастера.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-134">Adjust on-hand inventory or transactions by using a wizard.</span></span>

<span data-ttu-id="c2e0a-135">Существующие коды накладных расходов можно указать при корректировке себестоимости номенклатур на страницах **Наличие**, **Корректировать проводки** и **Мастер коррекции себестоимости складских проводок или всех запасов в наличии**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-135">You can specify existing miscellaneous charges codes when you adjust item cost on the **On-hand**, **Adjust transactions**, and **Wizard for cost value adjustment of inventory transactions or entire on-hand inventory** pages.</span></span>

### <a name="close-inventory"></a><a name="close-inventory"></a><span data-ttu-id="c2e0a-136">Закрыть запасы</span><span class="sxs-lookup"><span data-stu-id="c2e0a-136">Close inventory</span></span>

<span data-ttu-id="c2e0a-137">Перед корректировкой запасов в наличии необходимо закрыть запасы.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-137">Before you adjust on-hand inventory, you must close the inventory.</span></span> <span data-ttu-id="c2e0a-138">Дополнительные сведения о закрытии склада см. в разделе [Закрытие запасов](../../supply-chain/cost-management/inventory-close.md).</span><span class="sxs-lookup"><span data-stu-id="c2e0a-138">For more information about inventory closing, see [Inventory close](../../supply-chain/cost-management/inventory-close.md).</span></span>

1. <span data-ttu-id="c2e0a-139">Перейдите **Управление запасами** \> **Периодические задачи** \> **Закрытие и коррекция**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-139">Go to **Inventory management** \> **Periodic tasks** \> **Closing and adjustment**.</span></span>
2. <span data-ttu-id="c2e0a-140">На панели операций выберите **Процедура закрытия** \> **Закрыть запасы**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-140">On the Action Pane, select **Close procedure** \> **Close inventory**.</span></span>
3. <span data-ttu-id="c2e0a-141">В диалоговом окне **Закрыть запасы** в поле **Закрыть запасы до** укажите дату, с которой должны быть закрыты запасы.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-141">In the **Close inventory** dialog box, in the **Close inventory up to** field, specify the date that the inventory will be closed by.</span></span>
4. <span data-ttu-id="c2e0a-142">В поле **Детализация** выберите **Все**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-142">In the **Specification** field, select **All**.</span></span>

    ![Диалоговое окно закрытия запасов](media/2_Close_inventory.png)

5. <span data-ttu-id="c2e0a-144">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-144">Select **OK**.</span></span>

### <a name="cancel-inventory-closing"></a><a name="cancel-inventory-closing"></a><span data-ttu-id="c2e0a-145">Отмена закрытия запасов</span><span class="sxs-lookup"><span data-stu-id="c2e0a-145">Cancel inventory closing</span></span>

<span data-ttu-id="c2e0a-146">Прежде чем можно будет корректировать проводки, необходимо убедиться, что запасы не закрыты.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-146">Before you can adjust transactions, you must verify that the inventory wasn't closed.</span></span>

1.  <span data-ttu-id="c2e0a-147">Перейдите **Управление запасами** \> **Периодические задачи** \> **Закрытие и коррекция**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-147">Go to **Inventory management** \> **Periodic tasks** \> **Closing and adjustment**.</span></span>
2.  <span data-ttu-id="c2e0a-148">Выберите операцию закрытия запасов, а затем в области действий выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-148">Select the inventory closing operation, and then, on the Action Pane, select **Cancellation**.</span></span>
3.  <span data-ttu-id="c2e0a-149">В диалоговом окне **Отмена - Начать** выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-149">In the **Cancellation – initialize** dialog box, select **OK**.</span></span>

### <a name="adjust-on-hand-inventory"></a><a name="adjust-on-hand-inventory"></a><span data-ttu-id="c2e0a-150">Корректировка запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="c2e0a-150">Adjust on-hand inventory</span></span>

<span data-ttu-id="c2e0a-151">Дополнительные сведения о корректировке запасов в наличии см. в разделе [Корректировка себестоимости запасов в наличии](../../supply-chain/cost-management/adjust-hand-inventory-cost-values.md).</span><span class="sxs-lookup"><span data-stu-id="c2e0a-151">For more information about the adjustment of on-hand inventory, see [Adjust on-hand inventory cost values](../../supply-chain/cost-management/adjust-hand-inventory-cost-values.md).</span></span>

1.  <span data-ttu-id="c2e0a-152">Закройте складские запасы, как описано в разделе [Закрытие запасов](#close-inventory) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-152">Close the inventory as described in the [Close inventory](#close-inventory) section earlier in this topic.</span></span>
2.  <span data-ttu-id="c2e0a-153">Перейдите **Управление запасами** \> **Периодические задачи** \> **Закрытие и коррекция**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-153">Go to **Inventory management** \> **Periodic tasks** \> **Closing and adjustment**.</span></span>
3.  <span data-ttu-id="c2e0a-154">В области действий выберите **Корректировка \> Наличие**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-154">On the Action Pane, select **Adjustment \> On-hand**.</span></span>
4.  <span data-ttu-id="c2e0a-155">На панели операций выберите **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-155">On the Action Pane, select **Select**.</span></span>
5.  <span data-ttu-id="c2e0a-156">В диалоговом окне **Выбрать запасы в наличии** укажите складские аналитики, которые должны отображаться после завершения корректировки.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-156">In the **Select on-hand inventory** dialog box, specify the inventory dimensions that should be shown after the adjustment is done.</span></span>

    ![Диалоговое окно выбора параметров запасов в наличии](media/3_Select_on-hand_inventory.png)

6.  <span data-ttu-id="c2e0a-158">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-158">Select **OK**.</span></span> <span data-ttu-id="c2e0a-159">На странице **Наличие** показаны строки запасов, выбранные для корректировки, вместе с указанными складскими аналитиками.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-159">The **On-hand** page shows the inventory lines that you selected for adjustment, together with the specified inventory dimensions.</span></span>
7.  <span data-ttu-id="c2e0a-160">Выберите строку для номенклатуры, а затем в поле **Код накладных расходов** выберите код накладных расходов для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-160">Select the line for an item, and then, in the **Charges code** field, select a charges code for the item.</span></span> <span data-ttu-id="c2e0a-161">Выбранный код накладных расходов вводится в сопоставление запасов после разноски корректировки.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-161">The selected miscellaneous charge code is entered in the inventory settlement after the adjustment is posted.</span></span>

    ![Страница наличия](media/4_On-hand.png)

8.  <span data-ttu-id="c2e0a-163">Чтобы ввести код накладных расходов во всех строках на странице **Наличие**, в области действий выберите **Корректировка** \> **Код накладных расходов**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-163">To enter the charges code on all lines of the **On hands** page, on the Action Pane, select **Adjustment** \> **Charges code**.</span></span>
9.  <span data-ttu-id="c2e0a-164">В диалоговом окне **Изменить код накладного расхода.** задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-164">In the **Change Misc. charge code** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c2e0a-165">В поле **Код накладных расходов** выберите код накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-165">In the **Charges code** field, select a charges code.</span></span>
    - <span data-ttu-id="c2e0a-166">Установите параметр **Применить ко всем** как **Да**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-166">Set the **Apply to all** option to **Yes**.</span></span> <span data-ttu-id="c2e0a-167">Если этот параметр имеет значение **Нет**, значение в поле **Код накладных расходов** будет скорректировано только в строке, выбранной на странице **Наличие**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-167">If this option is set to **No**, the value in the **Charges code** field will be adjusted only on the line that is selected on the **On hands** page.</span></span>

    ![Диалоговое окно изменения кода накладных расходов](media/5_Change_misc._charges_code.png)

10. <span data-ttu-id="c2e0a-169">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-169">Select **OK**.</span></span>
11. <span data-ttu-id="c2e0a-170">На панели операций выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-170">On the Action Pane, select **Post**.</span></span>
12. <span data-ttu-id="c2e0a-171">В диалоговом окне **Коррекция запасов в наличии** в поле **Детализация** выберите способ разноски корректировок проводок:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-171">In the **Adjustment of on-hand inventory** dialog box, in the **Specification** field, select how transaction adjustments are posted:</span></span>

    - <span data-ttu-id="c2e0a-172">**Все** — корректировки разносятся для всех номенклатур с одинаковыми параметрами в профиле разноски.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-172">**Total** – Adjustments are posted for all items that have the same settings in the posting profile.</span></span>
    - <span data-ttu-id="c2e0a-173">**Номенклатурная группа** — разнесение корректировок выполняется для всех номенклатур из такой же номенклатурной группы.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-173">**Item group** – Adjustments are posted for all items that have the same item group.</span></span>
    - <span data-ttu-id="c2e0a-174">**Код номенклатуры** — корректировки разносятся для каждой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-174">**Item number** – Adjustments are posted for each item.</span></span>

13. <span data-ttu-id="c2e0a-175">В поле **Примечание** введите примечание для корректировки.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-175">In the **Note** field, enter a note about the adjustment.</span></span>

    ![Диалоговое окно коррекции запасов в наличии](media/6_Adjustment_of_on-hand_inventory.png)

14. <span data-ttu-id="c2e0a-177">Выберите **ОК**, чтобы разнести корректировку.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-177">Select **OK** to post the adjustment.</span></span>

<span data-ttu-id="c2e0a-178">При разноске корректировки корр. счет главной книги определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-178">When you post an adjustment, the general ledger offset account is defined in the following way:</span></span>

   - <span data-ttu-id="c2e0a-179">Если код накладных расходов введен в строке номенклатуры, корректировка разносится на корр. счет, настроенный для кода накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-179">If the miscellaneous charges code is entered on the item line, the adjustment is posted to the offset account that is set up for the miscellaneous charges code.</span></span>
   - <span data-ttu-id="c2e0a-180">Если код накладных расходов не введен в строке номенклатуры, корректировка назначается для корр. счета прибылей и убытков, который настраивается на вкладке **Запасы** на странице **Разноска** (**Управление запасами** \> **Настройка** \> **Разноска** \> **Разноска**).</span><span class="sxs-lookup"><span data-stu-id="c2e0a-180">If the miscellaneous charges code isn't entered on the item line, the adjustment is assigned to the offset profit or loss account that is set up on the **Inventory tab** of the **Posting** page (**Inventory management** \> **Setup** \> **Posting** \> **Posting**).</span></span>

### <a name="adjust-transactions"></a><span data-ttu-id="c2e0a-181">Корректировать проводки</span><span class="sxs-lookup"><span data-stu-id="c2e0a-181">Adjust transactions</span></span>

1. <span data-ttu-id="c2e0a-182">Убедитесь, что запасы не закрыты.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-182">Verify that the inventory wasn't closed.</span></span> <span data-ttu-id="c2e0a-183">Если они были закрыты, отмените закрытие запасов, как описано в разделе [Отмена закрытия запасов](#cancel-inventory-closing) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-183">If it was closed, cancel the inventory closing as described in the [Cancel inventory closing](#cancel-inventory-closing) section earlier in this topic.</span></span>
2. <span data-ttu-id="c2e0a-184">Перейдите **Управление запасами** \> **Периодические задачи** \> **Закрытие и коррекция**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-184">Go to **Inventory management** \> **Periodic tasks** \> **Closing and adjustment**.</span></span>
3. <span data-ttu-id="c2e0a-185">В области действий выберите **Корректировка** \> **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-185">On the Action Pane, select **Adjustment** \> **Transactions**.</span></span>
4. <span data-ttu-id="c2e0a-186">На панели операций выберите **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-186">On the Action Pane, select **Select**.</span></span>
5. <span data-ttu-id="c2e0a-187">В диалоговом окне **Корректировка проводок** укажите критерии выбора для проводок прихода на склад, которые необходимо скорректировать ,а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-187">In the **Adjust transactions** dialog box, specify selection criteria for the inventory receipt transactions that must be adjusted, and then select **OK**.</span></span>

    ![Диалоговое окно корректировки проводок](media/7_Adjust_transactions.png)

6. <span data-ttu-id="c2e0a-189">Выберите коды накладных расходов для номенклатур и разнесите корректировку, как описано в разделе [Корректировка запасов в наличии](#adjust-on-hand-inventory) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-189">Select charges codes for items, and post the adjustment, as described in the [Adjust on-hand inventory](#adjust-on-hand-inventory) section earlier in this topic.</span></span> <span data-ttu-id="c2e0a-190">Корр. счет главной книги будет определяться в соответствии с тем же принципом.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-190">The general ledger offset account will be defined according to the same principle.</span></span>

### <a name="use-a-wizard-to-adjust-item-cost"></a><span data-ttu-id="c2e0a-191">Используйте мастера для корректировки затрат на номенклатуру</span><span class="sxs-lookup"><span data-stu-id="c2e0a-191">Use a wizard to adjust item cost</span></span> 

<span data-ttu-id="c2e0a-192">Для получения дополнительной информации о см. раздел [Мастер корректировки запасов](rus-inventory-adjustment-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="c2e0a-192">For more information, see [Inventory adjustment wizard](rus-inventory-adjustment-wizard.md).</span></span>

1. <span data-ttu-id="c2e0a-193">Перейдите **Управление запасами** \> **Периодические задачи** \> **Закрытие и коррекция**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-193">Go to **Inventory management** \> **Periodic tasks** \> **Closing and adjustment**.</span></span>
2. <span data-ttu-id="c2e0a-194">В области действий выберите **Корректировка** \> **Мастер**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-194">On the Action Pane, select **Adjustment** \> **Wizard**.</span></span>
3. <span data-ttu-id="c2e0a-195">На странице **Добро пожаловать** выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-195">On the **Welcome** page, select **Next**.</span></span>
4. <span data-ttu-id="c2e0a-196">На странице **Метод коррекции себестоимости** выберите метод корректировки:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-196">On the **Method of cost value adjustment** page, select the method of adjustment:</span></span>

    - <span data-ttu-id="c2e0a-197">**В наличии** — коррекция запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-197">**On-hand** – Adjust on-hand inventory.</span></span>
    - <span data-ttu-id="c2e0a-198">**Проводки** — корректировка проводок.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-198">**Transactions** – Adjust transactions.</span></span>

5. <span data-ttu-id="c2e0a-199">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-199">Select **Next**.</span></span> <span data-ttu-id="c2e0a-200">Отображается либо страница **Выбрать запасы в наличии**, либо страница **Корректировать проводки** в зависимости от выбранного метода корректировки.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-200">Either the **Select on-hand inventory** page or the **Adjust transactions** page appears, depending on the method of adjustment that you selected.</span></span>
6. <span data-ttu-id="c2e0a-201">Укажите критерии выбора, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-201">Specify selection criteria, and then select **OK**.</span></span>
7. <span data-ttu-id="c2e0a-202">На странице **Результат выбора** можно просмотреть номенклатуры в наличии или проводки по номенклатуре, которые выбраны для корректировки, затем нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-202">On the **Selection result** page, review the items or item transactions that have been selected for adjustment, and then select **Next**.</span></span>

    ![Страница результатов выбора](media/8_Selection_result.png)

8. <span data-ttu-id="c2e0a-204">На странице **Функции для вычисления корректирующих сумм** выберите метод расчета корректирующих сумм, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-204">On the **Functions for calculating adjustment amounts** page, select the method for calculating adjustment amounts, and then select **Next**.</span></span>

    ![Страница функций для вычисления корректирующих сумм](media/9_Functions_for_calculating_adjustments_amounts.png)

9. <span data-ttu-id="c2e0a-206">На странице **Результаты распределения** можно просмотреть результаты распределения.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-206">On the **Results of allocation** page, review the allocation results.</span></span> <span data-ttu-id="c2e0a-207">В поле **Код накладных расходов** выберите код накладных расходов для строки.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-207">In the **Charges code** field, select a charge code for a line.</span></span>

    ![Страница результатов распределения](media/10_Results_of_allocation.png)

10. <span data-ttu-id="c2e0a-209">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-209">Select **Next**.</span></span>
11. <span data-ttu-id="c2e0a-210">На странице **Разноска** укажите сведения для разноски корректировки:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-210">On the **Posting** page, specify the details for posting the adjustment:</span></span>

   - <span data-ttu-id="c2e0a-211">В поле **Дата корректировки** укажите дату корректировки.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-211">In the **Adjustment date** field, specify the date of the adjustment.</span></span>
   - <span data-ttu-id="c2e0a-212">В поле **Детализация** выберите способ разноски корректировок проводок:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-212">In the **Specification** field, select how transaction adjustments are posted:</span></span>

     - <span data-ttu-id="c2e0a-213">**Все** — корректировки разносятся для всех номенклатур с одинаковыми параметрами в профиле разноски.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-213">**Total** – Adjustments are posted for all items that have the same settings in the posting profile.</span></span>
     - <span data-ttu-id="c2e0a-214">**Номенклатурная группа** — разнесение корректировок выполняется для всех номенклатур из такой же номенклатурной группы.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-214">**Item group** – Adjustments are posted for all items that have the same item group.</span></span>
     - <span data-ttu-id="c2e0a-215">**Код номенклатуры** — корректировки разносятся для каждой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-215">**Item number** – Adjustments are posted for each item.</span></span>
   - <span data-ttu-id="c2e0a-216">Задайте параметр **Корр. счет Прибыли/Убытки** и поле **Корр. счет** в зависимости от счета, которому должна быть назначена корректировка во время разноски:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-216">Set the **Corr. account profit/loss** option and the **Corr. account** field, depending on the account that an adjustment should be assigned to during posting:</span></span>

     - <span data-ttu-id="c2e0a-217">Если код накладных расходов введен в строке номенклатуры, корректировка назначается корр. счету, настроенному для кода накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-217">If the miscellaneous charges code is entered on the item line, the adjustment will be assigned to the offset account that is set up for the miscellaneous charges code.</span></span>
     - <span data-ttu-id="c2e0a-218">Если код накладных расходов не введен в строке номенклатуры, а параметр **Корр. счет Прибыли/Убытки** на странице **Разноска** имеет значение **Да**, корректировка назначается обычным способом для корр. счета прибылей и убытков, который настраивается на вкладке **Запасы** на странице **Разноска** (**Управление запасами \> Настройка \> Разноска \> Разноска**).</span><span class="sxs-lookup"><span data-stu-id="c2e0a-218">If the miscellaneous charges code isn't entered on the item line, and if the **Corr. account profit/loss** option on the **Posting** page is set to **Yes**, the adjustment will be assigned, in the usual way, to the offset profit or loss account that is set up on the **Inventory** tab of the **Posting** page (**Inventory management \> Setup \> Posting \> Posting**).</span></span>
     - <span data-ttu-id="c2e0a-219">Если код накладных расходов не введен в строке номенклатуры, а параметр **Корр. счет Прибыли/Убытки** на странице **Разноска** имеет значение **Нет**, корректировка назначается счету, указанному в поле **Корр. счет**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-219">If the miscellaneous charges code isn't entered on the item line, and if the **Corr. account profit/loss** option on the **Posting** page is set to **No**, the adjustment will be assigned to the account that is specified in the **Corr. account** field.</span></span>

   ![Страница разноски](media/11_Posting.png)

12. <span data-ttu-id="c2e0a-221">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-221">Select **Next**.</span></span>
13. <span data-ttu-id="c2e0a-222">На странице **Готово** установите флажок **Показать список ваучеров ГК**, чтобы отобразить список ваучеров ГК.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-222">On the **Finish** page, select the **Show ledger voucher list** check box to show the ledger voucher list.</span></span>
14. <span data-ttu-id="c2e0a-223">Выберите **Готово**, чтобы разнести корректировку.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-223">Select **Finish** to post the adjustment.</span></span>

## <a name="view-item-cost-structure-in-the-inventory-settlements-and-cost-explorer"></a><span data-ttu-id="c2e0a-224">Просмотр структуры затрат номенклатуры в сопоставлениях запасов и анализаторе себестоимости</span><span class="sxs-lookup"><span data-stu-id="c2e0a-224">View item cost structure in the inventory settlements and cost explorer</span></span>

<span data-ttu-id="c2e0a-225">На странице **Сопоставления** можно просмотреть проводки корректировки себестоимости запасов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-225">On the **Settlements** page, you can view inventory cost adjustment transactions.</span></span> <span data-ttu-id="c2e0a-226">В результате закрытия запасов проводки прихода сопоставляются с проводками расхода.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-226">As a result of inventory closing, receipt transactions are settled against issue transactions.</span></span> <span data-ttu-id="c2e0a-227">После завершения закрытия запасов можно открыть страницу **Анализатор себестоимости** для просмотра и изучения структуры затрат номенклатуры с точки зрения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-227">After inventory closing is completed, you can open the **Cost explorer** page to view and explore the item cost structure in terms of miscellaneous charges.</span></span>

1. <span data-ttu-id="c2e0a-228">Закройте складские запасы, как описано в разделе [Закрытие запасов](#close-inventory) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-228">Close the inventory as described in the [Close inventory](#close-inventory) section earlier in this topic.</span></span>
2. <span data-ttu-id="c2e0a-229">Щелкните **Управление сведениями о продукте** \> **Продукты** \> **Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-229">Go to **Product information management** \> **Products** \> **Released products**.</span></span>
3. <span data-ttu-id="c2e0a-230">На странице **Сведения об используемых продуктах** выберите номенклатуру, затем, в области действий, на вкладке **Управление затратами**, в группе **Проводки затрат**, выберите **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-230">On the **Released products details** page, select an item, and then, on the Action Pane, on the **Manage Costs** tab, in the **Cost transactions** group, select **Transactions**.</span></span>
4. <span data-ttu-id="c2e0a-231">На странице **Проводки по запасам** выберите проводку для полученной номенклатуры, для которой необходимо просмотреть структуру затрат.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-231">On the **Inventory transactions** page, select the transaction on the receipt item that you want to explore the cost structure for.</span></span> <span data-ttu-id="c2e0a-232">Затем в области действий на вкладке **Склад** в группе **Учет затрат** выберите **Сопоставления**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-232">Then, on the Action Pane, on the **Inventory** tab, in the **Costing** group, select **Settlements**.</span></span>
5. <span data-ttu-id="c2e0a-233">На странице **Сопоставления** изучите следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="c2e0a-233">On the **Settlements** page, review the following information:</span></span>

    - <span data-ttu-id="c2e0a-234">В поле **Код расходов** показан код накладных расходов, который был распределен для проводки прихода номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-234">The **Charges code** field shows the miscellaneous charges code that has been allocated to the item receipt transaction.</span></span>
    - <span data-ttu-id="c2e0a-235">В поле **Счет поставщика** показан счет поставщика, у которого накладные расходы были приобретены.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-235">The **Vendor account** field shows the account of the vendor that the miscellaneous charges were bought from.</span></span> <span data-ttu-id="c2e0a-236">Дополнительные сведения о приобретении накладных расходов от стороннего поставщика см. в разделе [Накладные расходы третьей стороны](rus-third-party-misc-charges.md).</span><span class="sxs-lookup"><span data-stu-id="c2e0a-236">For more information about how to buy miscellaneous charges from a third-party vendor, see [Third party miscellaneous charges](rus-third-party-misc-charges.md).</span></span>

    - <span data-ttu-id="c2e0a-237">В поле **Накладная** показан номер накладной по закупке накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-237">The **Invoice** field shows the invoice number of the miscellaneous chargespurchase.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c2e0a-238">Если поля **Счет поставщика** и **Накладная** не заполнены, операция корректировки затрат была выполнена стандартным методом распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-238">If the **Vendor account** and **Invoice** fields are blank, the standard method of miscellaneous charges allocation was used to perform the cost adjustment operation.</span></span>

    ![Страница сопоставлений](media/12_Settlements.png)

6. <span data-ttu-id="c2e0a-240">На странице **Проводки по запасам** в области действий на вкладке **Запасы** в группе **Учет затрат** выберите **Анализатор себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-240">On the **Inventory transactions** page, on the Action Pane, on the **Inventory** tab, in the **Costing** group, select **Cost explorer**.</span></span>

    ![Страница анализатора себестоимости](media/13_Cost_explorer.png)

<span data-ttu-id="c2e0a-242">На страницах **Сопоставление** и **Анализатор себестоимости** коды накладных расходов с типом дебета **Номенклатура** и типом кредита **Счет ГК** отображаются в виде отдельной строки.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-242">On the **Settlements** and **Cost explorer** pages, the miscellaneous charges codes that have the **Item** debit type and the **Ledger account** credit type are shown as a separate line.</span></span> <span data-ttu-id="c2e0a-243">Коды накладных расходов с другими типами дебета и кредита включаются в себестоимость номенклатуры как прямые расходы (стандартная функция).</span><span class="sxs-lookup"><span data-stu-id="c2e0a-243">The miscellaneous charges codes that have other debit and credit types are included in the item cost price as direct charges (standard functionality).</span></span> <span data-ttu-id="c2e0a-244">Они не распределяются на странице **Сопоставления**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-244">They aren't allocated on the **Settlements** page.</span></span> <span data-ttu-id="c2e0a-245">Следовательно, они не отображаются на странице **Анализатор себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-245">Therefore, they aren't shown as a separate line on the **Cost explorer** page.</span></span>

<span data-ttu-id="c2e0a-246">Если поле **Код накладных расходов** на странице **Сопоставления** не задано, код накладных расходов не будет показан на странице **Анализатор себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-246">If the **Charges code** field on the **Settlements** page isn't set, a charges code won't be shown on the **Cost explorer** page.</span></span> <span data-ttu-id="c2e0a-247">Если поле **Код накладных расходов** на странице **Сопоставления** задано, код накладных расходов будет показан как отдельная строка на странице **Анализатор себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="c2e0a-247">If the **Charges code** field on the **Settlements** page is set, the charges code will be shown as a separate line on the **Cost explorer** page.</span></span>
