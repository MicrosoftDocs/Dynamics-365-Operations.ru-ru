---
title: Процесс настройки расширенной банковской выверки
description: Расширенная банковская выверка позволяет импортировать электронные банковские выписки и автоматически выверять их с банковскими проводками в Microsoft Dynamics 365 Finance. В этой статье объясняется, как настроить процессы выверки.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a1757f7901a12a5b0fc3de730953c5b79cbefb
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715452"
---
# <a name="advanced-bank-reconciliation-setup-process"></a>Процесс настройки расширенной банковской выверки

[!include [banner](../includes/banner.md)]

Расширенная банковская выверка позволяет импортировать электронные банковские выписки и автоматически выверять их с банковскими проводками в Microsoft Dynamics 365 Finance. В этой статье объясняется, как настроить процессы выверки.  

Существует ряд элементов, которые необходимо настроить перед использованием функции расширенной банковской выверки. Дополнительные сведения о настройке импорта банковской выписки см. в разделе [Настройка процесса импорта расширенной банковской выверки](set-up-advanced-bank-reconciliation-import-process.md).  Ниже приведены требования к настройке процесса выверки.

## <a name="transaction-codes"></a>Коды проводок
Коды проводок могут использоваться как часть правил сопоставления банковской выверки. Коды проводок помогают сопоставлять только одинаковые типы проводок в Finance и банковской выписке. Чтобы выполнять этот сопоставление типов, необходимо сначала определить типы проводок, используемых для банковских проводок из Finance, затем сопоставить эти типы с кодами проводок выписок, используемых вашим банком. Типы проводок для банковских проводок определяются на странице **Тип банковской проводки**. Здесь также определяется счет ГК, который должен использоваться для разноски, связанной с этим типом проводки. 

После определения кодов банковской проводки необходимо сопоставить их кодам проводки, используемым в ваших электронных банковских выписках. Этот процесс сопоставления выполняется с помощью страницы **Сопоставление кодов проводок**. Сопоставление кодов проводок выполняется отдельно для каждого банковского счета.

## <a name="matching-rules-and-matching-rule-sets"></a>Правила сопоставления и наборы правил сопоставления
Правила сопоставления позволяют определить критерии для автоматической выверки между банковскими проводками Finance и проводками из банковской выписки. Настройка правил сопоставления выполняется на странице **Правила сопоставления выверки**. Дополнительные сведения см. в разделе [Настройка правил сопоставления банковской выверки](set-up-bank-reconciliation-matching-rules.md). 

Наборы правил сопоставления используются для определения группы правил сопоставления, которые выполняются последовательно во время процесса банковской выверки.  Наборы правил сопоставления настраиваются на странице **Наборы правил сопоставления выверки**.

## <a name="cash-and-bank-management-parameters"></a>Параметры управления банком и кассовыми операциями
Существует несколько параметров, относящихся к процессу расширенной банковской выверки на странице **Параметры управления банком и кассовыми операциями**.  Параметр **Показывать сумму строки выписки в формате дебета/кредита** изменяет представление сумм на странице **Банковская выписка**. Если этот параметр установлен, суммы проводок банковской выписки отображаются в отдельных столбцах дебета и кредита. Если флажок не установлен, суммы проводок банковской выписки будут показаны в одном столбце суммы с соответствующим знаком. 

Параметры проверки, заданные на странице параметров, переопределяют значения, заданные в правилах сопоставления. Например, нельзя вручную или автоматически сопоставлять документы, даты которых различаются больше, чем задано на странице параметров. Кроме того, если установлен флажок **Проверить сопоставление типов транзакций**, типы проводок должны быть сопоставлены между банковской проводкой в Finance и проводкой банковской выписки, чтобы эти проводки можно было сопоставить вручную или автоматически. 

Также необходимо настроить необходимые номерные серии на странице **Параметры управления банком и кассовыми операциями**.  На вкладке **Номерные серии** задайте коды номерных серий для ссылок **код загрузки, код инструкции, код выверки и банковская выверка**.

## <a name="bank-account-reconciliation-options"></a>Параметры выверки банковского счета
Сначала необходимо включить расширенную банковскую выверку для банковского счета. Дополнительные параметры будут доступны на странице **Банковский счет** после включения функции расширенной банковской выверки. 

Функция **Использовать банковские выписки в качестве подтверждения электронных платежей** интегрирует функцию банковской выверки со статусами электронных платежей. Когда эта функция включена, банковский документ будет создаваться автоматически, если статус электронных платежей — **Отправлено**. Кроме того, статус электронных платежей будет изменен с **Отправлено** на **Получено** после сопоставления, выверки и разноски платежа. 

Поле **Имя банковского счета в выписках** — это имя, используемое для банковского счета в электронных банковских выписках. Это имя используется при определении того, какие проводки будут импортированы для банковского счета из выписки, которая может содержать сведения для нескольких банковских счетов. 

Параметр **Выполнить выверку после импорта** автоматически проверяет банковскую выписку, создает новую банковскую выверку и лист и выполняет набор правил сопоставления по умолчанию. Эта функция автоматизирует процесс до того момента проводки, когда необходимо сопоставление вручную. Настройка в банковском счете будет использоваться по умолчанию при импорте.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
