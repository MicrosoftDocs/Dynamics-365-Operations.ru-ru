---
title: Изменение моделей и сопоставлений для формирования документов, содержащих данные приложений
description: В этой теме описано, как разработать конфигурации электронной отчетности для создания электронного документа и обновления данных приложений. (Часть 2 — Создание документов).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 025429c8e6775d20634703853df04d63c0651b98
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092905"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="e5488-104">Изменение моделей и сопоставлений для формирования документов, содержащих данные приложений</span><span class="sxs-lookup"><span data-stu-id="e5488-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5488-105">Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Формирование документов с обновлением данных приложения (Часть 2. Формирование документов)".</span><span class="sxs-lookup"><span data-stu-id="e5488-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="e5488-106">В этой процедуре поясняется разработка конфигураций электронной отчетности для формирования электронного документа и обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="e5488-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="e5488-107">В этой процедуре вам предстоит изменить конфигурации электронной отчетности, чтобы начать использовать их для формирования электронных документов и обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="e5488-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="e5488-108">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="e5488-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="e5488-109">Действия можно выполнять с использованием набора данных DEMF.</span><span class="sxs-lookup"><span data-stu-id="e5488-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="e5488-110">Изменение модели данных</span><span class="sxs-lookup"><span data-stu-id="e5488-110">Modify data model</span></span>
1. <span data-ttu-id="e5488-111">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="e5488-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e5488-112">В дереве выберите "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="e5488-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="e5488-113">Вам предстоит расширить способы использования этой модели данных.</span><span class="sxs-lookup"><span data-stu-id="e5488-113">You will extend how you use the data model.</span></span> <span data-ttu-id="e5488-114">Помимо использования ее в качестве источника данных для формирования отчета Интрастат, модель данных будет использоваться для сбора сведений о процессе составления отчетности Интрастат.</span><span class="sxs-lookup"><span data-stu-id="e5488-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="e5488-115">Эти сведения затем будут использоваться для обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="e5488-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="e5488-116">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="e5488-116">Click Designer.</span></span>
4. <span data-ttu-id="e5488-117">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e5488-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="e5488-118">В поле "Новый узел как" введите "Корень модели".</span><span class="sxs-lookup"><span data-stu-id="e5488-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="e5488-119">В поле "Имя" введите "Для обновления данных приложения".</span><span class="sxs-lookup"><span data-stu-id="e5488-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="e5488-120">Для обновления данных приложения</span><span class="sxs-lookup"><span data-stu-id="e5488-120">For application data update</span></span>  
7. <span data-ttu-id="e5488-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5488-121">Click Add.</span></span>
8. <span data-ttu-id="e5488-122">В дереве выберите "Для обновления данных приложения".</span><span class="sxs-lookup"><span data-stu-id="e5488-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="e5488-123">Этот новый корневой элемент добавляется для задания потока данных для перемещения данных из отчета Интрастат (используемого в качестве источника данных) в таблицы приложения (место назначения обновления).</span><span class="sxs-lookup"><span data-stu-id="e5488-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="e5488-124">Обратите внимание, что необходимо использовать разные корневые элементы для получения данных, разнесенных в исходящий документ, и для получения данных из документа, используемых для обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="e5488-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="e5488-125">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e5488-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="e5488-126">В поле "Имя" введите "Заголовок архива".</span><span class="sxs-lookup"><span data-stu-id="e5488-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="e5488-127">Заголовок архива</span><span class="sxs-lookup"><span data-stu-id="e5488-127">Archive header</span></span>  
11. <span data-ttu-id="e5488-128">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="e5488-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="e5488-129">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5488-129">Click Add.</span></span>
    * <span data-ttu-id="e5488-130">Поскольку вы будете создавать по записи для каждого формируемого отчета Интрастат, необходимо создать для этого новый элемент.</span><span class="sxs-lookup"><span data-stu-id="e5488-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="e5488-131">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e5488-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="e5488-132">В поле "Имя" введите "Имя файла".</span><span class="sxs-lookup"><span data-stu-id="e5488-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="e5488-133">Имя файла</span><span class="sxs-lookup"><span data-stu-id="e5488-133">File name</span></span>  
15. <span data-ttu-id="e5488-134">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="e5488-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="e5488-135">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5488-135">Click Add.</span></span>
17. <span data-ttu-id="e5488-136">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e5488-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="e5488-137">В поле "Имя" введите "Число строк".</span><span class="sxs-lookup"><span data-stu-id="e5488-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="e5488-138">Число строк</span><span class="sxs-lookup"><span data-stu-id="e5488-138">Number of lines</span></span>  
19. <span data-ttu-id="e5488-139">В поле "Тип элемента" выберите "Целочисленный".</span><span class="sxs-lookup"><span data-stu-id="e5488-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="e5488-140">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5488-140">Click Add.</span></span>
    * <span data-ttu-id="e5488-141">Добавьте этот элемент, чтобы он представлял число проводок Интрастат, включаемых в отчет в текущем процессе составления отчетности.</span><span class="sxs-lookup"><span data-stu-id="e5488-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="e5488-142">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e5488-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="e5488-143">В поле "Имя" введите "Строки архива".</span><span class="sxs-lookup"><span data-stu-id="e5488-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="e5488-144">Строки архива</span><span class="sxs-lookup"><span data-stu-id="e5488-144">Archive lines</span></span>  
