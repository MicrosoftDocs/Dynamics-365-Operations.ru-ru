---
title: Выпуск на склад
description: В этой статье приводятся сведения о процессе выпуска на склад. В нем описываются объекты, созданные при выпуске заказа на склад и параметры, которые можно использовать, чтобы инициировать процесс.
author: Mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: caa38c4ed1c7fb8cf1ead3ba6534f8405a5ff57f
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428045"
---
# <a name="release-to-warehouse"></a>Выпуск на склад

[!include [banner](../../includes/banner.md)]

В этой статье приводятся сведения о процессе выпуска на склад. В нем описываются объекты, созданные при выпуске заказа на склад и параметры, которые можно использовать, чтобы инициировать процесс.

## <a name="release-to-warehouse-overview"></a>Обзор выпуска на склад

Выпуск на склад — это процесс подготовки запасов к оправке При выпуске заказа на склад система создает строки загрузки и отгрузки. Если автоматическая обработка волн настроена, также создаются нагрузки и требуемые работы. Конфигурация используемых объектов зависит от параметров системы. В этом разделе статьи рассматриваются объекты, созданные в ходе процесса выпуска на склад, и параметры системы, определяющие их.

*Отгрузка* — это группа заказов на продажу или строк заказа на перемещение для одного и того же клиента или одного адреса поставки.

*Загрузка* — это группа заказов на продажу или строк заказа на перемещение, которые группируются вместе и обычно отправляются на одном грузовике, железнодорожном вагоне или другим способом транспортировки. Загрузка может иметь одну или несколько отгрузок. Загрузку можно создать вручную, добавляя строки заказа к новой загрузке. В этом случае для загрузки строки заказа назначаются до процесса выпуска на склад и они могут быть выпущены только на странице **Рабочее место планирования загрузки**.

*Работой* склада является любая складская операция, выполняемая работником склада. Как правило, рабочие операции склада состоят как минимум из двух последовательных действий: работник склада комплектует запасы в наличии в одном расположении и помещает их в другом расположении.

При выпуске заказов на склад система создает *строки загрузки* и группирует их в отгрузки. Процесс консолидации отгрузок позволяет автоматизировать консолидацию отгрузок во время процесса выпуска на склад. Дополнительные сведения см. в разделе [Обзор политик консолидации отгрузок](about-shipment-consolidation-policies.md).

Система использует *волны* для создания работы комплектации и загрузок для отгрузки. *Шаблон волны* должен быть доступен для типа волны, который требуется создать, и для склада строки заказа. Шаблоны волны типа *Отгрузка* используются, чтобы отгрузить номенклатуры для заказов на продажу и заказов на перемещение.

Каждый шаблон волны содержит *методы волны*. Методы волны выполняют такие действия, как создание работы для волны или создание загрузок. Например, шаблон волны для отгрузки может содержать методы для создания загрузок, распределения строк по волнам, пополнения и создания работы комплектации для волны. Шаблон волны задает параметры, определяющие, как волна будет генерироваться и обрабатываться, какие должны выполняться вручную, и какие — автоматически. Дополнительные сведения см. в разделе [Шаблоны волн](wave-templates.md). Таким образом, в зависимости от настройки шаблона волны, волна автоматически создается, обрабатывается и выпускается при выпуске заказа на склад, а некоторые или все эти действия выполняются вручную после выполнения выпуска на склад.

При обработке волны система создает работу комплектации, основываясь на подходящем *шаблоне работы* и *директиве местонахождения*, и делает эту работу доступной на мобильных устройствах. Шаблон работы определяет, как работа выполняется для каждого складского процесса, а в директиве местонахождения указывается места комплектации и размещения для движения запасов. Дополнительные сведения см. в разделе [Контроль работы склада с использованием шаблонов работы и директив местонахождения](control-warehouse-location-directives.md).

> [!NOTE]
> По умолчанию волны обрабатываются в пакетном режиме.

