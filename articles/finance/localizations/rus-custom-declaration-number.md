---
title: Номера таможенных деклараций
description: Этот раздел дает информацию, как настроить и отслеживать номера таможенных деклараций.
author: v-nadyuz
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: roschlom
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7ff5bcf06a6df61b2262a8ebb89316394f3d33bd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408584"
---
# <a name="customs-declaration-numbers"></a><span data-ttu-id="a2d80-103">Номера таможенных деклараций</span><span class="sxs-lookup"><span data-stu-id="a2d80-103">Customs declaration numbers</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2d80-104">Вы можете отслеживать таможенные декларации с момента прибытия товаров на таможенный терминал до момента отгрузки товаров конечному потребителю.</span><span class="sxs-lookup"><span data-stu-id="a2d80-104">You can track customs declarations (CDs) from the time when goods arrive at the customs terminal through the time when they are shipped to the end customer.</span></span>

<span data-ttu-id="a2d80-105">Номер таможенной декларации является одной из складских аналитик, введенных вручную при получении товаров.</span><span class="sxs-lookup"><span data-stu-id="a2d80-105">The customs declaration number is one of the inventory dimensions that is manually entered when goods are received.</span></span> <span data-ttu-id="a2d80-106">Например, можно ввести его при регистрации накладной с фактурой от поставщика, а затем предоставить соответствующие документы расхода полей, такие как фактура для заказа на продажу, клиенту.</span><span class="sxs-lookup"><span data-stu-id="a2d80-106">For example, you enter it when you register the invoice with the facture from the vendor and then provide the appropriate field expenditure documents, such as the facture for a sales order, to the customer.</span></span> <span data-ttu-id="a2d80-107">Таким образом клиент может проследить номер таможенной декларации.</span><span class="sxs-lookup"><span data-stu-id="a2d80-107">In this way, the customer can trace the customs declaration number.</span></span> <span data-ttu-id="a2d80-108">Указанный номер таможенной декларации также отображается в книге покупок.</span><span class="sxs-lookup"><span data-stu-id="a2d80-108">The specified customs declaration number is also shown in the purchase book.</span></span>

<span data-ttu-id="a2d80-109">Чтобы выполнить учет таможенной декларации, необходимо активировать соответствующую аналитику отслеживания в группе аналитик отслеживания номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a2d80-109">To do customs declaration accounting, you must activate the corresponding tracking dimension in the item's tracking dimension group.</span></span>

<span data-ttu-id="a2d80-110">Приемка и продажа товаров могут выполняться различными способами.</span><span class="sxs-lookup"><span data-stu-id="a2d80-110">The receipt and sale of goods can be done in various ways.</span></span> <span data-ttu-id="a2d80-111">Например, товары могут быть получены через заказы на покупку от поставщика и могут продаваться клиенту.</span><span class="sxs-lookup"><span data-stu-id="a2d80-111">For example, goods can be received through purchase orders from the vendor, and they can be sold to the customer.</span></span>

<span data-ttu-id="a2d80-112">Когда товары получают, номера их таможенных деклараций вводят вручную.</span><span class="sxs-lookup"><span data-stu-id="a2d80-112">When goods are received, their customs declaration numbers are manually entered.</span></span> <span data-ttu-id="a2d80-113">Когда товары продают, номера таможенных деклараций определяется автоматически в зависимости от лота номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a2d80-113">When goods are sold, their customs declaration numbers are automatically determined, based on the item lot.</span></span> <span data-ttu-id="a2d80-114">Номер таможенной декларации, который использовался при покупке товаров, отображается на документах, созданных при продаже товаров.</span><span class="sxs-lookup"><span data-stu-id="a2d80-114">The customs declaration number that was used when the goods were purchased is shown on the documents that are created when the goods are sold.</span></span>

## <a name="set-up-customs-declaration-numbers-in-tracking-dimensions"></a><span data-ttu-id="a2d80-115">Настройка номеров таможенных деклараций в аналитиках отслеживания</span><span class="sxs-lookup"><span data-stu-id="a2d80-115">Set up customs declaration numbers in tracking dimensions</span></span>

