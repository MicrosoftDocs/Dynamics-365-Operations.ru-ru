---
title: Настройка правил сопоставления банковской выверки
description: Эта статья описывает, как настроить правила сопоставления выверки и наборы правил сопоставления выверки, чтобы помочь процессу банковской выверки. Правила сопоставления выверки — это набор критериев, используемых при фильтрации строк банковской выписки и строки банковского документа во время процесса выверки.
author: angelad116
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac5ab5e2bcb9a63bb52d5a74bd5e4b5db51ba603
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803946"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Настройка правил сопоставления банковской выверки

[!include [banner](../includes/banner.md)]

Эта статья описывает, как настроить правила сопоставления выверки и наборы правил сопоставления выверки, чтобы помочь процессу банковской выверки. Правила сопоставления выверки — это набор критериев, используемых при фильтрации строк банковской выписки и строки банковского документа во время процесса выверки.

Можно настроить правила сопоставления выверки и наборы правил сопоставления выверки, чтобы помочь процессу банковской выверки. Правило сопоставления выверки — это набор критериев, используемых при фильтрации строк банковской выписки и строк банковской проводки Dynamics 365 Finance во время процесса выверки. Используйте страницу **Правила сопоставления выверки**, чтобы настроить правила сопоставления выверки. Вы можете настроить больше чем одно правило сопоставления и после этого создать правило сопоставления выверки на странице **Наборы правил сопоставления выверки**. 

> [!NOTE] 
> Правила сопоставления банковской выверки используется при выверке электронной банковской выписки, используя предварительную банковскую выверку. 

В странице **Правила сопоставления выверки**, можно выбрать, какие действия и критерии выбора используются, когда правило сопоставления выполняется. В группе полей **Действия** выберите действие, которое будет выполнено, когда правило сопоставления выполняется во время процесса выверки.  

По умолчанию правила сопоставления будут соответствовать первому банковскому документу, удовлетворяющему критериям правила сопоставления. Если критерию правила соответствует несколько банковских документов, параметр, требующий ручного сопоставления, может быть включен путем перехода к пункту **Управление банком и кассовыми операциями > Настройка > Параметры управления банком и кассовыми операциями > Банковская выверка > Требовать ручного сопоставления, когда правила сопоставления расширенной банковской выверки обнаруживают несколько документов с соответствующей суммой**.

> [!NOTE] 
> Выбранный вариант определяет отображаемые поля.

| Действие | описание   | Критерии выбора, доступные, когда действие выбрано     |
|--------|---------------|----------------------------------------------------------|
| **Сопоставить с банковским документом**       | Создание критериев для определения того, как строки банковских документов и банковской выписки сопоставляются, когда правило сопоставления запускается со страницы **Лист банковской выверки**. Строки проводки выбираются согласно настроенным дополнительным критериям на экспресс-вкладках. | <ul><li>**Раздел 1: Определите правило соответствия** — выберите критерии для того, чтобы определить, которые банковские выписки следует сопоставить с банковскими проводками Finance.</li><li> **Шаг 2 (Необязательный): Выберите линии выписки для того, чтобы снова выполнить правила сопоставления:**  Примените фильтр на строке выписки, относительно которой снова выполнить правила.</li></ul>                                       |
| **Очистить строки реверсирования выписки** | Создание критериев, чтобы определить, как строки реверсирования выписки следует удалить из страницы **Лист банковской выверки** когда правило сопоставления выполняется. Этот параметр используется, когда банк совершает ошибку и есть две строки банковской выписки, перечисленные в импортированной банковской выписке и строки необходимо выверить. |<ul><li> **Шаг 1**: **Найти строки выписки реверсирования** — Добавить критерии выбора для выбора строк банковской выписки реверсирования. Например, чтобы выбрать только чеки, выберите **Код банковской проводки** в поле **Поле**, выберите знак плюс (+) в поле **Оператор**, а затем введите **Чеки** в поле **Значение**. </li><li>**Шаг 2: Поиск строк исходной выписки** – можно добавить критерии выбора, чтобы сопоставлять строки банковского документа к строкам банковской выписки. </li><li>**Шаг 3: Поиск банковских проводок Finance** — можно добавить критерии выбора, чтобы сопоставлять банковские проводки Finance к строкам банковской выписки.</li></ul>  |
| **Пометить новые проводки**          | Создание критериев, чтобы определить, как новые проводки следует пометить на странице **Лист банковской выверки**, когда правило сопоставления выполняется.                                                                                                                                                                 | <ul><li>**Шаг 1: Поиск строк выписки** — добавьте поля выбора, чтобы определить, которые линии банковской выписки должны быть выбраны со страницы **Лист банковской выверки**.</li><li> **Шаг 2: Поиск в финансах и операциях** — можно добавить критерии выбора для поиска строк банковского документа. Если никакой документ банковский не найден, то строка выписки будет отмечена как новая проводка. </li></ul>         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

