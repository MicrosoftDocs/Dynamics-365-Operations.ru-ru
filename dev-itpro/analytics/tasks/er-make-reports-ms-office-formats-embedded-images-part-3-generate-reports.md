--- 
title: "Создание отчетов в форматах Microsoft Office с внедренными изображениями для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может разрабатывать конфигурации электронной отчетности для формирования электронных документов в форматах MS Office (Excel и Word), содержащих внедренные изображения."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: de2840ebc6c91e313546859f5c0d8939eb80977b
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="generate-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a><span data-ttu-id="37f43-103">Создание отчетов в форматах Microsoft Office с внедренными изображениями для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="37f43-103">Generate reports in Microsoft Office formats with embedded images for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37f43-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может разрабатывать конфигурации электронной отчетности для формирования электронных документов в форматах MS Office (Excel и Word), содержащих внедренные изображения.</span><span class="sxs-lookup"><span data-stu-id="37f43-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="37f43-105">В этом примере вам предстоит использовать созданные конфигурации электронной отчетности для демонстрационной компании Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="37f43-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="37f43-106">Для выполнения этих действий необходимо сначала выполнить действия в проводнике по задаче "Электронная отчетность — Создание отчетов в форматах MS Office с внедренными изображениями (Часть 2. Проверка конфигураций)".</span><span class="sxs-lookup"><span data-stu-id="37f43-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="37f43-107">Эти шаги можно выполнить в компании USMF.</span><span class="sxs-lookup"><span data-stu-id="37f43-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="37f43-108">Запуск формата с первоначальным сопоставлением модели</span><span class="sxs-lookup"><span data-stu-id="37f43-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="37f43-109">Перейдите в раздел "Управление банком и кассовыми операциями" > "Банковские счета" > "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="37f43-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="37f43-110">Используйте экспресс-фильтр для фильтрации поля "Банковский счет" по значению 'USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="37f43-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="37f43-111">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="37f43-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="37f43-112">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="37f43-112">Click Check.</span></span>
5. <span data-ttu-id="37f43-113">Щелкните "Печать шаблона".</span><span class="sxs-lookup"><span data-stu-id="37f43-113">Click Print test.</span></span>
    * <span data-ttu-id="37f43-114">Запустите формат в целях тестирования.</span><span class="sxs-lookup"><span data-stu-id="37f43-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="37f43-115">Выберите "Да" в поле "Формат оборотных чеков".</span><span class="sxs-lookup"><span data-stu-id="37f43-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="37f43-116">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="37f43-116">Click OK.</span></span>
    * <span data-ttu-id="37f43-117">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="37f43-117">Review the created output.</span></span> <span data-ttu-id="37f43-118">Обратите внимание, что логотип компании присутствует в отчете, также как и подпись уполномоченного лица.</span><span class="sxs-lookup"><span data-stu-id="37f43-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="37f43-119">Изображение подписи берется из поля типа данных "Контейнер" записи формата чека, связанной с выбранным банковским счетом.</span><span class="sxs-lookup"><span data-stu-id="37f43-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="37f43-120">Разверните раздел "Копии".</span><span class="sxs-lookup"><span data-stu-id="37f43-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="37f43-121">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="37f43-121">Click Edit.</span></span>
10. <span data-ttu-id="37f43-122">В поле "Водяной знак" введите "Печатать водяной знак как аннуляцию".</span><span class="sxs-lookup"><span data-stu-id="37f43-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="37f43-123">Измените параметр макета водяных знаков для отображения текста водяных знаков при создании документа в элементе формы Excel.</span><span class="sxs-lookup"><span data-stu-id="37f43-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="37f43-124">Щелкните "Печать шаблона".</span><span class="sxs-lookup"><span data-stu-id="37f43-124">Click Print test.</span></span>
12. <span data-ttu-id="37f43-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="37f43-125">Click OK.</span></span>
    * <span data-ttu-id="37f43-126">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="37f43-126">Review the created output.</span></span> <span data-ttu-id="37f43-127">Обратите внимание, что водяной знак отображается в созданном отчете в соответствии с параметром выбора.</span><span class="sxs-lookup"><span data-stu-id="37f43-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="37f43-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-128">Close the page.</span></span>
