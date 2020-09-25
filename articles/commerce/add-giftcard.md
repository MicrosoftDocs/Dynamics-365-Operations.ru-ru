---
title: Модуль подарочного сертификата
description: В этом разделе описываются модули подарочных сертификатов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761089"
---
# <a name="gift-card-module"></a><span data-ttu-id="31466-103">Модуль подарочного сертификата</span><span class="sxs-lookup"><span data-stu-id="31466-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="31466-104">В этом разделе описываются модули подарочных сертификатов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="31466-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="31466-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="31466-105">Overview</span></span>

<span data-ttu-id="31466-106">Модули подарочных сертификатов могут использоваться в модуле оформления покупки для приема подарочных сертификатов, которые являются распространенной формой оплаты, используемой в проводках электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="31466-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="31466-107">Модуль подарочного сертификата поддерживает подарочные сертификаты Dynamics 365, SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="31466-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="31466-108">Подарочные сертификаты SVS и Givex погашаются через поставщика платежей Adyen.</span><span class="sxs-lookup"><span data-stu-id="31466-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="31466-109">Дополнительные сведения о поддержке внешних подарочных сертификатов, таких как SVS и Givex, см. в разделе [Поддержка внешних подарочных сертификатов](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="31466-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="31466-110">Доступно два модуля подарочных сертификатов:</span><span class="sxs-lookup"><span data-stu-id="31466-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="31466-111">**Подарочный сертификат** — этот модуль может использоваться на странице оформления покупки для погашения подарочного сертификата в качестве платежного средства.</span><span class="sxs-lookup"><span data-stu-id="31466-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="31466-112">**Проверка сальдо подарочного сертификата** — этот модуль может использоваться на любой странице для проверки сальдо подарочного сертификата.</span><span class="sxs-lookup"><span data-stu-id="31466-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="31466-113">Этот модуль доступен в выпуске Commerce 10.0.14 и выше.</span><span class="sxs-lookup"><span data-stu-id="31466-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="31466-114">На следующем рисунке показан пример модуля подарочного сертификата на странице оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="31466-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![Пример модуля подарочного сертификата](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="31466-116">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="31466-116">Module properties</span></span>

- <span data-ttu-id="31466-117">**Показывать дополнительные поля** — это свойство определяет, какие поля должны отображаться для подарочных сертификатов в дополнение к номеру подарочного сертификата, который всегда отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="31466-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="31466-118">Например, некоторые подарочные сертификаты поддерживают отображение личного идентификационного номера (ПИН-кода), а другие поддерживают отображение ПИН-кода и даты истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="31466-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="31466-119">В качестве альтернативы для этого свойства может быть задано значение "Нет", и тогда отображается только номер подарочного сертификата, а никакие дополнительные поля не отображаются.</span><span class="sxs-lookup"><span data-stu-id="31466-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="31466-120">Поддерживаемые значения:</span><span class="sxs-lookup"><span data-stu-id="31466-120">Supported values:</span></span>
-   <span data-ttu-id="31466-121">ПИН-код</span><span class="sxs-lookup"><span data-stu-id="31466-121">PIN</span></span>
-   <span data-ttu-id="31466-122">Срок действия</span><span class="sxs-lookup"><span data-stu-id="31466-122">Expiration date</span></span>
-   <span data-ttu-id="31466-123">ПИН-код и срок действия</span><span class="sxs-lookup"><span data-stu-id="31466-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="31466-124">Не допускается</span><span class="sxs-lookup"><span data-stu-id="31466-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="31466-125">Параметры сайта для модулей подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="31466-125">Site settings for gift card modules</span></span>

<span data-ttu-id="31466-126">В конфигураторе сайта Commerce в пункте **Параметры сайта \> Расширения** имеется модуль подарочного сертификата с названием **Поддерживаемый тип подарочного сертификата**.</span><span class="sxs-lookup"><span data-stu-id="31466-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="31466-127">Эта настройка поддерживает три значения:</span><span class="sxs-lookup"><span data-stu-id="31466-127">This setting supports three values:</span></span>
- <span data-ttu-id="31466-128">**Подарочный сертификат Dynamics 365** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="31466-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="31466-129">Эта настройка поддерживается только для пользователей, выполнивших вход на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="31466-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="31466-130">**Подарочные сертификаты SVS и Givex** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="31466-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="31466-131">Эта настройка поддерживается для пользователей, выполнивших вход, и анонимных пользователей на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="31466-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="31466-132">**Подарочные сертификаты Dynamics 365, SVS и Givex** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов Dynamics 365, SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="31466-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="31466-133">Эта настройка поддерживается только для пользователей, выполнивших вход на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="31466-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="31466-134">Добавление модуля подарочных сертификатов на страницу</span><span class="sxs-lookup"><span data-stu-id="31466-134">Add a gift card module to a page</span></span>

<span data-ttu-id="31466-135">Инструкции по добавлению модуля подарочного сертификата на страницу оформления покупки и заданию требуемых свойств см. в разделе [Модуль оформления заказа](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="31466-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31466-136">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="31466-136">Additional resources</span></span>

[<span data-ttu-id="31466-137">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="31466-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="31466-138">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="31466-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="31466-139">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="31466-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="31466-140">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="31466-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="31466-141">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="31466-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="31466-142">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="31466-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="31466-143">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="31466-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="31466-144">Поддержка внешних подарочных карт</span><span class="sxs-lookup"><span data-stu-id="31466-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
