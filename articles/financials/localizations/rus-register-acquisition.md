---
title: Регистрация приобретений основных средств (Россия)
description: В этом разделе рассматривается регистрация приобретения основных средств для Microsoft Dynamics 365 for Finance and Operations в России.
author: ShylaThompson
manager: AnnBe
ms.date: 10/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 25630ed9567568006674cb6b8fc046176039e91d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556253"
---
# <a name="register-fixed-assets-acquisitions-russia"></a><span data-ttu-id="f4556-103">Регистрация приобретений основных средств (Россия)</span><span class="sxs-lookup"><span data-stu-id="f4556-103">Register fixed assets acquisitions (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4556-104">Можно зарегистрировать приобретение основных средств с помощью журнала накладных поставщика или заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f4556-104">You can register a fixed asset acquisitios using a vendor invoice journal or a purchase order.</span></span> <span data-ttu-id="f4556-105">Обычно журнал накладных поставщика используется, если нет необходимости отслеживать движение запасов ОС.</span><span class="sxs-lookup"><span data-stu-id="f4556-105">Typically, a vendor invoice journal is used if there is no need to track inventory movement of the fixed asset.</span></span> <span data-ttu-id="f4556-106">Например, основное средство покупается и вводится в эксплуатацию в течение одного периода.</span><span class="sxs-lookup"><span data-stu-id="f4556-106">For example, a fixed asset is bought and put into operation during the same period.</span></span> <span data-ttu-id="f4556-107">Заказ на покупку может использоваться, если приобретено несколько идентичных основных средств или необходимо отслеживать движение запасов ОС.</span><span class="sxs-lookup"><span data-stu-id="f4556-107">A purchase order might be used if several identical fixed assets are bought or it is necessary to track inventory movement of a fixed asset.</span></span> 

## <a name="register-a-fixed-asset-acquisition-using-an-invoice-journal"></a><span data-ttu-id="f4556-108">Регистрация приобретения основных средств с использованием журнала накладных</span><span class="sxs-lookup"><span data-stu-id="f4556-108">Register a fixed asset acquisition using an invoice journal</span></span> 

<span data-ttu-id="f4556-109">Перед регистрацией приобретения основных средств актив должен быть зарегистрирован на странице <STRONG>Основные средства</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f4556-109">Before you can register the purchase of a fixed asset, the asset must be registered on the <STRONG>Fixed assets</STRONG> page.</span></span>

1.  <span data-ttu-id="f4556-110">Перейдите в раздел **Основные средства (Россия)** \> **Общие** \> **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="f4556-110">Go to **Fixed assets (Russia)** \> **Common** \> **Fixed assets**.</span></span> <span data-ttu-id="f4556-111">В области действий щелкните **Основное средство**, чтобы создать основное средство, или выберите запись основного средства.</span><span class="sxs-lookup"><span data-stu-id="f4556-111">On the Action pane, click **Fixed asset** to create a fixed asset, or select a fixed asset record.</span></span>

2.  <span data-ttu-id="f4556-112">Щелкните **Создать** для создания основного средства со статусом **Запланировано**.</span><span class="sxs-lookup"><span data-stu-id="f4556-112">Click **New** to create a fixed asset with a **Scheduled** status.</span></span>
    
3.  <span data-ttu-id="f4556-113">Щелкните **Расчеты с поставщиками** \> **Накладные** \> **Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="f4556-113">Click **Accounts payable** \> **Invoices** \> **Invoice journal**.</span></span>

4.  <span data-ttu-id="f4556-114">Создайте новый журнал и в поле **Имя** выберите имя журнала.</span><span class="sxs-lookup"><span data-stu-id="f4556-114">Create a new journal and in the **Name** field, select the journal name.</span></span>

5.  <span data-ttu-id="f4556-115">Щелкните **Строки**, чтобы открыть страницу **Ваучер журнала**.</span><span class="sxs-lookup"><span data-stu-id="f4556-115">Click **Lines** to open the **Journal voucher** page.</span></span>

6.  <span data-ttu-id="f4556-116">Создайте новую строку.</span><span class="sxs-lookup"><span data-stu-id="f4556-116">Create a new line.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="f4556-117">Дата разноски и номер ваучера отображаются в полях <STRONG>Дата</STRONG> и <STRONG>Ваучер</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f4556-117">The posting date and voucher number are displayed in the <STRONG>Date</STRONG> and <STRONG>Voucher</STRONG> fields.</span></span></P>

