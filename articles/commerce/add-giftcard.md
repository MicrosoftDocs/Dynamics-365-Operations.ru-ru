---
title: Модуль подарочного сертификата
description: В этом разделе описываются модули подарочных сертификатов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962771"
---
# <a name="gift-card-module"></a><span data-ttu-id="378e5-103">Модуль подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="378e5-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="378e5-104">В этом разделе описываются модули подарочных сертификатов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="378e5-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="378e5-105">Модули подарочных сертификатов могут использоваться в модуле оформления покупки для приема подарочных сертификатов, которые являются распространенной формой оплаты, используемой в проводках электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="378e5-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="378e5-106">Модуль подарочного сертификата поддерживает подарочные сертификаты Dynamics 365, SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="378e5-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="378e5-107">Подарочные сертификаты SVS и Givex погашаются через поставщика платежей Adyen.</span><span class="sxs-lookup"><span data-stu-id="378e5-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="378e5-108">Дополнительные сведения о поддержке внешних подарочных сертификатов, таких как SVS и Givex, см. в разделе [Поддержка внешних подарочных сертификатов](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="378e5-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="378e5-109">Поддержка погашения подарочных сертификатов SVS и Givex во время потока оформления покупки доступен в выпуске Dynamics 365 Commerce 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="378e5-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="378e5-110">Доступно два модуля подарочных сертификатов:</span><span class="sxs-lookup"><span data-stu-id="378e5-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="378e5-111">**Подарочный сертификат** — этот модуль может использоваться на странице оформления покупки для погашения подарочного сертификата в качестве платежного средства.</span><span class="sxs-lookup"><span data-stu-id="378e5-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="378e5-112">**Проверка сальдо подарочного сертификата** — этот модуль может использоваться на любой странице для проверки сальдо подарочного сертификата.</span><span class="sxs-lookup"><span data-stu-id="378e5-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="378e5-113">Этот модуль доступен в выпуске Commerce 10.0.14 и выше.</span><span class="sxs-lookup"><span data-stu-id="378e5-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="378e5-114">Поддержка модуля проверки сальдо подарочного сертификата доступна в выпуске Dynamics 365 Commerce 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="378e5-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="378e5-115">На следующем рисунке показан пример модуля подарочного сертификата на странице оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="378e5-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Пример модуля подарочного сертификата](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="378e5-117">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="378e5-117">Module properties</span></span>

- <span data-ttu-id="378e5-118">**Показывать дополнительные поля** — это свойство определяет, какие поля должны отображаться для подарочных сертификатов в дополнение к номеру подарочного сертификата, который всегда отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="378e5-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="378e5-119">Например, некоторые подарочные сертификаты поддерживают отображение личного идентификационного номера (ПИН-кода), а другие поддерживают отображение ПИН-кода и даты истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="378e5-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="378e5-120">В качестве альтернативы для этого свойства может быть задано значение "Нет", и тогда отображается только номер подарочного сертификата, а никакие дополнительные поля не отображаются.</span><span class="sxs-lookup"><span data-stu-id="378e5-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="378e5-121">Поддерживаемые значения:</span><span class="sxs-lookup"><span data-stu-id="378e5-121">Supported values:</span></span>
-   <span data-ttu-id="378e5-122">ПИН-код</span><span class="sxs-lookup"><span data-stu-id="378e5-122">PIN</span></span>
-   <span data-ttu-id="378e5-123">Срок действия</span><span class="sxs-lookup"><span data-stu-id="378e5-123">Expiration date</span></span>
-   <span data-ttu-id="378e5-124">ПИН-код и срок действия</span><span class="sxs-lookup"><span data-stu-id="378e5-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="378e5-125">Не допускается</span><span class="sxs-lookup"><span data-stu-id="378e5-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="378e5-126">Параметры сайта для модулей подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="378e5-126">Site settings for gift card modules</span></span>

