--- 
title: "Изменение модели и сопоставления для создания документов с обновлением данных приложения для электронной отчетности (ER)"
description: "Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру \"Электронная отчетность — Формирование документов с обновлением данных приложения (Часть 2. Формирование документов)\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a29e273e5ef377826c0002a9a0a956defef6aa77
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="modify-model-and-mapping-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="f8757-103">Изменение модели и сопоставления для создания документов с обновлением данных приложения для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="f8757-103">Modify model and mapping to generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8757-104">Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Формирование документов с обновлением данных приложения (Часть 2. Формирование документов)".</span><span class="sxs-lookup"><span data-stu-id="f8757-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="f8757-105">В этой процедуре поясняется разработка конфигураций электронной отчетности для формирования электронного документа и обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="f8757-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="f8757-106">В этой процедуре вам предстоит изменить конфигурации электронной отчетности, чтобы начать использовать их для формирования электронных документов и обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="f8757-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="f8757-107">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="f8757-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="f8757-108">Действия можно выполнять с использованием набора данных DEMF.</span><span class="sxs-lookup"><span data-stu-id="f8757-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="f8757-109">Изменение модели данных</span><span class="sxs-lookup"><span data-stu-id="f8757-109">Modify data model</span></span>
1. <span data-ttu-id="f8757-110">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="f8757-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f8757-111">В дереве выберите "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="f8757-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="f8757-112">Вам предстоит расширить способы использования этой модели данных.</span><span class="sxs-lookup"><span data-stu-id="f8757-112">You will extend how you use the data model.</span></span> <span data-ttu-id="f8757-113">Помимо использования ее в качестве источника данных для формирования отчета Интрастат, модель данных будет использоваться для сбора сведений о процессе составления отчетности Интрастат.</span><span class="sxs-lookup"><span data-stu-id="f8757-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="f8757-114">Эти сведения затем будут использоваться для обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="f8757-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="f8757-115">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="f8757-115">Click Designer.</span></span>
4. <span data-ttu-id="f8757-116">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f8757-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="f8757-117">В поле "Новый узел как" введите "Корень модели".</span><span class="sxs-lookup"><span data-stu-id="f8757-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="f8757-118">В поле "Имя" введите "Для обновления данных приложения".</span><span class="sxs-lookup"><span data-stu-id="f8757-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="f8757-119">Для обновления данных приложения</span><span class="sxs-lookup"><span data-stu-id="f8757-119">For application data update</span></span>  
7. <span data-ttu-id="f8757-120">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f8757-120">Click Add.</span></span>
8. <span data-ttu-id="f8757-121">В дереве выберите "Для обновления данных приложения".</span><span class="sxs-lookup"><span data-stu-id="f8757-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="f8757-122">Этот новый корневой элемент добавляется для задания потока данных для перемещения данных из отчета Интрастат (используемого в качестве источника данных) в таблицы приложения (место назначения обновления).</span><span class="sxs-lookup"><span data-stu-id="f8757-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="f8757-123">Обратите внимание, что необходимо использовать разные корневые элементы для получения данных, разнесенных в исходящий документ, и для получения данных из документа, используемых для обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="f8757-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="f8757-124">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f8757-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="f8757-125">В поле "Имя" введите "Заголовок архива".</span><span class="sxs-lookup"><span data-stu-id="f8757-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="f8757-126">Заголовок архива</span><span class="sxs-lookup"><span data-stu-id="f8757-126">Archive header</span></span>  
11. <span data-ttu-id="f8757-127">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="f8757-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="f8757-128">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f8757-128">Click Add.</span></span>
    * <span data-ttu-id="f8757-129">Поскольку вы будете создавать по записи для каждого формируемого отчета Интрастат, необходимо создать для этого новый элемент.</span><span class="sxs-lookup"><span data-stu-id="f8757-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="f8757-130">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f8757-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="f8757-131">В поле "Имя" введите "Имя файла".</span><span class="sxs-lookup"><span data-stu-id="f8757-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="f8757-132">Имя файла</span><span class="sxs-lookup"><span data-stu-id="f8757-132">File name</span></span>  
15. <span data-ttu-id="f8757-133">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="f8757-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="f8757-134">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f8757-134">Click Add.</span></span>
17. <span data-ttu-id="f8757-135">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f8757-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="f8757-136">В поле "Имя" введите "Число строк".</span><span class="sxs-lookup"><span data-stu-id="f8757-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="f8757-137">Число строк</span><span class="sxs-lookup"><span data-stu-id="f8757-137">Number of lines</span></span>  
19. <span data-ttu-id="f8757-138">В поле "Тип элемента" выберите "Целочисленный".</span><span class="sxs-lookup"><span data-stu-id="f8757-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="f8757-139">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f8757-139">Click Add.</span></span>
    * <span data-ttu-id="f8757-140">Добавьте этот элемент, чтобы он представлял число проводок Интрастат, включаемых в отчет в текущем процессе составления отчетности.</span><span class="sxs-lookup"><span data-stu-id="f8757-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="f8757-141">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f8757-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="f8757-142">В поле "Имя" введите "Строки архива".</span><span class="sxs-lookup"><span data-stu-id="f8757-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="f8757-143">Строки архива</span><span class="sxs-lookup"><span data-stu-id="f8757-143">Archive lines</span></span>  
