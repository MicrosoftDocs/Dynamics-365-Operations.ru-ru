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
ms.openlocfilehash: f34302a32b2e06f281dc93d6df160b88ffac7123
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769793"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="fd8b7-103">(RCS) Импорт файлов в формате XML с дополнительными атрибутами</span><span class="sxs-lookup"><span data-stu-id="fd8b7-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd8b7-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может разработать конфигурацию формата ER для импорта файлов в формате XML, содержащих необязательные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="fd8b7-105">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="fd8b7-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="fd8b7-106">Перед началом загрузите и локально сохраните файл IncomingDocumentToLearnHowToHandleOptionalAttributes.xml из [центра загрузки Майкрософт](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="fd8b7-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="fd8b7-107">Перейдите в раздел **Все рабочие области** > **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="fd8b7-108">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="fd8b7-109">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре [Создание поставщиков конфигурации и пометка их как активных](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="fd8b7-109">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="fd8b7-110">Щелкните **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="fd8b7-111">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="fd8b7-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="fd8b7-112">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="fd8b7-113">В поле **Имя** введите "Модель для импорта XML-файла".</span><span class="sxs-lookup"><span data-stu-id="fd8b7-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="fd8b7-114">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="fd8b7-115">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="fd8b7-116">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="fd8b7-117">В поле **Имя** введите "Root".</span><span class="sxs-lookup"><span data-stu-id="fd8b7-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="fd8b7-118">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-118">Click **Add**.</span></span>
8.  <span data-ttu-id="fd8b7-119">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="fd8b7-120">В поле **Имя** введите "List".</span><span class="sxs-lookup"><span data-stu-id="fd8b7-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="fd8b7-121">В поле **Тип элемента** выберите **Список записей**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="fd8b7-122">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-122">Click **Add**.</span></span>
12. <span data-ttu-id="fd8b7-123">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="fd8b7-124">В поле **Имя** введите "Code".</span><span class="sxs-lookup"><span data-stu-id="fd8b7-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="fd8b7-125">В поле **Тип элемента** выберите **Строка**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="fd8b7-126">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-126">Click **Add**.</span></span>
16. <span data-ttu-id="fd8b7-127">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-127">Click **Save**.</span></span>
17. <span data-ttu-id="fd8b7-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-128">Close the page.</span></span>
18. <span data-ttu-id="fd8b7-129">Щелкните **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-129">Click **Change status**.</span></span>
19. <span data-ttu-id="fd8b7-130">Щелкните **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-130">Click **Complete**.</span></span>
20. <span data-ttu-id="fd8b7-131">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="fd8b7-132">Создание формата для импорта данных</span><span class="sxs-lookup"><span data-stu-id="fd8b7-132">Create a format for data import</span></span>
1.  <span data-ttu-id="fd8b7-133">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="fd8b7-134">В поле **Создать** введите "Формат, основанный на модели данных «Модель для импорта XML-файла»".</span><span class="sxs-lookup"><span data-stu-id="fd8b7-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="fd8b7-135">В поле **Имя** введите "Формат для импорта XML-файла".</span><span class="sxs-lookup"><span data-stu-id="fd8b7-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="fd8b7-136">Выберите **Да** в поле **Поддерживает импорт данных**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="fd8b7-137">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="fd8b7-138">Создание формата для разбора входящего файла в формате XML</span><span class="sxs-lookup"><span data-stu-id="fd8b7-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="fd8b7-139">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="fd8b7-140">Щелкните **Добавить корень**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="fd8b7-141">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="fd8b7-142">В поле **Имя** введите "root".</span><span class="sxs-lookup"><span data-stu-id="fd8b7-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="fd8b7-143">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-143">Click **OK**.</span></span>
6.  <span data-ttu-id="fd8b7-144">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="fd8b7-145">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="fd8b7-146">В поле **Имя** введите "document".</span><span class="sxs-lookup"><span data-stu-id="fd8b7-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="fd8b7-147">В поле **Кратность** выберите **Один — много**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="fd8b7-148">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-148">Click **OK**.</span></span>
11. <span data-ttu-id="fd8b7-149">В дереве выберите **root\document**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="fd8b7-150">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="fd8b7-151">В дереве выберите **XML\Атрибут**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="fd8b7-152">В поле **Имя** введите "ID".</span><span class="sxs-lookup"><span data-stu-id="fd8b7-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="fd8b7-153">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-153">Click **OK**.</span></span>
16. <span data-ttu-id="fd8b7-154">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="fd8b7-155">Создание сопоставления форматов для сохранения проанализированных данных в модели данных</span><span class="sxs-lookup"><span data-stu-id="fd8b7-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="fd8b7-156">Щелкните **Сопоставить формат модели**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="fd8b7-157">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-157">Click **New**.</span></span>
3. <span data-ttu-id="fd8b7-158">В поле **Определение** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="fd8b7-159">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="fd8b7-160">В поле **Имя** введите "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="fd8b7-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="fd8b7-161">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-161">Click **Save**.</span></span>
7. <span data-ttu-id="fd8b7-162">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-162">Click **Designer**.</span></span>
8. <span data-ttu-id="fd8b7-163">В дереве разверните **format**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="fd8b7-164">В дереве разверните узел **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="fd8b7-165">В дереве выберите \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="fd8b7-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="fd8b7-166">(документ)\*\*.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-166">(document)\*\*.</span></span>
11. <span data-ttu-id="fd8b7-167">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-167">Click **Bind**.</span></span>
12. <span data-ttu-id="fd8b7-168">В дереве разверните \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="fd8b7-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="fd8b7-169">(документ)\*\*.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-169">(document)\*\*.</span></span>
13. <span data-ttu-id="fd8b7-170">В дереве выберите \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="fd8b7-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="fd8b7-171">(документ)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="fd8b7-172">В дереве разверните **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="fd8b7-173">В дереве выберите **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="fd8b7-174">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-174">Click **Bind**.</span></span>
17. <span data-ttu-id="fd8b7-175">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-175">Click **Save**.</span></span>
18. <span data-ttu-id="fd8b7-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="fd8b7-177">Запуск сопоставления формата</span><span class="sxs-lookup"><span data-stu-id="fd8b7-177">Run format mapping</span></span>
1. <span data-ttu-id="fd8b7-178">Щелкните **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-178">Click **Run**.</span></span>
2. <span data-ttu-id="fd8b7-179">Нажмите кнопку **Обзор** и выберите **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="fd8b7-180">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="fd8b7-181">Выбранный файл не был импортирован, поскольку структура формата предполагает существование атрибута "id" для элемента "document", но импортированный файл не содержит такого атрибута.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="fd8b7-182">Изменение структуры формата, чтобы обрабатывать атрибут XML как необязательный</span><span class="sxs-lookup"><span data-stu-id="fd8b7-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="fd8b7-183">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-183">Close the page.</span></span>
2. <span data-ttu-id="fd8b7-184">В дереве разверните **root\document**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="fd8b7-185">В дереве выберите **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="fd8b7-186">Выберите **Да** в поле **Пустая строка для отсутствующего атрибута**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="fd8b7-187">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="fd8b7-188">Запуск сопоставления форматов для проверки изменений</span><span class="sxs-lookup"><span data-stu-id="fd8b7-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="fd8b7-189">Щелкните **Сопоставить формат модели**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="fd8b7-190">Щелкните **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-190">Click **Run**.</span></span>
3. <span data-ttu-id="fd8b7-191">Нажмите кнопку **Обзор** и выберите файл **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="fd8b7-192">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-192">Click **OK**.</span></span>
5. <span data-ttu-id="fd8b7-193">Просмотрите сформированный файл.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="fd8b7-194">Этот же файл, который был импортирован в качестве структуры формата, теперь считает атрибут "id" для элемента "document" необязательным.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