23. <span data-ttu-id="e5488-145">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="e5488-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="e5488-146">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5488-146">Click Add.</span></span>
    * <span data-ttu-id="e5488-147">Добавьте этот элемент, чтобы он представлял список проводок Интрастат, включаемых в отчет в текущем процессе составления отчетности.</span><span class="sxs-lookup"><span data-stu-id="e5488-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="e5488-148">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e5488-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="e5488-149">В поле "Имя" введите "Сумма".</span><span class="sxs-lookup"><span data-stu-id="e5488-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="e5488-150">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="e5488-150">Amount</span></span>  
27. <span data-ttu-id="e5488-151">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="e5488-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="e5488-152">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5488-152">Click Add.</span></span>
29. <span data-ttu-id="e5488-153">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e5488-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="e5488-154">В поле "Имя" введите "Код записи товара".</span><span class="sxs-lookup"><span data-stu-id="e5488-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="e5488-155">Код записи товара</span><span class="sxs-lookup"><span data-stu-id="e5488-155">Commodity rec id</span></span>  
31. <span data-ttu-id="e5488-156">В поле "Тип элемента" выберите "Int64".</span><span class="sxs-lookup"><span data-stu-id="e5488-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="e5488-157">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5488-157">Click Add.</span></span>
33. <span data-ttu-id="e5488-158">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e5488-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="e5488-159">В поле "Имя" введите "Код номенклатуры:".</span><span class="sxs-lookup"><span data-stu-id="e5488-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="e5488-160">Код номенклатуры</span><span class="sxs-lookup"><span data-stu-id="e5488-160">Item number</span></span>  
35. <span data-ttu-id="e5488-161">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="e5488-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="e5488-162">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5488-162">Click Add.</span></span>
37. <span data-ttu-id="e5488-163">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e5488-163">Click Save.</span></span>
38. <span data-ttu-id="e5488-164">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e5488-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="e5488-165">Изменение сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="e5488-165">Modify model mapping</span></span>
1. <span data-ttu-id="e5488-166">В дереве разверните узел "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="e5488-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="e5488-167">В дереве выберите "Intrastat (model)\Intrastat (mapping)".</span><span class="sxs-lookup"><span data-stu-id="e5488-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="e5488-168">Изменение существующее сопоставление модели, чтобы начать использовать его для обновления данных приложения и для архивирования сведений о составлении отчетности Интрастат.</span><span class="sxs-lookup"><span data-stu-id="e5488-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="e5488-169">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="e5488-169">Click Designer.</span></span>
4. <span data-ttu-id="e5488-170">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e5488-170">Click New.</span></span>
5. <span data-ttu-id="e5488-171">В поле "Имя" введите "Обновить архив".</span><span class="sxs-lookup"><span data-stu-id="e5488-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="e5488-172">Обновить архив</span><span class="sxs-lookup"><span data-stu-id="e5488-172">Update archive</span></span>  
6. <span data-ttu-id="e5488-173">В поле "Направление" выберите "В место назначения".</span><span class="sxs-lookup"><span data-stu-id="e5488-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="e5488-174">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e5488-174">Click Save.</span></span>
    * <span data-ttu-id="e5488-175">Это новое сопоставление задает поток данных для перемещения данных (сведений о составлении отчетности Интрастат) из модели данных в таблицы приложения (место назначения обновления).</span><span class="sxs-lookup"><span data-stu-id="e5488-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="e5488-176">Обратите внимание, что для получения данных из приложения для процесса составления отчетности и для использования данных из модели данных для обновления данных приложения необходимо использовать разные корневые элементы модели.</span><span class="sxs-lookup"><span data-stu-id="e5488-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="e5488-177">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="e5488-177">Click Designer.</span></span>
