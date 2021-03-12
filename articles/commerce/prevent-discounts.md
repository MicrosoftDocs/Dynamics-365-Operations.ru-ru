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
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7c408068ece94d47c0f41e286a2ce0ae7efd23dd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972510"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="5fdc5-103">Параметры для запрета скидок для розничных продуктов</span><span class="sxs-lookup"><span data-stu-id="5fdc5-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5fdc5-104">Существует несколько причин, по которым предприятиям розничной торговли может потребоваться запретить скидки на некоторые продукты либо в ходе рекламной акции, либо при продаже на POS.</span><span class="sxs-lookup"><span data-stu-id="5fdc5-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="5fdc5-105">Следующие параметры, которые находятся на вкладке **Commerce** выпущенных продуктов, позволяют настроить продукта так, чтобы запретить все или предоставляемые вручную скидки.</span><span class="sxs-lookup"><span data-stu-id="5fdc5-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="5fdc5-106">Эти параметры можно задать на уровне категории в иерархии категорий.</span><span class="sxs-lookup"><span data-stu-id="5fdc5-106">The settings can also be specified at the category level from the category hierarchy.</span></span>

- <span data-ttu-id="5fdc5-107">**Запретить все скидки** — выберите этот вариант, чтобы запретить применение к этому продукту всех типов скидок.</span><span class="sxs-lookup"><span data-stu-id="5fdc5-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="5fdc5-108">Это включает такие рекламные акции, как скидки при покупке комплекта, скидки при покупке определенного количества и скидки по пороговому значению, а также предоставляемые вручную скидки по строкам и транзакциям, применяемые при продаже пользователем POS.</span><span class="sxs-lookup"><span data-stu-id="5fdc5-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="5fdc5-109">**Запретить заданные вручную скидки** — выберите этот вариант, чтобы запретить применение к этому продукту предоставляемых вручную скидок по строкам и транзакциям, применяемых при продаже пользователем POS.</span><span class="sxs-lookup"><span data-stu-id="5fdc5-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="5fdc5-110">Продукты, для которых выбран этот вариант, по-прежнему могут участвовать в рекламных акциях, таких как скидки при покупке комплекта, скидки при покупке определенного количества и скидки по пороговому значению.</span><span class="sxs-lookup"><span data-stu-id="5fdc5-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="5fdc5-111">Эти параметры не ограничивают доступ к операции переопределения цены, поскольку при этом задается базисная цена, что не рассматривается как скидка.</span><span class="sxs-lookup"><span data-stu-id="5fdc5-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="5fdc5-112">[![Поле для запрета скидок](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="5fdc5-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>