7.  <span data-ttu-id="f4556-118">В поле **Тип счета** выберите тип счета **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="f4556-118">In the **Account type** field, select the **Vendor** account type.</span></span> 
  
8.  <span data-ttu-id="f4556-119">В поле **Счет** выберите код поставщика.</span><span class="sxs-lookup"><span data-stu-id="f4556-119">In the **Account** field, select a vendor code.</span></span>

9. <span data-ttu-id="f4556-120">В поле **Накладная** введите номер накладной для покупки основного средства.</span><span class="sxs-lookup"><span data-stu-id="f4556-120">In the **Invoice** field, enter the invoice number for the fixed asset purchase.</span></span>

10. <span data-ttu-id="f4556-121">В поле **Описание** введите любые замечания о накладной.</span><span class="sxs-lookup"><span data-stu-id="f4556-121">In the **Description** field, enter any notes about the invoice.</span></span>

11. <span data-ttu-id="f4556-122">В поле **Кредит** введите сумму накладной.</span><span class="sxs-lookup"><span data-stu-id="f4556-122">In the **Credit** field, enter the invoice amount.</span></span>

12. <span data-ttu-id="f4556-123">В поле **Тип корр. счета** выберите тип счета для текущего счета.</span><span class="sxs-lookup"><span data-stu-id="f4556-123">In the **Offset account type** field, select the account type for the current account.</span></span>

13. <span data-ttu-id="f4556-124">В поле **Корр. счет** выберите счет ГК для основного средства до его приобретения.</span><span class="sxs-lookup"><span data-stu-id="f4556-124">In the **Offset account** field, select the ledger account for the fixed asset before acquisition.</span></span>

14. <span data-ttu-id="f4556-125">На вкладке **Общее** в поле **Валюта** выберите текущую валюту накладной.</span><span class="sxs-lookup"><span data-stu-id="f4556-125">On the **General** tab in the **Currency** field, select the current invoice currency.</span></span>

15. <span data-ttu-id="f4556-126">На вкладке **Основное средство** в поле **Инвентарный номер ОС** выберите номер основного средства.</span><span class="sxs-lookup"><span data-stu-id="f4556-126">On the **Fixed asset** tab in the **FA inventory number** field, select the fixed asset number.</span></span>

16. <span data-ttu-id="f4556-127">Щелкните **Разнести** \> **Разнести** для создания проводок поставщика и главной книги.</span><span class="sxs-lookup"><span data-stu-id="f4556-127">Click **Post** \> **Post** to generate the vendor and ledger transactions.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f4556-128">После разноски накладной статус основного средства устанавливается равным **Куплено** на странице **Основные средства** (**Основные средства (Россия)** \> **Общие** \> **Основные средства**).</span><span class="sxs-lookup"><span data-stu-id="f4556-128">After posting the invoice, the status of the fixed asset is set to **Bought** on the **Fixed assets** page (**Fixed assets (Russia)** \> **Common** \> **Fixed assets**).</span></span> <span data-ttu-id="f4556-129">Если номер основного средства указан в строке журнала накладной и журнал накладных не разнесен, нельзя использовать это основное средство в другом журнале накладных.</span><span class="sxs-lookup"><span data-stu-id="f4556-129">If the fixed asset number is specified in the invoice journal line and the invoice journal is not posted, you cannot use this fixed asset in another invoice journal.</span></span>
    
## <a name="register-a-fixed-asset-acquisition-using-a-purchase-order"></a><span data-ttu-id="f4556-130">Регистрация приобретения основных средств с использованием заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="f4556-130">Register a fixed asset acquisition using a purchase order</span></span> 

<span data-ttu-id="f4556-131">Приобретение основного средства можно зарегистрировать путем создания заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f4556-131">You can register the purchase of a fixed asset by creating a purchase order.</span></span> <span data-ttu-id="f4556-132">Перед созданием заказа на покупку следует создать выпущенный продукт с типом продукта **Услуга** или **Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="f4556-132">Before creating a purchase order, you should create a released product with a **Service** or **Item** product type.</span></span> <span data-ttu-id="f4556-133">При выборе номенклатуры с типом продукта **Услуга** в строке заказа на покупку можно ввести несколько основных средств, связанных со строкой заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f4556-133">When you select an item with the **Service** product type in the purchase order line, you can enter several fixed assets, related with one purchase order line.</span></span> <span data-ttu-id="f4556-134">При выборе номенклатуры с типом продукта **Номенклатура** в строке заказа на покупку можно ввести только одно основное средство.</span><span class="sxs-lookup"><span data-stu-id="f4556-134">When you select an item with the **Item** product type in the purchase order line, you can only enter one fixed asset.</span></span> <span data-ttu-id="f4556-135">Это основное средство должно быть связано со строкой заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f4556-135">This fixed asset needs to be related to the purchase order line.</span></span>  


