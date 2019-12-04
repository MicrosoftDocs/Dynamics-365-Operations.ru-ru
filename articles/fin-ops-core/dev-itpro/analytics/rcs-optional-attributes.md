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
ms.openlocfilehash: 5e2989906c5aa3ead9e46b8ed5333e880e5cf1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769955"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="c879b-103">Импорт файлов в формате XML с дополнительными атрибутами</span><span class="sxs-lookup"><span data-stu-id="c879b-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="c879b-104">Можно разработать форматы электронной отчетности (ER) для синтаксического анализа входящих документов в формате XML.</span><span class="sxs-lookup"><span data-stu-id="c879b-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="c879b-105">Некоторые атрибуты элементов XML могут быть указаны в разработанном формате электронной отчетности как необязательные.</span><span class="sxs-lookup"><span data-stu-id="c879b-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="c879b-106">Это позволяет корректно обрабатывать входящие файлы с такими атрибутами XML и без них.</span><span class="sxs-lookup"><span data-stu-id="c879b-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="c879b-107">Затем можно использовать содержимое из этих файлов для обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="c879b-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="c879b-108">Чтобы получить дополнительные сведения об этой функции, выполните действия, указанные в теме [(RCS) Импорт файлов в формате XML с дополнительными атрибутами](tasks/import-files-xml-format-optional-attributes.md), которая являются частью бизнес-процесса 7.5.4.3 Приобретение/разработка компонентов ИТ-услуг и решений (10677).</span><span class="sxs-lookup"><span data-stu-id="c879b-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="c879b-109">Этот проводник по задаче и его демонстрационные файлы можно загрузить из [центра загрузки Майкрософт](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="c879b-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="c879b-110">Описание содержания</span><span class="sxs-lookup"><span data-stu-id="c879b-110">Content description</span></span>       | <span data-ttu-id="c879b-111">Хранилище файлов</span><span class="sxs-lookup"><span data-stu-id="c879b-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c879b-112">Образец файла в формате XML</span><span class="sxs-lookup"><span data-stu-id="c879b-112">Sample file in XML format</span></span> | <span data-ttu-id="c879b-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="c879b-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="c879b-114">руководство по задаче</span><span class="sxs-lookup"><span data-stu-id="c879b-114">Task guide</span></span>                | <span data-ttu-id="c879b-115">RCS Импорт файлов в формате XML с дополнительными атрибутами.axtr</span><span class="sxs-lookup"><span data-stu-id="c879b-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="c879b-116">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может разработать конфигурацию формата ER для импорта файлов в формате XML, содержащих необязательные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="c879b-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="c879b-117">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре [Создание поставщиков конфигурации и установка их в качестве активных](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="c879b-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="c879b-118">Перед началом загрузите и локально сохраните файл IncomingDocumentToLearnHowToHandleOptionalAttributes.xml из центра загрузки Майкрософт (https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="c879b-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="c879b-119">Перейдите в раздел **Управление организацией** > **Рабочие области** > **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="c879b-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="c879b-120">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="c879b-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="c879b-121">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в теме [Создание поставщиков конфигурации и пометка их как активных](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="c879b-121">If you don’t see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="c879b-122">Щелкните **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="c879b-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="c879b-123">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="c879b-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="c879b-124">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c879b-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="c879b-125">В поле **Имя** введите "Модель для импорта XML-файла".</span><span class="sxs-lookup"><span data-stu-id="c879b-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="c879b-126">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="c879b-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="c879b-127">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="c879b-127">Click **Designer**.</span></span>
5. <span data-ttu-id="c879b-128">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c879b-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="c879b-129">В поле **Имя** введите "Root".</span><span class="sxs-lookup"><span data-stu-id="c879b-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="c879b-130">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="c879b-130">Click **Add**.</span></span>
8. <span data-ttu-id="c879b-131">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c879b-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="c879b-132">В поле **Имя** введите "List".</span><span class="sxs-lookup"><span data-stu-id="c879b-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="c879b-133">В поле **Тип элемента** выберите **Список записей**.</span><span class="sxs-lookup"><span data-stu-id="c879b-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="c879b-134">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="c879b-134">Click **Add**.</span></span>
12. <span data-ttu-id="c879b-135">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c879b-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="c879b-136">В поле **Имя** введите "Code".</span><span class="sxs-lookup"><span data-stu-id="c879b-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="c879b-137">В поле **Тип элемента** выберите **Строка**.</span><span class="sxs-lookup"><span data-stu-id="c879b-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="c879b-138">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="c879b-138">Click **Add**.</span></span>
16. <span data-ttu-id="c879b-139">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c879b-139">Click **Save**.</span></span>
17. <span data-ttu-id="c879b-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c879b-140">Close the page.</span></span>
18. <span data-ttu-id="c879b-141">Щелкните **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="c879b-141">Click **Change status**.</span></span>
19. <span data-ttu-id="c879b-142">Щелкните **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="c879b-142">Click **Complete**.</span></span>
20. <span data-ttu-id="c879b-143">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="c879b-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="c879b-144">Создание формата для импорта данных</span><span class="sxs-lookup"><span data-stu-id="c879b-144">Create a format for data import</span></span>
1. <span data-ttu-id="c879b-145">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c879b-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="c879b-146">В поле **Создать** введите "Формат, основанный на модели данных «Модель для импорта XML-файла»".</span><span class="sxs-lookup"><span data-stu-id="c879b-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="c879b-147">В поле **Имя** введите "Формат для импорта XML-файла".</span><span class="sxs-lookup"><span data-stu-id="c879b-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="c879b-148">Выберите **Да** в поле **Поддерживает импорт данных**.</span><span class="sxs-lookup"><span data-stu-id="c879b-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="c879b-149">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="c879b-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="c879b-150">Создание формата для разбора входящего файла в формате XML</span><span class="sxs-lookup"><span data-stu-id="c879b-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="c879b-151">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="c879b-151">Click **Designer**.</span></span>
2. <span data-ttu-id="c879b-152">Щелкните **Добавить корень**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c879b-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="c879b-153">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="c879b-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="c879b-154">В поле **Имя** введите "root".</span><span class="sxs-lookup"><span data-stu-id="c879b-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="c879b-155">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="c879b-155">Click **OK**.</span></span>
6. <span data-ttu-id="c879b-156">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c879b-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="c879b-157">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="c879b-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="c879b-158">В поле **Имя** введите "document".</span><span class="sxs-lookup"><span data-stu-id="c879b-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="c879b-159">В поле **Кратность** выберите **Один — много**.</span><span class="sxs-lookup"><span data-stu-id="c879b-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="c879b-160">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="c879b-160">Click **OK**.</span></span>
11. <span data-ttu-id="c879b-161">В дереве выберите **root\document**.</span><span class="sxs-lookup"><span data-stu-id="c879b-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="c879b-162">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c879b-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="c879b-163">В дереве выберите **XML\Атрибут**.</span><span class="sxs-lookup"><span data-stu-id="c879b-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="c879b-164">В поле **Имя** введите "id".</span><span class="sxs-lookup"><span data-stu-id="c879b-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="c879b-165">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="c879b-165">Click **OK**.</span></span>
16. <span data-ttu-id="c879b-166">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c879b-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="c879b-167">Создание сопоставления форматов для сохранения проанализированных данных в модели данных</span><span class="sxs-lookup"><span data-stu-id="c879b-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="c879b-168">Щелкните **Сопоставить формат модели**.</span><span class="sxs-lookup"><span data-stu-id="c879b-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="c879b-169">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c879b-169">Click **New**.</span></span>
3.  <span data-ttu-id="c879b-170">В поле **Определение** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c879b-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="c879b-171">В поле **Имя** введите "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="c879b-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="c879b-172">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c879b-172">Click **Save**.</span></span>
6.  <span data-ttu-id="c879b-173">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="c879b-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="c879b-174">В дереве разверните **format**.</span><span class="sxs-lookup"><span data-stu-id="c879b-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="c879b-175">В дереве разверните узел **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="c879b-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="c879b-176">В дереве выберите \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="c879b-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="c879b-177">(документ)\*\*.</span><span class="sxs-lookup"><span data-stu-id="c879b-177">(document)\*\*.</span></span>
10. <span data-ttu-id="c879b-178">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="c879b-178">Click **Bind**.</span></span>
11. <span data-ttu-id="c879b-179">В дереве разверните \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="c879b-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="c879b-180">(документ)\*\*.</span><span class="sxs-lookup"><span data-stu-id="c879b-180">(document)\*\*.</span></span>
12. <span data-ttu-id="c879b-181">В дереве выберите \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="c879b-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="c879b-182">(документ)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="c879b-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="c879b-183">В дереве разверните **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="c879b-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="c879b-184">В дереве выберите **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="c879b-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="c879b-185">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="c879b-185">Click **Bind**.</span></span>
16. <span data-ttu-id="c879b-186">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c879b-186">Click **Save**.</span></span>
17. <span data-ttu-id="c879b-187">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c879b-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="c879b-188">Запуск сопоставления формата</span><span class="sxs-lookup"><span data-stu-id="c879b-188">Run format mapping</span></span>
1. <span data-ttu-id="c879b-189">Щелкните **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="c879b-189">Click **Run**.</span></span>
2. <span data-ttu-id="c879b-190">Нажмите кнопку **Обзор** и выберите файл **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="c879b-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="c879b-191">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="c879b-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="c879b-192">Выбранный файл не был импортирован, поскольку структура формата предполагает существование атрибута "id" для элемента "document", но импортированный файл не содержит такого атрибута.</span><span class="sxs-lookup"><span data-stu-id="c879b-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="c879b-193">Изменение структуры формата, чтобы обрабатывать атрибут XML как необязательный</span><span class="sxs-lookup"><span data-stu-id="c879b-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="c879b-194">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c879b-194">Close the page.</span></span>
2. <span data-ttu-id="c879b-195">В дереве разверните **root\document**.</span><span class="sxs-lookup"><span data-stu-id="c879b-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="c879b-196">В дереве выберите **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="c879b-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="c879b-197">В поле **Пустая строка для отсутствующего атрибута** выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="c879b-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="c879b-198">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c879b-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="c879b-199">Запуск сопоставления форматов для проверки изменений</span><span class="sxs-lookup"><span data-stu-id="c879b-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="c879b-200">Щелкните **Сопоставить формат модели**.</span><span class="sxs-lookup"><span data-stu-id="c879b-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="c879b-201">Щелкните **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="c879b-201">Click **Run**.</span></span>
3. <span data-ttu-id="c879b-202">Нажмите кнопку **Обзор** и выберите файл **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="c879b-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="c879b-203">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="c879b-203">Click **OK**.</span></span>
5. <span data-ttu-id="c879b-204">Просмотрите сформированный файл.</span><span class="sxs-lookup"><span data-stu-id="c879b-204">Review the generated file.</span></span> <span data-ttu-id="c879b-205">Обратите внимание, что этот же файл, который был импортирован в качестве структуры формата, теперь считает атрибут "id" для элемента "document" необязательным.</span><span class="sxs-lookup"><span data-stu-id="c879b-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
