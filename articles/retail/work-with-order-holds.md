---
title: "Удержания заказов"
description: "В этой статье поясняется, как блокировать заказы при использовании Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8b4c8ecbef1dc667d3b60411a53f0c63686529c2
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="order-holds"></a><span data-ttu-id="44501-103">Удержания заказов</span><span class="sxs-lookup"><span data-stu-id="44501-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="44501-104">В этой статье поясняется, как блокировать заказы при использовании Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="44501-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="44501-105">Заказ может быть заблокирован (поставлен на удержание) по разным причинам.</span><span class="sxs-lookup"><span data-stu-id="44501-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="44501-106">Например, заказ можно заблокировать, пока не будет проверен адрес или способ оплаты клиента, или пока менеджер не проверит кредитный лимит клиента.</span><span class="sxs-lookup"><span data-stu-id="44501-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="44501-107">Во время процесса продажи могут возникнуть ситуации, когда заказ на продажу необходимо заблокировать.</span><span class="sxs-lookup"><span data-stu-id="44501-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="44501-108">Например, заказ на продажу может быть заблокирован из-за проблем с платежом клиента, при подозрении на мошенничество или пока менеджер проверит заказ.</span><span class="sxs-lookup"><span data-stu-id="44501-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="44501-109">При блокировке заказа на продажу ему назначается код удержания заказа для определения причины блокировки.</span><span class="sxs-lookup"><span data-stu-id="44501-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="44501-110">Чтобы настроить коды удержания заказа на продажу, выберите **Продажи и маркетинг** &gt; **Настройка** &gt; **Заказы на продажу** &gt; **Коды удержания заказов**.</span><span class="sxs-lookup"><span data-stu-id="44501-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="44501-111">Заказ на продажу можно заблокировать вручную во время создания заказа или позже.</span><span class="sxs-lookup"><span data-stu-id="44501-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="44501-112">Кроме того, заказ может быть заблокирован автоматически, в соответствии с правилами проверки на мошенничество.</span><span class="sxs-lookup"><span data-stu-id="44501-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="44501-113">Пока заказ на продажу заблокирован, вам может понадобится обновить его, добавив дополнительную информацию.</span><span class="sxs-lookup"><span data-stu-id="44501-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="44501-114">Другой вариант — вам может понадобиться извлечь заказ на продажу, чтобы продолжить работу над ним.</span><span class="sxs-lookup"><span data-stu-id="44501-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="44501-115">Вы можете извлечь заказ на продажу, вернуть его обратно и даже перекрыть извлечение заказа другим пользователем с помощью рабочего места блокировки заказов (**Розничная торговля** &gt; **Клиенты** &gt; **Удержания заказов**).</span><span class="sxs-lookup"><span data-stu-id="44501-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="44501-116">Когда заказ готов для завершения, необходимо снять блокировку перед завершением процесса заказа.</span><span class="sxs-lookup"><span data-stu-id="44501-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