1. <span data-ttu-id="a2d80-116">Откройте **Управление сведениями о продукте** \> **Настройка** \> **Группы аналитик и вариантов** \> **Группы аналитик отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="a2d80-116">Go to **Product information management** \> **Setup** \> **Dimension and variant groups** \> **Tracking dimension groups**.</span></span>
2. <span data-ttu-id="a2d80-117">Выберите **Создать**, чтобы создать группу аналитик.</span><span class="sxs-lookup"><span data-stu-id="a2d80-117">Select **New** to create a dimension group.</span></span>
3. <span data-ttu-id="a2d80-118">В поле **Имя** введите полное имя группы аналитик.</span><span class="sxs-lookup"><span data-stu-id="a2d80-118">In the **Name** field, enter the name of the dimension group.</span></span>
4. <span data-ttu-id="a2d80-119">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="a2d80-119">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a2d80-120">На экспресс-вкладке **Аналитики отслеживания** в строке **Номер ГТД** установите флажок **Активно**.</span><span class="sxs-lookup"><span data-stu-id="a2d80-120">On the **Tracking dimensions** FastTab, in the row for **GTD number**, select the **Active** check box.</span></span>
6. <span data-ttu-id="a2d80-121">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a2d80-121">Select **Save**.</span></span>

    ![Автоматически создается снимок экрана описания мобильного телефона](media/1%20Tracking%20dimension%20groups.jpg)

## <a name="create-a-customs-declaration-number"></a><span data-ttu-id="a2d80-123">Создание номера таможенной декларации</span><span class="sxs-lookup"><span data-stu-id="a2d80-123">Create a customs declaration number</span></span>

<span data-ttu-id="a2d80-124">Перед регистрацией номеров таможенных деклараций для вновь полученных товаров их необходимо ввести в соответствующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="a2d80-124">Before you can register customs declaration numbers for newly received goods, you must enter them in a corresponding database.</span></span> <span data-ttu-id="a2d80-125">Необходимо также ввести наименования номенклатур и страну или регион происхождения.</span><span class="sxs-lookup"><span data-stu-id="a2d80-125">You must also enter item names, and the country or region of origin.</span></span>

1. <span data-ttu-id="a2d80-126">Перейдите в раздел **Управление запасами** \> **Запросы и отчеты** \> **Аналитики отслеживания** \> **Номера ГТД**.</span><span class="sxs-lookup"><span data-stu-id="a2d80-126">Go to **Inventory management** \> **Inquiries and reports** \> **Tracking dimensions** \> **Custom decl. numbers**.</span></span>
2. <span data-ttu-id="a2d80-127">Выберите **Создать** для создания нового номера таможенной декларации.</span><span class="sxs-lookup"><span data-stu-id="a2d80-127">Select **New** to create a customs declaration number.</span></span>
3. <span data-ttu-id="a2d80-128">В поле **Номер ГТД** введите номер таможенной декларации.</span><span class="sxs-lookup"><span data-stu-id="a2d80-128">In the **GTD number** field, enter the customs declaration number.</span></span>
4. <span data-ttu-id="a2d80-129">В поле **Код номенклатуры** выберите код номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a2d80-129">In the **Item number** field, select the item number.</span></span>

> [!NOTE]
> <span data-ttu-id="a2d80-130">Номенклатура должна иметь ранее созданную группу аналитик отслеживания, в которой активирована аналитика отслеживания **Номер ГТД**.</span><span class="sxs-lookup"><span data-stu-id="a2d80-130">The item should have the tracking dimension group that you created earlier, where the **GTD number** tracking dimension is activated.</span></span>

5. <span data-ttu-id="a2d80-131">В поле **Страна/регион** выберите страну или регион.</span><span class="sxs-lookup"><span data-stu-id="a2d80-131">In the **Country/region** field, select the country or region.</span></span>
6. <span data-ttu-id="a2d80-132">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a2d80-132">Select **Save**.</span></span>

    ![Страница номеров таможенных деклараций](media/2%20State%20custom%20declaration%20numbers.jpg)

## <a name="specify-the-customs-declaration-number-in-a-purchase-order"></a><span data-ttu-id="a2d80-134">Указание номера таможенной декларации в заказе на покупку</span><span class="sxs-lookup"><span data-stu-id="a2d80-134">Specify the customs declaration number in a purchase order</span></span>

1.  <span data-ttu-id="a2d80-135">Создайте заказ на покупку и в строке заказа на покупку выберите код номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a2d80-135">Create a purchase order, and on the purchase order line, select the item number.</span></span>

> [!NOTE]
> <span data-ttu-id="a2d80-136">Номенклатура должна иметь ранее созданную группу аналитик отслеживания, в которой активирована аналитика отслеживания **Номер ГТД**.</span><span class="sxs-lookup"><span data-stu-id="a2d80-136">The item should have the tracking dimension group that you created earlier, where the **GTD number** tracking dimension is activated.</span></span>

2. <span data-ttu-id="a2d80-137">На экспресс-вкладке **Сведения по строке** на вкладке **Продукт** в разделе **Аналитики отслеживания** в поле **Номер ГТД** выберите ранее созданный номер таможенной декларации.</span><span class="sxs-lookup"><span data-stu-id="a2d80-137">On the **Line details** FastTab, on the **Product** tab, in the **Tracking dimensions** section, in the **GTD number** field, select the customs declaration number that you created earlier.</span></span>

    ![Экспресс-вкладка сведений по строке на странице заказов на покупку](media/3%20All%20purchase%20orders.jpg)