Во время обработки волн система обычно создает новую загрузку для каждой отгрузки, для которой не назначена загрузка. Если требуется, чтобы система назначила не назначенные отгрузки существующим загрузкам, можно использовать функции расширенного формирования загрузки волны. Дополнительные сведения см. в разделе [Расширенное формирование загрузок во время волны](advanced-load-building-during-wave.md).

На страницах **заказы на продажу** и **Заказы на перемещение** можно просмотреть объекты, созданные для строк заказа в процессе выпуска на склад.

- Страница **Заказы на продажу**:

    - На экспресс-вкладке **строки заказа на продажу** выберите **Склад**, а затем в меню выберите пункт **Сведения об отгрузке**, чтобы открыть соответствующие отгрузки, **Сведения о загрузке**, чтобы открыть соответствующие загрузки или **Сведения о работе**, чтобы открыть соответствующие сведения о работе.
    - На экспресс-вкладке **Сведения по строке** выберите вкладку **Загрузка** для рассмотрения соответствующих загрузок.

- Страница **Заказы на перемещение**:

    - В области действий на вкладке **Отгрузка** выберите **Сведения об отгрузке**, чтобы открыть соответствующие отгрузки или **Сведения о загрузке** для открытия соответствующих загрузок.
    - На экспресс-вкладке **Строки заказа на перемещение** выберите **сведения о работе**, чтобы открыть соответствующие сведения о работе.

В заключение, когда заказ выпускается на склад, самый автоматизированный поток используется следующим образом:

1. Система создает отгрузку для заказа и волны.
1. Волна обрабатывается.
1. Система создает загрузку и код работы.

В зависимости от настроек шаблона волны, шаблонов работы и директив местонахождения, некоторые шаги этого потока могут выполняться вручную. Однако общий поток остается тем же.

Имеется несколько способов выпуска заказа на склад. Операцию можно выполнить вручную или можно настроить пакетное задание. В остальных разделах этой статьи подробно рассмотрены различные способы выполнения выпуска для складской операции.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Выпуск вручную на склад из страниц заказы на продажу и заказы на перемещение

Можно выпустить заказ на склад непосредственно со страницы **заказы на продажу** или со страницы **заказы на перемещение**, выбрав **выпустить на склад**.

- На странице **заказы на продажу** кнопка находится на вкладке **склад** в области действий.
- На странице **Заказы на перемещение** кнопка находится на вкладке **Отгрузка** в области действий.

На странице **заказы на продажу** можно одновременно выпустить несколько заказов на продажу.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Выпуск вручную на склад со страниц "Выпуск на склад"

В настоящее время на компьютере имеется три страницы, на которых можно просмотреть строки для нескольких заказов и выпустить их на склад:

- **Выпуск на склад** (**Управление складом \> Выпуск на склад \> Выпуск на склад**) — эта страница позволяет работать с заказами на продажу и заказами на перемещение. Однако она обеспечивает более низкую производительность, чем остальные две страницы. Эта страница скоро станет устаревшей.
- **Выпуск заказов на продажу на склад** (**Управление складом \> Выпуск на склад \> Выпуск заказов на продажу на склад**) — эта страница позволяет работать только с заказами на продажу. Однако он обеспечивает лучшую производительность , чем страница запуск **Выпуск на склад**.
- **Выпуск заказов на перемещение на склад** (**Управление складом \> Выпуск на склад \> Выпуск заказов на перемещение на склад**) — эта страница позволяет работать только с заказами на перемещение. Однако он обеспечивает лучшую производительность , чем страница запуск **Выпуск на склад**.

Все три страницы обеспечивают аналогичные функциональные возможности, как это описано в оставшейся части этого раздела. Все они позволяют выбрать строки заказа или целые заказы, а затем выпустить их на склад.

