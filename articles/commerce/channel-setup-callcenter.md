---
title: Настройка канала центра обработки вызовов
description: В этом разделе описывается, как создать канал центра обработки вызовов в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3f8c47c00b920dae01213d1d241ac8ee6a18d4e3
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/24/2020
ms.locfileid: "4415390"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="d6699-103">Настройка канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="d6699-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d6699-104">В этом разделе описывается, как создать канал центра обработки вызовов в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d6699-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d6699-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="d6699-105">Overview</span></span>


<span data-ttu-id="d6699-106">В Dynamics 365 Commerce центр обработки вызовов — это тип канала Commerce, который можно определить в приложении.</span><span class="sxs-lookup"><span data-stu-id="d6699-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="d6699-107">Определение канала для объектов центра обработки вызовов позволяет системе связывать отдельные данные и обработку заказов по умолчанию с заказами на продажу.</span><span class="sxs-lookup"><span data-stu-id="d6699-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="d6699-108">Хотя компания может определить несколько каналов обработки вызовов в Commerce, важно отметить, что отдельный пользователь может быть связан только с одним каналом обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="d6699-109">Перед созданием нового канала центра обработки вызовов убедитесь, что вы соблюдаете [Необходимые условия для настройки каналов](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d6699-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="d6699-110">Создание и настройка нового канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="d6699-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="d6699-111">Чтобы создать и настроить новый канал центра обработки вызовов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d6699-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="d6699-112">В области переходов откройте раздел **Розничная торговля и коммерция \> Каналы \> Центры обработки вызовов \> Все центры обработки вызовов**.</span><span class="sxs-lookup"><span data-stu-id="d6699-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="d6699-113">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d6699-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d6699-114">Вставьте имя для нового канала в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="d6699-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="d6699-115">Выберите подходящее **Юридическое лицо** из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="d6699-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="d6699-116">Выберите подходящее местоположение **Склад** из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="d6699-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="d6699-117">Это местоположение будет использоваться по умолчанию в заказах на продажу, созданных для данного канала центра обработки вызовов, если на уровне клиента или номенклатуры не определено никаких других значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6699-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="d6699-118">В поле **Клиент по умолчанию** укажите допустимый клиент по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6699-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="d6699-119">Эти данные используются для помощи в автоматическом заполнении значений по умолчанию при создании новых записей клиентов.</span><span class="sxs-lookup"><span data-stu-id="d6699-119">This data is used to assist in autopopulating defaults when new customer records are created.</span></span> <span data-ttu-id="d6699-120">При создании заказов в центре обработки вызовов не рекомендуется создавать заказы для клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6699-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="d6699-121">В поле **Профиль уведомлений по электронной почте** укажите допустимый профиль уведомлений по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="d6699-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="d6699-122">По мере создания и обработки заказов в центре обработки вызовов профиль уведомлений по электронной почте используется для запуска автоматических оповещений с помощью электронной почты для клиентов с информацией о статусе их заказов.</span><span class="sxs-lookup"><span data-stu-id="d6699-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="d6699-123">Предоставьте код информации **Переопределение цены**.</span><span class="sxs-lookup"><span data-stu-id="d6699-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="d6699-124">Возможно, для этого сначала потребуется создать код информации.</span><span class="sxs-lookup"><span data-stu-id="d6699-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="d6699-125">Этот информационный код предоставляет набор кодов причин, из которых пользователю будет предложено выбрать при использования функции переопределения цены в заказе центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="d6699-126">Введите код информации **Код удержания**.</span><span class="sxs-lookup"><span data-stu-id="d6699-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="d6699-127">Возможно, для этого сначала потребуется создать код информации.</span><span class="sxs-lookup"><span data-stu-id="d6699-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="d6699-128">Этот информационный код предоставляет набор необязательных кодов причин, из которых пользователю будет предложено выбрать при переводе заказа в состояние ожидания.</span><span class="sxs-lookup"><span data-stu-id="d6699-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="d6699-129">Введите код информации **Кредит**.</span><span class="sxs-lookup"><span data-stu-id="d6699-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="d6699-130">Возможно, для этого сначала потребуется создать код информации.</span><span class="sxs-lookup"><span data-stu-id="d6699-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="d6699-131">Этот информационный код предоставляет набор кодов причин, из которых пользователь может выбирать при использовании функции кредита по заказу центра обработки вызовов, и предоставляет клиентам различные способы возврата для причин обслуживания клиентов.</span><span class="sxs-lookup"><span data-stu-id="d6699-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="d6699-132">Необязательно: настройте финансовые аналитики на экспресс-вкладке **Финансовые аналитики**.</span><span class="sxs-lookup"><span data-stu-id="d6699-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="d6699-133">Введенные здесь аналитики будут использоваться по умолчанию для любого заказа на продажу, созданного в этом канале центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="d6699-134">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d6699-134">Click **Save**.</span></span>

<span data-ttu-id="d6699-135">На следующем рисунке показано создание нового канала центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-135">The following image shows the creation of a new call center channel.</span></span>

![Новый канал центра обработки вызовов](media/channel-setup-callcenter-1.png)

<span data-ttu-id="d6699-137">На следующем рисунке показан пример канала центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-137">The following image shows an example call center channel.</span></span>

![Пример канала центра обработки вызовов](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="d6699-139">Дополнительная настройка канала</span><span class="sxs-lookup"><span data-stu-id="d6699-139">Additional channel setup</span></span>

<span data-ttu-id="d6699-140">Дополнительные задачи, необходимые для настройки канала центра обработки вызовов, включают настройку способов оплаты и способов поставки.</span><span class="sxs-lookup"><span data-stu-id="d6699-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="d6699-141">На следующем рисунке показаны варианты настройки **Режимы поставки** и **Способы оплаты** на вкладке **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="d6699-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Дополнительные действия по настройке канала центра обработки вызовов](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="d6699-143">Настройка способов оплаты</span><span class="sxs-lookup"><span data-stu-id="d6699-143">Set up payment methods</span></span>

<span data-ttu-id="d6699-144">Для настройки способов оплаты выполните следующие действия для каждого типа платежа, поддерживаемого в этом канале.</span><span class="sxs-lookup"><span data-stu-id="d6699-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="d6699-145">Пользователям потребуется выбрать из заранее определенных способов оплаты, чтобы связать их с каналом центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="d6699-146">Перед настройкой методов платежа для центра обработки вызовов сначала настройте основные методы оплаты в пункте **Retail и Commerce \> Настройка канала \> Способы оплаты \> Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="d6699-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="d6699-147">На панели операций выберите вкладку **Настройка**, а затем выберите **Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="d6699-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="d6699-148">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d6699-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d6699-149">В области переходов выберите метод оплаты из доступных предварительно определенных платежей.</span><span class="sxs-lookup"><span data-stu-id="d6699-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="d6699-150">Настройте дополнительные параметры, необходимые для типа оплаты.</span><span class="sxs-lookup"><span data-stu-id="d6699-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="d6699-151">Для кредитных карт, подарочных сертификатов или карточек постоянного клиента дополнительная настройка необходима путем выбора функции **Настройка карты**.</span><span class="sxs-lookup"><span data-stu-id="d6699-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="d6699-152">Настройте соответствующие счета разноски для типа платежа в разделе **Разноска**.</span><span class="sxs-lookup"><span data-stu-id="d6699-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="d6699-153">В области операций щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d6699-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="d6699-154">На следующем рисунке показан пример способы наличной оплаты.</span><span class="sxs-lookup"><span data-stu-id="d6699-154">The following image shows an example of a cash payment method.</span></span>

![Пример способов оплаты](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="d6699-156">Настройка способов поставки</span><span class="sxs-lookup"><span data-stu-id="d6699-156">Set up modes of delivery</span></span>

<span data-ttu-id="d6699-157">Настроенные способы поставки можно просмотреть, выбрав **Способы поставки** на вкладке **Настройка** на **панели операций**.</span><span class="sxs-lookup"><span data-stu-id="d6699-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="d6699-158">Чтобы изменить или добавить режим доставки, который должен быть связан с каналом центра обработки вызовов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d6699-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="d6699-159">В форме режимов поставки центра обработки вызовов выберите **Управление режимами доставки**</span><span class="sxs-lookup"><span data-stu-id="d6699-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="d6699-160">В области действий выберите **Создать**, чтобы создать новый способ поставки, или выберите существующий режим.</span><span class="sxs-lookup"><span data-stu-id="d6699-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="d6699-161">В разделе **Каналы розничной торговли** щелкните **Добавить строку**, чтобы добавить канал центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="d6699-162">Добавление каналов с помощью узлов организации вместо добавления каждого канала по отдельности может ускорить добавление каналов.</span><span class="sxs-lookup"><span data-stu-id="d6699-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="d6699-163">Убедитесь, что режим доставки был настроен с данными на экспресс-вкладке **Продукты** и на экспресс-вкладке **Адреса**.</span><span class="sxs-lookup"><span data-stu-id="d6699-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="d6699-164">Если для данного способа поставки нет допустимых продуктов или адресов поставки, выбор этого параметра в процессе ввода заказов приведет к ошибкам.</span><span class="sxs-lookup"><span data-stu-id="d6699-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="d6699-165">После внесения каких-либо изменений в конфигурации доставки режима центра обработки вызовов необходимо выполнить задание **Обработка режимов доставки**, чтобы развернуть матрицу изменений.</span><span class="sxs-lookup"><span data-stu-id="d6699-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="d6699-166">Это задание можно найти , перейдя к пункту **Retail и Commerce \> ИТ Retail и Commerce \> Обработка режимов доставки**.</span><span class="sxs-lookup"><span data-stu-id="d6699-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="d6699-167">На следующем рисунке показан пример режима поставки.</span><span class="sxs-lookup"><span data-stu-id="d6699-167">The following image shows an example of a mode of delivery.</span></span>

![Настройка способов поставки](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="d6699-169">Настройка пользователей канала</span><span class="sxs-lookup"><span data-stu-id="d6699-169">Set up channel users</span></span>

<span data-ttu-id="d6699-170">Чтобы создать заказ на продажу, связанный с каналом центра обработки вызовов из Commerce Headquarters, пользователь, создающий заказ на продажу, должен быть связан с каналом центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="d6699-171">Пользователь не может вручную связать заказ на продажу, созданный в модуле Commerce Headquarters, с каналом центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-171">The user cannot manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="d6699-172">Связь является систематической и основана на пользователе и взаимосвязи пользователя с каналом центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="d6699-173">Пользователь может быть связан только с одним каналом центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="d6699-174">На панели операций выберите вкладку **Канал**, затем выберите **Пользователи канала**.</span><span class="sxs-lookup"><span data-stu-id="d6699-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="d6699-175">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d6699-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d6699-176">Выберите существующий **Идентификатор пользователя** из раскрывающегося списка выбора, чтобы связать этого пользователя с каналом центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="d6699-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="d6699-177">Когда после выполнения настройки пользователей канала пользователь создает новый заказ на продажу, связанный в Commerce Headquarters, заказ на продажу будет связан со связанным с ним каналом центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="d6699-178">Любые конфигурации для этого канала будут систематически применены к заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="d6699-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="d6699-179">Пользователь может проверить, с каким каналом центра обработки вызовов связан заказ на продажу, просмотрев ссылку на имя канала в заголовке заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="d6699-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="d6699-180">Настройка ценовых групп</span><span class="sxs-lookup"><span data-stu-id="d6699-180">Set up price groups</span></span>

<span data-ttu-id="d6699-181">Ценовые группы необязательны, но если они используются, могут управлять тем, какие цены продажи будут предложены клиентам, которые размещают заказы в канале центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d6699-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="d6699-182">Если ценовая группа не была настроена для клиента или если группы цен по каталогу не применяются к заказу на продажу (используя поле **Идентификатор исходного кода** в заголовке заказа центра обработки вызовов), то для поиска цен номенклатур используется ценовая группа канала.</span><span class="sxs-lookup"><span data-stu-id="d6699-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="d6699-183">Если ценовая группа не найдена в канале центра обработки вызовов, используются основные цены номенклатур по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6699-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="d6699-184">Чтобы настроить ценовую группу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d6699-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="d6699-185">На панели операций щелкните вкладку **Канал**, затем выберите **Ценовые группы**.</span><span class="sxs-lookup"><span data-stu-id="d6699-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="d6699-186">В области операций щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d6699-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="d6699-187">Выберите **Розничная ценовая группа** в раскрывающемся списке выбора.</span><span class="sxs-lookup"><span data-stu-id="d6699-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6699-188">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d6699-188">Additional resources</span></span>

[<span data-ttu-id="d6699-189">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="d6699-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d6699-190">Функциональность продажи центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="d6699-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="d6699-191">Настройка параметров обработки заказов центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="d6699-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="d6699-192">Каталоги центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="d6699-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="d6699-193">Настройка оповещений о мошенничестве и работа с ними</span><span class="sxs-lookup"><span data-stu-id="d6699-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="d6699-194">Настройка программ непрерывности для центров обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="d6699-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
