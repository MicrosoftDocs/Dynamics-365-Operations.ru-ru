--- 
title: "Расширение модели данных для использования файлов управления документами в выходных форматах для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ebbd442c9f69290dc995c05462ca70b554f7d9f2
ms.contentlocale: ru-ru
ms.lasthandoff: 03/26/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="08093-103">Расширение модели данных для использования файлов управления документами в выходных форматах для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="08093-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08093-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="08093-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="08093-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="08093-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="08093-106">Для выполнения этих действий необходимо сначала выполнить шаги в руководстве по задаче "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 1. Подготовка модели данных)".</span><span class="sxs-lookup"><span data-stu-id="08093-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="08093-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="08093-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="08093-108">Расширение модели данных, чтобы представлять в ней файлы управления документами</span><span class="sxs-lookup"><span data-stu-id="08093-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="08093-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="08093-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="08093-110">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="08093-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="08093-111">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="08093-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="08093-112">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="08093-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="08093-113">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="08093-113">Click Designer.</span></span>
6. <span data-ttu-id="08093-114">В дереве выберите "Накладная клиента(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="08093-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="08093-115">Мы расширим эту модель данных, чтобы представлять в ней любые файлы, которые были приложены к заказу на продажу, который относится к электронной обработке накладной.</span><span class="sxs-lookup"><span data-stu-id="08093-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="08093-116">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="08093-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="08093-117">В поле "Имя" введите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="08093-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="08093-118">Вложения накладной</span><span class="sxs-lookup"><span data-stu-id="08093-118">Invoice attachments</span></span>  
9. <span data-ttu-id="08093-119">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="08093-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="08093-120">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="08093-120">Click Add.</span></span>
11. <span data-ttu-id="08093-121">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="08093-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="08093-122">В поле "Имя" введите "Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="08093-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="08093-123">Содержание файла</span><span class="sxs-lookup"><span data-stu-id="08093-123">File content</span></span>  
13. <span data-ttu-id="08093-124">В поле "Тип элемента" выберите "Контейнер".</span><span class="sxs-lookup"><span data-stu-id="08093-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="08093-125">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="08093-125">Click Add.</span></span>
15. <span data-ttu-id="08093-126">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="08093-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="08093-127">В поле "Имя" введите "Имя файла".</span><span class="sxs-lookup"><span data-stu-id="08093-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="08093-128">Имя файла</span><span class="sxs-lookup"><span data-stu-id="08093-128">File name</span></span>  
17. <span data-ttu-id="08093-129">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="08093-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="08093-130">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="08093-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="08093-131">Сопоставление новых элементов модели данных с источниками данных Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="08093-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="08093-132">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="08093-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="08093-133">Используйте экспресс-фильтр для фильтрации поля "Описание" со значением "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="08093-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="08093-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="08093-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="08093-135">Мы составим новые элементы модели с соответствующими источниками данных.</span><span class="sxs-lookup"><span data-stu-id="08093-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="08093-136">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="08093-136">Click Designer.</span></span>
4. <span data-ttu-id="08093-137">В дереве выберите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="08093-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="08093-138">В дереве разверните "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="08093-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="08093-139">В дереве выберите "Вложения накладной\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="08093-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="08093-140">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="08093-140">Click Edit.</span></span>
8. <span data-ttu-id="08093-141">В поле "Формула" введите "CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'".</span><span class="sxs-lookup"><span data-stu-id="08093-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="08093-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="08093-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="08093-143">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="08093-143">Click Save.</span></span>
10. <span data-ttu-id="08093-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="08093-144">Close the page.</span></span>
11. <span data-ttu-id="08093-145">В дереве выберите "Вложения накладной\Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="08093-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="08093-146">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="08093-146">Click Edit.</span></span>
13. <span data-ttu-id="08093-147">В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="08093-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="08093-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="08093-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="08093-149">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="08093-149">Click Save.</span></span>
15. <span data-ttu-id="08093-150">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="08093-150">Close the page.</span></span>
16. <span data-ttu-id="08093-151">В дереве выберите "Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="08093-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="08093-152">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="08093-152">Click Edit.</span></span>
18. <span data-ttu-id="08093-153">В поле "Формула" введите 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="08093-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="08093-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="08093-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="08093-155">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="08093-155">Click Save.</span></span>
20. <span data-ttu-id="08093-156">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="08093-156">Close the page.</span></span>
21. <span data-ttu-id="08093-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="08093-157">Click Save.</span></span>
22. <span data-ttu-id="08093-158">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="08093-158">Close the page.</span></span>
23. <span data-ttu-id="08093-159">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="08093-159">Close the page.</span></span>
24. <span data-ttu-id="08093-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="08093-160">Close the page.</span></span>
25. <span data-ttu-id="08093-161">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="08093-161">Click Change status.</span></span>
26. <span data-ttu-id="08093-162">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="08093-162">Click Complete.</span></span>
27. <span data-ttu-id="08093-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="08093-163">Click OK.</span></span>


