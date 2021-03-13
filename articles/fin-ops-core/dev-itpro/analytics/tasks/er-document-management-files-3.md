---
title: Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 3 — Создание формата)
description: В этой теме описывается, как настроить формат электронной отчетности, чтобы в выходных данных электронной отчетности использовать файлы управления документами. (Часть 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 432cf4c41a7a223ab07b02edf6da7eac9965cff0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092624"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="f7f4f-104">Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 3 — Создание формата)</span><span class="sxs-lookup"><span data-stu-id="f7f4f-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7f4f-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f7f4f-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="f7f4f-107">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="f7f4f-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="f7f4f-109">Создание формата для обработки накладных</span><span class="sxs-lookup"><span data-stu-id="f7f4f-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="f7f4f-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f7f4f-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f7f4f-112">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="f7f4f-113">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="f7f4f-114">Вы создадите формат для создания электронных сообщений со сведениями о любых файлах, которые были приложены к заказу на продажу, который связан электронной обработкой накладной.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="f7f4f-115">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="f7f4f-116">В поле "Создать" введите "Формат, основанный на модели данных Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="f7f4f-117">В поле "Имя" введите "Пример сообщения электронной накладной".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="f7f4f-118">Пример сообщения электронной накладной</span><span class="sxs-lookup"><span data-stu-id="f7f4f-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="f7f4f-119">В поле "Определение модели данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="f7f4f-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="f7f4f-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="f7f4f-121">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="f7f4f-122">Разработка формата для заполнения вложений при создании сообщения в формате MIME</span><span class="sxs-lookup"><span data-stu-id="f7f4f-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="f7f4f-123">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-123">Click Designer.</span></span>
2. <span data-ttu-id="f7f4f-124">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="f7f4f-125">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="f7f4f-126">В поле "Имя" введите "Накладная".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="f7f4f-127">Счет-фактура</span><span class="sxs-lookup"><span data-stu-id="f7f4f-127">Invoice</span></span>  
5. <span data-ttu-id="f7f4f-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-128">Click OK.</span></span>
6. <span data-ttu-id="f7f4f-129">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="f7f4f-130">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="f7f4f-131">В поле "Имя" введите "SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="f7f4f-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="f7f4f-132">SalesOrder</span></span>  
9. <span data-ttu-id="f7f4f-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-133">Click OK.</span></span>
10. <span data-ttu-id="f7f4f-134">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="f7f4f-135">В поле "Имя" введите "InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="f7f4f-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="f7f4f-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="f7f4f-137">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-137">Click OK.</span></span>
13. <span data-ttu-id="f7f4f-138">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="f7f4f-139">В поле "Имя" введите "InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="f7f4f-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="f7f4f-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="f7f4f-141">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-141">Click OK.</span></span>
16. <span data-ttu-id="f7f4f-142">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="f7f4f-143">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="f7f4f-144">В поле "Имя" введите "EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="f7f4f-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="f7f4f-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="f7f4f-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-146">Click OK.</span></span>
20. <span data-ttu-id="f7f4f-147">В дереве выберите "Накладная\EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="f7f4f-148">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-148">Click Add Element.</span></span>
22. <span data-ttu-id="f7f4f-149">В поле "Имя" введите "Документ".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="f7f4f-150">Документ</span><span class="sxs-lookup"><span data-stu-id="f7f4f-150">Document</span></span>  
23. <span data-ttu-id="f7f4f-151">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-151">Click OK.</span></span>
24. <span data-ttu-id="f7f4f-152">В дереве выберите "Накладная\EnclosedDocs\Документ".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="f7f4f-153">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="f7f4f-154">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="f7f4f-155">В поле "Имя" введите "FileName".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="f7f4f-156">FileName</span><span class="sxs-lookup"><span data-stu-id="f7f4f-156">FileName</span></span>  
28. <span data-ttu-id="f7f4f-157">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-157">Click OK.</span></span>
29. <span data-ttu-id="f7f4f-158">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="f7f4f-159">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="f7f4f-160">В поле "Имя" введите "FileContent".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="f7f4f-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="f7f4f-161">FileContent</span></span>  
32. <span data-ttu-id="f7f4f-162">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-162">Click OK.</span></span>
33. <span data-ttu-id="f7f4f-163">В дереве выберите "Накладная\EnclosedDocs\Документ\FileContent".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="f7f4f-164">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="f7f4f-165">В дереве выберите "Текст\Base64".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="f7f4f-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="f7f4f-167">Сопоставление элементов формата с моделью данных в качестве источника данных</span><span class="sxs-lookup"><span data-stu-id="f7f4f-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="f7f4f-168">В дереве выберите "Накладная\SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="f7f4f-169">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="f7f4f-170">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="f7f4f-171">В дереве выберите "модуль\Номер заказа на продажу(SalesId)".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="f7f4f-172">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-172">Click Bind.</span></span>
6. <span data-ttu-id="f7f4f-173">В дереве выберите "Накладная\InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="f7f4f-174">В дереве разверните "модель\Базовая накладная(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="f7f4f-175">В дереве выберите "модель\Базовая накладная(InvoiceBase)\Номер накладной(Id)".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="f7f4f-176">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-176">Click Bind.</span></span>
10. <span data-ttu-id="f7f4f-177">В дереве выберите "Накладная\InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="f7f4f-178">В дереве выберите "модель\Базовая накладная(InvoiceBase)\Сумма накладной(Amount)".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="f7f4f-179">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-179">Click Bind.</span></span>
13. <span data-ttu-id="f7f4f-180">В дереве разверните "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="f7f4f-181">В дереве выберите "модель\Вложения накладной\Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="f7f4f-182">В дереве выберите "Накладная\EnclosedDocs\Документ\FileContent\Base64".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="f7f4f-183">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-183">Click Bind.</span></span>
17. <span data-ttu-id="f7f4f-184">В дереве выберите "модель\Вложения накладной\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="f7f4f-185">В дереве выберите "Накладная\EnclosedDocs\Документ\FileName".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="f7f4f-186">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-186">Click Bind.</span></span>
20. <span data-ttu-id="f7f4f-187">В дереве выберите "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="f7f4f-188">В дереве выберите "Накладная\EnclosedDocs\Документ".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="f7f4f-189">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-189">Click Bind.</span></span>
23. <span data-ttu-id="f7f4f-190">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f7f4f-190">Click Save.</span></span>
24. <span data-ttu-id="f7f4f-191">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f7f4f-191">Close the page.</span></span>

