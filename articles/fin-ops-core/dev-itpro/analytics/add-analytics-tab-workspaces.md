---
title: Добавление аналитики в рабочие области с помощью Power BI Embedded
description: В этом разделе показано, как внедрить отчет Power BI на вкладку "Аналитика" рабочей области.
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4e757ce585b16b23d65506068dcc337211107199
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568498"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="a49b7-103">Добавление аналитики в рабочие области с помощью Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="a49b7-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a49b7-104">Эта возможность поддерживается в Finance and Operations (версии 7.2 и выше).</span><span class="sxs-lookup"><span data-stu-id="a49b7-104">This feature is supported in Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="a49b7-105">Введение</span><span class="sxs-lookup"><span data-stu-id="a49b7-105">Introduction</span></span>
<span data-ttu-id="a49b7-106">В этом разделе показано, как внедрить отчет Microsoft Power BI на вкладку **Аналитика** рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a49b7-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="a49b7-107">В данном примере мы расширим рабочую область **Управление резервированием** в приложении "Управления автопарком" для внедрения аналитической рабочей области на вкладку **Аналитика**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a49b7-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="a49b7-108">Prerequisites</span></span>
+ <span data-ttu-id="a49b7-109">Доступ к среде разработчика, в которой выполняется обновление 8 платформы или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a49b7-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="a49b7-110">Аналитический отчет (PBIX-файл), созданный с помощью Microsoft Power BI Desktop и имеющий модель данных, взятую из базы данных хранилища объектов.</span><span class="sxs-lookup"><span data-stu-id="a49b7-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="a49b7-111">Обзор</span><span class="sxs-lookup"><span data-stu-id="a49b7-111">Overview</span></span>
<span data-ttu-id="a49b7-112">Независимо от того, расширяете ли вы существующую рабочую область приложения или вводите новую рабочую область, вы можете использовать внедренные аналитические представления для доставки важных и интерактивных представлений бизнес-данных.</span><span class="sxs-lookup"><span data-stu-id="a49b7-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="a49b7-113">Процесс добавления аналитической вкладки рабочей области состоит из четырех шагов.</span><span class="sxs-lookup"><span data-stu-id="a49b7-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="a49b7-114">Добавьте PBIX-файл как ресурс Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a49b7-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="a49b7-115">Определите аналитическую вкладку рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a49b7-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="a49b7-116">Внедрите PBIX-ресурс на вкладку рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a49b7-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="a49b7-117">Необязательно: добавьте расширения, чтобы настроить представление.</span><span class="sxs-lookup"><span data-stu-id="a49b7-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="a49b7-118">Дополнительные сведения о создании аналитических отчетов см. в разделе [Начало работы с Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="a49b7-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="a49b7-119">Эта страница является отличным источником важных данных, которые могут помочь создать привлекательные аналитические решения отчетности.</span><span class="sxs-lookup"><span data-stu-id="a49b7-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="a49b7-120">Добавление PBIX-файла как ресурса Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a49b7-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="a49b7-121">Прежде чем начать, необходимо создать или получить отчет Power BI, который будет внедрен в рабочую область.</span><span class="sxs-lookup"><span data-stu-id="a49b7-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="a49b7-122">Дополнительные сведения о создании аналитических отчетов см. в разделе [Начало работы с Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="a49b7-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span>

<span data-ttu-id="a49b7-123">Выполните следующие действия, чтобы добавить PBIX-файл в качестве артефакта проекта Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a49b7-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="a49b7-124">Создайте новый проект в соответствующей модели.</span><span class="sxs-lookup"><span data-stu-id="a49b7-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="a49b7-125">В обозревателе решений выберите проект, щелкните правой кнопкой мыши, а затем выберите **Добавить** \> **Новый элемент**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-125">In Solution Explorer, select the project, right-click, and then select **Add** \> **New Item**.</span></span>
3. <span data-ttu-id="a49b7-126">В диалоговом окне **Добавление нового элемента** в разделе **Артефакты операций** выберите шаблон **Ресурс**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="a49b7-127">Введите имя, которое будет использоваться для ссылки на отчет в метаданных X ++, и щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Диалоговое окно "Добавление нового элемента"](media/analytical-workspace-add.png)

5. <span data-ttu-id="a49b7-129">Найдите PBIX-файл, содержащий определение аналитического отчета, а затем щелкните **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Диалоговое окно "Выбор файла ресурса"](media/analytical-workspace-select-resource.png)

