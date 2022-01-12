---
title: Настройка кодов налогов
description: В этой теме описывается, как настроить коды налогов в службе расчета налогов.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 8bdb194e7d8b704d1e58d3c25bf2e1f6bff1ba00
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883876"
---
# <a name="set-up-tax-codes"></a>Настройка кодов налогов

[!include [banner](../includes/banner.md)]

В этой теме описывается, как настроить коды налогов в службе расчета налогов. Он включает в себя настройку простого сценария, чтобы работал налоговый код, и сведения о некоторых расширенных функциях налогового кода для сложных сценариев.

> [!IMPORTANT]
> Настройка налоговых кодов в службе расчета налогов не зависит от юридического лица. Эту настройку можно выполнить в Regulatory Configuration Service (RCS) только один раз. Налоговые коды автоматически синхронизируются с Microsoft Dynamics 365 Finance при включении службы расчета налогов для выбранного юридического лица в Finance.

## <a name="simple-setup"></a>Простая настройка

Выполните следующие шаги, чтобы использовать налоговый код в простом сценарии, например в ситуации, когда имеется только одна налоговая ставка.

1. Выполните вход в [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Перейдите в раздел **Рабочие области** \> **Функции глобализации** \> **Расчет налога**.
3. Выберите функцию и версию, которые необходимо настроить, и выберите **Изменить**.
4. На вкладке **Общие** выберите **Версия конфигурации**.
5. На вкладке **Коды налога** выберите **Добавить** и введите налоговый код и описание.
6. Выберите **База для расчета**. База для расчета — это группа методов, которая определена в выбранной версии налоговой конфигурации. Для этого простого сценария выберите **По чистой сумме**.
7. Нажмите **Сохранить**. В зависимости от выбранной базы для расчета становятся доступны дополнительные поля.
8. На экспресс-вкладке **Ставки** выберите **Добавить**, чтобы добавить одну ставку налога для этого налогового кода.
9. Нажмите **Сохранить**.

## <a name="calculation-origin"></a>Основание расчета

База для расчета определяет способ расчета суммы налоговой базы и суммы налога. Она настраивается конфигурацией налога в рабочей области **Электронная отчетность**. В поле **База для расчета** доступны следующие значения:

- По чистой сумме
- По валовой сумме
- По количеству
- По марже
- Налог на налог

### <a name="by-net-amount"></a>По чистой сумме

Если в поле **База для расчета** выбрано значение **По чистой сумме**, сумма налога рассчитывается как процент от суммы покупки или продажи, исключая любые другие налоговые коды.

Например, налоговая ставка составляет 25 процентов, в строке накладной указано количество 10 штук по 1,00 каждая, и клиенту предоставляется 10-процентная скидка по строке. В этом случае суммы рассчитываются следующим способом:

- **Чистая сумма:** (10 × 1,00) – 10 процентов = 9,00 
- **Налог:** 9,00 × 25 процентов = 2,25 
- **Итоговая сумма накладной:** = 9,00 + 2,25 = 11,25

### <a name="by-gross-amount"></a>По валовой сумме

Если в поле **База для расчета** выбрано значение **По валовой сумме**, то сумма налога рассчитывается как процент от валовой суммы продаж. Валовая суммы равна чистой сумме строки плюс все налоги и сборы для строки за исключением одного налога, для которого в поле **База для расчета** задано значение **По валовой сумме**.

Например, налоговым органом введены особые пошлины по номенклатуре. Суммы пошлины добавляются к чистой сумме до расчета налога. Используются следующие налоговые коды:

- **Пошлина 1** — ставка составляет 10 процентов, и используется метод расчета **По чистой сумме**.
- **Пошлина 2** — ставка составляет 20 процентов, и используется метод расчета **По чистой сумме**.
- **Ставка налога** — ставка составляет 25 процентов, и используется метод расчета **По валовой сумме**.

Если чистая сумма равна 10,00, то сумма пошлины 1 равна 1,00 (10,00 × 10 процентов), а сумма пошлины 2 равна 2,00 (10,00 × 20 процентов). В этом случае суммы рассчитываются следующим способом: 

- **Валовая сумма:** чистая сумма + пошлина 1 + пошлина 2 = 10,00 + 1,00 + 2,00 = 13,00 
- **Сумма налога:** 13,00 × 25 процентов = 3,25 
- **Итого пошлины и налог:** 1,00 + 2,00 + 3,25 = 6,25 
- **Итоговая сумма накладной:** = 10,00 + 6,25 = 16,25

### <a name="by-quantity"></a>По количеству

Когда выбрано значение **По количеству** в поле **База для расчета**, сумма налога рассчитывается как фиксированная сумма на единицу умноженная на количество, введенное в строку документа. Сумма на единицу указана на экспресс-вкладке **Ставки**.

Например, налоговый код настраивается как 1,20 за единицу. В строке накладной заказа на продажу продаются 25 единиц номенклатуры. В этом случае сумма налога вычисляется как 25 × 1,20 = 30,00.

### <a name="by-margin"></a>По марже

Если в поле **База для расчета** выбрано значение **По марже**, то сумма налога рассчитывается как процент от маржи продажи. Маржа продажи — это сумма продажи минус сумма затрат. Этот метод расчета применяется только к проводкам по продажам.

Например, налоговая ставка составляет 25 процентов, в строке накладной указано количество 10 штук по 10,00 каждая, и затраты на каждую единицу равны 6. В этом случае суммы рассчитываются следующим способом:

- **Маржа продажи:** 10 × ( 10,00 – 6,00) = 40,00
- **Сумма налога:** 40,00 × 25 процентов = 10,00
- **Итоговая сумма накладной:** = 100,00 + 10,00 = 110,00

### <a name="tax-on-tax"></a>Налог на налог

Если выбрано значение **Налог на налог** в поле **База для расчета**, налог рассчитывается как процент от всех других налоговых сумм в той же строке документа.

Например, используются следующие налоговые коды:

- **Пошлина 1** — ставка составляет 10 процентов, и используется метод расчета **По чистой сумме**.
- **Пошлина 2** — ставка составляет 20 процентов, и используется метод расчета **По чистой сумме**.
- **Налог на пошлину** — ставка составляет 25 процентов, и используется метод расчета **Налог на налог**.

В этом случае суммы рассчитываются следующим способом:

- **Чистая сумма:** 10,00 
- **Пошлина 1:** 10,00 × 10 процентов = 1,00 
- **Пошлина 2:** 10,00 × 20 процентов = 2,00 
- **Налог на пошлину:** 3,00 × 25 процентов = 0,75
- **Итоговый налог:** 1,00 + 2,00 + 0,75 = 3,75 
- **Итоговая сумма накладной:** = 10,00 + 3,75 = 13,75

## <a name="advanced-functionality"></a>Расширенные функции

В этом разделе описываются расширенные возможности настройки налогового кода для сложных сценариев.

### <a name="tax-exemption"></a>Налоговое освобождение

Если для параметра **Не облагается** задано значение **Да** на экспресс-вкладке **Общие**, сумма налога всегда будет переопределена на 0 (ноль), независимо от фактической налоговой ставки.

Поле **Код освобождения** можно настроить для определения причины исключения. 

Можно включить подстановку основных данных для поля **Код освобождения**. Таким образом можно выбирать значения кода освобождения, определенные в Finance. Сведения о включении подстановки основных данных см. в разделе [Включение подстановки основных данных для конфигурации расчета налога](tax-service-set-up-environment-master-data-lookup.md).

Например, налоговая ставка составляет 25 процентов, а для параметра **Не облагается** задано значение **Да** для налогового кода. В строке накладной количество равно 10 шт. по 1,00 каждая, и клиенту положена скидка 10% по строке. В этом случае суммы рассчитываются следующим способом:

- **Чистая сумма:** (10 × 1,00) – 10 процентов = 9,00 
- **Налог:** 0,00 
- **Итоговая сумма накладной:** = 9,00 + 0,00 = 9,00

### <a name="use-tax"></a>Налог за пользование

Если для параметра **Налог на пользование** задано значение **Да** на экспресс-вкладке **Общие**, сумма налога будет разнесена на счет **Налог за пользование, подлежащий уплате**, а не на счет **Поставщик — сводка**.

Например, налоговая ставка составляет 25 процентов, а для параметра **Налог на пользование** задано значение **Да** для налогового кода. В строке накладной количество равно 10 шт. по 1,00 каждая, и клиенту положена скидка 10% по строке. В этом случае суммы рассчитываются следующим способом:

- **Чистая сумма:** (10 × 1,00) – 10 процентов = 9,00 
- **Налог на пользование:** 9,00 × 25 процентов = 2,25
- **Итоговая сумма накладной:** = 9,00 + 0,00 = 9,00

> [!IMPORTANT]
> Если для обоих параметров **Не облагается** и **Налог на пользование** заданы значения **Да** для налогового кода, код будет распознан как освобожденный от налога для проводок по продажам и как налог на пользование для проводок покупки.

### <a name="reverse-charges"></a>Возмещения

Если для параметра **НДС, удерживаемый с покупателя** выбрано значение **Да** на экспресс-вкладке **Общие**, налоговая ставка может быть сконфигурирована как отрицательная. Для сценария с возмещением расходов рекомендуется настроить два налоговых кода: один с положительной налоговой ставкой, а второй с отрицательной ставкой налога. Оба налоговых кода должны иметь одинаковое значение ставки, а параметр **НДС, удерживаемый с покупателя** должен иметь значение **Да** для налогового кода, который имеет отрицательную налоговую ставку. Дополнительные сведения о решении налога с покупателя в модуле Finance см. в разделе [Механизм возмещения расходов для схемы НДС/GST](emea-reverse-charge.md).

Например, два налоговых кода определяются в одной строке накладной. Одна налоговая ставка составляет 25 процентов. Другая налоговая ставка составляет -25 процентов, а для параметра **НДС, удерживаемый с покупателя** задано значение **Да** для второго налогового кода. В строке накладной указано количество 10 штук по 1,00 каждая. В этом случае суммы рассчитываются следующим способом:

- **Чистая сумма:** (10 × 1,00) = 10,00 
- **Код налога 1:** 10,00 × 25 процентов = 2,50
- **Код налога 2:** 10 × -25 процентов = -2,50
- **Итоговая сумма накладной:** 10,00 + 2,50 -2,50 = 10,00

### <a name="exclusion-from-base-amount-calculations"></a>Исключение из расчета базовой суммы

Если для параметра **Исключить из расчета базовой суммы** задано значение **Да** на экспресс-вкладке **Общие**, вычисленная сумма налога для налогового кода исключается из базовой суммы налога для расчетов другого налогового кода в сценарии с инклюзивной ценой.

Дополнительные сведения см. в разделе [Расчет налога в ценах, когда активировано включение налога в цену](global-exclude-from-tax-base-amount-calculation.md).

### <a name="rates"></a>Ставки

На экспресс-вкладке **Ставка** можно определить другие налоговые ставки для других диапазонов базовых сумм налога. Для расчета суммы налога служба расчета налога всегда использует ставку, соответствующую сумме базы налога.

Например, можно настроить ставки налога, как показано в следующей таблице.

| Минимальная сумма | Максимальная сумма | Ставка налога   |
| -------------- | -------------- | ---------- |
| 0              | 1000          | 10 процентов |
| 1000          | 5 000          | 15 процентов |
| 5 000          | 10 000         | 20 процентов |
| 10 000         | 0              | 30 процентов |

В этом случае сумма налога рассчитывается следующим способом:

- Если сумма базы налога равна 300,00, налоговая ставка составляет 10 процентов, а сумма налога составляет 300,00 × 10 процентов = 30,00.
- Если сумма базы налога равна 3 000,00, налоговая ставка составляет 15 процентов, а сумма налога составляет 3 000,00 × 15 процентов = 450,00.
- Если сумма базы налога равна 6 000,00, налоговая ставка составляет 20 процентов, а сумма налога составляет 6 000,00 × 20 процентов = 1 200,00.
- Если сумма базы налога равна 20 000,00, налоговая ставка составляет 30 процентов, а сумма налога составляет 20 000,00 × 30 процентов = 6 000,00.

> [!NOTE]
> Если сумма базы налога может совпадать как с максимальной суммой в одной строке, так и с минимальной суммой в другой строке, в базе будет использоваться ставка налога, соответствующая минимальной базовой сумме. Например, если сумма базы налога равна 1000,00, налоговая ставка составляет 15 процентов, а сумма налога составляет 1 000,00 × 15 процентов = 150,00.

### <a name="limits"></a>Лимиты

На экспресс-вкладке **Пределы** можно определить налоговые ограничения, чтобы переопределить рассчитанную сумму налога, если сумма налога попадает в диапазон минимального/максимального значений.

- Если рассчитанная сумма налога больше или равна максимальной сумме налога, настроенной на экспресс-вкладке **Пределы**, окончательная сумма налога равна максимальной сумме налога.
- Если рассчитанная сумма налога меньше минимальной суммы налогов, настроенной на экспресс-вкладке **Пределы**, окончательная сумма налога будет равна 0 (нулю).

Например, лимиты налога настраиваются следующим образом:

- **Минимальная сумма налога:** 100 
- **Максимальная сумма налога:** 1 000

Если рассчитанная сумма налога равна 2 000, итоговая сумма налога составляет 1 000.

Если рассчитанная сумма налога равна 500, итоговая сумма налога составляет 500.

Если рассчитанная сумма налога равна 80, итоговая сумма налога составляет 0 (ноль).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]