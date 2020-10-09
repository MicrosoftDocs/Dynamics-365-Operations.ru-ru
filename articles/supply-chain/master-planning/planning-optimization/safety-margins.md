---
title: Резервное время
description: В этом разделе описывается, как резервное время можно использовать с надстройкой оптимизации планирования для Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05ac817081689f27cdf55cb86a3235d7707a737b
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803429"
---
# <a name="safety-margins"></a>Резервное время

[!include [banner](../../includes/banner.md)]

В этом разделе описывается, как резервное время можно использовать с надстройкой оптимизации планирования для Microsoft Dynamics 365 Supply Chain Management.

## <a name="safety-margins-overview"></a>Общие сведения о резервном времени

Целью резервного времени является включение настройки, предоставляющей некоторое буферное время сверх обычного времени упреждения. Например, если материал должен быть распакован или проверен после того, как они поступают от поставщика, нельзя просто добавить дополнительное время к времени упреждения покупки, поскольку этот подход предоставит поставщику дополнительное буферное время. В этом примере резервное время для поступления можно использовать, чтобы гарантировать, что поставщик доставляет ранее. Такой подход обеспечивает буферное время для внутренней обработки товаров.

Есть три типа заказов резервного времени:

- **Резерв заказа** — буферное время для размещения заказа на поставку
- **Резервное время для поступления** — буферное время для обработки входящих поставок
- **Резервное время для отпуска** — буферное время буфера для обработки отгрузок

На следующем рисунке показано, как эти значения резервного времени применяются с течением времени.

![Резервное время](media/safety-margins-1.png)

Все резервное время определено в днях. Значение по умолчанию *0* (ноль) указывает, что резервное время не применяется. Если настроено несколько значений резервного времени, все они добавляются к общему времени с *даты заказа* поставки до *даты потребности* в спросе. Например, у настройки нет времени упреждения, и для всех трех типов резерва устанавливается один день. В этом случае будет три дня между датой заказа на поставку и датой потребности в спросе, так что если датой заказа является 1 июля, датой потребности будет 4 июля.

### <a name="receipt-margin"></a>Резервное время для поступления

Резервное время для поступления, вероятно, является наиболее часто используемым из трех значений резервного времени. Она применяется к *дате поставки* и отсчитывается назад от *даты потребности*. Другими словами, для получения продуктов необходимо получить указанное число дней резервного времени для поступления, прежде чем они потребуются.

На следующем рисунке выделено резервное время для поступления.

![Резервное время для поступления](media/safety-margins-2.png)

Резервное время для поступления обычно используется в качестве буфера для обеспечения времени для регистрации на складе или других занимающих много времени процессов, которые не регистрируются как часть общего времени упреждения в системе. Для покупок одним преимуществом является то, что *дата поставки* заказа на покупку перемещается вперед соответствующим образом. Если вы увеличиваете время упреждения вместо использования резервного времени, поставщика по-прежнему будут просить выполнить доставку в последнюю минуту.

Обратите внимание на то, что резервное время для поступления не изменяет *дату потребности* поставки. Таким образом, резервное время для поступления не отображается непосредственно при сравнении дат потребности для спроса и поставки (например, на странице **Чистые потребности**). Например, если граница приемки установлена на четыре дня, а строка заказа на покупку планируется для приемки на пятнадцатый день месяца, в сводном планировании рассчитывается откорректированная дата приемки как девятнадцатый день месяца.

Обратите внимание, что резервное время для поступления не применяется, когда в качестве поставки используется запас в наличии. Все запасы в наличии считаются доступными немедленно, независимо от фактического получения.

### <a name="reorder-margin"></a>Резервное время для повторного заказа

> [!NOTE]
> **Скоро появится:** эта функция еще не поддерживается для оптимизации планирования. До тех пор, пока она не будет поддерживаться, все значения, введенные в поле **Резервное время для повторного заказа, добавленное ко времени упреждения для номенклатуры**, будут рассматриваться как *0* (ноль).

На следующем рисунке выделено резервное время для повторного заказа.

