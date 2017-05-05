---
title: "Моделирование цены"
description: "Эта статья представляет информацию о моделировании цены для предложений. Моделирование цены позволяет оценить последствия вычетов на будущую цену продажи в процессе предложения, до принятия определенной цены."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SalesQuotationPriceSimulation
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 286adc6e609cd0f98afd499d4ebf2ad75e00da30
ms.lasthandoff: 03/31/2017


---

# <a name="price-simulation"></a>Моделирование цены

[!include[banner](../includes/banner.md)]


Эта статья представляет информацию о моделировании цены для предложений. Моделирование цены позволяет оценить последствия вычетов на будущую цену продажи в процессе предложения, до принятия определенной цены.

Моделирование цены для предложения показывает новую общую сумму, основанную на предложенной новой цене. Моделирование цены может также показать новую сумму для конкретной строки, созданной в существующем предложении. Можно ввести моделирование цены и применить его позже. В качестве альтернативы можно использовать исходное предложение без моделирования цены и сделать дополнительные изменения с клиентом в процессе продажи.  

Моделирование цены не изменяет цену в предложении. Если моделирование цены применяется ко всему предложению, она указывается как специальная скидка в заголовке предложения. Если моделирование цены применяется к определенным номенклатурам, она указывается как специальная скидка в строках предложения. Цена продажи за единицу, указанная в созданной строке предложения, не меняется при применении моделирования цены. Вместо этого применяется процент скидки, соответствующий уменьшению цены в строке предложения. При применении моделирования цены цена продажи за единицу и процент скидки перемещаются в строку предложения или в заголовок предложения.  

**Примечание.** При моделировании цены используется только текущая валюта продаж. Однако при просмотре итоговых значений предложения отображается как валюта компании, так и валюта продаж.  

Добавление дополнительных номенклатур в строки предложения может привести к созданию скидок по строке и многострочных скидок. Оно также может активировать общие скидки, которые изменят маржинальную прибыль и процентную маржу строк предложения и всей скидки.  

Возможно также выполнение нескольких моделирований цены для отслеживания влияния корректировок цены на итоговые значения предложения. Выполнение такого моделирования позволяет корректировать общую цену предложения или цену по одной или нескольким конкретным строкам предложения, а затем применить моделирование цены, оптимальной для заключения сделки.  

Предусмотрена возможность настройки предупреждения при создании предложения. Вот некоторые примеры использования оповещений:

-   Они могут сообщать о статусе предложения в организации.
-   Они могут запускать проверку конкретного предложения или сообщать о превышении скидок.

## <a name="price-simulation-and-discounts"></a>Моделирование цены и скидки
Чтобы гарантировать правильность расчета скидок и цен, следует соблюдать осторожность при моделировании цены по предложениям со скидками. Поскольку все моделирования цены рассматриваются как особые скидки в активной строке предложения или во всем предложении, важно отслеживать различия в скидках.

### <a name="types-of-discounts-in-trade-agreements"></a>Типы скидок в торговых соглашениях

Торговые соглашения в Microsoft Dynamics 365 for Operations могут иметь четыре типа ценовых скидок. Эти скидки могут быть настроены для различных номенклатур, клиентов или ценовых групп и могут быть ограничены датой. Чтобы исключить неправильные расчеты, при моделировании цены следует учитывать торговые соглашения. Четыре типа скидок в торговых соглашениях:

-   **Цена продажи** — для номенклатур можно указать отдельные цены продажи. При создании строк предложения программа выполняет поиск правильной цены продажи для номенклатуры и переносит ее в строки предложения. Поэтому торговое соглашение с такой скидкой не влияет на моделирование цены. Цена продажи, которая используется в строке предложения, отражает торговое соглашение.
-   **Скидка по строке** — для номенклатур определены специальные скидки в зависимости от заказанного количества. Суммы по строкам обычно уменьшаются на значение скидки по строке перед выполнением моделирования. Поэтому торговое соглашение с такой скидкой влияет на моделирование цены.
-   **Многострочная скидка** — если количества в целом превышают установленный пользователем лимит, предварительно определенные комбинации заказанных номенклатур активируют скидку для всего заказа. Суммы по строкам обычно уменьшаются на значение скидки по строке перед выполнением моделирования. Поэтому торговое соглашение с такой скидкой влияет на моделирование цены.
-   **Общая скидка** — если суммы в целом превышают установленный пользователем лимит, предварительно определенные заказанные номенклатуры активируют скидку для всего заказа. Общая скидка создается строками предложения. Однако поскольку общая скидка применяется к итоговой сумме предложения как скидка, она уменьшает итоговую сумму предложения. Поэтому торговое соглашение с такой скидкой влияет на моделирование цены.

### <a name="quotation-lines-and-trade-agreements"></a>Строки предложения и коммерческие соглашения

При создании или корректировке строки предложения скидки по строке вычисляются автоматически. Соответствующая цена продажи находится для номенклатуры на основе торгового соглашения.

## <a name="price-simulation-examples"></a>Примеры моделирования цены
Ниже приведены примеры использования моделирования цены для заголовков и номенклатур отдельных строк предложения.

### <a name="price-simulation-for-quotation-headers"></a>Моделирование цены для заголовков предложения

Вы создаете предложение со следующими строками.

-   10 единиц номенклатуры BR-12 (себестоимость единицы 9,52 долларов США, цена продажи единицы 15,32 долларов США).
-   12 единиц номенклатуры BR-14 (себестоимость единицы 7,48 долларов США, цена продажи единицы 13,75 долларов США).

В следующей таблице показаны строки предложения.

