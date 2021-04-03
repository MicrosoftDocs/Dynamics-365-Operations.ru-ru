---
title: Параметр "Забрать это" не отображается на страницах "Корзина" или "сведения о продукте"
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том, что параметр для самовывоза из магазина не появился на странице корзины или на страницах сведений о продукте.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c78dee7289931cecd0f2d7c09caf7881eb8cfd23
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585498"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="56d12-103">Параметр "Забрать это" не отображается на страницах "Корзина" или "сведения о продукте"</span><span class="sxs-lookup"><span data-stu-id="56d12-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56d12-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том, что параметр для самовывоза из магазина не появился на странице корзины или на страницах сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="56d12-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="56d12-105">описание</span><span class="sxs-lookup"><span data-stu-id="56d12-105">Description</span></span>

<span data-ttu-id="56d12-106">Кнопка **Забрать это** не отображается на страницах "Корзина" или "сведения о продукте".</span><span class="sxs-lookup"><span data-stu-id="56d12-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="56d12-107">На следующем рисунке показан пример страницы, которая включает кнопку **Забрать это**.</span><span class="sxs-lookup"><span data-stu-id="56d12-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Кнопка "Забрать это"](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="56d12-109">Приказ</span><span class="sxs-lookup"><span data-stu-id="56d12-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="56d12-110">Включение расширения BOPIS в конструкторе сайтов Commerce</span><span class="sxs-lookup"><span data-stu-id="56d12-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="56d12-111">Чтобы включить функцию "купить в Интернете, забрать в магазине" (BOPIS) в конструкторе сайтов Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="56d12-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="56d12-112">Выберите ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="56d12-112">Select your site.</span></span>
1. <span data-ttu-id="56d12-113">Выберите **Параметры сайта**, затем выберите **Расширения**.</span><span class="sxs-lookup"><span data-stu-id="56d12-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="56d12-114">Убедитесь, что флажок **Отключить BOPIS** снят.</span><span class="sxs-lookup"><span data-stu-id="56d12-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="56d12-115">Настройка способов доставки в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="56d12-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="56d12-116">Чтобы настроить способы доставки в Commerce Headquarters, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="56d12-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="56d12-117">Переход к **Закупки и источники \> Настройка \> Способы доставки**.</span><span class="sxs-lookup"><span data-stu-id="56d12-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="56d12-118">Убедитесь, что был создан режим доставки **Самовывоз клиентом**, и что продукты и адреса назначены ему.</span><span class="sxs-lookup"><span data-stu-id="56d12-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="56d12-119">Перейдите в раздел **Retail и Commerce \> Настройка Headquarters \> Параметры**.</span><span class="sxs-lookup"><span data-stu-id="56d12-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="56d12-120">В левой области переходов выберите **Клиентские заказы**.</span><span class="sxs-lookup"><span data-stu-id="56d12-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="56d12-121">Убедитесь, что **Способ доставки для самовывоза** настроен правильно.</span><span class="sxs-lookup"><span data-stu-id="56d12-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="56d12-122">Настройка платежей по заказам клиентов</span><span class="sxs-lookup"><span data-stu-id="56d12-122">Configure customer orders payments</span></span>

<span data-ttu-id="56d12-123">Чтобы настроить платежи по заказам клиентов в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="56d12-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="56d12-124">Перейдите в раздел **Retail и Commerce \> Настройка Headquarters \> Параметры**.</span><span class="sxs-lookup"><span data-stu-id="56d12-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="56d12-125">В левой области переходов выберите **Клиентские заказы**.</span><span class="sxs-lookup"><span data-stu-id="56d12-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="56d12-126">На экспресс-вкладке **Платежи** убедитесь, что **условия оплаты** и **Способ оплаты** настроены правильно.</span><span class="sxs-lookup"><span data-stu-id="56d12-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56d12-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="56d12-127">Additional resources</span></span>

[<span data-ttu-id="56d12-128">Настройка BOPIS</span><span class="sxs-lookup"><span data-stu-id="56d12-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="56d12-129">Включение нескольких режимов доставки самовывозом для заказов клиентов</span><span class="sxs-lookup"><span data-stu-id="56d12-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="56d12-130">Платежи по заказам Commerce многоканального взаимодействия</span><span class="sxs-lookup"><span data-stu-id="56d12-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="56d12-131">Модуль выбора магазина</span><span class="sxs-lookup"><span data-stu-id="56d12-131">Store selector module</span></span>](../store-selector.md)
