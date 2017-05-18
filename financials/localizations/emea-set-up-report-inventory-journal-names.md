---
title: "Отчеты по журналу запасов"
description: "При использовании настраиваемых складских отчетов, основанных на электронной отчетности, необходимо настроить связь между конкретным отчетом и типом журнала."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: eeee93f2a48205e1b567c3f4421febe0dab6843a
ms.contentlocale: ru-ru
ms.lasthandoff: 04/25/2017


---

# <a name="inventory-journal-reports"></a>Отчеты по журналу запасов

[!include[banner](../includes/banner.md)]


При использовании настраиваемых складских отчетов, основанных на электронной отчетности, необходимо настроить связь между конкретным отчетом и типом журнала.

Чтобы настроить связь между конкретным отчетом и типом журнала, на странице **Имена журналов запасов** (**Управление запасами** &gt; **Настройка** &gt; **Наименования журналов** &gt; **Запасы**) введите имя для отчета. **Примечание.** Для настройки поддерживаемых конфигураций загрузите необходимые конфигурации электронной отчетности. Дополнительные сведения см. в разделе [Загрузка конфигураций электронной отчетности из Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). В следующей таблице приведены примеры отчетов о запасах с поддерживаемыми конфигурациями в Европе.
|                    |                                     |                  |                                         |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| **Страна**        | **Описание отчета**              | **Тип журнала** | **Имя сопоставления формата**                 |
| Литва, Венгрия | Отчет о выписке по запасам          | Инвентаризация         | Выписка по запасам (HU, LT)            |
| Латвия, Польша     | Документ реклассификации запасов | Перевод         | InventoryReclassificationDocument\_PLLV |
| Эстония            | Документ реклассификации запасов | Перевод         | InventoryReclassificationDocument\_EE   |
| Польша             | Внутренние PW/RW                      | Проводка         | InventJournalLinesDocPL                 |
| Латвия             | Документ Движения запасов         | Проводка         | Движение\_LV                            |
| Латвия             | Документ об уценке запасов       | Корректировка       | InventJournalLines\_LV                  |
| Латвия             | Перенос транспортной накладной              | Перевод         | InternalTransferDeliveryNote\_LV        |
| Латвия             | Отчет "Документ инвентаризации"            | Инвентаризация         | CountedDocument\_LV                     |
| Латвия             | Отчет "Инвентаризационная опись"                | Инвентаризация         | Инвентаризационная опись                           |






