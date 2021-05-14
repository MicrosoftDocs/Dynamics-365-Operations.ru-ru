---
title: Разработка конфигураций для формирования отчетов в формате Office, содержащих внедренные изображения
description: В этой теме описано, как разработать конфигурации, которые создают электронные документы в форматах Excel и Word, содержащих внедренные изображения.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944565"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="336e6-103">Разработка конфигураций для формирования отчетов в формате Office, содержащих внедренные изображения</span><span class="sxs-lookup"><span data-stu-id="336e6-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="336e6-104">Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="336e6-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="336e6-105">Эта процедура объясняет, как разрабатывать конфигурации электронной отчетности для формирования документа Microsoft Excel или Word, содержащего внедренные изображения.</span><span class="sxs-lookup"><span data-stu-id="336e6-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="336e6-106">В этой процедуре создаются необходимые конфигурации электронной отчетности для демонстрационной компании Litware, Inc. Эти действия могут быть выполнены с использованием набора данных USMF.</span><span class="sxs-lookup"><span data-stu-id="336e6-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="336e6-107">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="336e6-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="336e6-108">Перед началом необходимо загрузить и сохранить следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="336e6-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="336e6-109">описание</span><span class="sxs-lookup"><span data-stu-id="336e6-109">Description</span></span>                                          | <span data-ttu-id="336e6-110">Имя файла</span><span class="sxs-lookup"><span data-stu-id="336e6-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="336e6-111">Конфигурации модели данных электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="336e6-111">ER data model configuration</span></span>                          | [<span data-ttu-id="336e6-112">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="336e6-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="336e6-113">Конфигурация формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="336e6-113">ER format configuration</span></span>                              | [<span data-ttu-id="336e6-114">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="336e6-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="336e6-115">Изображение логотипа компании</span><span class="sxs-lookup"><span data-stu-id="336e6-115">Company logo image</span></span>                                   | [<span data-ttu-id="336e6-116">Company logo.png</span><span class="sxs-lookup"><span data-stu-id="336e6-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="336e6-117">Изображение подписи</span><span class="sxs-lookup"><span data-stu-id="336e6-117">Signature image</span></span>                                      | [<span data-ttu-id="336e6-118">Signature image.png</span><span class="sxs-lookup"><span data-stu-id="336e6-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="336e6-119">Альтернативное изображение подписи</span><span class="sxs-lookup"><span data-stu-id="336e6-119">Alternative signature image</span></span>                          | [<span data-ttu-id="336e6-120">Signature image 2.png</span><span class="sxs-lookup"><span data-stu-id="336e6-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="336e6-121">Шаблон Microsoft Word для печати чеков платежей</span><span class="sxs-lookup"><span data-stu-id="336e6-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="336e6-122">Cheque template Word.docx</span><span class="sxs-lookup"><span data-stu-id="336e6-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="336e6-123">Проверьте обязательные компоненты</span><span class="sxs-lookup"><span data-stu-id="336e6-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="336e6-124">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="336e6-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="336e6-125">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="336e6-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="336e6-126">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="336e6-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="336e6-127">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="336e6-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="336e6-128">Добавление новой конфигурации модели ER</span><span class="sxs-lookup"><span data-stu-id="336e6-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="336e6-129">Вместо того чтобы создавать новую модель, можно загрузить файл конфигурации модели ER (Model for cheques.xml), сохраненный ранее.</span><span class="sxs-lookup"><span data-stu-id="336e6-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="336e6-130">Этот файл содержит образец модели данных для платежных чеков и сопоставление модели данных с компонентами данных приложения Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="336e6-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="336e6-131">На экспресс-вкладке "Версии" щелкните "Обменять".</span><span class="sxs-lookup"><span data-stu-id="336e6-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="336e6-132">Щелкните "Загрузить из XML-файла".</span><span class="sxs-lookup"><span data-stu-id="336e6-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="336e6-133">Нажмите кнопку "Обзор" и выберите "Модель для cheques.xml".</span><span class="sxs-lookup"><span data-stu-id="336e6-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="336e6-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="336e6-134">Click OK.</span></span>  
 6. <span data-ttu-id="336e6-135">Загруженная модель будет использоваться как источник данных для сведений для создания документов, содержащих изображения в Excel и Word.</span><span class="sxs-lookup"><span data-stu-id="336e6-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="336e6-136">Добавление новой конфигурации формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="336e6-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="336e6-137">Вместо того чтобы создавать новую новый формат, можно загрузить файл конфигурации формата ER (Cheques printing format.xml), сохраненный ранее.</span><span class="sxs-lookup"><span data-stu-id="336e6-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="336e6-138">Этот файл содержит образец макета формата для печати чеков с помощью предварительно напечатанной формы и сопоставление данного формата с моделью данных "Модель для чеков".</span><span class="sxs-lookup"><span data-stu-id="336e6-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="336e6-139">Щелкните "Обменять".</span><span class="sxs-lookup"><span data-stu-id="336e6-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="336e6-140">Щелкните "Загрузить из XML-файла".</span><span class="sxs-lookup"><span data-stu-id="336e6-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="336e6-141">Щелкните "Обзор" и выберите файл Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="336e6-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="336e6-142">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="336e6-142">Click OK.</span></span>  
 6. <span data-ttu-id="336e6-143">В дереве разверните "Модель для чеков".</span><span class="sxs-lookup"><span data-stu-id="336e6-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="336e6-144">В дереве выберите "Модель для чеков\Формат печати чеков".</span><span class="sxs-lookup"><span data-stu-id="336e6-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="336e6-145">Загруженный формат будет использоваться для создания документов, содержащих изображения в Excel и Word.</span><span class="sxs-lookup"><span data-stu-id="336e6-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="336e6-146">Настройка параметров пользователей ER</span><span class="sxs-lookup"><span data-stu-id="336e6-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="336e6-147">В области действий щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="336e6-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="336e6-148">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="336e6-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="336e6-149">Выберите "Да" в поле "Запустить настройки".</span><span class="sxs-lookup"><span data-stu-id="336e6-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="336e6-150">Включите флаг "Запустить черновик" для запуска черновой версии выбранного формата вместо завершенной.</span><span class="sxs-lookup"><span data-stu-id="336e6-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="336e6-151">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="336e6-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="336e6-152">Настройка параметров управления банком и кассовыми операциями</span><span class="sxs-lookup"><span data-stu-id="336e6-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="336e6-153">Перейдите в раздел "Управление банком и кассовыми операциями" > "Банковские счета" > "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="336e6-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="336e6-154">Используйте экспресс-фильтр для фильтрации поля "Банковский счет" по значению 'USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="336e6-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="336e6-155">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="336e6-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="336e6-156">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="336e6-156">Click Check.</span></span>  
 5. <span data-ttu-id="336e6-157">Разверните раздел "Настройка".</span><span class="sxs-lookup"><span data-stu-id="336e6-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="336e6-158">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="336e6-158">Click Edit.</span></span>  
 7. <span data-ttu-id="336e6-159">В поле "Логотип компании" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="336e6-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="336e6-160">Щелкните "Логотип компании".</span><span class="sxs-lookup"><span data-stu-id="336e6-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="336e6-161">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="336e6-161">Click Change.</span></span>  
 10. <span data-ttu-id="336e6-162">Нажмите кнопку "Обзор" и выберите ранее загруженный файл Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="336e6-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="336e6-163">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="336e6-163">Click Save.</span></span>  
 12. <span data-ttu-id="336e6-164">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="336e6-164">Close the page.</span></span>  
 13. <span data-ttu-id="336e6-165">Разверните раздел "Подпись".</span><span class="sxs-lookup"><span data-stu-id="336e6-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="336e6-166">Выберите значение "Да" в поле "Печать первой подписи".</span><span class="sxs-lookup"><span data-stu-id="336e6-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="336e6-167">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="336e6-167">Click Change.</span></span>  
 16. <span data-ttu-id="336e6-168">Нажмите кнопку "Обзор" и выберите ранее загруженный файл Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="336e6-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="336e6-169">Разверните раздел "Копии".</span><span class="sxs-lookup"><span data-stu-id="336e6-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="336e6-170">В поле "Водяной знак" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="336e6-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="336e6-171">В поле "Универсальный электронный формат экспорта" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="336e6-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="336e6-172">Выберите конфигурацию "Форма печати чеков".</span><span class="sxs-lookup"><span data-stu-id="336e6-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="336e6-173">Теперь выбранный формат ER будет использоваться для печати чеков.</span><span class="sxs-lookup"><span data-stu-id="336e6-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="336e6-174">Щелкните "Привязать".</span><span class="sxs-lookup"><span data-stu-id="336e6-174">Click Attach.</span></span>  
 23. <span data-ttu-id="336e6-175">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="336e6-175">Click New.</span></span>  
 24. <span data-ttu-id="336e6-176">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="336e6-176">Click File.</span></span>  
 25. <span data-ttu-id="336e6-177">Нажмите кнопку "Обзор" и выберите ранее загруженный файл Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="336e6-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="336e6-178">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="336e6-178">Close the page.</span></span>  
 27. <span data-ttu-id="336e6-179">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="336e6-179">Close the page.</span></span>  
 28. <span data-ttu-id="336e6-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="336e6-180">Close the page.</span></span>  
 29. <span data-ttu-id="336e6-181">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Параметры управления банком и кассовыми операциями".</span><span class="sxs-lookup"><span data-stu-id="336e6-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="336e6-182">Выберите "Да" в поле "Разрешать создание контрольной операции в неактивных банковских счетах:".</span><span class="sxs-lookup"><span data-stu-id="336e6-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="336e6-183">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="336e6-183">Click Save.</span></span>  
 32. <span data-ttu-id="336e6-184">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="336e6-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
