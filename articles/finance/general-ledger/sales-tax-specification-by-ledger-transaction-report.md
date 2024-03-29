---
title: Отчет с налоговой информацией по проводке ГК
description: В этой статье объясняется, как использовать отчет "Налоговая информация по проводке ГК" для просмотра и печати сведений о проводках ГК, для которых рассчитан налог.
author: EricWang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: c96f457a0ea24aef1769f370c3c0657ada31eebf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898101"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>Отчет с налоговой информацией по проводке ГК
[!include [banner](../includes/banner.md)]

В этой статье объясняется, как использовать отчет **Налоговая информация по проводке ГК** для просмотра и печати сведений о проводках ГК, для которых рассчитан налог.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Налоговые счета и счета, не являющиеся налоговыми

В отчете **Налоговая информация по проводке ГК** отображаются налоговые проводки для налоговых и не налоговых счетов. Эти счета классифицируются следующим образом:

- **Налоговый счет** — счет считается налоговым счетом при разноске налоговой проводки, а счет ГК в строке журнала **Налог** является налоговым счетом, таким как счет уплаты налога или счет получения налога.
- **Неналоговый счет** — счет считается неналоговым счетом при разноске налоговой проводки, а счет ГК в исходной проводе является неналоговым счетом, таким как счет выручки или расходный счет.

Для налоговых счетов в столбцах **Источник**, **Входящий налог** и **Исходящий налог** в отчете отображается **0** (ноль). Для неналоговых счетов в этих столбцах отображаются суммы.

## <a name="filtering-the-data-on-the-report"></a>Фильтрация данных в отчете

При создании этого отчета доступны следующие поля по умолчанию. Эти поля можно использовать для фильтрации данных, отображаемых в отчете.

| Поле                      | Описание |
|----------------------------|-------------|
| Дата                       | Используйте поля в разделах **От** и **До** для определения диапазона дат для налоговых проводок. |
| Счет ГК               | Используйте поля в разделах **От** и **До** для определения диапазона счетов главной книги. |
| Код налога             | Используйте поля в разделах **От** и **До** для определения диапазона кодов налога. |
| Группировка                   | Выберите, должен ли отчет быть сгруппирован по счету книги учета или по налоговому коду. |
| Промежуточный итог по налоговому коду | Установите для этого параметра значение **Да**, чтобы отображать промежуточные итоги по налоговому коду. |
| Только итоги                | Установите для этого параметра значение **Да**, чтобы отображались только итоги. |
| Только счета ГК         | Установите для этого параметра значение **Да**, чтобы включить в отчет только счета ГК. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Отображение в отчете только счетов, не являющихся налоговыми

Чтобы отобразить в отчете только неналоговые счета, настройте условия фильтрации, такие как звездочка (\*), как показано на следующем рисунке.

![Отчет, отображающий неналоговые счета.](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