1.  <span data-ttu-id="f4556-136">Выберите **Управление сведениями о продукте** \> **Общее** \> **Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="f4556-136">Go to **Product information management** \> **Common** \> **Released products**.</span></span>

2.  <span data-ttu-id="f4556-137">Создайте новую номенклатуру и в поле **Тип номенклатуры** выберите **Услуга** или **Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="f4556-137">Create a new item and in the **Item type** field, select **Service** or **Item**.</span></span> <span data-ttu-id="f4556-138">На вкладке **Общие** заполните поле **Группа ОС**.</span><span class="sxs-lookup"><span data-stu-id="f4556-138">On the **General** tab, fill in the **FA group** field.</span></span> <span data-ttu-id="f4556-139">Дополнительные сведения см. в разделе **[Создание выпущенного продукта](../../supply-chain/pim/tasks/create-released-product-single-company.md)**.</span><span class="sxs-lookup"><span data-stu-id="f4556-139">For more information, see **[Create released product](../../supply-chain/pim/tasks/create-released-product-single-company.md)**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4556-140">Сведения, приведенные в строке покупки, определяют, принадлежит ли основное средство к указанной группе основных средств.</span><span class="sxs-lookup"><span data-stu-id="f4556-140">The information provided on the purchase line determines whether the fixed asset belongs to the specified fixed asset group.</span></span>
    
3.  <span data-ttu-id="f4556-141">Щелкните **Расчеты с поставщиками** \> **Общее** \> **Заказы на покупку** \> **Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="f4556-141">Click **Accounts payable** \> **Common** \> **Purchase orders** \> **All purchase orders**.</span></span>
4.  <span data-ttu-id="f4556-142">Щелкните **Создать**, чтобы создать новый заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="f4556-142">Click **New** to create a new purchase order.</span></span> <span data-ttu-id="f4556-143">Дополнительные сведения см. в разделе [Создание заказа на покупку](../../supply-chain/procurement/tasks/create-purchase-order.md).</span><span class="sxs-lookup"><span data-stu-id="f4556-143">For more information, see [Create a purchase order](../../supply-chain/procurement/tasks/create-purchase-order.md).</span></span>
5.  <span data-ttu-id="f4556-144">Щелкните вкладку **Строки** в нижней области.</span><span class="sxs-lookup"><span data-stu-id="f4556-144">Click the **Lines** tab in the lower pane.</span></span>
6.  <span data-ttu-id="f4556-145">В поле **Код номенклатуры** выберите номер номенклатуры, который связан с группой основных средств.</span><span class="sxs-lookup"><span data-stu-id="f4556-145">In the **Item number** field, select the item number, which is related to the fixed asset group.</span></span> <span data-ttu-id="f4556-146">На вкладке **Сведения по строке/Основное средство** введите основное средство (**Основные средства (Россия)**).</span><span class="sxs-lookup"><span data-stu-id="f4556-146">On the **Line detail/ Fixed asset** tab, enter the fixed assets (**Fixed asset (Russia)**).</span></span> <span data-ttu-id="f4556-147">Если выбрана номенклатура с типом продукта **Услуга** в строке заказа на покупку можно ввести несколько основных средств.</span><span class="sxs-lookup"><span data-stu-id="f4556-147">If you select an item with the **Service** product type in the purchase line you can enter several fixed assets.</span></span> <span data-ttu-id="f4556-148">В этом случае количество основных средств должно быть равно количеству, которое указано в строке покупки.</span><span class="sxs-lookup"><span data-stu-id="f4556-148">In this case, the quantity of fixed assets should be equal to the quantity that is specified on the purchase line.</span></span> <span data-ttu-id="f4556-149">Можно также ввести основное средство в строке покупки, если выбрана номенклатура с типом продукта **Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="f4556-149">You can also enter a fixed asset on the purchase line, if you select the item with the **Item** product type.</span></span>

7. <span data-ttu-id="f4556-150">Создайте накладную.</span><span class="sxs-lookup"><span data-stu-id="f4556-150">Create the invoice.</span></span> <span data-ttu-id="f4556-151">После разноски накладной основного средства статус изменяется на **Куплено**.</span><span class="sxs-lookup"><span data-stu-id="f4556-151">After posting invoice the fixed asset, the status will change to **Bought**.</span></span>