|                            | Расчет                          | Результат   |
|----------------------------|--------------------------------------|----------|
| Продаваемое количество             | 10 единиц + 12 единиц                  | 22 единицы |
| Сумма реализации, USD         | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Себестоимость, USD          | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Маржинальная прибыль, USD | 318,20 – 184,96                      | 133,24   |
| Процентная маржа         | (\[318,20 – 184,96\] ÷ 318,20) × 100 | 41,87%   |

Выполняется моделирование цены и применяется общая скидка на 15 процентов для всего предложения или для заголовка предложения. В следующей таблице показаны новые общие суммы по предложению после моделирования цены.

|                                                      | Расчет                               | Результат   |
|------------------------------------------------------|-------------------------------------------|----------|
| Продаваемое количество                                       | 10 единиц + 12 единиц                       | 22 единицы |
| Старая сумма реализации, USD                               | (10 × 15,32) + (12 × 13,75)               | 318,20   |
| Старая себестоимость, USD                                | (10 × 9,52) + (12 × 7,48)                 | 184,96   |
| Старая маржинальная прибыль, USD                       | 318,20 – 184,96                           | 133,24   |
| Старая процентная маржа                               | (\[318,20 – (10 × 9,52)\] ÷ 318,20) × 100 | 41,87%   |
| Моделирование цены с общей скидкой 15% в долларах США | (15 × 318,2) ÷ 100                        | 47,73    |
| Новая сумма реализации, USD                               | 318,20 – 47,73                            | 270,47   |
| Новая маржинальная прибыль, USD                       | 270,47 – 184,96                           | 85,51    |
| Новая процентная маржа                               | \[(270,47 – 184,96) ÷ 270,47\] × 100      | 31,61%   |

### <a name="price-simulation-for-single-line-items"></a>Моделирование цены для номенклатур отдельной строки

Вы создаете предложение со следующими строками.

-   10 единиц номенклатуры BR-12 (себестоимость единицы 9,52 долларов США, цена продажи единицы 15,32 долларов США).
-   12 единиц номенклатуры BR-14 (себестоимость единицы 7,48 долларов США, цена продажи единицы 13,75 долларов США).

В следующей таблице показаны строки предложения.

|                                      | Расчет                          | Результат   |
|--------------------------------------|--------------------------------------|----------|
| Продаваемое количество                       | 10 единиц + 12 единиц                  | 22 единицы |
| Сумма реализации для BR-12, USD         | 10 × 15,32                           | 153,20   |
| Сумма реализации для BR-14, USD         | 12 × 13,75                           | 165,00   |
| Себестоимость для BR-12, USD          | 10 × 9,52                            | 95,20    |
| Себестоимость для BR-14, USD          | 12 × 7,48                            | 89,76    |
| Маржинальная прибыль для BR-12, USD | 153,20 – 95,20                       | 58,00    |
| Маржинальная прибыль для BR-14, USD | 165,00 – 89,76                       | 75,24    |
| Процентная маржа для BR-12, USD  | \[(153,20 – 95,20) ÷ 153,20\] × 100  | 37,86    |
| Процентная маржа для BR-14, USD  | \[(165,00 – 89,76) ÷ 165,00\] × 100  | 45,60    |
| Общая сумма реализации, USD             | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Общая себестоимость, USD              | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Общая маржинальная прибыль, USD     | 318,20 – 184,96                      | 133,24   |
| Общая процентная маржа             | \[(318,20 – 184,96) ÷ 318,20\] × 100 | 41,87%   |

Выполняется моделирование цены и применяется общая скидка 10% для номенклатуры BR-12. В следующей таблице показаны новые общие суммы по предложению после моделирования цены для номенклатуры отдельной строки.

|                                                   | Расчет                             | Результат   |
|---------------------------------------------------|-----------------------------------------|----------|
| Количество для продажи                                    | 10 единиц + 12 единиц                     | 22 единицы |
| Старая сумма реализации для BR-12, USD                  | 10 × 15,32                              | 153,20   |
| Моделирование цены, скидка 10% для BR-12 | (10 × 153,2) ÷ 100                      | 15,32    |
| Новая сумма реализации для BR-12, USD                  | (10 × 15,32) – 15,32                    | 137,88   |
| Сумма реализации для BR-14, USD                      | 12 × 13,75                              | 165,00   |
| Себестоимость для BR-12, USD                       | 10 × 9,52                               | 95,20    |
| Себестоимость для BR-14, USD                       | 12 × 7,48                               | 89,76    |
| Новая маржинальная прибыль для BR-12, USD          | 137,88 – 95,20                          | 42,68    |
| Маржинальная прибыль для BR-14, USD              | 165,00 – 89,76                          | 75,24    |
| Новая процентная маржа для BR-12, USD           | \[(137,88 – 95,20) ÷ 137,88\] × 100     | 30,95    |
| Процентная маржа для BR-14, USD               | \[(165,00 – 89,76) ÷ 165,00\] × 100     | 45,60    |
| Новая общая сумма реализации, USD                      | \[(10 × 15,32) – 15,32\] + (12 × 13,75) | 302,88   |
| Общая себестоимость, USD                           | (10 × 9,52) + (12 × 7,48)               | 184,96   |
| Новая общая маржинальная прибыль, USD              | 302,88 – 184,96                         | 117,92   |
| Новая общая процентная маржа                      | \[(302,88 – 184,96) ÷ 302,88\] × 100    | 38,93%   |

Моделирование цены влияет только на строку, к которой оно применяется, уменьшая общую сумму для этой строки.



