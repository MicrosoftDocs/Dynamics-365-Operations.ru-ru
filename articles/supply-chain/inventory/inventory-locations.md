---
title: "Места хранения"
description: "Места хранения используются с базовым управлением складом (WMS I), чтобы определить, где хранятся номенклатуры и где комплектуются номенклатуры внутри склада WMS I."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 95d93c9d471cc86877f35340693c171958db71df
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---

# <a name="inventory-locations"></a>Места хранения

[!include[banner](../includes/banner.md)]


Места хранения используются с базовым управлением складом (WMS I), чтобы определить, где хранятся номенклатуры и где комплектуются номенклатуры внутри склада WMS I.

Этот раздел относится к функциям в модуле "Управление запасами". Он не применяется к функциям в модуле "Управление складом".

Термин местонахождение определяется как то место, в котором хранятся и откуда извлекаются номенклатуры.

Для каждой ячейки может быть также указано то место, куда помещается номенклатура. По умолчанию это одно и то же место. Номенклатуры обычно, но не всегда, вставляются и извлекаются с одной и той же стороны ячейки. Например, номенклатуры, хранящиеся на стеллажах склада текущего расхода, помещаются туда из одного прохода, а извлекаются из другого прохода. Основной вход задается именем ячейки, которое обычно определяется ее координатами: склад, проход, стеллаж, полка и позиция. Это наименование или код могут быть введены вручную или сформированы с использованием координат местоположения, например, 01-02-03-4 для прохода 1, стеллажа 2, полки 3, позиции 4 на странице "Места хранения".
Свойства местоположения

Для местоположения имеются следующие характеристики:
-   Размер (высота, ширина, глубина и, таким образом, объем)
-   Склад, проход, стеллаж, полка и ячейка
-   Тип местонахождения (буферная ячейка, ячейка комплектации, зона приемки, зона отгрузки, местонахождение поступлений на производство, местонахождение проверки или супермаркет канбана)

В интерактивной системе может использоваться проверочный текст, чтобы убедиться, что оператор выбрал правильную ячейку для определенной номенклатуры. Этот проверочный текст может быть создан вручную или по умолчанию.

## <a name="sort-codes"></a>Коды сортировки
Коды сортировки используются для оптимизации обработки строк комплектации, которые детализируют информацию, требуемую для комплектации номенклатур со склада, включая порядок комплектации. Коды сортировки могут быть определены проходом и другими координатами или назначаться ячейке вручную.

## <a name="blocked-locations"></a>Блокированные ячейки
Иногда может потребоваться указать, что местонахождение заблокировано на определенное время, например для проведения ремонта. Кроме того, может потребоваться указать блокировку только на вход или только на выход.

## <a name="tree-structure"></a>Структура в виде дерева

На странице "Места хранения" вы можете просмотреть план склада в древовидной структуре, основанной на координатах мест хранения в определенном формате отображения.

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>Поддержка мест хранения через форму склада

Можно копировать местонахождения из одного склада в другой и создавать местонахождения с помощью мастера. Перед запуском мастера вы должны убедиться, что вы определили имена местонахождения по умолчанию на странице "Склад".



<a name="see-also"></a>См. также
--------

[Создание нового макета склада (проводник по задаче)](/dynamics365/unified-operations/supply-chain/inventory/tasks/create-new-warehouse-layout)
