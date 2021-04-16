---
title: Регистрация товаров, отгруженных клиентам (Россия)
description: В этой теме объясняется, как зарегистрировать отгрузку и передачу прав собственности для товаров, которые транспортируются клиенту.
author: kfend
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Russia
ms.search.industry: ''
ms.author: kfend
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 3135751a0863beb2a537bb22aaa62d23a95cd42f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829766"
---
# <a name="register-goods-shipped-to-customers-russia"></a><span data-ttu-id="b761d-103">Регистрация товаров, отгруженных клиентам (Россия)</span><span class="sxs-lookup"><span data-stu-id="b761d-103">Register goods shipped to customers (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b761d-104">В соответствии с законодательством Российской Федерации компании необходимо зарегистрировать отгрузку товаров при транспортировке товаров клиенту.</span><span class="sxs-lookup"><span data-stu-id="b761d-104">In accordance with Russian legislation, a company must register the shipment of goods when goods are transported to a customer.</span></span> <span data-ttu-id="b761d-105">Когда товары отгружаются, право собственности на товары передается от продавца покупателю.</span><span class="sxs-lookup"><span data-stu-id="b761d-105">When goods are shipped, ownership of the goods is transferred from the seller to the buyer.</span></span> <span data-ttu-id="b761d-106">Такая передача права владения также называется передачей прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-106">This transfer of ownership is also referred to as the passing of property rights.</span></span>
<span data-ttu-id="b761d-107">Кроме того, можно отгружать товары, когда переход прав собственности откладывается на более позднюю дату.</span><span class="sxs-lookup"><span data-stu-id="b761d-107">You can also ship goods when the passing of property is postponed to a later date.</span></span> <span data-ttu-id="b761d-108">Клиент несет ответственность за товары только в том случае, когда происходит передача прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-108">The customer is liable for the goods only when the passing of property rights occurs.</span></span>
<span data-ttu-id="b761d-109">Включена следующая функциональность:</span><span class="sxs-lookup"><span data-stu-id="b761d-109">The following functionality is included:</span></span>

- <span data-ttu-id="b761d-110">Регистрация отгрузки в случае наличия отложенной передачи права собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-110">Registration of a shipment where there is postponed passing of property rights.</span></span>

  > <span data-ttu-id="b761d-111">[!ПРИМЕЧАНИЕ.] Хотя отгрузка не изменяет баланс клиента, поставщик все равно должен заплатить налог на добавленную стоимость (НДС).</span><span class="sxs-lookup"><span data-stu-id="b761d-111">[!NOTE:] Although the shipment doesn't change the customer's balance, the supplier must still pay value-added tax (VAT).</span></span> <span data-ttu-id="b761d-112">Товары перемещаются на специальный склад для отгруженных товаров.</span><span class="sxs-lookup"><span data-stu-id="b761d-112">The goods are moved to a special warehouse for shipped goods.</span></span>
  
- <span data-ttu-id="b761d-113">Регистрация передачи прав владения.</span><span class="sxs-lookup"><span data-stu-id="b761d-113">Registration of a transfer of ownership.</span></span> <span data-ttu-id="b761d-114">Эта регистрация включает регистрацию задолженности клиента и списание товаров, которые были проданы.</span><span class="sxs-lookup"><span data-stu-id="b761d-114">This registration includes registration of the customer's debt and write-off of the goods that were sold.</span></span>
- <span data-ttu-id="b761d-115">Отмена отгрузки в случае наличия отложенной передачи права собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-115">Cancellation of a shipment where there is postponed passing of property rights.</span></span>
- <span data-ttu-id="b761d-116">Распределение расходов по накладной по продаже.</span><span class="sxs-lookup"><span data-stu-id="b761d-116">Allocation of charges to a sales invoice.</span></span>

## <a name="settings"></a><span data-ttu-id="b761d-117">Настройки</span><span class="sxs-lookup"><span data-stu-id="b761d-117">Settings</span></span>
### <a name="set-up-a-warehouse"></a><span data-ttu-id="b761d-118">Настройка склада</span><span class="sxs-lookup"><span data-stu-id="b761d-118">Set up a warehouse</span></span>
1.  <span data-ttu-id="b761d-119">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Разделение запасов** \> **Склады**.</span><span class="sxs-lookup"><span data-stu-id="b761d-119">Go to **Inventory management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2.  <span data-ttu-id="b761d-120">Создайте склад типа **Товары отгруженные**.</span><span class="sxs-lookup"><span data-stu-id="b761d-120">Create a warehouse of the **Goods shipped** type.</span></span>

<span data-ttu-id="b761d-121">Для склада любого другого типа в поле **Склад для товаров отгруженных** можно указать склад **Товары отгруженные**, который должен использоваться для отгрузки товаров, когда имеется отсроченная передача прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-121">For a warehouse of any other type, in the **Warehouse for items shipped** field, you can specify a **Goods shipped** warehouse that should be used for the shipment of goods when there is postponed passing of property rights.</span></span>
<span data-ttu-id="b761d-122">Для склада типа **Товары отгруженные** можно задать местоположение для отгруженных номенклатур, если для номенклатур активирована аналитика **Местоположение**.</span><span class="sxs-lookup"><span data-stu-id="b761d-122">For a warehouse of the **Goods shipped** type, you can set a location for items that are shipped, if the **Location** dimension is activated for the items.</span></span>

