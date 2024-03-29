---
title: Маршруты и операции
description: Эта статья содержит сведения о маршрутах и операциях.
author: johanhoffmann
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable, ProdRouteJob, ProdRouteTrans, ProdRouteOverview, ProdRouteJobOverview, ProdRouteJobListPagePreviewPane, RouteTable, RouteVersionFeasibility, ProdRouteJobCurrent, RouteGroup, RouteProductionOrder, EngChgCaseRouteTablePart, EcoResProductProdTypeFormulaNoActiveRouteFormPart,
ms.author: johanho
audience: Application User
ms.reviewer: kamaybac
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 103c7007cd002c5953d096ff6001a93c4936b702
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856029"
---
# <a name="routes-and-operations"></a>Маршруты и операции

[!include [banner](../includes/banner.md)]

Эта статья содержит сведения о маршрутах и операциях. Маршрут определяет процесс для производства продукта или варианта продукта. Он описывает каждый шаг (операцию) в производственном процессе и порядок, в котором следует выполнять эти шаги. Для каждого шага маршрут также определяет необходимые операционные ресурсы, необходимое время настройки и время выполнения, а также порядок расчета затрат.

## <a name="overview"></a>Обзор

Маршрут описывает последовательность операций, необходимую для производства продукта или варианта продукта. Для каждой операции маршрут также определяет необходимые операционные ресурсы, время, необходимое для настройки и выполнения операции, а также порядок расчета затрат. Один и тот же маршрут можно использовать для производства нескольких продуктов, или можно определить уникальный маршрут для каждого продукта или варианта продукта. Можно даже иметь несколько маршрутов для одного продукта. В этом случае используемый маршрут зависит от таких факторов, как количество, которое должно быть произведено. Определение маршрута в Supply Chain Management состоит из четырех отдельных элементов, которые совместно описывают производственный процесс:

- **Маршрут** — маршрут определяет структуру производственного процесса. Другими словами, он определяет порядок операций.
- **Операция** — операция определяет именованный этап в маршруте, например **Сборка**. Одна и та же операция может использоваться в нескольких маршрутах или может иметь различные номера операции.
- **Связь операции** — связь операции определяет рабочие свойства операции, например время настройки и время выполнения, категории затрат, параметры потребления и потребности в ресурсах. Связь операции позволяет изменять рабочие свойства операции в зависимости от маршрута, в котором используется операция, или производимых продуктов.
- **Версия маршрута** — версия маршрута определяет маршрут, используемый для производства продукта или варианта продукта. Версии маршрута позволяют повторно использовать маршруты для нескольких продуктов или изменять их со временем. Они также позволяют использовать разные маршруты для производства одного продукта. В этом случае используемый маршрут зависит от таких факторов, как местонахождение или количество, которое должно быть произведено.

## <a name="routes"></a>Маршруты
Маршрут описывает последовательность операций, используемую для производства продукта или варианта продукта. Каждой операции присвоен номер операции и последующая операция. Порядок операций формирует маршрутную сеть, которая может быть представлена направленной диаграммой с одной или несколькими начальными точками и одной конечной точкой. В Supply Chain Management маршруты различаются в зависимости от типа структуры. Существует два типа маршрутов: простые маршруты и маршрутные сети. В параметрах управления производством можно указать, могут ли использоваться только простые маршруты или возможно использование более сложных маршрутных сетей.

### <a name="simple-routes"></a>Простые маршруты

Простой маршрут является последовательным и имеет только одну начальную точку маршрута.  

