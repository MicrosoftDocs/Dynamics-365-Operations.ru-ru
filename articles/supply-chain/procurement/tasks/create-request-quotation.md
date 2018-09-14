--- 
title: "Создание запроса предложения"
description: "Следующая процедура используется для создания запроса предложения."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4c09149fcbe5731126c2e48a37fafdf71c1d49df
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="a9721-103">Создание запроса предложения</span><span class="sxs-lookup"><span data-stu-id="a9721-103">Create a request for quotation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9721-104">Следующая процедура используется для создания запроса предложения.</span><span class="sxs-lookup"><span data-stu-id="a9721-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="a9721-105">Обычно это делает специалист по закупке.</span><span class="sxs-lookup"><span data-stu-id="a9721-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="a9721-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="a9721-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a9721-107">Перед началом процедуры необходимо настроить типы обращений.</span><span class="sxs-lookup"><span data-stu-id="a9721-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="a9721-108">После выполнения этой задачи, создания и отправки запроса предложения вы можете ввести ответы для каждого поставщика, сравнить их и заключить контракт.</span><span class="sxs-lookup"><span data-stu-id="a9721-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="a9721-109">Подготовка нового запроса предложения</span><span class="sxs-lookup"><span data-stu-id="a9721-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="a9721-110">Перейдите в раздел "Закупки и источники" > "Запросы предложений" > "Все запросы предложений".</span><span class="sxs-lookup"><span data-stu-id="a9721-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="a9721-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a9721-111">Click New.</span></span>
    * <span data-ttu-id="a9721-112">Доступны следующие типы покупки: "Заявка на покупку" (это значение по умолчанию) — документ, который подтверждает предложение купить продукт, или принятие предложения продажи продуктов в обмен на платеж.</span><span class="sxs-lookup"><span data-stu-id="a9721-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="a9721-113">"Заявка на покупку" — этот тип выбирается автоматически при создании запроса предложения непосредственно из заявки на закупку.</span><span class="sxs-lookup"><span data-stu-id="a9721-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="a9721-114">При выборе этого параметра вручную выдается ошибка.</span><span class="sxs-lookup"><span data-stu-id="a9721-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="a9721-115">"Договор покупки" — договор на покупку определенного количества продукта или продукта на определенную сумму за период времени.</span><span class="sxs-lookup"><span data-stu-id="a9721-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="a9721-116">При выборе этого параметра необходимо выбрать диапазон дат, который применяется к договору покупки.</span><span class="sxs-lookup"><span data-stu-id="a9721-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="a9721-117">В поле "Заголовок документа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a9721-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="a9721-118">В поле "Тип обращения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a9721-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="a9721-119">Если метод оценки с типом связан типом обращения, то этот метод оценки будет использоваться по умолчанию в создаваемом запросе предложения.</span><span class="sxs-lookup"><span data-stu-id="a9721-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="a9721-120">Метод оценки можно изменить позже.</span><span class="sxs-lookup"><span data-stu-id="a9721-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="a9721-121">В поле "Дата поставки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="a9721-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="a9721-122">Выберите дату, до которой вы хотите получить номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a9721-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="a9721-123">В поле "Дата и время окончания срока действия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="a9721-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="a9721-124">Укажите дату и время, до которых поставщики должны ответить на запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="a9721-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="a9721-125">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a9721-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a9721-126">Адресом поставки по умолчанию будет адрес склада.</span><span class="sxs-lookup"><span data-stu-id="a9721-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="a9721-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9721-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="a9721-128">Добавление строк</span><span class="sxs-lookup"><span data-stu-id="a9721-128">Add lines</span></span>
    * <span data-ttu-id="a9721-129">После указания основных сведений о запросе предложения необходимо указать товары или услуги, по которым требуется получить предложения от поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a9721-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="a9721-130">Номенклатура — это тип строки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a9721-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="a9721-131">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a9721-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a9721-132">При использовании USMF можно выбрать T0020.</span><span class="sxs-lookup"><span data-stu-id="a9721-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="a9721-133">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="a9721-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="a9721-134">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="a9721-134">Click Add line.</span></span>
