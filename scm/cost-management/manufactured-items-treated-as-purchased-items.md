---
title: "Настройка продуктов, которые можно произвести или приобрести"
description: "Продукты могут получаться из различных источников — их можно произвести (изготовить) или приобрести (купить). В этой статье описываются некоторые типичные моменты, которые следует учитывать при настройке продуктов для поддержки нескольких источника."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 5360c7b1475763b8e33205bff560393e9ee51882
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-products-that-can-be-produced-or-procured"></a>Настройка продуктов, которые можно произвести или приобрести

[!include[banner](../includes/banner.md)]


Продукты могут получаться из различных источников — их можно произвести (изготовить) или приобрести (купить). В этой статье описываются некоторые типичные моменты, которые следует учитывать при настройке продуктов для поддержки нескольких источника. 

Несколько источников обычно используется для покупной номенклатуры, которая иногда изготавливается, или когда номенклатура, которая раньше обычно изготавливалась, изменена таким образом, что теперь она в основном закупается. Сначала номенклатура указывается как произведенная номенклатура, чтобы можно было определить спецификацию и данные маршрута и обеспечить поддержку производственных заказов на номенклатуру. Для типа производства должно быть установлено значение **Спецификация** (или, для непрерывного производства, **Формула** или **Сопутствующий продукт**).

Когда вы используете стандартную себестоимость, запись стоимости номенклатуры может быть рассчитана для изготовленной номенклатуры. Однако запись стоимости номенклатуры может не соответствовать стандартной себестоимости, которая требуется для целей закупки. В таком случае стандартную себестоимость нужно ввести вручную и активировать для записи по себестоимости номенклатуры. Для вычисления стоимости рассмотрите использование специальной спецификации и маршрута, которые представляют смесь поставок продукта в течение финансового периода, чтобы уменьшить отклонения с течением времени. Кроме того, произведенную номенклатуру на одном сайте можно перенести на другой сайт. Поэтому стоимость номенклатуры необходимо вводить вручную и активировать для сайта, куда номенклатура перемещается. При использовании произведенной номенклатуры в качестве компонента продуктов более высокого уровня затраты на компонент должны рассматриваться как приобретенная номенклатура. Эта рекомендация действует независимо от того, рассчитывались ли затраты или вводились вручную. Другими словами, в расчете спецификации затраты на номенклатуру должны рассматриваться как приобретенный компонент вместо использования сведений о спецификации и маршруте для расчета затрат. Во избежание выполнения этого расчета, выберите флага **Остановка развертывания**, который внедрен в группу расчета спецификации, назначенную этой номенклатуре. Для предотвращения развертывания требований номенклатуры при подсчете сводного планирования, задайте границу развертывания, равную 0 (нулю) дней, в покрытии номенклатуры или в группе покрытия. Расчет свободного планирования будет затем рассматривать номенклатуру как купленную номенклатуру и не будет производить дальнейшие расчеты по данным спецификации и маршрута номенклатуры.





