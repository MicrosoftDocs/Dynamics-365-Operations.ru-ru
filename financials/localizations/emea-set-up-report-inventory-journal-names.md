---
title: "Отчеты журнала запасов"
description: "При использовании настраиваемых складских отчетов, основанных на электронной отчетности, необходимо установить связь между конкретного отчета и типа журнала."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalName
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265144
ms.assetid: 0f07f62f-1053-46e9-b235-a7b38cbda409
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: eed3398651612743958722814ec5594ec34e4e5e
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-journal-reports"></a>Отчеты журнала запасов

При использовании настраиваемых складских отчетов, основанных на электронной отчетности, необходимо установить связь между конкретного отчета и типа журнала.

Чтобы настроить связь между конкретного отчета и тип журнала на **имена журналов запасов** страница (**Управление запасами**&gt;**установки**&gt;**имена журналов**&gt;**складских**), введите имя для отчета. **Примечание:** для настройки конфигурации, загрузите необходимые настройки электронной отчетности. Дополнительные сведения см. в разделе [загрузить электронной отчетности конфигурации из Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). В следующей таблице перечислены примеры отчетов запасов с поддерживаемые конфигурации в Европе.
|                    |                                     |                  |                                         |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| **Country**        | **Описание отчета**              | **Journal type** | **Имя формата сопоставления**                 |
| Литве, Венгрии | Отчет запасов          | Инвентаризация         | Выписка по номенклатуре (Венгрия, LT)            |
| Латвия в Польше     | Документ реклассификации запасов | Перевод         | InventoryReclassificationDocument\_PLLV |
| Эстония            | Документ реклассификации запасов | Перевод         | InventoryReclassificationDocument\_(ЭТ)   |
| Польша             | Внутренние пароль/RW                      | Проводка         | InventJournalLinesDocPL                 |
| Латвия             |  Документ Движения запасов         | Проводка         | Перемещение\_LV                            |
| Латвия             | Документ понижения стоимости запасов       | Корректировка       | InventJournalLines\_LV                  |
| Латвия             | Перенос транспортной накладной              | Перевод         | InternalTransferDeliveryNote\_LV        |
| Латвия             | Отчет по документу инвентаризации            | Инвентаризация         | CountedDocument\_LV                     |
| Латвия             | Отчет по списку инвентаризации                | Инвентаризация         | Инвентаризационная опись                            |




