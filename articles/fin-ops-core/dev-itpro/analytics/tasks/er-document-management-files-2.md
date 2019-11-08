---
title: Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)
description: В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24eba0402caefb611a212db19cdb8feafa7c1fee
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550748"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="296f5-103">Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)</span><span class="sxs-lookup"><span data-stu-id="296f5-103">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="296f5-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="296f5-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="296f5-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="296f5-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="296f5-106">Для выполнения этих действий необходимо сначала выполнить шаги в руководстве по задаче "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 1. Подготовка модели данных)".</span><span class="sxs-lookup"><span data-stu-id="296f5-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="296f5-107">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="296f5-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="296f5-108">Расширение модели данных, чтобы представлять в ней файлы управления документами</span><span class="sxs-lookup"><span data-stu-id="296f5-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="296f5-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="296f5-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="296f5-110">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="296f5-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="296f5-111">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="296f5-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="296f5-112">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="296f5-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="296f5-113">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="296f5-113">Click Designer.</span></span>
6. <span data-ttu-id="296f5-114">В дереве выберите "Накладная клиента(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="296f5-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="296f5-115">Мы расширим эту модель данных, чтобы представлять в ней любые файлы, которые были приложены к заказу на продажу, который относится к электронной обработке накладной.</span><span class="sxs-lookup"><span data-stu-id="296f5-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="296f5-116">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="296f5-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="296f5-117">В поле "Имя" введите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="296f5-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="296f5-118">Вложения накладной</span><span class="sxs-lookup"><span data-stu-id="296f5-118">Invoice attachments</span></span>  
9. <span data-ttu-id="296f5-119">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="296f5-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="296f5-120">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="296f5-120">Click Add.</span></span>
11. <span data-ttu-id="296f5-121">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="296f5-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="296f5-122">В поле "Имя" введите "Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="296f5-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="296f5-123">Содержание файла</span><span class="sxs-lookup"><span data-stu-id="296f5-123">File content</span></span>  
13. <span data-ttu-id="296f5-124">В поле "Тип элемента" выберите "Контейнер".</span><span class="sxs-lookup"><span data-stu-id="296f5-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="296f5-125">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="296f5-125">Click Add.</span></span>
15. <span data-ttu-id="296f5-126">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="296f5-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="296f5-127">В поле "Имя" введите "Имя файла".</span><span class="sxs-lookup"><span data-stu-id="296f5-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="296f5-128">Имя файла</span><span class="sxs-lookup"><span data-stu-id="296f5-128">File name</span></span>  
17. <span data-ttu-id="296f5-129">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="296f5-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="296f5-130">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="296f5-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="296f5-131">Сопоставление новых элементов модели данных с источниками данных</span><span class="sxs-lookup"><span data-stu-id="296f5-131">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="296f5-132">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="296f5-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="296f5-133">Используйте экспресс-фильтр для фильтрации поля "Описание" со значением "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="296f5-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="296f5-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="296f5-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="296f5-135">Мы составим новые элементы модели с соответствующими источниками данных.</span><span class="sxs-lookup"><span data-stu-id="296f5-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="296f5-136">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="296f5-136">Click Designer.</span></span>
4. <span data-ttu-id="296f5-137">В дереве выберите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="296f5-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="296f5-138">В дереве разверните "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="296f5-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="296f5-139">В дереве выберите "Вложения накладной\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="296f5-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="296f5-140">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="296f5-140">Click Edit.</span></span>
8. <span data-ttu-id="296f5-141">В поле "Формула" введите "CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'".</span><span class="sxs-lookup"><span data-stu-id="296f5-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="296f5-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="296f5-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="296f5-143">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="296f5-143">Click Save.</span></span>
10. <span data-ttu-id="296f5-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="296f5-144">Close the page.</span></span>
11. <span data-ttu-id="296f5-145">В дереве выберите "Вложения накладной\Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="296f5-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="296f5-146">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="296f5-146">Click Edit.</span></span>
13. <span data-ttu-id="296f5-147">В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="296f5-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="296f5-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="296f5-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="296f5-149">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="296f5-149">Click Save.</span></span>
15. <span data-ttu-id="296f5-150">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="296f5-150">Close the page.</span></span>
16. <span data-ttu-id="296f5-151">В дереве выберите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="296f5-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="296f5-152">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="296f5-152">Click Edit.</span></span>
18. <span data-ttu-id="296f5-153">В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="296f5-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="296f5-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="296f5-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="296f5-155">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="296f5-155">Click Save.</span></span>
20. <span data-ttu-id="296f5-156">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="296f5-156">Close the page.</span></span>
21. <span data-ttu-id="296f5-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="296f5-157">Click Save.</span></span>
22. <span data-ttu-id="296f5-158">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="296f5-158">Close the page.</span></span>
23. <span data-ttu-id="296f5-159">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="296f5-159">Close the page.</span></span>
24. <span data-ttu-id="296f5-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="296f5-160">Close the page.</span></span>
25. <span data-ttu-id="296f5-161">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="296f5-161">Click Change status.</span></span>
26. <span data-ttu-id="296f5-162">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="296f5-162">Click Complete.</span></span>
27. <span data-ttu-id="296f5-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="296f5-163">Click OK.</span></span>

