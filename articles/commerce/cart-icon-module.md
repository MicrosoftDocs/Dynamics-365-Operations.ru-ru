---
title: Модуль значка корзины
description: В этом разделе описывается модуль значка корзины, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4ab1609d332b96c0588b06aa086dd4fee944e5d9
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055768"
---
# <a name="cart-icon-module"></a><span data-ttu-id="4f45f-103">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="4f45f-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f45f-104">В этом разделе описывается модуль значка корзины, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4f45f-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4f45f-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="4f45f-105">Overview</span></span>

<span data-ttu-id="4f45f-106">Модуль значка корзины представляет корзину в модуле заголовка страницы и отображает количество номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="4f45f-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="4f45f-107">В модуле значка корзины также отображается сводка по корзине (также называется мини-корзиной), когда на значок корзины наводится указатель.</span><span class="sxs-lookup"><span data-stu-id="4f45f-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="4f45f-108">Мини-корзина предоставляет пользователю сводку номенклатур в корзине без перехода на страницу корзины.</span><span class="sxs-lookup"><span data-stu-id="4f45f-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="4f45f-109">Кроме того, она позволяет пользователю непосредственно перейти на страницу оформления заказа, если его устраивает сводка.</span><span class="sxs-lookup"><span data-stu-id="4f45f-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="4f45f-110">Это позволяет сократить число переходов между страницами и ускорить оформление.</span><span class="sxs-lookup"><span data-stu-id="4f45f-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="4f45f-111">Поддержка использования модуля значка корзины в выпуске Dynamics 365 Commerce 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="4f45f-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="4f45f-112">На следующем рисунке показан пример модуля значка корзины, в котором отображается мини-корзина в заголовке Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="4f45f-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Пример модуля значка корзины](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="4f45f-114">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="4f45f-114">Module properties</span></span>

- <span data-ttu-id="4f45f-115">**Показать мини- корзину** — если задано значение true, это свойство позволяет отображать сводку корзины (мини-корзину), когда указатель наводится на значок корзины.</span><span class="sxs-lookup"><span data-stu-id="4f45f-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="4f45f-116">Эта функциональная возможность поддерживается только для портов просмотра рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="4f45f-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="4f45f-117">Добавление модуля значка корзины на страницу</span><span class="sxs-lookup"><span data-stu-id="4f45f-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="4f45f-118">Чтобы добавить модуль значка корзины, см. раздел [Модуль заголовка](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="4f45f-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f45f-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4f45f-119">Additional resources</span></span>

[<span data-ttu-id="4f45f-120">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="4f45f-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4f45f-121">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="4f45f-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4f45f-122">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="4f45f-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="4f45f-123">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="4f45f-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="4f45f-124">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="4f45f-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="4f45f-125">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="4f45f-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4f45f-126">Модуль подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="4f45f-126">Gift card module</span></span>](add-giftcard.md)
