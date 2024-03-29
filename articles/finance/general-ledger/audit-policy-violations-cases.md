---
title: Нарушения политики аудита и соответствующие случаи
description: Статья описывает, как обращения аудита создаются из нарушений правил политики аудита. Она также включает информацию о различных способах, которые политики аудита используют для диапазон дат выбора документа.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: kfend
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbef92865c0a463b3922d7cc6c3f46759ffdc9ad
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711127"
---
# <a name="audit-policy-violations-and-cases"></a>Нарушения политики аудита и соответствующие случаи

[!include [banner](../includes/banner.md)]

Статья описывает, как обращения аудита создаются из нарушений правил политики аудита. Она также включает информацию о различных способах, которые политики аудита используют для диапазон дат выбора документа.

## <a name="how-audit-cases-are-generated"></a>Как создаются обращения аудита

Политики аудита используются для определения отчетов по расходам, заказов на покупку и накладных поставщика, которые не соответствуют бизнес-правилам, определенным и настроенным в качестве правил политики аудита. 

Политики аудита выполняются в пакетном режиме. При выполнении политики аудита все правил политики, которые являются частью этой политики, выполняются одновременно.

Каждое правило политики оценивает комплект документов. Правило политики выбирает документы, которые находятся в требуемом диапазоне дат и соответствуют указанным критериям. Например, одно из правил политик может отбирать отчеты по расходам, в которых упоминаются обеды стоимостью более 50 долларов. В другом правиле политики могут отбираться накладные поставщика, подлежащие оплате в пользу определенного поставщика. Для каждого документа в выбранном наборе создается нарушение. Такое нарушение – это запись о том, что определенный документ, например, накладная 12345, не соответствует правилу политики. 

Несколько записей о нарушениях аудита группируются и связываются с обращениями аудита. По умолчанию обращения для каждой политики аудита группируются по правилу политики аудита. Если вы предпочитаете, то вы можете выбрать другие критерии группировки путем использования страница **Критерии группировки обращений**. Например, можно сгруппировать заголовки расходов по коду проекта, а накладные поставщика — по счету поставщика. В этом случае все нарушения заголовков расходов с одинаковым кодом проекта группируются в одно обращение, и все накладные поставщика с одинаковым счетом поставщика группируются в одно обращение. 

> [!NOTE]
> Для правил политики аудита, которые основаны на типе запроса **Дубликат**, нарушения не группируются по правилу политики или по критериям, заданным на странице **Критерии группировки обращений**. Вместо этого они группируются по критериям, которые встроены в правило политики аудита. Например, если правило политики оценивает отчеты по расходам на наличие двойных расходов с одинаковым кодом получателя платежа и датой, все расходы с одинаковыми значениями в этих полях будут представлять одно обращение. Все расходы которые имеют различные значения, будут отдельным случаем.

После создания обращений аудита они обрабатываются посредством типовых процессов управления обращениями.

## <a name="document-selection-date-ranges"></a>Диапазоны дат выбора документов
Если политика аудита запущена, все правила политики выбирают документы указанного типа, дата которых находится в диапазоне дат выбора документа. Диапазон дат выбора документа определяется на странице **Дополнительные параметры**. Многие документы имеют несколько дат, связанных с ними. Поле даты, которое использует правило политики аудита, указано на странице **Тип правила политики**.

Вот некоторые другие способы, которыми политика аудита использует диапазон дат выбора документа:

-   Политика использует версию каждого правила политики, которое является действующим в последний день диапазона дат выбора документа. Вы можете осмотреть даты действия для каждого правила политики на странице списка **Политики аудита**.
-   Политика использует узлы организации, связанные с политикой на последний день диапазона дат выбора документа. Только узлы организации, которые в настоящее время связаны с политикой, отображаются на странице списка **Политики аудита**.
-   Для правил политики, основанных на типе запроса **Поиск по списку**, политика оценивает документы для отслеживаемых объектов, действующих в последний день диапазона дат выбора документа.


Дополнительные сведения см. в разделе [Правила политики аудита](audit-policy-rules.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
