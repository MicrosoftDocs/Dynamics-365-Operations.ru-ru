---
title: Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)
description: В этой теме описывается, как настроить формат электронной отчетности (ER), чтобы в выходных данных электронной отчетности использовать файлы управления документами (вложения). (Часть 2)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd06cdfd9bae57577c2e3ec97848e319b197f41
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092599"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="64f6d-104">Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)</span><span class="sxs-lookup"><span data-stu-id="64f6d-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64f6d-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="64f6d-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="64f6d-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="64f6d-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="64f6d-107">Для выполнения этих действий необходимо сначала выполнить шаги в руководстве по задаче "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 1. Подготовка модели данных)".</span><span class="sxs-lookup"><span data-stu-id="64f6d-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="64f6d-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="64f6d-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="64f6d-109">Расширение модели данных, чтобы представлять в ней файлы управления документами</span><span class="sxs-lookup"><span data-stu-id="64f6d-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="64f6d-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="64f6d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="64f6d-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="64f6d-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="64f6d-112">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="64f6d-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="64f6d-113">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="64f6d-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="64f6d-114">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="64f6d-114">Click Designer.</span></span>
6. <span data-ttu-id="64f6d-115">В дереве выберите "Накладная клиента(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="64f6d-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="64f6d-116">Мы расширим эту модель данных, чтобы представлять в ней любые файлы, которые были приложены к заказу на продажу, который относится к электронной обработке накладной.</span><span class="sxs-lookup"><span data-stu-id="64f6d-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="64f6d-117">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="64f6d-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="64f6d-118">В поле "Имя" введите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="64f6d-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="64f6d-119">Вложения накладной</span><span class="sxs-lookup"><span data-stu-id="64f6d-119">Invoice attachments</span></span>  
9. <span data-ttu-id="64f6d-120">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="64f6d-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="64f6d-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="64f6d-121">Click Add.</span></span>
11. <span data-ttu-id="64f6d-122">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="64f6d-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="64f6d-123">В поле "Имя" введите "Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="64f6d-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="64f6d-124">Содержание файла</span><span class="sxs-lookup"><span data-stu-id="64f6d-124">File content</span></span>  
13. <span data-ttu-id="64f6d-125">В поле "Тип элемента" выберите "Контейнер".</span><span class="sxs-lookup"><span data-stu-id="64f6d-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="64f6d-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="64f6d-126">Click Add.</span></span>
15. <span data-ttu-id="64f6d-127">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="64f6d-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="64f6d-128">В поле "Имя" введите "Имя файла".</span><span class="sxs-lookup"><span data-stu-id="64f6d-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="64f6d-129">Имя файла</span><span class="sxs-lookup"><span data-stu-id="64f6d-129">File name</span></span>  
17. <span data-ttu-id="64f6d-130">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="64f6d-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="64f6d-131">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="64f6d-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="64f6d-132">Сопоставление новых элементов модели данных с источниками данных</span><span class="sxs-lookup"><span data-stu-id="64f6d-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="64f6d-133">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="64f6d-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="64f6d-134">Используйте экспресс-фильтр для фильтрации поля "Описание" со значением "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="64f6d-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="64f6d-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="64f6d-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="64f6d-136">Мы составим новые элементы модели с соответствующими источниками данных.</span><span class="sxs-lookup"><span data-stu-id="64f6d-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="64f6d-137">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="64f6d-137">Click Designer.</span></span>
4. <span data-ttu-id="64f6d-138">В дереве выберите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="64f6d-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="64f6d-139">В дереве разверните "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="64f6d-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="64f6d-140">В дереве выберите "Вложения накладной\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="64f6d-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="64f6d-141">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="64f6d-141">Click Edit.</span></span>
8. <span data-ttu-id="64f6d-142">В поле "Формула" введите "CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'".</span><span class="sxs-lookup"><span data-stu-id="64f6d-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="64f6d-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="64f6d-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="64f6d-144">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="64f6d-144">Click Save.</span></span>
10. <span data-ttu-id="64f6d-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64f6d-145">Close the page.</span></span>
11. <span data-ttu-id="64f6d-146">В дереве выберите "Вложения накладной\Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="64f6d-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="64f6d-147">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="64f6d-147">Click Edit.</span></span>
13. <span data-ttu-id="64f6d-148">В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="64f6d-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="64f6d-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="64f6d-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="64f6d-150">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="64f6d-150">Click Save.</span></span>
15. <span data-ttu-id="64f6d-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64f6d-151">Close the page.</span></span>
16. <span data-ttu-id="64f6d-152">В дереве выберите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="64f6d-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="64f6d-153">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="64f6d-153">Click Edit.</span></span>
18. <span data-ttu-id="64f6d-154">В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="64f6d-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="64f6d-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="64f6d-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="64f6d-156">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="64f6d-156">Click Save.</span></span>
20. <span data-ttu-id="64f6d-157">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64f6d-157">Close the page.</span></span>
21. <span data-ttu-id="64f6d-158">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="64f6d-158">Click Save.</span></span>
22. <span data-ttu-id="64f6d-159">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64f6d-159">Close the page.</span></span>
23. <span data-ttu-id="64f6d-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64f6d-160">Close the page.</span></span>
24. <span data-ttu-id="64f6d-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64f6d-161">Close the page.</span></span>
25. <span data-ttu-id="64f6d-162">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="64f6d-162">Click Change status.</span></span>
26. <span data-ttu-id="64f6d-163">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="64f6d-163">Click Complete.</span></span>
27. <span data-ttu-id="64f6d-164">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="64f6d-164">Click OK.</span></span>

