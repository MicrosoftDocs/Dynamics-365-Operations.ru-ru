---
title: Разработка конфигураций для формирования отчетов в формате Office, содержащих внедренные изображения
description: Шаги в этом разделе содержат сведения о том, как разрабатывать конфигурации электронной отчетности, которые формируют электронные документы в форматах Microsoft Office (Excel и Word), содержащие внедренные изображения.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
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
ms.openlocfilehash: 0145565ba060308162620f29a42499b0bffe6496
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684411"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="41ff7-103">Разработка конфигураций для формирования отчетов в формате Office, содержащих внедренные изображения</span><span class="sxs-lookup"><span data-stu-id="41ff7-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41ff7-104">Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="41ff7-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="41ff7-105">Эта процедура объясняет, как разрабатывать конфигурации электронной отчетности для формирования документа Microsoft Excel или Word, содержащего внедренные изображения.</span><span class="sxs-lookup"><span data-stu-id="41ff7-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="41ff7-106">В этой процедуре создаются необходимые конфигурации электронной отчетности для демонстрационной компании Litware, Inc. Эти действия могут быть выполнены с использованием набора данных USMF.</span><span class="sxs-lookup"><span data-stu-id="41ff7-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="41ff7-107">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="41ff7-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="41ff7-108">Прежде чем начать, загрузите и сохраните файлы, перечисленные в разделе справки [Внедрение изображений и фигур в документы, создаваемые с помощью ER](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="41ff7-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="41ff7-109">Это файлы: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png и Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="41ff7-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="41ff7-110">Проверьте обязательные компоненты</span><span class="sxs-lookup"><span data-stu-id="41ff7-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="41ff7-111">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="41ff7-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="41ff7-112">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="41ff7-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="41ff7-113">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="41ff7-113">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="41ff7-114">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="41ff7-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="41ff7-115">Добавление новой конфигурации модели ER</span><span class="sxs-lookup"><span data-stu-id="41ff7-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="41ff7-116">Вместо того чтобы создавать новую модель, можно загрузить файл конфигурации модели ER (Model for cheques.xml), сохраненный ранее.</span><span class="sxs-lookup"><span data-stu-id="41ff7-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="41ff7-117">Этот файл содержит образец модели данных для платежных чеков и сопоставление модели данных с компонентами данных приложения Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="41ff7-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="41ff7-118">На экспресс-вкладке "Версии" щелкните "Обменять".</span><span class="sxs-lookup"><span data-stu-id="41ff7-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="41ff7-119">Щелкните "Загрузить из XML-файла".</span><span class="sxs-lookup"><span data-stu-id="41ff7-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="41ff7-120">Нажмите кнопку "Обзор" и выберите "Модель для cheques.xml".</span><span class="sxs-lookup"><span data-stu-id="41ff7-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="41ff7-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="41ff7-121">Click OK.</span></span>  
 6. <span data-ttu-id="41ff7-122">Загруженная модель будет использоваться как источник данных для сведений для создания документов, содержащих изображения в Excel и Word.</span><span class="sxs-lookup"><span data-stu-id="41ff7-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="41ff7-123">Добавление новой конфигурации формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="41ff7-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="41ff7-124">Вместо того чтобы создавать новую новый формат, можно загрузить файл конфигурации формата ER (Cheques printing format.xml), сохраненный ранее.</span><span class="sxs-lookup"><span data-stu-id="41ff7-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="41ff7-125">Этот файл содержит образец макета формата для печати чеков с помощью предварительно напечатанной формы и сопоставление данного формата с моделью данных "Модель для чеков".</span><span class="sxs-lookup"><span data-stu-id="41ff7-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="41ff7-126">Щелкните "Обменять".</span><span class="sxs-lookup"><span data-stu-id="41ff7-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="41ff7-127">Щелкните "Загрузить из XML-файла".</span><span class="sxs-lookup"><span data-stu-id="41ff7-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="41ff7-128">Щелкните "Обзор" и выберите файл Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="41ff7-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="41ff7-129">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="41ff7-129">Click OK.</span></span>  
 6. <span data-ttu-id="41ff7-130">В дереве разверните "Модель для чеков".</span><span class="sxs-lookup"><span data-stu-id="41ff7-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="41ff7-131">В дереве выберите "Модель для чеков\Формат печати чеков".</span><span class="sxs-lookup"><span data-stu-id="41ff7-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="41ff7-132">Загруженный формат будет использоваться для создания документов, содержащих изображения в Excel и Word.</span><span class="sxs-lookup"><span data-stu-id="41ff7-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="41ff7-133">Настройка параметров пользователей ER</span><span class="sxs-lookup"><span data-stu-id="41ff7-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="41ff7-134">В области действий щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="41ff7-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="41ff7-135">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="41ff7-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="41ff7-136">Выберите "Да" в поле "Запустить настройки".</span><span class="sxs-lookup"><span data-stu-id="41ff7-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="41ff7-137">Включите флаг "Запустить черновик" для запуска черновой версии выбранного формата вместо завершенной.</span><span class="sxs-lookup"><span data-stu-id="41ff7-137">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="41ff7-138">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="41ff7-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="41ff7-139">Настройка параметров управления банком и кассовыми операциями</span><span class="sxs-lookup"><span data-stu-id="41ff7-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="41ff7-140">Перейдите в раздел "Управление банком и кассовыми операциями" > "Банковские счета" > "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="41ff7-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="41ff7-141">Используйте экспресс-фильтр для фильтрации поля "Банковский счет" по значению 'USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="41ff7-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="41ff7-142">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="41ff7-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="41ff7-143">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="41ff7-143">Click Check.</span></span>  
 5. <span data-ttu-id="41ff7-144">Разверните раздел "Настройка".</span><span class="sxs-lookup"><span data-stu-id="41ff7-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="41ff7-145">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="41ff7-145">Click Edit.</span></span>  
 7. <span data-ttu-id="41ff7-146">В поле "Логотип компании" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="41ff7-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="41ff7-147">Щелкните "Логотип компании".</span><span class="sxs-lookup"><span data-stu-id="41ff7-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="41ff7-148">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="41ff7-148">Click Change.</span></span>  
 10. <span data-ttu-id="41ff7-149">Нажмите кнопку "Обзор" и выберите ранее загруженный файл Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="41ff7-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="41ff7-150">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="41ff7-150">Click Save.</span></span>  
 12. <span data-ttu-id="41ff7-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="41ff7-151">Close the page.</span></span>  
 13. <span data-ttu-id="41ff7-152">Разверните раздел "Подпись".</span><span class="sxs-lookup"><span data-stu-id="41ff7-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="41ff7-153">Выберите значение "Да" в поле "Печать первой подписи".</span><span class="sxs-lookup"><span data-stu-id="41ff7-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="41ff7-154">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="41ff7-154">Click Change.</span></span>  
 16. <span data-ttu-id="41ff7-155">Нажмите кнопку "Обзор" и выберите ранее загруженный файл Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="41ff7-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="41ff7-156">Разверните раздел "Копии".</span><span class="sxs-lookup"><span data-stu-id="41ff7-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="41ff7-157">В поле "Водяной знак" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="41ff7-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="41ff7-158">В поле "Универсальный электронный формат экспорта" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="41ff7-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="41ff7-159">Выберите конфигурацию "Форма печати чеков".</span><span class="sxs-lookup"><span data-stu-id="41ff7-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="41ff7-160">Теперь выбранный формат ER будет использоваться для печати чеков.</span><span class="sxs-lookup"><span data-stu-id="41ff7-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="41ff7-161">Щелкните "Привязать".</span><span class="sxs-lookup"><span data-stu-id="41ff7-161">Click Attach.</span></span>  
 23. <span data-ttu-id="41ff7-162">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="41ff7-162">Click New.</span></span>  
 24. <span data-ttu-id="41ff7-163">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="41ff7-163">Click File.</span></span>  
 25. <span data-ttu-id="41ff7-164">Нажмите кнопку "Обзор" и выберите ранее загруженный файл Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="41ff7-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="41ff7-165">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="41ff7-165">Close the page.</span></span>  
 27. <span data-ttu-id="41ff7-166">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="41ff7-166">Close the page.</span></span>  
 28. <span data-ttu-id="41ff7-167">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="41ff7-167">Close the page.</span></span>  
 29. <span data-ttu-id="41ff7-168">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Параметры управления банком и кассовыми операциями".</span><span class="sxs-lookup"><span data-stu-id="41ff7-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="41ff7-169">Выберите "Да" в поле "Разрешать создание контрольной операции в неактивных банковских счетах:".</span><span class="sxs-lookup"><span data-stu-id="41ff7-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="41ff7-170">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="41ff7-170">Click Save.</span></span>  
 32. <span data-ttu-id="41ff7-171">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="41ff7-171">Close the page.</span></span>  
