---
title: "Места хранения"
description: "Места хранения используются с базовым управлением складом (WMS I), чтобы определить, где хранятся номенклатуры и где комплектуются номенклатуры внутри склада WMS I."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: cdf9eaeba076576d4adaa5fb5e18cd5a3f1c7b2d
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-locations"></a>Места хранения

[!include[banner](../includes/banner.md)]


Места хранения используются с базовым управлением складом (WMS I), чтобы определить, где хранятся номенклатуры и где комплектуются номенклатуры внутри склада WMS I.

Этот раздел относится к функциям в модуле "Управление запасами". Он не применяется к функциям в модуле "Управление складом".

Термин местонахождение определяется как то место, в котором хранятся и откуда извлекаются номенклатуры.

Для каждой ячейки может быть также указано то место, куда помещается номенклатура. По умолчанию это одно и то же место. Номенклатуры обычно, но не всегда, вставляются и извлекаются с одной и той же стороны ячейки. Например, номенклатуры, хранящиеся на стеллажах склада текущего расхода, помещаются туда из одного прохода, а извлекаются из другого прохода. Основной вход задается именем ячейки, которое обычно определяется ее координатами: склад, проход, стеллаж, полка и позиция. Это наименование или код могут быть введены вручную или сформированы с использованием координат местоположения, например, 01-02-03-4 для прохода 1, стеллажа 2, полки 3, позиции 4 на странице "Места хранения".
Свойства местоположения
-------------------

Для местоположения имеются следующие характеристики:
-   Размер (высота, ширина, глубина и, таким образом, объем)
-   Склад, проход, стеллаж, полка и ячейка
-   Тип местонахождения (буферная ячейка, ячейка комплектации, зона приемки, зона отгрузки, местонахождение поступлений на производство, местонахождение проверки или супермаркет канбана)

В интерактивной системе может использоваться проверочный текст, чтобы убедиться, что оператор выбрал правильную ячейку для определенной номенклатуры. Этот проверочный текст может быть создан вручную или по умолчанию.

## <a name="sort-codes"></a>Коды сортировки
Коды сортировки используются для оптимизации обработки строк комплектации, которые детализируют информацию, требуемую для комплектации номенклатур со склада, включая порядок комплектации. Коды сортировки могут быть определены проходом и другими координатами или назначаться ячейке вручную.

## <a name="blocked-locations"></a>Блокированные ячейки
Иногда может потребоваться указать, что местонахождение заблокировано на определенное время, например для проведения ремонта. Кроме того, может потребоваться указать блокировку только на вход или только на выход.
Структура в виде дерева
--------------

На странице "Места хранения" вы можете просмотреть план склада в древовидной структуре, основанной на координатах мест хранения в определенном формате отображения.
Поддержка мест хранения через форму склада
---------------------------------------------------

Можно копировать местонахождения из одного склада в другой и создавать местонахождения с помощью мастера. Перед запуском мастера вы должны убедиться, что вы определили имена местонахождения по умолчанию на странице "Склад".



<a name="see-also"></a>См. также
--------

[Создание нового макета склада (руководство по задаче)](https://ax.help.dynamics.com/en/wiki/create-a-new-warehouse-layout/)