![Резервное время для повторного заказа](media/safety-margins-3.png)

Резервное время для повторного заказа добавляется до времени упреждения номенклатуры по всем спланированным заказам при сводном планировании. Таким образом, обеспечивается дополнительное время для размещения заказа на поставку. Это резервное время обычно используется в качестве буфера для обеспечения времени для процессов утверждения или других внутренних процессов, которые требуются во время создания заказов на поставку. Резервное время для повторного заказа помещается между датой *заказа на поставку* и *начальной датой*.

### <a name="issue-margin"></a>Резервное время для отпуска

> [!NOTE]
> **Скоро появится:** эта функция еще не поддерживается для оптимизации планирования. До тех пор, пока она не будет поддерживаться, все значения, введенные в поле **Резервное время для расхода, вычтенное из даты потребности**, будут рассматриваться как *0* (ноль).

На следующем рисунке выделено резервное время для отпуска.

![Резервное время для отпуска](media/safety-margins-4.png)

Резервное время для отпуска вычитается из даты потребности спроса во время сводного планирования. Это помогает гарантировать, что у вас будет время для реакции входящие заказы на спрос и их отгрузки. Это резервное время обычно используется в качестве буфера для обеспечения времени для отгрузки и соответствующих исходящих складских процессов.

Обратите внимание, что при применении резервного времени для отпуска соответствующие даты потребности в поставках и по спросу не совпадают. Вместо этого они отличаются на резервное время для отпуска, потому что резервное время для отпуска добавляется между *датой потребности* в поставках и *датой потребности* для спроса.

## <a name="set-up-safety-margins"></a>Настройка значений резервного времени

### <a name="turn-on-safety-margins-in-feature-management"></a>Включение резервного времени в управлении функциями

Прежде чем использовать эту функцию с оптимизацией планирования, она должна быть включена в системе. Администраторы могут использовать рабочую область [Управление функциями](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) для проверки статуса функции и ее включения, если это требуется. В этом случае функция указана следующим образом:

- **Модуль:** _Сводное планирование_
- **Имя компонента:** _Резервное время для оптимизации планирования_

### <a name="define-safety-margins"></a>Определение значений резервного времени

Значения резервного времени обладают гибкой настройкой. Они могут быть установлены как для *группы покрытия*, так и для *сводного плана*. Важно понимать, что значения резервного времени добавляются поверх друг друга. Например, резервное время получения, равное двум дням в группе покрытия, и трем дням в сводном плане, будет создавать эффективное резервное время получения, равное пяти дням.

Возможность задать резервное время в сводном плане может быть полезной, если требуется имитировать более длительное время упреждения или неопределенность для конкретного плана, но не затрагивая ежедневного планирования.

#### <a name="coverage-group-safety-margins"></a>Значения резервного времени для группы покрытия

Чтобы применить резервное время к группе покрытия, выполните следующие действия.

1. Выберите **Сводное планирование \> Настройка \> Группы покрытия**.
1. В области списка выберите нужную группу покрытия.
1. На экспресс-вкладке **Прочие** в разделе **Резервное время в днях** используйте следующие поля, чтобы задать требуемые значения резервного времени (в днях):

    - Резервное время для поступления, добавленное к дате потребности
    - Резервное время для расхода, вычтенное из даты потребности
    - Резервное время для повторного заказа, добавленное ко времени упреждения для номенклатуры

#### <a name="master-plan-safety-margins"></a>Значения резервного времени в сводном плане

Чтобы применить резервное время к сводному плану, выполните следующие действия.

1. Выберите **Сводное планирование \> Настройка \> Планы \> Сводные планы**.
1. В области списка выберите нужный сводный план.
1. На экспресс-вкладке **Резервное время в днях** используйте следующие поля, чтобы задать требуемые значения резервного времени (в днях):

    - Резервное время для поступления, добавленное к дате потребности
    - Резервное время для расхода, вычтенное из даты потребности
    - Резервное время для повторного заказа, добавленное ко времени упреждения для номенклатуры

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>Определение того, основаны ли расчеты на календарных днях или рабочих днях

