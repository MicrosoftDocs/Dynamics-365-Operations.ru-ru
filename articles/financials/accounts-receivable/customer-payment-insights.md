---
title: "Аналитика платежей клиентов (предварительное ознакомление)"
description: "В этом разделе описывается, как анализ платежей клиентов помогает прогнозировать сроки оплаты накладной и помогает организациям создавать стратегии оптимизации, повышающие вероятность своевременной оплаты."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: 
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---

# <a name="customer-payment-insights-preview"></a>Аналитика платежей клиентов (предварительное ознакомление)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Эта функция является частью целевого выпуска и доступна только пользователям, принимающим участие в закрытом предварительном ознакомлении. Эта функция будет включена в будущую общедоступную версию.

# <a name="overview"></a>Обзор

Организациям часто сложно прогнозировать, когда клиент будет оплачивать свои накладные. Отсутствие понимания может привести к неточным прогнозам денежных потоков, неэффективным процессам сбора и к возможности отгрузки заказов клиентам, которые могут представлять кредитный риск. Анализ платежей клиентов (предварительное ознакомление) использует машинное обучение для прогнозирования, когда накладная будет оплачена. Он также предоставляет стратегии оптимизации, которые можно адаптировать для повышения вероятности своевременной оплаты клиентами.

## <a name="predictions"></a>Прогнозы

Прогнозы оплаты позволяют организациям улучшить свои бизнес-процессы, помогая:

-   Легко идентифицировать накладные, для которых прогнозируется задержка оплаты.
-   Принять соответствующие меры для повышения шансов на своевременную оплату.

Анализ платежей клиентов (предварительное ознакомление) использует машинное обучение для прогнозирования, когда накладная будет оплачена. В ней используется исторические данные по накладным, платежам и клиентам для создания модели машинного обучения, которая используется для прогнозирования срока оплаты накладной.

Для каждой открытой накладной анализ платежей клиентов (предварительное ознакомление) прогнозирует три вероятности оплаты:

-  Вероятность оплаты вовремя (в пределах срока оплаты накладной).
-  Вероятность оплаты в течение 30 дней от срока оплаты накладной.
-  Вероятность оплаты позже 30 дней от срока оплаты накладной.

Вероятности платежей можно просмотреть в разделе прогнозов.

[![Прогнозы платежей](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Каждой накладной также присваивается наибольшая вероятность оплаты с использованием одного из трех сценариев прогнозируемых вероятностей платежа, определенных выше. Сценарий с наибольшей вероятностью оплаты является победившим сценарием.


Например, предположим, что прогноз по накладной показывает 71% вероятности оплаты вовремя, 13 процентов вероятности того, что накладная оплачивается в течение 30 дней после срока оплаты накладной, 16 процентов вероятность того, что накладная будет оплачена позже 30 дней после срока оплаты. Наибольшая вероятность указывает, что накладная будет оплачена вовремя, поэтому накладная будут помечена с вероятность оплаты вовремя.

[![Прогнозы платежей](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Стратегии оптимизации

Помимо прогнозов платежей, анализ платежей клиентов (предварительное ознакомление) может использовать стратегии оптимизации для повышения шансов на получение оплаты вовремя. Это позволяет организациям делать анализ «Что если», позволяя пользователям корректировать параметры накладных и клиентов, а затем сравнивать соответствующее влияние на вероятность получения оплаты по накладным вовремя.

Например, организации может потребоваться оценить результат обновления скидки при оплате в накладных на вероятность получения платежей вовремя. Когда накладные оптимизированы для использования новой скидки, пользователи могут просматривать результаты применения скидки на вероятность получения платежей для этих накладных вовремя. Если стоимость применения скидки минимальна по сравнению с преимуществом получение платежей вовремя, организация может решить применить выбранную скидку для всех будущих открытых заказов.

> [!NOTE] 
> В настоящее время только скидка доступна как стратегия оптимизации для анализа платежей клиентов (предварительное ознакомление).

[![Оптимизированные прогнозы](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Как получить аналитику платежей клиентов (предварительное ознакомление)

Если вы хотите попробовать аналитику платежей клиентов (предварительное ознакомление), отправьте по электронной почте сообщение [рабочей группе предварительной версии финансовой аналитики](mailto:fiap@microsoft.com). 

## <a name="privacy-statement"></a>Заявление о конфиденциальности

Версии для предварительного ознакомления хранят информацию о клиентах в США. Кроме того, версии для предварительного ознакомления (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 for Finance and Operations, (2) не включаются в соглашение об уровне обслуживания для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.