9. <span data-ttu-id="e5488-178">В дереве выберите "Модель данных\Модель данных".</span><span class="sxs-lookup"><span data-stu-id="e5488-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="e5488-179">Добавьте требуемый источник данных.</span><span class="sxs-lookup"><span data-stu-id="e5488-179">Add the required data source.</span></span> <span data-ttu-id="e5488-180">Это модель данных, которая содержит сведения о включенных в отчет проводках Интрастат, которые необходимо архивировать.</span><span class="sxs-lookup"><span data-stu-id="e5488-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="e5488-181">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="e5488-181">Click Add root.</span></span>
11. <span data-ttu-id="e5488-182">В поле "Имя" введите "модель".</span><span class="sxs-lookup"><span data-stu-id="e5488-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="e5488-183">модель</span><span class="sxs-lookup"><span data-stu-id="e5488-183">model</span></span>  
12. <span data-ttu-id="e5488-184">В поле "Определение" введите или выберите значение "Для обновления данных приложения".</span><span class="sxs-lookup"><span data-stu-id="e5488-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="e5488-185">Для обновления данных приложения</span><span class="sxs-lookup"><span data-stu-id="e5488-185">For application data update</span></span>  
13. <span data-ttu-id="e5488-186">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e5488-186">Click OK.</span></span>
14. <span data-ttu-id="e5488-187">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="e5488-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="e5488-188">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="e5488-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="e5488-189">В дереве выберите "модель\Заголовок архива".</span><span class="sxs-lookup"><span data-stu-id="e5488-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="e5488-190">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5488-190">Click Add.</span></span>
    * <span data-ttu-id="e5488-191">Поскольку для архивирования необходимо перечислить включенные в отчет проводки Интрастат, необходимо добавить соответствующий источник данных.</span><span class="sxs-lookup"><span data-stu-id="e5488-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="e5488-192">В поле "Имя" введите "Перечисленные строки".</span><span class="sxs-lookup"><span data-stu-id="e5488-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="e5488-193">Перечисленные строки</span><span class="sxs-lookup"><span data-stu-id="e5488-193">Enumerated lines</span></span>  
19. <span data-ttu-id="e5488-194">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="e5488-194">Click Edit formula.</span></span>
20. <span data-ttu-id="e5488-195">В дереве выберите "Список\ENUMERATE".</span><span class="sxs-lookup"><span data-stu-id="e5488-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="e5488-196">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="e5488-196">Click Add function.</span></span>
22. <span data-ttu-id="e5488-197">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="e5488-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="e5488-198">В дереве разверните "модель\Заголовок архива".</span><span class="sxs-lookup"><span data-stu-id="e5488-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="e5488-199">В дереве выберите "модель\Заголовок архива\Строки архива".</span><span class="sxs-lookup"><span data-stu-id="e5488-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="e5488-200">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="e5488-200">Click Add data source.</span></span>
26. <span data-ttu-id="e5488-201">В поле "Формула" введите "ENUMERATE(модель.'Заголовок архива'.'Строки архива')".</span><span class="sxs-lookup"><span data-stu-id="e5488-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="e5488-202">ENUMERATE(модель.'Заголовок архива'.'Строки архива')</span><span class="sxs-lookup"><span data-stu-id="e5488-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="e5488-203">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e5488-203">Click Save.</span></span>
28. <span data-ttu-id="e5488-204">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e5488-204">Close the page.</span></span>
29. <span data-ttu-id="e5488-205">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e5488-205">Click OK.</span></span>
30. <span data-ttu-id="e5488-206">Щелкните "Добавить место назначения".</span><span class="sxs-lookup"><span data-stu-id="e5488-206">Click Add destination.</span></span>
    * <span data-ttu-id="e5488-207">Добавьте таблицы приложения в качестве необходимых мест назначения, требующих обновления сведений об архивации проводок Интрастат, включенных в отчет.</span><span class="sxs-lookup"><span data-stu-id="e5488-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="e5488-208">В поле "Имя" введите "Архив".</span><span class="sxs-lookup"><span data-stu-id="e5488-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="e5488-209">Архивировать</span><span class="sxs-lookup"><span data-stu-id="e5488-209">Archive</span></span>  
