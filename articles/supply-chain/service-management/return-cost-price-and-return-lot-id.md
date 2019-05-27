---
title: Себестоимость по возврату и номер возвращенного лота
description: Может потребоваться, чтобы стоимость возвращенных продуктов совпадала со стоимостью продуктов на момент их продажи клиенту. Это можно сделать с помощью параметра **Номер возвращенного лота**.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33cd3d50fe342ba12a17419f4e759c243a60b3e0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565542"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="8e9d0-104">Себестоимость по возврату и номер возвращенного лота</span><span class="sxs-lookup"><span data-stu-id="8e9d0-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="8e9d0-105">Стоимость продуктов, возвращенных на склад, рассчитывается с учетом текущей стоимости продуктов.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="8e9d0-106">Однако может потребоваться, чтобы стоимость возвращенных продуктов совпадала со стоимостью продуктов на момент их продажи клиенту.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="8e9d0-107">Это можно сделать с помощью поля **Номер возвращенного лота** на экспресс-вкладке **Сведения по строке** в форме **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="8e9d0-108">Рассмотрим следующий сценарий.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-108">For example, consider the following scenario.</span></span> <span data-ttu-id="8e9d0-109">Клиент получает накладную.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-109">You invoice a customer.</span></span> <span data-ttu-id="8e9d0-110">Затем он возвращает вам поставленные продукты.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="8e9d0-111">Вы возвращаете продукты на склад.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-111">You return the products to stock.</span></span> <span data-ttu-id="8e9d0-112">В этом случае при кредитовании клиента за возвращенные продукты стоимость этих продуктов рассчитывается с учетом текущей стоимости продуктов.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="8e9d0-113">Однако, если используется поле **Номер возвращенного лота**, стоимость возвращенных продуктов рассчитывается с учетом стоимости, указанной в накладной при исходной продаже клиенту.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="8e9d0-114">Чтобы использовать стоимость, отличную от текущей стоимости, для возвратов от клиентов, воспользуйтесь одним из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="8e9d0-115">Метод 1. Ввод себестоимости возврата вручную</span><span class="sxs-lookup"><span data-stu-id="8e9d0-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="8e9d0-116">По умолчанию при добавлении номенклатур в заказ на возврат номенклатуры возвращаются на склад по текущей себестоимости.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="8e9d0-117">Чтобы указать другую себестоимость возврата, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="8e9d0-118">Выберите **Продажи и маркетинг** \> **Общее** \> **Заказы на возврат** \> **Все заказы на возврат**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="8e9d0-119">В разделе **Панель операций** в группе **Создать** щелкните **Заказ на возврат**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="8e9d0-120">В форме **Создание заказа на возврат** выберите счет клиента и нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="8e9d0-121">В форме **Заказ на возврат - номер RMA: %1, %2** выберите номенклатуру, а затем в поле **Количество** введите отрицательное количество.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="8e9d0-122">Перейдите на экспресс-вкладку **Сведения о строке**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="8e9d0-123">На вкладке **Общие** введите значение в поле **Себестоимость по возврату**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="8e9d0-124">Это значение используется при возврате товаров на склад.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="8e9d0-125">Если это значение не введено, при возврате товаров на склад используется текущая себестоимость.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="8e9d0-126">Метод 2. Автоматическое создание себестоимости на основе строки накладной клиента</span><span class="sxs-lookup"><span data-stu-id="8e9d0-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="8e9d0-127">Этот метод является предпочтительным для создания строк возврата.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="8e9d0-128">Чтобы использовать стоимость продуктов на момент их продажи клиенту, создайте заказ на возврат и укажите строки продажи для возврата.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="8e9d0-129">Выберите **Продажи и маркетинг** \> **Общее** \> **Заказы на возврат** \> **Все заказы на возврат**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="8e9d0-130">В разделе **Панель операций** в группе **Создать** щелкните **Заказ на возврат**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="8e9d0-131">В форме **Создание заказа на возврат** выберите счет клиента и нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="8e9d0-132">В форме **Заказ на возврат - номер RMA: %1, %2** в разделе **Панель операций** щелкните **Найти заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="8e9d0-133">В форме **Найти заказ на продажу** выберите строку накладной для возврата, а затем нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="8e9d0-134">На экспресс-вкладке **Сведения о строке** на вкладке **Общие** в поле **Номер возвращенного лота** отображается значение из строки исходной продажи.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="8e9d0-135">Кроме того, в поле **Себестоимость по возврату** отображается значение себестоимости из строки исходной продажи.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="8e9d0-136">Пример расчета стоимости</span><span class="sxs-lookup"><span data-stu-id="8e9d0-136">Cost calculation example</span></span>

