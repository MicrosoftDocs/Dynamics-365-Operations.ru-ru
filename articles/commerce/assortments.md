---
title: Управление ассортиментами
description: В этой статье описываются основные понятия управления ассортиментом в Dynamics 365 Commerce и обсуждаются вопросы реализации для вашего проекта.
author: josaw1
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.openlocfilehash: 255e0ccfd9e5cb41cdd0a3713d611f1e8008aadf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279717"
---
# <a name="assortment-management"></a>Управление ассортиментом

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Обзор

Dynamics 365 Commerce предоставляет *ассортименты*, которые позволяют управлять доступность продукта в разных каналах. Ассортименты определяют, какие продукты доступны в конкретных магазинах и в течение определенного периода.

В Commerce ассортимент является сопоставлением одного или нескольких каналов (или групп каналов, когда используются иерархии организаций) с одним или несколькими продуктами (или группами продуктов, когда используются иерархии категорий).

Общая номенклатура продуктов канала определяется опубликованными ассортиментами, назначенными для канала. Таким образом можно настроить несколько активных ассортиментов в каждом канале.

### <a name="basic-assortment-setup"></a>Базовая настройка ассортимента

В следующем примере уникальный ассортимент настраивается для каждого магазина. В этом случае только продукт 1 доступен в магазине 1, и только продукт 2 доступен в магазине 2.

![Каждый продукт доступен в одном магазине.](./media/Managing-assortments-figure1.png)

Чтобы сделать продукт 2 доступным в магазине 1, можно добавить продукт в ассортимент 1.

![Продукт 2 добавлен в ассортимент 1.](./media/Managing-assortments-figure2.png)

Можно также добавить магазин 1 в ассортимент 2.

