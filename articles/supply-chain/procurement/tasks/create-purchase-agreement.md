---
title: Создание договора покупки
description: Эта процедура демонстрирует создание договора покупки.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df74eaad51fc4ef28caf96e4bcdc7b03f7e6ec3b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836375"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="bdeb9-103">Создание договора покупки</span><span class="sxs-lookup"><span data-stu-id="bdeb9-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bdeb9-104">Эта процедура демонстрирует создание договора покупки.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="bdeb9-105">Обычно это делает менеджер по закупкам.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="bdeb9-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="bdeb9-107">Перед началом процедуры необходимо настроить классификации договоров покупки.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="bdeb9-108">После создания договора его можно использовать при создании заказа на покупку, в результате чего условия договора покупки будут скопированы в заголовок и в строки заказа, на которые влияет этот договор.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="bdeb9-109">Создание нового договора покупки</span><span class="sxs-lookup"><span data-stu-id="bdeb9-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="bdeb9-110">Перейдите в раздел "Закупки и источники" > "Договоры покупки" > "Договоры покупки".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="bdeb9-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-111">Click New.</span></span>
3. <span data-ttu-id="bdeb9-112">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bdeb9-113">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="bdeb9-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="bdeb9-115">В поле "Классификация договоров покупки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bdeb9-116">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="bdeb9-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bdeb9-118">Разверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-118">Expand the General section.</span></span>
10. <span data-ttu-id="bdeb9-119">В поле "Дата окончания срока действия" введите дату.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="bdeb9-120">Эта дата окончания срока действия будет использоваться по умолчанию для всех строк обязательств и будет определять, как долго действует каждое конкретное обязательство.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="bdeb9-121">В поле "Заголовок документа" введите имя для договора покупки.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="bdeb9-122">Оставьте в поле "Обязательство по умолчанию" значение "Обязательство по качеству продукта" (или измените его, если выбрано другое значение).</span><span class="sxs-lookup"><span data-stu-id="bdeb9-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="bdeb9-123">Значение по умолчанию обязательства определяет доступные параметры в строках соглашения.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="bdeb9-124">Если при создании строк соглашения вам необходим новый тип обязательства, необходимо изменить обязательство по умолчанию в заголовке.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="bdeb9-125">Существует четыре типа обязательств: обязательство по количеству продукта — на определенное количество продукта; обязательство по стоимости продукта — на конкретную стоимость продукта в определенной валюте; обязательство по стоимости категории продукта — на конкретную сумму в валюте в категории закупаемой продукции, когда сумма может быть представлена номенклатурой из каталога или номенклатурой не из каталога; обязательство по стоимости — на конкретную сумму в валюте, которая может быть представлена любым продуктом или любой категорией закупаемой продукцией.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="bdeb9-126">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="bdeb9-127">Добавление обязательства</span><span class="sxs-lookup"><span data-stu-id="bdeb9-127">Add a commitment</span></span>
1. <span data-ttu-id="bdeb9-128">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-128">Click Add line.</span></span>
2. <span data-ttu-id="bdeb9-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="bdeb9-130">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bdeb9-131">Выберите продукт, обязательство по которому требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="bdeb9-132">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="bdeb9-133">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="bdeb9-134">Это общее количество, которое вы согласились купить у поставщика.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="bdeb9-135">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="bdeb9-136">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="bdeb9-137">Установите параметр "Используется максимум" в значение "Да".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="bdeb9-138">Параметр "Используется максимум" ограничивает использование обязательства.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="bdeb9-139">Вы можете купить не больше количества, указанного в поле "Количество" для строки.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="bdeb9-140">Сверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="bdeb9-141">Добавление условий заголовка</span><span class="sxs-lookup"><span data-stu-id="bdeb9-141">Add header conditions</span></span>
1. <span data-ttu-id="bdeb9-142">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="bdeb9-143">Щелкните "Изменить режим просмотра".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-143">Click Change view.</span></span>
3. <span data-ttu-id="bdeb9-144">Щелкните Вид заголовка.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-144">Click Header view.</span></span>
4. <span data-ttu-id="bdeb9-145">Разверните раздел "Условия".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="bdeb9-146">В поле "Способ оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bdeb9-147">Здесь по умолчанию отображаются условия оплаты из счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="bdeb9-148">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="bdeb9-149">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="bdeb9-150">В поле "Способ поставки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="bdeb9-151">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="bdeb9-152">В поле "Условия поставки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="bdeb9-153">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="bdeb9-154">Подтверждение и активация договора</span><span class="sxs-lookup"><span data-stu-id="bdeb9-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="bdeb9-155">В области действий щелкните "Договор покупки".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="bdeb9-156">Щелкните "Подтверждение".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-156">Click Confirmation.</span></span>
    * <span data-ttu-id="bdeb9-157">Установите параметр "Пометить договор как действующий" в значение "Да".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="bdeb9-158">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-158">Click OK.</span></span>
4. <span data-ttu-id="bdeb9-159">В области действий щелкните "Договор покупки".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="bdeb9-160">Щелкните "Подтверждения договора покупки".</span><span class="sxs-lookup"><span data-stu-id="bdeb9-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="bdeb9-161">Параметр "Просмотр/печать" позволяет сформировать для договора покупки документ, который можно впоследствии напечатать или отправить поставщику.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="bdeb9-162">Если вы позднее обновите соглашение и заново его подтвердите, здесь будут отображаться обе версии.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="bdeb9-163">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-163">Close the page.</span></span>