32. <span data-ttu-id="e5488-210">В поле "Имя таблицы" введите "IntrastatArchiveGeneral".</span><span class="sxs-lookup"><span data-stu-id="e5488-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="e5488-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="e5488-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="e5488-212">Оставьте действие с записью "Вставка", чтобы вы могли добавлять записи во время архивирования сведений о каждом процессе подготовки отчетности Интрастат.</span><span class="sxs-lookup"><span data-stu-id="e5488-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="e5488-213">Выберите "Да" в поле "Записывать в infolog".</span><span class="sxs-lookup"><span data-stu-id="e5488-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="e5488-214">Выберите "Да", чтобы получать информацию о проблемах, возникающих при обновлении данных приложения.</span><span class="sxs-lookup"><span data-stu-id="e5488-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="e5488-215">Выберите "Да" в поле "Пропустить проверку действия с записью".</span><span class="sxs-lookup"><span data-stu-id="e5488-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="e5488-216">Выберите "Да", чтобы подавить ошибки проверки, связанные с пустым полем "Код архива Интрастат".</span><span class="sxs-lookup"><span data-stu-id="e5488-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="e5488-217">Это будет делаться после добавления записей на основании параметров порядкового номера, настроенных для этой таблицы в форме "Параметры внешней торговли".</span><span class="sxs-lookup"><span data-stu-id="e5488-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="e5488-218">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e5488-218">Click OK.</span></span>
    * <span data-ttu-id="e5488-219">Привяжите элементы добавленного источника данных (отфильтрованной модели на основе выбранного корневого элемента) к элементам из добавленного места назначения.</span><span class="sxs-lookup"><span data-stu-id="e5488-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="e5488-220">В дереве разверните "Архив".</span><span class="sxs-lookup"><span data-stu-id="e5488-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="e5488-221">В дереве разверните "Архив\<Связи".</span><span class="sxs-lookup"><span data-stu-id="e5488-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="e5488-222">В дереве разверните "Архив\<Связи\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="e5488-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="e5488-223">В дереве выберите "Архив\<Связи\IntrastatArchiveDetail\Сумма(AmountMST)".</span><span class="sxs-lookup"><span data-stu-id="e5488-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="e5488-224">В дереве разверните "модель\Заголовок архива\Перечисленные строки".</span><span class="sxs-lookup"><span data-stu-id="e5488-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="e5488-225">В дереве разверните "модель\Заголовок архива\Перечисленные строки\Значение".</span><span class="sxs-lookup"><span data-stu-id="e5488-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="e5488-226">В дереве выберите "модель\Заголовок архива\Перечисленные строки\Значение\Сумма".</span><span class="sxs-lookup"><span data-stu-id="e5488-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="e5488-227">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="e5488-227">Click Bind.</span></span>
44. <span data-ttu-id="e5488-228">В дереве выберите "Архив\<Связи\IntrastatArchiveDetail\Товар(IntrastatCommodity)".</span><span class="sxs-lookup"><span data-stu-id="e5488-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="e5488-229">В дереве выберите "модель\Заголовок архива\Перечисленные строки\Значение\Код записи товара".</span><span class="sxs-lookup"><span data-stu-id="e5488-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="e5488-230">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="e5488-230">Click Bind.</span></span>
47. <span data-ttu-id="e5488-231">В дереве выберите "Архив\<Связи\IntrastatArchiveDetail\Код номенклатуры(ItemId)".</span><span class="sxs-lookup"><span data-stu-id="e5488-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="e5488-232">В дереве выберите "модель\Заголовок архива\Перечисленные строки\Значение\Код номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="e5488-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="e5488-233">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="e5488-233">Click Bind.</span></span>
50. <span data-ttu-id="e5488-234">В дереве выберите "Архив\<Связи\IntrastatArchiveDetail\Номер строки(LineNumber)".</span><span class="sxs-lookup"><span data-stu-id="e5488-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="e5488-235">В дереве выберите "модель\Заголовок архива\Перечисленные строки\Номер".</span><span class="sxs-lookup"><span data-stu-id="e5488-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="e5488-236">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="e5488-236">Click Bind.</span></span>
53. <span data-ttu-id="e5488-237">В дереве выберите "Архив\<Связи\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="e5488-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="e5488-238">В дереве выберите "модель\Заголовок архива\Перечисленные строки".</span><span class="sxs-lookup"><span data-stu-id="e5488-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="e5488-239">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="e5488-239">Click Bind.</span></span>
56. <span data-ttu-id="e5488-240">В дереве выберите "Архив\Имя файла(FileName)".</span><span class="sxs-lookup"><span data-stu-id="e5488-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="e5488-241">В дереве выберите "модель\Заголовок архива\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="e5488-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="e5488-242">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="e5488-242">Click Bind.</span></span>
59. <span data-ttu-id="e5488-243">В дереве выберите "Архив\Число строк(NumberOfLines)".</span><span class="sxs-lookup"><span data-stu-id="e5488-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="e5488-244">В дереве выберите "модель\Заголовок архива\Число строк".</span><span class="sxs-lookup"><span data-stu-id="e5488-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="e5488-245">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="e5488-245">Click Bind.</span></span>
62. <span data-ttu-id="e5488-246">В дереве выберите "Архив".</span><span class="sxs-lookup"><span data-stu-id="e5488-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="e5488-247">В дереве выберите "модель\Заголовок архива".</span><span class="sxs-lookup"><span data-stu-id="e5488-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="e5488-248">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="e5488-248">Click Bind.</span></span>
65. <span data-ttu-id="e5488-249">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e5488-249">Click Save.</span></span>
66. <span data-ttu-id="e5488-250">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e5488-250">Close the page.</span></span>
67. <span data-ttu-id="e5488-251">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e5488-251">Close the page.</span></span>

