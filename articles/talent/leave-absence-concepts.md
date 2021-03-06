---
title: Концепции отпусков и отсутствия на работе
description: В этой теме описываются концепции отпусков и отсутствия на работе, а также способ определения сальдо отгулов.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 03e2557e29194f17a9a586470ced5b352408b07c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462380"
---
# <a name="leave-and-absence-concepts"></a>Концепции отпусков и отсутствия на работе

Понятия и термины, которые описаны в этом разделе, помогут определить, как сотрудникам начисляется время отгулов и как рассчитываются сальдо отгулов для сотрудников. Дополнительные сведения об управлении отпусками и отгулами см. в разделе [Управление отпусками и отгулами](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).

## <a name="leave-plan-details"></a>Сведения плана отпусков

### <a name="start-date"></a>Начальная дата

Дата начала — это дата начала обработки начисления. Начальная дата также служит датой юбилея, которая используется для расчета переносимых сумм.

## <a name="accruals"></a>Начисления

Начисления определяют, когда и как часто сотрудникам начисляется время отгулов. Политики относительно времени начисления и политики пропорций определяются в разделе **Начисления** при настройте плана отпусков и отгулов.

### <a name="accrual-frequency"></a>Частота начисления

Частота начисления определяет, как часто начисляется или предоставляется отпуск. Имеются следующие варианты:

- Ежедневно
- Еженедельно
- Один раз в две недели
- Два раза в месяц
- ежемесячно
- Ежеквартально
- Раз в полгода
- Ежегодно
- Не допускается

### <a name="accrual-period-basis"></a>Базис периода начисления

Базис периода начисления определяет дату, которая используется для расчета периодов начисления. Имеются следующие варианты:

- **Дата начала плана**
- **Дата конкретного сотрудника** — если этот параметр выбран, значение определяет источник значения начальной даты, используемый для расчета периодов начисления. Имеются следующие варианты:

    - Произвольная
    - Дата юбилея
    - Дата первоначального приема на работу
    - Дата начала стажа
    - Скорректированная дата приема работника на работу
    - Дата приема работника на работу

### <a name="accrual-award-date"></a>Дата вознаграждения начисления

Дата начисления определяет, когда сотруднику начисляется время отгулов. Имеются следующие варианты:

- **Дата окончания периода начисления** — сотруднику начисляется время отгула в последний день периода вознаграждения.

    Для начисления правильной суммы процесс начисления должен включать весь период. Например, период начисления с 1 января 2018 по 31 января 2018. В этом случае для включения января необходимо выполнить начисление для 1 февраля 2018.

- **Дата начала периода начисления** — сотруднику начисляется время отгула в первый день периода вознаграждения.

### <a name="accrual-policy-on-enrollment"></a>Политика начисления по заявке

Эта политика начисления по заявке определяет способ расчета начисления, когда сотрудник зарегистрирован в середине периода начисления. Имеются следующие варианты:

- **Пропорционально** — диапазон дат между датой регистрации и датой начала используется для определения разницы в днях. Эта разница учитывается при обработке начислений.
- **Полное начисления** — полное начисления суммы в зависимости от уровня производится во время обработки первого начисления.
- **Без начисления** — до следующего периода начисления никакие начисления не производятся.

### <a name="accrual-policy-on-unenrollment"></a>Политика начисления при отмене регистрации

Эта политика начисления по отмене регистрации определяет способ расчета начисления, когда регистрация сотрудника отменена в середине периода начисления. Имеются следующие варианты:

- **Пропорционально** — диапазон дат между датой регистрации и датой начала используется для определения разницы в днях. Эта разница учитывается при обработке начислений.
- **Полное начисления** — полное начисления суммы в зависимости от уровня производится во время обработки первого начисления.
- **Без начисления** — до следующего периода начисления никакие начисления не производятся.

## <a name="accrual-schedule"></a>График начисления

График начисления определяет способ начисления сотрудникам времени отгулов, а также какие суммы будут начислены сотруднику и перенесены на будущее. Уровни могут создаваться таким образом, чтобы отгулы начислялись на основе различных уровней.

### <a name="months-of-service"></a>Месяцы службы

Значение **Месяцы службы** определяет минимальное количество месяцев, которые сотрудники должны отработать для получения права на начисления. Если для сотрудников нет минимального срока, задайте значение **0**.

