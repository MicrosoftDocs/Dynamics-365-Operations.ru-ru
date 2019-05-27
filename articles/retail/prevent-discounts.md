---
title: Параметры для запрета скидок для розничных продуктов
description: Существует несколько причин, по которым предприятиям розничной торговли может потребоваться запретить скидки на некоторые продукты либо в ходе рекламной акции, либо при продаже на POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c9d3e7af95dffddfddc34059d93a2a5a350d08e5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550752"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="74115-103">Параметры для запрета скидок для розничных продуктов</span><span class="sxs-lookup"><span data-stu-id="74115-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="74115-104">Существует несколько причин, по которым предприятиям розничной торговли может потребоваться запретить скидки на некоторые продукты либо в ходе рекламной акции, либо при продаже на POS.</span><span class="sxs-lookup"><span data-stu-id="74115-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="74115-105">Следующие параметры, которые находятся на вкладке **Розница** выпущенных продуктов, позволяют настроить продукта так, чтобы запретить все или предоставляемые вручную скидки.</span><span class="sxs-lookup"><span data-stu-id="74115-105">The following options, which can be found on the **Retail** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="74115-106">Эти параметры можно задать на уровне категории в иерархии категорий розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="74115-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

- <span data-ttu-id="74115-107">**Запретить все скидки** — выберите этот вариант, чтобы запретить применение к этому продукту всех типов скидок.</span><span class="sxs-lookup"><span data-stu-id="74115-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="74115-108">Это включает такие рекламные акции, как скидки при покупке комплекта, скидки при покупке определенного количества и скидки по пороговому значению, а также предоставляемые вручную скидки по строкам и транзакциям, применяемые при продаже пользователем POS.</span><span class="sxs-lookup"><span data-stu-id="74115-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="74115-109">**Запретить заданные вручную скидки** — выберите этот вариант, чтобы запретить применение к этому продукту предоставляемых вручную скидок по строкам и транзакциям, применяемых при продаже пользователем POS.</span><span class="sxs-lookup"><span data-stu-id="74115-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="74115-110">Продукты, для которых выбран этот вариант, по-прежнему могут участвовать в рекламных акциях, таких как скидки при покупке комплекта, скидки при покупке определенного количества и скидки по пороговому значению.</span><span class="sxs-lookup"><span data-stu-id="74115-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="74115-111">Эти параметры не ограничивают доступ к операции переопределения цены, поскольку при этом задается базисная цена, что не рассматривается как скидка.</span><span class="sxs-lookup"><span data-stu-id="74115-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="74115-112">[![поле для запрета скидок](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="74115-112">[![prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>