23. <span data-ttu-id="f8757-144">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="f8757-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="f8757-145">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f8757-145">Click Add.</span></span>
    * <span data-ttu-id="f8757-146">Добавьте этот элемент, чтобы он представлял список проводок Интрастат, включаемых в отчет в текущем процессе составления отчетности.</span><span class="sxs-lookup"><span data-stu-id="f8757-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="f8757-147">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f8757-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="f8757-148">В поле "Имя" введите "Сумма".</span><span class="sxs-lookup"><span data-stu-id="f8757-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="f8757-149">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="f8757-149">Amount</span></span>  
27. <span data-ttu-id="f8757-150">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="f8757-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="f8757-151">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f8757-151">Click Add.</span></span>
29. <span data-ttu-id="f8757-152">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f8757-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="f8757-153">В поле "Имя" введите "Код записи товара".</span><span class="sxs-lookup"><span data-stu-id="f8757-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="f8757-154">Код записи товара</span><span class="sxs-lookup"><span data-stu-id="f8757-154">Commodity rec id</span></span>  
31. <span data-ttu-id="f8757-155">В поле "Тип элемента" выберите "Int64".</span><span class="sxs-lookup"><span data-stu-id="f8757-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="f8757-156">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f8757-156">Click Add.</span></span>
33. <span data-ttu-id="f8757-157">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f8757-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="f8757-158">В поле "Имя" введите "Код номенклатуры:".</span><span class="sxs-lookup"><span data-stu-id="f8757-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="f8757-159">Код номенклатуры</span><span class="sxs-lookup"><span data-stu-id="f8757-159">Item number</span></span>  
35. <span data-ttu-id="f8757-160">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="f8757-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="f8757-161">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f8757-161">Click Add.</span></span>
37. <span data-ttu-id="f8757-162">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f8757-162">Click Save.</span></span>
38. <span data-ttu-id="f8757-163">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f8757-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="f8757-164">Изменение сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="f8757-164">Modify model mapping</span></span>
1. <span data-ttu-id="f8757-165">В дереве разверните узел "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="f8757-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="f8757-166">В дереве выберите "Intrastat (model)\Intrastat (mapping)".</span><span class="sxs-lookup"><span data-stu-id="f8757-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="f8757-167">Изменение существующее сопоставление модели, чтобы начать использовать его для обновления данных приложения и для архивирования сведений о составлении отчетности Интрастат.</span><span class="sxs-lookup"><span data-stu-id="f8757-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="f8757-168">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="f8757-168">Click Designer.</span></span>
4. <span data-ttu-id="f8757-169">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f8757-169">Click New.</span></span>
5. <span data-ttu-id="f8757-170">В поле "Имя" введите "Обновить архив".</span><span class="sxs-lookup"><span data-stu-id="f8757-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="f8757-171">Обновить архив</span><span class="sxs-lookup"><span data-stu-id="f8757-171">Update archive</span></span>  
6. <span data-ttu-id="f8757-172">В поле "Направление" выберите "В место назначения".</span><span class="sxs-lookup"><span data-stu-id="f8757-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="f8757-173">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f8757-173">Click Save.</span></span>
    * <span data-ttu-id="f8757-174">Это новое сопоставление задает поток данных для перемещения данных (сведений о составлении отчетности Интрастат) из модели данных в таблицы приложения (место назначения обновления).</span><span class="sxs-lookup"><span data-stu-id="f8757-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="f8757-175">Обратите внимание, что для получения данных из приложения для процесса составления отчетности и для использования данных из модели данных для обновления данных приложения необходимо использовать разные корневые элементы модели.</span><span class="sxs-lookup"><span data-stu-id="f8757-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="f8757-176">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="f8757-176">Click Designer.</span></span>
