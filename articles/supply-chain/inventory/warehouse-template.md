---
title: "Настройка склада с помощью шаблона конфигурации склада"
description: "В этом разделе рассматривается настройка склада с помощью шаблона конфигурации склада."
author: perlynne
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0b54e7f6f4b0dfb994d271aaeb547e27bf03e294
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a><span data-ttu-id="2fed1-103">Настройка склада с помощью шаблона конфигурации склада</span><span class="sxs-lookup"><span data-stu-id="2fed1-103">Set up a warehouse by using a warehouse configuration template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2fed1-104">В этом разделе рассматривается настройка склада с помощью шаблона конфигурации склада.</span><span class="sxs-lookup"><span data-stu-id="2fed1-104">This topic explains how to set up a warehouse by using a warehouse configuration template.</span></span> <span data-ttu-id="2fed1-105">Существует несколько предварительно заданных шаблонов конфигурации, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="2fed1-105">There are several predefined configuration templates that you can use.</span></span> <span data-ttu-id="2fed1-106">Сведения об использовании этих шаблонов см. в разделе [Шаблоны конфигурационных данных](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="2fed1-106">For information about how to use these templates, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a><span data-ttu-id="2fed1-107">Сценарии, где могут быть полезными шаблоны конфигурации</span><span class="sxs-lookup"><span data-stu-id="2fed1-107">Scenarios where configuration templates can be helpful</span></span>

<span data-ttu-id="2fed1-108">Шаблоны конфигурации могут быть полезными во многих сценариях.</span><span class="sxs-lookup"><span data-stu-id="2fed1-108">Configuration templates can be helpful in many scenarios.</span></span> <span data-ttu-id="2fed1-109">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="2fed1-109">Here are some examples:</span></span>

- <span data-ttu-id="2fed1-110">Вы завершили и проверили настройку конфигурации в тестовой среде и теперь хотите скопировать настройку в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="2fed1-110">You've completed and tested a configuration setup in a test environment, and you now want to copy the setup to a production environment.</span></span>
- <span data-ttu-id="2fed1-111">Вы хотите развернуть настройку склада в нескольких юридических лицах или создать новый склад в том же юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="2fed1-111">You want to roll the warehouse setup out to several legal entities or create a new warehouse in the same legal entity.</span></span>
- <span data-ttu-id="2fed1-112">Требуется быстро подготовиться для демонстрации функций склада.</span><span class="sxs-lookup"><span data-stu-id="2fed1-112">You want to quickly prepare for a demo of the warehouse functionality.</span></span>
- <span data-ttu-id="2fed1-113">Требуется, чтобы существующие номенклатуры и склады использовали функциональные возможности модуля управления складом вместо функциональных возможностей управления запасами.</span><span class="sxs-lookup"><span data-stu-id="2fed1-113">You want existing items and warehouses to use the functionality in Warehouse management instead of the functionality in Inventory management.</span></span>

<span data-ttu-id="2fed1-114">В этом разделе рассматриваются первые два из этих сценариев.</span><span class="sxs-lookup"><span data-stu-id="2fed1-114">This topic focuses on the first of these scenarios.</span></span> <span data-ttu-id="2fed1-115">В нем показано, как можно использовать шаблон конфигурации для копирования настроек конфигурации из тестовой среды в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="2fed1-115">It shows how you can use a configuration template to copy a configuration setup from a test environment to a production environment.</span></span>

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a><span data-ttu-id="2fed1-116">Копирование настройки конфигурации из тестовой среды в производственную среду</span><span class="sxs-lookup"><span data-stu-id="2fed1-116">Copy a configuration setup from a test environment to a production environment</span></span>

