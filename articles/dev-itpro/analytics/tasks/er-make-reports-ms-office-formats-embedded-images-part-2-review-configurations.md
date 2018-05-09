--- 
title: "Обзор конфигураций для подготовки отчетов в форматах Microsoft Office с внедренными изображениями"
description: "Для выполнения этих действий необходимо сначала выполнить действия в проводнике по задаче \"Электронная отчетность — Создание отчетов в форматах MS Office с внедренными изображениями (Часть 1. Настройка параметров)\"."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ca4749904607b458dbc0e81e451eb23cc465752e
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="review-configurations-to-make-reports-in-microsoft-office-formats-with-embedded-images"></a><span data-ttu-id="4c2a5-103">Обзор конфигураций для подготовки отчетов в форматах Microsoft Office с внедренными изображениями</span><span class="sxs-lookup"><span data-stu-id="4c2a5-103">Review configurations to make reports in Microsoft Office formats with embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4c2a5-104">Для выполнения этих действий необходимо сначала выполнить действия в проводнике по задаче "Электронная отчетность — Создание отчетов в форматах MS Office с внедренными изображениями (Часть 1. Настройка параметров)".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-104">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)” task guide.</span></span>

<span data-ttu-id="4c2a5-105">Эта процедура показывает, как разрабатывать конфигурации электронной отчетности для формирования электронных документов, содержащих внедренные изображения, в Microsoft Excel и Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="4c2a5-106">В этом примере вам предстоит рассмотреть конфигурации электронной отчетности для демонстрационной компании Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="4c2a5-107">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="4c2a5-108">Действия можно выполнять с использованием набора данных USMF.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="4c2a5-109">Просмотр импортированной модели данных</span><span class="sxs-lookup"><span data-stu-id="4c2a5-109">Review the imported data model</span></span>
1. <span data-ttu-id="4c2a5-110">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="4c2a5-111">В дереве выберите "Модель для чеков".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="4c2a5-112">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-112">Click Designer.</span></span>
    * <span data-ttu-id="4c2a5-113">Эта модель предназначена для представления платежных чеков с точки зрения бизнеса и сопоставления этой модели источникам данных приложения.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application’s data sources.</span></span> <span data-ttu-id="4c2a5-114">Просмотрите эту модель в конструкторе операций электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="4c2a5-115">Обратите внимание на присутствующие атрибуты элементов модели: структуру, имя, описание, тип данных и т. д.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="4c2a5-116">В дереве разверните "root".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="4c2a5-117">В дереве выберите "root\cheques".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="4c2a5-118">В дереве разверните "root\cheques".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="4c2a5-119">В дереве разверните "root\cheques\attributes".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="4c2a5-120">В дереве разверните "root\payer".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="4c2a5-121">В дереве выберите "root\istestrun".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="4c2a5-122">В дереве выберите "root\layout".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="4c2a5-123">Элемент "макет" этой модели представляет сведения о макете формы печати чеков для выбранного банковского счета.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="4c2a5-124">Он также включает два узла типа данных "Контейнер" для хранения изображений.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="4c2a5-125">В дереве разверните "root\layout".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="4c2a5-126">В дереве выберите "root\layout\company logo".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="4c2a5-127">В дереве разверните "root\layout\company logo".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="4c2a5-128">В дереве выберите "root\layout\company logo\image".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="4c2a5-129">В дереве выберите "root\layout\company logo\isprinted".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="4c2a5-130">В дереве выберите "root\layout\signature".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="4c2a5-131">В дереве разверните "root\layout\signature".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="4c2a5-132">В дереве выберите "root\layout\signature\image".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="4c2a5-133">В дереве выберите "root\layout\signature\isprinted".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="4c2a5-134">Обратите внимание, что два элемента модели данных "изображение" привязаны к полям таблиц, содержащих изображения логотипа компании и подписи уполномоченного лица в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person’s signature in binary format.</span></span>  