Каждая страница состоит из верхнего раздела, в которой можно выбрать строки заказа и нижнего раздела, в которой можно запустить процесс выпуска на склад. Можно использовать фильтры в верхней области для поиска строк заказа на продажу, которые необходимо выпустить. Страница **Выпуск на склад** предоставляет отдельную вкладку для заказов на продажу и заказов на перемещение в верхней области, в то время как каждая из двух других страниц показывает только один тип заказа.

Панель инструментов в верхней секции содержит следующие кнопки, которые можно использовать для выбора строк заказа для выпуска на склад:

- **Добавить** — выберите одну или несколько строк заказа в верхней области, а затем выберите эту кнопку для этих строк в нижней области.
- **Добавить все** — добавление всех строк из верхнего раздела в нижний раздел.
- **Добавить заказ** — выберите заказ, а затем нажмите эту кнопку, чтобы добавить все строки из этого заказа в нижнюю секцию.

После завершения добавления строк к нижнему разделу пометьте каждую строку, которую необходимо выпустить. Затем выберите **Выпуск на склад** на панели инструментов, чтобы выпустить эти строки на склад.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Команда "Выпуск на склад вручную" на странице "Рабочее место планирования загрузки"

Можно также вручную выпустить заказы на склад, используя страницу **Рабочее место планирования загрузки**. Эта страница позволяет объединить строки заказа в загрузки, а затем выпустить эти загрузки на склад.

Чтобы открыть страницу **Рабочее место планирования загрузки**, перейдите к **Управление складом \> Загрузки**. Ее можно также открыть на страницах **заказы на продажу** и **Заказы на перемещение**. В верхней части страницы можно выбрать строки заказа на продажу на вкладке **строки продаж** и в строках заказа на перемещение на вкладке **строки перемещения**, а затем добавить эти строки к новой или существующей загрузке.

Вкладка **поставка и спрос** в области действий содержит следующие кнопки, которые можно использовать для добавления строк заказа в верхнем разделе к загрузке:

- **В новую загрузку** — выберите одну или несколько строк заказа в верхней области, а затем выберите эту кнопку для создания новой загрузки и добавления этих строк в нее.
- **В существующую загрузку** — выберите одну или несколько строк заказа в верхней области, а затем выберите эту кнопку для добавления этих строк в существующую загрузку.
- **Весь заказ в новую загрузку** — выберите заказы, а затем выберите эту кнопку для создания новой загрузки и добавления всех строк из этих заказов в нее.
- **Весь заказ в существующую загрузку** — выберите заказ, а затем выберите эту кнопку для добавления всех строк из этого заказа в существующую загрузку.

В нижней области можно просмотреть созданные загрузки. Чтобы выпустить загрузки на склад, выберите их, затем выберите **Выпуск \> Выпуск на склад** на панели инструментов. При использовании автоматической обработки волны, поскольку загрузки уже назначены строкам заказа, система создает отгрузки и коды работ, когда выполняется операция выпуска на склад.

## <a name="automatic-release-to-the-warehouse"></a>Автоматический выпуск на склад

Для автоматического выпуска заказов на склад следует использовать задания **Автоматический выпуск заказов на продажу** и **Автоматический выпуск заказов на перемещение**.

Чтобы настроить пакетное задание для выпуска заказов на продажу, выполните следующие действия.