### <a name="set-up-a-posting-type-and-number-sequences-for-passing-of-property-rights"></a><span data-ttu-id="b761d-123">Настройка типа разноски и номерных серий для передачи прав собственности</span><span class="sxs-lookup"><span data-stu-id="b761d-123">Set up a posting type and number sequences for passing of property rights</span></span>
1.  <span data-ttu-id="b761d-124">Перейдите в раздел **Расчеты с клиентами** \> **Настройка** \> **Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="b761d-124">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2.  <span data-ttu-id="b761d-125">На вкладке **Общие** на экспресс-вкладке **Значения по умолчанию для продаж** в поле **Тип разноски** выберите тип разноски:</span><span class="sxs-lookup"><span data-stu-id="b761d-125">On the **General** tab, on the **Sales default values** FastTab, in the **Posting type** field, select the type of posting:</span></span>

- <span data-ttu-id="b761d-126">**Стандартная** — права собственности передаются покупателю, когда разносится накладная по продаже.</span><span class="sxs-lookup"><span data-stu-id="b761d-126">**Standard** – Property rights are passed to the buyer when the sales invoice is posted.</span></span>
- <span data-ttu-id="b761d-127">**Отлож. переход прав собств-ти** — передача права собственности покупателю откладывается при разноске накладной заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b761d-127">**Postponed passing of property** – The passing of the property rights to the buyer is postponed when the sales invoice is posted.</span></span>

3.  <span data-ttu-id="b761d-128">На вкладке **Номерные серии** в поле **Код номерной серии** выберите номерную серию для пунктов **Журнал перехода прав собственности**, **Ваучер перехода прав собственности** и **Ссылки ваучера накладных расходов**.</span><span class="sxs-lookup"><span data-stu-id="b761d-128">On the **Number sequences** tab, in the **Number sequence code** field, select a number sequence for the **Journal of passing of property**, **Voucher of passing of property**, and **Charges voucher references**.</span></span>

### <a name="set-up-a-ledger-posting-group-to-post-shipped-goods-tax"></a><span data-ttu-id="b761d-129">Настройка группы разноски ГК для разноски налога за отправленные товары</span><span class="sxs-lookup"><span data-stu-id="b761d-129">Set up a ledger posting group to post shipped goods tax</span></span>
1.  <span data-ttu-id="b761d-130">Перейдите в раздел **Налог** \> **Настройка** \> **Налог** \> **Группы разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="b761d-130">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
2.  <span data-ttu-id="b761d-131">Выберите группу разноски главной книги и на экспресс-вкладке **Общее** в поле **Налог на товары отгруженные** выберите счет ГК для налога на отгруженные товары.</span><span class="sxs-lookup"><span data-stu-id="b761d-131">Select the ledger posting group and on the **General** FastTab in the **Shipped item tax** field, select a ledger account for shipped goods tax.</span></span>

### <a name="set-up-a-charge-code-that-uses-a-transit-account"></a><span data-ttu-id="b761d-132">Настройка кода накладных расходов, который использует транзитный счет</span><span class="sxs-lookup"><span data-stu-id="b761d-132">Set up a charge code that uses a transit account</span></span>
<span data-ttu-id="b761d-133">Страница **Код накладных расходов** служит для настройки кодов накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="b761d-133">Use the **Charges code** page to set up a charge code.</span></span> <span data-ttu-id="b761d-134">Можно также распределить расходы, воспользовавшись транзитным счетом.</span><span class="sxs-lookup"><span data-stu-id="b761d-134">You can allocate the charges by using a transit account.</span></span>

1.  <span data-ttu-id="b761d-135">Перейдите в раздел **Расчеты с клиентами** \> **Настройка** \> **Настройка накладных расходов** \> **Код накладных расходов**.</span><span class="sxs-lookup"><span data-stu-id="b761d-135">Go to **Accounts receivable** \> **Setup** \> **Charges setup** \> **Charges code**.</span></span>
2.  <span data-ttu-id="b761d-136">На экспресс-вкладке **Разноска** в разделе **Дебет** в поле **Тип** выберите **Клиент/Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="b761d-136">On the **Posting** FastTab, in the **Debit** section, in the **Type** field, select **Customer/Vendor**.</span></span>
3.  <span data-ttu-id="b761d-137">В разделе **Кредит** в поле **Тип** выберите **Счет ГК**.</span><span class="sxs-lookup"><span data-stu-id="b761d-137">In the **Credit** section, in the **Type** field, select **Ledger account**.</span></span>
4.  <span data-ttu-id="b761d-138">В разделе **Кредит** в поле **Разноска** выберите тип разноски для кредитового счета.</span><span class="sxs-lookup"><span data-stu-id="b761d-138">In the **Credit** section, in the **Posting** field, select the posting type for the credit account.</span></span>
5.  <span data-ttu-id="b761d-139">В разделе **Кредит** в поле **Счет** выберите номер счета, на который должны быть кредитованы накладные расходы.</span><span class="sxs-lookup"><span data-stu-id="b761d-139">In the **Credit** section, in the **Account** field, select the account number that the charge should be credited to.</span></span>
6.  <span data-ttu-id="b761d-140">Установите для параметра **Использовать транзитный счет** значение **Да**, чтобы использовать транзитный счет ГК для накладных расходов при разноске накладной заказа на продажу, где существует отложенная передача прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-140">Set the **Use transit account** option to **Yes** to use the transit ledger account for charges when you post a sales invoice where there is postponed passing of property rights.</span></span>

