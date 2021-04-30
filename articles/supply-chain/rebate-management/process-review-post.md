---
title: Обработка, проверка и разноска ретробонусов
description: В этом разделе описывается, как обрабатывать операции управления ретробонусами, рассчитывать свои скидки, просматривать созданные проводки, разносить проводки и просматривать разноски.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 53a24866786f209a1d0f6932bb4f782bf936bd21
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819264"
---
# <a name="process-review-and-post-rebates"></a>Обработка, проверка и разноска ретробонусов

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

В этом разделе описывается, как обрабатывать операции управления ретробонусами, рассчитывать свои скидки, просматривать созданные проводки, разносить проводки и просматривать разноски.

## <a name="change-the-status-of-a-deal"></a>Изменение состояния сделки

Можно назначить статус каждой из сделок, чтобы помочь отслеживать ее. Этот статус предназначен только для информационных целей.

1. Выберите сделку (например, на [странице **Все сделки управления ретробонусами**](rebate-management-deals.md)).
1. В области действий на вкладке **Сделки управления ретробонусами** в группе **Ведение** выберите **Изменить статус**.
1. В диалоговом окне **Изменение статуса** введите в поле **Статус ретробонуса** новый статус.
1. Нажмите **ОК**.

## <a name="calculate-fifo-purchase-prices"></a>Расчет закупочных цен ФИФО

Периодическая задача **Рассчитать цену покупки ФИФО** должна запускаться для расчета ретробонусов для [сделок](rebate-management-deals.md), в которых для поля **Базис цены** установлено значение *ФИФО*. Система использует правило "первый пришел — первым ушел" (ФИФО) для расчета стоимости проданных запасов. Эта сумма затем будет использоваться для расчета ретробонусов поставщика.

Перейдите в раздел **Управление ретробонусами \> Периодические задачи \> Расчет стоимости покупки ФИФО**. В появившемся диалоговом окне выберите **ОК**, чтобы выполнить расчет.

## <a name="process-rebate-management-deals"></a>Обработка сделок управления ретробонусами

При обработке сделки система вычисляет все соответствующие ретробонусы и роялти, которые были настроены. Будут обработаны только выбранные сделки, для которых определены периоды расчета, готовые для расчета и имеющие статус *Активно*. После завершения обработки система создает набор проводок, которые можно просмотреть, а затем выполнить разноску.

> [!NOTE]
> Во всех случаях ретробонусы обрабатываются на уровне, который указан в параметра **Выверять по** каждой сделки (*Сделка* или *Строка*). Можно выполнить однострочный расчет только для сделок, в которых для поля **Выверять по** выбрано значение *Строка*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Обработка всех строк для одной или нескольких сделок

1. Откройте соответствующую [страницу со списком сделок с ретробонусами](rebate-management-deals.md) для типа сделки, с которой вы хотите работать.
1. Выберите строку для каждой сделки, которую необходимо обработать (или откройте сделку, которую необходимо обработать).
1. В области действий на вкладке **Сделки управления ретробонусами** в группе **Создать** выберите одну из следующих команд:

    - **Обработать \> Подготовить** – подготовка набора начислений для каждой соответствующей сделки по ретробонусам, но не их разноска.
    - **Обработать \> Управление ретробонусами** — обработка ряда проводок, которые обеспечивают стоимость ретробонуса для каждой сделки.
    - **Обработать \> Списать** — сторнировать ранее разнесенные проводки, чтобы списать их, чтобы можно было рассчитать новые проводки сделок по ретробонусам.

1. В появившемся диалоговом окне установите поля **Начальная дата** и **Конечная дата**, чтобы определить диапазон дат для расчета.
1. Выберите **ОК**, чтобы выполнить расчет.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Обработка одной или нескольких конкретных строк сделки для выбранной сделки

1. Откройте соответствующую [страницу со списком сделок с ретробонусами](rebate-management-deals.md) для типа сделки, с которой вы хотите работать.
1. Откройте сделку, из которой необходимо обработать строку.
1. В верхнем правом углу выберите вкладку **Строки**.
1. На экспресс-вкладке **Управление ретробонусами** выберите строку для каждой строки сделки, которую необходимо обработать.
1. На панели инструментов экспресс-вкладки **Управление ретробонусами** выберите одну из следующих команд. (Эти команды доступны только для сделок, в которых в поле **Выверка по** установлено значение *Строка*.)

    - **Обработать \> Подготовить** – подготовка набора начислений для каждой соответствующей строки сделки, но не их разноска.
    - **Обработать \> Управление ретробонусами** — обработка ряда проводок, которые обеспечивают стоимость ретробонуса для каждой строки сделки.
    - **Обработать \> Списать** — сторнировать ранее разнесенные проводки, чтобы списать их, чтобы можно было рассчитать новые проводки сделок по ретробонусам.