<span data-ttu-id="378e5-127">В конфигураторе сайта Commerce в пункте **Параметры сайта \> Расширения** имеется модуль подарочного сертификата с названием **Поддерживаемый тип подарочного сертификата**.</span><span class="sxs-lookup"><span data-stu-id="378e5-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="378e5-128">Эта настройка поддерживает три значения:</span><span class="sxs-lookup"><span data-stu-id="378e5-128">This setting supports three values:</span></span>
- <span data-ttu-id="378e5-129">**Подарочный сертификат Dynamics 365** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="378e5-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="378e5-130">Эта настройка поддерживается только для пользователей, выполнивших вход на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="378e5-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="378e5-131">**Подарочные сертификаты SVS и Givex** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="378e5-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="378e5-132">Эта настройка поддерживается для пользователей, выполнивших вход, и анонимных пользователей на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="378e5-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="378e5-133">**Подарочные сертификаты Dynamics 365, SVS и Givex** — когда этот параметр применяется, модуль подарочного сертификата разрешает погашение подарочных сертификатов Dynamics 365, SVS и Givex.</span><span class="sxs-lookup"><span data-stu-id="378e5-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="378e5-134">Эта настройка поддерживается только для пользователей, выполнивших вход на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="378e5-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="378e5-135">Эти параметры доступны в выпуске Dynamics 365 Commerce 10.0.11 и требуются только в том случае, если необходима поддержка подарочных сертификатов SVS или Givex.</span><span class="sxs-lookup"><span data-stu-id="378e5-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="378e5-136">Если выполняется обновление из более ранней версии Dynamics 365 Commerce, необходимо вручную обновить файл appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="378e5-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="378e5-137">Инструкции по обновлению файла appsettings.json см. в разделе [Обновления SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="378e5-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="378e5-138">Расширение внутренних подарочных сертификатов для использования в витринах электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="378e5-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="378e5-139">По умолчанию внутренние подарочные сертификаты не оптимизируются для использования в витринах электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="378e5-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="378e5-140">Поэтому перед тем как разрешить использование внутренних подарочных сертификатов для платежа, их следует настроить с помощью расширений, которые увеличивают их безопасность.</span><span class="sxs-lookup"><span data-stu-id="378e5-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="378e5-141">Здесь следует расширить области подарочного сертификата перед тем, как разрешить использование внутренних подарочных сертификатов в производстве:</span><span class="sxs-lookup"><span data-stu-id="378e5-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="378e5-142">**Номер подарочного сертификата** — номерные серии используются для создания номеров подарочных сертификатов для внутренних подарочных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="378e5-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="378e5-143">Так как можно легко предсказать номерные серии, следует расширить создание номеров подарочных сертификатов таким образом, чтобы случайные зашифрованные строки использовались для выпущенных номеров подарочных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="378e5-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="378e5-144">**GetBalance** — API **GetBalance** используется для поиска сальдо подарочных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="378e5-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="378e5-145">По умолчанию этот API является общедоступным.</span><span class="sxs-lookup"><span data-stu-id="378e5-145">By default, this API public.</span></span> <span data-ttu-id="378e5-146">Если для поиска сальдо подарочного сертификата не требуется PIN-код, существует риск того, что атаки методом подбора могут использовать API **GetBalance**, чтобы найти номера подарочных сертификатов, имеющие сальдо.</span><span class="sxs-lookup"><span data-stu-id="378e5-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="378e5-147">При реализации обоих требований к PIN для внутренних подарочных сертификатов и регулирования количества запросов API можно снизить риск.</span><span class="sxs-lookup"><span data-stu-id="378e5-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="378e5-148">**PIN-код** — по умолчанию внутренние подарочные сертификаты не поддерживают PIN-коды.</span><span class="sxs-lookup"><span data-stu-id="378e5-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="378e5-149">Необходимо расширить внутренние подарочные сертификаты, чтобы для поиска сальдо был обязателен PIN-код.</span><span class="sxs-lookup"><span data-stu-id="378e5-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="378e5-150">Эта функция также может использоваться для блокировки подарочных сертификатов после неудачных попыток ввода ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="378e5-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="378e5-151">Включение платежей подарочных сертификатов для оформления заказа клиента-гостя</span><span class="sxs-lookup"><span data-stu-id="378e5-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="378e5-152">По умолчанию платежи подарочного сертификата не разрешены для оформления заказа клиента-гостя (анонимного).</span><span class="sxs-lookup"><span data-stu-id="378e5-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="378e5-153">Для включения выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="378e5-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="378e5-154">В Commerce Headquarters перейдите в раздел **Retail и Commerce \> Настройка канала \> Настройка POS \> POS \> Операции POS**.</span><span class="sxs-lookup"><span data-stu-id="378e5-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="378e5-155">Выберите и удерживайте (или щелкните правой кнопкой мыши) заголовок сетки, а затем выберите **Вставить столбцы**.</span><span class="sxs-lookup"><span data-stu-id="378e5-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="378e5-156">В диалоговом окне **Вставка столбцов** установите флажок **AllowAnonymousAccess**.</span><span class="sxs-lookup"><span data-stu-id="378e5-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="378e5-157">Выберите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="378e5-157">Select **Update**.</span></span>
1. <span data-ttu-id="378e5-158">Для операций **520** (сальдо подарочного сертификата) и **214** задайте значение **AllowAnonymousAccess** как **1**.</span><span class="sxs-lookup"><span data-stu-id="378e5-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="378e5-159">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="378e5-159">Select **Save**.</span></span>
1. <span data-ttu-id="378e5-160">Выполните задание планировщика **1090**, чтобы синхронизировать изменения в базе данных канала.</span><span class="sxs-lookup"><span data-stu-id="378e5-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="378e5-161">Добавление модуля подарочных сертификатов на страницу</span><span class="sxs-lookup"><span data-stu-id="378e5-161">Add a gift card module to a page</span></span>

<span data-ttu-id="378e5-162">Инструкции по добавлению модуля подарочного сертификата на страницу оформления покупки и заданию требуемых свойств см. в разделе [Модуль оформления заказа](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="378e5-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="378e5-163">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="378e5-163">Additional resources</span></span>

[<span data-ttu-id="378e5-164">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="378e5-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="378e5-165">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="378e5-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="378e5-166">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="378e5-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="378e5-167">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="378e5-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="378e5-168">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="378e5-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="378e5-169">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="378e5-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="378e5-170">Модуль сведений о самовывозе</span><span class="sxs-lookup"><span data-stu-id="378e5-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="378e5-171">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="378e5-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="378e5-172">Поддержка внешних подарочных карт</span><span class="sxs-lookup"><span data-stu-id="378e5-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="378e5-173">Обновления SDK и библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="378e5-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
