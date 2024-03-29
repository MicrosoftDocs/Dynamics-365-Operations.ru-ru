---
title: Методы расчета налога в поле "Основание"
description: В этой статье описываются параметры в поле "Источник" на странице налоговых кодов, а также порядок расчета налога на основе выбранного параметра для налогового кода.
author: kailiang
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4442f47029e2bd579b4d8fe59f380e4fad094b9f
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715560"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>Методы расчета налога в поле "Основание"

[!include [banner](../includes/banner.md)]

В этой статье описываются параметры в поле "Источник" на странице налоговых кодов, а также порядок расчета налога на основе выбранного параметра для налогового кода.

Для каждого из налоговых кодов, создаваемых на странице "Налоговые коды", необходимо указать метод расчета для базовой суммы налога в поле "Основание".

## <a name="percentage-of-net-amount"></a>Процент от чистой суммы
Метод расчета процента от чистой суммы — это значение по умолчанию в поле "Основание". Этот налог рассчитывается как процент от суммы покупки или суммы продаж за вычетом всех остальных налогов.
### <a name="example"></a>Пример

Ставка налога = 25%. В строке накладной количество равно 10 шт. по 1,00 каждая, и клиенту положена скидка 10%. Чистая сумма: (10 x 1,00) -10% = 9,00 Налог: 9,00 x 25% = 2,25 Общая сумма: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a>Процент от валовой суммы
Если вы выбираете метод "Процент от валовой суммы", то налог рассчитывается как процент от валовой суммы продаж. Валовая суммы равна чистой сумме строки плюс все налоги и сборы для строки за исключением одного налога с "Основание" = "Процент от валовой суммы".
### <a name="example"></a>Пример

Налоговым органом введены особые пошлины по данной номенклатуре. Суммы пошлины добавляются к чистой сумме до расчета налога. Если имеются следующие налоговые коды:
-   ПОШЛИНА 1 = 10% с использованием метода расчета процента от чистой суммы
-   ПОШЛИНА 2 = 20% с использованием метода расчета процента от чистой суммы
-   НАЛОГ С ПРОДАЖ = 25% с использованием метода расчета "Процент от валовой суммы"

Если чистая сумма составляет 10,00, то ПОШЛИНА 1 составляет 1,00 (10,00 x 10%), а ПОШЛИНА 2 составляет 2,00 (10,00 х 20%). Суммы будут следующие: Валовая сумма: Чистая сумма + сумма ПОШЛИНА 1 + сумма ПОШЛИНА 2 (10,00 + 1,00 + 2,00) = 13,00 НАЛОГ С ПРОДАЖ = 13,00 x 25% = 3,25 Итого ПОШЛИНЫ и НАЛОГ С ПРОДАЖ: 1,00 + 2,00 + 3,25 = 6,25 Общая сумма: 10,00 + 6,25 = 16,25

| **Примечание**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Только один код налога с "Основание" = "Процент от валовой суммы" может использоваться для проводки. Если для проводки определено более одного такого кода налога, отображается ошибка с предупреждением о невозможности расчета налога. |


## <a name="percentage-of-sales-tax"></a>Процент от другого налога

При выборе в поле "Основание" значения "Процент от другого налога" налог рассчитывается как процент налога, выбранного в поле "Налог на налог". Расчет налога, выбранного в поле "Налог на налог", выполняется в первую очередь. Затем на основании суммы первого налога рассчитывается второй налог.
### <a name="example"></a>Пример

Если имеются следующие налоговые коды:
-   ПОШЛИНА 1 = 10% с использованием метода расчета процента от чистой суммы
-   ПОШЛИНА 2 = 20% с использованием метода "Процент от другого налога", когда в поле "Налог на налог" указано значение Пошлина 1
-   НАЛОГ С ПРОДАЖ = 25% с использованием метода "Процент от валовой суммы"

Чистая сумма: 10,00 ПОШЛИНА 1: 10,00 x 10% = 1,00 ПОШЛИНА 2: 1,00 x 20% = 0,20 Валовая сумма: 10,00 + 1,00 + 0,20 = 11,20 НАЛОГ С ПРОДАЖ: 11,20 x 25% = 2,80 Итого ПОШЛИНЫ и НАЛОГ С ПРОДАЖ: 1,00 + 0,20 + 2,80 = 4,00 Общая сумма: 10,00 + 4,00 = 14,00

| **Примечание**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Расчеты многоуровневых налогов на налоги невозможны. Налог нельзя рассчитать на основе налога, который уже рассчитан на основе другого налога. Несколько одноуровневых кодов налогов на налоги можно рассчитать в одной проводке. |

## <a name="amount-per-unit"></a>Сумма на единицу
Когда вы выбираете метод "Сумма на единицу" в поле "Основание", налог рассчитывается как фиксированная сумма на единицу умноженная на количество, введенное в строку документа. Единица измерения выбирается в поле "Единица измерения". Сумма на единицу указывается на странице "Значения налогового кода".
### <a name="example"></a>Пример

Код налога настраивается следующим образом: USD 1,20 на единицу = коробка. В строке накладной заказа на продажу продано 25 коробок номенклатуры. Налог рассчитывается как 25 x 1,20 = 30,00