<span data-ttu-id="2fed1-117">В этом сценарии настройка конфигурации для склада и некоторых процессов проводки уже существует в тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="2fed1-117">For this scenario, the configuration setup for a warehouse and some transaction processes already exist in a test environment.</span></span> <span data-ttu-id="2fed1-118">Теперь требуется скопировать настройку конфигурации для склада из тестовой среды в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="2fed1-118">You now want to copy the configuration setup for the warehouse from the test environment to a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="2fed1-119">Важно, чтобы при копировании настройки конфигурации были включены другие связанные данные настройки.</span><span class="sxs-lookup"><span data-stu-id="2fed1-119">It's important that you include other related setup data when you copy a configuration setup.</span></span> <span data-ttu-id="2fed1-120">Например, необходимо настроить продукты путем копирования настройки из тестовой среды.</span><span class="sxs-lookup"><span data-stu-id="2fed1-120">For example, you want to set up products by copying the setup from a test environment.</span></span> <span data-ttu-id="2fed1-121">Однако вы не можете настроить фиксированные ячейки комплектации для продукта до создания этого продукта.</span><span class="sxs-lookup"><span data-stu-id="2fed1-121">However, you can't set up a fixed picking location for a product before that product is created.</span></span> <span data-ttu-id="2fed1-122">Хотя отдельные шаблоны конфигурации не поддерживают этот тип зависимости, существуют шаблоны данных по умолчанию, которые его поддерживают.</span><span class="sxs-lookup"><span data-stu-id="2fed1-122">Although individual configuration templates don't support this type of dependency, there are default data templates that support it.</span></span> <span data-ttu-id="2fed1-123">Можно легко включить эти шаблоны данных по умолчанию в процесс настройки конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2fed1-123">You can easily include these default data templates in a configuration process.</span></span>

### <a name="export-a-default-warehouse-template"></a><span data-ttu-id="2fed1-124">Экспорт шаблона склада по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2fed1-124">Export a default warehouse template</span></span> 

1. <span data-ttu-id="2fed1-125">Откройте рабочую область **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="2fed1-125">Open the **Data management** workspace.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2fed1-126">При использовании этой рабочей области в первый раз необходимо загрузить все информационные объекты перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="2fed1-126">If you're using this workspace for the first time, you must load all the data entities before you continue.</span></span>

2. <span data-ttu-id="2fed1-127">Выберите плитку **Шаблоны**, затем выберите **Загрузить шаблоны по умолчанию** для загрузки шаблонов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2fed1-127">Select the **Templates** tile, and then select **Load default templates** to load the default templates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2fed1-128">Пункт **Загрузить шаблоны по умолчанию** доступен только в представлении **Расширенное**.</span><span class="sxs-lookup"><span data-stu-id="2fed1-128">**Load default templates** is available only in the **Enhanced** view.</span></span> <span data-ttu-id="2fed1-129">Выберите **Параметры структуры**, затем в поле **Просмотр значений по умолчанию** выберите **Расширенное представление**.</span><span class="sxs-lookup"><span data-stu-id="2fed1-129">Select **Framework parameters**, and then, in the **View defaults** field, select **Enhanced view**.</span></span>

3. <span data-ttu-id="2fed1-130">После загрузки шаблонов по умолчанию их можно изменить, чтобы они соответствовали требованиям бизнеса.</span><span class="sxs-lookup"><span data-stu-id="2fed1-130">After the default templates are loaded, you can change them so that they meet your business requirements.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2fed1-131">Для загрузки шаблонов по умолчанию и импорта шаблонов необходимо иметь доступ администратора системы.</span><span class="sxs-lookup"><span data-stu-id="2fed1-131">To load default templates and import templates, you must have system administrator access.</span></span> <span data-ttu-id="2fed1-132">Это требование гарантирует, что все объекты правильно загружены в шаблон.</span><span class="sxs-lookup"><span data-stu-id="2fed1-132">This requirement helps guarantee that all entities are correctly loaded into the template.</span></span>

4. <span data-ttu-id="2fed1-133">Убедитесь, что вы находитесь в юридическом лице, из которого требуется экспортировать относящиеся к компании данные.</span><span class="sxs-lookup"><span data-stu-id="2fed1-133">Make sure that you're in the legal entity that you want to export the company-specific data from.</span></span>
5. <span data-ttu-id="2fed1-134">В рабочей области выберите **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="2fed1-134">In the workspace, select **Export**.</span></span>
6. <span data-ttu-id="2fed1-135">Создайте новый проект экспорта.</span><span class="sxs-lookup"><span data-stu-id="2fed1-135">Create a new export project.</span></span>
7. <span data-ttu-id="2fed1-136">Выберите **+ Добавить шаблон** и найдите шаблон склада по умолчанию **400 - WMS**.</span><span class="sxs-lookup"><span data-stu-id="2fed1-136">Select **+ Add template**, and find the **400 - WMS** default warehouse template.</span></span> <span data-ttu-id="2fed1-137">Этот шаблон добавляет информационные объекты в конфигурацию склада.</span><span class="sxs-lookup"><span data-stu-id="2fed1-137">This template adds data entities for warehouse configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2fed1-138">Если требуется фильтрация экспортируемых данных (например, требуется экспортировать только данные, относящиеся к определенному складу), необходимо оценить каждый информационный объект и добавить фильтрацию через запрос.</span><span class="sxs-lookup"><span data-stu-id="2fed1-138">If the data that you're exporting must be filtered (for example, you want to export only the data that is related to a specific warehouse), you must evaluate each data entity and add filtering via a query.</span></span> <span data-ttu-id="2fed1-139">Можно также экспортировать все данные, а затем удалить записи, которые не требуются в конечных файлах.</span><span class="sxs-lookup"><span data-stu-id="2fed1-139">Alternatively, you can export all data and then delete the records that aren't required in the destination files.</span></span>