3. <span data-ttu-id="a2d80-139">Задайте другие параметры заказа на покупку и создайте счет-фактуру обычным способом.</span><span class="sxs-lookup"><span data-stu-id="a2d80-139">Set other purchase order parameters, and create a facture in the usual way.</span></span> <span data-ttu-id="a2d80-140">Столбец 11 в фактуре содержит информацию о номере таможенной декларации.</span><span class="sxs-lookup"><span data-stu-id="a2d80-140">Column 11 of the facture shows the information about the customs declaration number.</span></span>

    ![Фактура накладной](media/4%20Invoice-facture.jpg)

## <a name="view-the-customs-declaration-number-in-the-purchase-book"></a><span data-ttu-id="a2d80-142">Просмотр номера таможенной декларации в книге покупок</span><span class="sxs-lookup"><span data-stu-id="a2d80-142">View the customs declaration number in the purchase book</span></span>

1. <span data-ttu-id="a2d80-143">После завершения процедуры **Обработка входящего НДС** на странице **Журнал книг покупок** в области действий выберите **Обновить**, чтобы обновить книгу покупок.</span><span class="sxs-lookup"><span data-stu-id="a2d80-143">After the **Incoming VAT processing** procedure is completed, on the **Purchase books journal** page, on the Action Pane, select **Update** to update the purchase book.</span></span>
2. <span data-ttu-id="a2d80-144">В области действий выберите **Строки** и выберите накладную, которая была только что создана.</span><span class="sxs-lookup"><span data-stu-id="a2d80-144">On the Action Pane, select **Lines**, and select the invoice that you just created.</span></span> <span data-ttu-id="a2d80-145">На вкладке **Общие** в поле **Номера ГТД** отображаются сведения о счете-фактуре и номере таможенной декларации.</span><span class="sxs-lookup"><span data-stu-id="a2d80-145">On the **General** tab, the **Custom decl. numbers** field shows the information about the facture and the customs declaration number.</span></span>

    ![Вкладка "Общие" для строк книги покупок](media/5%20Purchase%20book%20lines.jpg)

## <a name="ship-goods-that-have-customs-declaration-numbers"></a><span data-ttu-id="a2d80-147">Отгрузка товаров с номерами таможенных деклараций</span><span class="sxs-lookup"><span data-stu-id="a2d80-147">Ship goods that have customs declaration numbers</span></span>

1. <span data-ttu-id="a2d80-148">Создайте заказ на продажу и в строке заказа на продажу выберите тот же номер номенклатуры, который использовался в предыдущих процедурах данного раздела.</span><span class="sxs-lookup"><span data-stu-id="a2d80-148">Create a sales order, and on the sales order line, select the same item number that you used in the previous procedures in this topic.</span></span>
2. <span data-ttu-id="a2d80-149">На экспресс-вкладке **Сведения по строке** на вкладке **Настройка** в поле **Резервирование** выберите **Автоматически**, чтобы при создании строки заказа на продажу номенклатура автоматически была зарезервирована из существующих приходов.</span><span class="sxs-lookup"><span data-stu-id="a2d80-149">On the **Line details** FastTab, on the **Setup** tab, in the **Reservation** field, select **Automatic**, so that the item is automatically reserved from existing receipts when you create a sales order line.</span></span>
3. <span data-ttu-id="a2d80-150">На экспресс-вкладке **Продукт** в разделе **Аналитики отслеживания** в поле **Номер ГТД** выберите ранее созданный номер таможенной декларации.</span><span class="sxs-lookup"><span data-stu-id="a2d80-150">On the **Product** tab, in the **Tracking dimensions** section, in the **GTD number** field, select the customs declaration number that you created earlier.</span></span>

    ![Экспресс-вкладка сведений по строке на странице заказов на продажу](media/6%20Sales%20order.jpg)

4. <span data-ttu-id="a2d80-152">Задайте другие параметры заказа на продажу и создайте счет-фактуру обычным способом.</span><span class="sxs-lookup"><span data-stu-id="a2d80-152">Set other sales order parameters, and create a facture in the usual way.</span></span> <span data-ttu-id="a2d80-153">Столбец 11 в фактуре содержит информацию о номере таможенной декларации.</span><span class="sxs-lookup"><span data-stu-id="a2d80-153">Column 11 of the facture shows the information about the customs declaration number.</span></span>

    ![Фактура накладной](media/7%20Invoice-facture.jpg)