### <a name="set-up-revenue-consumption-and-transit-accounts-to-post-miscellaneous-sales-charges"></a><span data-ttu-id="b761d-141">Настройка счетов выручки, потребления и транзитного счета для разноски накладных расходов продажи</span><span class="sxs-lookup"><span data-stu-id="b761d-141">Set up revenue, consumption, and transit accounts to post miscellaneous sales charges</span></span>
1.  <span data-ttu-id="b761d-142">Перейдите в раздел **Расчеты с клиентами** \> **Настройка накладных расходов** \> **Разноска расходов**.</span><span class="sxs-lookup"><span data-stu-id="b761d-142">Go to **Accounts receivable** \> **Charges setup** \> **Charges posting**.</span></span>
2.  <span data-ttu-id="b761d-143">В группе полей **Тип разноски накладных расходов** выберите тип разноски для накладных расходов:</span><span class="sxs-lookup"><span data-stu-id="b761d-143">In the **Misc. charges posting type** field group, select the posting type for miscellaneous charges:</span></span>

  - <span data-ttu-id="b761d-144">**Выручка** — настройка счетов учета, на которые следует разносить выручку для накладных расходов продажи.</span><span class="sxs-lookup"><span data-stu-id="b761d-144">**Revenue** – Set up ledger accounts to post revenue for sales miscellaneous charges to.</span></span>
  - <span data-ttu-id="b761d-145">**Потребление** — настройка счетов учета, на которые следует разносить потребление для накладных расходов продажи.</span><span class="sxs-lookup"><span data-stu-id="b761d-145">**Consumption** – Set up ledger accounts to post consumption for sales miscellaneous charges to.</span></span>
  - <span data-ttu-id="b761d-146">**Транзитный счет** — настройка счетов ГК, на которые требуется разносить накладные расходы продажи для отложенной передачи прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-146">**Transit account** – Set up ledger accounts to post sales miscellaneous charges for postponed passing of property rights to.</span></span>

> [!NOTE]
> <span data-ttu-id="b761d-147">Необходимо настроить счета выручки, потребления и транзита для разноски заказов на продажу, в которых имеются накладные расходы и отложенный перенос прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-147">You must set up revenue, consumption, and transit accounts to post sales orders where there are miscellaneous charges and postponed passing of property rights.</span></span>

3.  <span data-ttu-id="b761d-148">В поле **Код счета** выберите связь счета:</span><span class="sxs-lookup"><span data-stu-id="b761d-148">In the **Account code** field, select an account relation:</span></span>

  - <span data-ttu-id="b761d-149">**Таблица** — задать связь счетов для конкретного клиента.</span><span class="sxs-lookup"><span data-stu-id="b761d-149">**Table** – The account relation is for a specific customer.</span></span>
  - <span data-ttu-id="b761d-150">**Группа** — задать связь счетов для списка групп клиентов.</span><span class="sxs-lookup"><span data-stu-id="b761d-150">**Group** – The account relation is for a list of customer groups.</span></span>
  - <span data-ttu-id="b761d-151">**Все** — задать связь счетов для всех клиентов.</span><span class="sxs-lookup"><span data-stu-id="b761d-151">**All** – The account relation is for all customers.</span></span>
  
4.  <span data-ttu-id="b761d-152">В поле **Связь счета** выберите клиента или группу клиентов для настройки связи счетов.</span><span class="sxs-lookup"><span data-stu-id="b761d-152">In the **Account relation** field, select the customer or customer group to set up an account relation.</span></span>
  > [!NOTE]
  > <span data-ttu-id="b761d-153">Это поле доступно, только если выбран вариант **Таблица** или **Группа** в поле **Связь счета**.</span><span class="sxs-lookup"><span data-stu-id="b761d-153">This field is available only if you selected **Table** or **Group** in the **Account code** field.</span></span>
  
5.  <span data-ttu-id="b761d-154">В поле **Связь накл. расходов** выберите код накладных расходов:</span><span class="sxs-lookup"><span data-stu-id="b761d-154">In the **Misc. charges relation** field, select a miscellaneous charges code:</span></span>
  - <span data-ttu-id="b761d-155">**Таблица** — разноска настраивается для определенного кода накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="b761d-155">**Table** – Posting is set up for a specific miscellaneous charges code.</span></span>
  - <span data-ttu-id="b761d-156">**Все** — разноска настраивается для всех кодов накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="b761d-156">**All** – Posting is set up for all miscellaneous charges codes.</span></span>
  
6.  <span data-ttu-id="b761d-157">В поле **Код накладных расходов** выберите код накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="b761d-157">In the **Charges code** field, select the miscellaneous charges code.</span></span>
  > [!NOTE]
  > <span data-ttu-id="b761d-158">Это поле доступно, только если выбран вариант **Таблица** в поле **Связь накл. расходов**.</span><span class="sxs-lookup"><span data-stu-id="b761d-158">This field is available only if you selected **Table** in the **Misc. charges relation** field.</span></span>
  
7.  <span data-ttu-id="b761d-159">В поле **Счет ГК** выберите счет учета, на который разносятся проводки.</span><span class="sxs-lookup"><span data-stu-id="b761d-159">In the **Main account** field, select the ledger account that the transactions are posted to.</span></span>
8.  <span data-ttu-id="b761d-160">В поле **Тип разноски** выберите тип разноски для разноски накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="b761d-160">In the **Posting type** field, select the posting type for posting miscellaneous charges.</span></span>

