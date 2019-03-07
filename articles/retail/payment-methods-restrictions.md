---
title: Ограничение способов оплаты для возвратов без чека
description: В этой теме описывается, как определенные типы платежа могут быть ограничены для возмещения, если возврат производится без чека.
author: rapraj
manager: AnnBe
ms.date: 01/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 1f84a6382453c0ba7540e618ad90ae1d3c684a2b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "315920"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="3ff04-103">Ограничение способов оплаты для возвратов без чека</span><span class="sxs-lookup"><span data-stu-id="3ff04-103">Restrict payment methods for returns without a receipt</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3ff04-104">Каждый тип платежа, принимаемый розничным магазином, нужно настроить в процессе настройки системы.</span><span class="sxs-lookup"><span data-stu-id="3ff04-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="3ff04-105">В этой теме описывается, как определенные типы платежа могут быть ограничены для возмещения, если возврат производится без чека.</span><span class="sxs-lookup"><span data-stu-id="3ff04-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="3ff04-106">Настройка способов оплаты</span><span class="sxs-lookup"><span data-stu-id="3ff04-106">Set up payment methods</span></span>

<span data-ttu-id="3ff04-107">Для настройки способов оплаты следует выполнить следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="3ff04-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="3ff04-108">Создайте способы оплаты, принимаемые целой организацией.</span><span class="sxs-lookup"><span data-stu-id="3ff04-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="3ff04-109">Создайте типы и номера карт на уровне организации.</span><span class="sxs-lookup"><span data-stu-id="3ff04-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="3ff04-110">Если кредитные карты или дебетовые карты принимаются, необходимо создать один способ оплаты картами, а затем создать типы и номера карт на уровне организации.</span><span class="sxs-lookup"><span data-stu-id="3ff04-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="3ff04-111">Настройте способы оплаты для магазина.</span><span class="sxs-lookup"><span data-stu-id="3ff04-111">Set up store payment methods.</span></span> <span data-ttu-id="3ff04-112">Свяжите способы оплаты с каждым магазином, а затем введите параметры для каждого способа оплаты, характерные для конкретного магазина.</span><span class="sxs-lookup"><span data-stu-id="3ff04-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="3ff04-113">Настройте способы платежа картами для магазинов.</span><span class="sxs-lookup"><span data-stu-id="3ff04-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="3ff04-114">Завершите настройку карты для любого карточного способа оплаты, используемого в магазине.</span><span class="sxs-lookup"><span data-stu-id="3ff04-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="3ff04-115">![Настройка розничного магазина](media/NoReceiptReturns1.png "Настройка розничного магазина")</span><span class="sxs-lookup"><span data-stu-id="3ff04-115">![Retail Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="3ff04-116">Ограничение способов оплаты для возвратов без чека</span><span class="sxs-lookup"><span data-stu-id="3ff04-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="3ff04-117">Для каждого способа оплаты в магазине на странице **Руководство розничного магазина** в области странице в области **Возвраты без чека** задайте для параметра **Ограничить возврат денежных средств для возвратов без чека** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="3ff04-117">For each store payment method, on the **Retail store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="3ff04-118">По умолчанию значение переключателя равно **Нет**, что гарантирует допустимость метод платежа для возмещения.</span><span class="sxs-lookup"><span data-stu-id="3ff04-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="3ff04-119">Если для параметра **Ограничить возврат денежных средств без чека** установлено значение **Да**, выбранный способ платежа не будет разрешен для возврата денежных средств.</span><span class="sxs-lookup"><span data-stu-id="3ff04-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="3ff04-120">![Способ оплаты для розничного магазина](media/NoReceiptReturns3.png "Способ оплаты для розничного магазина")</span><span class="sxs-lookup"><span data-stu-id="3ff04-120">![Retail Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="3ff04-121">Когда кассир выбирает способ оплаты, который ограничен для возврата денежных средств без чека, отображается сообщение для проверки приемлемых методов оплаты.</span><span class="sxs-lookup"><span data-stu-id="3ff04-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="3ff04-122">![Допустимые способы платежа](media/NoReceiptReturns4.png "Допустимые способы платежа")</span><span class="sxs-lookup"><span data-stu-id="3ff04-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="3ff04-123">Если в проводке имеется как возврат с чеком, так и возврат без чека, условия ограничения не накладываются, поскольку проводка будет workflow-процессом возврата с чеком.</span><span class="sxs-lookup"><span data-stu-id="3ff04-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