9. <span data-ttu-id="f8757-177">В дереве выберите "Модель данных\Модель данных".</span><span class="sxs-lookup"><span data-stu-id="f8757-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="f8757-178">Добавьте требуемый источник данных.</span><span class="sxs-lookup"><span data-stu-id="f8757-178">Add the required data source.</span></span> <span data-ttu-id="f8757-179">Это модель данных, которая содержит сведения о включенных в отчет проводках Интрастат, которые необходимо архивировать.</span><span class="sxs-lookup"><span data-stu-id="f8757-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="f8757-180">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="f8757-180">Click Add root.</span></span>
11. <span data-ttu-id="f8757-181">В поле "Имя" введите "модель".</span><span class="sxs-lookup"><span data-stu-id="f8757-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="f8757-182">модель</span><span class="sxs-lookup"><span data-stu-id="f8757-182">model</span></span>  
12. <span data-ttu-id="f8757-183">В поле "Определение" введите или выберите значение "Для обновления данных приложения".</span><span class="sxs-lookup"><span data-stu-id="f8757-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="f8757-184">Для обновления данных приложения</span><span class="sxs-lookup"><span data-stu-id="f8757-184">For application data update</span></span>  
13. <span data-ttu-id="f8757-185">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f8757-185">Click OK.</span></span>
14. <span data-ttu-id="f8757-186">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="f8757-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="f8757-187">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="f8757-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="f8757-188">В дереве выберите "модель\Заголовок архива".</span><span class="sxs-lookup"><span data-stu-id="f8757-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="f8757-189">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f8757-189">Click Add.</span></span>
    * <span data-ttu-id="f8757-190">Поскольку для архивирования необходимо перечислить включенные в отчет проводки Интрастат, необходимо добавить соответствующий источник данных.</span><span class="sxs-lookup"><span data-stu-id="f8757-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="f8757-191">В поле "Имя" введите "Перечисленные строки".</span><span class="sxs-lookup"><span data-stu-id="f8757-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="f8757-192">Перечисленные строки</span><span class="sxs-lookup"><span data-stu-id="f8757-192">Enumerated lines</span></span>  
19. <span data-ttu-id="f8757-193">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="f8757-193">Click Edit formula.</span></span>
20. <span data-ttu-id="f8757-194">В дереве выберите "Список\ENUMERATE".</span><span class="sxs-lookup"><span data-stu-id="f8757-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="f8757-195">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="f8757-195">Click Add function.</span></span>
22. <span data-ttu-id="f8757-196">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="f8757-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="f8757-197">В дереве разверните "модель\Заголовок архива".</span><span class="sxs-lookup"><span data-stu-id="f8757-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="f8757-198">В дереве выберите "модель\Заголовок архива\Строки архива".</span><span class="sxs-lookup"><span data-stu-id="f8757-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="f8757-199">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="f8757-199">Click Add data source.</span></span>
26. <span data-ttu-id="f8757-200">В поле "Формула" введите "ENUMERATE(модель.'Заголовок архива'.'Строки архива')".</span><span class="sxs-lookup"><span data-stu-id="f8757-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="f8757-201">ENUMERATE(модель.'Заголовок архива'.'Строки архива')</span><span class="sxs-lookup"><span data-stu-id="f8757-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="f8757-202">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f8757-202">Click Save.</span></span>
28. <span data-ttu-id="f8757-203">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f8757-203">Close the page.</span></span>
29. <span data-ttu-id="f8757-204">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f8757-204">Click OK.</span></span>
30. <span data-ttu-id="f8757-205">Щелкните "Добавить место назначения".</span><span class="sxs-lookup"><span data-stu-id="f8757-205">Click Add destination.</span></span>
    * <span data-ttu-id="f8757-206">Добавьте таблицы приложения в качестве необходимых мест назначения, требующих обновления сведений об архивации проводок Интрастат, включенных в отчет.</span><span class="sxs-lookup"><span data-stu-id="f8757-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="f8757-207">В поле "Имя" введите "Архив".</span><span class="sxs-lookup"><span data-stu-id="f8757-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="f8757-208">Архивировать</span><span class="sxs-lookup"><span data-stu-id="f8757-208">Archive</span></span>  
