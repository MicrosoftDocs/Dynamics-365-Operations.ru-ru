---
title: Создание договора покупки
description: Эта тема демонстрирует создание договора покупки.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1edfd4e56910376d0596eec5eff2af888f7dc98d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435981"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="6059d-103">Создание договора покупки</span><span class="sxs-lookup"><span data-stu-id="6059d-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6059d-104">Эта тема демонстрирует создание договора покупки.</span><span class="sxs-lookup"><span data-stu-id="6059d-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="6059d-105">Обычно это делает менеджер по закупкам.</span><span class="sxs-lookup"><span data-stu-id="6059d-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="6059d-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="6059d-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6059d-107">Перед началом процедуры необходимо настроить классификации договоров покупки.</span><span class="sxs-lookup"><span data-stu-id="6059d-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="6059d-108">После создания договора его можно использовать при создании заказа на покупку, в результате чего условия договора покупки будут скопированы в заголовок и в строки заказа, на которые влияет этот договор.</span><span class="sxs-lookup"><span data-stu-id="6059d-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="6059d-109">Создание нового договора покупки</span><span class="sxs-lookup"><span data-stu-id="6059d-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="6059d-110">Перейдите к **Область перехода > Модули > Закупки и источники > Договоры покупки > Договоры покупки**.</span><span class="sxs-lookup"><span data-stu-id="6059d-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="6059d-111">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="6059d-111">Click **New**.</span></span>
3. <span data-ttu-id="6059d-112">В поле **Счет поставщика** выберите раскрывающееся меню и выберите строку нужной записи.</span><span class="sxs-lookup"><span data-stu-id="6059d-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="6059d-113">В поле **Классификация договоров покупки** выберите раскрывающееся меню и выберите строку нужной записи.</span><span class="sxs-lookup"><span data-stu-id="6059d-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="6059d-114">Перейдите на экспресс-вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="6059d-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="6059d-115">В поле **Дата окончания срока действия** введите дату.</span><span class="sxs-lookup"><span data-stu-id="6059d-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="6059d-116">Эта дата окончания срока действия будет использоваться по умолчанию для всех строк обязательств и будет определять, как долго действует каждое конкретное обязательство.</span><span class="sxs-lookup"><span data-stu-id="6059d-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="6059d-117">В поле **Заголовок документа** введите имя для договора покупки.</span><span class="sxs-lookup"><span data-stu-id="6059d-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="6059d-118">Оставьте в поле **Обязательство по умолчанию** значение **Обязательство по качеству продукта** (или измените его, если выбрано другое значение).</span><span class="sxs-lookup"><span data-stu-id="6059d-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="6059d-119">Значение по умолчанию обязательства определяет доступные параметры в строках соглашения.</span><span class="sxs-lookup"><span data-stu-id="6059d-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="6059d-120">Если при создании строк соглашения вам необходим новый тип обязательства, необходимо изменить обязательство по умолчанию в заголовке.</span><span class="sxs-lookup"><span data-stu-id="6059d-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="6059d-121">Существует четыре типа обязательств: **Обязательство по количеству продукта** — на определенное количество продукта; **Обязательство по стоимости продукта** — на конкретную стоимость продукта в определенной валюте; **Обязательство по стоимости категории продукта** — на конкретную сумму в валюте в категории закупаемой продукции, когда сумма может быть представлена номенклатурой из каталога или номенклатурой не из каталога; **Обязательство по стоимости** — на конкретную сумму в валюте, которая может быть представлена любым продуктом или любой категорией закупаемой продукцией.</span><span class="sxs-lookup"><span data-stu-id="6059d-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="6059d-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6059d-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="6059d-123">Добавление обязательства</span><span class="sxs-lookup"><span data-stu-id="6059d-123">Add a commitment</span></span>
1. <span data-ttu-id="6059d-124">Выберите **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="6059d-124">Select **Add line**.</span></span>
2. <span data-ttu-id="6059d-125">В поле **Код номенклатуры** выберите требуемую запись из раскрывающегося меню.</span><span class="sxs-lookup"><span data-stu-id="6059d-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="6059d-126">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="6059d-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="6059d-127">Это общее количество, которое вы согласились купить у поставщика.</span><span class="sxs-lookup"><span data-stu-id="6059d-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="6059d-128">В поле **Цена за единицу** введите число.</span><span class="sxs-lookup"><span data-stu-id="6059d-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="6059d-129">Разверните раздел **Сведения о строке**.</span><span class="sxs-lookup"><span data-stu-id="6059d-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="6059d-130">Установите параметр **Используется максимум** в значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="6059d-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="6059d-131">Параметр **Используется максимум** ограничивает использование обязательства.</span><span class="sxs-lookup"><span data-stu-id="6059d-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="6059d-132">Вы можете купить не больше количества, указанного в поле **Количество** для строки.</span><span class="sxs-lookup"><span data-stu-id="6059d-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="6059d-133">Добавление условий заголовка</span><span class="sxs-lookup"><span data-stu-id="6059d-133">Add header conditions</span></span>
1. <span data-ttu-id="6059d-134">В области панели операций выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="6059d-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="6059d-135">Выберите **Изменить режим просмотра**.</span><span class="sxs-lookup"><span data-stu-id="6059d-135">Select **Change view**.</span></span>
3. <span data-ttu-id="6059d-136">Выберите **Представление заголовка**.</span><span class="sxs-lookup"><span data-stu-id="6059d-136">Select **Header view**.</span></span>
4. <span data-ttu-id="6059d-137">Разверните раздел **Условия**.</span><span class="sxs-lookup"><span data-stu-id="6059d-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="6059d-138">В поле **Способ оплаты** выберите требуемую запись в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="6059d-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="6059d-139">Здесь по умолчанию отображаются условия оплаты из счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="6059d-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="6059d-140">В поле **Способ поставки** выберите требуемую запись в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="6059d-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="6059d-141">В поле **Условия поставки** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="6059d-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="6059d-142">Подтверждение и активация договора</span><span class="sxs-lookup"><span data-stu-id="6059d-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="6059d-143">В области действий выберите **Договор покупки**.</span><span class="sxs-lookup"><span data-stu-id="6059d-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="6059d-144">Выберите **Подтверждение**.</span><span class="sxs-lookup"><span data-stu-id="6059d-144">Select **Confirmation**.</span></span> <span data-ttu-id="6059d-145">Установите параметр **Пометить договор как действующий** в значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="6059d-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="6059d-146">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6059d-146">Select **OK**.</span></span>
4. <span data-ttu-id="6059d-147">В области действий выберите **Договор покупки**.</span><span class="sxs-lookup"><span data-stu-id="6059d-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="6059d-148">Выберите **Подтверждения договора покупки**.</span><span class="sxs-lookup"><span data-stu-id="6059d-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="6059d-149">Параметр **Просмотр/печать** позволяет сформировать для договора покупки документ, который можно впоследствии напечатать или отправить поставщику.</span><span class="sxs-lookup"><span data-stu-id="6059d-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="6059d-150">Если вы позднее обновите соглашение и заново его подтвердите, здесь будут отображаться обе версии.</span><span class="sxs-lookup"><span data-stu-id="6059d-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="6059d-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6059d-151">Close the page.</span></span>