### <a name="set-up-ledger-accounts-and-offset-ledger-accounts-for-shipped-goods"></a><span data-ttu-id="b761d-161">Настройка счетов учета и корр. счетов учета для отгруженных товаров</span><span class="sxs-lookup"><span data-stu-id="b761d-161">Set up ledger accounts and offset ledger accounts for shipped goods</span></span>
1.  <span data-ttu-id="b761d-162">Выберите **Управление запасами** \> **Настройка** \> **Разноска** \> **Разноска**.</span><span class="sxs-lookup"><span data-stu-id="b761d-162">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
2.  <span data-ttu-id="b761d-163">На вкладке **Заказ на продажу** в левой области выберите тип счета учета для настройки отгруженных товаров:</span><span class="sxs-lookup"><span data-stu-id="b761d-163">On the **Sales order** tab, in the left pane, select the type of ledger account to set up for shipped goods:</span></span>

  - <span data-ttu-id="b761d-164">**Товары отгруженные** — настройка счетов учета для разноски проводок главной книги для отгруженных товаров.</span><span class="sxs-lookup"><span data-stu-id="b761d-164">**Goods shipped** – Set up ledger accounts to post the ledger transactions for shipped goods to.</span></span>
  - <span data-ttu-id="b761d-165">**Корр. счет товаров отгруженных** — настройка корр. счетов учета для разноски проводок главной книги для отгруженных товаров.</span><span class="sxs-lookup"><span data-stu-id="b761d-165">**oods shipped offset** – Set up offset ledger accounts to post the ledger transactions for shipped goods to.</span></span>
  
3.  <span data-ttu-id="b761d-166">В поле **Код номенклатуры** выберите связь номенклатуры:</span><span class="sxs-lookup"><span data-stu-id="b761d-166">In the **Item code** field, select an item relation:</span></span>

  - <span data-ttu-id="b761d-167">**Таблица** — код номенклатуры относится к конкретной номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="b761d-167">**Table** – The item code is for a specific item.</span></span>
  - <span data-ttu-id="b761d-168">**Группа** — код номенклатуры относится к конкретной группе номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b761d-168">**Group** – The item code is for a specific item group.</span></span>
  - <span data-ttu-id="b761d-169">**Все** — код номенклатуры для всей номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b761d-169">**All** – The item code is for all items.</span></span>
  
4.  <span data-ttu-id="b761d-170">В поле **Связь номенклатуры** выберите номенклатуру или номенклатурную группу.</span><span class="sxs-lookup"><span data-stu-id="b761d-170">In the **Item relation** field, select an item or item group.</span></span>

  >[!NOTE]
  > <span data-ttu-id="b761d-171">Это поле доступно, только если выбран вариант **Таблица** или **Группа** в поле **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="b761d-171">This field is available only if you selected **Table** or **Group** in the **Item code** field.</span></span>
  
5.  <span data-ttu-id="b761d-172">В поле **Код счета** выберите связь счета:</span><span class="sxs-lookup"><span data-stu-id="b761d-172">In the **Account code** field, select an account relation:</span></span>

  - <span data-ttu-id="b761d-173">**Таблица** — задать связь счетов для конкретного клиента.</span><span class="sxs-lookup"><span data-stu-id="b761d-173">**Table** – The account relation is for a specific customer.</span></span>
  - <span data-ttu-id="b761d-174">**Группа** — задать связь счетов для списка групп клиентов.</span><span class="sxs-lookup"><span data-stu-id="b761d-174">**Group** – The account relation is for a list of customer groups.</span></span>
  - <span data-ttu-id="b761d-175">**Все** — задать связь счетов для всех клиентов.</span><span class="sxs-lookup"><span data-stu-id="b761d-175">**All** – The account relation is for all customers.</span></span>
  
6.  <span data-ttu-id="b761d-176">В поле **Связь счета** выберите клиента или группу клиентов для настройки связи счетов.</span><span class="sxs-lookup"><span data-stu-id="b761d-176">In the **Account relation** field, select a customer or customer group to set up an account relation.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b761d-177">Это поле доступно, только если выбран вариант **Таблица** или **Группа** в поле **Связь счета**.</span><span class="sxs-lookup"><span data-stu-id="b761d-177">This field is available only if you selected **Table** or **Group** in the **Account code** field.</span></span>
  
7.  <span data-ttu-id="b761d-178">В поле **Настройка налоговой группы** выберите налоговую группу.</span><span class="sxs-lookup"><span data-stu-id="b761d-178">In the **Sales tax group** field, select a sales tax group.</span></span>
8.  <span data-ttu-id="b761d-179">В поле **Счет ГК** выберите номер счета ГК.</span><span class="sxs-lookup"><span data-stu-id="b761d-179">In the **Main account** field, select the ledger account number.</span></span>

