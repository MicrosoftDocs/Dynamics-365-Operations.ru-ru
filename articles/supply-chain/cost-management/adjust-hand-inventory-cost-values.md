---
title: Настройка себестоимости запасов в наличии
description: Вы можете использовать страницу "Коррекция запасов в наличии", чтобы настроить себестоимость количеств запасов в наличии после выполнения процесса закрытия запасов.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62122454b2fe0f6a9f04f073057156603e66bb22
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673308"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Настройка себестоимости запасов в наличии

[!include [banner](../includes/banner.md)]

Вы можете использовать страницу "Коррекция запасов в наличии", чтобы настроить себестоимость количеств запасов в наличии после выполнения процесса закрытия запасов.

Вы можете использовать страницу **Настройка себестоимости запасов в наличии**, чтобы настроить себестоимость количеств запасов в наличии после выполнения процесса закрытия запасов. **Примечание.** Чтобы открыть страницу **Коррекция запасов в наличии** на странице **Закрытие и коррекция** выберите запись завершенного процесса закрытия запасов и после этого щелкните **Корректировка** &gt; **В наличии**. **Пример.** В феврале имеются следующие проводки:

-   1-ое февраля: Финансовый приход запасов в количестве равном 2 при себестоимости USD 10,00
-   5-ое февраля: Финансовый приход запасов в количестве равном 1 при себестоимости USD 13,00
-   19-ое февраля: Финансовый расход запасов в количестве равном 1 при скользящей средней себестоимости USD 11,00

Для этой номенклатуры настроена складская модель ФИФО, а закрытие запасов выполнялось 28 февраля. Проводка по финансовому расходу в сумме USD 11,00 будет сопоставлена с финансовым приходом от 1 февраля, и будет выполнена коррекция на USD 1,00. Следующие приходы на склад будут содержать открытые складские количества:

-   1-ое февраля: Количество 1 шт. при затратах USD 10,00
-   5-ое февраля: Количество 1 шт. при затратах USD 13,00

Для определения стоимости этих двух элементов равной USD 15,00, используйте опцию коррекции запасов в наличии для изменения открытых количеств запасов в наличии по состоянию на последний период закрытия складов. **Примечание.** Датой разноски операции по коррекции запасов в наличии будет дата последнего закрытия складов. Эту дату нельзя изменять.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]