![Магазин 1 добавлен в ассортимент 2.](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a>Организационные иерархии

В ситуациях, когда несколько каналов используют одинаковые ассортименты продуктов, можно настраивать ассортименты с использованием организационной иерархии розничного ассортимента Commerce. При добавлении узлов из этой иерархии, будут включены все каналы в этом узле и его дочерних узлах.

![Организационная иерархия.](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a>Категории продуктов

Аналогично, со стороны продукта можно включить группы продуктов с помощью иерархий категорий продуктов. Можно настроить ассортименты, включая один или несколько узлов иерархии категорий. В этом случае ассортимент будет включать все продукты в этом узле категорий и его дочерних узлах.

![Категории продуктов.](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a>Исключенные продукты или категории

Помимо включения продуктов и категорий в ассортименты, можно использовать параметр "Исключить" для определения конкретных продуктов или категорий, которые должны быть исключены из ассортиментов. В следующем примере необходимо включить все продукты из конкретной категории, за исключением продукта 2. В этом случае не нужно определить ассортимент, перечисляя все продукты, или создавать дополнительные узлы категорий. Вместо этого можно просто включить категорию, но исключить продукт.

> [!NOTE]
> Если продукт является как включенным, так и исключенным в одном или нескольких ассортиментов по определению, продукт будет всегда считаться исключенным.

![Исключенный продукт.](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a>Глобальные и запущенные в производство продукты

Ассортименты определяются на глобальном уровне и могут содержать каналы от нескольких юридических лиц. Продукты и категории, которые включены в ассортименты, также являются общими для юридических лиц. Однако продукт должно быть выпущен, прежде чем его можно будет продавать, заказывать, инвентаризировать или получать в канале (например, в POS-терминале \[POS\]). Таким образом, хотя два магазина в различных юридических лицах могут совместно использовать ассортимент, который содержит одинаковые продукты, продукты доступны только в том случае, если они были выпущены для этих юридических лиц.

### <a name="dynamic-and-static-assortments"></a>Динамические и статические ассортименты

Ассортименты можно определять с конкретными каналами и продуктами или путем включения организационных подразделений и категорий. Ассортименты, включающие ссылки на эти группы, рассматриваются как динамические ассортименты. Если определение или содержимое этих групп изменяется, когда ассортимент является активным, определение ассортимента также изменяется.

Например, ассортимент изначально определен и опубликован таким образом, что он ссылается на категорию продуктов. Если позднее дополнительные продукты добавляются в эту категорию, эти продукты автоматически включаются в определение существующего ассортимента. Не требуется вручную добавлять новые продукты в ассортимент. Аналогичным образом, если организационное подразделение добавлено в другой узел, ассортимент этого организационного подразделения автоматически корректируется на основе этого определения.

### <a name="stopped-products"></a>Остановленные продукты

Можно "остановить" выпущенные продукты для процесса продаж, включив параметр в настройках **Заказ по умолчанию**. Этот параметр чаще всего используется, когда продукт находится в конце его жизненного цикла и не должен продаваться ни в одном из каналов. Ассортименты учитывают этот параметр, и остановленные продукты не будут включаться в ассортимент, вне зависимости от конфигурации ассортимента.

### <a name="blocked-products"></a>Заблокированные продукты

Помимо остановки продаж продукта, можно временно заблокировать продажи продукта. Этот параметр можно настроить на вкладке **Commerce** выпущенного продукта. Заблокированные продукты по-прежнему включаются в ассортимент, но вы получите сообщение в POS-терминале о том, что продукт не может быть продан.

### <a name="date-effectivity"></a>Даты вступления в силу

Ассортименты имеют дату вступления в силу. Поэтому предприятия розничной торговли могут настроить, когда продукты должны или не должны быть доступны в канале. Можно определить и опубликовать ассортименты заранее и указать даты начала и окончания срока действия. Продукты автоматически станут доступны или недоступны в указанные даты.

### <a name="process-assortments-batch-job"></a>Обработка пакетного задания ассортиментов

Ассортименты, которые определены в Commerce, должны быть обработаны, прежде чем они вступят в силу. Эта обработка выполняется по следующим причинам:

- Необходимо удалить нормализацию определений ассортимента, чтобы каналам было легче их использовать. Номенклатура продуктов для канала может быть определена через несколько ассортиментов, которые охватывают различные диапазоны дат. Когда часть этой информации рассчитывается заранее на сервере, повышается производительность в канале.
- Продукты и каналы в ассортименте могут изменяться за пределами самого ассортимента. Динамические ассортименты, которые содержат ссылки на категории или подразделения, должны периодически обрабатываться для включения или исключения записей на основе их текущего назначения.

## <a name="implementation-considerations"></a>Вопросы реализации

Учитывайте следующие требования к реализации при планировании ассортиментов и управлении ими для вашей реализации Commerce:

- **Репликация данных и размер базы данных** — хотя ассортименты помогают удовлетворять потребности бизнеса для управления доступностью продуктов, они также являются важным средством для управления размером канала и автономных баз данных. Хорошо управляемые ассортименты помогают снизить объем данных, которые должны обрабатываться и реплицироваться в канал и автономные базы данных. Они также помогают уменьшить количество записей, которые должны постоянно храниться. Меньше количество записей в этих базах данных увеличит производительность при добавлении номенклатур в проводку, поиске и обзоре продуктов.
- **Ассортименты с датами начала и окончания срока действия** — одно из наиболее эффективных средств для управления количеством продуктов в канале и автономных базах данных — это даты срока действия ассортиментов. Если оставить ассортименты с открытой датой завершения (без ограничения срока действия) на сезонные продукты или продукты, срок жизни которых заканчивается, эти базы данных будет неограниченно увеличиваться. Для управления этой ситуацией можно использовать различные подходы. Например, можно поддерживать отдельные ассортименты для сезонных продуктов и продуктов, которые должны быть всегда доступны.
- **Продажи и возвраты вне ассортиментов** — эта возможность помогает предприятиям розничной торговли эффективно управлять своим ассортиментом, позволяя ограничивать число доступных продуктов теми продуктами, которые входят в базовую номенклатуру продуктов для магазина. Эта возможность позволяет также предприятиям розничной торговли обрабатывать ситуации, когда продукт по ошибке не был включен в ассортимент, или при возврате продукта за пределами сроков действия ассортимента.

Если данные о продукте отсутствуют в базе данных канала, POS-терминал вызывает в режиме реального времени центральный офис для получения требуемых сведений, чтобы продукт можно было продать, вернуть или включить в заказ клиента. Сведения о продукте, полученные таким образом, доступны только в рамках этой транзакции. Продукт не добавляется в определение ассортимента. Таким образом, последующие вызовы в режиме реального времени будут выполняться по мере необходимости.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
