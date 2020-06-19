---
title: Модуль значка корзины
description: В этом разделе описывается модуль значка корзины, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 6771a84118504cd5c8e44302380eb970e4658902
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411097"
---
# <a name="cart-icon-module"></a><span data-ttu-id="2c679-103">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="2c679-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2c679-104">В этом разделе описывается модуль значка корзины, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2c679-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2c679-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="2c679-105">Overview</span></span>

<span data-ttu-id="2c679-106">Модуль значка корзины представляет корзину в модуле заголовка страницы и отображает количество номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="2c679-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="2c679-107">В модуле значка корзины также отображается сводка по корзине (также называется мини-корзиной), когда на значок корзины наводится указатель.</span><span class="sxs-lookup"><span data-stu-id="2c679-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="2c679-108">Мини-корзина предоставляет пользователю сводку номенклатур в корзине без перехода на страницу корзины.</span><span class="sxs-lookup"><span data-stu-id="2c679-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="2c679-109">Кроме того, она позволяет пользователю непосредственно перейти на страницу оформления заказа, если его устраивает сводка.</span><span class="sxs-lookup"><span data-stu-id="2c679-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="2c679-110">Это позволяет сократить число переходов между страницами и ускорить оформление.</span><span class="sxs-lookup"><span data-stu-id="2c679-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="2c679-111">На следующем рисунке показан пример модуля значка корзины, в котором отображается мини-корзина в заголовке Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="2c679-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Пример модуля значка корзины](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="2c679-113">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="2c679-113">Module properties</span></span>

- <span data-ttu-id="2c679-114">**Показать мини- корзину** — если задано значение true, это свойство позволяет отображать сводку корзины (мини-корзину), когда указатель наводится на значок корзины.</span><span class="sxs-lookup"><span data-stu-id="2c679-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="2c679-115">Эта функциональная возможность поддерживается только для портов просмотра рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="2c679-115">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="2c679-116">Добавление модуля значка корзины на страницу</span><span class="sxs-lookup"><span data-stu-id="2c679-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="2c679-117">Чтобы добавить модуль значка корзины, см. раздел [Модуль заголовка](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="2c679-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="2c679-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2c679-118">Additional resources</span></span>

[<span data-ttu-id="2c679-119">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="2c679-119">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2c679-120">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="2c679-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2c679-121">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="2c679-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2c679-122">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="2c679-122">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2c679-123">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="2c679-123">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2c679-124">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="2c679-124">Footer module</span></span>](author-footer-module.md)
