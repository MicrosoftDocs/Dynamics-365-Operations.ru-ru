---
title: Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 5. Изменение и выполнение формата)
description: В этой теме описывается, как настроить формат электронной отчетности (ER), чтобы в выходных данных электронной отчетности использовать файлы управления документами (вложения). (Часть 5)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f96189163d5ecac47ade9f713b3fd689e41352d0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092496"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="4bce5-104">Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 5. Изменение и выполнение формата)</span><span class="sxs-lookup"><span data-stu-id="4bce5-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4bce5-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="4bce5-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="4bce5-106">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="4bce5-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="4bce5-107">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 4: Выполнение формата)".</span><span class="sxs-lookup"><span data-stu-id="4bce5-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="4bce5-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="4bce5-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="4bce5-109">Изменение формата для заполнения вложений при создании сообщений в двоичном формате</span><span class="sxs-lookup"><span data-stu-id="4bce5-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="4bce5-110">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="4bce5-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="4bce5-111">В дереве разверните "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="4bce5-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="4bce5-112">В дереве разверните узел "Модель накладной клиента\Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="4bce5-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="4bce5-113">В дереве выберите "Модель накладной клиента\Модель накладной клиента (настраиваемая)\Пример сообщения электронной накладной".</span><span class="sxs-lookup"><span data-stu-id="4bce5-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="4bce5-114">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="4bce5-114">Click Designer.</span></span>
    * <span data-ttu-id="4bce5-115">Вы заполните сообщение накладной при создании выходных данных в виде XML-файла с использованием кодировку UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4bce5-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="4bce5-116">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4bce5-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="4bce5-117">В дереве выберите "Общее\Файл".</span><span class="sxs-lookup"><span data-stu-id="4bce5-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="4bce5-118">В поле "Имя" введите "XML-сообщение".</span><span class="sxs-lookup"><span data-stu-id="4bce5-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="4bce5-119">XML-сообщение</span><span class="sxs-lookup"><span data-stu-id="4bce5-119">Xml message</span></span>  
9. <span data-ttu-id="4bce5-120">В поле "Кодировка" введите "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="4bce5-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="4bce5-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="4bce5-121">UTF-8</span></span>  
10. <span data-ttu-id="4bce5-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4bce5-122">Click OK.</span></span>
    * <span data-ttu-id="4bce5-123">Настройте создание выходных данных в виде ZIP-файла.</span><span class="sxs-lookup"><span data-stu-id="4bce5-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="4bce5-124">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4bce5-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="4bce5-125">В дереве выберите "Общее\Папка".</span><span class="sxs-lookup"><span data-stu-id="4bce5-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="4bce5-126">В поле "Имя" введите "Выходные данные ZIP".</span><span class="sxs-lookup"><span data-stu-id="4bce5-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="4bce5-127">Выходные данные ZIP</span><span class="sxs-lookup"><span data-stu-id="4bce5-127">Zip output</span></span>  