1. В появившемся диалоговом окне установите поля **Начальная дата** и **Конечная дата**, чтобы определить диапазон дат для расчета.
1. Выберите **ОК**, чтобы выполнить расчет.

### <a name="process-deals-using-a-batch-job"></a>Обработка сделок с использованием пакетного задания

Вместо обработки определенных сделок или строк сделки, можно выполнить пакетное задание для одновременной обработки нескольких сделок. Имеется также возможность применить фильтры записей и/или настроить повторяющееся расписание. Для обработки сделок с использованием пакетного задания выполните следующие действия.

1. Выполните одно из следующих действий.

    - Перейдите в раздел **Управление ретробонусами \> Периодические задачи \> Обработать \> Подготовить** для подготовки набора начислений для каждой соответствующей сделки, но без их разноски.
    - Перейдите в раздел **Управление ретробонусами \> Периодические задачи \> Обработать \> Управление ретробонусами**, чтобы обработать ряд проводок, которые обеспечивают стоимость ретробонуса для каждой строки сделки.
    - Перейдите в раздел **Управление ретробонусами \> Периодические задачи \> Обработать \> Списать**, чтобы сторнировать ранее разнесенные проводки, чтобы списать их, чтобы можно было рассчитать новые проводки сделок по ретробонусам.

1. В появившемся диалоговом окне на экспресс-вкладке **Параметры** в разделе **Период** установите значения в полях **Начальная дата** и **Конечная дата**, чтобы определить диапазон дат для проводок для расчета.
1. В разделе **Период гарантии** установите поля **Начальная дата** и **Конечная дата**, чтобы определить диапазон дат для гарантий для расчета.
1. На экспресс-вкладке **Включаемые записи** можно настроить фильтры для ограничения набора сделок, которые будут обрабатываться пакетным заданием. Эти параметры работают так же, как они работают для других типов пакетных заданий.
1. На экспресс-вкладке **Выполнять в фоновом режиме** можно настроить требуемые параметры пакетной обработки и планирования. Эти параметры работают так же, как они работают для других типов пакетных заданий.
1. Выберите **ОК**, чтобы выполнить и/или спланировать расчет.

## <a name="view-and-edit-rebate-management-transactions"></a>Просмотр и редактирование проводок управления ретробонусами

При обработке одной или нескольких сделок система создает проводки, которые можно просмотреть и, возможно, изменить перед их разноской.

1. Выполните одно из следующих действий.

    - Выберите сделку для просмотра проводок (например, на [странице **Все сделки управления ретробонусами**](rebate-management-deals.md)). В области действий на вкладке **Сделки управления ретробонусами** в группе **Проводки** выберите **Проводки** или **Проводки гарантии**, в зависимости от типа проводки, которую необходимо просмотреть.
    - Откройте сделку (например, на [странице **Все сделки управления ретробонусами**](rebate-management-deals.md)), чтобы просмотреть сведения о ней. На экспресс-вкладке **Управление ретробонусами** выберите строку сделки, для которой требуется просмотреть проводки. Затем на панели инструментов выберите **Проводки** или **Проводки гарантии**, в зависимости от типа проводки, которую необходимо просмотреть. (Эти кнопки доступны только для сделок, в которых в поле **Выверка по** установлено значение *Строка*.)

