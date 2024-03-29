---
title: Управление обновлениями стандартных затрат
description: Управлять обновлениями данных по стандартным затратам можно, используя два разных подхода — подход на основе одной версии или подход на основе двух версий.
author: JennySong-SH
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a6d693b58e7fbbd8e082d68d124eae52fb840b02
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674543"
---
# <a name="manage-standard-cost-updates"></a>Управление обновлениями стандартных затрат

[!include [banner](../includes/banner.md)]

Управлять обновлениями данных по стандартным затратам можно, используя два разных подхода — подход на основе одной версии или подход на основе двух версий.

Подход на основе одной версии предполагает использование одной версии цены, которая содержит все записи затрат. Эти записи включают исходные затраты и все обновления затрат.

Подход на основе двух версий предполагает использование одной версии, содержащей записи исходных затрат, и второй версии, содержащей записи всех обновлений затрат. Основное преимущество подхода на основе двух версий состоит в четком разделении и отслеживании обновлений затрат в отдельной версии цены, без оказания влияния на исходную версию цены. Подход на основе двух версий может использоваться для определения нескольких инкрементных обновлений, когда каждое инкрементное обновление имеет отдельную версию цены, содержащую инкрементные записи затрат.

## <a name="example"></a>Пример

В следующем примере показано, как можно использовать подходы на основе одной и двух версий для обновления стандартных затрат в производственной среде. Например, это могут быть обновления которые отражают новые номенклатуры или исправления ошибок. Предположим, что единственная версия цены представляет стандартные затраты для текущего года. Идентификатор этой версии — 2020-STD. Версия 2020-STD содержит текущие активные затраты для всех номенклатур. Кроме того, она содержит все категории затрат, связанные с маршрутизацией, и формулы расчета производственных накладных расходов, которые были известны на начало 2020 года. 2020-STD — это исходная версия цены.

- **Подход к обновлениям данных затрат на основе одной версии** — при использовании подхода на основе одной версии исходная версия цены 2020-STD будет содержать все записи затрат. Обновления затрат записываются в 2020-STD и получают статус "Ожидание". Ожидаемые затраты могут быть введены вручную для новых приобретенных номенклатур или они могут быть рассчитаны для произведенной номенклатуры с целью отразить корректировки. При использовании подхода на основе одной версии для расчетов спецификаций не требуется источник данных для отката, поскольку все активные затраты содержатся в версии цены. После активации ожидаемых затрат исходная версия цены 2020-STD будет снова содержать все текущие активные затраты.
- **Подход к обновлениям данных затрат на основе одной версии** — при использовании подхода на основе двух версий необходима дополнительная версия цены, содержащая только обновления затрат. Идентификатор этой версии — 2020-STD-CHANGES. Обновления затрат записываются в 2020-STD-CHANGES и получают статус "Ожидание". При использовании подхода на основе двух версий для расчетов спецификаций ожидаемых затрат для производимых номенклатур требуется источника данных для отката. Это необходимо, поскольку дополнительная версия цены 2020-STD-CHANGES содержит только подмножество данных затрат. В качестве отката могут использоваться активные затраты или версия цены 2020-STD, поскольку оба варианта определяют источник данных по затратам в том случае, когда он не существует в версии цены 2020-STD-CHANGES. После активации ожидаемых затрат дополнительная версия цены 2020-STD-CHANGES будет содержать текущие активные затраты, отражающие обновления, в то время как исходная версия цены 2020-STD не затрагивается. При использовании подхода на основе двух версий должны быть настроены политики блокирования для исходной версии цены, чтобы предотвратить возможность обновлений. Идентичные политики блокирования должны быть настроены для дополнительной версии цены, за исключением указанной начальной даты и выборочного использования политик блокирования для разрешения обновлений. Указанная дата вступления в силу должна обновляться вместе с каждым пакетом обновлений, чтобы отражать запланированную дату активации.

В этом примере использовалась одна дополнительная версия цены для управления обновлениями в течение всего 2020 года. Можно использовать несколько дополнительных версий цены, например, отдельную версию для каждого пакета обновлений. При использовании более чем одной дополнительной версии цены в качестве отката должны использоваться активные затраты, поскольку они распространяются на несколько версий цены.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Финансовые аналитики для переоценки стандартной себестоимости

Активация новой стандартной цены обычно приводит к переоценке стоимости запасов в наличии через проводки переоценки стандартной себестоимости. Обычно финансовые аналитики номенклатуры затем разносятся по проводкам. Однако если требуется управлять тем, требуется ли разносить финансовые аналитики, и способом их разноски, используйте [управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), чтобы включить функцию с именем *Параметры задания значений по умолчанию для финансовых аналитик для переоценки стандартной себестоимости запасов*. После включения этой функции перейдите в раздел **Управление затратами > Настройка учетных политик запасов > Параметры** и задайте для нового раскрывающегося списка **Источник финансовых аналитик** одно из следующих значений:

- **Нет** — никакие финансовые аналитики не разносятся в проводках по переоценке. Если ваша структура счетов включает необходимую финансовую аналитику, то процесс переоценки все равно выполняется, но он будет создавать записи учета, не имеющие финансовых аналитик. В этом случае пользователи будут сначала получать предупреждающее сообщение, чтобы при необходимости можно было отменить переоценку.
- **Таблица** — финансовые аналитики номенклатуры разносятся по проводкам переоценки. Этот параметр используется по умолчанию и согласуется с исходным поведением системы без включения функции *Параметры задания значений по умолчанию для финансовых аналитик для переоценки стандартной себестоимости запасов*.
- **Разноска** — финансовые аналитики проводок, которые переоцениваются, разносятся в проводках по переоценке. По умолчанию финансовые аналитики из счета запасов исходной проводки будут использоваться как для счета запасов, так и для счета переоценки.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]