32. <span data-ttu-id="f8757-209">В поле "Имя таблицы" введите "IntrastatArchiveGeneral".</span><span class="sxs-lookup"><span data-stu-id="f8757-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="f8757-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="f8757-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="f8757-211">Оставьте действие с записью «Вставка», чтобы вы могли добавлять записи во время архивирования сведений о каждом процессе подготовки отчетности Интрастат.</span><span class="sxs-lookup"><span data-stu-id="f8757-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="f8757-212">Выберите "Да" в поле "Записывать в infolog".</span><span class="sxs-lookup"><span data-stu-id="f8757-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="f8757-213">Выберите "Да", чтобы получать информацию о проблемах, возникающих при обновлении данных приложения.</span><span class="sxs-lookup"><span data-stu-id="f8757-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="f8757-214">Выберите "Да" в поле "Пропустить проверку действия с записью".</span><span class="sxs-lookup"><span data-stu-id="f8757-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="f8757-215">Выберите "Да", чтобы подавить ошибки проверки, связанные с пустым полем "Код архива Интрастат".</span><span class="sxs-lookup"><span data-stu-id="f8757-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="f8757-216">Это будет делаться после добавления записей на основании параметров порядкового номера, настроенных для этой таблицы в форме "Параметры внешней торговли".</span><span class="sxs-lookup"><span data-stu-id="f8757-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="f8757-217">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f8757-217">Click OK.</span></span>
    * <span data-ttu-id="f8757-218">Привяжите элементы добавленного источника данных (отфильтрованной модели на основе выбранного корневого элемента) к элементам из добавленного места назначения.</span><span class="sxs-lookup"><span data-stu-id="f8757-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="f8757-219">В дереве разверните "Архив".</span><span class="sxs-lookup"><span data-stu-id="f8757-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="f8757-220">В дереве разверните "Архив\<Связи".</span><span class="sxs-lookup"><span data-stu-id="f8757-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="f8757-221">В дереве разверните "Архив\<Связи\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="f8757-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="f8757-222">В дереве выберите "Архив\<Связи\IntrastatArchiveDetail\Сумма(AmountMST)".</span><span class="sxs-lookup"><span data-stu-id="f8757-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="f8757-223">В дереве разверните "модель\Заголовок архива\Перечисленные строки".</span><span class="sxs-lookup"><span data-stu-id="f8757-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="f8757-224">В дереве разверните "модель\Заголовок архива\Перечисленные строки\Значение".</span><span class="sxs-lookup"><span data-stu-id="f8757-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="f8757-225">В дереве выберите "модель\Заголовок архива\Перечисленные строки\Значение\Сумма".</span><span class="sxs-lookup"><span data-stu-id="f8757-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="f8757-226">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f8757-226">Click Bind.</span></span>
44. <span data-ttu-id="f8757-227">В дереве выберите "Архив\<Связи\IntrastatArchiveDetail\Товар(IntrastatCommodity)".</span><span class="sxs-lookup"><span data-stu-id="f8757-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="f8757-228">В дереве выберите "модель\Заголовок архива\Перечисленные строки\Значение\Код записи товара".</span><span class="sxs-lookup"><span data-stu-id="f8757-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="f8757-229">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f8757-229">Click Bind.</span></span>
47. <span data-ttu-id="f8757-230">В дереве выберите "Архив\<Связи\IntrastatArchiveDetail\Код номенклатуры(ItemId)".</span><span class="sxs-lookup"><span data-stu-id="f8757-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="f8757-231">В дереве выберите "модель\Заголовок архива\Перечисленные строки\Значение\Код номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="f8757-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="f8757-232">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f8757-232">Click Bind.</span></span>
50. <span data-ttu-id="f8757-233">В дереве выберите "Архив\<Связи\IntrastatArchiveDetail\Номер строки(LineNumber)".</span><span class="sxs-lookup"><span data-stu-id="f8757-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="f8757-234">В дереве выберите "модель\Заголовок архива\Перечисленные строки\Номер".</span><span class="sxs-lookup"><span data-stu-id="f8757-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="f8757-235">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f8757-235">Click Bind.</span></span>
53. <span data-ttu-id="f8757-236">В дереве выберите "Архив\<Связи\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="f8757-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="f8757-237">В дереве выберите "модель\Заголовок архива\Перечисленные строки".</span><span class="sxs-lookup"><span data-stu-id="f8757-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="f8757-238">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f8757-238">Click Bind.</span></span>
56. <span data-ttu-id="f8757-239">В дереве выберите "Архив\Имя файла(FileName)".</span><span class="sxs-lookup"><span data-stu-id="f8757-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="f8757-240">В дереве выберите "модель\Заголовок архива\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="f8757-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="f8757-241">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f8757-241">Click Bind.</span></span>
59. <span data-ttu-id="f8757-242">В дереве выберите "Архив\Число строк(NumberOfLines)".</span><span class="sxs-lookup"><span data-stu-id="f8757-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="f8757-243">В дереве выберите "модель\Заголовок архива\Число строк".</span><span class="sxs-lookup"><span data-stu-id="f8757-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="f8757-244">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f8757-244">Click Bind.</span></span>
62. <span data-ttu-id="f8757-245">В дереве выберите "Архив".</span><span class="sxs-lookup"><span data-stu-id="f8757-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="f8757-246">В дереве выберите "модель\Заголовок архива".</span><span class="sxs-lookup"><span data-stu-id="f8757-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="f8757-247">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="f8757-247">Click Bind.</span></span>
65. <span data-ttu-id="f8757-248">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f8757-248">Click Save.</span></span>
66. <span data-ttu-id="f8757-249">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f8757-249">Close the page.</span></span>
67. <span data-ttu-id="f8757-250">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f8757-250">Close the page.</span></span>