### <a name="hours-worked"></a>Отработанные часы

Значение **Отработанные часы** определяет минимальное количество часов, которые сотрудники должны отработать за период начисления для получения права на начисления. Если для сотрудников нет минимального срока, задайте значение **0**.

### <a name="accrual-amount"></a>Сумма начисления

Сумма начисления — это число часов или дней, которые будут начисляться сотрудникам за период. Период основан на частоте начисления.

### <a name="minimum-balance"></a>Минимальное сальдо

Отрицательное значение может использоваться для минимального сальдо, если сотрудники могут запрашивать больше отпуска, чем им доступно на данный момент.

### <a name="maximum-carry-forward"></a>Максимальный перенос

Процесс начисления настроит сальдо отпуска, которое превышающих максимальное сальдо переноса на день годовщины даты начала.

### <a name="grant-amount"></a>Предоставляемая сумма

Предоставляемая сумма — это начальное количество часов или дней, которое предоставляется сотрудникам при начальной регистрации в плане отпусков. Эта сумма не начисляется за каждый период начисления.

## <a name="enrollments-and-balances"></a>Регистрации и сальдо

### <a name="enrollment-date"></a>Дата регистрации

Дата регистрации определяет, когда сотрудник может начинать начисление времени отпуска. Например, если сотрудник зарегистрирован в плане отпуска 15 июня 2018, она не может начислять никакое время отпуска до 15 июня 2018.

### <a name="current-balance"></a>Текущее сальдо

Текущее сальдо — это количество, доступное для запросов отгулов. Эта сумма включает в себя начисления, одобренные запросы и корректировки до текущей даты.

### <a name="current-balance-examples"></a>Примеры текущего сальдо

#### <a name="annual-plan"></a>Годовой план

**Настройка плана**

| Дата начала плана | Дата регистрации | Частота начисления | Базис периода начисления | Дата вознаграждения начисления    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01.01.2018        | 01.01.2018        | Ежегодный            | Дата начала плана      | Конец периода начисления |

Начисления обрабатываются на 1 января 2019 (01.01.2019), чтобы весь период был добавлен.

**Результаты**