8. <span data-ttu-id="2fed1-140">Выберите **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="2fed1-140">Select **Export**.</span></span> <span data-ttu-id="2fed1-141">Экспортируются данные, связанные связаны со всеми информационными объектами в проекте.</span><span class="sxs-lookup"><span data-stu-id="2fed1-141">Data that is related to all the data entities in the project is exported.</span></span>

<span data-ttu-id="2fed1-142">Можно загрузить файл ZIP для пакета данных.</span><span class="sxs-lookup"><span data-stu-id="2fed1-142">You can download a zip file for the data package.</span></span> <span data-ttu-id="2fed1-143">Этот файл содержит все данные в выбранном формате (например, формат Excel).</span><span class="sxs-lookup"><span data-stu-id="2fed1-143">This file contains all the data in the selected format (for example, Excel format).</span></span> <span data-ttu-id="2fed1-144">Как было указано, некоторые записи в файлах пакетов данных могут потребовать обновления, прежде чем их можно будет импортировать в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="2fed1-144">As has been mentioned, some records in the data package files might have to be updated before you can import them into the production environment.</span></span> <span data-ttu-id="2fed1-145">При обновлении записи убедитесь в том, что вы не изменили имя файла.</span><span class="sxs-lookup"><span data-stu-id="2fed1-145">If you update a record, make sure that you don't change the file name.</span></span>

### <a name="import-a-warehouse-configuration-setup"></a><span data-ttu-id="2fed1-146">Импорт настройки конфигурации склада</span><span class="sxs-lookup"><span data-stu-id="2fed1-146">Import a warehouse configuration setup</span></span>

1. <span data-ttu-id="2fed1-147">В конечной среде убедитесь, что вы находитесь в компании, в которую необходимо импортировать данные склада.</span><span class="sxs-lookup"><span data-stu-id="2fed1-147">In the destination environment, make sure that you're in the company that you want to import the warehouse data into.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2fed1-148">Перед выполнением импорта необходимо определить все зависимости данных.</span><span class="sxs-lookup"><span data-stu-id="2fed1-148">Before you do the import, you should identify any data dependencies.</span></span> <span data-ttu-id="2fed1-149">Например, шаблон **Управление складом** включает в себя информационный объект, который называется **Коды обработки склада**.</span><span class="sxs-lookup"><span data-stu-id="2fed1-149">For example, the **Warehouse management** template includes a data entity that is named **Warehouse disposition codes**.</span></span> <span data-ttu-id="2fed1-150">Этот объект содержит данные, относящиеся к странице настройки **Коды метода обработки** (**Управление складом** > **Настройка** > **Мобильное устройство** > **Коды метода обработки**).</span><span class="sxs-lookup"><span data-stu-id="2fed1-150">This entity contains data that is related to the **Disposition codes** setup page (**Warehouse management** > **Setup** > **Mobile device** > **Disposition codes**).</span></span> <span data-ttu-id="2fed1-151">Если имеющаяся настройка уже обрабатывает процесс возврата для заказов на продажу, поле **Код метода обработки возврата** содержит значение.</span><span class="sxs-lookup"><span data-stu-id="2fed1-151">If an existing setup already handles the return process for sales orders, the **Return disposition code** field contains a value.</span></span> <span data-ttu-id="2fed1-152">Код метода обработки в этом поле относится к информационному объекту **Код метода обработки**, который входит в состав шаблона **Продажи и маркетинг**.</span><span class="sxs-lookup"><span data-stu-id="2fed1-152">The disposition code in this field is related to the **Disposition code** data entity, which is part of the **Sales and marketing** template.</span></span> <span data-ttu-id="2fed1-153">Если данные из информационного объекта **Код метода обработки** не будут импортированы перед данными из поля **Коды методов обработки склада**, произойдет сбой процесса импорта.</span><span class="sxs-lookup"><span data-stu-id="2fed1-153">If the data from the **Disposition code** data entity isn't imported before the data from the **Warehouse disposition codes** field, the import will fail.</span></span>

