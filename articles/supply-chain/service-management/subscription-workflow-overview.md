---
title: Обзор последовательности подписки
description: В этом разделе представлен обзор последовательности подписки.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5cff6910dcb273fc081443546676426387f6625
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "321647"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="8996f-103">Обзор последовательности подписки</span><span class="sxs-lookup"><span data-stu-id="8996f-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8996f-104">Вы являетесь администратором подписок в электротехнической компании, которая предлагает подписки на обслуживание осветительного оборудования.</span><span class="sxs-lookup"><span data-stu-id="8996f-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="8996f-105">Клиент связывается с компанией для приобретения годовой подписки на обслуживание осветительного оборудования.</span><span class="sxs-lookup"><span data-stu-id="8996f-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="8996f-106">Создание подписок</span><span class="sxs-lookup"><span data-stu-id="8996f-106">Setting up subscriptions</span></span>

<span data-ttu-id="8996f-107">Для настройки подписки, следует сначала создать группу подписки для нового соглашения на обслуживание или убедиться, что группа подписки существует.</span><span class="sxs-lookup"><span data-stu-id="8996f-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="8996f-108">Если группа подписки существует, необходимо настроить ежегодное выставление счета клиенту и начисления выручки с продаж каждый месяц года.</span><span class="sxs-lookup"><span data-stu-id="8996f-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="8996f-109">Дополнительные сведения о настройке подписок см. в форме [Настройка групп подписки](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="8996f-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="8996f-110">После создания группы подписки можно создать саму подписку.</span><span class="sxs-lookup"><span data-stu-id="8996f-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="8996f-111">Дополнительные сведения о создании подписок на сервисное обслуживание см. в разделе [Создание подписок на обслуживание из группы подписки](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="8996f-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="8996f-112">Создание и изменение проводок по подписке</span><span class="sxs-lookup"><span data-stu-id="8996f-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="8996f-113">После настройки подписки, создается проводка по сборам по подписке для первого периода обработки накладной, который один год.</span><span class="sxs-lookup"><span data-stu-id="8996f-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="8996f-114">Проводки типа **Обычный**.</span><span class="sxs-lookup"><span data-stu-id="8996f-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="8996f-115">Таким образом, можно создать только проводки по подписке, где даты начала и окончания соответствуют периодам, ранее созданным в форме **Типы периодов**.</span><span class="sxs-lookup"><span data-stu-id="8996f-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="8996f-116">Дополнительные сведения о проводкам по сборам см. в разделе [Создание проводок по сборам по подписке](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="8996f-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="8996f-117">После настройки подписки для клиента, вас вспоминаете, что существует договоренность о скидке 10 процентов, по всем прайс-листам предложений на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="8996f-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="8996f-118">Поэтому необходимо уменьшить цену проводки по сборам, которая была создана.</span><span class="sxs-lookup"><span data-stu-id="8996f-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="8996f-119">Далее в тот же день, вам звонит контактное лицо клиента и уведомляет, что все равно, хотя они хотят соглашение на обслуживание осветительного оборудования они планируют в течение года установить новое осветительное оборудование.</span><span class="sxs-lookup"><span data-stu-id="8996f-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="8996f-120">Обслуживание потребуется только до октября 2013 г.</span><span class="sxs-lookup"><span data-stu-id="8996f-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="8996f-121">Для уменьшения числа месяцев подписки для клиента создается новая проводка по сборам по подписке типа **Дни сокращения**.</span><span class="sxs-lookup"><span data-stu-id="8996f-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="8996f-122">Дополнительные сведения об уменьшении дней см. в разделе [Уменьшение дней в сборах по подписке](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="8996f-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="8996f-123">Выставление накладной и начисление проводок по подписке</span><span class="sxs-lookup"><span data-stu-id="8996f-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="8996f-124">Теперь вы завершили настройки подписке, и вы готовы выставить его клиенту.</span><span class="sxs-lookup"><span data-stu-id="8996f-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="8996f-125">Дополнительные сведения о выставлении накладных по подпискам см. в разделе [Обработка накладных для проводок по подписке](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="8996f-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="8996f-126">Дня спустя ваш клиент звонит и уведомляет, что накладная должна быть выставлена в долларах США, не евро.</span><span class="sxs-lookup"><span data-stu-id="8996f-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="8996f-127">Поэтому вы создаете кредит-ноту, и можно также создавать новую проводку по подписке в нужной валюте.</span><span class="sxs-lookup"><span data-stu-id="8996f-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="8996f-128">Дополнительные сведения о кредитовании проводок по подписке см. в разделе [Кредитование проводок по подписке](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="8996f-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="8996f-129">В конце каждого месяца, выручка за один месяц может быть начислена из подписки клиента на счет прибылей и убытков и на счета НЗП.</span><span class="sxs-lookup"><span data-stu-id="8996f-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="8996f-130">Дополнительные сведения о настройке начисления выручки по подпискам см. в разделе [Начисление выручки по подписке](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="8996f-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  


