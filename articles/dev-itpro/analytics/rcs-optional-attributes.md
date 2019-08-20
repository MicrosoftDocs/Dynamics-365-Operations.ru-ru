---
title: Импорт файлов в формате XML с дополнительными атрибутами
description: В этой теме приводятся сведения о разработке форматов электронной отчетности, которые определяют атрибуты XML для разбора входящих электронных документов в формате XML.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb5d721784f45097ab466f75d43256495aac36ca
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850003"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="63630-103">Импорт файлов в формате XML с дополнительными атрибутами</span><span class="sxs-lookup"><span data-stu-id="63630-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="63630-104">Можно разработать форматы электронной отчетности (ER) для синтаксического анализа входящих документов в формате XML.</span><span class="sxs-lookup"><span data-stu-id="63630-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="63630-105">Некоторые атрибуты элементов XML могут быть указаны в разработанном формате электронной отчетности как необязательные.</span><span class="sxs-lookup"><span data-stu-id="63630-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="63630-106">Это позволяет корректно обрабатывать входящие файлы с такими атрибутами XML и без них.</span><span class="sxs-lookup"><span data-stu-id="63630-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="63630-107">Затем можно использовать содержимое из этих файлов для обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="63630-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="63630-108">Чтобы получить дополнительные сведения об этой функции, выполните действия, указанные в теме [RCS: Импорт файлов в формате XML с дополнительными атрибутами](tasks/import-files-xml-format-optional-attributes.md), которая являются частью бизнес-процесса 7.5.4.3 Приобретение/разработка компонентов ИТ-услуг и решений (10677).</span><span class="sxs-lookup"><span data-stu-id="63630-108">To learn more about this feature, complete the steps in the topic, [RCS Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="63630-109">Этот проводник по задаче и его демонстрационные файлы можно загрузить из [центра загрузки Майкрософт](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="63630-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="63630-110">Описание содержания</span><span class="sxs-lookup"><span data-stu-id="63630-110">Content description</span></span>       | <span data-ttu-id="63630-111">Хранилище файлов</span><span class="sxs-lookup"><span data-stu-id="63630-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="63630-112">Образец файла в формате XML</span><span class="sxs-lookup"><span data-stu-id="63630-112">Sample file in XML format</span></span> | <span data-ttu-id="63630-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="63630-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="63630-114">руководство по задаче</span><span class="sxs-lookup"><span data-stu-id="63630-114">Task guide</span></span>                | <span data-ttu-id="63630-115">RCS Импорт файлов в формате XML с дополнительными атрибутами.axtr</span><span class="sxs-lookup"><span data-stu-id="63630-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="63630-116">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может разработать конфигурацию формата ER для импорта файлов в формате XML, содержащих необязательные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="63630-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="63630-117">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре [Создание поставщика конфигурации и установка его в качестве активного](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="63630-117">To complete these steps, you must first complete the steps in the procedure, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="63630-118">Перед началом загрузите и локально сохраните файл IncomingDocumentToLearnHowToHandleOptionalAttributes.xml из центра загрузки Майкрософт (https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="63630-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="63630-119">Перейдите в раздел **Управление организацией** > **Рабочие области** > **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="63630-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="63630-120">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="63630-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="63630-121">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в разделе [Создание поставщика конфигурации и пометка его как активного](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="63630-121">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="63630-122">Щелкните **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="63630-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="63630-123">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="63630-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="63630-124">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63630-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="63630-125">В поле **Имя** введите "Модель для импорта XML-файла".</span><span class="sxs-lookup"><span data-stu-id="63630-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="63630-126">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="63630-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="63630-127">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="63630-127">Click **Designer**.</span></span>
5. <span data-ttu-id="63630-128">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63630-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="63630-129">В поле **Имя** введите "Root".</span><span class="sxs-lookup"><span data-stu-id="63630-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="63630-130">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="63630-130">Click **Add**.</span></span>
8. <span data-ttu-id="63630-131">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63630-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="63630-132">В поле **Имя** введите "List".</span><span class="sxs-lookup"><span data-stu-id="63630-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="63630-133">В поле **Тип элемента** выберите **Список записей**.</span><span class="sxs-lookup"><span data-stu-id="63630-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="63630-134">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="63630-134">Click **Add**.</span></span>
12. <span data-ttu-id="63630-135">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63630-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="63630-136">В поле **Имя** введите "Code".</span><span class="sxs-lookup"><span data-stu-id="63630-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="63630-137">В поле **Тип элемента** выберите **Строка**.</span><span class="sxs-lookup"><span data-stu-id="63630-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="63630-138">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="63630-138">Click **Add**.</span></span>
16. <span data-ttu-id="63630-139">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="63630-139">Click **Save**.</span></span>
17. <span data-ttu-id="63630-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="63630-140">Close the page.</span></span>
18. <span data-ttu-id="63630-141">Щелкните **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="63630-141">Click **Change status**.</span></span>
19. <span data-ttu-id="63630-142">Щелкните **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="63630-142">Click **Complete**.</span></span>
20. <span data-ttu-id="63630-143">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="63630-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="63630-144">Создание формата для импорта данных</span><span class="sxs-lookup"><span data-stu-id="63630-144">Create a format for data import</span></span>
1. <span data-ttu-id="63630-145">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63630-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="63630-146">В поле **Создать** введите "Формат, основанный на модели данных «Модель для импорта XML-файла»".</span><span class="sxs-lookup"><span data-stu-id="63630-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="63630-147">В поле **Имя** введите "Формат для импорта XML-файла".</span><span class="sxs-lookup"><span data-stu-id="63630-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="63630-148">Выберите **Да** в поле **Поддерживает импорт данных**.</span><span class="sxs-lookup"><span data-stu-id="63630-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="63630-149">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="63630-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="63630-150">Создание формата для разбора входящего файла в формате XML</span><span class="sxs-lookup"><span data-stu-id="63630-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="63630-151">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="63630-151">Click **Designer**.</span></span>
2. <span data-ttu-id="63630-152">Щелкните **Добавить корень**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63630-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="63630-153">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="63630-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="63630-154">В поле **Имя** введите "root".</span><span class="sxs-lookup"><span data-stu-id="63630-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="63630-155">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="63630-155">Click **OK**.</span></span>
6. <span data-ttu-id="63630-156">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63630-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="63630-157">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="63630-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="63630-158">В поле **Имя** введите "document".</span><span class="sxs-lookup"><span data-stu-id="63630-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="63630-159">В поле **Кратность** выберите **Один — много**.</span><span class="sxs-lookup"><span data-stu-id="63630-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="63630-160">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="63630-160">Click **OK**.</span></span>
11. <span data-ttu-id="63630-161">В дереве выберите **root\document**.</span><span class="sxs-lookup"><span data-stu-id="63630-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="63630-162">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63630-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="63630-163">В дереве выберите **XML\Атрибут**.</span><span class="sxs-lookup"><span data-stu-id="63630-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="63630-164">В поле **Имя** введите "id".</span><span class="sxs-lookup"><span data-stu-id="63630-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="63630-165">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="63630-165">Click **OK**.</span></span>
16. <span data-ttu-id="63630-166">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="63630-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="63630-167">Создание сопоставления форматов для сохранения проанализированных данных в модели данных</span><span class="sxs-lookup"><span data-stu-id="63630-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="63630-168">Щелкните **Сопоставить формат модели**.</span><span class="sxs-lookup"><span data-stu-id="63630-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="63630-169">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="63630-169">Click **New**.</span></span>
3.  <span data-ttu-id="63630-170">В поле **Определение** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="63630-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="63630-171">В поле **Имя** введите "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="63630-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="63630-172">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="63630-172">Click **Save**.</span></span>
6.  <span data-ttu-id="63630-173">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="63630-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="63630-174">В дереве разверните **format**.</span><span class="sxs-lookup"><span data-stu-id="63630-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="63630-175">В дереве разверните узел **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="63630-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="63630-176">В дереве выберите \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="63630-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="63630-177">(документ)\*\*.</span><span class="sxs-lookup"><span data-stu-id="63630-177">(document)\*\*.</span></span>
10. <span data-ttu-id="63630-178">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="63630-178">Click **Bind**.</span></span>
11. <span data-ttu-id="63630-179">В дереве разверните \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="63630-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="63630-180">(документ)\*\*.</span><span class="sxs-lookup"><span data-stu-id="63630-180">(document)\*\*.</span></span>
12. <span data-ttu-id="63630-181">В дереве выберите \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="63630-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="63630-182">(документ)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="63630-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="63630-183">В дереве разверните **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="63630-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="63630-184">В дереве выберите **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="63630-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="63630-185">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="63630-185">Click **Bind**.</span></span>
16. <span data-ttu-id="63630-186">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="63630-186">Click **Save**.</span></span>
17. <span data-ttu-id="63630-187">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="63630-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="63630-188">Запуск сопоставления формата</span><span class="sxs-lookup"><span data-stu-id="63630-188">Run format mapping</span></span>
1. <span data-ttu-id="63630-189">Щелкните **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="63630-189">Click **Run**.</span></span>
2. <span data-ttu-id="63630-190">Нажмите кнопку **Обзор** и выберите файл **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="63630-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="63630-191">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="63630-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="63630-192">Выбранный файл не был импортирован, поскольку структура формата предполагает существование атрибута "id" для элемента "document", но импортированный файл не содержит такого атрибута.</span><span class="sxs-lookup"><span data-stu-id="63630-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="63630-193">Изменение структуры формата, чтобы обрабатывать атрибут XML как необязательный</span><span class="sxs-lookup"><span data-stu-id="63630-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="63630-194">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="63630-194">Close the page.</span></span>
2. <span data-ttu-id="63630-195">В дереве разверните **root\document**.</span><span class="sxs-lookup"><span data-stu-id="63630-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="63630-196">В дереве выберите **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="63630-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="63630-197">В поле **Пустая строка для отсутствующего атрибута** выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="63630-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="63630-198">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="63630-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="63630-199">Запуск сопоставления форматов для проверки изменений</span><span class="sxs-lookup"><span data-stu-id="63630-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="63630-200">Щелкните **Сопоставить формат модели**.</span><span class="sxs-lookup"><span data-stu-id="63630-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="63630-201">Щелкните **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="63630-201">Click **Run**.</span></span>
3. <span data-ttu-id="63630-202">Нажмите кнопку **Обзор** и выберите файл **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="63630-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="63630-203">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="63630-203">Click **OK**.</span></span>
5. <span data-ttu-id="63630-204">Просмотрите сформированный файл.</span><span class="sxs-lookup"><span data-stu-id="63630-204">Review the generated file.</span></span> <span data-ttu-id="63630-205">Обратите внимание, что этот же файл, который был импортирован в качестве структуры формата, теперь считает атрибут "id" для элемента "document" необязательным.</span><span class="sxs-lookup"><span data-stu-id="63630-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
