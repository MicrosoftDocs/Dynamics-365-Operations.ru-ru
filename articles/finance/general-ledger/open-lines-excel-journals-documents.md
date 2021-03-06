---
title: Публикация строк журналов и документов из Excel
description: В этом разделе объясняется, как вводить и публиковать строки для финансовых журналов из Microsoft Excel. Сюда входят сведения о различных шаблонах, которые можно использовать в зависимости от типа вводимых проводок.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d95584ff02eac7353b01c2159be02e694b4c83fe
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897752"
---
# <a name="publish-journal-lines-and-documents-from-excel"></a>Публикация строк журналов и документов из Excel

[!include [banner](../includes/banner.md)]

В этом разделе объясняется, как вводить и публиковать строки для финансовых журналов из Microsoft Excel. Сюда входят сведения о различных шаблонах, которые можно использовать в зависимости от типа вводимых проводок.

Пользователи могут вводить и публиковать строки для финансовых журналов из Microsoft Excel. После того как пользователь создал журнал, кнопка **Открыть строки в Excel** отображает доступные шаблоны. Шаблоны разработаны для поддержки конкретных сценариев, однако не все комбинации типа счета поддерживаются в журнале. В следующей таблице показаны доступных шаблонов и типы счетов, которые они поддерживают.

| Шаблон             | Поддерживаемые типы счетов | Порядок доступа к шаблону                                                          |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| Строки журнала ГК     | Счет: ГК, Клиент, Поставщик, Банк Корр. счет: ГК, Клиент, Поставщик, Банк Внутрихолдинговый поддерживается.       | Общий журнал                                                                         |
| Регистрация накладных         | Счет: Поставщик Корр. счет: ГК Внутрихолдинговый не поддерживается.                                                    | Расчеты с поставщиками — Регистрация накладных                                                                     |
| Журнал накладных          | Счета: Поставщик Корр. счет: ГК Внутрихолдинговый поддерживается.                                                      | Журнал накладных AP                                                                      |
| Накладная поставщика           |                                                                                                                         | Накладная поставщика                                                                          |
| Журнал накладных клиента | Счет: Клиент Корр. счет: ГК Внутрихолдинговый поддерживается.                                                     | Общий журнал                                                                         |
| Накладная с произвольным текстом        |                                                                                                                         | На странице **Накладная с произвольным текстом** щелкните **Открыть в Excel** (значок Microsoft Office). |
| Журнал "Основные средства"     | Основное средство в ГК, банк, клиент или поставщик. Внутрихолдинговый не поддерживается.                                               | Журнал основных средств                                                                     |
| Журнал платежей поставщикам   | Счет: Поставщик Корр. счет: ГК, Банк Внутрихолдинговый поддерживается.                                                 | Журнал платежей поставщикам                                                                  |
| Журнал платежей клиентов | Счет: Клиент Корр. счет: ГК, Банк Внутрихолдинговый поддерживается.                                               | Журнал платежей клиентов                                                                |
| Журнал расходов по проекту  | Счет: Проект, ГК, Клиент, Поставщик, Банк Корр. счет: Проект, ГК, Клиент, Поставщик, Банк Внутрихолдинговый поддерживается. | Общий журнал расходов (в области "Управление и учет по проектам")                       |

При публикации строк они проходят проверку, чтобы убедиться в том, что они соответствуют правилам, которые настроены в финансовых журналах. После публикации строк пользователи могут редактировать или разносить ваучеры из Dynamics 365 Finance. 

Чтобы добавить финансовые аналитики в шаблон требуются дополнительные изменения. Дополнительные сведения см. в разделе [Добавление аналитик в шаблон Microsoft Excel](../../fin-ops-core/dev-itpro/financial/add-dimensions-excel-templates.md). После добавления аналитик к объекту они будут доступны в конструкторе Excel и могут быть добавлены в шаблон.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]