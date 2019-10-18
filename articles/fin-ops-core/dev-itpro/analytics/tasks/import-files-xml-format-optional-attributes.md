---
title: (RCS) Импорт файлов в формате XML с дополнительными атрибутами
description: В этой теме содержится информация о том, как пользователь может проектировать конфигурацию формата ER для импорта файлов в формате XML, содержащих дополнительные атрибуты.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182194"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="1f54e-103">(RCS) Импорт файлов в формате XML с дополнительными атрибутами</span><span class="sxs-lookup"><span data-stu-id="1f54e-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f54e-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может разработать конфигурацию формата ER для импорта файлов в формате XML, содержащих необязательные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="1f54e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="1f54e-105">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="1f54e-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="1f54e-106">Перед началом загрузите и локально сохраните файл IncomingDocumentToLearnHowToHandleOptionalAttributes.xml из [центра загрузки Майкрософт](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="1f54e-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="1f54e-107">Перейдите в раздел **Все рабочие области** > **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="1f54e-108">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="1f54e-109">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре [Создание поставщика конфигурации и пометка его как активного](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1f54e-109">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="1f54e-110">Щелкните **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="1f54e-111">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="1f54e-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="1f54e-112">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1f54e-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="1f54e-113">В поле **Имя** введите "Модель для импорта XML-файла".</span><span class="sxs-lookup"><span data-stu-id="1f54e-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="1f54e-114">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="1f54e-115">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="1f54e-116">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1f54e-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="1f54e-117">В поле **Имя** введите "Root".</span><span class="sxs-lookup"><span data-stu-id="1f54e-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="1f54e-118">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-118">Click **Add**.</span></span>
8.  <span data-ttu-id="1f54e-119">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1f54e-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="1f54e-120">В поле **Имя** введите "List".</span><span class="sxs-lookup"><span data-stu-id="1f54e-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="1f54e-121">В поле **Тип элемента** выберите **Список записей**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="1f54e-122">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-122">Click **Add**.</span></span>
12. <span data-ttu-id="1f54e-123">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1f54e-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="1f54e-124">В поле **Имя** введите "Code".</span><span class="sxs-lookup"><span data-stu-id="1f54e-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="1f54e-125">В поле **Тип элемента** выберите **Строка**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="1f54e-126">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-126">Click **Add**.</span></span>
16. <span data-ttu-id="1f54e-127">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-127">Click **Save**.</span></span>
17. <span data-ttu-id="1f54e-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1f54e-128">Close the page.</span></span>
18. <span data-ttu-id="1f54e-129">Щелкните **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-129">Click **Change status**.</span></span>
19. <span data-ttu-id="1f54e-130">Щелкните **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-130">Click **Complete**.</span></span>
20. <span data-ttu-id="1f54e-131">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="1f54e-132">Создание формата для импорта данных</span><span class="sxs-lookup"><span data-stu-id="1f54e-132">Create a format for data import</span></span>
1.  <span data-ttu-id="1f54e-133">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1f54e-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="1f54e-134">В поле **Создать** введите "Формат, основанный на модели данных «Модель для импорта XML-файла»".</span><span class="sxs-lookup"><span data-stu-id="1f54e-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="1f54e-135">В поле **Имя** введите "Формат для импорта XML-файла".</span><span class="sxs-lookup"><span data-stu-id="1f54e-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="1f54e-136">Выберите **Да** в поле **Поддерживает импорт данных**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="1f54e-137">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="1f54e-138">Создание формата для разбора входящего файла в формате XML</span><span class="sxs-lookup"><span data-stu-id="1f54e-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="1f54e-139">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="1f54e-140">Щелкните **Добавить корень**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1f54e-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="1f54e-141">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="1f54e-142">В поле **Имя** введите "root".</span><span class="sxs-lookup"><span data-stu-id="1f54e-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="1f54e-143">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-143">Click **OK**.</span></span>
6.  <span data-ttu-id="1f54e-144">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1f54e-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="1f54e-145">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="1f54e-146">В поле **Имя** введите "document".</span><span class="sxs-lookup"><span data-stu-id="1f54e-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="1f54e-147">В поле **Кратность** выберите **Один — много**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="1f54e-148">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-148">Click **OK**.</span></span>
11. <span data-ttu-id="1f54e-149">В дереве выберите **root\document**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="1f54e-150">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1f54e-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="1f54e-151">В дереве выберите **XML\Атрибут**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="1f54e-152">В поле **Имя** введите "ID".</span><span class="sxs-lookup"><span data-stu-id="1f54e-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="1f54e-153">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-153">Click **OK**.</span></span>
16. <span data-ttu-id="1f54e-154">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="1f54e-155">Создание сопоставления форматов для сохранения проанализированных данных в модели данных</span><span class="sxs-lookup"><span data-stu-id="1f54e-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="1f54e-156">Щелкните **Сопоставить формат модели**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="1f54e-157">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-157">Click **New**.</span></span>
3. <span data-ttu-id="1f54e-158">В поле **Определение** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1f54e-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="1f54e-159">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="1f54e-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1f54e-160">В поле **Имя** введите "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="1f54e-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="1f54e-161">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-161">Click **Save**.</span></span>
7. <span data-ttu-id="1f54e-162">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-162">Click **Designer**.</span></span>
8. <span data-ttu-id="1f54e-163">В дереве разверните **format**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="1f54e-164">В дереве разверните узел **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="1f54e-165">В дереве выберите \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="1f54e-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="1f54e-166">(документ)\*\*.</span><span class="sxs-lookup"><span data-stu-id="1f54e-166">(document)\*\*.</span></span>
11. <span data-ttu-id="1f54e-167">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-167">Click **Bind**.</span></span>
12. <span data-ttu-id="1f54e-168">В дереве разверните \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="1f54e-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="1f54e-169">(документ)\*\*.</span><span class="sxs-lookup"><span data-stu-id="1f54e-169">(document)\*\*.</span></span>
13. <span data-ttu-id="1f54e-170">В дереве выберите \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="1f54e-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="1f54e-171">(документ)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="1f54e-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="1f54e-172">В дереве разверните **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="1f54e-173">В дереве выберите **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="1f54e-174">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-174">Click **Bind**.</span></span>
17. <span data-ttu-id="1f54e-175">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-175">Click **Save**.</span></span>
18. <span data-ttu-id="1f54e-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1f54e-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="1f54e-177">Запуск сопоставления формата</span><span class="sxs-lookup"><span data-stu-id="1f54e-177">Run format mapping</span></span>
1. <span data-ttu-id="1f54e-178">Щелкните **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-178">Click **Run**.</span></span>
2. <span data-ttu-id="1f54e-179">Нажмите кнопку **Обзор** и выберите **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="1f54e-180">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="1f54e-181">Выбранный файл не был импортирован, поскольку структура формата предполагает существование атрибута "id" для элемента "document", но импортированный файл не содержит такого атрибута.</span><span class="sxs-lookup"><span data-stu-id="1f54e-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="1f54e-182">Изменение структуры формата, чтобы обрабатывать атрибут XML как необязательный</span><span class="sxs-lookup"><span data-stu-id="1f54e-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="1f54e-183">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1f54e-183">Close the page.</span></span>
2. <span data-ttu-id="1f54e-184">В дереве разверните **root\document**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="1f54e-185">В дереве выберите **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="1f54e-186">Выберите **Да** в поле **Пустая строка для отсутствующего атрибута**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="1f54e-187">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="1f54e-188">Запуск сопоставления форматов для проверки изменений</span><span class="sxs-lookup"><span data-stu-id="1f54e-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="1f54e-189">Щелкните **Сопоставить формат модели**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="1f54e-190">Щелкните **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-190">Click **Run**.</span></span>
3. <span data-ttu-id="1f54e-191">Нажмите кнопку **Обзор** и выберите файл **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="1f54e-192">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f54e-192">Click **OK**.</span></span>
5. <span data-ttu-id="1f54e-193">Просмотрите сформированный файл.</span><span class="sxs-lookup"><span data-stu-id="1f54e-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="1f54e-194">Этот же файл, который был импортирован в качестве структуры формата, теперь считает атрибут "id" для элемента "document" необязательным.</span><span class="sxs-lookup"><span data-stu-id="1f54e-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
