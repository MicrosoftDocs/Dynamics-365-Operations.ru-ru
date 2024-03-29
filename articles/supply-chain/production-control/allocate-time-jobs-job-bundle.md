---
title: Распределение времени для заданий в наборе заданий
description: В модуле "Управление производством" можно объединять задания в наборы. Затем можно запустить одновременно несколько заданий на странице списка заданий.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0236f9f39afc67cb5c8cedecee5278a6555d03deefb859fc134a4a4160285b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766615"
---
# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Распределение времени для заданий в наборе заданий

[!include [banner](../includes/banner.md)]

В модуле "Управление производством" можно объединять задания в наборы. Затем можно запустить одновременно несколько заданий на странице списка заданий.

Если задания объединяются в набор, необходимо указать, каким образом следует распределять по заданиям общее регистрируемое время для всех заданий. Вы задаете способ распределения, выбрав один из перечисленных ниже вариантов в поле **Тип набора** на странице **Ключи распределения**.

-   **Оценка**. Время делится между всеми заданиями на основе времени, выделенного для заданий.
-   **Задания**. Время делится в соответствии с числом заданий в пакете и количеством времени, которое было потрачено на их выполнение.
-   **Чистое время**. Время делится поровну между всеми объединенными заданиями.
-   **Реальное время**. Выделяется фактическое время задания. Стоимость можно вычислить на основе фактических затрат по зарплате. **Примечание.** Ключ распределения **Реальное время** доступен только в том случае, если ваша компания использует функциональность зарплаты в модуле "Посещаемость и время присутствия".

Следующие примеры демонстрируют результаты использования различных ключей распределения.

## <a name="example-scenario"></a>Пример сценария
Необходимо выполнить три задания из вашей очереди заданий. Вы запускаете первое задание, и пока оно выполняется, вы запускаете второе и третье задания. Поэтому имеется набор из трех заданий. В следующей таблице представлено предполагаемое время производства для каждого задания.

| Задание   | Время производства |
|-------|-----------------|
| Задание 1 | 1 час          |
| Задание 2 | 3 часа         |
| Задание 3 | 4 часа         |
| Итого | 8 часов         |

В следующей таблице представлено фактическое рабочее время, затраченное на каждое из заданий.

| Задание    | Время начала | Время завершения | Итого |
|--------|------------|----------|-------------|
| Задание 1  | 09:00      | 11:00    | 2 часа     |
| Задание 2  | 10:00      | 13:00    | 3 часа     |
| Задание 3  | 10:00      | 15:00    | 5 часов     |
| Итого | 09:00      | 15:00    | 6 часов     |

В следующих разделах описаны результаты расчета времени для каждого из ключей распределения.

## <a name="estimation-allocation-key"></a>Оценка ключа распределения
Следующая таблица демонстрирует применение формулы для расчета выделяемого времени. Формула: Время на каждое задание = Общее время для набора × (Оценка времени на задание ÷ Общее оцененное время)

| Задание   | Формула           | Выделенное время |
|-------|-------------------|----------------|
| Задание 1 | 6 × (1 ÷ 8) ч | 0,75 часа      |
| Задание 2 | 6 × (3 ÷ 8) ч | 2,25 часа     |
| Задание 3 | 6 × (4 ÷ 8) ч | 3,00 часа     |

## <a name="jobs-allocation-key"></a>Ключ распределения заданий
Следующая таблица демонстрирует применение формулы для расчета выделяемого времени. Формула: Время на задание = Общее время на набор ÷ Количество заданий

| Задание   | Формула | Выделенное время |
|-------|---------|----------------|
| Задание 1 | 6 ÷ 3   | 2 часа        |
| Задание 2 | 6 ÷ 3   | 2 часа        |
| Задание 3 | 6 ÷ 3   | 2 часа        |

## <a name="net-time-allocation-key"></a>Ключ распределения остаточного времени
Следующая таблица демонстрирует применение формулы для расчета выделяемого времени. Формула: Расчетное время по отчету = Время на набор ÷ Количество заданий

| Пример                       | 09:00–10:00 (1 ч) | 10:00–11:00 (1 ч) | 11:00–13:00 (2 ч) | 13:00–15:00 (2 ч) | Выделенное время |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Число заданий в наборе | 1                    | 3                    | 2                     | 1                     | Неприменимо |
| Задание 1                        | 1 ÷ 1 = 1 ч       | 1 ÷ 3 = 0,33 ч    | Неприменимо        | Неприменимо        | 1,33 часа     |
| Задание 2                        | Неприменимо       | 1 ÷ 3 = 0,33 ч    | 2 ÷ 2 = 1 ч        | Неприменимо        | 1,33 часа     |
| Задание 3                        | Неприменимо       | 1 ÷ 3 = 0,33 ч    | 2 ÷ 2 = 1 ч        | 2 ÷ 1 = 2 ч       | 3,33 часа     |

## <a name="real-time-allocation-key"></a>Ключ распределения "Реальное время"
Если вы хотите, чтобы цены производства высчитывались на основе фактических затрат, необходимо снять флажок **Категория затрат** на странице **Значения по умолчанию для производственного заказа**. Следующая таблица демонстрирует применение формулы для расчета выделяемого времени. Формула: Фактическое время на задание = Фактическое время в наборе

| Задание   | Фактическое время |
|-------|-------------|
| Задание 1 | 2 часа     |
| Задание 2 | 3 часа     |
| Задание 3 | 5 часов     |

Рассмотрим три задания, которые выполнил работник с почасовой оплатой в 12,00 долларов США. Никаких премий за переработку или других вознаграждений за время, потраченное на выполнение заданий, получено не было. Работник в сумме потратил шесть часов на эти три объединенных в набор задания. Таким образом, затраты на зарплату составят 6 * 12,00 долларов США = 72,00 доллара США. При использовании распределения по реальному времени пересчет почасовых затрат выполняется с учетом коэффициента из формулы "Чистое время". Фактическое время, потраченное на каждое задание, потом переводится вместе с верной почасовой ставкой. В примере на выполнение задания было потрачено шесть часов, хотя выделено 10. Следующая таблица демонстрирует применение формулы для расчета стоимости. Формула: Стоимость часа = (Общее время в наборе на задание (чистое время) ÷ Фактическое время, затраченное на задание) × Стандартные почасовые затраты

| Задание   | Вычисление скорректированных почасовых затрат | Скорректированные почасовые затраты | Выделенное время | Общие затраты по заданию |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| Задание 1 | (1,33 ÷ 2) × 12,00 долларов США                 | 8,00 USD                | 2 часа        | 16,00 USD         |
| Задание 2 | (1,33 ÷ 3) × 12,00 долларов США                 | 5,33 USD                | 3 часа        | 16,00 USD         |
| Задание 3 | (3,33 ÷ 5) × 12,00 долларов США                 | 8,00 USD                | 5 часов        | 40,00 USD         |

Скорректированные почасовые затраты и время задания разносятся в производственном журнале. **Примечание.** Если вы выбираете вариант **Категория затрат** на вкладке **Общие** на странице **Значения по умолчанию для производственного заказа**, то фактическое время для каждого задания переносится в производственный журнал, где затраты применяются к категории затрат конкретного задания.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]