4. <span data-ttu-id="a9721-135">В поле "Тип строки" выберите "Категория".</span><span class="sxs-lookup"><span data-stu-id="a9721-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="a9721-136">Можно использовать тип строки "Категория" для создания запросов предложений по нескладским товарам или услугам.</span><span class="sxs-lookup"><span data-stu-id="a9721-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="a9721-137">В этом случае необходимо выбрать тип товаров или услуг в иерархии категорий закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="a9721-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="a9721-138">В поле "Категория закупаемой продукции " введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a9721-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="a9721-139">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a9721-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="a9721-140">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="a9721-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="a9721-141">В поле "Единица измерения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a9721-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="a9721-142">Добавить поставщиков</span><span class="sxs-lookup"><span data-stu-id="a9721-142">Add vendors</span></span>
1. <span data-ttu-id="a9721-143">Щелкните заголовок, чтобы изменить представление строк на представление заголовка.</span><span class="sxs-lookup"><span data-stu-id="a9721-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="a9721-144">Развернуть раздел "Поставщик".</span><span class="sxs-lookup"><span data-stu-id="a9721-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="a9721-145">Щелкните "Автоматически добавлять поставщиков".</span><span class="sxs-lookup"><span data-stu-id="a9721-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="a9721-146">Можно автоматически добавить поставщиков в запрос предложения на основе категории закупаемой продукции запрашиваемых номенклатур.</span><span class="sxs-lookup"><span data-stu-id="a9721-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="a9721-147">Если нет утвержденных поставщиков для категорий, включенных в строки, поставщиков можно добавить вручную.</span><span class="sxs-lookup"><span data-stu-id="a9721-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="a9721-148">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="a9721-148">Click Add.</span></span>
5. <span data-ttu-id="a9721-149">В поле "Счет поставщика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a9721-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="a9721-150">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="a9721-150">Click Add.</span></span>
7. <span data-ttu-id="a9721-151">В поле "Счет поставщика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a9721-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="a9721-152">После выбора поставщика статус изменится на "Создано".</span><span class="sxs-lookup"><span data-stu-id="a9721-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="a9721-153">Это означает, что информация о поставщике сохранена в запросе предложения, но запрос предложения не отправлен поставщику.</span><span class="sxs-lookup"><span data-stu-id="a9721-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="a9721-154">Можно добавить поставщика в запрос предложения независимо от статуса поставщика.</span><span class="sxs-lookup"><span data-stu-id="a9721-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="a9721-155">Отправить запрос предложения поставщикам</span><span class="sxs-lookup"><span data-stu-id="a9721-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="a9721-156">Нажмите кнопку Отправить.</span><span class="sxs-lookup"><span data-stu-id="a9721-156">Click Send.</span></span>
    * <span data-ttu-id="a9721-157">На странице "Отправка запроса предложения" убедитесь, что в списке указаны именно те поставщики, которые должны получить запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="a9721-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="a9721-158">Нажмите кнопку Печать.</span><span class="sxs-lookup"><span data-stu-id="a9721-158">Click Print.</span></span>
    * <span data-ttu-id="a9721-159">Это диалоговое окно позволяет напечатать запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="a9721-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="a9721-160">Если выбрать печать листа ответа, содержимое этого листа определяется в параметрах модуля "Закупки и источники".</span><span class="sxs-lookup"><span data-stu-id="a9721-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="a9721-161">Чтобы выбрать способ печати листов ответа, при открытии диалогового окна "Печать" щелкните "Расширенные параметры печати".</span><span class="sxs-lookup"><span data-stu-id="a9721-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="a9721-162">Для каждого поставщика будет напечатан один запрос предложения, содержащий строки со статусом "Создано" или "Отправлено".</span><span class="sxs-lookup"><span data-stu-id="a9721-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="a9721-163">Отмененные строки и строки с зарегистрированными ответами не печатаются.</span><span class="sxs-lookup"><span data-stu-id="a9721-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="a9721-164">Щелкните "Отмена".</span><span class="sxs-lookup"><span data-stu-id="a9721-164">Click Cancel.</span></span>
4. <span data-ttu-id="a9721-165">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9721-165">Click OK.</span></span>
5. <span data-ttu-id="a9721-166">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a9721-166">Close the page.</span></span>
6. <span data-ttu-id="a9721-167">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a9721-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="a9721-168">Просмотр журнала запросов предложений</span><span class="sxs-lookup"><span data-stu-id="a9721-168">View the RFQ journal</span></span>
1. <span data-ttu-id="a9721-169">Перейдите в раздел "Закупки и источники" > "Запросы предложений" > "Обработка результатов по запросам предложения" > "Журналы запросов предложений".</span><span class="sxs-lookup"><span data-stu-id="a9721-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="a9721-170">Щелкните "Просмотр/печать".</span><span class="sxs-lookup"><span data-stu-id="a9721-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="a9721-171">Щелкните "Просмотр оригинала".</span><span class="sxs-lookup"><span data-stu-id="a9721-171">Click Original preview.</span></span>
4. <span data-ttu-id="a9721-172">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a9721-172">Close the page.</span></span>
5. <span data-ttu-id="a9721-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a9721-173">Close the page.</span></span>


