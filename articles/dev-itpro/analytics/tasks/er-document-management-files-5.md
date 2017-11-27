--- 
title: "Изменение и выполнение формата для использования файлов управления документами в выходных форматах для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: 5d4f57ae2a309d9e15c1afe60c3e91d7d7eb3870
ms.openlocfilehash: e145c4c7a1f3fd88481ad32d0af05511437e21dc
ms.contentlocale: ru-ru
ms.lasthandoff: 11/02/2017

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="be504-103">Изменение и выполнение формата для использования файлов управления документами в выходных форматах для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="be504-103">Modify and run format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be504-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="be504-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="be504-105">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="be504-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="be504-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 4. Выполнение формата)".</span><span class="sxs-lookup"><span data-stu-id="be504-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="be504-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="be504-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="be504-108">Изменение формата для заполнения вложений при создании сообщений в двоичном формате</span><span class="sxs-lookup"><span data-stu-id="be504-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="be504-109">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="be504-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="be504-110">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="be504-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="be504-111">В дереве разверните узел "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="be504-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="be504-112">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)\Пример сообщения электронной накладной".</span><span class="sxs-lookup"><span data-stu-id="be504-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="be504-113">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="be504-113">Click Designer.</span></span>
    * <span data-ttu-id="be504-114">Вы заполните сообщение накладной при создании выходных данных в виде XML-файла с использованием кодировку UNICODE.</span><span class="sxs-lookup"><span data-stu-id="be504-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="be504-115">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="be504-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="be504-116">В дереве выберите "Общее\Файл".</span><span class="sxs-lookup"><span data-stu-id="be504-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="be504-117">В поле "Имя" введите "XML-сообщение".</span><span class="sxs-lookup"><span data-stu-id="be504-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="be504-118">XML-сообщение</span><span class="sxs-lookup"><span data-stu-id="be504-118">Xml message</span></span>  
9. <span data-ttu-id="be504-119">В поле "Кодировка" введите "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="be504-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="be504-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="be504-120">UTF-8</span></span>  
10. <span data-ttu-id="be504-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="be504-121">Click OK.</span></span>
    * <span data-ttu-id="be504-122">Настройте создание выходных данных в виде ZIP-файла.</span><span class="sxs-lookup"><span data-stu-id="be504-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="be504-123">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="be504-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="be504-124">В дереве выберите "Общее\Папка".</span><span class="sxs-lookup"><span data-stu-id="be504-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="be504-125">В поле "Имя" введите "Выходные данные ZIP".</span><span class="sxs-lookup"><span data-stu-id="be504-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="be504-126">Выходные данные ZIP</span><span class="sxs-lookup"><span data-stu-id="be504-126">Zip output</span></span>  
14. <span data-ttu-id="be504-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="be504-127">Click OK.</span></span>
15. <span data-ttu-id="be504-128">В дереве выберите "Выходные данные ZIP".</span><span class="sxs-lookup"><span data-stu-id="be504-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="be504-129">Добавьте вложения в созданный ZIP-файл в виде файлов с исходными именами и расширениями.</span><span class="sxs-lookup"><span data-stu-id="be504-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="be504-130">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="be504-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="be504-131">В дереве выберите "Общее\Файл".</span><span class="sxs-lookup"><span data-stu-id="be504-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="be504-132">В поле "Имя" введите "Вложенный файл".</span><span class="sxs-lookup"><span data-stu-id="be504-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="be504-133">Прикрепленный файл</span><span class="sxs-lookup"><span data-stu-id="be504-133">Attached file</span></span>  
19. <span data-ttu-id="be504-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="be504-134">Click OK.</span></span>
20. <span data-ttu-id="be504-135">В дереве выберите "Выходные данные ZIP\Вложенный файл".</span><span class="sxs-lookup"><span data-stu-id="be504-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="be504-136">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="be504-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="be504-137">В дереве выберите "Текст\Base64".</span><span class="sxs-lookup"><span data-stu-id="be504-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="be504-138">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="be504-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="be504-139">Сопоставление новых элементов формата с моделью данных</span><span class="sxs-lookup"><span data-stu-id="be504-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="be504-140">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="be504-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="be504-141">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="be504-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="be504-142">В дереве разверните "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="be504-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="be504-143">В дереве выберите "Выходные данные ZIP\Вложенный файл\Base64".</span><span class="sxs-lookup"><span data-stu-id="be504-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="be504-144">В дереве выберите "модель\Вложения накладной\Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="be504-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="be504-145">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="be504-145">Click Bind.</span></span>
7. <span data-ttu-id="be504-146">В дереве выберите "Выходные данные ZIP\Вложенный файл".</span><span class="sxs-lookup"><span data-stu-id="be504-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="be504-147">Щелкните "Изменить имя файла".</span><span class="sxs-lookup"><span data-stu-id="be504-147">Click Edit filename.</span></span>
9. <span data-ttu-id="be504-148">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="be504-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="be504-149">В дереве разверните "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="be504-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="be504-150">В дереве выберите "модель\Вложения накладной\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="be504-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="be504-151">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="be504-151">Click Add data source.</span></span>
13. <span data-ttu-id="be504-152">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="be504-152">Click Save.</span></span>
14. <span data-ttu-id="be504-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="be504-153">Close the page.</span></span>
15. <span data-ttu-id="be504-154">В дереве выберите "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="be504-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="be504-155">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="be504-155">Click Bind.</span></span>
17. <span data-ttu-id="be504-156">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="be504-156">Click Save.</span></span>
18. <span data-ttu-id="be504-157">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="be504-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="be504-158">Выполните разработанный отчет для выбранной накладной</span><span class="sxs-lookup"><span data-stu-id="be504-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="be504-159">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="be504-159">Click Run.</span></span>
2. <span data-ttu-id="be504-160">Разверните раздел "Записи для добавления ()".</span><span class="sxs-lookup"><span data-stu-id="be504-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="be504-161">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="be504-161">Click Filter.</span></span>
4. <span data-ttu-id="be504-162">Выберите строку журнала накладных клиента и поле "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="be504-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="be504-163">В поле "Критерии". В поле "Заказ на продажу" критериев введите номер заказа 000148.</span><span class="sxs-lookup"><span data-stu-id="be504-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="be504-164">000148</span><span class="sxs-lookup"><span data-stu-id="be504-164">000148</span></span>  
6. <span data-ttu-id="be504-165">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="be504-165">Click OK.</span></span>
7. <span data-ttu-id="be504-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="be504-166">Click OK.</span></span>
    * <span data-ttu-id="be504-167">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="be504-167">Review the generated output.</span></span> <span data-ttu-id="be504-168">Обратите внимание, что помимо сообщения накладной в XML-формате отдельный файл был создан для каждого вложения.</span><span class="sxs-lookup"><span data-stu-id="be504-168">Note, in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="be504-169">Файлы вложений заполняются сжатыми выходными данными ZIP в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="be504-169">The attachment files are populated with the zipped output in binary format.</span></span>  


