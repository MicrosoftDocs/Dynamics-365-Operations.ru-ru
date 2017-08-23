---
title: "Добавление аналитики в рабочие области с помощью Power BI Embedded"
description: "В этом разделе показано, как внедрить отчет Power BI на вкладку \"Аналитика\" рабочей области."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations, Platform, UnifiedOperations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.intro: Platform update 8
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: e819aafbdf55fbc2a6dc996d275244de1e11d89b
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Добавление аналитики в рабочие области с помощью Power BI Embedded

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Эта функция поддерживается в Dynamics 365 for Finance and Operations (версия 7.2 и выше).

# <a name="introduction"></a>Приветствие
В этом разделе показано, как внедрить отчет Microsoft Power BI на вкладку **Аналитика** рабочей области. В данном примере мы расширим рабочую область **Управление резервированием** в приложении "Управления автопарком" для внедрения аналитической рабочей области на вкладку **Аналитика**.

# <a name="prerequisites"></a>Необходимые условия
+ Доступ к среде разработчика, в которой выполняется обновление 8 платформы или более поздней версии.
+ Аналитический отчет (PBIX-файл), созданный с помощью Microsoft Power BI Desktop и имеющий модель данных, взятую из базы данных хранилища объектов.

# <a name="overview"></a>Обзор
Независимо от того, расширяете ли вы существующую рабочую область приложения или вводите новую рабочую область, вы можете использовать внедренные аналитические представления для доставки важных и интерактивных представлений бизнес-данных. Процесс добавления аналитической вкладки рабочей области состоит из четырех шагов.

1. Добавьте PBIX-файл как ресурс Dynamics 365.
2. Определите аналитическую вкладку рабочей области.
3. Внедрите PBIX-ресурс на вкладку рабочей области.
4. Необязательно: добавьте расширения, чтобы настроить представление.

> [!NOTE]
> Дополнительные сведения о создании аналитических отчетов см. в разделе [Начало работы с Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/). Эта страница является отличным источником важных данных, которые могут помочь создать привлекательные аналитические решения отчетности.

# <a name="add-a-pbix-file-as-a-resource"></a>Добавление PBIX-файла как ресурса Dynamics 365
Прежде чем начать, необходимо создать или получить отчет Power BI, который будет внедрен в рабочую область. Дополнительные сведения о создании аналитических отчетов см. в разделе [Начало работы с Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).
 
Выполните следующие действия, чтобы добавить PBIX-файл в качестве артефакта проекта Visual Studio.

1. Создайте новый проект в соответствующей модели.
2. В обозревателе решений выберите проект, щелкните правой кнопкой мыши, а затем выберите **Добавить** > **Новый элемент**.
3. В диалоговом окне **Добавление нового элемента** в разделе **Артефакты операций** выберите шаблон **Ресурс**.
4. Введите имя, которое будет использоваться для ссылки на отчет в метаданных X ++, и щелкните **Добавить**.

    ![Диалоговое окно "Добавление нового элемента"](media/analytical-workspace-add.png)

5. Найдите PBIX-файл, содержащий определение аналитического отчета, а затем щелкните **Открыть**.

    ![Диалоговое окно "Выбор файла ресурса"](media/analytical-workspace-select-resource.png)
  
Теперь, когда вы добавили PBIX-файл как ресурс Dynamics 365, можно внедрить отчеты в рабочие области и добавить прямые ссылки с помощью пунктов меню.

# <a name="add-a-tab-control-to-an-application-workspace"></a>Добавление элемента управления вкладкой в рабочую область приложения
В этом примере мы расширим рабочую область **Управление резервированием** в "Управления автопарком", добавив вкладку **Аналитика** к определению формы **FMClerkWorkspace**.
 
На следующем рисунке показано, как выглядит форма **FMClerkWorkspace** в конструкторе в Microsoft Visual Studio.

![Форма FMClerkWorkspace до изменений](media/analytical-workspace-definition-before.png)

Выполните следующие шаги для расширения определения формы для рабочей области **Управление резервированием**.

