---
title: Проверка конфигураций для формирования отчетов в формате Office, содержащих внедренные изображения
description: В этой теме описано, как разработать конфигурации отчетности для создания электронных документов, содержащих внедренные изображения. (Часть 1 — Настройка параметров).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6aa5c4d45f9139c65f3aaf1ae392829e3e4967df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569446"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="3a466-104">Проверка конфигураций для формирования отчетов в формате Office, содержащих внедренные изображения</span><span class="sxs-lookup"><span data-stu-id="3a466-104">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a466-105">Для выполнения этих действий необходимо сначала выполнить действия в проводнике по задаче "Электронная отчетность — Создание отчетов в форматах MS Office с внедренными изображениями (Часть 1. Настройка параметров)".</span><span class="sxs-lookup"><span data-stu-id="3a466-105">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="3a466-106">Эта процедура показывает, как разрабатывать конфигурации электронной отчетности для формирования электронных документов, содержащих внедренные изображения, в Microsoft Excel и Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="3a466-106">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="3a466-107">В этом примере вам предстоит рассмотреть конфигурации электронной отчетности для демонстрационной компании Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="3a466-107">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="3a466-108">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="3a466-108">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="3a466-109">Действия можно выполнять с использованием набора данных USMF.</span><span class="sxs-lookup"><span data-stu-id="3a466-109">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="3a466-110">Просмотр импортированной модели данных</span><span class="sxs-lookup"><span data-stu-id="3a466-110">Review the imported data model</span></span>
1. <span data-ttu-id="3a466-111">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="3a466-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="3a466-112">В дереве выберите "Модель для чеков".</span><span class="sxs-lookup"><span data-stu-id="3a466-112">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="3a466-113">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="3a466-113">Click Designer.</span></span>
    * <span data-ttu-id="3a466-114">Эта модель предназначена для представления платежных чеков с точки зрения бизнеса и сопоставления этой модели источникам данных приложения.</span><span class="sxs-lookup"><span data-stu-id="3a466-114">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="3a466-115">Просмотрите эту модель в конструкторе операций электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="3a466-115">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="3a466-116">Обратите внимание на присутствующие атрибуты элементов модели: структуру, имя, описание, тип данных и т. д.</span><span class="sxs-lookup"><span data-stu-id="3a466-116">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="3a466-117">В дереве разверните "root".</span><span class="sxs-lookup"><span data-stu-id="3a466-117">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="3a466-118">В дереве выберите "root\cheques".</span><span class="sxs-lookup"><span data-stu-id="3a466-118">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="3a466-119">В дереве разверните "root\cheques".</span><span class="sxs-lookup"><span data-stu-id="3a466-119">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="3a466-120">В дереве разверните "root\cheques\attributes".</span><span class="sxs-lookup"><span data-stu-id="3a466-120">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="3a466-121">В дереве разверните "root\payer".</span><span class="sxs-lookup"><span data-stu-id="3a466-121">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="3a466-122">В дереве выберите "root\istestrun".</span><span class="sxs-lookup"><span data-stu-id="3a466-122">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="3a466-123">В дереве выберите "root\layout".</span><span class="sxs-lookup"><span data-stu-id="3a466-123">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="3a466-124">Элемент "макет" этой модели представляет сведения о макете формы печати чеков для выбранного банковского счета.</span><span class="sxs-lookup"><span data-stu-id="3a466-124">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="3a466-125">Он также включает два узла типа данных "Контейнер" для хранения изображений.</span><span class="sxs-lookup"><span data-stu-id="3a466-125">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="3a466-126">В дереве разверните "root\layout".</span><span class="sxs-lookup"><span data-stu-id="3a466-126">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="3a466-127">В дереве выберите "root\layout\company logo".</span><span class="sxs-lookup"><span data-stu-id="3a466-127">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="3a466-128">В дереве разверните "root\layout\company logo".</span><span class="sxs-lookup"><span data-stu-id="3a466-128">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="3a466-129">В дереве выберите "root\layout\company logo\image".</span><span class="sxs-lookup"><span data-stu-id="3a466-129">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="3a466-130">В дереве выберите "root\layout\company logo\isprinted".</span><span class="sxs-lookup"><span data-stu-id="3a466-130">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="3a466-131">В дереве выберите "root\layout\signature".</span><span class="sxs-lookup"><span data-stu-id="3a466-131">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="3a466-132">В дереве разверните "root\layout\signature".</span><span class="sxs-lookup"><span data-stu-id="3a466-132">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="3a466-133">В дереве выберите "root\layout\signature\image".</span><span class="sxs-lookup"><span data-stu-id="3a466-133">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="3a466-134">В дереве выберите "root\layout\signature\isprinted".</span><span class="sxs-lookup"><span data-stu-id="3a466-134">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="3a466-135">Обратите внимание, что два элемента модели данных "изображение" привязаны к полям таблиц, содержащих изображения логотипа компании и подписи уполномоченного лица в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="3a466-135">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="3a466-136">В дереве разверните "root\layout\watermark".</span><span class="sxs-lookup"><span data-stu-id="3a466-136">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="3a466-137">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="3a466-137">Click Map model to datasource.</span></span>