| Сумма начисления | Минимальное сальдо | Максимальный перенос | Сумма запроса | Текущее сальдо (на 01.01.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Текущее сальдо (160) = Сумма начислений (200) — Сумма запроса (40)

#### <a name="semimonthly-plan"></a>План два раза в месяц

**Настройка плана**

| Дата начала плана | Дата регистрации | Частота начисления | Базис периода начисления | Дата вознаграждения начисления    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01.01.2018        | 01.02.2018        | Два раза в месяц       | Дата начала плана      | Конец периода начисления |

Начисления обрабатываются на 1 мая 2018 (01.05.2018), чтобы весь период был добавлен.

**Результаты**

| Сумма начисления | Минимальное сальдо | Максимальный перенос | Сумма запроса | Текущее сальдо (на 01.01.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Текущее сальдо (22) = Сумма начислений (5 × 6) — Сумма запроса (8)

#### <a name="monthly-plan"></a>Месячный план

**Настройка плана**

| Дата начала плана | Дата регистрации | Частота начисления | Базис периода начисления | Дата вознаграждения начисления    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01.01.2018        | 01.02.2018        | Два раза в месяц       | Дата начала плана      | Конец периода начисления |

Начисления обрабатываются на 1 мая 2018 (01.05.2018), чтобы весь период был добавлен.

**Результаты**

| Сумма начисления | Минимальное сальдо | Максимальный перенос | Сумма запроса | Текущее сальдо (на 01.01.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Текущее сальдо (7) = Сумма начислений (5 × 3) — Сумма запроса (8)

### <a name="forecasted-balance"></a>Прогнозируемое сальдо

*Прогнозируемое сальдо* равно сумме отпуска, которая доступна на будущую дату. Начисления и корректировки переноса прогнозируются до этой даты.

Используется следующая формула:

Прогнозируемое сальдо на понедельник = Текущее сальдо — Запросы + Начисления — Корректировки переноса

### <a name="forecasted-balance-examples"></a>Примеры прогнозируемого сальдо

#### <a name="annual-plan"></a>Годовой план

**Настройка плана**

| Дата начала плана | Дата регистрации | Частота начисления | Базис периода начисления | Дата вознаграждения начисления    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01.01.2018        | 01.01.2018        | Ежегодный            | Дата начала плана      | Конец периода начисления |

Начисления обрабатываются на 15 февраля 2019 (15.02.2019), чтобы весь период был добавлен.

**Результаты**

| Сумма начисления | Минимальное сальдо | Максимальный перенос | Текущее сальдо | Прогнозируемое сальдо (на 15.02.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Прогнозируемое сальдо (40) = Сумма начислений (20) + Текущее сальдо (40) — Корректировка переноса (20)

#### <a name="semimonthly-plan"></a>План два раза в месяц

**Настройка плана**

| Дата начала плана | Дата регистрации | Частота начисления | Базис периода начисления | Дата вознаграждения начисления    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01.01.2018        | 01.02.2018        | Два раза в месяц       | Дата начала плана      | Конец периода начисления |

Начисления обрабатываются на 15 февраля 2019 (15.02.2019), чтобы весь период был добавлен.

**Результаты**

| Сумма начисления | Минимальное сальдо | Максимальный перенос | Текущее сальдо | Прогнозируемое сальдо (на 15.02.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Прогнозируемое сальдо (35) = Сумма начислений (5 × 3) + Текущее сальдо (40) — Корректировка переноса (20)

#### <a name="monthly-plan"></a>Месячный план

**Настройка плана**

| Дата начала плана | Дата регистрации | Частота начисления | Базис периода начисления | Дата вознаграждения начисления    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01.01.2018        | 01.02.2018        | Два раза в месяц       | Дата начала плана      | Конец периода начисления |

Начисления обрабатываются на 15 февраля 2019 (15.02.2019), чтобы весь период был добавлен.

**Результаты**

| Сумма начисления | Минимальное сальдо | Максимальный перенос | Текущее сальдо | Прогнозируемое сальдо (на 15.02.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Прогнозируемое сальдо (30) = Сумма начислений (10 × 1) + Текущее сальдо (40) — Корректировка переноса (20)

### <a name="proration-balance-examples"></a>Примеры пропорционального сальдо

#### <a name="prorated-monthly-plan"></a>Пропорциональный ежемесячный план

**Настройка плана**

| Дата начала плана | Частота начисления | Базис периода начисления |
|-----------------|-------------------|----------------------|
| 01.01.2018        | ежемесячно           | Дата начала плана      |

**Результаты**

| Код сотрудника            | Месяцы службы | Дата регистрации | Начальная дата | Сумма начисления | Обработка начисления | Баланс |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson (Джанет Никольсон) | 0,00              | 01.06.2018        | 01.06.2018   | 1.00           | 01.09.2018        | 3,00    |
| Jay Norman (Джей Норман)          | 0,00              | 15.06.2018       | 15.06.2018  | 1.00           | 01.09.2018        | 2.53    |

#### <a name="full-accrual-monthly-plan"></a>Ежемесячный план с полным начислением

**Настройка плана**

| Дата начала плана | Частота начисления | Базис периода начисления |
|-----------------|-------------------|----------------------|
| 01.01.2018        | ежемесячно           | Дата начала плана      |

**Результаты**

| Код сотрудника            | Месяцы службы | Дата регистрации | Начальная дата | Сумма начисления | Обработка начисления | Баланс |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson (Джанет Никольсон) | 0,00              | 01.06.2018        | 01.06.2018   | 1.00           | 01.09.2018        | 3,00    |
| Jay Norman (Джей Норман)          | 0,00              | 15.06.2018       | 15.06.2018  | 1.00           | 01.09.2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Ежемесячный план без начисления

**Настройка плана**

| Дата начала плана | Частота начисления | Базис периода начисления |
|-----------------|-------------------|----------------------|
| 01.01.2018        | ежемесячно           | Дата начала плана      |

**Результаты**

| Код сотрудника            | Месяцы службы | Дата регистрации | Начальная дата | Сумма начисления | Обработка начисления | Баланс |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson (Джанет Никольсон) | 0,00              | 01.06.2018        | 01.06.2018   | 1.00           | 01.09.2018        | 3,00    |
| Jay Norman (Джей Норман)          | 0,00              | 15.06.2018       | 15.06.2018  | 1.00           | 01.09.2018        | 2.00    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]