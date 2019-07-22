---
title: Подготовка метаданных для конкретного приложения для RCS и ER
description: В этом разделе описана процедура подготовки метаданных конкретного приложения для службы Regulatory Configuration Service (RCS) и электронной отчетности (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 289f901501a68319c9d85e993d8dfbfc3838a8eb
ms.sourcegitcommit: d940c7892b6caa6141b3bda8abf1c56e9df4687a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726440"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a><span data-ttu-id="d2f57-103">Подготовка метаданных для конкретного приложения для RCS</span><span class="sxs-lookup"><span data-stu-id="d2f57-103">Prepare application-specific metadata for RCS</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d2f57-104">В этом разделе рассматриваются примеры пошагового выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="d2f57-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="d2f57-105">Подготовка метаданных приложения, которые могут использоваться в RCS</span><span class="sxs-lookup"><span data-stu-id="d2f57-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="d2f57-106">Доступ к метаданным приложения с помощью конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="d2f57-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="d2f57-107">Доступ к метаданным приложения с помощью подключенных приложений</span><span class="sxs-lookup"><span data-stu-id="d2f57-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="d2f57-108">Подготовка метаданных приложения, которые могут использоваться в RCS</span><span class="sxs-lookup"><span data-stu-id="d2f57-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="d2f57-109">Следующая процедура показывает, как пользователь Finance and Operations, имеющий роль **Системный администратор** или **Разработчик электронной отчетности**, может создать конфигурацию электронной отчетности (ER), которая содержит метаданные для приложения Microsoft Dynamics 365 for Finance and Operations и которая используется для разработки конфигураций сопоставления модели ER в службе Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="d2f57-109">The following procedure shows how a user of Finance and Operations who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the Microsoft Dynamics 365 for Finance and Operations application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="d2f57-110">Образец конфигурации сопоставления модели ER, созданный в этом примере, будет использоваться для доступа к проводкам внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="d2f57-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="d2f57-111">В этом примере необходимо использовать RCS для создания решения ER для Finance and Operations, которое будет использоваться для создания электронных документов, содержащих информацию из бизнес-домена зарубежной торговли.</span><span class="sxs-lookup"><span data-stu-id="d2f57-111">For this example, you want to use RCS to design an ER solution for Finance and Operations that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="d2f57-112">Чтобы указать сопоставление модели данных ER с источниками необходимых данных, необходимо иметь доступ к метаданным приложения для Finance and Operations в RCS.</span><span class="sxs-lookup"><span data-stu-id="d2f57-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata for Finance and Operations in RCS.</span></span> <span data-ttu-id="d2f57-113">Таким образом, в ходе процесса разработки решения ER необходимо настроить новую конфигурацию метаданных ER, которая содержит все текущие необходимые метаданные для создания отчетов ER для выбранного бизнес-домена.</span><span class="sxs-lookup"><span data-stu-id="d2f57-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="d2f57-114">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="d2f57-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="d2f57-115">Перейдите в раздел **Управление организацией \> Рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="d2f57-116">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="d2f57-117">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре [Создание поставщика конфигурации и пометка его как активного](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d2f57-117">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="d2f57-118">Выберите **Конфигурации метаданных**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="d2f57-119">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="d2f57-120">В диалоговом окне в раскрывающемся списке в поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="d2f57-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="d2f57-121">В данном примере введите **Метаданные внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="d2f57-122">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="d2f57-123">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-123">Select **Designer**.</span></span>
8. <span data-ttu-id="d2f57-124">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2f57-125">Можно выбрать все метаданные либо для всего приложения, либо для выбранных моделей или модулей.</span><span class="sxs-lookup"><span data-stu-id="d2f57-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="d2f57-126">В обоих случаях следует иметь в виду, что следующие метаданные будут автоматически добавлены: таблицы записей, перечисления и расширенные типы данных (EDT).</span><span class="sxs-lookup"><span data-stu-id="d2f57-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="d2f57-127">Когда требуются дополнительные типы метаданных, они должны быть добавлены вручную.</span><span class="sxs-lookup"><span data-stu-id="d2f57-127">When additional types of metadata are required, they must be manually added.</span></span>

<span data-ttu-id="d2f57-128">Необходимо добавить некоторые метаданные, которые относятся к проводкам внешней торговли, и вручную выбрать элементы метаданных.</span><span class="sxs-lookup"><span data-stu-id="d2f57-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="d2f57-129">Выберите **Добавить источник данных \> Записи таблицы**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="d2f57-130">Выполните фильтрацию по значению **Интрастат** в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="d2f57-131">Выберите запись таблицы **Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="d2f57-132">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-132">Select **OK**.</span></span>

<span data-ttu-id="d2f57-133">Необходимо добавить сведения метаданных о записях таблицы Интрастат</span><span class="sxs-lookup"><span data-stu-id="d2f57-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="d2f57-134">В дереве выберите **Таблицы записей Интрастат \> \>Отношения \> IntrastatCommodity (записи таблицы EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="d2f57-135">Выберите **Добавить метаданные**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2f57-136">Метаданные о необходимых отношениях для выбранной таблицы записей необходимо добавить вручную.</span><span class="sxs-lookup"><span data-stu-id="d2f57-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="d2f57-137">Выберите **Добавить источник данных**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="d2f57-138">Выберите **Перечисление**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="d2f57-139">Выполните фильтрацию по значению **IntrastatDirection** в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="d2f57-140">Выберите запись перечисления **IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="d2f57-141">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-141">Select **OK**.</span></span>
20. <span data-ttu-id="d2f57-142">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-142">Select **Save**.</span></span>
21. <span data-ttu-id="d2f57-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d2f57-143">Close the page.</span></span>
22. <span data-ttu-id="d2f57-144">Завершите черновую версию конфигурации метаданных:</span><span class="sxs-lookup"><span data-stu-id="d2f57-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="d2f57-145">Выберите **Изменить статус \> Завершено**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="d2f57-146">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-146">Select **OK**.</span></span>
    3. <span data-ttu-id="d2f57-147">Выберите завершенную версию 1.</span><span class="sxs-lookup"><span data-stu-id="d2f57-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="d2f57-148">Экспортируйте завершенную версию конфигурации метаданных из приложения в виде файла XML:</span><span class="sxs-lookup"><span data-stu-id="d2f57-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="d2f57-149">Выберите **Обменять \> Экспорт в виде XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="d2f57-150">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-150">Select **OK**.</span></span>

<span data-ttu-id="d2f57-151">Созданная конфигурация метаданных ER будет сохранена в виде файла **Метаданные внешней торговли.xml**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="d2f57-152">Теперь можно импортировать его в RCS, чтобы его можно было использовать в качестве источника метаданных для бизнес-домена внешней торговли в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d2f57-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain in Finance and Operations.</span></span> <span data-ttu-id="d2f57-153">На основе этих сведений можно указать сопоставление между метаданными приложения и моделью данных ER.</span><span class="sxs-lookup"><span data-stu-id="d2f57-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="d2f57-154">Доступ к метаданным приложения с помощью конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="d2f57-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="d2f57-155">Следующая процедура показывает, как пользователь RCS, имеющий роль **Системный администратор** или **Разработчик электронной отчетности**, может разработать новое сопоставление модели ER с помощью метаданных из приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d2f57-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the Finance and Operations application.</span></span> <span data-ttu-id="d2f57-156">Доступ к метаданным приложения будет осуществляться с помощью конфигурации метаданных ER, которая содержит образец набора метаданных для доступа к проводкам внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="d2f57-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="d2f57-157">Перед окончанием выполнения этой процедуры необходимо сначала выполнить следующие процедуры:</span><span class="sxs-lookup"><span data-stu-id="d2f57-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="d2f57-158">Создание поставщика конфигурации и пометка его как активного</span><span class="sxs-lookup"><span data-stu-id="d2f57-158">Create a configuration provider and mark it as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="d2f57-159">Подготовка метаданных приложения, которые могут использоваться в RCS</span><span class="sxs-lookup"><span data-stu-id="d2f57-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="d2f57-160">Перейдите в раздел **Все рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="d2f57-161">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="d2f57-162">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре [Создание поставщика конфигурации и пометка его как активного](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d2f57-162">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="d2f57-163">Импортируйте конфигурацию метаданных ER, которая содержит метаданные для приложения Finance and Operations и настроена для создания электронных документов для бизнес-домена внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="d2f57-163">Import the ER metadata configuration that contains metadata for the Finance and Operations application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="d2f57-164">Вы создали конфигурацию метаданных ER и экспортировали ее как XML-файл в процедуре [Подготовка метаданных приложения, которые могут использоваться в RCS](#prepare-application-metadata-that-can-be-used-in-rcs) ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d2f57-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="d2f57-165">Выберите **Конфигурации метаданных**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="d2f57-166">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="d2f57-167">Выберите **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="d2f57-168">Найдите и выберите файл **Метаданные внешней торговли.xml**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="d2f57-169">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-169">Select **OK**.</span></span>
    6. <span data-ttu-id="d2f57-170">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d2f57-170">Close the page.</span></span>

4. <span data-ttu-id="d2f57-171">Создание конфигурации модели данных:</span><span class="sxs-lookup"><span data-stu-id="d2f57-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="d2f57-172">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="d2f57-173">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="d2f57-174">В диалоговом окне в раскрывающемся списке в поле **Имя** введите **Модель внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="d2f57-175">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="d2f57-176">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="d2f57-177">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d2f57-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="d2f57-178">В поле **Имя** введите **Корень**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="d2f57-179">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="d2f57-180">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d2f57-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="d2f57-181">В поле **Имя** введите **Проводка**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="d2f57-182">В поле **Тип элемента** выберите **Список записей**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="d2f57-183">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="d2f57-184">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d2f57-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="d2f57-185">В поле **Имя** введите **Код товара**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="d2f57-186">В поле **Тип элемента** выберите **Строка**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="d2f57-187">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-187">Select **Add**.</span></span>

    9. <span data-ttu-id="d2f57-188">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d2f57-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="d2f57-189">В поле "Имя" введите **Сумма, выставленная по накладным**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="d2f57-190">В поле **Тип элемента** выберите **Вещественный**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="d2f57-191">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-191">Select **Add**.</span></span>

    10. <span data-ttu-id="d2f57-192">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d2f57-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="d2f57-193">В поле **Имя** введите **Дата**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="d2f57-194">В поле **Тип элемента** выберите **Дата**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="d2f57-195">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="d2f57-196">Выберите **Добавить \> Корневая ссылка**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="d2f57-197">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-197">Select **OK**.</span></span>
    13. <span data-ttu-id="d2f57-198">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-198">Select **Save**.</span></span>
    14. <span data-ttu-id="d2f57-199">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d2f57-199">Close the page.</span></span>
    15. <span data-ttu-id="d2f57-200">Выберите **Изменить статус \> Завершено**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="d2f57-201">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-201">Select **OK**.</span></span>

5. <span data-ttu-id="d2f57-202">Создайте конфигурацию сопоставления модели:</span><span class="sxs-lookup"><span data-stu-id="d2f57-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="d2f57-203">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="d2f57-204">В раскрывающемся диалоговом окне в полей **Создать** введите **Сопоставление модели на основе модели данных внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="d2f57-205">В поле **Имя** введите **Сопоставление внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="d2f57-206">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="d2f57-207">На экспресс-вкладке **Необходимые условия** выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="d2f57-208">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-208">Select **New**.</span></span>
    7. <span data-ttu-id="d2f57-209">В поле **Тип необходимого компонента** выберите **Конфигурация**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="d2f57-210">Выберите конфигурацию **Метаданные внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="d2f57-211">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-211">Select **Save**.</span></span> <span data-ttu-id="d2f57-212">Обратите внимание, что ссылка добавляется к версии 1 конфигурации **Метаданные внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="d2f57-213">Метаданные приложения из этой конфигурации будут предлагаться при разработке сопоставления моделей.</span><span class="sxs-lookup"><span data-stu-id="d2f57-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="d2f57-214">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d2f57-214">Close the page.</span></span>
    11. <span data-ttu-id="d2f57-215">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="d2f57-216">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="d2f57-217">В дереве выберите узел **Dynamics 365 for Operations \> Записи таблиц**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="d2f57-218">Выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="d2f57-219">В поле **Имя** введите **Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="d2f57-220">Выберите записи таблицы **Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="d2f57-221">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d2f57-222">Предлагаются только две таблицы, поскольку только две таблицы были добавлены в набор метаданных, которые в настоящее время используются.</span><span class="sxs-lookup"><span data-stu-id="d2f57-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="d2f57-223">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="d2f57-224">В дереве выберите **Интрастат \> AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="d2f57-225">В дереве выберите **Проводка = Интрастат \> Сумма, выставленная по накладным**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="d2f57-226">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="d2f57-227">В дереве выберите **Интрастат \> TransDate**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="d2f57-228">В дереве выберите **Проводка = Интрастат \> Дата**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="d2f57-229">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="d2f57-230">В дереве выберите **Интрастат \> \>Отношения \> IntrastatCommodity \> Код**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="d2f57-231">В дереве выберите **Проводка = Интрастат \> Товарный код**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="d2f57-232">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="d2f57-233">Выберите **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d2f57-234">После завершения проверки вы успешно привязываете элементы модели данных к элементам источников данных, которые описаны с помощью подробных сведений метаданных приложения из указанной конфигурации метаданных ER.</span><span class="sxs-lookup"><span data-stu-id="d2f57-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="d2f57-235">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-235">Select **Save**.</span></span>

<span data-ttu-id="d2f57-236">При необходимости можно расширить существующий набор метаданных в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d2f57-236">As you require, you can extend the existing set of metadata in Finance and Operations.</span></span> <span data-ttu-id="d2f57-237">Затем можно экспортировать новую завершенную версию конфигурации метаданных ER из Finance and Operations, импортировать их в RCS и обновить необходимые условия настроенной конфигурации сопоставления модели, чтобы они ссылались на новую версию импортированной конфигурации метаданных.</span><span class="sxs-lookup"><span data-stu-id="d2f57-237">You can then export the new completed version of the ER metadata configuration from Finance and Operations, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="d2f57-238">Этот метод получения сведений о метаданных приложения является единственным доступным методом для локально развернутых приложений (то есть, когда для Finance and Operations используются локальные бизнес-данные \[LBD\] или локальная модель развертывания).</span><span class="sxs-lookup"><span data-stu-id="d2f57-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for Finance and Operations).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="d2f57-239">Доступ к метаданным приложения с помощью подключенных приложений</span><span class="sxs-lookup"><span data-stu-id="d2f57-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="d2f57-240">Следующая процедура показывает, как пользователь RCS, имеющий роль **Системный администратор** или **Разработчик электронной отчетности**, может разработать новое сопоставление модели ER с помощью метаданных приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d2f57-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the Finance and Operations application.</span></span> <span data-ttu-id="d2f57-241">Доступ к метаданным приложения производится в сети с помощью подключенного приложения RCS.</span><span class="sxs-lookup"><span data-stu-id="d2f57-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="d2f57-242">Образец сопоставления модели ER будет настроен для доступа к проводкам внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="d2f57-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="d2f57-243">Для выполнения этой процедуры необходимо сначала выполнить процедуру [Создание поставщика конфигурации и пометка его как активного](tasks/er-configuration-provider-mark-it-active-2016-11.md) в RCS.</span><span class="sxs-lookup"><span data-stu-id="d2f57-243">To complete this procedure, you must first complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="d2f57-244">Если вы еще не выполнили процедуру [Доступ к метаданным приложения с помощью конфигурации электронной отчетности](#access-application-metadata-by-using-an-er-configuration), приведенную выше в этом разделе, перейдите на страницу [Руководства по задачам электронной отчетности для Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739), чтобы загрузить следующие файлы электронной отчетности заранее и сохранить их локально : **Метаданные внешней торговли.xml**, **Модель внешней торговли.xml** и **Сопоставление внешней торговли.xml**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="d2f57-245">Получение необходимых конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="d2f57-245">Get required ER configurations</span></span>

<span data-ttu-id="d2f57-246">Если вы уже выполнили процедуру [Доступ к метаданным приложения с помощью конфигурации электронной отчетности](#access-application-metadata-by-using-an-er-configuration) ранее в этом разделе, у вас уже имеются все необходимые конфигурации ER (конфигурации метаданных, моделей и сопоставлений внешней торговли) в текущем экземпляре RCS.</span><span class="sxs-lookup"><span data-stu-id="d2f57-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="d2f57-247">В этом случае эту процедуру можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="d2f57-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="d2f57-248">Перейдите в раздел **Все рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="d2f57-249">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="d2f57-250">Загрузите файлы конфигурации **Метаданные внешней торговли.xml**, **Модель внешней торговли.xml** и **Сопоставление внешней торговли.xml**, повторив следующую последовательность шагов для каждого из них:</span><span class="sxs-lookup"><span data-stu-id="d2f57-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="d2f57-251">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="d2f57-252">Выберите **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="d2f57-253">Выберите **Обзор** и выберите файл.</span><span class="sxs-lookup"><span data-stu-id="d2f57-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="d2f57-254">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-finance-and-operations"></a><span data-ttu-id="d2f57-255">Регистрация соединения с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d2f57-255">Register the connection with Finance and Operations</span></span>

1. <span data-ttu-id="d2f57-256">Перейдите в раздел **Все рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="d2f57-257">Выберите **Подключенные приложения**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="d2f57-258">Убедитесь, что настроенное приложение основано на Microsoft Azure, и что оно доступно в общем доступе пользователям RCS.</span><span class="sxs-lookup"><span data-stu-id="d2f57-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="d2f57-259">Текущий пользователь RCS должен иметь доступ к настроенному приложению, будучи зарегистрированным в качестве пользователя данного приложения в роли, которая дает ему право доступа к метаданным приложения.</span><span class="sxs-lookup"><span data-stu-id="d2f57-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives him or her privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="d2f57-260">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-260">Select **New**.</span></span>
5. <span data-ttu-id="d2f57-261">В поле **Имя** введите **MyConnectedApp** в качестве имени подключенного приложения.</span><span class="sxs-lookup"><span data-stu-id="d2f57-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="d2f57-262">В поле **Приложение** укажите URL-адрес приложения.</span><span class="sxs-lookup"><span data-stu-id="d2f57-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="d2f57-263">В поле **Клиент** укажите поставщика приложения.</span><span class="sxs-lookup"><span data-stu-id="d2f57-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="d2f57-264">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-264">Select **Save**.</span></span> 
9. <span data-ttu-id="d2f57-265">При проверке подключения к настроенному приложению на странице **Подключение к удаленному приложению** выберите ссылку **Выберите здесь, чтобы подключиться к выбранному удаленному приложению**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="d2f57-266">Выберите **Проверить подключение** для проверки доступа к настроенному приложению.</span><span class="sxs-lookup"><span data-stu-id="d2f57-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="d2f57-267">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-267">Select **Close**.</span></span>

<span data-ttu-id="d2f57-268">После выполнения этой процедуры и успешной проверки подключения сведения о версии и клиенте для настроенного приложения будут обновлены в текущей сетке.</span><span class="sxs-lookup"><span data-stu-id="d2f57-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="d2f57-269">Проверка существующей конфигурации сопоставлений модели</span><span class="sxs-lookup"><span data-stu-id="d2f57-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="d2f57-270">Перейдите в раздел **Все рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="d2f57-271">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="d2f57-272">В дереве выберите **Модель внешней торговли \> Сопоставление внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="d2f57-273">Выберите экспресс-вкладку **Необходимые условия**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2f57-274">В настоящее время это сопоставление ссылается на конфигурацию метаданных.</span><span class="sxs-lookup"><span data-stu-id="d2f57-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="d2f57-275">Метаданные приложения из этой конфигурации будут предлагаться при разработке этого сопоставления моделей.</span><span class="sxs-lookup"><span data-stu-id="d2f57-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="d2f57-276">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-276">Select **Designer**.</span></span>
5. <span data-ttu-id="d2f57-277">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-277">Select **Designer**.</span></span>
6. <span data-ttu-id="d2f57-278">В дереве выберите узел **Dynamics 365 for Operations \> Записи таблиц**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="d2f57-279">Выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-279">Select **Add root**.</span></span>
8. <span data-ttu-id="d2f57-280">В поле **Таблица** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d2f57-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2f57-281">В настоящее время это сопоставление ссылается на конфигурацию метаданных.</span><span class="sxs-lookup"><span data-stu-id="d2f57-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="d2f57-282">Метаданные приложения из этой конфигурации будут предлагаться при разработке этого сопоставления моделей.</span><span class="sxs-lookup"><span data-stu-id="d2f57-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="d2f57-283">Выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="d2f57-284">Назначение подключенного приложения сопоставлению модели</span><span class="sxs-lookup"><span data-stu-id="d2f57-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="d2f57-285">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-285">Select **Edit**.</span></span>
2. <span data-ttu-id="d2f57-286">В поле **Подключенное приложение** выберите приложение **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2f57-287">Это сопоставление ссылается на метаданные выбранного подключенного приложения.</span><span class="sxs-lookup"><span data-stu-id="d2f57-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="d2f57-288">Если сопоставление ссылается одновременно на конфигурацию метаданных и подключенное приложение, будут использоваться метаданные подключенного приложения.</span><span class="sxs-lookup"><span data-stu-id="d2f57-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="d2f57-289">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-289">Select **Designer**.</span></span>
4. <span data-ttu-id="d2f57-290">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-290">Select **Designer**.</span></span>
5. <span data-ttu-id="d2f57-291">В дереве выберите узел **Dynamics 365 for Operations \> Записи таблиц**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="d2f57-292">Выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-292">Select **Add root**.</span></span>
7. <span data-ttu-id="d2f57-293">В поле **Таблица** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d2f57-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2f57-294">В этот момент предлагается более двух таблиц приложений, поскольку в этом сопоставлении используются все метаданные подключенного приложения, которое было назначено для него.</span><span class="sxs-lookup"><span data-stu-id="d2f57-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="d2f57-295">Выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="d2f57-296">Выберите **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="d2f57-296">Select **Validate**.</span></span>

<span data-ttu-id="d2f57-297">Теперь вы привязали элементы модели данных к элементам источников данных, которые описаны с помощью подробных сведений метаданных подключенного приложения, которое было назначено этому сопоставлению.</span><span class="sxs-lookup"><span data-stu-id="d2f57-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="d2f57-298">Когда необходимо оценить сопоставление модели с помощью метаданных другой версии приложения, зарегистрируйте другое подключенное приложение, назначьте его этому сопоставлению модели и проверьте его по новым метаданным.</span><span class="sxs-lookup"><span data-stu-id="d2f57-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2f57-299">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d2f57-299">Additional resources</span></span>

<span data-ttu-id="d2f57-300">Кроме того, можно воспроизвести руководство по задаче **Подготовка метаданных приложения, которые могут использоваться в RCS** в Finance and Operations, а также руководства по задачам **Доступ к метаданным приложения с помощью конфигурации электронной отчетности** и **Доступ к метаданным приложения с помощью подключенных приложений** в RCS</span><span class="sxs-lookup"><span data-stu-id="d2f57-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in Finance and Operationsas as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="d2f57-301">Эти руководства по задачам можно загрузить со страницы [Руководства по задачам электронной отчетности для Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="d2f57-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>