22. <span data-ttu-id="3a466-138">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="3a466-138">Click Designer.</span></span>
23. <span data-ttu-id="3a466-139">В дереве разверните "chequesselected".</span><span class="sxs-lookup"><span data-stu-id="3a466-139">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="3a466-140">В дереве разверните "layout".</span><span class="sxs-lookup"><span data-stu-id="3a466-140">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="3a466-141">В дереве разверните "layout\company logo".</span><span class="sxs-lookup"><span data-stu-id="3a466-141">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="3a466-142">В дереве разверните "layout\signature".</span><span class="sxs-lookup"><span data-stu-id="3a466-142">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="3a466-143">В дереве разверните "layout\watermark".</span><span class="sxs-lookup"><span data-stu-id="3a466-143">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="3a466-144">Установите переключатель "Показать сведения" в положение "Вкл.".</span><span class="sxs-lookup"><span data-stu-id="3a466-144">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="3a466-145">Обратите внимание, что элемент модели данных "чеки" связан с таблицей TmpChequePrintout, которая во время выполнения будет содержать записи для чеков, выбранных пользователем для печати.</span><span class="sxs-lookup"><span data-stu-id="3a466-145">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="3a466-146">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a466-146">Close the page.</span></span>
30. <span data-ttu-id="3a466-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a466-147">Close the page.</span></span>
31. <span data-ttu-id="3a466-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a466-148">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="3a466-149">Просмотр импортированного формата</span><span class="sxs-lookup"><span data-stu-id="3a466-149">Review the imported format</span></span>
1. <span data-ttu-id="3a466-150">В дереве разверните "Модель для чеков".</span><span class="sxs-lookup"><span data-stu-id="3a466-150">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="3a466-151">В дереве выберите "Модель для чеков\Формат печати чеков".</span><span class="sxs-lookup"><span data-stu-id="3a466-151">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="3a466-152">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="3a466-152">Click Designer.</span></span>
4. <span data-ttu-id="3a466-153">Нажмите кнопку Вложения.</span><span class="sxs-lookup"><span data-stu-id="3a466-153">Click Attachments.</span></span>
5. <span data-ttu-id="3a466-154">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="3a466-154">Click Open.</span></span>
    * <span data-ttu-id="3a466-155">Откройте шаблон вложенного отчета в Excel.</span><span class="sxs-lookup"><span data-stu-id="3a466-155">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="3a466-156">Просмотрите шаблон Excel вложенного отчета, который будет использоваться для печати чеков.</span><span class="sxs-lookup"><span data-stu-id="3a466-156">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="3a466-157">Шаблон содержит по два чека на страницу и предназначен для печати на предварительно напечатанной форме.</span><span class="sxs-lookup"><span data-stu-id="3a466-157">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="3a466-158">Обратите внимание, что внедрено два пустых изображения.</span><span class="sxs-lookup"><span data-stu-id="3a466-158">Note that two blank images are embedded.</span></span> <span data-ttu-id="3a466-159">Эти пустые изображения предназначены для логотипа компании и подписи человека, авторизующего платеж.</span><span class="sxs-lookup"><span data-stu-id="3a466-159">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="3a466-160">Убедитесь, что в Excel изображения называются CompLogo и SignatureImage соответственно.</span><span class="sxs-lookup"><span data-stu-id="3a466-160">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="3a466-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a466-161">Close the page.</span></span>
7. <span data-ttu-id="3a466-162">В дереве разверните "Отчет".</span><span class="sxs-lookup"><span data-stu-id="3a466-162">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="3a466-163">В дереве разверните "Отчет\ChequeLines".</span><span class="sxs-lookup"><span data-stu-id="3a466-163">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="3a466-164">В дереве выберите "Отчет\ChequeLines\CompLogo".</span><span class="sxs-lookup"><span data-stu-id="3a466-164">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="3a466-165">Установите переключатель "Показать сведения" в положение "Вкл.".</span><span class="sxs-lookup"><span data-stu-id="3a466-165">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="3a466-166">Обратите внимание, что элемент ячейки "CompLogo" формата представляет объект Excel, используемый для заполнения изображения логотипа компании в отчете.</span><span class="sxs-lookup"><span data-stu-id="3a466-166">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="3a466-167">Этот элемент формата привязан к элементу модели данных "изображение", который во время выполнения содержит логотип компании в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="3a466-167">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="3a466-168">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="3a466-168">Click the Mapping tab.</span></span>
12. <span data-ttu-id="3a466-169">Щелкните "Изменить включенное".</span><span class="sxs-lookup"><span data-stu-id="3a466-169">Click Edit enabled.</span></span>
    * <span data-ttu-id="3a466-170">Обратите внимание, что элемент ячейки "CompLogo" формата можно отключить.</span><span class="sxs-lookup"><span data-stu-id="3a466-170">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="3a466-171">В этом случае связанный элемент изображения Excel будет скрывать логотип компании в сформированном отчете.</span><span class="sxs-lookup"><span data-stu-id="3a466-171">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="3a466-172">Если выражение включения возвращает значение TRUE и заданная привязка не предоставляет изображения, в связанном элементе изображения Excel будет отображаться изображение, сохраненное в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="3a466-172">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="3a466-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a466-173">Close the page.</span></span>
14. <span data-ttu-id="3a466-174">В дереве разверните "labels: Контейнер".</span><span class="sxs-lookup"><span data-stu-id="3a466-174">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="3a466-175">Некоторые подписи, которые присутствуют в предварительно напечатанной форме чека, будут включены в отчет при его создании в целях тестирования.</span><span class="sxs-lookup"><span data-stu-id="3a466-175">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="3a466-176">Тем не менее эти подписи не будут печататься при реальной печати, поскольку они уже есть в предварительно напечатанной форме.</span><span class="sxs-lookup"><span data-stu-id="3a466-176">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="3a466-177">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a466-177">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]