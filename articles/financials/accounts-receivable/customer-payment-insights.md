---
title: Аналитика платежей клиентов (предварительное ознакомление)
description: В этом разделе описывается, как анализ платежей клиентов помогает прогнозировать сроки оплаты накладной и помогает организациям создавать стратегии оптимизации, повышающие вероятность своевременной оплаты.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "344670"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="484e4-103">Аналитика платежей клиентов (предварительное ознакомление)</span><span class="sxs-lookup"><span data-stu-id="484e4-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="484e4-104">Эта функция является частью целевого выпуска и доступна только пользователям, принимающим участие в закрытом предварительном ознакомлении.</span><span class="sxs-lookup"><span data-stu-id="484e4-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="484e4-105">Эта функция будет включена в будущую общедоступную версию.</span><span class="sxs-lookup"><span data-stu-id="484e4-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="484e4-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="484e4-106">Overview</span></span>

<span data-ttu-id="484e4-107">Организациям часто сложно прогнозировать, когда клиент будет оплачивать свои накладные.</span><span class="sxs-lookup"><span data-stu-id="484e4-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="484e4-108">Отсутствие понимания может привести к неточным прогнозам денежных потоков, неэффективным процессам сбора и к возможности отгрузки заказов клиентам, которые могут представлять кредитный риск.</span><span class="sxs-lookup"><span data-stu-id="484e4-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="484e4-109">Анализ платежей клиентов (предварительное ознакомление) использует машинное обучение для прогнозирования, когда накладная будет оплачена.</span><span class="sxs-lookup"><span data-stu-id="484e4-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="484e4-110">Он также предоставляет стратегии оптимизации, которые можно адаптировать для повышения вероятности своевременной оплаты клиентами.</span><span class="sxs-lookup"><span data-stu-id="484e4-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="484e4-111">Прогнозы</span><span class="sxs-lookup"><span data-stu-id="484e4-111">Predictions</span></span>

<span data-ttu-id="484e4-112">Прогнозы оплаты позволяют организациям улучшить свои бизнес-процессы, помогая:</span><span class="sxs-lookup"><span data-stu-id="484e4-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="484e4-113">Легко идентифицировать накладные, для которых прогнозируется задержка оплаты.</span><span class="sxs-lookup"><span data-stu-id="484e4-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="484e4-114">Принять соответствующие меры для повышения шансов на своевременную оплату.</span><span class="sxs-lookup"><span data-stu-id="484e4-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="484e4-115">Анализ платежей клиентов (предварительное ознакомление) использует машинное обучение для прогнозирования, когда накладная будет оплачена.</span><span class="sxs-lookup"><span data-stu-id="484e4-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="484e4-116">В ней используется исторические данные по накладным, платежам и клиентам для создания модели машинного обучения, которая используется для прогнозирования срока оплаты накладной.</span><span class="sxs-lookup"><span data-stu-id="484e4-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="484e4-117">Для каждой открытой накладной анализ платежей клиентов (предварительное ознакомление) прогнозирует три вероятности оплаты:</span><span class="sxs-lookup"><span data-stu-id="484e4-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="484e4-118">Вероятность оплаты вовремя (в пределах срока оплаты накладной).</span><span class="sxs-lookup"><span data-stu-id="484e4-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="484e4-119">Вероятность оплаты в течение 30 дней от срока оплаты накладной.</span><span class="sxs-lookup"><span data-stu-id="484e4-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="484e4-120">Вероятность оплаты позже 30 дней от срока оплаты накладной.</span><span class="sxs-lookup"><span data-stu-id="484e4-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="484e4-121">Вероятности платежей можно просмотреть в разделе прогнозов.</span><span class="sxs-lookup"><span data-stu-id="484e4-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="484e4-122">[![Прогнозы платежей](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="484e4-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="484e4-123">Каждой накладной также присваивается наибольшая вероятность оплаты с использованием одного из трех сценариев прогнозируемых вероятностей платежа, определенных выше.</span><span class="sxs-lookup"><span data-stu-id="484e4-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="484e4-124">Сценарий с наибольшей вероятностью оплаты является победившим сценарием.</span><span class="sxs-lookup"><span data-stu-id="484e4-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="484e4-125">Например, предположим, что прогноз по накладной показывает 71% вероятности оплаты вовремя, 13 процентов вероятности того, что накладная оплачивается в течение 30 дней после срока оплаты накладной, 16 процентов вероятность того, что накладная будет оплачена позже 30 дней после срока оплаты.</span><span class="sxs-lookup"><span data-stu-id="484e4-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="484e4-126">Наибольшая вероятность указывает, что накладная будет оплачена вовремя, поэтому накладная будут помечена с вероятность оплаты вовремя.</span><span class="sxs-lookup"><span data-stu-id="484e4-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="484e4-127">[![Прогнозы платежей](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="484e4-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="484e4-128">Стратегии оптимизации</span><span class="sxs-lookup"><span data-stu-id="484e4-128">Optimization strategies</span></span>

<span data-ttu-id="484e4-129">Помимо прогнозов платежей, анализ платежей клиентов (предварительное ознакомление) может использовать стратегии оптимизации для повышения шансов на получение оплаты вовремя.</span><span class="sxs-lookup"><span data-stu-id="484e4-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="484e4-130">Это позволяет организациям делать анализ «Что если», позволяя пользователям корректировать параметры накладных и клиентов, а затем сравнивать соответствующее влияние на вероятность получения оплаты по накладным вовремя.</span><span class="sxs-lookup"><span data-stu-id="484e4-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="484e4-131">Например, организации может потребоваться оценить результат обновления скидки при оплате в накладных на вероятность получения платежей вовремя.</span><span class="sxs-lookup"><span data-stu-id="484e4-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="484e4-132">Когда накладные оптимизированы для использования новой скидки, пользователи могут просматривать результаты применения скидки на вероятность получения платежей для этих накладных вовремя.</span><span class="sxs-lookup"><span data-stu-id="484e4-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="484e4-133">Если стоимость применения скидки минимальна по сравнению с преимуществом получение платежей вовремя, организация может решить применить выбранную скидку для всех будущих открытых заказов.</span><span class="sxs-lookup"><span data-stu-id="484e4-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="484e4-134">В настоящее время только скидка доступна как стратегия оптимизации для анализа платежей клиентов (предварительное ознакомление).</span><span class="sxs-lookup"><span data-stu-id="484e4-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="484e4-135">[![Оптимизированные прогнозы](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="484e4-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="484e4-136">Как получить аналитику платежей клиентов (предварительное ознакомление)</span><span class="sxs-lookup"><span data-stu-id="484e4-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="484e4-137">Если вы хотите попробовать аналитику платежей клиентов (предварительное ознакомление), отправьте по электронной почте сообщение [рабочей группе предварительной версии финансовой аналитики](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="484e4-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="484e4-138">Заявление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="484e4-138">Privacy Statement</span></span>

<span data-ttu-id="484e4-139">Версии для предварительного ознакомления хранят информацию о клиентах в США.</span><span class="sxs-lookup"><span data-stu-id="484e4-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="484e4-140">Кроме того, версии для предварительного ознакомления (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 for Finance and Operations, (2) не включаются в соглашение об уровне обслуживания для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.</span><span class="sxs-lookup"><span data-stu-id="484e4-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>