2. <span data-ttu-id="2fed1-154">В рабочей области **Управление данными** выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="2fed1-154">In the **Data management** workspace, select **Import**.</span></span>
3. <span data-ttu-id="2fed1-155">Создать новый проект импорта.</span><span class="sxs-lookup"><span data-stu-id="2fed1-155">Create a new import project.</span></span>
4. <span data-ttu-id="2fed1-156">Выберите **+ Добавить файл** и отправьте ZIP-файл для пакета данных.</span><span class="sxs-lookup"><span data-stu-id="2fed1-156">Select **+ Add file**, and upload the zip file for the data package.</span></span>
5. <span data-ttu-id="2fed1-157">Выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="2fed1-157">Select **Import**.</span></span> <span data-ttu-id="2fed1-158">В представлении **Расширенное** можно использовать параметр **Фильтр** для быстрого получения обзора проблем, которые могут возникнуть во время импорта.</span><span class="sxs-lookup"><span data-stu-id="2fed1-158">In the **Enhanced** view, you can use the **Filter** option to quickly get an overview of issues that might occur during the import.</span></span>

<span data-ttu-id="2fed1-159">Журнал **Просмотр выполнения** содержит подробные сведения о каждом импортированном информационном объекте.</span><span class="sxs-lookup"><span data-stu-id="2fed1-159">The **View execution** log provides detailed information about each data entity that is imported.</span></span> <span data-ttu-id="2fed1-160">Можно использовать представление промежуточного хранения данных для быстрого перехода к целевым данным.</span><span class="sxs-lookup"><span data-stu-id="2fed1-160">You can use the staging data view to quickly get to the target data.</span></span> <span data-ttu-id="2fed1-161">Таким образом можно просмотреть, как выглядят импортированные данные на соответствующих страницах в приложении.</span><span class="sxs-lookup"><span data-stu-id="2fed1-161">In this way, you can see what the imported data looks like on the related pages in the application.</span></span> <span data-ttu-id="2fed1-162">При использовании шаблонов данных по умолчанию последовательность импорта для каждого информационного объекта работает заранее определенным образом, помогая гарантировать, что все зависимые данные импортируются сначала.</span><span class="sxs-lookup"><span data-stu-id="2fed1-162">When you use the default data templates, the import sequence for each data entity works in the predefined manner, to help guarantee that all dependent data is imported first.</span></span> <span data-ttu-id="2fed1-163">Если проект содержит пользовательские информационные объекты, необходимо убедиться, что определена правильная последовательность.</span><span class="sxs-lookup"><span data-stu-id="2fed1-163">If custom data entities are part of the project, you must make sure that the correct sequence is defined.</span></span> <span data-ttu-id="2fed1-164">Дополнительные сведения см. в разделе [Шаблоны конфигурационных данных](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="2fed1-164">For more information, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

<span data-ttu-id="2fed1-165">Для получения дополнительных сведений об использовании складского шаблона для копирования конфигурации склада из одной организации в новую организацию в это же экземпляре см. 3-минутное видео на YouTube.</span><span class="sxs-lookup"><span data-stu-id="2fed1-165">To learn more about how to use warehouse template to copy the configuration of a warehouse from one company to a new company within the same instance, see this 3-minute video on YouTube.</span></span>

> [!Video https://www.youtube.com/embed/K2WIfFlqJYs]


## <a name="related-topic"></a><span data-ttu-id="2fed1-166">Связанные раздел</span><span class="sxs-lookup"><span data-stu-id="2fed1-166">Related topic</span></span>

[<span data-ttu-id="2fed1-167">Шаблоны данных о конфигурации</span><span class="sxs-lookup"><span data-stu-id="2fed1-167">Configuration data templates</span></span>](../../dev-itpro/data-entities/configuration-data-templates.md)