### <a name="set-up-a-posting-type-for-a-customer-and-an-agreement"></a><span data-ttu-id="b761d-180">Настройка типа разноски для клиента и соглашения</span><span class="sxs-lookup"><span data-stu-id="b761d-180">Set up a posting type for a customer and an agreement</span></span>
1.  <span data-ttu-id="b761d-181">Перейдите в раздел **Расчеты с клиентами** \> **Клиенты** \> **Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="b761d-181">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2.  <span data-ttu-id="b761d-182">Выберите счет клиента.</span><span class="sxs-lookup"><span data-stu-id="b761d-182">Select a customer account.</span></span>
3.  <span data-ttu-id="b761d-183">На экспресс-вкладке **Значения заказов на продажу по умолчанию** в поле **Тип разноски** выберите тип разноски:</span><span class="sxs-lookup"><span data-stu-id="b761d-183">On the **Sales order defaults** FastTab, in the **Posting type** field, select the posting type:</span></span>

  - <span data-ttu-id="b761d-184">**Стандартная** — права собственности передаются клиенту, когда разносится накладная по продаже.</span><span class="sxs-lookup"><span data-stu-id="b761d-184">**Standard** – Property rights are passed to the customer when the sales invoice is posted.</span></span>
  - <span data-ttu-id="b761d-185">**Отлож. переход прав собств-ти** — передача права собственности клиенту откладывается при разноске накладной заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b761d-185">**Postponed passing of property** – The passing of the property rights to the customer is postponed when the sales invoice is posted.</span></span>
  
4.  <span data-ttu-id="b761d-186">Перейдите в раздел **Продажи и маркетинг** \> **Договоры продажи** \> **Договоры продажи**.</span><span class="sxs-lookup"><span data-stu-id="b761d-186">Go to **Sales and marketing** \> **Sales agreements** \> **Sales agreements**.</span></span>
5.  <span data-ttu-id="b761d-187">Выберите договор продажи.</span><span class="sxs-lookup"><span data-stu-id="b761d-187">Select a sales agreement.</span></span>
6.  <span data-ttu-id="b761d-188">Перейдите к представлению **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="b761d-188">Switch to the **Header** view.</span></span>
7.  <span data-ttu-id="b761d-189">На экспресс-вкладке **Финансы** в поле **Тип разноски** выберите тип разноски:</span><span class="sxs-lookup"><span data-stu-id="b761d-189">On the **Financial** FastTab, in the **Posting type** field, select the posting type:</span></span>

  - <span data-ttu-id="b761d-190">**Стандартная** — права собственности передаются клиенту, когда разносится накладная по продаже.</span><span class="sxs-lookup"><span data-stu-id="b761d-190">**Standard** – Property rights are passed to the customer when the sales invoice is posted.</span></span>
  - <span data-ttu-id="b761d-191">**Отлож. переход прав собств-ти** — передача права собственности клиенту откладывается при разноске накладной заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b761d-191">**Postponed passing of property** – The passing of the property rights to the customer is postponed when the sales invoice is posted.</span></span>

## <a name="working-with-sales-invoices-where-there-is-postponed-passing-of-property-rights"></a><span data-ttu-id="b761d-192">Работа с накладными по продаже, в которых имеется отсроченный переход прав собственности</span><span class="sxs-lookup"><span data-stu-id="b761d-192">Working with sales invoices where there is postponed passing of property rights</span></span>
<span data-ttu-id="b761d-193">Выполните процедуры, описанные в этом разделе, чтобы создать заказ на продажу, в котором имеется отсроченный перенос прав собственности, разнесите накладную заказа на продажу и зарегистрируйте передачу прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-193">Complete the procedures in this section to create a sales order where there is postponed passing of property rights, post the sales invoice, and register the passing of property rights.</span></span>

### <a name="create-a-sales-order-and-post-a-sales-invoice-where-there-is-postponed-passing-of-property-rights"></a><span data-ttu-id="b761d-194">Создание заказа на продажу и разноска накладной заказа на продажу, где имеется отложенный перенос прав собственности</span><span class="sxs-lookup"><span data-stu-id="b761d-194">Create a sales order and post a sales invoice where there is postponed passing of property rights</span></span>
1.  <span data-ttu-id="b761d-195">Перейдите в раздел **Расчеты с клиентами** \> **Заказы** \> **Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="b761d-195">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2.  <span data-ttu-id="b761d-196">Создание заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b761d-196">Create a sales order.</span></span>
3.  <span data-ttu-id="b761d-197">Перейдите к представлению **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="b761d-197">Switch to the **Header** view.</span></span>
4.  <span data-ttu-id="b761d-198">На экспресс-вкладке **Настройка** в поле **Тип разноски** выберите **Отлож. переход прав собств-ти**.</span><span class="sxs-lookup"><span data-stu-id="b761d-198">On the **Setup** FastTab, in the **Posting type** field, select **Postponed passing of property**.</span></span>
5.  <span data-ttu-id="b761d-199">В поле **Налоговая группа** выберите налоговую группу для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b761d-199">In the **Sales tax group** field, select the sales tax group for the sales order.</span></span>
6.  <span data-ttu-id="b761d-200">Перейдите обратно в представление **Строки**.</span><span class="sxs-lookup"><span data-stu-id="b761d-200">Switch back to **Lines** view.</span></span>
7.  <span data-ttu-id="b761d-201">Создайте строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b761d-201">Create sales order lines.</span></span> <span data-ttu-id="b761d-202">В поле **Налоговая группа номенклатур** выберите налоговую группу.</span><span class="sxs-lookup"><span data-stu-id="b761d-202">In the **Item sales tax group** field, select the sales tax group.</span></span>
8.  <span data-ttu-id="b761d-203">Разноска накладной.</span><span class="sxs-lookup"><span data-stu-id="b761d-203">Post the invoice.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b761d-204">Чтобы разнести накладную типа **Отлож. переход прав собств-ти**, убедитесь, что условия оплаты, назначенные для заказов на продажу, не используют оплату наличными, и что для поля **Вида деятельности** не установлено значение **Хранитель** или **Комиссионер**.</span><span class="sxs-lookup"><span data-stu-id="b761d-204">To post an invoice of the **Postponed passing of property** type, make sure that the terms of payment that are assigned to the sales orders aren't for a cash payment, and that the **Kind of activity** field isn't set to **Bailee** or **Commission agent**.</span></span>

