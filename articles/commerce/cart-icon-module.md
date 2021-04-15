---
title: Модуль значка корзины
description: В этом разделе описывается модуль значка корзины, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793089"
---
# <a name="cart-icon-module"></a><span data-ttu-id="94b7d-103">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="94b7d-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94b7d-104">В этом разделе описывается модуль значка корзины, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="94b7d-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="94b7d-105">Модуль значка корзины представляет корзину в модуле заголовка страницы и отображает количество номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="94b7d-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="94b7d-106">В модуле значка корзины также отображается сводка по корзине (также называется мини-корзиной), когда на значок корзины наводится указатель.</span><span class="sxs-lookup"><span data-stu-id="94b7d-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="94b7d-107">Мини-корзина предоставляет пользователю сводку номенклатур в корзине без перехода на страницу корзины.</span><span class="sxs-lookup"><span data-stu-id="94b7d-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="94b7d-108">Кроме того, она позволяет пользователю непосредственно перейти на страницу оформления заказа, если его устраивает сводка.</span><span class="sxs-lookup"><span data-stu-id="94b7d-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="94b7d-109">Это позволяет сократить число переходов между страницами и ускорить оформление.</span><span class="sxs-lookup"><span data-stu-id="94b7d-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="94b7d-110">Поддержка использования модуля значка корзины в выпуске Dynamics 365 Commerce 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="94b7d-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="94b7d-111">На следующем рисунке показан пример модуля значка корзины, в котором отображается мини-корзина в заголовке Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="94b7d-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Пример модуля значка корзины](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="94b7d-113">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="94b7d-113">Module properties</span></span>

- <span data-ttu-id="94b7d-114">**Показать мини- корзину** — если задано значение true, это свойство позволяет отображать сводку корзины (мини-корзину), когда указатель наводится на значок корзины.</span><span class="sxs-lookup"><span data-stu-id="94b7d-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="94b7d-115">Эта функциональная возможность поддерживается только для портов просмотра рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="94b7d-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="94b7d-116">Добавление модуля значка корзины на страницу</span><span class="sxs-lookup"><span data-stu-id="94b7d-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="94b7d-117">Чтобы добавить модуль значка корзины, см. раздел [Модуль заголовка](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="94b7d-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94b7d-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="94b7d-118">Additional resources</span></span>

[<span data-ttu-id="94b7d-119">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="94b7d-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="94b7d-120">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="94b7d-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="94b7d-121">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="94b7d-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="94b7d-122">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="94b7d-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="94b7d-123">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="94b7d-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="94b7d-124">Модуль сведений о самовывозе</span><span class="sxs-lookup"><span data-stu-id="94b7d-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="94b7d-125">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="94b7d-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="94b7d-126">Модуль подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="94b7d-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]