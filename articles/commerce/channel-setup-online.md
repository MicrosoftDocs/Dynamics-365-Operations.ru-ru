---
title: Настройка канала онлайн-торговли
description: В этом разделе описывается, как создать интернет-канал в Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: f0f1e0f3e7145c66b8f2b082b44ad7035c57d947
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936952"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="3f405-103">Настройка канала онлайн-торговли</span><span class="sxs-lookup"><span data-stu-id="3f405-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3f405-104">В этом разделе описывается, как создать интернет-канал в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f405-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3f405-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="3f405-105">Overview</span></span>

<span data-ttu-id="3f405-106">Dynamics 365 Commerce поддерживает несколько розничных каналов.</span><span class="sxs-lookup"><span data-stu-id="3f405-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="3f405-107">Эти розничные каналы включают в себя интернет-магазины, центры обработки вызовов и розничные магазины (также называются физическими магазинами).</span><span class="sxs-lookup"><span data-stu-id="3f405-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="3f405-108">Интернет-магазины дает возможность покупать продукты не только в розничных магазинах торговца, но и в интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="3f405-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="3f405-109">Чтобы создать интернет-магазин в модуле Commerce, необходимо сначала создать интернет-канал.</span><span class="sxs-lookup"><span data-stu-id="3f405-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="3f405-110">Перед созданием нового интернет-канала убедитесь, что вы соблюдаете [Необходимые условия для настройки каналов](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="3f405-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="3f405-111">Прежде чем можно будет создать новый сайт, необходимо создать по крайней мере один интернет-магазин в Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f405-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="3f405-112">Дополнительные сведения см. в разделе [Создание сайта электронной коммерции](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="3f405-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="3f405-113">Создание и настройка нового интернет-канала</span><span class="sxs-lookup"><span data-stu-id="3f405-113">Create and configure a new online channel</span></span>

<span data-ttu-id="3f405-114">Чтобы создать и настроить новый интернет-канал, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f405-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="3f405-115">В области переходов перейдите **Модули \> Каналы \> Интернет-магазины**.</span><span class="sxs-lookup"><span data-stu-id="3f405-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="3f405-116">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3f405-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3f405-117">Вставьте имя для нового канала в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="3f405-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="3f405-118">В раскрывающемся списке **Юридическое лицо** введите соответствующее юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="3f405-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="3f405-119">В раскрывающемся списке **Склад** введите соответствующий склад.</span><span class="sxs-lookup"><span data-stu-id="3f405-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="3f405-120">В поле **Часовой пояс магазина** выберите нужный часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="3f405-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="3f405-121">В поле **Валюта** выберите подходящую валюту.</span><span class="sxs-lookup"><span data-stu-id="3f405-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="3f405-122">В поле **Клиент по умолчанию** укажите допустимый клиент по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3f405-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="3f405-123">В поле **Адресная книга клиентов** укажите допустимую адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="3f405-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="3f405-124">В поле **Профиль функциональности** выберите профиль функциональности, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="3f405-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="3f405-125">В поле **Профиль уведомлений по электронной почте** укажите допустимый профиль уведомлений по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="3f405-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="3f405-126">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3f405-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="3f405-127">На следующем рисунке показано создание нового интернет-канала.</span><span class="sxs-lookup"><span data-stu-id="3f405-127">The following image shows the creation of a new online channel.</span></span>

![Новый интернет-канал](media/channel-setup-online-1.png)

<span data-ttu-id="3f405-129">На следующем рисунке показан пример интернет-канала.</span><span class="sxs-lookup"><span data-stu-id="3f405-129">The following image shows an example online channel.</span></span>

![Пример интернет-канала](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="3f405-131">Настройка языков</span><span class="sxs-lookup"><span data-stu-id="3f405-131">Set up languages</span></span>

<span data-ttu-id="3f405-132">Если веб-узел электронной коммерции поддерживает несколько языков, разверните раздел **Языки** и добавьте дополнительные языки по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="3f405-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="3f405-133">Настрое счета оплаты</span><span class="sxs-lookup"><span data-stu-id="3f405-133">Set up payment account</span></span>

<span data-ttu-id="3f405-134">В разделе **Счет оплаты** можно добавить стороннего поставщика платежа.</span><span class="sxs-lookup"><span data-stu-id="3f405-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="3f405-135">Информацию о настройках соединителя платежей Ayden см. в разделе [Соединитель платежей Dynamics 365 для Adyen](./dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="3f405-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="3f405-136">Дополнительная настройка канала</span><span class="sxs-lookup"><span data-stu-id="3f405-136">Additional channel setup</span></span>

<span data-ttu-id="3f405-137">Дополнительные задачи, которые необходимы для настройки интернет-канала, включают настройку способов оплаты, способов поставки и назначения группы выполнения.</span><span class="sxs-lookup"><span data-stu-id="3f405-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="3f405-138">На следующем рисунке показаны варианты настройки **Режимы поставки**, **Способы оплаты** и **Назначение группы выполнения** на вкладке **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="3f405-138">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Дополнительные действия по настройке интернет-канала](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="3f405-140">Настройка способов оплаты</span><span class="sxs-lookup"><span data-stu-id="3f405-140">Set up payment methods</span></span>

<span data-ttu-id="3f405-141">Для настройки способов оплаты для каждого типа платежа, поддерживаемого в этом канале, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f405-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="3f405-142">На панели операций выберите вкладку **Настройка**, а затем выберите **Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="3f405-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="3f405-143">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3f405-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3f405-144">В области переходов выберите нужный способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="3f405-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="3f405-145">В разделе **Общие** введите **Имя операции** и настройте другие необходимые элементы.</span><span class="sxs-lookup"><span data-stu-id="3f405-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="3f405-146">Настройте дополнительные параметры, необходимые для типа оплаты.</span><span class="sxs-lookup"><span data-stu-id="3f405-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="3f405-147">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3f405-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="3f405-148">На следующем рисунке показан пример способы наличной оплаты.</span><span class="sxs-lookup"><span data-stu-id="3f405-148">The following image shows an example of a cash payment method.</span></span>

![Пример способов оплаты](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="3f405-150">Настройка способов поставки</span><span class="sxs-lookup"><span data-stu-id="3f405-150">Set up modes of delivery</span></span>

<span data-ttu-id="3f405-151">Настроенные способы поставки можно просмотреть, выбрав **Способы поставки** на вкладке **Настройка** на **панели операций**.</span><span class="sxs-lookup"><span data-stu-id="3f405-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="3f405-152">Чтобы изменить или добавить способ поставки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f405-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="3f405-153">В области переходов перейдите **Модули \> Управление запасами \> Режимы поставки**.</span><span class="sxs-lookup"><span data-stu-id="3f405-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="3f405-154">В области действий выберите **Создать**, чтобы создать новый способ поставки, или выберите существующий режим.</span><span class="sxs-lookup"><span data-stu-id="3f405-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="3f405-155">В разделе **Каналы розничной торговли** выберите **Добавить строку**, чтобы добавить канал.</span><span class="sxs-lookup"><span data-stu-id="3f405-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="3f405-156">Добавление каналов с помощью узлов организации вместо добавления каждого канала по отдельности может ускорить добавление каналов.</span><span class="sxs-lookup"><span data-stu-id="3f405-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="3f405-157">На следующем рисунке показан пример режима поставки.</span><span class="sxs-lookup"><span data-stu-id="3f405-157">The following image shows an example of a mode of delivery.</span></span>

![Настройка способов поставки](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="3f405-159">Настройка назначения группы выполнения</span><span class="sxs-lookup"><span data-stu-id="3f405-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="3f405-160">Чтобы настроить назначение группы выполнения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f405-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="3f405-161">На панели операций выберите вкладку **Настройка**, а затем выберите **Назначение группы выполнения**.</span><span class="sxs-lookup"><span data-stu-id="3f405-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="3f405-162">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3f405-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3f405-163">В раскрывающемся списке **Группа выполнения** выберите группу выполнения.</span><span class="sxs-lookup"><span data-stu-id="3f405-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="3f405-164">В **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="3f405-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="3f405-165">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3f405-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="3f405-166">На следующем рисунке показан пример настройки назначения группы выполнения.</span><span class="sxs-lookup"><span data-stu-id="3f405-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Настройка назначения группы выполнения](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="3f405-168">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3f405-168">Additional resources</span></span>

[<span data-ttu-id="3f405-169">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="3f405-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="3f405-170">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="3f405-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="3f405-171">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="3f405-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="3f405-172">Настройка канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="3f405-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="3f405-173">Соединитель платежей Dynamics 365 для Adyen</span><span class="sxs-lookup"><span data-stu-id="3f405-173">Dynamics 365 Payment Connector for Adyen</span></span>](./dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]