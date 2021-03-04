---
title: Создание аналитик и импорт элементов аналитик
description: Учет затрат — это независимый модуль, для работы которого требуются данные справочников из других модулей.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d61358be79adc943572bb4a5d624cb7c80b52e6e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447229"
---
# <a name="create-dimensions-and-import-dimension-members"></a>Создание аналитик и импорт элементов аналитик

[!include [banner](../includes/banner.md)]

Учет затрат — это независимый модуль, для работы которого требуются данные из других модулей. Эти данные подразделяется на следующие:

-  Элементы затрат
-  Объекты затрат
-  Статистические аналитики

**Элемент затрат** соответствует связанному с затратами элементу в плане счетов. **Объект затрат** соответствует любому типу финансовой аналитики, такому как продукты, центры затрат и проекты, которые вы хотите оценивать, затраты на которые вы хотите распределять или изменять непосредственно. **Статистическая аналитика** и ее элементы используются для регистрации немонетарных записей. Элементы статистической аналитики могут использоваться в качестве базы распределения в распределении затрат и распределении стоимости. 

На следующей схеме показаны аналитики, которые используются в модуле "Учет затрат".

[![Аналитики учета затрат](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

После импорта данных в модуль "Учет затрат" их можно использовать для построения различных перспектив, позволяющих руководителям на всех уровнях организации делать обоснованные выводы. В следующих темах содержатся сведения о создании аналитик и импорте элементов аналитик. 

-  [Аналитики элементов затрат](cost-elements.md)
-  [Создание элементов затрат](./tasks/create-cost-elements.md)
-  [Аналитики объектов затрат](cost-objects.md)
-  [Сопоставление элементов аналитик элементов затрат с общим набором элементов аналитик](map-cost-elements-dimension-members.md)
-  [Сопоставление аналитики элемента затрат](./tasks/map-cost-element-dimension.md)
-  [Элементы статистических аналитик и шаблоны поставщиков статистических мер](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]