<span data-ttu-id="8e9d0-137">Если для указания себестоимости возврата используется поле **Номер возвращенного лота** в строке заказа на возврат, используется стоимость в строке заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="8e9d0-138">При закрытии запасов или пересчете стоимость корректируется в строке исходной продажи.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="8e9d0-139">Стоимость в строке заказа на возврат автоматически корректируется для отражения такой же стоимости за штуку.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="8e9d0-140">Создайте и выпустите продукт с именем "Тест".</span><span class="sxs-lookup"><span data-stu-id="8e9d0-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="8e9d0-141">В форме **Сведения об используемом продукте** необходимо указать следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="8e9d0-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="8e9d0-142">На экспресс-вкладке **Управление затратами** в поле **Номенклатурная группа** выберите **Части**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="8e9d0-143">На экспресс-вкладке **Общие** в поле **Группа номенклатурных моделей** выберите **DEF**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="8e9d0-144">На экспресс-вкладке **Покупка** в поле **Цена** введите 10,00 в качестве себестоимости номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="8e9d0-145">В разделе **Панель операций** щелкните **Группы аналитики**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="8e9d0-146">В поле **Группа аналитик хранения** выберите **Только сайт и склад**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="8e9d0-147">В поле **Группа аналитик отслеживания** выберите **Без активных аналитик отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="8e9d0-148">Создайте заказ на покупку для 10 штук тестовой номенклатуры по цене 6,00 за штуку, а затем разнесите накладную для заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="8e9d0-149">Создайте второй заказ на покупку для 10 единиц тестовой номенклатуры по цене 8,00 за единицу, а затем разнесите накладную для заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="8e9d0-150">Разнесите накладную для заказа на продажу, чтобы продать 5 единиц тестовой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="8e9d0-151">В этом случае в строке заказа на продажу указано 35,00 (5 штук \* 7,00 (средняя стоимость за единицу)).</span><span class="sxs-lookup"><span data-stu-id="8e9d0-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="8e9d0-152">Создайте заказ на возврат для поставщика.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-152">Create a return order for the customer.</span></span> <span data-ttu-id="8e9d0-153">В форме **Найти заказ на продажу** выберите строку накладной, а затем нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="8e9d0-154">В форме **Заказ на возврат - номер RMA: %1, %2** проверьте, что создан заказ на возврат для тестовой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="8e9d0-155">В заказе на возврат указано количество, равное 5.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="8e9d0-156">В поле **Номер возвращенного лота** отобразится номер лота.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="8e9d0-157">Номер лота берется из исходного заказа на продажу номенклатуры, проданной клиенту.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="8e9d0-158">В поле **Себестоимость по возврату** отобразится себестоимость из строки исходной продажи.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="8e9d0-159">Зарегистрируйте прихода возвращенных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="8e9d0-160">Разнесите лист комплектации для возвращенных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="8e9d0-161">Разнесите накладную для заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-161">Post an invoice for the return order.</span></span> <span data-ttu-id="8e9d0-162">На странице списка **Все заказы на продажу** выберите заказ на продажу, для которого задан тип заказа **Возвращенный заказ**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="8e9d0-163">Откройте форму **Складские проводки**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="8e9d0-164">Убедитесь, что цена возвращенного продукта составляет 7,00 за единицу, используя значение в поле **Себестоимость по возврату**, для общей суммы, составляющей 35,00, в поле **Сумма стоимости**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="8e9d0-165">Можно открыть форму **Складские проводки** из формы **Заказ на возврат - номер RMA: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="8e9d0-166">В сетке **Строки** щелкните **Запасы** \> **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="8e9d0-167">В модуле "Управление запасами и складом" используйте форму **Закрытие и коррекция** для выполнения процедуры **3. Закрытие**.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="8e9d0-168">Это действие корректирует стоимость в строке исходной продажи с -35,00 (5 единиц \* 7,00) до -30,00 (5 единиц \* 6,00).</span><span class="sxs-lookup"><span data-stu-id="8e9d0-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="8e9d0-169">Это связано с тем, что группа складских моделей метод ФИФО, и 6,00 за единицу является ценой ФИФО из первого заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="8e9d0-170">Кроме того, это действие корректирует стоимость в строке возврата для соответствия цене за единицу в исходной строке продажи.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="8e9d0-171">Поэтому стоимость в строке возврата меняется с 35,00 на 30,00.</span><span class="sxs-lookup"><span data-stu-id="8e9d0-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