1. Будет открыта страница **Проводки по дате управления ретробонусами** или **Проводки гарантии управления ретробонусами**. Она содержит сетку, в которой каждая строка представляет коллекцию проводок по одному периоду ретробонусов или гарантий. Выберите строку в сетке, а затем в области действий выберите **Исходные проводки** для просмотра проводок, относящихся к этой строке.
1. На отображаемой странице отображается список проводок выбранного типа, относящихся к выбранной строке. Каждая проводка предоставляет соответствующие сведения в зависимости от типа проводки. Для проводок гарантии возможен только просмотр списка. Для других типов проводок на этой странице можно выполнить следующие действия:

    - Чтобы проверить общую стоимость всех затребованных проводок на странице, просмотрите поле **Затребованная сумма**.
    - Для просмотра дополнительных сведений о любой проводке выберите ее, затем перейдите на вкладку **Общие**, **Финансовая аналитика** или **Аналитика**.
    - Чтобы просмотреть все применяемые вычеты, выберите **Проводки вычетов** на панели операций. Дополнительные сведения см. в разделе [Принципы сокращения ретробонусов](rebate-reduction-principle.md).
    - Чтобы пометить проводки как затребованные или невостребованные, если используется процесс утверждения, выберите соответствующие строки, а затем на панели операций выберите одну из следующих команд. (Процессы заявок активируются на [странице **Параметры управления ретробонусами**](rebate-management-parameters.md).)

        - **Задать затребованные \> Все** — пометить все проводки как затребованные.
        - **Задать затребованные \> Выбранные** — пометить выбранные проводки как затребованные.
        - **Задать незатребованные \> Все** — пометить все проводки как незатребованные.
        - **Задать незатребованные \> Выбранные** — пометить выбранные проводки как незатребованные.

    - Чтобы разнести требование для одной или нескольких строк, выберите соответствующие строки, затем на панели операций выберите **Разнести**. (Кнопка **Разнести** доступна только для проводок ретробонусов. Она недоступна для проводок подготовки и списания.) В диалоговом окне **Разноска** поля **Начальная дата** и **Конечная дата** устанавливаются автоматически. Задайте поле **Дата разноски**, затем выберите **ОК**.
    - Для корректировки суммы, отображаемой для любой открытой или неразнесенной проводки, выберите проводку, а затем выполните одно из следующих действий:

        - Измените значение в поле **Скорректированная сумма**.
        - В области действий выберите **Задать коррекцию**. Затем в появившемся диалоговом окне в поле **Скорректированная сумма** введите значение.

> [!NOTE]
> При обработке следующего периода список проводок будет включать все незатребованные проводки из предыдущей разноски и любые новые проводки за выбранный период.

## <a name="post-rebates-transactions"></a>Разноска проводок ретробонусов

Чтобы разнести стоимость ретробонусов и вычетов, необходимо выполнить процесс разноски, если только система не настроена на автоматическую разноску этих сумм.

### <a name="set-up-the-system-to-post-all-transactions-automatically"></a>Настройка системы для автоматической разноски всех проводок