| **Примечание**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Если проводка введена в других единицах, чем единицы, определенные в коде налога на продажу, то они автоматически преобразуются на основе преобразований единиц измерения, настроенных на странице "Пересчеты единиц измерения". |

###  <a name="amount-per-unit-additional-option"></a>Метод "Сумма на единицу": дополнительные возможности

На вкладке "Расчет" вы можете выбрать, будет ли налог с расчетом на единицу рассчитываться до других налоговых кодов и добавляться к чистой сумме до расчета других налоговых кодов с "Основание" = "Процент от чистой суммы".

### <a name="examples"></a>Примеры

Предположим, что для проводки рассчитываются 2 налоговых кода:

-   ПОШЛИНА: "Основание" = "Сумма на единицу" и налог, значение установлено 5,00 на единицу = шт.
-   НАЛОГ С ПРОДАЖ: "Основание" = как показано в примерах ниже, значение установлено равным 25%

Мы продаем 1 единицу номенклатуры в ценой единицы 10,00
#### <a name="example-1"></a>Пример 1

НАЛОГ С ПРОДАЖ: "Основание" = метод "Процент от валовой суммы". Параметр "Расчет сборов до расчета налогов" не действует, так как НАЛОГ С ПРОДАЖ рассчитывается как процент от валовой суммы. ПОШЛИНА: 1 x 5,00 = 5,00 Валовая сумма: 10,00 + 5,00 = 15,00 НАЛОГ С ПРОДАЖ: 15,00 x 25% = 3,75 Всего налог: 5,00 + 3,75 = 8,75 Общая сумма: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>Пример 2

НАЛОГ С ПРОДАЖ: "Основание" = "Процент от чистой суммы" Параметр "Расчет сборов до расчета налогов" не выбран для расчета ПОШЛИНЫ. Чистая сумма: 10,00 ПОШЛИНА: 1 x 5,00 = 5,00 НАЛОГ С ПРОДАЖ: 10,00 x 25% = 2,50 Всего налог: 5,00 + 2,50 = 7,50 Общая сумма: 10,00 + 7,50 = 17,50

#### <a name="example-3"></a>Пример 3

НАЛОГ С ПРОДАЖ: "Основание" = "Процент от чистой суммы" Параметр "Расчет сборов до расчета налогов" выбран для расчета ПОШЛИНЫ. Чистая сумма: 10,00 ПОШЛИНА: 1 x 5,00 = 5,00 НАЛОГ С ПРОДАЖ: (10,00 + 5,00) x 25% = 3,75 Всего налог: 5,00 + 3,75 = 8,75 Общая сумма: 10,00 + 8,75 = 18,75

#### <a name="example-4"></a>Пример 4

Результаты Примеров 3 и 1 одинаковы, так как существует только одна пошлина. Предположим, что имеются две ПОШЛИНЫ, и только одна из них включена в чистую сумму для расчета налога: ПОШЛИНА 1: 5,00, с использованием метода "Сумма на единицу", и выбран параметр "Расчет сборов до расчета налогов" ПОШЛИНА 2: 2,50, с использованием метода "Сумма на единицу", и параметр "Расчет сборов до расчета налогов" не выбран Налог: 25%, с использованием метода "Процент от чистой суммы" Чистая сумма: 10,00 ПОШЛИНА 1: 1 x 5,00 = 5,00 ПОШЛИНА 2: 1 x 2,50 = 2,50 Чистая сумма для налога с продаж: 10,00 + 5,00 = 15,00 НАЛОГ С ПРОДАЖ: 15,00 x 25% = 3,75 Итого налоги с продаж, включая пошлины: 5,00 + 2,50 + 3,75 = 11,25 Общая сумма: 10,00 + 11,25 = 21,25 НАЛОГ С ПРОДАЖ 25% рассчитывается для суммы чистой суммы (10,00) + ПОШЛИНА 1 (5,00) = 15,00. ПОШЛИНА 2 будет добавлена к сумме налога после расчета налога с продаж.

## <a name="calculated-percentage-of-net-amount"></a>Рассчитанный процент чистой суммы
Расчет налога методом "Рассчитанный процент чистой суммы" производится по-разному в зависимости от настройки параметра "Суммы включают налог" для документа или журнала.
### <a name="example-1"></a>Пример 1

Для документа или журнала задано значение "Суммы включают налог" = "Да" Сумма в строке проводки: 10,00 Ставка налога: 25% Налог с продаж: Сумма в строке проводки x Ставка налога (10,00 x 25%) = 2,50 Сумма налоговой базы (сумма основания): Сумма в строке проводки - Налог с продаж (10,00 - 2,50) = 7,50

### <a name="example-2"></a>Пример 2

Для документа или журнала задано значение "Суммы включают налог" = "Нет" Сумма в строке проводки: 10,00 Ставка налога: 25% Налог с продаж: (Сумма в строке проводки x Ставка налога)/(100 - Ставка налога) (10,00 x 25%)/(100% - 25%) = 3,33 Сумма налоговой базы (сумма основания): Сумма в строке проводки = 10,00



## <a name="additional-resources"></a>Дополнительные ресурсы

[Ставки налога на основе базы маржинальной прибыли и методов расчета](marginal-base-field.md)

[Параметры расчета "Полная сумма" и "Интервал" для налоговых кодов](whole-amount-interval-options-sales-tax-codes.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