<span data-ttu-id="b761d-205">Для каждой складской проводки со статусом расхода **Продано** создаются две дополнительные складские проводки для **Склад отгруженных товаров**: одна проводка имеет статус прихода **Куплено**, а другая проводка имеет статус выпуска **Списано**.</span><span class="sxs-lookup"><span data-stu-id="b761d-205">For each inventory transaction that has an issue status of **Sold**, two additional inventory transactions are created for the **Goods shipped warehouse**: one transaction has a receipt status of **Purchased**, and the other transaction has an issue status of **Deducted**.</span></span>
<span data-ttu-id="b761d-206">На этом этапе не создаются проводки сальдо клиента и выручки.</span><span class="sxs-lookup"><span data-stu-id="b761d-206">No customer balance and revenue transactions are generated at this point.</span></span>
<span data-ttu-id="b761d-207">Следующие проводки ГК создаются:</span><span class="sxs-lookup"><span data-stu-id="b761d-207">The following ledger transactions are generated:</span></span>

  - <span data-ttu-id="b761d-208">**Дебет**: заказ на продажу, корр. счет товаров отгруженных; **Кредит**: стоимость единиц измерения с выставленными накладными</span><span class="sxs-lookup"><span data-stu-id="b761d-208">**Debit**: Sales order, Goods shipped offset; **Credit**: Cost of units, invoiced</span></span>
  - <span data-ttu-id="b761d-209">**Дебет**: заказ на продажу, отгруженные товары; **Кредит**: заказ на продажу, корр. счет товаров отгруженных</span><span class="sxs-lookup"><span data-stu-id="b761d-209">**Debit**: Sales order, Goods shipped; **Credit**: Sales order, Goods shipped offset</span></span>
  - <span data-ttu-id="b761d-210">**Дебет**: налог на товары отгруженные; **Кредит**: исходящий налог</span><span class="sxs-lookup"><span data-stu-id="b761d-210">**Debit**: Shipped items tax; **Credit**: Sales tax payable</span></span>

### <a name="allocate-miscellaneous-charges-to-a-sales-invoice"></a><span data-ttu-id="b761d-211">Распределение накладных расходов для накладной заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="b761d-211">Allocate miscellaneous charges to a sales invoice</span></span>
<span data-ttu-id="b761d-212">Диалоговое окно **Распределить накладные расходы** служит для отнесения расходов на разнесенную накладную по продаже.</span><span class="sxs-lookup"><span data-stu-id="b761d-212">Use the **Allocate charges** dialog box to allocate charges to a posted sales invoice.</span></span>
1.  <span data-ttu-id="b761d-213">Перейдите в раздел **Расчеты с клиентами** \> **Запросы и отчеты** \> **Накладные** \> **Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="b761d-213">Go to **Accounts receivable** \> **Inquiries and reports** \> **Invoices** \> **Invoice journal**.</span></span>
2.  <span data-ttu-id="b761d-214">Выберите накладную заказа на продажу типа разноски **Отлож. переход прав собств-ти**, затем выберите **Корректировка**, чтобы открыть диалоговое окно **Распределить накладные расходы**.</span><span class="sxs-lookup"><span data-stu-id="b761d-214">Select a sales invoice of the **Postponed passing of property** posting type, and then select **Adjustment** to open the **Allocate charges** dialog box.</span></span>
3.  <span data-ttu-id="b761d-215">В поле **Дата разноски** введите дату, когда накладные расходы необходимо разнести.</span><span class="sxs-lookup"><span data-stu-id="b761d-215">In the **Posting date** field, enter the date when miscellaneous charges should be posted.</span></span>
4.  <span data-ttu-id="b761d-216">Установите для параметра **Корректировка по кредиту** значение **Да**, чтобы указать, что накладные расходы должны разноситься как корректировки по кредиту.</span><span class="sxs-lookup"><span data-stu-id="b761d-216">Set the **Credit correction** option to **Yes** to indicate that charges should be posted as credit corrections.</span></span>
5.  <span data-ttu-id="b761d-217">В поле **Код накладных расходов** выберите код расходов.</span><span class="sxs-lookup"><span data-stu-id="b761d-217">In the **Charges code** field, select the charge code.</span></span> <span data-ttu-id="b761d-218">В этом поле перечислены только расходы, для которых поле **Тип** в разделах **Дебет** и **Кредит** имеет значение **Счет ГК**.</span><span class="sxs-lookup"><span data-stu-id="b761d-218">This field lists only charges where the **Type** field in both the **Debit** and **Credit** sections is set to **Ledger account**.</span></span>
6.  <span data-ttu-id="b761d-219">В поле **Значение расходов** введите значение расхода.</span><span class="sxs-lookup"><span data-stu-id="b761d-219">In the **Charges value** field, enter the value of the charge.</span></span>
7.  <span data-ttu-id="b761d-220">Выберите **ОК** для разноски расхода на накладную по продаже.</span><span class="sxs-lookup"><span data-stu-id="b761d-220">Select **OK** to post the charge to the sales invoice.</span></span>

