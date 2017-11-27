---
title: "Отгрузка заказа из другого магазина"
description: "В этом разделе описывается функция отправки накладных расходов."
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail Version
ms.translationtype: HT
ms.sourcegitcommit: 986ec7835dac52c326085c47313205d08b1bafa8
ms.openlocfilehash: d217bc31ad9d93c5440e5329f7b7327d089137f4
ms.contentlocale: ru-ru
ms.lasthandoff: 10/10/2017

---

# <a name="ship-an-order-from-a-different-store"></a><span data-ttu-id="c0c28-103">Отгрузка заказа из другого магазина</span><span class="sxs-lookup"><span data-stu-id="c0c28-103">Ship an order from a different store</span></span>

<span data-ttu-id="c0c28-104">С помощью функции отправки накладных расходов в Dynamics 365 for Retail заказы клиента могут быть размещены в одном магазине и отгружены из другого магазина.</span><span class="sxs-lookup"><span data-stu-id="c0c28-104">With the Charge send feature in Dynamics 365 for Retail, customer orders can be placed in one store and shipped from another store.</span></span> <span data-ttu-id="c0c28-105">Заказы клиента в клиенте POS-терминала поддерживают несколько вариантов исполнения.</span><span class="sxs-lookup"><span data-stu-id="c0c28-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="c0c28-106">Некоторые примеры вариантов выполнения приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="c0c28-106">Some examples of fulfillment options include:</span></span>
-   <span data-ttu-id="c0c28-107">Получение в том же магазине в другой день.</span><span class="sxs-lookup"><span data-stu-id="c0c28-107">Pick up from the same store on a different date.</span></span>
-   <span data-ttu-id="c0c28-108">Получение в другом магазине в этот же или в другой день.</span><span class="sxs-lookup"><span data-stu-id="c0c28-108">Pick up from a different store on the same date or a different date.</span></span>
-   <span data-ttu-id="c0c28-109">Отгрузка со склада отгрузки по умолчанию, который назначен магазину, и доставка в определенную дату.</span><span class="sxs-lookup"><span data-stu-id="c0c28-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="c0c28-110">Функция отправки накладных расходов использует следующие операции POS-терминала: "Отгрузить все продукты" и "Отгрузить выбранные продукты".</span><span class="sxs-lookup"><span data-stu-id="c0c28-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="c0c28-111">Это позволяет служащему магазина выбрать "место отгрузки", из которого может быть выполнен заказ или строка заказа.</span><span class="sxs-lookup"><span data-stu-id="c0c28-111">This allows the store clerk to select the “ship from” location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="c0c28-112">По умолчанию "место отгрузки" — это склад отгрузки, который связан с магазином.</span><span class="sxs-lookup"><span data-stu-id="c0c28-112">By default, the “ship from” location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="c0c28-113">Однако служащий магазина может изменить этот склад и выбрать любой магазин, который определен в группе локатора магазина, которая назначена магазину.</span><span class="sxs-lookup"><span data-stu-id="c0c28-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span> 

<span data-ttu-id="c0c28-114">Возможность выбора адреса "доставки" остается неизменной.</span><span class="sxs-lookup"><span data-stu-id="c0c28-114">The ability to select “ship to” addresses remains unchanged.</span></span> 

<span data-ttu-id="c0c28-115">Методы доставки, которые можно использовать для выполнения строки заказа, основаны на конфигурации допустимых способов доставки продуктов и адресов.</span><span class="sxs-lookup"><span data-stu-id="c0c28-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="c0c28-116">Поскольку правила в отношении допустимых способов доставки поддерживаются только в центральном офисе розничной сети (HQ), клиент POS-терминала выполняет вызов в режиме реального времени для выборки допустимых способов доставки для строки отгрузки.</span><span class="sxs-lookup"><span data-stu-id="c0c28-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span> 