1. Откройте конструктор форм для расширения определения конструктора.
2. В определении конструктора выберите верхний элемент, помеченный как **Дизайн | Шаблон: операционный, рабочая область**.
3. Щелкните правой кнопкой мыши, а затем выберите **Создать** > **Вкладка** для добавления нового элемента управления с именем **FormTabControl1**.
4. В конструкторе форм выберите **FormTabControl1**.
5. Щелкните правой кнопкой мыши, а затем выберите **Новая страница вкладки**, чтобы добавить новую страницу вкладки.
6. Переименуйте страницу вкладки на значимое имя, например **Рабочая область**.
7. В конструкторе форм выберите **FormTabControl1**.
8. Щелкните правой кнопкой мыши, а затем выберите **Новая страница вкладки**.
9. Переименуйте страницу вкладки на значимое имя, например **Аналитика**.
10. В конструкторе форм выберите **Аналитика (страница вкладки)**.
11. Задайте для свойства **Заголовок** значение **Аналитика**.
12. Щелкните правой кнопкой мыши элемент управления, а затем выберите **Создать** > **Группа** для добавления нового элемента управления группой форм.
13. Переименуйте группу форм на значимое имя, например **powerBIReportGroup**.
14. В конструкторе форм выберите **PanoramaBody (вкладка)**, а затем перетащите элемент управления на вкладку **Рабочая область**.
15. В определении конструктора выберите верхний элемент, помеченный как **Дизайн | Шаблон: операционный, рабочая область**.
16. Щелкните правой кнопкой мыши, а затем выберите **Удалить шаблон**.
17. Снова щелкните правой кнопкой мыши, а затем выберите **Добавить шаблон** > **Рабочая область с вкладками**.
18. Выполните сборку, чтобы проверить изменения.
 
На следующем рисунке показан дизайн после применения этих изменений.

![FMClerkWorkspace после изменений](media/analytical-workspace-definition-after.png)

Теперь, когда вы добавили элементы управления формой, которые будут использоваться для внедрения отчета рабочей области, необходимо определить размер родительского элемента управления, чтобы он соответствовал макету. По умолчанию обе страницы **Область фильтров** и **Вкладка** будут отображаться в отчете. Тем не менее, можно изменить видимость этих элементов управления в зависимости от целевого потребителя отчета.
 
> [!NOTE]
> Для встроенных рабочих областей рекомендуется использовать расширения, чтобы скрыть страницы **Область фильтров** и **Вкладка** для согласованности.
 
Вы завершили задачу расширения определения формы приложения. Дополнительные сведения о том, как использовать расширения для настройки, см. в разделе [Настройка: перекрытия и расширения](../extensibility/customization-overlayering-extensions.md).

# <a name="add-x-business-logic-to-embed-a-viewer-control"></a>Добавление бизнес-логики X ++ для внедрения элемента управления средством просмотра
Выполните следующие действия, чтобы добавить бизнес-логику, которая инициализирует элемент управления средством просмотра отчетов, который внедрен в рабочую область **Управление резервированием**.

1. Откройте конструктор форм **FMClerkWorkspace** для расширения определения конструктора.
2. Нажмите клавишу F7 для доступа к коду определения кода.
3. Добавьте следующий код X++:

    ```
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
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
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

4. Выполните сборку, чтобы проверить изменения.

Вы выполнили задачу по добавлению бизнес-логики для инициализации внедренного элемента управления средством просмотра отчетов. На следующем рисунке показана рабочая область после применения этих изменений.

![Отчет, внедренный в рабочую область](media/analytical-workspace-final.png)

> [!NOTE]
> Вы можете получить доступ к существующему операционному представлению с помощью вкладок рабочей области под заголовком страницы.

# <a name="reference"></a>Справка

## <a name="pbireporthelperinitializereportcontrol-method"></a>Метод PBIReportHelper.initializeReportControl
В этом разделе представлены сведения о вспомогательном классе, который используется для внедрения отчета Power BI (PBIXресурс) в элемент управления группой форм.

### <a name="syntax"></a>Синтаксис
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

### <a name="parameters"></a>Параметры

| Наименование | описание |
|---|---|
| resourceName | Имя PBIX-ресурса. |
| formGroupControl | Элемент управления группой форм, к которому применяется элемент управления отчетом Power BI. |
| defaultPageName | Имя страницы по умолчанию. |
| showFilterPane | Логическое значение, указывающее, должна ли отображаться область фильтров (**true**) или нет (**false**). |
| showNavPane | Логическое значение, указывающее, должна ли отображаться область перехода (**true**) или нет (**false**). |
| defaultFilters | Фильтры по умолчанию для отчета Power BI. |
