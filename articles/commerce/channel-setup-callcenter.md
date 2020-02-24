---
title: Настройка канала центра обработки вызовов
description: В этом разделе описывается, как создать канал центра обработки вызовов в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002458"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="34c9f-103">Настройка канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="34c9f-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="34c9f-104">В этом разделе описывается, как создать канал центра обработки вызовов в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="34c9f-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="34c9f-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="34c9f-105">Overview</span></span>

<span data-ttu-id="34c9f-106">В Dynamics 365 Commerce центр обработки вызовов — это тип канала розничной торговли, который можно определить в приложении.</span><span class="sxs-lookup"><span data-stu-id="34c9f-106">In Dynamics 365 Commerce, a call center is a type of retail channel that can be defined in the application.</span></span> <span data-ttu-id="34c9f-107">Определение канала для объектов центра обработки вызовов позволяет системе связывать отдельные данные и обработку заказов по умолчанию с заказами на продажу.</span><span class="sxs-lookup"><span data-stu-id="34c9f-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="34c9f-108">Компания может определить несколько каналов центра обработки вызовов в Commerce.</span><span class="sxs-lookup"><span data-stu-id="34c9f-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="34c9f-109">Перед созданием нового канала центра обработки вызовов убедитесь, что вы соблюдаете [Необходимые условия для настройки каналов](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="34c9f-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="34c9f-110">Создание и настройка нового канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="34c9f-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="34c9f-111">Чтобы создать и настроить новый канал центра обработки вызовов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="34c9f-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="34c9f-112">В области переходов перейдите к **Модули \> Каналы \> Центры обработки вызовов \> Все центры обработки вызовов**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="34c9f-113">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="34c9f-114">Вставьте имя для нового канала в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="34c9f-115">Выберите подходящее **Юридическое лицо** из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="34c9f-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="34c9f-116">Выберите подходящее местоположение **Склад** из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="34c9f-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="34c9f-117">В поле **Клиент по умолчанию** укажите допустимый клиент по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="34c9f-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="34c9f-118">В поле **Профиль уведомлений по электронной почте** укажите допустимый профиль уведомлений по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="34c9f-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="34c9f-119">Предоставьте код информации **Переопределение цены**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="34c9f-120">Для этого, возможно, сначала потребуется создать код информации.</span><span class="sxs-lookup"><span data-stu-id="34c9f-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="34c9f-121">Введите код информации **Код удержания**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="34c9f-122">Для этого, возможно, сначала потребуется создать код информации.</span><span class="sxs-lookup"><span data-stu-id="34c9f-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="34c9f-123">Введите код информации **Кредит**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="34c9f-124">Для этого, возможно, сначала потребуется создать код информации.</span><span class="sxs-lookup"><span data-stu-id="34c9f-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="34c9f-125">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-125">Select **Save**.</span></span>

<span data-ttu-id="34c9f-126">На следующем рисунке показано создание нового канала центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="34c9f-126">The following image shows the creation of a new call center channel.</span></span>

![Новый канал центра обработки вызовов](media/channel-setup-callcenter-1.png)

<span data-ttu-id="34c9f-128">На следующем рисунке показан пример канала центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="34c9f-128">The following image shows an example call center channel.</span></span>

![Пример канала центра обработки вызовов](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="34c9f-130">Дополнительная настройка канала</span><span class="sxs-lookup"><span data-stu-id="34c9f-130">Additional channel setup</span></span>

<span data-ttu-id="34c9f-131">Дополнительные задачи, необходимые для настройки канала центра обработки вызовов, включают настройку способов оплаты и способов поставки.</span><span class="sxs-lookup"><span data-stu-id="34c9f-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="34c9f-132">На следующем рисунке показаны варианты настройки **Режимы поставки** и **Способы оплаты** на вкладке **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Дополнительные действия по настройке канала центра обработки вызовов](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="34c9f-134">Настройка способов оплаты</span><span class="sxs-lookup"><span data-stu-id="34c9f-134">Set up payment methods</span></span>

<span data-ttu-id="34c9f-135">Для настройки способов оплаты для каждого типа платежа, поддерживаемого в этом канале, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="34c9f-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="34c9f-136">На панели операций выберите вкладку **Настройка**, а затем выберите **Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="34c9f-137">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="34c9f-138">В области переходов выберите нужный способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="34c9f-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="34c9f-139">В разделе **Общие** введите **Имя операции** и настройте другие необходимые элементы.</span><span class="sxs-lookup"><span data-stu-id="34c9f-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="34c9f-140">Настройте дополнительные параметры, необходимые для типа оплаты.</span><span class="sxs-lookup"><span data-stu-id="34c9f-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="34c9f-141">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="34c9f-142">На следующем рисунке показан пример способы наличной оплаты.</span><span class="sxs-lookup"><span data-stu-id="34c9f-142">The following image shows an example of a cash payment method.</span></span>

![Пример способов оплаты](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="34c9f-144">Настройка способов поставки</span><span class="sxs-lookup"><span data-stu-id="34c9f-144">Set up modes of delivery</span></span>

<span data-ttu-id="34c9f-145">Настроенные способы поставки можно просмотреть, выбрав **Способы поставки** на вкладке **Настройка** на **панели операций**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="34c9f-146">Чтобы изменить или добавить способ поставки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="34c9f-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="34c9f-147">В области переходов перейдите **Модули \> Управление запасами \> Режимы поставки**.</span><span class="sxs-lookup"><span data-stu-id="34c9f-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="34c9f-148">В области действий выберите **Создать**, чтобы создать новый способ поставки, или выберите существующий режим.</span><span class="sxs-lookup"><span data-stu-id="34c9f-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="34c9f-149">В разделе **Каналы розничной торговли** выберите **Добавить строку**, чтобы добавить канал.</span><span class="sxs-lookup"><span data-stu-id="34c9f-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="34c9f-150">Добавление каналов с помощью узлов организации вместо добавления каждого канала по отдельности может ускорить добавление каналов.</span><span class="sxs-lookup"><span data-stu-id="34c9f-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="34c9f-151">На следующем рисунке показан пример режима поставки.</span><span class="sxs-lookup"><span data-stu-id="34c9f-151">The following image shows an example of a mode of delivery.</span></span>

![Настройка способов поставки](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="34c9f-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="34c9f-153">Additional resources</span></span>

[<span data-ttu-id="34c9f-154">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="34c9f-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="34c9f-155">Функциональность продажи центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="34c9f-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="34c9f-156">Настройка параметров обработки заказов центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="34c9f-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="34c9f-157">Каталоги центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="34c9f-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="34c9f-158">Настройка оповещений о мошенничестве и работа с ними</span><span class="sxs-lookup"><span data-stu-id="34c9f-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="34c9f-159">Настройка программ непрерывности для центров обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="34c9f-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
