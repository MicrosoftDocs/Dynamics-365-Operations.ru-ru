---
title: Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)
description: В этой теме описывается, как настроить формат электронной отчетности (ER), чтобы в выходных данных электронной отчетности использовать файлы управления документами (вложения). (Часть 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e79dd0a6c68aa6ba7b857c31c9159c68543d93b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754922"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="97500-104">Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)</span><span class="sxs-lookup"><span data-stu-id="97500-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97500-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="97500-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="97500-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="97500-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="97500-107">Для выполнения этих действий необходимо сначала выполнить шаги в руководстве по задаче "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 1. Подготовка модели данных)".</span><span class="sxs-lookup"><span data-stu-id="97500-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="97500-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="97500-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="97500-109">Расширение модели данных, чтобы представлять в ней файлы управления документами</span><span class="sxs-lookup"><span data-stu-id="97500-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="97500-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="97500-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="97500-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="97500-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="97500-112">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="97500-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="97500-113">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="97500-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="97500-114">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="97500-114">Click Designer.</span></span>
6. <span data-ttu-id="97500-115">В дереве выберите "Накладная клиента(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="97500-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="97500-116">Мы расширим эту модель данных, чтобы представлять в ней любые файлы, которые были приложены к заказу на продажу, который относится к электронной обработке накладной.</span><span class="sxs-lookup"><span data-stu-id="97500-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="97500-117">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="97500-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="97500-118">В поле "Имя" введите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="97500-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="97500-119">Вложения накладной</span><span class="sxs-lookup"><span data-stu-id="97500-119">Invoice attachments</span></span>  
9. <span data-ttu-id="97500-120">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="97500-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="97500-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="97500-121">Click Add.</span></span>
11. <span data-ttu-id="97500-122">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="97500-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="97500-123">В поле "Имя" введите "Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="97500-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="97500-124">Содержание файла</span><span class="sxs-lookup"><span data-stu-id="97500-124">File content</span></span>  
13. <span data-ttu-id="97500-125">В поле "Тип элемента" выберите "Контейнер".</span><span class="sxs-lookup"><span data-stu-id="97500-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="97500-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="97500-126">Click Add.</span></span>
15. <span data-ttu-id="97500-127">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="97500-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="97500-128">В поле "Имя" введите "Имя файла".</span><span class="sxs-lookup"><span data-stu-id="97500-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="97500-129">Имя файла</span><span class="sxs-lookup"><span data-stu-id="97500-129">File name</span></span>  
17. <span data-ttu-id="97500-130">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="97500-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="97500-131">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="97500-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="97500-132">Сопоставление новых элементов модели данных с источниками данных</span><span class="sxs-lookup"><span data-stu-id="97500-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="97500-133">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="97500-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="97500-134">Используйте экспресс-фильтр для фильтрации поля "Описание" со значением "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="97500-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="97500-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="97500-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="97500-136">Мы составим новые элементы модели с соответствующими источниками данных.</span><span class="sxs-lookup"><span data-stu-id="97500-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="97500-137">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="97500-137">Click Designer.</span></span>
4. <span data-ttu-id="97500-138">В дереве выберите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="97500-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="97500-139">В дереве разверните "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="97500-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="97500-140">В дереве выберите "Вложения накладной\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="97500-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="97500-141">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="97500-141">Click Edit.</span></span>
8. <span data-ttu-id="97500-142">В поле "Формула" введите "CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'".</span><span class="sxs-lookup"><span data-stu-id="97500-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="97500-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="97500-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="97500-144">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="97500-144">Click Save.</span></span>
10. <span data-ttu-id="97500-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="97500-145">Close the page.</span></span>
11. <span data-ttu-id="97500-146">В дереве выберите "Вложения накладной\Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="97500-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="97500-147">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="97500-147">Click Edit.</span></span>
13. <span data-ttu-id="97500-148">В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="97500-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="97500-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="97500-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="97500-150">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="97500-150">Click Save.</span></span>
15. <span data-ttu-id="97500-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="97500-151">Close the page.</span></span>
16. <span data-ttu-id="97500-152">В дереве выберите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="97500-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="97500-153">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="97500-153">Click Edit.</span></span>
18. <span data-ttu-id="97500-154">В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="97500-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="97500-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="97500-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="97500-156">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="97500-156">Click Save.</span></span>
20. <span data-ttu-id="97500-157">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="97500-157">Close the page.</span></span>
21. <span data-ttu-id="97500-158">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="97500-158">Click Save.</span></span>
22. <span data-ttu-id="97500-159">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="97500-159">Close the page.</span></span>
23. <span data-ttu-id="97500-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="97500-160">Close the page.</span></span>
24. <span data-ttu-id="97500-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="97500-161">Close the page.</span></span>
25. <span data-ttu-id="97500-162">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="97500-162">Click Change status.</span></span>
26. <span data-ttu-id="97500-163">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="97500-163">Click Complete.</span></span>
27. <span data-ttu-id="97500-164">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="97500-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]