14. <span data-ttu-id="4bce5-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4bce5-128">Click OK.</span></span>
15. <span data-ttu-id="4bce5-129">В дереве выберите "Выходные данные ZIP".</span><span class="sxs-lookup"><span data-stu-id="4bce5-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="4bce5-130">Добавьте вложения в созданный ZIP-файл в виде файлов с исходными именами и расширениями.</span><span class="sxs-lookup"><span data-stu-id="4bce5-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="4bce5-131">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4bce5-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="4bce5-132">В дереве выберите "Общее\Файл".</span><span class="sxs-lookup"><span data-stu-id="4bce5-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="4bce5-133">В поле "Имя" введите "Вложенный файл".</span><span class="sxs-lookup"><span data-stu-id="4bce5-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="4bce5-134">Прикрепленный файл</span><span class="sxs-lookup"><span data-stu-id="4bce5-134">Attached file</span></span>  
19. <span data-ttu-id="4bce5-135">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4bce5-135">Click OK.</span></span>
20. <span data-ttu-id="4bce5-136">В дереве выберите "Выходные данные ZIP\Вложенный файл".</span><span class="sxs-lookup"><span data-stu-id="4bce5-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="4bce5-137">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4bce5-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="4bce5-138">В дереве выберите "Текст\Base64".</span><span class="sxs-lookup"><span data-stu-id="4bce5-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="4bce5-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4bce5-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="4bce5-140">Сопоставление новых элементов формата с моделью данных</span><span class="sxs-lookup"><span data-stu-id="4bce5-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="4bce5-141">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="4bce5-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="4bce5-142">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="4bce5-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="4bce5-143">В дереве разверните "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="4bce5-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="4bce5-144">В дереве выберите "Выходные данные ZIP\Вложенный файл\Base64".</span><span class="sxs-lookup"><span data-stu-id="4bce5-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="4bce5-145">В дереве выберите "модель\Вложения накладной\Содержимое файла".</span><span class="sxs-lookup"><span data-stu-id="4bce5-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="4bce5-146">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="4bce5-146">Click Bind.</span></span>
7. <span data-ttu-id="4bce5-147">В дереве выберите "Выходные данные ZIP\Вложенный файл".</span><span class="sxs-lookup"><span data-stu-id="4bce5-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="4bce5-148">Щелкните "Изменить имя файла".</span><span class="sxs-lookup"><span data-stu-id="4bce5-148">Click Edit filename.</span></span>
9. <span data-ttu-id="4bce5-149">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="4bce5-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="4bce5-150">В дереве разверните "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="4bce5-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="4bce5-151">В дереве выберите "модель\Вложения накладной\Имя файла".</span><span class="sxs-lookup"><span data-stu-id="4bce5-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="4bce5-152">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="4bce5-152">Click Add data source.</span></span>
13. <span data-ttu-id="4bce5-153">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="4bce5-153">Click Save.</span></span>
14. <span data-ttu-id="4bce5-154">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4bce5-154">Close the page.</span></span>
15. <span data-ttu-id="4bce5-155">В дереве выберите "модель\Вложения накладной".</span><span class="sxs-lookup"><span data-stu-id="4bce5-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="4bce5-156">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="4bce5-156">Click Bind.</span></span>
17. <span data-ttu-id="4bce5-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bce5-157">Click Save.</span></span>
18. <span data-ttu-id="4bce5-158">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4bce5-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="4bce5-159">Выполните разработанный отчет для выбранной накладной</span><span class="sxs-lookup"><span data-stu-id="4bce5-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="4bce5-160">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="4bce5-160">Click Run.</span></span>
2. <span data-ttu-id="4bce5-161">Разверните раздел "Записи для добавления ()".</span><span class="sxs-lookup"><span data-stu-id="4bce5-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="4bce5-162">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="4bce5-162">Click Filter.</span></span>
4. <span data-ttu-id="4bce5-163">Выберите строку журнала накладных клиента и поле "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="4bce5-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="4bce5-164">В поле "Критерии". В поле "Заказ на продажу" критериев введите номер заказа 000148.</span><span class="sxs-lookup"><span data-stu-id="4bce5-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="4bce5-165">000148</span><span class="sxs-lookup"><span data-stu-id="4bce5-165">000148</span></span>  
6. <span data-ttu-id="4bce5-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4bce5-166">Click OK.</span></span>
7. <span data-ttu-id="4bce5-167">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4bce5-167">Click OK.</span></span>
    * <span data-ttu-id="4bce5-168">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="4bce5-168">Review the generated output.</span></span> <span data-ttu-id="4bce5-169">Обратите внимание, что помимо сообщения накладной в XML-формате отдельный файл был создан для каждого вложения.</span><span class="sxs-lookup"><span data-stu-id="4bce5-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="4bce5-170">Файлы вложений заполняются сжатыми выходными данными ZIP в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="4bce5-170">The attachment files are populated with the zipped output in binary format.</span></span>  