14. <span data-ttu-id="37f43-129">На панели операций щелкните "Управление платежами".</span><span class="sxs-lookup"><span data-stu-id="37f43-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="37f43-130">Щелкните "Чеки".</span><span class="sxs-lookup"><span data-stu-id="37f43-130">Click Checks.</span></span>
16. <span data-ttu-id="37f43-131">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="37f43-131">Click Show filters.</span></span>
17. <span data-ttu-id="37f43-132">Примените следующие фильтры: введите значение фильтрации "381","385","389" в поле "Номер чека", используя оператор фильтра "один из".</span><span class="sxs-lookup"><span data-stu-id="37f43-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="37f43-133">В списке пометьте все строки.</span><span class="sxs-lookup"><span data-stu-id="37f43-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="37f43-134">Щелкните "Печатать копию чека".</span><span class="sxs-lookup"><span data-stu-id="37f43-134">Click Print check copy.</span></span>
    * <span data-ttu-id="37f43-135">Запустите формат для повторной печати выбранных чеков.</span><span class="sxs-lookup"><span data-stu-id="37f43-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="37f43-136">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="37f43-136">Review the created output.</span></span> <span data-ttu-id="37f43-137">Обратите внимание, что выбранные чеки были напечатаны повторно.</span><span class="sxs-lookup"><span data-stu-id="37f43-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="37f43-138">Логотип компании и метки не печатаются, так как они присутствуют на предварительно напечатанной форме.</span><span class="sxs-lookup"><span data-stu-id="37f43-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="37f43-139">Изменение сопоставления импортированной модели данных</span><span class="sxs-lookup"><span data-stu-id="37f43-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="37f43-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-140">Close the page.</span></span>
2. <span data-ttu-id="37f43-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-141">Close the page.</span></span>
3. <span data-ttu-id="37f43-142">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="37f43-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="37f43-143">В дереве выберите "Модель для чеков".</span><span class="sxs-lookup"><span data-stu-id="37f43-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="37f43-144">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="37f43-144">Click Designer.</span></span>
6. <span data-ttu-id="37f43-145">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="37f43-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="37f43-146">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="37f43-146">Click Designer.</span></span>
    * <span data-ttu-id="37f43-147">Мы изменим привязку элемента "подпись" модели данных для получения изображения подписи из файла, который был прикреплен к записи макета чека, связанной с выбранным банковским счетом.</span><span class="sxs-lookup"><span data-stu-id="37f43-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="37f43-148">Отключите отображение подробностей.</span><span class="sxs-lookup"><span data-stu-id="37f43-148">Turn Show details off.</span></span>
9. <span data-ttu-id="37f43-149">В дереве разверните "layout".</span><span class="sxs-lookup"><span data-stu-id="37f43-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="37f43-150">В дереве разверните "layout\signature".</span><span class="sxs-lookup"><span data-stu-id="37f43-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="37f43-151">В дереве выберите "layout\signature\image = chequesaccount.'<Связи'.BankChequeLayout.Signature1Bmp".</span><span class="sxs-lookup"><span data-stu-id="37f43-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="37f43-152">В дереве разверните "chequesaccount".</span><span class="sxs-lookup"><span data-stu-id="37f43-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="37f43-153">В дереве разверните "chequesaccount\<Связи".</span><span class="sxs-lookup"><span data-stu-id="37f43-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="37f43-154">В дереве разверните "chequesaccount\<Связи\BankChequeLayout".</span><span class="sxs-lookup"><span data-stu-id="37f43-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="37f43-155">В дереве разверните "chequesaccount\<Связи\BankChequeLayout\<Связи".</span><span class="sxs-lookup"><span data-stu-id="37f43-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="37f43-156">В дереве разверните "chequesaccount\<Связи\BankChequeLayout\<Связи\<Документы".</span><span class="sxs-lookup"><span data-stu-id="37f43-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="37f43-157">В дереве выберите "chequesaccount\<Связи\BankChequeLayout\<Связи\<Документы\getFileContentAsContainer()".</span><span class="sxs-lookup"><span data-stu-id="37f43-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="37f43-158">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="37f43-158">Click Bind.</span></span>
19. <span data-ttu-id="37f43-159">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="37f43-159">Click Save.</span></span>
20. <span data-ttu-id="37f43-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-160">Close the page.</span></span>
21. <span data-ttu-id="37f43-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-161">Close the page.</span></span>
22. <span data-ttu-id="37f43-162">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-162">Close the page.</span></span>
23. <span data-ttu-id="37f43-163">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="37f43-164">Запуск формата с использованием откорректированного сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="37f43-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="37f43-165">Перейдите в раздел "Управление банком и кассовыми операциями" > "Банковские счета" > "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="37f43-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="37f43-166">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="37f43-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="37f43-167">Например, отфильтруйте поле "Банковский счет" по значению "USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="37f43-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="37f43-168">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="37f43-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="37f43-169">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="37f43-169">Click Check.</span></span>
5. <span data-ttu-id="37f43-170">Щелкните "Печать шаблона".</span><span class="sxs-lookup"><span data-stu-id="37f43-170">Click Print test.</span></span>
6. <span data-ttu-id="37f43-171">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="37f43-171">Click OK.</span></span>
    * <span data-ttu-id="37f43-172">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="37f43-172">Review the created output.</span></span> <span data-ttu-id="37f43-173">Обратите внимание, что изображение из вложения модуля "Управление документами" представлено как подпись уполномоченного лица.</span><span class="sxs-lookup"><span data-stu-id="37f43-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="37f43-174">Использование документа MS Word в качестве шаблона в импортированном формате</span><span class="sxs-lookup"><span data-stu-id="37f43-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="37f43-175">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-175">Close the page.</span></span>
