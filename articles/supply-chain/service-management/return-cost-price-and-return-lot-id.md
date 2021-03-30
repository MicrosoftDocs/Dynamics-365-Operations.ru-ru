---
title: Себестоимость по возврату и номер возвращенного лота
description: Может потребоваться, чтобы стоимость возвращенных продуктов совпадала со стоимостью продуктов на момент их продажи клиенту. Это можно сделать с помощью параметра **Номер возвращенного лота**.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b420c0716823f587ea3f349a5d654ace23d84f41
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219277"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="6c41f-104">Себестоимость по возврату и номер возвращенного лота</span><span class="sxs-lookup"><span data-stu-id="6c41f-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="6c41f-105">Стоимость продуктов, возвращенных на склад, рассчитывается с учетом текущей стоимости продуктов.</span><span class="sxs-lookup"><span data-stu-id="6c41f-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="6c41f-106">Однако может потребоваться, чтобы стоимость возвращенных продуктов совпадала со стоимостью продуктов на момент их продажи клиенту.</span><span class="sxs-lookup"><span data-stu-id="6c41f-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="6c41f-107">Это можно сделать с помощью поля **Номер возвращенного лота** на экспресс-вкладке **Сведения по строке** в форме **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="6c41f-108">Рассмотрим следующий сценарий.</span><span class="sxs-lookup"><span data-stu-id="6c41f-108">For example, consider the following scenario.</span></span> <span data-ttu-id="6c41f-109">Клиент получает накладную.</span><span class="sxs-lookup"><span data-stu-id="6c41f-109">You invoice a customer.</span></span> <span data-ttu-id="6c41f-110">Затем он возвращает вам поставленные продукты.</span><span class="sxs-lookup"><span data-stu-id="6c41f-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="6c41f-111">Вы возвращаете продукты на склад.</span><span class="sxs-lookup"><span data-stu-id="6c41f-111">You return the products to stock.</span></span> <span data-ttu-id="6c41f-112">В этом случае при кредитовании клиента за возвращенные продукты стоимость этих продуктов рассчитывается с учетом текущей стоимости продуктов.</span><span class="sxs-lookup"><span data-stu-id="6c41f-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="6c41f-113">Однако, если используется поле **Номер возвращенного лота**, стоимость возвращенных продуктов рассчитывается с учетом стоимости, указанной в накладной при исходной продаже клиенту.</span><span class="sxs-lookup"><span data-stu-id="6c41f-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="6c41f-114">Чтобы использовать стоимость, отличную от текущей стоимости, для возвратов от клиентов, воспользуйтесь одним из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="6c41f-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="6c41f-115">Метод 1. Ввод себестоимости возврата вручную</span><span class="sxs-lookup"><span data-stu-id="6c41f-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="6c41f-116">По умолчанию при добавлении номенклатур в заказ на возврат номенклатуры возвращаются на склад по текущей себестоимости.</span><span class="sxs-lookup"><span data-stu-id="6c41f-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="6c41f-117">Чтобы указать другую себестоимость возврата, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6c41f-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="6c41f-118">Выберите **Продажи и маркетинг** \> **Общее** \> **Заказы на возврат** \> **Все заказы на возврат**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="6c41f-119">В разделе **Панель операций** в группе **Создать** щелкните **Заказ на возврат**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="6c41f-120">В форме **Создание заказа на возврат** выберите счет клиента и нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="6c41f-121">В форме **Заказ на возврат - номер RMA: %1, %2** выберите номенклатуру, а затем в поле **Количество** введите отрицательное количество.</span><span class="sxs-lookup"><span data-stu-id="6c41f-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="6c41f-122">Перейдите на экспресс-вкладку **Сведения о строке**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="6c41f-123">На вкладке **Общие** введите значение в поле **Себестоимость по возврату**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="6c41f-124">Это значение используется при возврате товаров на склад.</span><span class="sxs-lookup"><span data-stu-id="6c41f-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="6c41f-125">Если это значение не введено, при возврате товаров на склад используется текущая себестоимость.</span><span class="sxs-lookup"><span data-stu-id="6c41f-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="6c41f-126">Метод 2. Автоматическое создание себестоимости на основе строки накладной клиента</span><span class="sxs-lookup"><span data-stu-id="6c41f-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="6c41f-127">Этот метод является предпочтительным для создания строк возврата.</span><span class="sxs-lookup"><span data-stu-id="6c41f-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="6c41f-128">Чтобы использовать стоимость продуктов на момент их продажи клиенту, создайте заказ на возврат и укажите строки продажи для возврата.</span><span class="sxs-lookup"><span data-stu-id="6c41f-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="6c41f-129">Выберите **Продажи и маркетинг** \> **Общее** \> **Заказы на возврат** \> **Все заказы на возврат**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="6c41f-130">В разделе **Панель операций** в группе **Создать** щелкните **Заказ на возврат**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="6c41f-131">В форме **Создание заказа на возврат** выберите счет клиента и нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="6c41f-132">В форме **Заказ на возврат - номер RMA: %1, %2** в разделе **Панель операций** щелкните **Найти заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="6c41f-133">В форме **Найти заказ на продажу** выберите строку накладной для возврата, а затем нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="6c41f-134">На экспресс-вкладке **Сведения о строке** на вкладке **Общие** в поле **Номер возвращенного лота** отображается значение из строки исходной продажи.</span><span class="sxs-lookup"><span data-stu-id="6c41f-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="6c41f-135">Кроме того, в поле **Себестоимость по возврату** отображается значение себестоимости из строки исходной продажи.</span><span class="sxs-lookup"><span data-stu-id="6c41f-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="6c41f-136">Пример расчета стоимости</span><span class="sxs-lookup"><span data-stu-id="6c41f-136">Cost calculation example</span></span>

