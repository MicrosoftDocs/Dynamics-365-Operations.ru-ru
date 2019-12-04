---
title: Аналитика платежей клиентов (предварительная версия)
description: В этой теме описывается функция анализа платежей, которая помогает улучшить понимание типичных способов оплаты отдельных клиентов и может определить обстоятельства, которые обосновывают инициирование процессов сбора данных раньше, чем вы это обычно делали.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774034"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="ba32a-103">Аналитика платежей клиентов (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="ba32a-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ba32a-104">В этой теме описывается функция анализа платежей, которая помогает улучшить понимание типичных способов оплаты отдельных клиентов и может определить обстоятельства, которые обосновывают инициирование процессов сбора данных раньше, чем вы могли это обычно делать.</span><span class="sxs-lookup"><span data-stu-id="ba32a-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="ba32a-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="ba32a-105">Overview</span></span>

<span data-ttu-id="ba32a-106">Организациям часто сложно прогнозировать, когда клиенты будут оплачивать свои накладные.</span><span class="sxs-lookup"><span data-stu-id="ba32a-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="ba32a-107">Отсутствие аналитики приводит к снижению точности прогнозов движения денежных средств, запоздалому запуску процессов сбора и заказов, выпущенных для клиентов, которые по умолчанию могут иметь свой платеж.</span><span class="sxs-lookup"><span data-stu-id="ba32a-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="ba32a-108">Анализ платежей клиентов (предварительный просмотр) помогает организациям прогнозировать сроки оплаты накладных клиентов и создавать стратегии сбора, повышающие вероятность своевременной оплаты.</span><span class="sxs-lookup"><span data-stu-id="ba32a-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="ba32a-109">Прогнозы</span><span class="sxs-lookup"><span data-stu-id="ba32a-109">Predictions</span></span>

<span data-ttu-id="ba32a-110">Прогнозы платежей позволяют организациям совершенствовать свои бизнес-процессы, помогая им легко определять накладные, которые, вероятно, будут оплачены с задержкой, и предпринимать соответствующие меры, которые повысят шансы на получение оплаты вовремя.</span><span class="sxs-lookup"><span data-stu-id="ba32a-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="ba32a-111">Используя модель машинного обучения, которая использует исторические накладные, платежи и данные о клиентах, аналитика платежей клиентов (предварительный просмотр) более точно предсказывает, когда клиент оплатит неоплаченную накладную.</span><span class="sxs-lookup"><span data-stu-id="ba32a-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="ba32a-112">Для каждой открытой накладной анализ платежей клиентов (предварительный просмотр) прогнозирует три вероятности оплаты:</span><span class="sxs-lookup"><span data-stu-id="ba32a-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="ba32a-113">Вероятность оплаты вовремя</span><span class="sxs-lookup"><span data-stu-id="ba32a-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="ba32a-114">Вероятность поздней оплаты</span><span class="sxs-lookup"><span data-stu-id="ba32a-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="ba32a-115">Вероятность очень поздней оплаты</span><span class="sxs-lookup"><span data-stu-id="ba32a-115">Probability of payment being made very late</span></span>

<span data-ttu-id="ba32a-116">Чтобы помочь организациям понять общую сумму платежей, которую они могут ожидать от клиента в одном из трех сегментов (вовремя, поздно, очень поздно), аналитика платежей клиентов (предварительный просмотр) также предоставляет сводное представление по ожидаемым платежам.</span><span class="sxs-lookup"><span data-stu-id="ba32a-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="ba32a-117">[![Сводное представление о прогнозе платежей](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="ba32a-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="ba32a-118">Кроме того, каждой накладной назначается вероятность оплаты вовремя.</span><span class="sxs-lookup"><span data-stu-id="ba32a-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="ba32a-119">Если вероятность оплаты составляет менее 50%, накладные помечаются красным кружком, чтобы указать на то, что для этих накладных, возможно, потребуется уделить внимание сбору.</span><span class="sxs-lookup"><span data-stu-id="ba32a-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="ba32a-120">[![Список вероятностей оплаты](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="ba32a-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="ba32a-121">Аналитика платежей клиентов (предварительная версия) также предоставляет контекстные сведения для объяснения прогноза, например, верхние коэффициенты, влияющие на прогнозы, текущее состояние бизнеса с клиентом и подробные сведения об историческом поведении платежей клиентов.</span><span class="sxs-lookup"><span data-stu-id="ba32a-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="ba32a-122">Во многих компаниях процесс сбора был реактивным действием; процесс сбора не начинается, пока не наступит срок оплаты накладных.</span><span class="sxs-lookup"><span data-stu-id="ba32a-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="ba32a-123">Благодаря аналитике платежей клиентов (предварительная версия) организации могут действовать проактивно в отношении сборов.</span><span class="sxs-lookup"><span data-stu-id="ba32a-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="ba32a-124">В этом случае больше не придется ждать, пока проводки не станут активными в связи с началом процесса сбора.</span><span class="sxs-lookup"><span data-stu-id="ba32a-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="ba32a-125">Вместо этого они могут использовать функцию прогнозирования платежей, чтобы определить, улучшат ли проактивные сборы вероятность оплаты вовремя.</span><span class="sxs-lookup"><span data-stu-id="ba32a-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="ba32a-126">Прогнозирование платежей также дает компаниям сведения, необходимые для раннего начала процесса сбора.</span><span class="sxs-lookup"><span data-stu-id="ba32a-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="ba32a-127">Методология</span><span class="sxs-lookup"><span data-stu-id="ba32a-127">Methodology</span></span>

<span data-ttu-id="ba32a-128">Разработка и развертывание решения ИИ выполняется сложно.</span><span class="sxs-lookup"><span data-stu-id="ba32a-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="ba32a-129">Нужна группа специалистов по обработке данных, эксперты по теме и инженеры, работающими в течение продолжительного периода времени для формулировки, разработки, развертывания и поддержки пригодного к использованию решения ИИ.</span><span class="sxs-lookup"><span data-stu-id="ba32a-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="ba32a-130">Развертывание и использование решений ИИ в Finance упрощается.</span><span class="sxs-lookup"><span data-stu-id="ba32a-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="ba32a-131">Мы упаковываем решения ИИ в Finance, которые созданы на основе Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="ba32a-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="ba32a-132">Конечный пользователь при однократном нажатии кнопки может развернуть решение ИИ и приступить к использованию преимуществ интеллектуальных прогнозов.</span><span class="sxs-lookup"><span data-stu-id="ba32a-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="ba32a-133">Если организацию не устраивает точность прогнозов, опытного пользователь одним щелчком мыши может открыть расширение AI Builder, а затем выбрать или снять выделение с полей, используемых для создания прогнозов.</span><span class="sxs-lookup"><span data-stu-id="ba32a-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="ba32a-134">После готовности они могут обучить и опубликовать изменения, а новая обученная модель будет автоматически отобрана для прогнозирования в Finance.</span><span class="sxs-lookup"><span data-stu-id="ba32a-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="ba32a-135">Как получить аналитику платежей клиентов (предварительное ознакомление)</span><span class="sxs-lookup"><span data-stu-id="ba32a-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="ba32a-136">Если вы хотите попробовать аналитику платежей клиентов (предварительное ознакомление), отправьте по электронной почте сообщение [Аналитика платежей клиентов (предварительная версия)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ba32a-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="ba32a-137">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="ba32a-137">Privacy Notice</span></span>

<span data-ttu-id="ba32a-138">Версии для предварительного ознакомления (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.</span><span class="sxs-lookup"><span data-stu-id="ba32a-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


