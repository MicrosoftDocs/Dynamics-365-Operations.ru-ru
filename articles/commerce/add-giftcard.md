---
title: Модуль подарочного сертификата
description: В этом разделе описываются модули подарочных сертификатов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: b7d28e041b8adc828a2447ab09a0c1d28cc2aec0
ms.sourcegitcommit: 69075e001d1fb4ef69282667052cd8d082273094
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022013"
---
# <a name="gift-card-module"></a><span data-ttu-id="8ed6c-103">Модуль подарочного сертификата</span><span class="sxs-lookup"><span data-stu-id="8ed6c-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ed6c-104">В этом разделе описываются модули подарочных сертификатов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8ed6c-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="8ed6c-105">Overview</span></span>

<span data-ttu-id="8ed6c-106">Модули подарочных сертификатов могут использоваться в модуле оформления покупки для приема подарочных сертификатов, которые являются распространенной формой оплаты, используемой в проводках электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="8ed6c-107">Модуль подарочного сертификата поддерживает подарочные сертификаты Dynamics 365, SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="8ed6c-108">Подарочные сертификаты SVS и Givex погашаются через поставщика платежей Adyen.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="8ed6c-109">Дополнительные сведения о поддержке внешних подарочных сертификатов, таких как SVS и Givex, см. в разделе [Поддержка внешних подарочных сертификатов](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="8ed6c-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="8ed6c-110">Поддержка погашения подарочных сертификатов SVS и Givex во время потока оформления покупки доступен в выпуске Dynamics 365 Commerce 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="8ed6c-111">Доступно два модуля подарочных сертификатов:</span><span class="sxs-lookup"><span data-stu-id="8ed6c-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="8ed6c-112">**Подарочный сертификат** — этот модуль может использоваться на странице оформления покупки для погашения подарочного сертификата в качестве платежного средства.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="8ed6c-113">**Проверка сальдо подарочного сертификата** — этот модуль может использоваться на любой странице для проверки сальдо подарочного сертификата.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="8ed6c-114">Этот модуль доступен в выпуске Commerce 10.0.14 и выше.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="8ed6c-115">Поддержка модуля проверки сальдо подарочного сертификата доступна в выпуске Dynamics 365 Commerce 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="8ed6c-116">На следующем рисунке показан пример модуля подарочного сертификата на странице оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![Пример модуля подарочного сертификата](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="8ed6c-118">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="8ed6c-118">Module properties</span></span>

- <span data-ttu-id="8ed6c-119">**Показывать дополнительные поля** — это свойство определяет, какие поля должны отображаться для подарочных сертификатов в дополнение к номеру подарочного сертификата, который всегда отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="8ed6c-120">Например, некоторые подарочные сертификаты поддерживают отображение личного идентификационного номера (ПИН-кода), а другие поддерживают отображение ПИН-кода и даты истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="8ed6c-121">В качестве альтернативы для этого свойства может быть задано значение "Нет", и тогда отображается только номер подарочного сертификата, а никакие дополнительные поля не отображаются.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="8ed6c-122">Поддерживаемые значения:</span><span class="sxs-lookup"><span data-stu-id="8ed6c-122">Supported values:</span></span>
-   <span data-ttu-id="8ed6c-123">ПИН-код</span><span class="sxs-lookup"><span data-stu-id="8ed6c-123">PIN</span></span>
-   <span data-ttu-id="8ed6c-124">Срок действия</span><span class="sxs-lookup"><span data-stu-id="8ed6c-124">Expiration date</span></span>
-   <span data-ttu-id="8ed6c-125">ПИН-код и срок действия</span><span class="sxs-lookup"><span data-stu-id="8ed6c-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="8ed6c-126">Не допускается</span><span class="sxs-lookup"><span data-stu-id="8ed6c-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="8ed6c-127">Параметры сайта для модулей подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="8ed6c-127">Site settings for gift card modules</span></span>

<span data-ttu-id="8ed6c-128">В конфигураторе сайта Commerce в пункте **Параметры сайта \> Расширения** имеется модуль подарочного сертификата с названием **Поддерживаемый тип подарочного сертификата**.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-128">In Commerce site builder under **Site Settings \> Extensions** , there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="8ed6c-129">Эта настройка поддерживает три значения:</span><span class="sxs-lookup"><span data-stu-id="8ed6c-129">This setting supports three values:</span></span>
- <span data-ttu-id="8ed6c-130">**Подарочный сертификат Dynamics 365** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="8ed6c-131">Эта настройка поддерживается только для пользователей, выполнивших вход на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="8ed6c-132">**Подарочные сертификаты SVS и Givex** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="8ed6c-133">Эта настройка поддерживается для пользователей, выполнивших вход, и анонимных пользователей на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="8ed6c-134">**Подарочные сертификаты Dynamics 365, SVS и Givex** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов Dynamics 365, SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="8ed6c-135">Эта настройка поддерживается только для пользователей, выполнивших вход на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ed6c-136">Эти параметры доступны в выпуске Dynamics 365 Commerce 10.0.11 и требуются только в том случае, если необходима поддержка подарочных сертификатов SVS или Givex.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="8ed6c-137">Если выполняется обновление из более ранней версии Dynamics 365 Commerce, необходимо вручную обновить файл appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="8ed6c-138">Инструкции по обновлению файла appsettings.json см. в разделе [Обновления SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="8ed6c-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="8ed6c-139">Добавление модуля подарочных сертификатов на страницу</span><span class="sxs-lookup"><span data-stu-id="8ed6c-139">Add a gift card module to a page</span></span>

<span data-ttu-id="8ed6c-140">Инструкции по добавлению модуля подарочного сертификата на страницу оформления покупки и заданию требуемых свойств см. в разделе [Модуль оформления заказа](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="8ed6c-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ed6c-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8ed6c-141">Additional resources</span></span>

[<span data-ttu-id="8ed6c-142">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="8ed6c-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8ed6c-143">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="8ed6c-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="8ed6c-144">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="8ed6c-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8ed6c-145">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="8ed6c-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="8ed6c-146">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="8ed6c-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="8ed6c-147">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="8ed6c-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="8ed6c-148">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="8ed6c-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8ed6c-149">Поддержка внешних подарочных карт</span><span class="sxs-lookup"><span data-stu-id="8ed6c-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="8ed6c-150">Обновления SDK и библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="8ed6c-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
