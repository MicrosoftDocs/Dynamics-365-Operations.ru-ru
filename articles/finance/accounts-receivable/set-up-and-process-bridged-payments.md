---
title: Настройка и обработка платежей с промежуточными счетами
description: В этой статье объясняется, как настраивать и обрабатывать платежи клиентам с промежуточными счетами. Платеж с промежуточным счетом — это платеж, который разносится в главную книгу в два этапа.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb563008f156e1bfa6e4e9a705e9170342719ce7
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775177"
---
# <a name="set-up-and-process-bridged-payments"></a>Настройка и обработка платежей с промежуточными счетами

[!include [banner](../includes/banner.md)]

Платеж с промежуточным счетом — это платеж, который разносится в главную книгу в два этапа. Обычно этот подход используется, когда для метода платежа задано значение **Банк** и необходимо выполнять разноску проводок на банковский счет только тогда, когда выполнен клиринг проводки в банке. Однако его можно также использовать для счета ГК. В этом случае суммы будут перемещены с одного счета ГК на другой счет ГК при обработке разноски на промежуточный счет.

Можно создавать платежи с промежуточными счетами из модуля расчетов с поставщиками или расчетов с клиентами. Хотя в этой статье описан порядок настройки разноски на промежуточный счет для расчетов с клиентами, шаги для проводок по расчетам с поставщиками аналогичны.

## <a name="set-up-bridging-posting"></a>Настройка разноски на промежуточный счет

Для использования разноски на промежуточный счет необходимо настроить один или несколько способов оплаты, чтобы они использовали метод **Разноска на промежуточный счет**. Затем необходимо выбрать промежуточный счет.

1. Перейдите в раздел **Расчеты с клиентами &gt; Настройка платежей &gt; Способы оплаты**.
2. Выберите существующий метод платежа для включения разноски на промежуточный счет. Можно также создать новый способ оплаты.
3. Установите флажок **Разноска на промежуточный счет**.
4. В поле **Промежуточный счет** выберите счет ГК, на который должны быть разнесены платежи, прежде чем будет выполнен их клиринг на банковский счет.
5. Закройте страницу.

## <a name="process-and-transfer-bridging-posting"></a>Обработка и перенос разноски на промежуточный счет

Чтобы создать и обработать разноску на промежуточный счет, выполните следующие действия.

1. Перейдите в раздел **Расчеты с клиентами &gt; Платежи &gt; Журнал платежей клиентов**.
2. Выберите **Создать**, чтобы создать журнал.
3. В поле **Имя** выберите имя.
4. Добавьте строки в журнал платежей клиента и выберите способ оплаты, настроенный для разноски на промежуточный счет.
5. Разноска журнала. Проводки будут разнесены на счет ГК, который выбран в поле **Промежуточный счет** в предыдущей процедуре.

Когда после выполнения клиринга проводки в банке вы хотите перенести платеж с промежуточного счета на платежный счет, указанный для метода оплаты, выполните следующие действия.

1. Перейдите к **Главная книга &gt; Записи в журнале &gt; Общие журналы**.
2. Выберите **Создать**, чтобы создать журнал.
3. В поле **Имя** выберите имя.
4. Выберите **Строки**, чтобы открыть сведения о журнале.
5. Выберите **Функции &gt; Выбрать проводки на промежуточный счет**.
6. Пометьте каждый платеж, для которого выполнен клиринг, затем выберите **Принять**.
7. Разноска журнала.
