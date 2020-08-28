---
title: Модуль подарочного сертификата
description: В этом разделе описываются модули подарочных сертификатов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661250"
---
# <a name="gift-card-module"></a><span data-ttu-id="fe412-103">Модуль подарочного сертификата</span><span class="sxs-lookup"><span data-stu-id="fe412-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fe412-104">В этом разделе описываются модули подарочных сертификатов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe412-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fe412-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="fe412-105">Overview</span></span>

<span data-ttu-id="fe412-106">Подарочные сертификаты являются обычной формой платежа, и модуль подарочного сертификата может использоваться в модуле оформления покупки для приема подарочных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="fe412-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="fe412-107">Модуль подарочного сертификата поддерживает подарочные сертификаты Dynamics 365, SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="fe412-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="fe412-108">Подарочные сертификаты SVS и Givex погашаются через поставщика платежей Adyen.</span><span class="sxs-lookup"><span data-stu-id="fe412-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="fe412-109">Дополнительные сведения о поддержке внешних подарочных сертификатов, таких как SVS и Givex, см. в разделе [Поддержка внешних подарочных сертификатов](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="fe412-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="fe412-110">На следующем рисунке показан пример модуля подарочного сертификата на странице оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="fe412-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![Пример модуля подарочного сертификата](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="fe412-112">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="fe412-112">Module properties</span></span>

- <span data-ttu-id="fe412-113">**Показывать дополнительные поля** — это свойство определяет, какие поля должны отображаться для подарочных сертификатов в дополнение к номеру подарочного сертификата, который всегда отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fe412-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="fe412-114">Например, некоторые подарочные сертификаты поддерживают отображение личного идентификационного номера (ПИН-кода), а другие поддерживают отображение ПИН-кода и даты истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="fe412-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="fe412-115">В качестве альтернативы для этого свойства может быть задано значение "Нет", и тогда отображается только номер подарочного сертификата, а никакие дополнительные поля не отображаются.</span><span class="sxs-lookup"><span data-stu-id="fe412-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="fe412-116">Поддерживаемые значения:</span><span class="sxs-lookup"><span data-stu-id="fe412-116">Supported values:</span></span>
-   <span data-ttu-id="fe412-117">ПИН-код</span><span class="sxs-lookup"><span data-stu-id="fe412-117">PIN</span></span>
-   <span data-ttu-id="fe412-118">Срок действия</span><span class="sxs-lookup"><span data-stu-id="fe412-118">Expiration date</span></span>
-   <span data-ttu-id="fe412-119">ПИН-код и срок действия</span><span class="sxs-lookup"><span data-stu-id="fe412-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="fe412-120">Не допускается</span><span class="sxs-lookup"><span data-stu-id="fe412-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="fe412-121">Параметры сайта для модулей подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="fe412-121">Site settings for gift card modules</span></span>

<span data-ttu-id="fe412-122">В конфигураторе сайта Commerce в пункте **Параметры сайта \> Расширения** имеется модуль подарочного сертификата с названием **Поддерживаемый тип подарочного сертификата**.</span><span class="sxs-lookup"><span data-stu-id="fe412-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="fe412-123">Эта настройка поддерживает три значения:</span><span class="sxs-lookup"><span data-stu-id="fe412-123">This setting supports three values:</span></span>
- <span data-ttu-id="fe412-124">**Подарочный сертификат Dynamics 365** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fe412-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="fe412-125">Эта настройка поддерживается только для пользователей, выполнивших вход на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="fe412-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="fe412-126">**Подарочные сертификаты SVS и Givex** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="fe412-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="fe412-127">Эта настройка поддерживается для пользователей, выполнивших вход, и анонимных пользователей на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="fe412-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="fe412-128">**Подарочные сертификаты Dynamics 365, SVS и Givex** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов Dynamics 365, SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="fe412-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="fe412-129">Эта настройка поддерживается только для пользователей, выполнивших вход на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="fe412-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="fe412-130">Добавление модуля подарочных сертификатов на страницу</span><span class="sxs-lookup"><span data-stu-id="fe412-130">Add a gift card module to a page</span></span>

<span data-ttu-id="fe412-131">Инструкции по добавлению модуля подарочного сертификата на страницу оформления покупки и заданию требуемых свойств см. в разделе [Модуль оформления заказа](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="fe412-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe412-132">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fe412-132">Additional resources</span></span>

[<span data-ttu-id="fe412-133">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="fe412-133">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fe412-134">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="fe412-134">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="fe412-135">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="fe412-135">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fe412-136">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="fe412-136">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="fe412-137">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="fe412-137">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="fe412-138">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="fe412-138">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="fe412-139">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="fe412-139">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fe412-140">Поддержка внешних подарочных карт</span><span class="sxs-lookup"><span data-stu-id="fe412-140">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