### <a name="cancel-a-shipment-for-the-passing-of-property-rights"></a><span data-ttu-id="b761d-221">Отмена отгрузки для передачи прав собственности</span><span class="sxs-lookup"><span data-stu-id="b761d-221">Cancel a shipment for the passing of property rights</span></span>
<span data-ttu-id="b761d-222">Диалоговое окно **Отмена отгрузки** используется для отмены отгрузки.</span><span class="sxs-lookup"><span data-stu-id="b761d-222">Use the **Cancel shipment** dialog box to cancel a shipment.</span></span> <span data-ttu-id="b761d-223">Можно отменить отгрузку для товаров, если передача прав собственности не была полностью или частично зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="b761d-223">You can cancel the shipment for goods if the passing of property rights isn't fully or partially registered.</span></span> <span data-ttu-id="b761d-224">При отмене отгрузки создается кредит-нота.</span><span class="sxs-lookup"><span data-stu-id="b761d-224">When you cancel a shipment, a credit note is created.</span></span>
1.  <span data-ttu-id="b761d-225">Перейдите в раздел **Расчеты с клиентами** \> **Запросы и отчеты** \> **Накладные** \> **Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="b761d-225">Go to **Accounts receivable** \> **Inquiries and reports** \> **Invoices** \> **Invoice journal**.</span></span>
2.  <span data-ttu-id="b761d-226">Выберите накладную заказа на продажу для типа разноски **Отлож. переход прав собств-ти**.</span><span class="sxs-lookup"><span data-stu-id="b761d-226">Select a sales invoice of the **Postponed passing of property** posting type.</span></span>
3.  <span data-ttu-id="b761d-227">Выберите **Переход прав собственности** \> **Отмена отгрузки**, чтобы открыть диалоговое окно **Отмена отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="b761d-227">Select **Passing of property** \> **Shipment cancellation** to open the **Cancel shipment** dialog box.</span></span>
4.  <span data-ttu-id="b761d-228">В разделе **Обработка** в поле **Дата** выберите дату отмены.</span><span class="sxs-lookup"><span data-stu-id="b761d-228">In the **Processing** section, in the **Date** field, select the date of cancellation.</span></span>
5.  <span data-ttu-id="b761d-229">Установите для параметра **Корректировка по кредиту (физическая)** значение **Да**, чтобы указать, что физическое обновление запасов должно разноситься как корректировка по кредиту.</span><span class="sxs-lookup"><span data-stu-id="b761d-229">Set the **Credit correction (physical)** option to **Yes** to indicate that physical inventory update should be posted as a credit correction.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b761d-230">Этот параметр автоматически устанавливается в значение **Да**, если для параметра **Сторно для физической разноски** задано значение **Да** на вкладке **Учет запасов** на странице **Параметры модуля "Управление запасами и складами"**.</span><span class="sxs-lookup"><span data-stu-id="b761d-230">This option is automatically set to **Yes** if the **Storno for physical posting** option is set to **Yes** on the **Inventory accounting** tab of the **Inventory and warehouse management parameters** page.</span></span>
  
6.  <span data-ttu-id="b761d-231">Установите для параметра **Корректирующая кредит-нота** значение **Да**, чтобы разнести проводку по кредит-ноте как корректировку по кредиту.</span><span class="sxs-lookup"><span data-stu-id="b761d-231">Set the **Credit note as correction** option to **Yes** to post the credit note transaction as a credit correction.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b761d-232">Этот параметр автоматически устанавливается в значение **Да**, если для параметра **Корректирующая кредит-нота** выбрано значение **Да** на вкладке **Обновления** на странице **Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="b761d-232">This option is automatically set to **Yes** if the **Credit note as correction** option is set to **Yes** on the **Updates** tab of the **Accounts receivable parameters** page.</span></span>
  
7.  <span data-ttu-id="b761d-233">Установите для параметра **Кредитовать оставшееся количество** значение **Да**, чтобы восстановить открытое количество заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b761d-233">Set the **Credit remaining quantity** option to **Yes** to restore the open quantity of the sales order.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b761d-234">Когда накладная по продаже отменяется, количество, определенное в заказе на продажу, открыто для другой отгрузки.</span><span class="sxs-lookup"><span data-stu-id="b761d-234">When a sales invoice is canceled, the quantity that is specified in the sales order is open for another shipment.</span></span>
  
8.  <span data-ttu-id="b761d-235">Установите для параметра **Корректирующий документ** значение **Да**, чтобы предоставить ссылку на исходную накладную заказа на продажу в кредит-ноте.</span><span class="sxs-lookup"><span data-stu-id="b761d-235">Set the **Corrective document** option to **Yes** to provide a reference to the source sales invoice in the credit note.</span></span>
9.  <span data-ttu-id="b761d-236">Для выбора одной или нескольких строк накладной для отмены используется поле **Пометка**.</span><span class="sxs-lookup"><span data-stu-id="b761d-236">Use the **Mark** field to select one or more invoice lines for cancellation.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b761d-237">Чтобы выбрать все строки накладной, можно установить для параметра **Выбрать все** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="b761d-237">To select all invoice lines, you can set the **Select all** option to **Yes**.</span></span>
  
