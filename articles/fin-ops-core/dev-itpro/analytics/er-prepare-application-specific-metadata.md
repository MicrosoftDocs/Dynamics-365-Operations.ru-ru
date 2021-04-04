---
title: Подготовка метаданных для конкретного приложения для RCS и ER
description: В этом разделе описана процедура подготовки метаданных конкретного приложения для службы Regulatory Configuration Service (RCS) и электронной отчетности (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 37da06f4ba86594c6368dcd1049456c58bf87e3a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565473"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="13de4-103">Подготовка метаданных для конкретного приложения для RCS и ER</span><span class="sxs-lookup"><span data-stu-id="13de4-103">Prepare application-specific metadata for RCS and ER</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="13de4-104">В этом разделе рассматриваются примеры пошагового выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="13de4-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="13de4-105">Подготовка метаданных приложения, которые могут использоваться в RCS</span><span class="sxs-lookup"><span data-stu-id="13de4-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="13de4-106">Доступ к метаданным приложения с помощью конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="13de4-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="13de4-107">Доступ к метаданным приложения с помощью подключенных приложений</span><span class="sxs-lookup"><span data-stu-id="13de4-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="13de4-108">Подготовка метаданных приложения, которые могут использоваться в RCS</span><span class="sxs-lookup"><span data-stu-id="13de4-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="13de4-109">Следующая процедура показывает, как пользователь, имеющий роль **Системный администратор** или **Разработчик электронной отчетности**, может создать конфигурацию электронной отчетности (ER), которая содержит метаданные для приложения и которая используется для разработки конфигураций сопоставления модели ER в службе Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="13de4-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="13de4-110">Образец конфигурации сопоставления модели ER, созданный в этом примере, будет использоваться для доступа к проводкам внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="13de4-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="13de4-111">В этом примере необходимо использовать RCS для создания решения ER для приложения, которое будет использоваться для создания электронных документов, содержащих информацию из бизнес-домена зарубежной торговли.</span><span class="sxs-lookup"><span data-stu-id="13de4-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="13de4-112">Чтобы указать сопоставление модели данных ER с источниками необходимых данных, необходимо иметь доступ к метаданным приложения в RCS.</span><span class="sxs-lookup"><span data-stu-id="13de4-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="13de4-113">Таким образом, в ходе процесса разработки решения ER необходимо настроить новую конфигурацию метаданных ER, которая содержит все текущие необходимые метаданные для создания отчетов ER для выбранного бизнес-домена.</span><span class="sxs-lookup"><span data-stu-id="13de4-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="13de4-114">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="13de4-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="13de4-115">Перейдите в раздел **Управление организацией \> Рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="13de4-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="13de4-116">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="13de4-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="13de4-117">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре [Создание поставщиков конфигураций и пометка их как активных](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="13de4-117">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="13de4-118">Выберите **Конфигурации метаданных**.</span><span class="sxs-lookup"><span data-stu-id="13de4-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="13de4-119">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="13de4-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="13de4-120">В диалоговом окне в раскрывающемся списке в поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="13de4-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="13de4-121">В данном примере введите **Метаданные внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="13de4-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="13de4-122">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="13de4-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="13de4-123">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="13de4-123">Select **Designer**.</span></span>
8. <span data-ttu-id="13de4-124">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13de4-125">Можно выбрать все метаданные либо для всего приложения, либо для выбранных моделей или модулей.</span><span class="sxs-lookup"><span data-stu-id="13de4-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="13de4-126">В обоих случаях следует иметь в виду, что следующие метаданные будут автоматически добавлены: таблицы записей, перечисления и расширенные типы данных (EDT).</span><span class="sxs-lookup"><span data-stu-id="13de4-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="13de4-127">Когда требуются дополнительные типы метаданных, они должны быть добавлены вручную.</span><span class="sxs-lookup"><span data-stu-id="13de4-127">When additional types of metadata are required, they must be manually added.</span></span>

    <span data-ttu-id="13de4-128">Необходимо добавить некоторые метаданные, которые относятся к проводкам внешней торговли, и вручную выбрать элементы метаданных.</span><span class="sxs-lookup"><span data-stu-id="13de4-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="13de4-129">Выберите **Добавить источник данных \> Записи таблицы**.</span><span class="sxs-lookup"><span data-stu-id="13de4-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="13de4-130">Выполните фильтрацию по значению **Интрастат** в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="13de4-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="13de4-131">Выберите запись таблицы **Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="13de4-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="13de4-132">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13de4-132">Select **OK**.</span></span>

    <span data-ttu-id="13de4-133">Необходимо добавить сведения метаданных о записях таблицы Интрастат</span><span class="sxs-lookup"><span data-stu-id="13de4-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="13de4-134">В дереве выберите **Таблицы записей Интрастат \> \>Отношения \> IntrastatCommodity (записи таблицы EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="13de4-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="13de4-135">Выберите **Добавить метаданные**.</span><span class="sxs-lookup"><span data-stu-id="13de4-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13de4-136">Метаданные о необходимых отношениях для выбранной таблицы записей необходимо добавить вручную.</span><span class="sxs-lookup"><span data-stu-id="13de4-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="13de4-137">Выберите **Добавить источник данных**.</span><span class="sxs-lookup"><span data-stu-id="13de4-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="13de4-138">Выберите **Перечисление**.</span><span class="sxs-lookup"><span data-stu-id="13de4-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="13de4-139">Выполните фильтрацию по значению **IntrastatDirection** в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="13de4-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="13de4-140">Выберите запись перечисления **IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="13de4-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="13de4-141">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13de4-141">Select **OK**.</span></span>
20. <span data-ttu-id="13de4-142">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-142">Select **Save**.</span></span>
21. <span data-ttu-id="13de4-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="13de4-143">Close the page.</span></span>
22. <span data-ttu-id="13de4-144">Завершите черновую версию конфигурации метаданных:</span><span class="sxs-lookup"><span data-stu-id="13de4-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="13de4-145">Выберите **Изменить статус \> Завершено**.</span><span class="sxs-lookup"><span data-stu-id="13de4-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="13de4-146">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13de4-146">Select **OK**.</span></span>
    3. <span data-ttu-id="13de4-147">Выберите завершенную версию 1.</span><span class="sxs-lookup"><span data-stu-id="13de4-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="13de4-148">Экспортируйте завершенную версию конфигурации метаданных из приложения в виде файла XML:</span><span class="sxs-lookup"><span data-stu-id="13de4-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="13de4-149">Выберите **Обменять \> Экспорт в виде XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="13de4-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="13de4-150">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13de4-150">Select **OK**.</span></span>

<span data-ttu-id="13de4-151">Созданная конфигурация метаданных ER будет сохранена в виде файла **Метаданные внешней торговли.xml**.</span><span class="sxs-lookup"><span data-stu-id="13de4-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="13de4-152">Теперь можно импортировать его в RCS, чтобы его можно было использовать в качестве источника метаданных для бизнес-домена внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="13de4-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="13de4-153">На основе этих сведений можно указать сопоставление между метаданными приложения и моделью данных ER.</span><span class="sxs-lookup"><span data-stu-id="13de4-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="13de4-154">Доступ к метаданным приложения с помощью конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="13de4-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="13de4-155">Следующая процедура показывает, как пользователь RCS, имеющий роль **Системный администратор** или **Разработчик электронной отчетности**, может разработать новое сопоставление модели ER с помощью метаданных из приложения.</span><span class="sxs-lookup"><span data-stu-id="13de4-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="13de4-156">Доступ к метаданным приложения будет осуществляться с помощью конфигурации метаданных ER, которая содержит образец набора метаданных для доступа к проводкам внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="13de4-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="13de4-157">Перед окончанием выполнения этой процедуры необходимо сначала выполнить следующие процедуры:</span><span class="sxs-lookup"><span data-stu-id="13de4-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="13de4-158">Создание поставщиков конфигураций и пометка их как активных</span><span class="sxs-lookup"><span data-stu-id="13de4-158">Create configuration providers and mark them as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="13de4-159">Подготовка метаданных приложения, которые могут использоваться в RCS</span><span class="sxs-lookup"><span data-stu-id="13de4-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="13de4-160">Перейдите в раздел **Все рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="13de4-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="13de4-161">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="13de4-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="13de4-162">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре [Создание поставщиков конфигураций и пометка их как активных](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="13de4-162">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="13de4-163">Импортируйте конфигурацию метаданных ER, которая содержит метаданные для приложения и настроена для создания электронных документов для бизнес-домена внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="13de4-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="13de4-164">Вы создали конфигурацию метаданных ER и экспортировали ее как XML-файл в процедуре [Подготовка метаданных приложения, которые могут использоваться в RCS](#prepare-application-metadata-that-can-be-used-in-rcs) ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="13de4-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="13de4-165">Выберите **Конфигурации метаданных**.</span><span class="sxs-lookup"><span data-stu-id="13de4-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="13de4-166">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="13de4-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="13de4-167">Выберите **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="13de4-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="13de4-168">Найдите и выберите файл **Метаданные внешней торговли.xml**.</span><span class="sxs-lookup"><span data-stu-id="13de4-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="13de4-169">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13de4-169">Select **OK**.</span></span>
    6. <span data-ttu-id="13de4-170">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="13de4-170">Close the page.</span></span>

4. <span data-ttu-id="13de4-171">Создание конфигурации модели данных:</span><span class="sxs-lookup"><span data-stu-id="13de4-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="13de4-172">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="13de4-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="13de4-173">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="13de4-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="13de4-174">В диалоговом окне в раскрывающемся списке в поле **Имя** введите **Модель внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="13de4-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="13de4-175">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="13de4-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="13de4-176">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="13de4-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="13de4-177">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="13de4-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="13de4-178">В поле **Имя** введите **Корень**.</span><span class="sxs-lookup"><span data-stu-id="13de4-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="13de4-179">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="13de4-180">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="13de4-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="13de4-181">В поле **Имя** введите **Проводка**.</span><span class="sxs-lookup"><span data-stu-id="13de4-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="13de4-182">В поле **Тип элемента** выберите **Список записей**.</span><span class="sxs-lookup"><span data-stu-id="13de4-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="13de4-183">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="13de4-184">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="13de4-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="13de4-185">В поле **Имя** введите **Код товара**.</span><span class="sxs-lookup"><span data-stu-id="13de4-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="13de4-186">В поле **Тип элемента** выберите **Строка**.</span><span class="sxs-lookup"><span data-stu-id="13de4-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="13de4-187">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-187">Select **Add**.</span></span>

    9. <span data-ttu-id="13de4-188">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="13de4-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="13de4-189">В поле "Имя" введите **Сумма, выставленная по накладным**.</span><span class="sxs-lookup"><span data-stu-id="13de4-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="13de4-190">В поле **Тип элемента** выберите **Вещественный**.</span><span class="sxs-lookup"><span data-stu-id="13de4-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="13de4-191">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-191">Select **Add**.</span></span>

    10. <span data-ttu-id="13de4-192">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="13de4-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="13de4-193">В поле **Имя** введите **Дата**.</span><span class="sxs-lookup"><span data-stu-id="13de4-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="13de4-194">В поле **Тип элемента** выберите **Дата**.</span><span class="sxs-lookup"><span data-stu-id="13de4-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="13de4-195">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="13de4-196">Выберите **Добавить \> Корневая ссылка**.</span><span class="sxs-lookup"><span data-stu-id="13de4-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="13de4-197">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13de4-197">Select **OK**.</span></span>
    13. <span data-ttu-id="13de4-198">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-198">Select **Save**.</span></span>
    14. <span data-ttu-id="13de4-199">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="13de4-199">Close the page.</span></span>
    15. <span data-ttu-id="13de4-200">Выберите **Изменить статус \> Завершено**.</span><span class="sxs-lookup"><span data-stu-id="13de4-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="13de4-201">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13de4-201">Select **OK**.</span></span>

5. <span data-ttu-id="13de4-202">Создайте конфигурацию сопоставления модели:</span><span class="sxs-lookup"><span data-stu-id="13de4-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="13de4-203">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="13de4-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="13de4-204">В раскрывающемся диалоговом окне в полей **Создать** введите **Сопоставление модели на основе модели данных внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="13de4-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="13de4-205">В поле **Имя** введите **Сопоставление внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="13de4-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="13de4-206">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="13de4-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="13de4-207">На экспресс-вкладке **Необходимые условия** выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="13de4-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="13de4-208">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="13de4-208">Select **New**.</span></span>
    7. <span data-ttu-id="13de4-209">В поле **Тип необходимого компонента** выберите **Конфигурация**.</span><span class="sxs-lookup"><span data-stu-id="13de4-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="13de4-210">Выберите конфигурацию **Метаданные внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="13de4-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="13de4-211">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-211">Select **Save**.</span></span> <span data-ttu-id="13de4-212">Обратите внимание, что ссылка добавляется к версии 1 конфигурации **Метаданные внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="13de4-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="13de4-213">Метаданные приложения из этой конфигурации будут предлагаться при разработке сопоставления моделей.</span><span class="sxs-lookup"><span data-stu-id="13de4-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="13de4-214">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="13de4-214">Close the page.</span></span>
    11. <span data-ttu-id="13de4-215">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="13de4-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="13de4-216">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="13de4-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="13de4-217">В дереве выберите узел **Dynamics 365 for Operations \> Записи таблиц**.</span><span class="sxs-lookup"><span data-stu-id="13de4-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="13de4-218">Выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="13de4-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="13de4-219">В поле **Имя** введите **Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="13de4-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="13de4-220">Выберите записи таблицы **Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="13de4-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="13de4-221">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13de4-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="13de4-222">Предлагаются только две таблицы, поскольку только две таблицы были добавлены в набор метаданных, которые в настоящее время используются.</span><span class="sxs-lookup"><span data-stu-id="13de4-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="13de4-223">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="13de4-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="13de4-224">В дереве выберите **Интрастат \> AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="13de4-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="13de4-225">В дереве выберите **Проводка = Интрастат \> Сумма, выставленная по накладным**.</span><span class="sxs-lookup"><span data-stu-id="13de4-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="13de4-226">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="13de4-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="13de4-227">В дереве выберите **Интрастат \> TransDate**.</span><span class="sxs-lookup"><span data-stu-id="13de4-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="13de4-228">В дереве выберите **Проводка = Интрастат \> Дата**.</span><span class="sxs-lookup"><span data-stu-id="13de4-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="13de4-229">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="13de4-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="13de4-230">В дереве выберите **Интрастат \> \>Отношения \> IntrastatCommodity \> Код**.</span><span class="sxs-lookup"><span data-stu-id="13de4-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="13de4-231">В дереве выберите **Проводка = Интрастат \> Товарный код**.</span><span class="sxs-lookup"><span data-stu-id="13de4-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="13de4-232">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="13de4-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="13de4-233">Выберите **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="13de4-234">После завершения проверки вы успешно привязываете элементы модели данных к элементам источников данных, которые описаны с помощью подробных сведений метаданных приложения из указанной конфигурации метаданных ER.</span><span class="sxs-lookup"><span data-stu-id="13de4-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="13de4-235">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-235">Select **Save**.</span></span>

<span data-ttu-id="13de4-236">При необходимости можно расширить существующий набор метаданных в приложении.</span><span class="sxs-lookup"><span data-stu-id="13de4-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="13de4-237">Затем можно экспортировать новую завершенную версию конфигурации метаданных ER, импортировать их в RCS и обновить необходимые условия настроенной конфигурации сопоставления модели, чтобы они ссылались на новую версию импортированной конфигурации метаданных.</span><span class="sxs-lookup"><span data-stu-id="13de4-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="13de4-238">Этот метод получения сведений о метаданных приложения является единственным доступным методом для локально развернутых приложений (то есть, когда для приложения используются локальные бизнес-данные \[LBD\] или локальная модель развертывания).</span><span class="sxs-lookup"><span data-stu-id="13de4-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="13de4-239">Доступ к метаданным приложения с помощью подключенных приложений</span><span class="sxs-lookup"><span data-stu-id="13de4-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="13de4-240">Следующая процедура показывает, как пользователь RCS, имеющий роль **Системный администратор** или **Разработчик электронной отчетности**, может разработать новое сопоставление модели ER с помощью метаданных приложения.</span><span class="sxs-lookup"><span data-stu-id="13de4-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="13de4-241">Доступ к метаданным приложения производится в сети с помощью подключенного приложения RCS.</span><span class="sxs-lookup"><span data-stu-id="13de4-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="13de4-242">Образец сопоставления модели ER будет настроен для доступа к проводкам внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="13de4-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="13de4-243">Для выполнения этой процедуры необходимо сначала выполнить процедуру [Создание поставщиков конфигураций и пометка их как активных](tasks/er-configuration-provider-mark-it-active-2016-11.md) в RCS.</span><span class="sxs-lookup"><span data-stu-id="13de4-243">To complete this procedure, you must first complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="13de4-244">Если вы еще не выполнили процедуру [Доступ к метаданным приложения с помощью конфигурации электронной отчетности](#access-application-metadata-by-using-an-er-configuration), приведенную выше в этом разделе, перейдите на страницу [Руководства по задачам электронной отчетности для Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739), чтобы загрузить следующие файлы электронной отчетности заранее и сохранить их локально : **Метаданные внешней торговли.xml**, **Модель внешней торговли.xml** и **Сопоставление внешней торговли.xml**.</span><span class="sxs-lookup"><span data-stu-id="13de4-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="13de4-245">Получение необходимых конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="13de4-245">Get required ER configurations</span></span>

<span data-ttu-id="13de4-246">Если вы уже выполнили процедуру [Доступ к метаданным приложения с помощью конфигурации электронной отчетности](#access-application-metadata-by-using-an-er-configuration) ранее в этом разделе, у вас уже имеются все необходимые конфигурации ER (конфигурации метаданных, моделей и сопоставлений внешней торговли) в текущем экземпляре RCS.</span><span class="sxs-lookup"><span data-stu-id="13de4-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="13de4-247">В этом случае эту процедуру можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="13de4-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="13de4-248">Перейдите в раздел **Все рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="13de4-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="13de4-249">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="13de4-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="13de4-250">Загрузите файлы конфигурации **Метаданные внешней торговли.xml**, **Модель внешней торговли.xml** и **Сопоставление внешней торговли.xml**, повторив следующую последовательность шагов для каждого из них:</span><span class="sxs-lookup"><span data-stu-id="13de4-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="13de4-251">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="13de4-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="13de4-252">Выберите **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="13de4-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="13de4-253">Выберите **Обзор** и выберите файл.</span><span class="sxs-lookup"><span data-stu-id="13de4-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="13de4-254">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13de4-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="13de4-255">Регистрация подключения к приложению</span><span class="sxs-lookup"><span data-stu-id="13de4-255">Register the connection with the application</span></span>

1. <span data-ttu-id="13de4-256">Перейдите в раздел **Все рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="13de4-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="13de4-257">Выберите **Подключенные приложения**.</span><span class="sxs-lookup"><span data-stu-id="13de4-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="13de4-258">Убедитесь, что настроенное приложение основано на Microsoft Azure, и что оно доступно в общем доступе пользователям RCS.</span><span class="sxs-lookup"><span data-stu-id="13de4-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="13de4-259">Текущий пользователь RCS должен иметь доступ к настроенному приложению, будучи зарегистрированным в качестве пользователя данного приложения в роли, которая дает ему право доступа к метаданным приложения.</span><span class="sxs-lookup"><span data-stu-id="13de4-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives them privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="13de4-260">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="13de4-260">Select **New**.</span></span>
5. <span data-ttu-id="13de4-261">В поле **Имя** введите **MyConnectedApp** в качестве имени подключенного приложения.</span><span class="sxs-lookup"><span data-stu-id="13de4-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="13de4-262">В поле **Приложение** укажите URL-адрес приложения.</span><span class="sxs-lookup"><span data-stu-id="13de4-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="13de4-263">В поле **Клиент** укажите поставщика приложения.</span><span class="sxs-lookup"><span data-stu-id="13de4-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="13de4-264">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-264">Select **Save**.</span></span> 
9. <span data-ttu-id="13de4-265">При проверке подключения к настроенному приложению на странице **Подключение к удаленному приложению** выберите ссылку **Выберите здесь, чтобы подключиться к выбранному удаленному приложению**.</span><span class="sxs-lookup"><span data-stu-id="13de4-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="13de4-266">Выберите **Проверить подключение** для проверки доступа к настроенному приложению.</span><span class="sxs-lookup"><span data-stu-id="13de4-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="13de4-267">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="13de4-267">Select **Close**.</span></span>

<span data-ttu-id="13de4-268">После выполнения этой процедуры и успешной проверки подключения сведения о версии и клиенте для настроенного приложения будут обновлены в текущей сетке.</span><span class="sxs-lookup"><span data-stu-id="13de4-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="13de4-269">Проверка существующей конфигурации сопоставлений модели</span><span class="sxs-lookup"><span data-stu-id="13de4-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="13de4-270">Перейдите в раздел **Все рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="13de4-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="13de4-271">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="13de4-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="13de4-272">В дереве выберите **Модель внешней торговли \> Сопоставление внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="13de4-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="13de4-273">Выберите экспресс-вкладку **Необходимые условия**.</span><span class="sxs-lookup"><span data-stu-id="13de4-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13de4-274">В настоящее время это сопоставление ссылается на конфигурацию метаданных.</span><span class="sxs-lookup"><span data-stu-id="13de4-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="13de4-275">Метаданные приложения из этой конфигурации будут предлагаться при разработке этого сопоставления моделей.</span><span class="sxs-lookup"><span data-stu-id="13de4-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="13de4-276">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="13de4-276">Select **Designer**.</span></span>
5. <span data-ttu-id="13de4-277">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="13de4-277">Select **Designer**.</span></span>
6. <span data-ttu-id="13de4-278">В дереве выберите узел **Dynamics 365 for Operations \> Записи таблиц**.</span><span class="sxs-lookup"><span data-stu-id="13de4-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="13de4-279">Выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="13de4-279">Select **Add root**.</span></span>
8. <span data-ttu-id="13de4-280">В поле **Таблица** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="13de4-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13de4-281">В настоящее время это сопоставление ссылается на конфигурацию метаданных.</span><span class="sxs-lookup"><span data-stu-id="13de4-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="13de4-282">Метаданные приложения из этой конфигурации будут предлагаться при разработке этого сопоставления моделей.</span><span class="sxs-lookup"><span data-stu-id="13de4-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="13de4-283">Выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="13de4-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="13de4-284">Назначение подключенного приложения сопоставлению модели</span><span class="sxs-lookup"><span data-stu-id="13de4-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="13de4-285">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="13de4-285">Select **Edit**.</span></span>
2. <span data-ttu-id="13de4-286">В поле **Подключенное приложение** выберите приложение **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="13de4-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13de4-287">Это сопоставление ссылается на метаданные выбранного подключенного приложения.</span><span class="sxs-lookup"><span data-stu-id="13de4-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="13de4-288">Если сопоставление ссылается одновременно на конфигурацию метаданных и подключенное приложение, будут использоваться метаданные подключенного приложения.</span><span class="sxs-lookup"><span data-stu-id="13de4-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="13de4-289">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="13de4-289">Select **Designer**.</span></span>
4. <span data-ttu-id="13de4-290">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="13de4-290">Select **Designer**.</span></span>
5. <span data-ttu-id="13de4-291">В дереве выберите узел **Dynamics 365 for Operations \> Записи таблиц**.</span><span class="sxs-lookup"><span data-stu-id="13de4-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="13de4-292">Выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="13de4-292">Select **Add root**.</span></span>
7. <span data-ttu-id="13de4-293">В поле **Таблица** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="13de4-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13de4-294">В этот момент предлагается более двух таблиц приложений, поскольку в этом сопоставлении используются все метаданные подключенного приложения, которое было назначено для него.</span><span class="sxs-lookup"><span data-stu-id="13de4-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="13de4-295">Выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="13de4-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="13de4-296">Выберите **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="13de4-296">Select **Validate**.</span></span>

<span data-ttu-id="13de4-297">Теперь вы привязали элементы модели данных к элементам источников данных, которые описаны с помощью подробных сведений метаданных подключенного приложения, которое было назначено этому сопоставлению.</span><span class="sxs-lookup"><span data-stu-id="13de4-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="13de4-298">Когда необходимо оценить сопоставление модели с помощью метаданных другой версии приложения, зарегистрируйте другое подключенное приложение, назначьте его этому сопоставлению модели и проверьте его по новым метаданным.</span><span class="sxs-lookup"><span data-stu-id="13de4-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13de4-299">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="13de4-299">Additional resources</span></span>

<span data-ttu-id="13de4-300">Кроме того, можно воспроизвести руководство по задаче **Подготовка метаданных приложения, которые могут использоваться в RCS** в приложении, а также руководства по задачам **Доступ к метаданным приложения с помощью конфигурации электронной отчетности** и **Доступ к метаданным приложения с помощью подключенных приложений** в RCS</span><span class="sxs-lookup"><span data-stu-id="13de4-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="13de4-301">Эти руководства по задачам можно загрузить со страницы [Руководства по задачам электронной отчетности для Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="13de4-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]