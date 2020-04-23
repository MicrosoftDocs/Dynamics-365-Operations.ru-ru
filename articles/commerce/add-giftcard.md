---
title: Модуль подарочного сертификата
description: В этом разделе описываются модули подарочных сертификатов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 70047376cec44523cc9cfe4df792bde23c776d8c
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261587"
---
# <a name="gift-card-module"></a><span data-ttu-id="da140-103">Модуль подарочного сертификата</span><span class="sxs-lookup"><span data-stu-id="da140-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da140-104">В этом разделе описываются модули подарочных сертификатов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="da140-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="da140-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="da140-105">Overview</span></span>

<span data-ttu-id="da140-106">Подарочные сертификаты являются обычной формой платежа, и модуль подарочного сертификата может использоваться в модуле оформления покупки для приема подарочных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="da140-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="da140-107">Модуль подарочного сертификата поддерживает подарочные сертификаты Dynamics 365, SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="da140-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="da140-108">Подарочные сертификаты SVS и Givex погашаются через поставщика платежей Adyen.</span><span class="sxs-lookup"><span data-stu-id="da140-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="da140-109">Дополнительные сведения о поддержке внешних подарочных сертификатов, таких как SVS и Givex, см. в разделе [Поддержка внешних подарочных сертификатов](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="da140-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

## <a name="module-properties"></a><span data-ttu-id="da140-110">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="da140-110">Module properties</span></span>

- <span data-ttu-id="da140-111">**Показывать дополнительные поля** — это свойство определяет, какие поля должны отображаться для подарочных сертификатов в дополнение к номеру подарочного сертификата, который всегда отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="da140-111">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="da140-112">Например, некоторые подарочные сертификаты поддерживают отображение личного идентификационного номера (ПИН-кода), а другие поддерживают отображение ПИН-кода и даты истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="da140-112">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="da140-113">В качестве альтернативы для этого свойства может быть задано значение "Нет", и тогда отображается только номер подарочного сертификата, а никакие дополнительные поля не отображаются.</span><span class="sxs-lookup"><span data-stu-id="da140-113">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="da140-114">Поддерживаемые значения:</span><span class="sxs-lookup"><span data-stu-id="da140-114">Supported values:</span></span>
-   <span data-ttu-id="da140-115">ПИН-код</span><span class="sxs-lookup"><span data-stu-id="da140-115">PIN</span></span>
-   <span data-ttu-id="da140-116">Срок действия</span><span class="sxs-lookup"><span data-stu-id="da140-116">Expiration date</span></span>
-   <span data-ttu-id="da140-117">ПИН-код и срок действия</span><span class="sxs-lookup"><span data-stu-id="da140-117">PIN and expiration date</span></span> 
-   <span data-ttu-id="da140-118">Не допускается</span><span class="sxs-lookup"><span data-stu-id="da140-118">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="da140-119">Параметры сайта для модулей подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="da140-119">Site settings for gift card modules</span></span>

<span data-ttu-id="da140-120">В конфигураторе сайта Commerce в пункте **Параметры сайта \> Расширения** имеется модуль подарочного сертификата с названием **Поддерживаемый тип подарочного сертификата**.</span><span class="sxs-lookup"><span data-stu-id="da140-120">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="da140-121">Эта настройка поддерживает три значения:</span><span class="sxs-lookup"><span data-stu-id="da140-121">This setting supports three values:</span></span>
- <span data-ttu-id="da140-122">**Подарочный сертификат Dynamics 365** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="da140-122">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="da140-123">Эта настройка поддерживается только для пользователей, выполнивших вход на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="da140-123">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="da140-124">**Подарочные сертификаты SVS и Givex** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="da140-124">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="da140-125">Эта настройка поддерживается для пользователей, выполнивших вход, и анонимных пользователей на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="da140-125">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="da140-126">**Подарочные сертификаты Dynamics 365, SVS и Givex** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов Dynamics 365, SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="da140-126">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="da140-127">Эта настройка поддерживается только для пользователей, выполнивших вход на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="da140-127">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="da140-128">Добавление модуля подарочных сертификатов на страницу</span><span class="sxs-lookup"><span data-stu-id="da140-128">Add a gift card module to a page</span></span>

<span data-ttu-id="da140-129">Инструкции по добавлению модуля подарочного сертификата на страницу оформления покупки и заданию требуемых свойств см. в разделе [Модуль оформления заказа](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="da140-129">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da140-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="da140-130">Additional resources</span></span>

[<span data-ttu-id="da140-131">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="da140-131">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="da140-132">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="da140-132">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="da140-133">Поддержка внешних подарочных карт</span><span class="sxs-lookup"><span data-stu-id="da140-133">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