10. <span data-ttu-id="b761d-238">В поле **Для обработки** введите количество, для которого должна быть отменена отгрузка.</span><span class="sxs-lookup"><span data-stu-id="b761d-238">In the **For processing** field, enter the quantity that shipment should be canceled for.</span></span>
11. <span data-ttu-id="b761d-239">Выберите **ОК**, чтобы отменить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="b761d-239">Select **OK** to cancel the shipment.</span></span>
12. <span data-ttu-id="b761d-240">Закройте страницу **Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="b761d-240">Close the **Invoice journal** page.</span></span>

### <a name="register-the-passing-of-property-rights-for-a-posted-sales-invoice"></a><span data-ttu-id="b761d-241">Регистрация передачи прав собственности для разнесенной накладной по продаже</span><span class="sxs-lookup"><span data-stu-id="b761d-241">Register the passing of property rights for a posted sales invoice</span></span>
<span data-ttu-id="b761d-242">Для регистрации передачи прав собственности для разнесенной накладной заказа на продажу используется диалоговое окно **Регистрация перехода прав собственности**.</span><span class="sxs-lookup"><span data-stu-id="b761d-242">Use the **Register a passing of property** dialog box to register the passing of property rights for a posted sales invoice.</span></span> <span data-ttu-id="b761d-243">Каждая строка накладной в диалоговом окне содержит количество, для которого должна быть зарегистрирована передача прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-243">Each invoice line in the dialog box contains the quantity that the passing of property rights must be registered for.</span></span> <span data-ttu-id="b761d-244">Для подтверждения передачи прав собственности можно указать дату и количество в строке накладной.</span><span class="sxs-lookup"><span data-stu-id="b761d-244">You can specify a date and the quantity on the invoice line to confirm the passing of property rights.</span></span> <span data-ttu-id="b761d-245">Начисленный налог и накладные расходы пересчитываются на основе количества, даты отгрузки и даты передачи прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-245">The sales tax charges and miscellaneous charges are recalculated based on the quantity, date of shipment, and the date of the passing of property rights.</span></span>
1.  <span data-ttu-id="b761d-246">Перейдите в раздел **Расчеты с клиентами** \> **Запросы и отчеты** \> **Накладные** \> **Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="b761d-246">Go to **Accounts receivable** \> **Inquiries and reports** \> **Invoices** \> **Invoice journal**.</span></span>
2.  <span data-ttu-id="b761d-247">Выберите накладную заказа на продажу для типа разноски **Отлож. переход прав собств-ти**.</span><span class="sxs-lookup"><span data-stu-id="b761d-247">Select a sales invoice of the **Postponed passing of property** posting type.</span></span>
3.  <span data-ttu-id="b761d-248">Выберите **Переход прав собственности** \> **Переход прав собственности**, чтобы открыть диалоговое окно **Регистрация перехода прав собственности**.</span><span class="sxs-lookup"><span data-stu-id="b761d-248">Select **Passing of property** \> **Passing of property** to open the **Register a passing of property** dialog box.</span></span>
4.  <span data-ttu-id="b761d-249">В разделе **Обработка** в поле **Дата** выберите дату перехода прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-249">In the **Processing** section, in the **Date** field, select the date of the passing of property rights.</span></span>
5.  <span data-ttu-id="b761d-250">Для выбора одной или нескольких строк накладной для перехода прав собственности используется поле **Пометка**.</span><span class="sxs-lookup"><span data-stu-id="b761d-250">Use the **Mark** field to select one or more invoice lines for the passing of property rights.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b761d-251">Чтобы выбрать все строки накладной, можно установить для параметра **Выбрать все** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="b761d-251">To select all invoice lines, you can set the **Select all** option to **Yes**.</span></span>
  
6.  <span data-ttu-id="b761d-252">В поле **Для обработки** выберите количество, регистрируемое для передачи прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-252">In the **For processing** field, select the quantity to register the passing of property rights for.</span></span>
7.  <span data-ttu-id="b761d-253">Выберите **ОК**, чтобы зарегистрировать передачу прав собственности.</span><span class="sxs-lookup"><span data-stu-id="b761d-253">Select **OK** to register the passing of property rights.</span></span>
<span data-ttu-id="b761d-254">На этом этапе создаются проводки сальдо клиента и выручки.</span><span class="sxs-lookup"><span data-stu-id="b761d-254">At this point, the customer balance and revenue transactions are created.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b761d-255">Накладные расходы обрабатываются как общая сумма, независимо от того, была ли регистрация передачи прав собственности полностью обработана или частично обработана.</span><span class="sxs-lookup"><span data-stu-id="b761d-255">The charges are processed as a total amount, regardless of whether the registration of the passing of property rights is fully processed or partially processed.</span></span>
  
<span data-ttu-id="b761d-256">Следующие проводки ГК разносятся:</span><span class="sxs-lookup"><span data-stu-id="b761d-256">The following ledger transactions are posted:</span></span>

  - <span data-ttu-id="b761d-257">**Дебет**: себестоимость проданных товаров, по которым выставлена накладная; **Кредит**: заказ на продажу, корр. счет товаров отгруженных</span><span class="sxs-lookup"><span data-stu-id="b761d-257">**Debit**: Cost of goods sold, invoiced; **Credit**: Sales order, Goods shipped</span></span>
  - <span data-ttu-id="b761d-258">**Дебет**: корр. счет уплаты (налог); **Кредит**: исходящий налог</span><span class="sxs-lookup"><span data-stu-id="b761d-258">**Debit**: Payment offset account (Sales tax); **Credit**: Shipped items tax</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]