<span data-ttu-id="a49b7-131">Теперь, когда вы добавили PBIX-файл как ресурс Dynamics 365, можно внедрить отчеты в рабочие области и добавить прямые ссылки с помощью пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="a49b7-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="a49b7-132">Добавление элемента управления вкладкой в рабочую область приложения</span><span class="sxs-lookup"><span data-stu-id="a49b7-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="a49b7-133">В этом примере мы расширим рабочую область **Управление резервированием** в "Управления автопарком", добавив вкладку **Аналитика** к определению формы **FMClerkWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>

<span data-ttu-id="a49b7-134">На следующем рисунке показано, как выглядит форма **FMClerkWorkspace** в конструкторе в Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a49b7-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![Форма FMClerkWorkspace до изменений](media/analytical-workspace-definition-before.png)

<span data-ttu-id="a49b7-136">Выполните следующие шаги для расширения определения формы для рабочей области **Управление резервированием**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="a49b7-137">Откройте конструктор форм для расширения определения конструктора.</span><span class="sxs-lookup"><span data-stu-id="a49b7-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="a49b7-138">В определении конструктора выберите верхний элемент, помеченный как **Дизайн | Шаблон: операционный, рабочая область**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="a49b7-139">Щелкните правой кнопкой мыши, а затем выберите **Создать** \> **Вкладка** для добавления нового элемента управления с именем **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-139">Right-click, and then select **New** \> **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="a49b7-140">В конструкторе форм выберите **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="a49b7-141">Щелкните правой кнопкой мыши, а затем выберите **Новая страница вкладки**, чтобы добавить новую страницу вкладки.</span><span class="sxs-lookup"><span data-stu-id="a49b7-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="a49b7-142">Переименуйте страницу вкладки на значимое имя, например **Рабочая область**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="a49b7-143">В конструкторе форм выберите **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="a49b7-144">Щелкните правой кнопкой мыши, а затем выберите **Новая страница вкладки**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="a49b7-145">Переименуйте страницу вкладки на значимое имя, например **Аналитика**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="a49b7-146">В конструкторе форм выберите **Аналитика (страница вкладки)**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="a49b7-147">Установите для свойства **Подпись** значение **Analytics** и задайте для свойства **Автоматическое объявление** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-147">Set the **Caption** property to **Analytics**, and set the **Auto Declaration** property to **Yes**.</span></span>
12. <span data-ttu-id="a49b7-148">Щелкните правой кнопкой мыши элемент управления, а затем выберите **Создать** \> **Группа** для добавления нового элемента управления группой форм.</span><span class="sxs-lookup"><span data-stu-id="a49b7-148">Right-click the control, and then select **New** \> **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="a49b7-149">Переименуйте группу форм на значимое имя, например **powerBIReportGroup**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="a49b7-150">В конструкторе форм выберите **PanoramaBody (вкладка)**, а затем перетащите элемент управления на вкладку **Рабочая область**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="a49b7-151">В определении конструктора выберите верхний элемент, помеченный как **Дизайн | Шаблон: операционный, рабочая область**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="a49b7-152">Щелкните правой кнопкой мыши, а затем выберите **Удалить шаблон**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="a49b7-153">Снова щелкните правой кнопкой мыши, а затем выберите **Добавить шаблон** \> **Рабочая область с вкладками**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-153">Right-click again, and then select **Add pattern** \> **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="a49b7-154">Выполните сборку, чтобы проверить изменения.</span><span class="sxs-lookup"><span data-stu-id="a49b7-154">Perform a build to verify your changes.</span></span>

<span data-ttu-id="a49b7-155">На следующем рисунке показан дизайн после применения этих изменений.</span><span class="sxs-lookup"><span data-stu-id="a49b7-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace после изменений](media/analytical-workspace-definition-after.png)

<span data-ttu-id="a49b7-157">Теперь, когда вы добавили элементы управления формой, которые будут использоваться для внедрения отчета рабочей области, необходимо определить размер родительского элемента управления, чтобы он соответствовал макету.</span><span class="sxs-lookup"><span data-stu-id="a49b7-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="a49b7-158">По умолчанию обе страницы **Область фильтров** и **Вкладка** будут отображаться в отчете.</span><span class="sxs-lookup"><span data-stu-id="a49b7-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="a49b7-159">Тем не менее, можно изменить видимость этих элементов управления в зависимости от целевого потребителя отчета.</span><span class="sxs-lookup"><span data-stu-id="a49b7-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>

> [!NOTE]
> <span data-ttu-id="a49b7-160">Для встроенных рабочих областей рекомендуется использовать расширения, чтобы скрыть страницы **Область фильтров** и **Вкладка** для согласованности.</span><span class="sxs-lookup"><span data-stu-id="a49b7-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>