1. Перейдите на **Управление складом \> Запуск на склад \> Автоматический выпуск заказов на продажу**.
1. В диалоговом окне **Автоматический выпуск заказов на продажу** на экспресс-вкладке **Параметры** установите следующие поля:

    - **Количество для выпуска** — выберите, следует ли выпускать на склад все количество или только физически зарезервированное количество.
    - **Разрешить выпуск частично выпущенных заказов** — укажите, должны ли оставшиеся количества частично выпущенных заказов выпускаться на склад.
    - **Сохранять резервирования при сбое выпуска** — укажите, должны ли количества, которые были автоматически зарезервированы для заказа на продажу, оставаться зарезервированными в случае сбоя процесса выпуска на склад.
    - **Группировать выпуски по клиенту** — укажите, должна ли система обрабатывать операции выпуска на склад отдельно для каждого клиента или же выпускать все заказы на продажу одновременно. Если для этого параметра задано значение *Да*, система будет собирать все строки заказов на продажу для выбранного клиента, выпускать эти заказы на склад, а затем обрабатывать следующего клиента. Если для этого параметра задано значение *Нет*, система будет выпускать все доступные строки заказов на продажу в одной операции выпуска на склад. Включив этот параметр, можно повысить производительность и устойчивость процесса выпуска на склад. Однако будьте осторожны при использовании этого параметра вместе с шаблонами волн, для которых включена обработка волны перед выпуском на склад, поскольку это сочетание может создать множество волн с одним клиентом, в каждой из которых будет работа, которая была создана только для данного клиента. Если требуется создать работу, объединяющую отгрузки для нескольких клиентов, следует отключить параметр *Группировать выпуски по клиенту* или настроить шаблоны волн для использования отложенной обработки.
    - **Обработка заблокированных заказов** — выберите, как система должна обрабатывать заказы на продажу, которые в настоящее время заблокированы, поскольку они редактируются другими пользователями или процессами:

        - *Дожидаться разблокировки заказов* — система должна ожидать разблокирования заказов, прежде чем они будут выпущены на склад. В этом случае процесс выпуска на склад может занять больше времени.
        - *Пропустить заблокированные заказы* — система должна пропустить заблокированные заказы.

    - **Допустимые типы заказов** — выберите типы заказов на продажу, которые будут включены в пакет.
    - **Тип кредитного лимита** — выберите, следует ли выполнять проверки кредитного лимита во время процесса выпуска на склад, и, если необходимо выполнить эти проверки, сведения о проводках, которые будут включены в эти проверки.

1. Чтобы контролировать порядок обработки заказов, на экспресс-вкладке **Включаемые записи** выберите **Фильтр**. Появится стандартное диалоговое окно запроса, в котором можно определить критерии выбора, критерии сортировки и соединения. Поля работают так же, как они работают для других типов запросов в Microsoft Dynamics 365 Supply Chain Management.
1. На экспресс-вкладке **Выполнять в фоновый режиме** выберите, должно ли задание выполняться в пакетном режиме, и/или настройте повторяющийся график. Поля работают так же, как они работают для других типов [фоновых заданий](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) в Supply Chain Management.
1. Нажмите кнопку **ОК**, чтобы применить параметры, и инициировать процесс выпуска на склад

Чтобы настроить пакетное задание для выпуска заказов на перемещение, выполните следующие действия.

1. Перейдите на **Управление складом \> Запуск на склад \> Автоматический выпуск заказов на перемещение**.
1. В диалоговом окне **Автоматический выпуск заказов на перемещение** на экспресс-вкладке **Параметры** установите следующие поля:

    - **Количество для выпуска** — выберите, следует ли выпускать на склад все количество или только физически зарезервированное количество.
    - **Разрешить выпуск частично выпущенных заказов** — укажите, должны ли оставшиеся количества частично выпущенных заказов выпускаться на склад.
    - **Группировать выпуски по складу назначения** — указывается, должны ли в системе запускаться все заказы на перемещение в одно и то же время, или же они должны сгруппировать строки заказа на перемещение по складу назначения, а затем выпустить каждую группу на склад отдельно.

1. Чтобы контролировать порядок обработки заказов, на экспресс-вкладке **Включаемые записи** выберите **Фильтр**. Появится стандартное диалоговое окно запроса, в котором можно определить критерии выбора, критерии сортировки и соединения. Поля работают так же, как они работают для других типов запросов в Supply Chain Management.
1. На экспресс-вкладке **Выполнять в фоновый режиме** выберите, должно ли задание выполняться в пакетном режиме, и/или настройте повторяющийся график. Поля работают так же, как они работают для других типов [фоновых заданий](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) в Supply Chain Management.
1. Нажмите кнопку **ОК**, чтобы применить параметры, и инициировать процесс выпуска на склад

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