Можно настроить все резервные времена так, чтобы они рассчитывались на основе либо календарных дней, либо рабочих дней.

1. Перейдите в раздел **Сводное планирование \> Настройка \> Параметры сводного планирования**.
1. На вкладке **Общие** в разделе **Резервное время в днях** установите для параметра **Рабочие дни** значение *Да*, чтобы рассчитать резервное время на основе рабочих дней. Установите для параметра значение *Нет*, чтобы рассчитать значения резервного времени на основе календарных дней.

Например, календарь открывается с понедельника по пятницу и закрывается с субботы по воскресенье. Если имеется резервное время для поступления на один день, дата потребности в понедельник создает дату поставки на предыдущую пятницу, так как суббота и воскресенье не являются рабочими днями.

Календарь, используемый для определения рабочих дней, зависит от настройки и типа поставок. Управление может осуществляться с помощью календарей группы покрытия, склада и поставщика.

> [!NOTE]
> Если *склад* не является частью аналитики покрытия (иными словами, планирование основано только на *сайте*), календарь склада не используется.

Система может обработать настройку, для которой определен один или несколько календарей. В следующих подразделах описываются возможные комбинации, которые могут использоваться для управления результатом.

#### <a name="calendar-that-is-used-for-the-duration"></a>Календарь, используемый для длительности

Определенные календари управляют фактическим общим временем упреждения в календарных днях с даты заказа на поставку до даты потребности в спросе. Используется следующее определение приоритетов календарей:

- **Время упреждения для покупки** — учитывается только календарь группы покрытия.
- **Резервное время для поступления** — используется календарь группы покрытия, если он определен. В противном случае используется календарь склада.
- **Резервное время для отпуска** — используется календарь группы покрытия, если он определен. В противном случае используется календарь склада.
- **Резервное время для заказа** — учитывается только календарь группы покрытия.

#### <a name="calendar-that-is-used-for-the-final-date"></a>Календарь, используемый для конечной даты

Для определения того, может ли механизм планирования использовать данную дату для данного типа даты, применяются следующие правила:

- **Дата поступления покупки** — используется календарь поставщика, если он определен. В противном случае используется календарь группы покрытия, если он определен. Если не определен ни один из этих календарей, используется календарь склада.
- **Дата поступления перемещения** — используется календарь группы покрытия, если он определен. В противном случае используется календарь склада.
- **Дата поступления с производства** — используется календарь группы покрытия, если он определен. В противном случае используется календарь склада.
- **День открытия отпуска спроса** — используется календарь склада, если он определен. В противном случае используется календарь группы покрытия.
- **День открытия заказа** — используется комбинация (пересечение) календаря группы покрытия и календаря поставщика. Оба календаря должны быть открыты для использования даты. Если определен только один из этих календарей, этот календарь используйте один.

#### <a name="calendar-setup-overview-matrix"></a>Матрица обзора настройки календаря

На следующем рисунке представлена матрица, в которой приведены общие сведения о том, какие календари применяются при расчете значений резервного времени. Для указания места, где указывается каждый тип календаря, используются следующие аббревиатуры и цвета:

- **Группа покрытия (CG):** зеленый
- **Склад (WH):** желтый
- **Поставщик (V):** синий

![Матрица обзора настройки календаря](media/safety-margins-calendar-matrix.png)

## <a name="calculating-delays"></a>Расчет задержек

Все три типа резервного времени учитываются, когда система определяет, является ли заказ задержанным.

Например, номенклатура имеет время упреждения, равное одному дню, и резервное время для поступления составляет три дня. Заказ на продажу для этой номенклатуры устанавливается как требуемый сегодня. В этом случае задержка рассчитывается как *время упреждения* + *резервное время для поступления* = четыре дня. Таким образом, если сегодня 14 августа, то четыре дня задержки приводят к доставке на 18 августа. Следующая иллюстрация показывает этот пример.

![Пример расчета задержки](media/safety-margins-delays.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Начало работы с оптимизацией планирования](get-started.md)

[Анализ соответствия оптимизации планирования](planning-optimization-fit-analysis.md)