Чтобы настроить систему для разноски всех проводок сразу после их создания, включите параметры **Автоматически разносить журналы** и/или **Автоматически разносить накладные с произвольным текстом** на странице **Параметры управления ретробонусами**. Дополнительные сведения см. в разделе [Параметры управления ретробонусами](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Разноска проводок для всех строк для одной или нескольких сделок

Если автоматическая разноска не используется, после обработки соответствующих сделок выполните следующие шаги для просмотра и разноски созданных проводок по всем строкам для одной или нескольких сделок.

1. Откройте соответствующую [страницу со списком сделок с ретробонусами](rebate-management-deals.md) для типа сделки, с которой вы хотите работать.
1. Выберите строку для каждой сделки, которую необходимо разнести (или откройте сделку, которую необходимо разнести).
1. В области действий на вкладке **Сделки управления ретробонусами** в группе **Создать** выберите одну из следующих команд:

    - **Разнести \> Подготовить** — разноска доступных проводок начислений, которые были созданы.
    - **Разнести \> Управление ретробонусами** — разноска доступных проводок ретробонусов, которые были созданы.
    - **Разнести \> Списать** — разноска доступных проводок списания, которые были созданы.

1. В открывшемся диалоговом окне задайте поле **Дата разноски**. Затем установите поля **Начальная дата** и **Конечная дата**, чтобы определить диапазон дат для проводок, которые должны быть разнесены.
1. Выберите **ОК**, чтобы разнести проводки.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Разноска проводок для одной или нескольких конкретных строк сделки для выбранной сделки

Если автоматическая разноска не используется, после обработки соответствующих сделок выполните следующие шаги для просмотра и разноски созданных проводок по всем строкам для одной или нескольких конкретных строк сделки для выбранной сделки.

1. Откройте соответствующую [страницу со списком сделок с ретробонусами](rebate-management-deals.md) для типа сделки, с которой вы хотите работать.
1. Откройте сделку, в которой есть строка, для которой требуется выполнить разноску проводок.
1. В верхнем правом углу выберите вкладку **Строки**.
1. На экспресс-вкладке **Управление ретробонусами** выберите строку для каждой строки сделки, которую необходимо разнести.
1. На панели инструментов экспресс-вкладки **Управление ретробонусами** выберите одну из следующих команд. (Эти команды доступны только для сделок, в которых в поле **Выверка по** установлено значение *Строка*.)

    - **Разнести \> Подготовить** — разноска доступных проводок начислений, которые были созданы.
    - **Разнести \> Управление ретробонусами** — разноска доступных проводок ретробонусов, которые были созданы.
    - **Разнести \> Списать** — разноска доступных проводок списания, которые были созданы.

1. В открывшемся диалоговом окне задайте поле **Дата разноски**. Затем установите поля **Начальная дата** и **Конечная дата**, чтобы определить диапазон дат для проводок, которые должны быть разнесены.
1. Выберите **ОК**, чтобы разнести проводки.

### <a name="post-transactions-using-a-batch-job"></a>Разноска проводок с использованием пакетного задания

Вместо разноски проводок для определенных сделок или строк сделки, можно выполнить пакетное задание для одновременной разноски проводок нескольких сделок. Имеется также возможность применить фильтры записей и/или настроить повторяющееся расписание. Для разноски проводок с использованием пакетного задания выполните следующие действия.

1. Выполните одно из следующих действий.

    - Перейдите в раздел **Управление ретробонусами \> Периодические задачи \> Разнести \> Подготовить** для разноски доступных проводок начислений, которые были созданы.
    - Перейдите в раздел **Управление ретробонусами \> Периодические задачи \> Разнести \> Управление ретробонусами** для разноски доступных проводок ретробонусов, которые были созданы.
    - Перейдите в раздел **Управление ретробонусами \> Периодические задачи \> Разнести \> Списать** для разноски доступных проводок списания, которые были созданы.

1. В появившемся диалоговом окне на экспресс-вкладке **Параметры** в разделе **Период** задайте значение в поле **Дата разноски**. Затем установите поля **Начальная дата** и **Конечная дата**, чтобы определить диапазон дат для проводок, которые должны быть разнесены. 
1. В разделе **Период гарантии** установите поля **Начальная дата** и **Конечная дата**, чтобы определить диапазон дат для гарантий, которые требуется разнести.
1. На экспресс-вкладке **Включаемые записи** можно настроить фильтры для ограничения набора сделок, которые будут обрабатываться пакетным заданием. Эти параметры работают так же, как они работают для других типов пакетных заданий.
1. На экспресс-вкладке **Выполнять в фоновом режиме** можно настроить требуемые параметры пакетной обработки и планирования. Эти параметры работают так же, как они работают для других типов пакетных заданий.
1. Выберите **ОК**, чтобы выполнить и/или спланировать расчет.

## <a name="review-rebate-management-journals"></a>Просмотр журналов управления ретробонусами

После разноски проводок можно просмотреть итоговые журналы, документы или номенклатуры. Целевые проводки для ретробонусов и роялти основываются на типе платежа, который указан в профиле разноски и типе выходных данных ретробонуса. Например, если для вывода ретробонуса задано значение *Номенклатура*, будет создан заказ на продажу, который можно просмотреть с помощью целевых проводок. В качестве альтернативы, если платеж настроен на использование модуля расчетов с поставщиками, накладная поставщика для поставщика, настроенного для клиента, будет создана для ретробонусов клиента.

Для просмотра записей журнала, связанных со сделкой управления ретробонусами, выполните следующие действия.

1. Откройте соответствующую [страницу со списком сделок с ретробонусами](rebate-management-deals.md) для типа сделки, с которой вы хотите работать.
1. Выберите сделку, для которой требуется проверить записи журнала.
1. В области действий на вкладке **Сделки управления ретробонусами** в группе **Проводки** выберите **Проводки** или **Проводки ретробонусов**, в зависимости от типа проводок, которые необходимо просмотреть.
1. Убедитесь, что в поле **Показать** установлено значение *Все* или *Разнесенные*.
1. Найдите и выберите коллекцию проводок, которую необходимо проверить, затем на панели операций выберите одну из следующих кнопок. (Эти кнопки доступны только в том случае, если имеются соответствующие разноски для выбранной коллекции проводок.)

    - **Целевые проводки** — просмотр соответствующих журналов и других типов документов, которые были созданы в выбранной сделке.
    - **Номенклатуры** — проверка соответствующих номенклатур, созданных выбранной сделкой.

1. Появится список соответствующих журналов, документов или номенклатур. Чтобы просмотреть дополнительные сведения о каком-либо журнале, документе или номенклатуре, выберите соответствующую строку, затем на панели операций выберите **Просмотреть сведения**.