## <a name="reverse-a-fixed-asset-acquisition-transaction"></a><span data-ttu-id="f4556-152">Сторнирование проводки приобретения ОС</span><span class="sxs-lookup"><span data-stu-id="f4556-152">Reverse a fixed asset acquisition transaction</span></span>    
    
<span data-ttu-id="f4556-153">При создании реверсирующей проводки сохраняются сведения и сумма исходной проводки.</span><span class="sxs-lookup"><span data-stu-id="f4556-153">When you create a reverse transaction, the information and amount of the original transaction are saved.</span></span> <span data-ttu-id="f4556-154">По умолчанию дата реверсирования и дата исходной проводки совпадают.</span><span class="sxs-lookup"><span data-stu-id="f4556-154">By default, the reversal date and the original transaction date are the same.</span></span> <span data-ttu-id="f4556-155">Тем не менее при реверсировании проводок можно указать дату реверсирования, которая будет отличаться от даты исходной проводки.</span><span class="sxs-lookup"><span data-stu-id="f4556-155">However, when reversing transactions, you can specify a reversal date that is different from the original transaction date.</span></span> <span data-ttu-id="f4556-156">Используя данную процедуру, можно также реверсировать проводку амортизации.</span><span class="sxs-lookup"><span data-stu-id="f4556-156">You can also reverse an amortization transaction using this process.</span></span> 

1.  <span data-ttu-id="f4556-157">Перейдите в раздел **Основные средства** \> **Общие** \> **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="f4556-157">Go to **Fixed assets** \> **Common** \> **Fixed assets**.</span></span> <span data-ttu-id="f4556-158">Щелкните **Модели стоимости**\> **Проводки**, чтобы открыть страницу **Проводки по ОС**.</span><span class="sxs-lookup"><span data-stu-id="f4556-158">Click **Value Models**\> **Transactions** to open the **FA Transactions** page.</span></span>

2.  <span data-ttu-id="f4556-159">Выберите проводку приобретения основного средства и нажмите кнопку **Реверсирующая проводка**, чтобы открыть страницу **Реверсирующая проводка**.</span><span class="sxs-lookup"><span data-stu-id="f4556-159">Select the fixed asset acquisition transaction, and then click **Reverse transaction** to open the **Reverse transaction** page.</span></span>

3.  <span data-ttu-id="f4556-160">В поле **Дата реверсирования** выберите дату реверсирования проводки.</span><span class="sxs-lookup"><span data-stu-id="f4556-160">In the **Reverse date**, select the transaction reverse date.</span></span>

4.  <span data-ttu-id="f4556-161">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f4556-161">Click **OK**.</span></span> <span data-ttu-id="f4556-162">На странице **Проводки по ОС** создается проводка, которая реверсирует исходную проводку.</span><span class="sxs-lookup"><span data-stu-id="f4556-162">A transaction is created on the **FA transactions** page that reverses the original transaction.</span></span>

5.  <span data-ttu-id="f4556-163">Щелкните **Ваучер**, чтобы просмотреть проводку в книге учета на странице **Проводки ваучера**.</span><span class="sxs-lookup"><span data-stu-id="f4556-163">Click **Voucher** to view the transaction in the ledger on the **Voucher transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4556-164">Чтобы изменить статус на **Запланировано**, выполните реверсирующую проводку приобретения для всех моделей стоимости.</span><span class="sxs-lookup"><span data-stu-id="f4556-164">To change the status to **Scheduled**, run the reverse acquisition transaction for all value models.</span></span> <span data-ttu-id="f4556-165">Если актив, который был реверсирован, состоял из складских компонентов, создаются проводки для записи возврата компонентов в запасы.</span><span class="sxs-lookup"><span data-stu-id="f4556-165">If the asset that was reversed was built from inventory components, transactions are created to record the return of the components to the inventory.</span></span> <span data-ttu-id="f4556-166">При реверсировании проводки приобретения себестоимость возвращаемых компонентов может отличаться от текущей складской себестоимости.</span><span class="sxs-lookup"><span data-stu-id="f4556-166">When you reverse an acquisition transaction, the cost price of the returned components may differ from the current warehouse cost price.</span></span> <span data-ttu-id="f4556-167">Однако после закрытия запасов компоненты будут отражать текущее ценообразование.</span><span class="sxs-lookup"><span data-stu-id="f4556-167">However, after inventory closure, the components will reflect the current pricing.</span></span>
