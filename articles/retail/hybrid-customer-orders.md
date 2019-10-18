---
title: Гибридные клиентские заказы
description: Гибридный клиентский заказ представляет собой один заказ, содержащий продукты, которые клиент может унести с собой из магазина, а также продукты, которые он заберет или которые будут доставлены позже.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 92be01210b677228f4c096ffef09d7109ba2b332
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023401"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="0ce8a-103">Гибридные клиентские заказы</span><span class="sxs-lookup"><span data-stu-id="0ce8a-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0ce8a-104">Гибридный клиентский заказ представляет собой один заказ, содержащий продукты, которые клиент может унести с собой из магазина, а также продукты, которые он заберет или которые будут доставлены позже.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="0ce8a-105">В Retail для заказа клиента можно выбрать, что клиент заберет все продукты или заберет выбранные продукты.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-105">In Retail, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="0ce8a-106">Для строк продуктов, помеченных как "на вынос", автоматически выставляется накладная после создания заказа, аналогично тому, как для заказа, который клиент заберет после создания заказа.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="0ce8a-107">Суммы, подлежащая оплате по гибридным заказам, определяется путем добавления процента депозита по строкам комплектации и отгрузки товаров к полной сумме строка "на вынос".</span><span class="sxs-lookup"><span data-stu-id="0ce8a-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="0ce8a-108">Для гибридных заказов система переключается между режимом заказа клиента и режимом "оплатил наличными и забрал" следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0ce8a-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="0ce8a-109">Если все товары в корзине заданы как установлены как **Способ поставки "На вынос"**, заказ будет обрабатываться как проводка "Продажа без доставки при оплате наличными".</span><span class="sxs-lookup"><span data-stu-id="0ce8a-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="0ce8a-110">Если для какой-либо строки или всех строк в корзине задана **Комплектация** или **Доставка**, заказ будет обрабатываться как проводка заказа клиента.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="0ce8a-111">Если строка корзины выбрана и выбрано значение **Отобрать выбранное**, **Отгрузить выбранные** или **Вынести выбранные**, этот метод доставки будет установлен только для конкретной строки корзины.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="0ce8a-112">В этом случае дальнейший поток операций продолжается в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="0ce8a-113">Однако если значение **Отобрать выбранное**, **Отгрузить выбранные** или **Вынести выбранные** выбрано, когда никакая строка корзины не выбрана, открывается новая страница, на которой отображаются все строки корзины.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="0ce8a-114">На этом окне можно выбрать несколько строк за один раз, чтобы задать способ доставки.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="0ce8a-115">При использовании этого метода для выбора строк будут переопределены все предыдущие методы доставки, назначенные данной строке.</span><span class="sxs-lookup"><span data-stu-id="0ce8a-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ce8a-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0ce8a-116">Additional resources</span></span>

[<span data-ttu-id="0ce8a-117">Обзор клиентских заказов</span><span class="sxs-lookup"><span data-stu-id="0ce8a-117">Customer orders overview</span></span>](customer-orders-overview.md)