2. <span data-ttu-id="37f43-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-176">Close the page.</span></span>
3. <span data-ttu-id="37f43-177">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="37f43-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="37f43-178">В дереве разверните "Модель для чеков".</span><span class="sxs-lookup"><span data-stu-id="37f43-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="37f43-179">В дереве выберите "Модель для чеков\Формат печати чеков".</span><span class="sxs-lookup"><span data-stu-id="37f43-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="37f43-180">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="37f43-180">Click Designer.</span></span>
7. <span data-ttu-id="37f43-181">Нажмите кнопку Вложения.</span><span class="sxs-lookup"><span data-stu-id="37f43-181">Click Attachments.</span></span>
8. <span data-ttu-id="37f43-182">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="37f43-182">Click Delete.</span></span>
9. <span data-ttu-id="37f43-183">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="37f43-183">Click Yes.</span></span>
10. <span data-ttu-id="37f43-184">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="37f43-184">Click New.</span></span>
11. <span data-ttu-id="37f43-185">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="37f43-185">Click File.</span></span>
    * <span data-ttu-id="37f43-186">Щелкните "Обзор" и выберите заранее загруженный файл Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="37f43-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="37f43-187">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-187">Close the page.</span></span>
13. <span data-ttu-id="37f43-188">В поле "Шаблон" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="37f43-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="37f43-189">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="37f43-189">Click Save.</span></span>
15. <span data-ttu-id="37f43-190">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-190">Close the page.</span></span>
16. <span data-ttu-id="37f43-191">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="37f43-191">Click Edit.</span></span>
17. <span data-ttu-id="37f43-192">Выберите "Да" в поле "Запустить черновик".</span><span class="sxs-lookup"><span data-stu-id="37f43-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="37f43-193">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37f43-193">Close the page.</span></span>
19. <span data-ttu-id="37f43-194">Перейдите в раздел "Управление банком и кассовыми операциями" > "Банковские счета" > "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="37f43-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="37f43-195">Используйте экспресс-фильтр для фильтрации поля "Банковский счет" по значению 'USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="37f43-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="37f43-196">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="37f43-196">Click Check.</span></span>
22. <span data-ttu-id="37f43-197">Щелкните "Печать шаблона".</span><span class="sxs-lookup"><span data-stu-id="37f43-197">Click Print test.</span></span>
23. <span data-ttu-id="37f43-198">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="37f43-198">Click OK.</span></span>
    * <span data-ttu-id="37f43-199">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="37f43-199">Review the created output.</span></span> <span data-ttu-id="37f43-200">Обратите внимание, что выходные данные были созданы как документ MS Word с внедренными изображениями, представляющими логотип компании, подпись уполномоченного лица и выбранный текст водяного знака.</span><span class="sxs-lookup"><span data-stu-id="37f43-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  