20. <span data-ttu-id="4c2a5-135">В дереве разверните "root\layout\watermark".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="4c2a5-136">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="4c2a5-137">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-137">Click Designer.</span></span>
23. <span data-ttu-id="4c2a5-138">В дереве разверните "chequesselected".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="4c2a5-139">В дереве разверните "layout".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="4c2a5-140">В дереве разверните "layout\company logo".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="4c2a5-141">В дереве разверните "layout\signature".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="4c2a5-142">В дереве разверните "layout\watermark".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="4c2a5-143">Установите переключатель "Показать сведения" в положение "Вкл.".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="4c2a5-144">Обратите внимание, что элемент модели данных "чеки" связан с таблицей TmpChequePrintout, которая во время выполнения будет содержать записи для чеков, выбранных пользователем для печати.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="4c2a5-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-145">Close the page.</span></span>
30. <span data-ttu-id="4c2a5-146">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-146">Close the page.</span></span>
31. <span data-ttu-id="4c2a5-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="4c2a5-148">Просмотр импортированного формата</span><span class="sxs-lookup"><span data-stu-id="4c2a5-148">Review the imported format</span></span>
1. <span data-ttu-id="4c2a5-149">В дереве разверните "Модель для чеков".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="4c2a5-150">В дереве выберите "Модель для чеков\Формат печати чеков".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="4c2a5-151">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-151">Click Designer.</span></span>
4. <span data-ttu-id="4c2a5-152">Нажмите кнопку Вложения.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-152">Click Attachments.</span></span>
5. <span data-ttu-id="4c2a5-153">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-153">Click Open.</span></span>
    * <span data-ttu-id="4c2a5-154">Откройте шаблон вложенного отчета в Excel.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-154">Open the attached report’s template in Excel.</span></span>  
    * <span data-ttu-id="4c2a5-155">Просмотрите шаблон Excel вложенного отчета, который будет использоваться для печати чеков.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-155">Review the attached report’s Excel template that will be used to print cheques.</span></span> <span data-ttu-id="4c2a5-156">Шаблон содержит по два чека на страницу и предназначен для печати на предварительно напечатанной форме.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="4c2a5-157">Обратите внимание, что внедрено два пустых изображения.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="4c2a5-158">Эти пустые изображения предназначены для логотипа компании и подписи человека, авторизующего платеж.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="4c2a5-159">Убедитесь, что в Excel изображения называются CompLogo и SignatureImage соответственно.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="4c2a5-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-160">Close the page.</span></span>
7. <span data-ttu-id="4c2a5-161">В дереве разверните "Отчет".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="4c2a5-162">В дереве разверните "Отчет\ChequeLines".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="4c2a5-163">В дереве выберите "Отчет\ChequeLines\CompLogo".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="4c2a5-164">Установите переключатель "Показать сведения" в положение "Вкл.".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="4c2a5-165">Обратите внимание, что элемент ячейки "CompLogo" формата представляет объект Excel, используемый для заполнения изображения логотипа компании в отчете.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-165">Note that the ‘CompLogo’ format’s cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="4c2a5-166">Этот элемент формата привязан к элементу модели данных "изображение", который во время выполнения содержит логотип компании в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="4c2a5-167">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="4c2a5-168">Щелкните "Изменить включенное".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="4c2a5-169">Обратите внимание, что элемент ячейки "CompLogo" формата можно отключить.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-169">Note that you can make the ‘CompLogo’ format’s cell element so that it’s no longer enabled.</span></span> <span data-ttu-id="4c2a5-170">В этом случае связанный элемент изображения Excel будет скрывать логотип компании в сформированном отчете.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="4c2a5-171">Если выражение включения возвращает значение TRUE и заданная привязка не предоставляет изображения, в связанном элементе изображения Excel будет отображаться изображение, сохраненное в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="4c2a5-172">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-172">Close the page.</span></span>
14. <span data-ttu-id="4c2a5-173">В дереве разверните "labels: Контейнер".</span><span class="sxs-lookup"><span data-stu-id="4c2a5-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="4c2a5-174">Некоторые подписи, которые присутствуют в предварительно напечатанной форме чека, будут включены в отчет при его создании в целях тестирования.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-174">Some labels that are presented in the preprinted cheque form will be included in the report when it’s created for testing purposes.</span></span> <span data-ttu-id="4c2a5-175">Тем не менее эти подписи не будут печататься при реальной печати, поскольку они уже есть в предварительно напечатанной форме.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-175">However, those labels won’t be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="4c2a5-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4c2a5-176">Close the page.</span></span>


