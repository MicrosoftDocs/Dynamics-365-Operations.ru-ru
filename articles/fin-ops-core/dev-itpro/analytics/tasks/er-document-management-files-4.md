---
title: Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 4 — Выполнение формата)
description: В этой теме описывается, как настроить формат электронной отчетности, чтобы в выходных данных электронной отчетности использовать файлы управления документами. (Часть 4)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a7c9705d8b53ef13cd3faf13290f3f1b1d1c43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749125"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="2a2c5-104">Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 4 — Выполнение формата)</span><span class="sxs-lookup"><span data-stu-id="2a2c5-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a2c5-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="2a2c5-106">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="2a2c5-107">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 3. Создание формата)".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="2a2c5-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="2a2c5-109">Добавьте необходимые вложения для заказа на продажу одной накладной</span><span class="sxs-lookup"><span data-stu-id="2a2c5-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="2a2c5-110">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Открытые накладные клиента".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="2a2c5-111">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2a2c5-112">Например, отфильтруйте поле "Накладная" по значению "CIV-000148".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="2a2c5-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="2a2c5-113">CIV-000148</span></span>  
3. <span data-ttu-id="2a2c5-114">Нажмите, чтобы перейти по ссылке выбранной накладной.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="2a2c5-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="2a2c5-115">CIV-000148</span></span>  
4. <span data-ttu-id="2a2c5-116">Щелкните для перехода по ссылке в поле "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="2a2c5-117">000148</span><span class="sxs-lookup"><span data-stu-id="2a2c5-117">000148</span></span>  
5. <span data-ttu-id="2a2c5-118">В поле "Строки или заголовок" выберите вариант "Заголовок".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="2a2c5-119">Выберите "Заголовок" для указания, чтобы это будет целью для добавления вложений.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="2a2c5-120">Щелкните "Привязать".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-120">Click Attach.</span></span>
    * <span data-ttu-id="2a2c5-121">Добавьте несколько файлов как вложения для данного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="2a2c5-122">Используйте файлы типов документов, поддерживаемых модулем управления документами (с расширениями файла DOCX, DPF, XML, JPG и т. д.).</span><span class="sxs-lookup"><span data-stu-id="2a2c5-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="2a2c5-123">Просмотрите и выберите файлы, которые должны быть вложены и далее обработаны с соответствующей накладной в электронном сообщении электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="2a2c5-124">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-124">Click New.</span></span>
8. <span data-ttu-id="2a2c5-125">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-125">Click File.</span></span>
9. <span data-ttu-id="2a2c5-126">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-126">Click New.</span></span>
10. <span data-ttu-id="2a2c5-127">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-127">Click File.</span></span>
11. <span data-ttu-id="2a2c5-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-128">Close the page.</span></span>
12. <span data-ttu-id="2a2c5-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-129">Close the page.</span></span>
13. <span data-ttu-id="2a2c5-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-130">Close the page.</span></span>
14. <span data-ttu-id="2a2c5-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="2a2c5-132">Выполните разработанный отчет для выбранной накладной</span><span class="sxs-lookup"><span data-stu-id="2a2c5-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="2a2c5-133">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="2a2c5-134">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="2a2c5-135">В дереве разверните узел "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="2a2c5-136">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)\Пример сообщения электронной накладной".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="2a2c5-137">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-137">Click Run.</span></span>
6. <span data-ttu-id="2a2c5-138">Разверните раздел "Записи для добавления ()".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="2a2c5-139">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-139">Click Filter.</span></span>
8. <span data-ttu-id="2a2c5-140">Выберите строку журнала накладных клиента и поле "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="2a2c5-141">В поле "Критерии" введите "000148".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="2a2c5-142">В поле "Заказ на продажу" критериев введите номер заказа 000148.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="2a2c5-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-143">Click OK.</span></span>
11. <span data-ttu-id="2a2c5-144">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2a2c5-144">Click OK.</span></span>
    * <span data-ttu-id="2a2c5-145">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-145">Review the generated output.</span></span> <span data-ttu-id="2a2c5-146">Обратите внимание, что для каждого вложения был создан один узел XML.</span><span class="sxs-lookup"><span data-stu-id="2a2c5-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="2a2c5-147">Содержимое вложения записывается в выходные данные XML в текстовом формате MIME (base64).</span><span class="sxs-lookup"><span data-stu-id="2a2c5-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]