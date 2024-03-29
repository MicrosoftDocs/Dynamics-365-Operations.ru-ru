---
title: Обработка распределений
description: Эта статья представляет информацию о распределениях, о параметрах для их обработки в Microsoft Dynamics 365 Finance и о том, как их можно использовать при планировании бюджета. Распределения используются для распределения сумм на несколько комбинаций счетов ГК. Они помогают обеспечить, что расходы или выручка начисляются на правильные объекты учета.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: kfend
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0629b32d39f4d74ec37eebe92b92e0b186b5fce2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877993"
---
# <a name="process-allocations"></a>Обработка распределений

[!include [banner](../includes/banner.md)]

Эта статья представляет информацию о распределениях, параметры для их обработки и как их можно использовать в бюджетном планировании. Распределения используются для распределения сумм на несколько комбинаций счетов ГК. Они помогают обеспечить, что расходы или выручка начисляются на правильные объекты учета.

Этот процесс поддерживают следующие возможности:

-   Распределение сумм проводок вручную с помощью действия "Разделить" в распределении по бухгалтерским счетам или путем применения шаблонов финансовых аналитик по умолчанию к документу. Дополнительные сведения см. в разделе [Распределения по бухгалтерским счетам](../accounts-payable/accounting-distributions.md).
-   Автоматическое распределение сумм проводок на основании условий распределения, определенных в отдельном счете ГК. Записи счета распределения будут созданы для каждого журнала на основании процента и целевого счета ГК, когда запись учета соответствует критериям, определенным как исходный счет ГК. Дополнительные сведения см. в разделе [Условия распределения счета ГК](../general-ledger/main-account-allocation-terms.md)
-   Автоматическое распределение сальдо ГК или фиксированных сумм на основании правила распределения ГК. Правила распределения ГК обрабатываются на периодической основе с помощью журналов распределения. Дополнительные сведения см. в разделе [Правила распределения](../general-ledger/ledger-allocation-rules.md).

###  <a name="allocations-in-budget-planning"></a>Распределения в бюджетном планировании

Правила распределения ГК можно использовать для бюджетных планов. Если правила распределения главной книги используются при бюджетном планировании, правила распределения работают таким же образом, как в главной книге, но исходные данные и конечные данные поступают из бюджетного плана. Правила распределения главной книги для использования в бюджетных планах можно выбрать вручную. В качестве альтернативы можно использовать график распределения, выполняемый в рамках workflow-процесса.

> [!NOTE]
> При бюджетной планировании невозможно использовать внутрихолдинговые правила распределения главной книги.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
