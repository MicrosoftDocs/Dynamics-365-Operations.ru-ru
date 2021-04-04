---
title: Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)
description: В этой теме описывается, как настроить формат электронной отчетности (ER), чтобы в выходных данных электронной отчетности использовать файлы управления документами (вложения). (Часть 2)
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: b47c35790ce04a494b6c58f6e04fa9b829d2ab93
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559781"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="57d88-104">Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 2. Расширение модели данных)</span><span class="sxs-lookup"><span data-stu-id="57d88-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57d88-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="57d88-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="57d88-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="57d88-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="57d88-107">Для выполнения этих действий необходимо сначала выполнить шаги в руководстве по задаче "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 1. Подготовка модели данных)".</span><span class="sxs-lookup"><span data-stu-id="57d88-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="57d88-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="57d88-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="57d88-109">Расширение модели данных, чтобы представлять в ней файлы управления документами</span><span class="sxs-lookup"><span data-stu-id="57d88-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="57d88-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="57d88-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="57d88-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="57d88-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="57d88-112">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="57d88-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="57d88-113">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="57d88-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="57d88-114">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="57d88-114">Click Designer.</span></span>
6. <span data-ttu-id="57d88-115">В дереве выберите "Накладная клиента(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="57d88-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="57d88-116">Мы расширим эту модель данных, чтобы представлять в ней любые файлы, которые были приложены к заказу на продажу, который относится к электронной обработке накладной.</span><span class="sxs-lookup"><span data-stu-id="57d88-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="57d88-117">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="57d88-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="57d88-118">В поле "Имя" введите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="57d88-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="57d88-119">Вложения накладной</span><span class="sxs-lookup"><span data-stu-id="57d88-119">Invoice attachments</span></span>  
9. <span data-ttu-id="57d88-120">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="57d88-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="57d88-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="57d88-121">Click Add.</span></span>
11. <span data-ttu-id="57d88-122">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="57d88-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="57d88-123">В поле "Имя" введите "Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="57d88-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="57d88-124">Содержание файла</span><span class="sxs-lookup"><span data-stu-id="57d88-124">File content</span></span>  
13. <span data-ttu-id="57d88-125">В поле "Тип элемента" выберите "Контейнер".</span><span class="sxs-lookup"><span data-stu-id="57d88-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="57d88-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="57d88-126">Click Add.</span></span>
15. <span data-ttu-id="57d88-127">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="57d88-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="57d88-128">В поле "Имя" введите "Имя файла".</span><span class="sxs-lookup"><span data-stu-id="57d88-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="57d88-129">Имя файла</span><span class="sxs-lookup"><span data-stu-id="57d88-129">File name</span></span>  
17. <span data-ttu-id="57d88-130">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="57d88-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="57d88-131">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="57d88-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="57d88-132">Сопоставление новых элементов модели данных с источниками данных</span><span class="sxs-lookup"><span data-stu-id="57d88-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="57d88-133">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="57d88-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="57d88-134">Используйте экспресс-фильтр для фильтрации поля "Описание" со значением "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="57d88-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="57d88-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="57d88-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="57d88-136">Мы составим новые элементы модели с соответствующими источниками данных.</span><span class="sxs-lookup"><span data-stu-id="57d88-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="57d88-137">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="57d88-137">Click Designer.</span></span>
4. <span data-ttu-id="57d88-138">В дереве выберите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="57d88-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="57d88-139">В дереве разверните "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="57d88-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="57d88-140">В дереве выберите "Вложения накладной\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="57d88-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="57d88-141">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="57d88-141">Click Edit.</span></span>
8. <span data-ttu-id="57d88-142">В поле "Формула" введите "CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'".</span><span class="sxs-lookup"><span data-stu-id="57d88-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="57d88-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="57d88-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="57d88-144">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="57d88-144">Click Save.</span></span>
10. <span data-ttu-id="57d88-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57d88-145">Close the page.</span></span>
11. <span data-ttu-id="57d88-146">В дереве выберите "Вложения накладной\Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="57d88-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="57d88-147">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="57d88-147">Click Edit.</span></span>
13. <span data-ttu-id="57d88-148">В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="57d88-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="57d88-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="57d88-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="57d88-150">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="57d88-150">Click Save.</span></span>
15. <span data-ttu-id="57d88-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57d88-151">Close the page.</span></span>
16. <span data-ttu-id="57d88-152">В дереве выберите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="57d88-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="57d88-153">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="57d88-153">Click Edit.</span></span>
18. <span data-ttu-id="57d88-154">В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="57d88-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="57d88-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="57d88-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="57d88-156">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="57d88-156">Click Save.</span></span>
20. <span data-ttu-id="57d88-157">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57d88-157">Close the page.</span></span>
21. <span data-ttu-id="57d88-158">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="57d88-158">Click Save.</span></span>
22. <span data-ttu-id="57d88-159">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57d88-159">Close the page.</span></span>
23. <span data-ttu-id="57d88-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57d88-160">Close the page.</span></span>
24. <span data-ttu-id="57d88-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57d88-161">Close the page.</span></span>
25. <span data-ttu-id="57d88-162">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="57d88-162">Click Change status.</span></span>
26. <span data-ttu-id="57d88-163">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="57d88-163">Click Complete.</span></span>
27. <span data-ttu-id="57d88-164">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="57d88-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]