<span data-ttu-id="6c41f-137">Если для указания себестоимости возврата используется поле **Номер возвращенного лота** в строке заказа на возврат, используется стоимость в строке заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="6c41f-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="6c41f-138">При закрытии запасов или пересчете стоимость корректируется в строке исходной продажи.</span><span class="sxs-lookup"><span data-stu-id="6c41f-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="6c41f-139">Стоимость в строке заказа на возврат автоматически корректируется для отражения такой же стоимости за штуку.</span><span class="sxs-lookup"><span data-stu-id="6c41f-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="6c41f-140">Создайте и выпустите продукт с именем "Тест".</span><span class="sxs-lookup"><span data-stu-id="6c41f-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="6c41f-141">В форме **Сведения об используемом продукте** необходимо указать следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="6c41f-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="6c41f-142">На экспресс-вкладке **Управление затратами** в поле **Номенклатурная группа** выберите **Части**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="6c41f-143">На экспресс-вкладке **Общие** в поле **Группа номенклатурных моделей** выберите **DEF**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="6c41f-144">На экспресс-вкладке **Покупка** в поле **Цена** введите 10,00 в качестве себестоимости номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="6c41f-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="6c41f-145">В разделе **Панель операций** щелкните **Группы аналитики**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="6c41f-146">В поле **Группа аналитик хранения** выберите **Только сайт и склад**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="6c41f-147">В поле **Группа аналитик отслеживания** выберите **Без активных аналитик отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="6c41f-148">Создайте заказ на покупку для 10 штук тестовой номенклатуры по цене 6,00 за штуку, а затем разнесите накладную для заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="6c41f-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="6c41f-149">Создайте второй заказ на покупку для 10 единиц тестовой номенклатуры по цене 8,00 за единицу, а затем разнесите накладную для заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="6c41f-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="6c41f-150">Разнесите накладную для заказа на продажу, чтобы продать 5 единиц тестовой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="6c41f-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="6c41f-151">В этом случае в строке заказа на продажу указано 35,00 (5 штук \* 7,00 (средняя стоимость за единицу)).</span><span class="sxs-lookup"><span data-stu-id="6c41f-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="6c41f-152">Создайте заказ на возврат для поставщика.</span><span class="sxs-lookup"><span data-stu-id="6c41f-152">Create a return order for the customer.</span></span> <span data-ttu-id="6c41f-153">В форме **Найти заказ на продажу** выберите строку накладной, а затем нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="6c41f-154">В форме **Заказ на возврат - номер RMA: %1, %2** проверьте, что создан заказ на возврат для тестовой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="6c41f-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="6c41f-155">В заказе на возврат указано количество, равное 5.</span><span class="sxs-lookup"><span data-stu-id="6c41f-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="6c41f-156">В поле **Номер возвращенного лота** отобразится номер лота.</span><span class="sxs-lookup"><span data-stu-id="6c41f-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="6c41f-157">Номер лота берется из исходного заказа на продажу номенклатуры, проданной клиенту.</span><span class="sxs-lookup"><span data-stu-id="6c41f-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="6c41f-158">В поле **Себестоимость по возврату** отобразится себестоимость из строки исходной продажи.</span><span class="sxs-lookup"><span data-stu-id="6c41f-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="6c41f-159">Зарегистрируйте прихода возвращенных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="6c41f-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="6c41f-160">Разнесите лист комплектации для возвращенных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="6c41f-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="6c41f-161">Разнесите накладную для заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="6c41f-161">Post an invoice for the return order.</span></span> <span data-ttu-id="6c41f-162">На странице списка **Все заказы на продажу** выберите заказ на продажу, для которого задан тип заказа **Возвращенный заказ**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="6c41f-163">Откройте форму **Складские проводки**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="6c41f-164">Убедитесь, что цена возвращенного продукта составляет 7,00 за единицу, используя значение в поле **Себестоимость по возврату**, для общей суммы, составляющей 35,00, в поле **Сумма стоимости**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="6c41f-165">Можно открыть форму **Складские проводки** из формы **Заказ на возврат - номер RMA: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="6c41f-166">В сетке **Строки** щелкните **Запасы** \> **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="6c41f-167">В модуле "Управление запасами и складом" используйте форму **Закрытие и коррекция** для выполнения процедуры **3. Закрытие**.</span><span class="sxs-lookup"><span data-stu-id="6c41f-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="6c41f-168">Это действие корректирует стоимость в строке исходной продажи с -35,00 (5 единиц \* 7,00) до -30,00 (5 единиц \* 6,00).</span><span class="sxs-lookup"><span data-stu-id="6c41f-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="6c41f-169">Это связано с тем, что группа складских моделей метод ФИФО, и 6,00 за единицу является ценой ФИФО из первого заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="6c41f-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="6c41f-170">Кроме того, это действие корректирует стоимость в строке возврата для соответствия цене за единицу в исходной строке продажи.</span><span class="sxs-lookup"><span data-stu-id="6c41f-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="6c41f-171">Поэтому стоимость в строке возврата меняется с 35,00 на 30,00.</span><span class="sxs-lookup"><span data-stu-id="6c41f-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]