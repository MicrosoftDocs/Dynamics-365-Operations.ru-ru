---
title: Обзор конфигураций продуктов на основе аналитик
description: Конфигурация продукта на основе аналитик представляет простое решение для создания нескольких вариантов продукта из одного шаблона продукта и его спецификации.
author: t-benebo
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19821"
- intro-internal
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba11a561f320a7f4e787e4fe3f4e6f4fb88bbfb
ms.sourcegitcommit: ca73177dedf40df16860eaf88b1c701c61992028
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2022
ms.locfileid: "9754119"
---
# <a name="dimension-based-product-configuration-overview"></a>Обзор конфигураций продуктов на основе аналитик

[!include [banner](../includes/banner.md)]

Конфигурация продукта на основе аналитик представляет простое решение для создания нескольких вариантов продукта из одного шаблона продукта и его спецификации.

Конфигурация продукта на основе аналитик — это одна из трех встроенных технологий конфигурации продукта. Две другие технологии — это предопределенные варианты и конфигурация на основе ограничений. Все три технологии используют шаблон продукта как отправную точку и позволяют пользователю создавать множество вариантов продукта для одного шаблона продукта.

## <a name="key-concepts"></a>Ключевые понятия
Конфигурация продукта на основе аналитики основана на следующих ключевых понятиях:

-   Шаблоны продукта
-   Аналитика продукта конфигурации
-   Конфигурационные группы
-   Спецификация (BOM)
-   Конфигурационный маршрут
-   Правила конфигурации

### <a name="product-masters"></a>Шаблоны продукта

Шаблон продукта — это отправная точка для любого процесса конфигурации продукта. В случае конфигурации продукта на основе аналитики необходим шаблон продукта с этой определенной технологией конфигурации и группа аналитик продукта, которая включает аналитику продукта конфигурации.

### <a name="configuration-product-dimension"></a>Аналитика продукта конфигурации

Аналитика продукта конфигурации используется для определения вариантов продукта для шаблона продукта с технологией конфигурации на основе аналитик. Значение аналитики конфигурации вводится пользователем и должно помочь определить отдельные варианты продукта.

### <a name="configuration-groups"></a>Конфигурационные группы

Конфигурационные группы определяются в центральном репозитории и могут использоваться для всех моделей конфигурации продукта на основе аналитик. Конфигурационные группы связаны с отдельными строками спецификации и вместе составляют группу строк, которые являются взаимоисключающими. Это значит что только одну строку в группе можно выбрать для одного варианта продукта.

### <a name="bill-of-materials-bom"></a>Спецификация (BOM)

Спецификация представляет строительные блоки для конфигурации продукта на основе аналитики. Она должна включать все различные продукты, которые можно использовать в любом варианте продукта. Каждая строка в конфигурации может ссылаться на конфигурационную группу. Если строка не ссылается на конфигурационную группу, она будет включена во все варианты продукта.

### <a name="configuration-route"></a>Конфигурационный маршрут

Конфигурационный маршрут определяет последовательность конфигурационных групп по мере того, как они отображаются пользователю в процессе конфигурации продукта.

### <a name="configuration-rules"></a>Правила конфигурации

Правила конфигурации представляют механизм, гарантирующий, что продукт, включенный в одну конфигурационную группу в спецификации, приведет либо к включению, либо исключению продукта в другой конфигурационной группе в той же спецификации.

## <a name="product-modeling-process"></a>Процесс моделирования продукта
Естественная последовательность создания модели продукта для продукта на основе аналитики начинается с определения соответствующих конфигурационных групп. Важно гарантировать, что все продукты, которые будут использоваться в конфигурации, были выпущены в компании, для которой создается модель продукта. С помощью этих строительных блоков пользователь может создать спецификацию и назначить конфигурационные группы всем соответствующим строкам спецификации. По завершении спецификации можно определить конфигурационный маршрут для организации конфигурационных групп в правильной последовательности. [![Процесс моделирования продукции на основе аналитик.](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Если имеются определенные продукты из других конфигурационных групп, которые должны или не должны использоваться вместе, можно создать правила конфигурации, которые будут определять отношения этих продуктов. После привязки спецификации к шаблону продукта на основе аналитики с помощью версии спецификации, их утверждения и активации можно создать конфигурации продукта и ввести имя для каждой конфигурации. Конфигурации можно определить перед созданием проводок, или когда есть потребность в определенной конфигурации.

### <a name="suggested-use"></a>Предполагаемое использование

Технология конфигурация на основе аналитик рекомендуется использовать для продуктов с ограниченной изменчивостью, и когда сочетание стандартного размера, цвета, стиля и конфигурации аналитик продукта не подходит для определения конкретного варианта продукта. Примером может служить велосипед с высотой рамы, размером колес, типами тормозов и различными передачами.

### <a name="next-step"></a><a name="sequence"></a>Далее

Следующие восемь проводников по задачам указаны в том в порядке, в каком их следует выполнять. 

1.  [Создание шаблона продукта на основе аналитик](tasks/create-dimension-based-product-master.md)
2.  [Выпуск шаблона продукта на основе аналитик](tasks/release-dimension-based-product-master.md)
3.  [Завершение базовой настройки шаблона запущенных в производство продуктов](tasks/complete-basic-setup-released-product-master.md)
4.  [Определение конфигурационных групп](tasks/define-configuration-groups.md)
5.  [Создание спецификации для шаблона продукта на основе аналитик](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Определение конфигурационных маршрутов](tasks/define-configuration-route.md)
7.  [Создание правил конфигурации](tasks/create-configuration-rules.md)
8.  [Создание конфигураций на основе аналитик](tasks/create-dimension-based-configurations.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]