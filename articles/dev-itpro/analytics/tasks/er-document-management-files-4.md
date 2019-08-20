---
title: Выполнение форматов для использования файлов управления документами в выходных данных электронной отчетности
description: В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами в выходных данных электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8dc541af4d26b61ff9b90e08a8ca2c6a6bb8e70
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850263"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4-run-format"></a><span data-ttu-id="f2485-103">Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 4. Выполнение формата)</span><span class="sxs-lookup"><span data-stu-id="f2485-103">ER Use Document Management files in format outputs (Part 4: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2485-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f2485-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f2485-105">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="f2485-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="f2485-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 3. Создание формата)".</span><span class="sxs-lookup"><span data-stu-id="f2485-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="f2485-107">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="f2485-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="f2485-108">Добавьте необходимые вложения для заказа на продажу одной накладной</span><span class="sxs-lookup"><span data-stu-id="f2485-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="f2485-109">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Открытые накладные клиента".</span><span class="sxs-lookup"><span data-stu-id="f2485-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="f2485-110">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="f2485-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f2485-111">Например, отфильтруйте поле "Накладная" по значению "CIV-000148".</span><span class="sxs-lookup"><span data-stu-id="f2485-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="f2485-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="f2485-112">CIV-000148</span></span>  
3. <span data-ttu-id="f2485-113">Нажмите, чтобы перейти по ссылке выбранной накладной.</span><span class="sxs-lookup"><span data-stu-id="f2485-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="f2485-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="f2485-114">CIV-000148</span></span>  
4. <span data-ttu-id="f2485-115">Щелкните для перехода по ссылке в поле "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="f2485-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="f2485-116">000148</span><span class="sxs-lookup"><span data-stu-id="f2485-116">000148</span></span>  
5. <span data-ttu-id="f2485-117">В поле "Строки или заголовок" выберите вариант "Заголовок".</span><span class="sxs-lookup"><span data-stu-id="f2485-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="f2485-118">Выберите "Заголовок" для указания, чтобы это будет целью для добавления вложений.</span><span class="sxs-lookup"><span data-stu-id="f2485-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="f2485-119">Щелкните "Привязать".</span><span class="sxs-lookup"><span data-stu-id="f2485-119">Click Attach.</span></span>
    * <span data-ttu-id="f2485-120">Добавьте несколько файлов как вложения для данного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="f2485-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="f2485-121">Используйте файлы типов документов, поддерживаемых модулем управления документами (с расширениями файла DOCX, DPF, XML, JPG и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f2485-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="f2485-122">Просмотрите и выберите файлы, которые должны быть вложены и далее обработаны с соответствующей накладной в электронном сообщении электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f2485-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="f2485-123">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f2485-123">Click New.</span></span>
8. <span data-ttu-id="f2485-124">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="f2485-124">Click File.</span></span>
9. <span data-ttu-id="f2485-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f2485-125">Click New.</span></span>
10. <span data-ttu-id="f2485-126">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="f2485-126">Click File.</span></span>
11. <span data-ttu-id="f2485-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f2485-127">Close the page.</span></span>
12. <span data-ttu-id="f2485-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f2485-128">Close the page.</span></span>
13. <span data-ttu-id="f2485-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f2485-129">Close the page.</span></span>
14. <span data-ttu-id="f2485-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f2485-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="f2485-131">Выполните разработанный отчет для выбранной накладной</span><span class="sxs-lookup"><span data-stu-id="f2485-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="f2485-132">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="f2485-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f2485-133">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="f2485-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="f2485-134">В дереве разверните узел "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="f2485-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="f2485-135">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)\Пример сообщения электронной накладной".</span><span class="sxs-lookup"><span data-stu-id="f2485-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="f2485-136">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="f2485-136">Click Run.</span></span>
6. <span data-ttu-id="f2485-137">Разверните раздел "Записи для добавления ()".</span><span class="sxs-lookup"><span data-stu-id="f2485-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="f2485-138">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="f2485-138">Click Filter.</span></span>
8. <span data-ttu-id="f2485-139">Выберите строку журнала накладных клиента и поле "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="f2485-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="f2485-140">В поле "Критерии" введите "000148".</span><span class="sxs-lookup"><span data-stu-id="f2485-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="f2485-141">В поле «Заказ на продажу» критериев введите номер заказа 000148.</span><span class="sxs-lookup"><span data-stu-id="f2485-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="f2485-142">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f2485-142">Click OK.</span></span>
11. <span data-ttu-id="f2485-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f2485-143">Click OK.</span></span>
    * <span data-ttu-id="f2485-144">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="f2485-144">Review the generated output.</span></span> <span data-ttu-id="f2485-145">Обратите внимание, что для каждого вложения был создан один узел XML.</span><span class="sxs-lookup"><span data-stu-id="f2485-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="f2485-146">Содержимое вложения записывается в выходные данные XML в текстовом формате MIME (base64).</span><span class="sxs-lookup"><span data-stu-id="f2485-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  

