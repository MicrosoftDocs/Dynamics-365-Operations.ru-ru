---
title: Настройка интернет-канала
description: В этом разделе описывается, как создать интернет-канал в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002435"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="09509-103">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="09509-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="09509-104">В этом разделе описывается, как создать интернет-канал в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="09509-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="09509-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="09509-105">Overview</span></span>

<span data-ttu-id="09509-106">Dynamics 365 Commerce поддерживает несколько розничных каналов.</span><span class="sxs-lookup"><span data-stu-id="09509-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="09509-107">Эти розничные каналы включают в себя интернет-магазины, центры обработки вызовов и розничные магазины (также называются физическими магазинами).</span><span class="sxs-lookup"><span data-stu-id="09509-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="09509-108">Интернет-магазины дает возможность покупать продукты не только в розничных магазинах торговца, но и в интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="09509-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="09509-109">Чтобы создать интернет-магазин в модуле Commerce, необходимо сначала создать интернет-канал.</span><span class="sxs-lookup"><span data-stu-id="09509-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="09509-110">Перед созданием нового интернет-канала убедитесь, что вы соблюдаете [Необходимые условия для настройки каналов](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="09509-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="09509-111">Создание и настройка нового интернет-канала</span><span class="sxs-lookup"><span data-stu-id="09509-111">Create and configure a new online channel</span></span>

<span data-ttu-id="09509-112">Чтобы создать и настроить новый интернет-канал, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="09509-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="09509-113">В области переходов перейдите **Модули \> Каналы \> Интернет-магазины**.</span><span class="sxs-lookup"><span data-stu-id="09509-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="09509-114">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="09509-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="09509-115">Вставьте имя для нового канала в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="09509-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="09509-116">В раскрывающемся списке **Юридическое лицо** введите соответствующее юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="09509-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="09509-117">В раскрывающемся списке **Склад** введите соответствующий склад.</span><span class="sxs-lookup"><span data-stu-id="09509-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="09509-118">В поле **Часовой пояс магазина** выберите нужный часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="09509-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="09509-119">В поле **Валюта** выберите подходящую валюту.</span><span class="sxs-lookup"><span data-stu-id="09509-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="09509-120">В поле **Клиент по умолчанию** укажите допустимый клиент по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="09509-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="09509-121">В поле **Адресная книга клиентов** укажите допустимую адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="09509-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="09509-122">В поле **Профиль функциональности** выберите профиль функциональности, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="09509-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="09509-123">В поле **Профиль уведомлений по электронной почте** укажите допустимый профиль уведомлений по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="09509-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="09509-124">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="09509-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="09509-125">На следующем рисунке показано создание нового интернет-канала.</span><span class="sxs-lookup"><span data-stu-id="09509-125">The following image shows the creation of a new online channel.</span></span>

![Новый интернет-канал](media/channel-setup-online-1.png)

<span data-ttu-id="09509-127">На следующем рисунке показан пример интернет-канала.</span><span class="sxs-lookup"><span data-stu-id="09509-127">The following image shows an example online channel.</span></span>

![Пример интернет-канала](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="09509-129">Настройка языков</span><span class="sxs-lookup"><span data-stu-id="09509-129">Set up languages</span></span>

<span data-ttu-id="09509-130">Если веб-узел электронной коммерции поддерживает несколько языков, разверните раздел **Языки** и добавьте дополнительные языки по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="09509-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="09509-131">Настрое счета оплаты</span><span class="sxs-lookup"><span data-stu-id="09509-131">Set up payment account</span></span>

<span data-ttu-id="09509-132">В разделе **Счет оплаты** можно добавить стороннего поставщика платежа.</span><span class="sxs-lookup"><span data-stu-id="09509-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="09509-133">Информацию о настройках соединителя платежей Ayden см. в разделе [Соединитель платежей Dynamics 365 для Adyen](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="09509-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="09509-134">Дополнительная настройка канала</span><span class="sxs-lookup"><span data-stu-id="09509-134">Additional channel set up</span></span>

<span data-ttu-id="09509-135">Дополнительные задачи, необходимые для настройки интернет-канала, включают настройку способов оплаты, способов поставки и назначения группы выполнения.</span><span class="sxs-lookup"><span data-stu-id="09509-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="09509-136">На следующем рисунке показаны варианты настройки **Режимы поставки**, **Способы оплаты** и **Назначение группы выполнения** на вкладке **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="09509-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Дополнительные действия по настройке интернет-канала](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="09509-138">Настройка способов оплаты</span><span class="sxs-lookup"><span data-stu-id="09509-138">Set up payment methods</span></span>

<span data-ttu-id="09509-139">Для настройки способов оплаты для каждого типа платежа, поддерживаемого в этом канале, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="09509-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="09509-140">На панели операций выберите вкладку **Настройка**, а затем выберите **Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="09509-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="09509-141">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="09509-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="09509-142">В области переходов выберите нужный способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="09509-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="09509-143">В разделе **Общие** введите **Имя операции** и настройте другие необходимые элементы.</span><span class="sxs-lookup"><span data-stu-id="09509-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="09509-144">Настройте дополнительные параметры, необходимые для типа оплаты.</span><span class="sxs-lookup"><span data-stu-id="09509-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="09509-145">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="09509-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="09509-146">На следующем рисунке показан пример способы наличной оплаты.</span><span class="sxs-lookup"><span data-stu-id="09509-146">The following image shows an example of a cash payment method.</span></span>

![Пример способов оплаты](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="09509-148">Настройка способов поставки</span><span class="sxs-lookup"><span data-stu-id="09509-148">Set up modes of delivery</span></span>

<span data-ttu-id="09509-149">Настроенные способы поставки можно просмотреть, выбрав **Способы поставки** на вкладке **Настройка** на **панели операций**.</span><span class="sxs-lookup"><span data-stu-id="09509-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="09509-150">Чтобы изменить или добавить способ поставки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="09509-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="09509-151">В области переходов перейдите **Модули \> Управление запасами \> Режимы поставки**.</span><span class="sxs-lookup"><span data-stu-id="09509-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="09509-152">В области действий выберите **Создать**, чтобы создать новый способ поставки, или выберите существующий режим.</span><span class="sxs-lookup"><span data-stu-id="09509-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="09509-153">В разделе **Каналы розничной торговли** выберите **Добавить строку**, чтобы добавить канал.</span><span class="sxs-lookup"><span data-stu-id="09509-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="09509-154">Добавление каналов с помощью узлов организации вместо добавления каждого канала по отдельности может ускорить добавление каналов.</span><span class="sxs-lookup"><span data-stu-id="09509-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="09509-155">На следующем рисунке показан пример режима поставки.</span><span class="sxs-lookup"><span data-stu-id="09509-155">The following image shows an example of a mode of delivery.</span></span>

![Настройка способов поставки](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="09509-157">Настройка назначения группы выполнения</span><span class="sxs-lookup"><span data-stu-id="09509-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="09509-158">Чтобы настроить назначение группы выполнения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="09509-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="09509-159">На панели операций выберите вкладку **Настройка**, а затем выберите **Назначение группы выполнения**.</span><span class="sxs-lookup"><span data-stu-id="09509-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="09509-160">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="09509-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="09509-161">В раскрывающемся списке **Группа выполнения** выберите группу выполнения.</span><span class="sxs-lookup"><span data-stu-id="09509-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="09509-162">В **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="09509-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="09509-163">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="09509-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="09509-164">На следующем рисунке показан пример настройки назначения группы выполнения.</span><span class="sxs-lookup"><span data-stu-id="09509-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Настройка назначения группы выполнения](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="09509-166">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="09509-166">Additional resources</span></span>

[<span data-ttu-id="09509-167">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="09509-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="09509-168">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="09509-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="09509-169">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="09509-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="09509-170">Настройка канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="09509-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="09509-171">Соединитель платежей Dynamics 365 для Adyen</span><span class="sxs-lookup"><span data-stu-id="09509-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