<span data-ttu-id="a49b7-161">Вы завершили задачу расширения определения формы приложения.</span><span class="sxs-lookup"><span data-stu-id="a49b7-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="a49b7-162">Дополнительные сведения о том, как использовать расширения для настройки, см. в разделе [Настройка с помощью расширения и перекрытия](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a49b7-162">For more information about how to use extensions to do customizations, see [Customize through extension and overlayering](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="a49b7-163">Добавление бизнес-логики X ++ для внедрения элемента управления средством просмотра</span><span class="sxs-lookup"><span data-stu-id="a49b7-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="a49b7-164">Выполните следующие действия, чтобы добавить бизнес-логику, которая инициализирует элемент управления средством просмотра отчетов, который внедрен в рабочую область **Управление резервированием**.</span><span class="sxs-lookup"><span data-stu-id="a49b7-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="a49b7-165">Откройте конструктор форм **FMClerkWorkspace** для расширения определения конструктора.</span><span class="sxs-lookup"><span data-stu-id="a49b7-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="a49b7-166">Нажмите клавишу F7 для доступа к коду определения кода.</span><span class="sxs-lookup"><span data-stu-id="a49b7-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="a49b7-167">Добавьте следующий код X++:</span><span class="sxs-lookup"><span data-stu-id="a49b7-167">Add the following X++ code.</span></span>

    ```xpp
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="a49b7-168">Выполните сборку, чтобы проверить изменения.</span><span class="sxs-lookup"><span data-stu-id="a49b7-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="a49b7-169">Вы выполнили задачу по добавлению бизнес-логики для инициализации внедренного элемента управления средством просмотра отчетов.</span><span class="sxs-lookup"><span data-stu-id="a49b7-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="a49b7-170">На следующем рисунке показана рабочая область после применения этих изменений.</span><span class="sxs-lookup"><span data-stu-id="a49b7-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![Отчет, внедренный в рабочую область](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="a49b7-172">Вы можете получить доступ к существующему операционному представлению с помощью вкладок рабочей области под заголовком страницы.</span><span class="sxs-lookup"><span data-stu-id="a49b7-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="a49b7-173">Справка</span><span class="sxs-lookup"><span data-stu-id="a49b7-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="a49b7-174">Метод PBIReportHelper.initializeReportControl</span><span class="sxs-lookup"><span data-stu-id="a49b7-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="a49b7-175">В этом разделе представлены сведения о вспомогательном классе, который используется для внедрения отчета Power BI (PBIX-ресурс) в элемент управления группой форм.</span><span class="sxs-lookup"><span data-stu-id="a49b7-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="a49b7-176">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a49b7-176">Syntax</span></span>
```xpp
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="a49b7-177">Параметры</span><span class="sxs-lookup"><span data-stu-id="a49b7-177">Parameters</span></span>

| <span data-ttu-id="a49b7-178">Наименование</span><span class="sxs-lookup"><span data-stu-id="a49b7-178">Name</span></span>             | <span data-ttu-id="a49b7-179">описание</span><span class="sxs-lookup"><span data-stu-id="a49b7-179">Description</span></span>                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a49b7-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="a49b7-180">resourceName</span></span>     | <span data-ttu-id="a49b7-181">Имя PBIX-ресурса.</span><span class="sxs-lookup"><span data-stu-id="a49b7-181">The name of the .pbix resource.</span></span>                                                                              |
| <span data-ttu-id="a49b7-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="a49b7-182">formGroupControl</span></span> | <span data-ttu-id="a49b7-183">Элемент управления группой форм, к которому применяется элемент управления отчетом Power BI.</span><span class="sxs-lookup"><span data-stu-id="a49b7-183">The form group control to apply the Power BI report control to.</span></span>                                              |
| <span data-ttu-id="a49b7-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="a49b7-184">defaultPageName</span></span>  | <span data-ttu-id="a49b7-185">Имя страницы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a49b7-185">The default page name.</span></span>                                                                                       |
| <span data-ttu-id="a49b7-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="a49b7-186">showFilterPane</span></span>   | <span data-ttu-id="a49b7-187">Логическое значение, указывающее, должна ли отображаться область фильтров (**true**) или нет (**false**).</span><span class="sxs-lookup"><span data-stu-id="a49b7-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span>     |
| <span data-ttu-id="a49b7-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="a49b7-188">showNavPane</span></span>      | <span data-ttu-id="a49b7-189">Логическое значение, указывающее, должна ли отображаться область перехода (**true**) или нет (**false**).</span><span class="sxs-lookup"><span data-stu-id="a49b7-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="a49b7-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="a49b7-190">defaultFilters</span></span>   | <span data-ttu-id="a49b7-191">Фильтры по умолчанию для отчета Power BI.</span><span class="sxs-lookup"><span data-stu-id="a49b7-191">The default filters for the Power BI report.</span></span>                                                                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]