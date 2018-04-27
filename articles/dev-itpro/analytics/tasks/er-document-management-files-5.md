--- 
title: "Изменение и выполнение формата для использования файлов управления документами в выходных форматах"
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b38f69fc169367aa56468b2c8f06b65fd1291c79
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs"></a><span data-ttu-id="c94ee-103">Изменение и выполнение формата для использования файлов управления документами в выходных форматах</span><span class="sxs-lookup"><span data-stu-id="c94ee-103">Modify and run format to use Document Management files in format outputs</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c94ee-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="c94ee-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="c94ee-105">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="c94ee-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c94ee-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 4. Выполнение формата)".</span><span class="sxs-lookup"><span data-stu-id="c94ee-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="c94ee-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="c94ee-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="c94ee-108">Изменение формата для заполнения вложений при создании сообщений в двоичном формате</span><span class="sxs-lookup"><span data-stu-id="c94ee-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="c94ee-109">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="c94ee-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c94ee-110">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="c94ee-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="c94ee-111">В дереве разверните узел "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="c94ee-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="c94ee-112">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)\Пример сообщения электронной накладной".</span><span class="sxs-lookup"><span data-stu-id="c94ee-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="c94ee-113">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="c94ee-113">Click Designer.</span></span>
    * <span data-ttu-id="c94ee-114">Вы заполните сообщение накладной при создании выходных данных в виде XML-файла с использованием кодировку UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c94ee-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="c94ee-115">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c94ee-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="c94ee-116">В дереве выберите "Общее\Файл".</span><span class="sxs-lookup"><span data-stu-id="c94ee-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="c94ee-117">В поле "Имя" введите "XML-сообщение".</span><span class="sxs-lookup"><span data-stu-id="c94ee-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="c94ee-118">XML-сообщение</span><span class="sxs-lookup"><span data-stu-id="c94ee-118">Xml message</span></span>  
9. <span data-ttu-id="c94ee-119">В поле "Кодировка" введите "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="c94ee-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="c94ee-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="c94ee-120">UTF-8</span></span>  
10. <span data-ttu-id="c94ee-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c94ee-121">Click OK.</span></span>
    * <span data-ttu-id="c94ee-122">Настройте создание выходных данных в виде ZIP-файла.</span><span class="sxs-lookup"><span data-stu-id="c94ee-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="c94ee-123">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c94ee-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="c94ee-124">В дереве выберите "Общее\Папка".</span><span class="sxs-lookup"><span data-stu-id="c94ee-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="c94ee-125">В поле "Имя" введите "Выходные данные ZIP".</span><span class="sxs-lookup"><span data-stu-id="c94ee-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="c94ee-126">Выходные данные ZIP</span><span class="sxs-lookup"><span data-stu-id="c94ee-126">Zip output</span></span>  
14. <span data-ttu-id="c94ee-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c94ee-127">Click OK.</span></span>
15. <span data-ttu-id="c94ee-128">В дереве выберите "Выходные данные ZIP".</span><span class="sxs-lookup"><span data-stu-id="c94ee-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="c94ee-129">Добавьте вложения в созданный ZIP-файл в виде файлов с исходными именами и расширениями.</span><span class="sxs-lookup"><span data-stu-id="c94ee-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="c94ee-130">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c94ee-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="c94ee-131">В дереве выберите "Общее\Файл".</span><span class="sxs-lookup"><span data-stu-id="c94ee-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="c94ee-132">В поле "Имя" введите "Вложенный файл".</span><span class="sxs-lookup"><span data-stu-id="c94ee-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="c94ee-133">Прикрепленный файл</span><span class="sxs-lookup"><span data-stu-id="c94ee-133">Attached file</span></span>  
19. <span data-ttu-id="c94ee-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c94ee-134">Click OK.</span></span>
20. <span data-ttu-id="c94ee-135">В дереве выберите "Выходные данные ZIP\Вложенный файл".</span><span class="sxs-lookup"><span data-stu-id="c94ee-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="c94ee-136">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c94ee-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="c94ee-137">В дереве выберите "Текст\Base64".</span><span class="sxs-lookup"><span data-stu-id="c94ee-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="c94ee-138">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c94ee-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="c94ee-139">Сопоставление новых элементов формата с моделью данных</span><span class="sxs-lookup"><span data-stu-id="c94ee-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="c94ee-140">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="c94ee-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="c94ee-141">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="c94ee-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="c94ee-142">В дереве разверните "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="c94ee-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="c94ee-143">В дереве выберите "Выходные данные ZIP\Вложенный файл\Base64".</span><span class="sxs-lookup"><span data-stu-id="c94ee-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="c94ee-144">В дереве выберите "модель\Вложения накладной\Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="c94ee-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="c94ee-145">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c94ee-145">Click Bind.</span></span>
7. <span data-ttu-id="c94ee-146">В дереве выберите "Выходные данные ZIP\Вложенный файл".</span><span class="sxs-lookup"><span data-stu-id="c94ee-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="c94ee-147">Щелкните "Изменить имя файла".</span><span class="sxs-lookup"><span data-stu-id="c94ee-147">Click Edit filename.</span></span>
9. <span data-ttu-id="c94ee-148">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="c94ee-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="c94ee-149">В дереве разверните "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="c94ee-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="c94ee-150">В дереве выберите "модель\Вложения накладной\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="c94ee-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="c94ee-151">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="c94ee-151">Click Add data source.</span></span>
13. <span data-ttu-id="c94ee-152">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="c94ee-152">Click Save.</span></span>
14. <span data-ttu-id="c94ee-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c94ee-153">Close the page.</span></span>
15. <span data-ttu-id="c94ee-154">В дереве выберите "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="c94ee-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="c94ee-155">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c94ee-155">Click Bind.</span></span>
17. <span data-ttu-id="c94ee-156">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c94ee-156">Click Save.</span></span>
18. <span data-ttu-id="c94ee-157">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c94ee-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="c94ee-158">Выполните разработанный отчет для выбранной накладной</span><span class="sxs-lookup"><span data-stu-id="c94ee-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="c94ee-159">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="c94ee-159">Click Run.</span></span>
2. <span data-ttu-id="c94ee-160">Разверните раздел "Записи для добавления ()".</span><span class="sxs-lookup"><span data-stu-id="c94ee-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="c94ee-161">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="c94ee-161">Click Filter.</span></span>
4. <span data-ttu-id="c94ee-162">Выберите строку журнала накладных клиента и поле "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="c94ee-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="c94ee-163">В поле "Критерии". В поле "Заказ на продажу" критериев введите номер заказа 000148.</span><span class="sxs-lookup"><span data-stu-id="c94ee-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="c94ee-164">000148</span><span class="sxs-lookup"><span data-stu-id="c94ee-164">000148</span></span>  
6. <span data-ttu-id="c94ee-165">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c94ee-165">Click OK.</span></span>
7. <span data-ttu-id="c94ee-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c94ee-166">Click OK.</span></span>
    * <span data-ttu-id="c94ee-167">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="c94ee-167">Review the generated output.</span></span> <span data-ttu-id="c94ee-168">Обратите внимание, что помимо сообщения накладной в XML-формате отдельный файл был создан для каждого вложения.</span><span class="sxs-lookup"><span data-stu-id="c94ee-168">Note, in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="c94ee-169">Файлы вложений заполняются сжатыми выходными данными ZIP в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="c94ee-169">The attachment files are populated with the zipped output in binary format.</span></span>  


