---
title: Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 3 — Создание формата)
description: В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами в выходных данных электронной отчетности.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4324ed62c56abea6d90d83d950429b6ddf7a84b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142043"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="4f5fc-103">Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 3 — Создание формата)</span><span class="sxs-lookup"><span data-stu-id="4f5fc-103">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f5fc-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="4f5fc-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="4f5fc-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="4f5fc-107">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="4f5fc-108">Создание формата для обработки накладных</span><span class="sxs-lookup"><span data-stu-id="4f5fc-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="4f5fc-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4f5fc-110">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="4f5fc-111">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="4f5fc-112">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="4f5fc-113">Вы создадите формат для создания электронных сообщений со сведениями о любых файлах, которые были приложены к заказу на продажу, который связан электронной обработкой накладной.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="4f5fc-114">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="4f5fc-115">В поле "Создать" введите "Формат, основанный на модели данных Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="4f5fc-116">В поле "Имя" введите "Пример сообщения электронной накладной".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="4f5fc-117">Пример сообщения электронной накладной</span><span class="sxs-lookup"><span data-stu-id="4f5fc-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="4f5fc-118">В поле "Определение модели данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="4f5fc-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="4f5fc-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="4f5fc-120">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="4f5fc-121">Разработка формата для заполнения вложений при создании сообщения в формате MIME</span><span class="sxs-lookup"><span data-stu-id="4f5fc-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="4f5fc-122">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-122">Click Designer.</span></span>
2. <span data-ttu-id="4f5fc-123">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="4f5fc-124">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="4f5fc-125">В поле "Имя" введите "Накладная".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="4f5fc-126">Счет-фактура</span><span class="sxs-lookup"><span data-stu-id="4f5fc-126">Invoice</span></span>  
5. <span data-ttu-id="4f5fc-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-127">Click OK.</span></span>
6. <span data-ttu-id="4f5fc-128">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="4f5fc-129">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="4f5fc-130">В поле "Имя" введите "SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="4f5fc-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="4f5fc-131">SalesOrder</span></span>  
9. <span data-ttu-id="4f5fc-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-132">Click OK.</span></span>
10. <span data-ttu-id="4f5fc-133">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="4f5fc-134">В поле "Имя" введите "InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="4f5fc-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="4f5fc-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="4f5fc-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-136">Click OK.</span></span>
13. <span data-ttu-id="4f5fc-137">Щелкните "Добавить атрибут".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="4f5fc-138">В поле "Имя" введите "InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="4f5fc-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="4f5fc-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="4f5fc-140">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-140">Click OK.</span></span>
16. <span data-ttu-id="4f5fc-141">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="4f5fc-142">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="4f5fc-143">В поле "Имя" введите "EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="4f5fc-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="4f5fc-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="4f5fc-145">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-145">Click OK.</span></span>
20. <span data-ttu-id="4f5fc-146">В дереве выберите "Накладная\EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="4f5fc-147">Щелкните "Добавить элемент".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-147">Click Add Element.</span></span>
22. <span data-ttu-id="4f5fc-148">В поле "Имя" введите "Документ".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="4f5fc-149">Документ</span><span class="sxs-lookup"><span data-stu-id="4f5fc-149">Document</span></span>  
23. <span data-ttu-id="4f5fc-150">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-150">Click OK.</span></span>
24. <span data-ttu-id="4f5fc-151">В дереве выберите "Накладная\EnclosedDocs\Документ".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="4f5fc-152">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="4f5fc-153">В дереве выберите "'XML\Атрибут".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="4f5fc-154">В поле "Имя" введите "FileName".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="4f5fc-155">FileName</span><span class="sxs-lookup"><span data-stu-id="4f5fc-155">FileName</span></span>  
28. <span data-ttu-id="4f5fc-156">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-156">Click OK.</span></span>
29. <span data-ttu-id="4f5fc-157">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="4f5fc-158">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="4f5fc-159">В поле "Имя" введите "FileContent".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="4f5fc-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="4f5fc-160">FileContent</span></span>  
32. <span data-ttu-id="4f5fc-161">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-161">Click OK.</span></span>
33. <span data-ttu-id="4f5fc-162">В дереве выберите "Накладная\EnclosedDocs\Документ\FileContent".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="4f5fc-163">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="4f5fc-164">В дереве выберите "Текст\Base64".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="4f5fc-165">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="4f5fc-166">Сопоставление элементов формата с моделью данных в качестве источника данных</span><span class="sxs-lookup"><span data-stu-id="4f5fc-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="4f5fc-167">В дереве выберите "Накладная\SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="4f5fc-168">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="4f5fc-169">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="4f5fc-170">В дереве выберите "модуль\Номер заказа на продажу(SalesId)".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="4f5fc-171">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-171">Click Bind.</span></span>
6. <span data-ttu-id="4f5fc-172">В дереве выберите "Накладная\InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="4f5fc-173">В дереве разверните "модель\Базовая накладная(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="4f5fc-174">В дереве выберите "модель\Базовая накладная(InvoiceBase)\Номер накладной(Id)".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="4f5fc-175">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-175">Click Bind.</span></span>
10. <span data-ttu-id="4f5fc-176">В дереве выберите "Накладная\InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="4f5fc-177">В дереве выберите "модель\Базовая накладная(InvoiceBase)\Сумма накладной(Amount)".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="4f5fc-178">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-178">Click Bind.</span></span>
13. <span data-ttu-id="4f5fc-179">В дереве разверните "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="4f5fc-180">В дереве выберите "модель\Вложения накладной\Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="4f5fc-181">В дереве выберите "Накладная\EnclosedDocs\Документ\FileContent\Base64".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="4f5fc-182">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-182">Click Bind.</span></span>
17. <span data-ttu-id="4f5fc-183">В дереве выберите "модель\Вложения накладной\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="4f5fc-184">В дереве выберите "Накладная\EnclosedDocs\Документ\FileName".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="4f5fc-185">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-185">Click Bind.</span></span>
20. <span data-ttu-id="4f5fc-186">В дереве выберите "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="4f5fc-187">В дереве выберите "Накладная\EnclosedDocs\Документ".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="4f5fc-188">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-188">Click Bind.</span></span>
23. <span data-ttu-id="4f5fc-189">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4f5fc-189">Click Save.</span></span>
24. <span data-ttu-id="4f5fc-190">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-190">Close the page.</span></span>