[![Простой маршрут.](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Если в параметрах управления производством включены только простые маршруты, при определении маршрута Supply Chain Management автоматически создает номера операций (10, 20, 30 и т. д.).

### <a name="route-networks"></a>Маршрутные сети

Если включить в параметрах управления производством более сложные маршрутные сети, можно определить маршруты, которые имеют несколько начальных точек, и операции в которых могут выполняться параллельно.  

[![Маршрутная сеть.](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

> [!NOTE]
> - Каждая операция может иметь только одну последующую операцию, а весь маршрут должен заканчиваться одной операцией.
> - Это не гарантирует, что несколько операций, которые имеют одну и ту же последующую операцию (например, операции 30 и 40 на приведенном выше рисунке) действительно будут выполняться параллельно. Доступность и мощности ресурсов могут накладывать ограничения на то, как планируются эти операции.
> - Не допускается использовать 0 (ноль) в качестве номера операции. Этот номер зарезервирован и используется для указания, что последняя операция в маршруте не имеет последующей операции.

### <a name="parallel-operations"></a>Параллельные операции

В некоторых случаях для выполнения операции требуется сочетание нескольких операционных ресурсов, имеющих различные характеристики. Например, для операции сборки могут потребоваться станок, инструмент и один работник на каждые два станка для наблюдения за операцией. Этот пример можно смоделировать с использованием параллельных операций, где одна операция назначается в качестве основной операции, а остальные являются дополнительными.  

[![Маршрут с основной и дополнительными операциями.](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Как правило, основная операция представляет собой минимальный (ограничивающий) ресурс и определяет время выполнения для дополнительных операций. Однако во время планирования, которое включает ограничения по мощности, ресурсы, которые запланированы как для основной операции, так и для дополнительных операций, должны быть доступны и иметь свободную мощность в одно и то же время.  

Основная операция и дополнительные операции должны иметь один и тот же номер операции (30 на приведенном выше рисунке).  

В предыдущем примере потребность в ресурсах для основной операции (30) — это станок, тогда как потребность в ресурсах для дополнительных операций (30' и 30'') — это инструмент и работник. 50% нагрузка гарантирует, что запланированный работник может наблюдать за двумя станками одновременно.

### <a name="approval-of-routes"></a>Утверждение маршрутов

Маршрут должен быть утвержден, прежде чем его можно будет использовать в процессе планирования или производства. Утверждение указывает, что разработка маршрута завершена. Один и тот же выпущенный продукта или вариант продукта может иметь несколько утвержденных маршрутов. Обычно маршрут утверждается при утверждении первой соответствующей версии маршрута. Однако в некоторых бизнес-сценариях утверждение маршрута и версии маршрута являются отдельными действиями, в которых могут участвовать различные владельцы процессов.  

Каждый маршрут можно утвердить или не утвердить отдельно. Однако обратите внимание, что если маршрут не утвержден, все связанные версии маршрута также не будут утверждены. В параметрах управления производством можно указать, могут ли маршруты быть неутвержденными и возможно ли изменение утвержденных маршрутов.  

Если необходимо вести журнал записей, которые утверждают каждый маршрут, можно требовать электронные подписи для утверждения маршрута. Пользователям будет необходимо подтвердить свою подлинность с помощью [электронной подписи](../../fin-ops-core/fin-ops/organization-administration/electronic-signature-overview.md).

## <a name="operations"></a>Operations
Операция является шагом производственного процесса. Каждая операция имеет код и простое описание. В следующих таблицах приведены типичные примеры операций в цехе.

| Операция  | описание        |
|------------|--------------------|
| PipeCut    | Обрезка трубы       |
| TIGweld    | Дуговая сварка        |
| JigAssy    | Сборка в оправке       |
| Инвентаризация | Контроль качества |

Рабочие свойства операции, например время настройки и время выполнения, потребности в ресурсах, сведения о затратах и расчеты потребления указываются в связи операции. (Дополнительные сведения о связях операций см. в следующем разделе.)

## <a name="operation-relations"></a>Связи операции
Следующие рабочие свойства операции сохраняются в связи операции:

- Категории затрат
- Параметры потребления
- Значения времени обработки
- Количества для обработки
- Потребности ресурса
- Примечания и инструкции

Можно определить несколько связей операций для одной операции. Однако каждая связь операции относится к одной операции и хранит свойства, характерные для маршрута, выпущенного продукта или набора выпущенных продуктов, которые относятся к группе номенклатур. Таким образом одна операция может использовать в нескольких маршрутах с различными рабочими свойствами. Кроме того, можно упростить ведение основных данных, если использовать стандартные операций, которые имеют одинаковые рабочие свойства независимо от используемого маршрута и производимого продукта. Область действия связи операции определяется с помощью свойств **Код номенклатуры**, **Связь номенклатуры**, **Код маршрута** и **Связь маршрута**, как показано в следующей таблице.

| Код номенклатуры | Связь номенклатуры         | Код маршрута | Связь маршрута   | Область действия связи операции                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Таблица     | &lt;Код номенклатуры&gt;       | Маршрут      | &lt;Код маршрута&gt; | Рабочие свойства операции, когда она используется в маршруте, где **Номер маршрута**=&lt;Код маршрута&gt;, для производства выпущенного продукта, где **Номер номенклатуры**=&lt;Код номенклатуры&gt;.                                                                                                                        |
| Таблица     | &lt;Код номенклатуры&gt;       | Все        |                  | Рабочие свойства операции по умолчанию, когда она используется в маршруте, где **Номер маршрута**=&lt;Код маршрута&gt;. Иными словами, эти рабочие свойства применяются при наличии не зависящей от маршрута связи операции для выпущенного продукта.                                     |
| Групповое     | &lt;Код номенклатурной группы&gt; | Маршрут      | &lt;Код маршрута&gt; | Рабочие свойства операции при использовании в маршруте, где **Номер маршрута**=&lt;Код маршрута&gt;, для производства запущенных в производство продуктов, которые связаны с группой номенклатур &lt;Код номенклатурной группы&gt;, кроме случая, когда существует специфичная для маршрута связь операции для запущенного в производство продукта.                         |
| Групповое     | &lt;Код номенклатурной группы&gt; | Все        |                  | Рабочие свойства операции по умолчанию для операции, когда она используется для производства запущенных в производство продуктов, которые связаны с группой номенклатур &lt;Код номенклатурной группы&gt;, если не существует более конкретная связь операции.                                                                                                  |
| Все       |                       | Маршрут      | &lt;Код маршрута&gt; | Рабочие свойства операции по умолчанию, когда она используется в маршруте, где **Номер маршрута**=&lt;Код маршрута&gt;. Иными словами, эти рабочие свойства применяются, когда нет связи операции для этого маршрута, которая специфична для запущенного в производство продукта или связанной с ним номенклатурной группы. |
| Все       |                       | Все        |                  | Рабочие свойства операции по умолчанию. Эти рабочие свойства применяется, когда более конкретная связь операции не существует.                                                                                                                                                                |

Можно также указать, что связь операции относится к площадке. Таким образом рабочие свойства операции могут отличаться в зависимости от местоположения (т. е., площадки), где эта операция выполняется. Для сконфигурированных продуктов можно также указать различные рабочие свойства для каждой конфигурации продукта.  

Связи операции дают большую гибкость при определении маршрутов. Кроме того, возможность определять свойства по умолчанию помогает сократить объем основных данных, которые необходимо поддерживать. Однако эта гибкость также означает, что вы должны помнить о контексте, в котором изменяете связь операции.  

> [!NOTE]
> Поскольку рабочие свойства сохраняются в связях операций по операциям для каждого маршрута, все вхождения одной и той же операции (например, "Сборка") имеют одинаковые время настройки, время выполнения и потребности в ресурсах. Поэтому если два вхождения операции необходимы в одном маршруте, но они имеют разное время выполнения, необходимо создать две отдельные операции, такие как Сборка1 и Сборка2.

### <a name="modifying-product-specific-routes"></a>Изменение маршрутов для конкретного продукта

При открытии страницы **Маршрут** со страницы **Сведения об используемом продукте** отображаются версии маршрута, которые связаны с выбранным запущенным в производство продуктом. В этом контексте для каждой операции Supply Chain Management отображает рабочие свойства из связи операции, которые наилучшим образом соответствуют версии маршрута. Можно заметить, что список операций включает в себя свойства **Код номенклатуры** и **Код маршрута** из связи операции. Таким образом можно определить, какая связь операции отображается.  

На странице **Маршрут** можно изменить рабочие свойства операции, например время выполнения или категории затрат. Изменения сохраняются в связи операции, которая специфична для маршрута и запущенного в производство продукта, указанных в текущей версии маршрута. Если связь операции, которая отображается, не является специфичной для маршрута и запущенного в производство продукта, перед сохранением изменений система создает копию связи операции. Эта копия *является* специфичной для маршрута и запущенного в производство продукта. Поэтому ваши изменения не повлияют на другие маршруты или запущенные в производство продукты. Чтобы проверить, какие связи операции изменяется на странице **Маршрут**, просмотрите на поля **Код номенклатуры** и **Код маршрута**.  

Можно также вручную создать операцию, специфичную для маршрута и запущенного в производство продукта, с помощью функции **Копировать и редактировать связь**.  

> [!NOTE]
> При добавлении новой операции к маршруту на странице **Маршрут** связь операции создается только для текущего запущенного в производство продукта. Таким образом, если маршрут используется также для производства других запущенных в производство продуктов, применяемая связь операции не будет существовать для этих запущенных в производство продуктов, и маршрут больше не может использоваться для этих запущенных в производство продуктов.

### <a name="maintaining-operation-relations-per-route"></a>Ведение связей операций по маршрутам

При открытии страницы **Сведения о маршруте** со страницы списка **Маршруты** отображается список всех связей операций, которые применяются к выбранному маршруту. Таким образом вы можете легко проверить, какие рабочие свойства используются для каких продуктов. Можно изменить как значения свойств по умолчанию, так и значения свойств для конкретного продукта.  

Если добавить новую связь операции на странице **Сведения о маршруте**, в поле **Код маршрута** автоматически устанавливается значение **Маршрут**, а в поле **Связь маршрута** устанавливается номер маршрута для текущего маршрута.

### <a name="maintaining-operation-relations-per-operation"></a>Ведение связей операций по операциям

Со страницы **Операции** можно открыть страницу **Связи операции**. На этой странице можно изменять все связи операции для определенной операции. Можно даже изменить связи операции, которые содержат значения по умолчанию.  

Если организация использует стандартные операции, и если рабочие параметры одинаковы для всех продуктов и процессов, страница **Связи операции** предоставляет удобный способ поддержки рабочих свойств по умолчанию для этих операций.

### <a name="applying-operation-relations"></a>Применение связей операций

В некоторых случаях Supply Chain Management необходимо найти рабочие свойства для операции. Например, при создании заказа на покупку рабочие свойства каждой операции должны быть скопированы из связей операции для маршрута производства. В таких случаях Supply Chain Management выполняет поиск соответствующий связей операций в порядке от наиболее конкретного сочетания до наименее конкретного сочетания.  

Когда Supply Chain Management ищет наиболее подходящую связь операции для запущенного в производство продукта, связи операций, соответствующая коду номенклатуры запущенного в производство продукта, является более предпочтительной, чем связь операции, соответствующая коду номенклатурной группы. В свою очередь, связь операций, соответствующая коду номенклатурной группы, является более предпочтительной, чем связь операции по умолчанию. Поиск выполняется в следующем порядке:

1.  **Код номенклатуры**=**Таблица** и **Связь номенклатуры**=&lt;код номенклатуры&gt;
2.  **Код номенклатуры**=**Группа** и **Связь номенклатуры**=&lt;код номенклатурной группы&gt;
3.  **Код номенклатуры**=**Все**
4.  **Код маршрута**=**Маршрут** и **Связь маршрута**=&lt;код маршрута&gt;
5.  **Код маршрута**=**Все**
6.  **Конфигурация**=&lt;код конфигурации&gt;
7.  **Конфигурация**=
8.  **Сайт**=&lt;код сайта&gt;
9.  **Сайт**=

Таким образом, операция должна использоваться только один раз для каждого маршрута. Если операция выполняется несколько раз в одном маршруте, все вхождения этой операции будут иметь одинаковую связь операции и вы не сможете задавать различные свойства (например, время выполнения) для каждого экземпляра.

## <a name="route-versions"></a>Версии маршрута

Версии маршрута используются для учета возможных вариантов производства продуктов или для обеспечения большей управляемости производственного процесса. Они определяют, какой маршрут следует использовать при производстве конкретного выпущенного продукта или варианта выпущенного продукта. Чтобы определить, какой маршрут используется для выпущенного продукта, можно использовать следующие ограничения:

- Аналитики продукта (размер, цвет, стиль или конфигурация)
- Количество в производстве
- Сайт производства
- Дата производства

Когда вы производите продукт на определенном сайте, в определенном количестве или в определенный период, можно назначить определенную версию маршрута в качестве версии маршрута по умолчанию. Однако обратите внимание, что только один активный маршрут допускается для конкретного выпущенного продукта и конкретного набора ограничений.  

В параметрах управления производством можно потребовать, чтобы всегда был указан срок действия версии маршрута.

### <a name="approval-of-route-versions"></a>Утверждение версий маршрута

Прежде чем маршрут можно будет использовать в процессе планирования или производства, он должен быть утвержден. При утверждении версии маршрута вы также утверждаете связанный маршрут. Однако обратите внимание, что версия маршрута может быть утверждена только в случае, если связанный маршрут также утвержден.

### <a name="activating-the-default-route-version"></a>Активация версии маршрута по умолчанию

При активации версии маршрута он назначается как версия маршрута по умолчанию, которая будет использоваться в сводном планировании или которая будет использоваться для создания производственных заказов. Можно иметь только одну активную версию маршрута для данного набора ограничений (например, период, сайт или количество). Если версия, что вы пытаетесь активировать, конфликтует с уже активной версией, вы получаете сообщение об ошибке. Чтобы предотвратить неоднозначную активацию, следует либо деактивировать конфликтующую версию, либо изменить ограничения версии (обычно период).

### <a name="electronic-signatures"></a>Электронные подписи

Если необходимо вести журнал записей, которые утверждают и активируют каждую версию маршрута, можно требовать электронные подписи для этих задач. Тогда пользователи, которые утверждают и активируют версии маршрута, должны будут подтверждать свою личность, используя [электронную подпись](../../fin-ops-core/fin-ops/organization-administration/electronic-signature-overview.md).

### <a name="product-change-that-uses-case-management"></a>Изменение продукта, которое использует управление запросами

Запрос изменения продукта для утверждения и активации новых или измененных маршрутов или версий маршрутов предоставляет простой способ просмотреть обзор ограничений версии маршрута. Можно также утвердить и активировать все маршруты, которые относятся к определенному изменению в одной операции и задокументировать результаты в запросе изменения продукта.

## <a name="maintaining-routes"></a>Ведение маршрутов

В зависимости от бизнес-требований можно сократить усилия, необходимые для ведения определений процессов.

### <a name="making-routes-independent-of-resources"></a>Создание независящих от ресурсов маршрутов

Во многих системах операционный ресурс или группа ресурсов, которые должны выполнять операцию, должны быть указаны в маршруте. Однако в Supply Chain Management можно определить набор требований, которым должен удовлетворять операционный ресурс, чтобы он был применим для операции. Таким образом, конкретный операционный ресурс или группа ресурсов, которые следует использовать, не обязательно должны быть определены до момента фактического планирования операции. Эта функция особенно полезна, если имеется много работников или станков, которые могут выполнить эту операцию.  

Например, вы указали, что для операции требуется операционный ресурс типа **Станок**, который имеет способность **Штамповка** с усилием 20 тонн. Механизм планирования будет затем разрешать эти требования, выбирая конкретный операционный ресурс или группу ресурсов при планировании операции. Поскольку можно просто указать эти требования вместо привязки операции к конкретному станку, гибкость значительно повышается. Кроме того, обслуживание будет проще, если ресурсы перемещаются или добавляются новые ресурсы.  

Дополнительные сведения о различных типах потребностей в ресурсах и порядке их использования см. в разделе "Потребности в операционных ресурсах" и [Возможности ресурса](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Совместное использование маршрутов для сайтов

Если один и тот же продукт производится на нескольких производственных площадках (сайтах) и шаги для производства продукта одинаковы на всех площадках, часто можно разработать общий маршрут, который будет использоваться на всех производственных площадках. Чтобы создать общий маршрут, не указывайте площадку в самом маршруте. Однако по-прежнему необходимо создать версию маршрута, которая связывает общий маршрут с продуктом на каждой площадке.  

Необходимо также убедиться, что требования к ресурсам для каждой операции в маршруте не относятся к конкретным операционным ресурсам или группам ресурсов, а выражены в терминах характеристик необходимых ресурсов. Тогда механизм планирования сможет назначать соответствующие операционные ресурсы с площадки, на которой запланировано производство. Например, если имеются небольшие различия во времени выполнения или если время настройки для определенной операции зависит от конкретной площадки, можно указать эту информацию, добавив дополнительную связь операции для данной площадки.  

Чтобы воспользоваться всеми преимуществами общих маршрутов, также следует использовать потребление ресурсов по соответствующим спецификациям (BOM). При установке флага для потребления ресурса в строке спецификации, склад и местоположение, из которых должно потребляться сырье, определяется из операционных ресурсов, для которых планируется операция. Таким образом, склад и местонахождение не обязательно должны быть определены до момента фактического планирования производства. Таким образом можно сделать спецификации и маршрут независимыми от физического местоположения, в которой производится продукт.

### <a name="standard-operation-relations"></a>Стандартные связи операций

Если ваше предприятие использует стандартизированные операции в течение всего производства и если вариации времени настройки, времени выполнения, расчета потребления, расчета затрат и т. д. отсутствуют или незначительны, может быть удобно создать связи операций по умолчанию для всех операций. В этом случае следует избегать создания связей операций, которые относятся к какому-либо конкретному маршруту или выпускаемому продукту.  

Если вы также выражаете требования к ресурсам с точки зрения навыков или возможностей и создаете маршруты, не зависящие от площадки, это может помочь свести к минимуму текущее обслуживание ваших бизнес-процессов.  

При использовании этого подхода страница **Связи операции** страница становится основным местом для ведения значений времени выполнения и других свойств.

### <a name="resource-specific-process-times"></a>Специфичные для ресурсов значения времени обработки

Если не указывать операционный ресурс или группу ресурсов как часть требований к ресурсам для операции, соответствующие ресурсы могут работать на разных скоростях. Таким образом время, необходимое для выполнения операции, может быть различным. Чтобы решить эту проблему, можно использовать поле **Формула** в связи операции для указания способа расчета времени выполнения. Имеются следующие варианты:

- **Стандартный** — (вариант по умолчанию) в расчетах используются только поля из связи операции, и указанное время выполнения умножается на количество по заказу.
- **Мощность** — вычисление включает поле **Мощность** из операционного ресурса. Поэтому время зависит от ресурса. Значение, указанное в операционном ресурсе, является производительностью в час. **Время выполнения** рассчитывается как **Количество заказа**, разделенное на **Мощность**. Значение по мощности не зависит от конкретной единицы измерения и, следовательно, не конвертируется на основе поля **Единица измерения емкости**, которое является просто описательным полем, которое не используется в расчетах.
- **Партия** — производительность в партиях вычисляется с помощью данных из связи операции. Количество партий и, следовательно, время выполнения затем вычисляется на основе количества по заказу.
- **Пакет ресурсов** — этот вариант в целом аналогичен варианту **Партия**. Однако вычисление включает поле **Объем пакета** из операционного ресурса. Поэтому время зависит от ресурса.

### <a name="set-up-route-groups"></a>Настройка группы маршрутов

Можно определить маршрутные группы и настройку для их типов маршрута или заданий в разделе **Управление производством > Настройка > Маршруты > Группы маршрутов**. Для каждого типа маршрута/задания в маршрутной группе можно установить или снять следующие параметры:

- **Активация** — выберите этот вариант, чтобы включать расчеты и планирование для выбранного типа задания и получать обратную связь задания при запуске планирования заданий. Необходимо выбрать этот параметр, чтобы включить тип задания, а затем выберите другие параметры для этого типа заданий. Если активация не выбрана, этот тип заданий не будет включен, независимо от выбора других параметров. 
- **Управление заданиями** — выберите этот параметр, чтобы включить тип заданий для управления заданиями при запуске планирования заданий. 
- **Рабочее время** — выберите этот параметр, чтобы запланировать тип задания по календарю рабочего времени, указанный для операционного ресурса; в противном случае используется григорианский календарь. Для планирования рабочего времени можно пользоваться григорианским календарем или определенным рабочим календарем. Если этот флажок установлен, планирование основано на конкретном календаре рабочего времени. Кроме того, задание типа "Задание" запланировано от полуночи на дату, указанную в качестве начальной задания.
- **Мощность** — выберите этот параметр, чтобы зарезервировать мощность для типа задания во время планирования заданий. Если этот флажок установлен, мощность резервируется, если планирование выполняется для выбранного типа задания. Это дает понимание того, какие типы заданий в каждой маршрутной группе используют операционные ресурсы. Например, в ситуации, когда ресурсы сушки ограничены, эти ресурсы необходимо указать в качестве таковых. Операции сушки, которые назначены в очередь типов заданий, резервируют сушильные ресурсы. 

Для каждого из типов заданий необходимо сначала активировать или отключить его. Если деактивирован, ни одна из других настроек (Управление заданиями, рабочее время и мощность) не будет рассматриваться, так как тип задания не будет активен. 

Среди типов заданий можно найти перекрытие. Перекрытие позволяет выполнять различные задания в одно и то же время. Если задания перекрываются, ресурсы можно использовать, но их нельзя зарезервировать для определенных заданий.
Таким образом, если активация выбрана для перекрытия, остальные параметры (Управление заданиями, рабочее время и мощность) никак не влияют на маршрутную группу. 

> [!NOTE]
> При обновлении версии может возникнуть следующее сообщение об ошибке: **"Ошибка CLR при вызове ядра планирования"**. Если эта ошибка возникает, перейдите на страницу **Маршрутные группы** и для всех маршрутов, где был активирован параметр **Перекрытие** снимите флажки **Управление заданиями**, **Рабочее время** и **Мощность**. 

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Спецификации и формулы](bill-of-material-bom.md)

- [Категории затрат, используемые в маршрутизации производства](../cost-management/cost-categories-used-production-routings.md)

- [Возможности ресурса](resource-capabilities.md)

- [Обзор электронной подписи](../../fin-ops-core/fin-ops/organization-administration/electronic-signature-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]