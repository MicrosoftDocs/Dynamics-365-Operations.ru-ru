---
title: Интегрированная книга учета
description: В этой статье описывается интеграция данных книги учета между приложениями для управления финансами и операциями и другими приложениями Dynamics 365 с помощью Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e5598295a25e31b33cd8b4d7ce3250a982ab4e87
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112251"
---
# <a name="integrated-ledger"></a>Интегрированная книга учета

[!include [banner](../../includes/banner.md)]



В бизнес-приложении данные главной книги определяют основные настройки для ведения бизнеса компании. Например, данные ГК описывают финансовый год, который используется в компании, валюты, которые она использует, и счета, используемые в ней. В этой статье описывается интеграция этих основных финансовых данных.

## <a name="templates"></a>Шаблоны

Данные ГК включают коллекцию сопоставлений основных финансовых таблиц, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.

Приложения Finance and Operations | Приложения для взаимодействия с клиентами     | описание
---------------------------------|----------------------------------|------------
[Валютные курсы CDS](mapping-reference.md#123) | msdyn_currencyexchangerates |
[План счетов](mapping-reference.md#121) | msdyn_chartofaccountses |
[Валюты](mapping-reference.md#218) | transactioncurrencies |
[Пара валют валютного курса](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[Тип валютного курса](mapping-reference.md#129) | msdyn_exchangeratetypes |
[Формат финансовой аналитики](mapping-reference.md#130) | msdyn_financialdimensionformats |
[Финансовые аналитики](mapping-reference.md#128) | msdyn_dimensionattributes |
[Объект интеграции финансового календаря](mapping-reference.md#132) | msdyn_fiscalcalendars |
[Период финансового календаря](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[Объект интеграции года финансового календаря](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Ledger](mapping-reference.md#148) | msdyn_ledgers |
[Счет ГК](mapping-reference.md#152) | msdyn_mainaccounts |
[Категории счета ГК](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

