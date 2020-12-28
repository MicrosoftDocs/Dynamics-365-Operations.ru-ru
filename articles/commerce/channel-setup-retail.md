---
title: Настройка канала розничной торговли
description: В этом разделе описывается, как создать канал розничной торговли в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: a9291dddf7d4dc080b6eb1ec60702de32a761f45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415200"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="857fb-103">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="857fb-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="857fb-104">В этом разделе описывается, как создать канал розничной торговли в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="857fb-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="857fb-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="857fb-105">Overview</span></span>

<span data-ttu-id="857fb-106">Dynamics 365 Commerce поддерживает несколько розничных каналов.</span><span class="sxs-lookup"><span data-stu-id="857fb-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="857fb-107">Эти розничные каналы включают в себя интернет-магазины, центры обработки вызовов и розничные магазины (также называются физическими магазинами).</span><span class="sxs-lookup"><span data-stu-id="857fb-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="857fb-108">Каждый канал розничного магазина может иметь свои собственные способы оплаты, группы цен, контрольно-кассовые машины POS, счета выручки и расходов и сотрудников.</span><span class="sxs-lookup"><span data-stu-id="857fb-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="857fb-109">Необходимо настроить все эти элементы перед тем, как можно создать канал розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="857fb-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="857fb-110">Перед созданием канала розничной торговли убедитесь, что выполнены [необходимые условия для канала](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="857fb-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="857fb-111">Создание и настройка нового канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="857fb-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="857fb-112">В области переходов перейдите **Модули \> Каналы \> Магазины \> Все магазины**.</span><span class="sxs-lookup"><span data-stu-id="857fb-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="857fb-113">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="857fb-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="857fb-114">Вставьте имя для нового канала в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="857fb-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="857fb-115">В поле **Номер магазина** выберите уникальный номер магазина.</span><span class="sxs-lookup"><span data-stu-id="857fb-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="857fb-116">Это число может состоять из букв и цифр и не больше 10 символов.</span><span class="sxs-lookup"><span data-stu-id="857fb-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="857fb-117">В раскрывающемся списке **Юридическое лицо** введите соответствующее юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="857fb-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="857fb-118">В раскрывающемся списке **Склад** введите соответствующий склад.</span><span class="sxs-lookup"><span data-stu-id="857fb-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="857fb-119">В поле **Часовой пояс магазина** выберите нужный часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="857fb-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="857fb-120">В раскрывающемся списке **Налоговая группа** выберите подходящую налоговую группу для магазина.</span><span class="sxs-lookup"><span data-stu-id="857fb-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="857fb-121">В поле **Валюта** выберите подходящую валюту.</span><span class="sxs-lookup"><span data-stu-id="857fb-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="857fb-122">В поле **Адресная книга клиентов** укажите допустимую адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="857fb-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="857fb-123">В поле **Клиент по умолчанию** укажите допустимый клиент по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="857fb-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="857fb-124">В поле **Профиль функциональности** выберите профиль функциональности, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="857fb-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="857fb-125">В поле **Профиль уведомлений по электронной почте** укажите допустимый профиль уведомлений по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="857fb-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="857fb-126">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="857fb-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="857fb-127">На следующем рисунке показано создание нового канала розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="857fb-127">The following image shows the creation of a new retail channel.</span></span>

![Новый канал розничной торговли](media/channel-setup-retail-1.png)

<span data-ttu-id="857fb-129">На следующем рисунке показан пример канала розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="857fb-129">The following image shows an example retail channel.</span></span>

![Пример канала розничной торговли](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="857fb-131">Другие параметры</span><span class="sxs-lookup"><span data-stu-id="857fb-131">Other settings</span></span>

<span data-ttu-id="857fb-132">Имеется множество других необязательных настроек, которые могут быть заданы в разделах **Операция/закрытие** и **Разный** в зависимости от потребностей розничного магазина.</span><span class="sxs-lookup"><span data-stu-id="857fb-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="857fb-133">Кроме того, см. [Макеты экрана для POS](pos-screen-layouts.md) для получения сведений о настройке макета экрана по умолчанию в разделе **Макет экрана** и [Настройка и установка Retail Hardware Station](retail-hardware-station-configuration-installation.md) для настройки сведений о разделе **Станции оборудования**.</span><span class="sxs-lookup"><span data-stu-id="857fb-133">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="857fb-134">На следующем рисунке показан пример конфигурации настройки канала розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="857fb-134">The following image shows an example retail channel setup configuration.</span></span>

![Пример конфигурации канала розничной торговли](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="857fb-136">Дополнительная настройка канала</span><span class="sxs-lookup"><span data-stu-id="857fb-136">Additional channel set up</span></span>

<span data-ttu-id="857fb-137">Имеются дополнительные элементы, которые необходимо настроить для канала, который можно найти на **панели операций** в разделе **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="857fb-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="857fb-138">Дополнительные задачи, необходимые для настройки интернет-канала, включают настройку способов оплаты, декларацию наличных денег, способов поставки, приходный/расходный счет, разделы, назначения группы выполнения и безопасности.</span><span class="sxs-lookup"><span data-stu-id="857fb-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="857fb-139">На следующем рисунке показаны дополнительные параметры настройки канала розничной торговли на вкладке **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="857fb-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Настройка канала](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="857fb-141">Настройка способов оплаты</span><span class="sxs-lookup"><span data-stu-id="857fb-141">Set up payment methods</span></span>

<span data-ttu-id="857fb-142">Для настройки способов оплаты для каждого типа платежа, поддерживаемого в этом канале, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="857fb-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="857fb-143">На панели операций выберите вкладку **Настройка**, а затем выберите **Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="857fb-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="857fb-144">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="857fb-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="857fb-145">В области переходов выберите нужный способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="857fb-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="857fb-146">В разделе **Общие** введите **Имя операции** и настройте другие необходимые элементы.</span><span class="sxs-lookup"><span data-stu-id="857fb-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="857fb-147">Настройте дополнительные параметры, необходимые для типа оплаты.</span><span class="sxs-lookup"><span data-stu-id="857fb-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="857fb-148">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="857fb-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="857fb-149">На следующем рисунке показан пример способы наличной оплаты.</span><span class="sxs-lookup"><span data-stu-id="857fb-149">The following image shows an example of a cash payment method.</span></span>

![Пример способов оплаты](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="857fb-151">Настройка декларирования наличности</span><span class="sxs-lookup"><span data-stu-id="857fb-151">Set up cash declaration</span></span>

1. <span data-ttu-id="857fb-152">На панели операций выберите вкладку **Настройка**, а затем выберите **Декларирование наличности**.</span><span class="sxs-lookup"><span data-stu-id="857fb-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="857fb-153">В области действий выберите **Создать**, а затем создайте все номиналы **Монета** и **Банкнота**, которые используются.</span><span class="sxs-lookup"><span data-stu-id="857fb-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="857fb-154">На следующем рисунке показан пример способы декларирования наличности.</span><span class="sxs-lookup"><span data-stu-id="857fb-154">The following image shows an example of a cash declaration.</span></span>

![Настройка декларирования наличности](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="857fb-156">Настройка способов поставки</span><span class="sxs-lookup"><span data-stu-id="857fb-156">Set up modes of delivery</span></span>

<span data-ttu-id="857fb-157">Настроенные способы поставки можно просмотреть, выбрав **Способы поставки** на вкладке **Настройка** на **панели операций**.</span><span class="sxs-lookup"><span data-stu-id="857fb-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="857fb-158">Чтобы изменить или добавить способ поставки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="857fb-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="857fb-159">В области переходов перейдите **Модули \> Управление запасами \> Режимы поставки**.</span><span class="sxs-lookup"><span data-stu-id="857fb-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="857fb-160">В области действий выберите **Создать**, чтобы создать новый способ поставки, или выберите существующий режим.</span><span class="sxs-lookup"><span data-stu-id="857fb-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="857fb-161">В разделе **Каналы розничной торговли** выберите **Добавить строку**, чтобы добавить канал.</span><span class="sxs-lookup"><span data-stu-id="857fb-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="857fb-162">Добавление каналов с помощью узлов организации вместо добавления каждого канала по отдельности может ускорить добавление каналов.</span><span class="sxs-lookup"><span data-stu-id="857fb-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="857fb-163">На следующем рисунке показан пример режима поставки.</span><span class="sxs-lookup"><span data-stu-id="857fb-163">The following image shows an example of a mode of delivery.</span></span>

![Настройка способов поставки](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="857fb-165">Настройка приходного/расходного счета</span><span class="sxs-lookup"><span data-stu-id="857fb-165">Set up income/expense account</span></span>

<span data-ttu-id="857fb-166">Чтобы настроить приходный/расходный счет, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="857fb-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="857fb-167">На панели операций выберите вкладку **Настройка**, а затем выберите **Приходный/расходный счет**.</span><span class="sxs-lookup"><span data-stu-id="857fb-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="857fb-168">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="857fb-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="857fb-169">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="857fb-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="857fb-170">В области **Краткое наименование** введите краткое наименование.</span><span class="sxs-lookup"><span data-stu-id="857fb-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="857fb-171">В **Тип счета** введите тип счета.</span><span class="sxs-lookup"><span data-stu-id="857fb-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="857fb-172">Введите текст для **Строка сообщения 1**, **Строка сообщения 2**, **Текст квитанции 1** и **Текст квитанции 2**, как необходимо.</span><span class="sxs-lookup"><span data-stu-id="857fb-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="857fb-173">В области **Разноска** введите сведения о разноске.</span><span class="sxs-lookup"><span data-stu-id="857fb-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="857fb-174">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="857fb-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="857fb-175">На следующем рисунке показан пример счета приходного/расходного счета.</span><span class="sxs-lookup"><span data-stu-id="857fb-175">The following image shows an example of an income/expense account.</span></span>

![Настройка приходных/расходных счетов](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="857fb-177">Настройка разделов</span><span class="sxs-lookup"><span data-stu-id="857fb-177">Set up sections</span></span>

<span data-ttu-id="857fb-178">Чтобы настроить разделы, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="857fb-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="857fb-179">На панели операций выберите вкладку **Настройка**, а затем выберите **Разделы**.</span><span class="sxs-lookup"><span data-stu-id="857fb-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="857fb-180">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="857fb-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="857fb-181">В поле **Номер раздела** введите номер раздела.</span><span class="sxs-lookup"><span data-stu-id="857fb-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="857fb-182">В **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="857fb-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="857fb-183">В поле **Размер раздела** введите размер раздела.</span><span class="sxs-lookup"><span data-stu-id="857fb-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="857fb-184">При необходимости настройте дополнительные параметры для **Общее** и **Статистика по продажам**.</span><span class="sxs-lookup"><span data-stu-id="857fb-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="857fb-185">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="857fb-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="857fb-186">Настройка назначения группы выполнения</span><span class="sxs-lookup"><span data-stu-id="857fb-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="857fb-187">Чтобы настроить назначение группы выполнения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="857fb-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="857fb-188">На панели операций выберите вкладку **Настройка**, а затем выберите **Назначение группы выполнения**.</span><span class="sxs-lookup"><span data-stu-id="857fb-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="857fb-189">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="857fb-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="857fb-190">В раскрывающемся списке **Группа выполнения** выберите группу выполнения.</span><span class="sxs-lookup"><span data-stu-id="857fb-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="857fb-191">В **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="857fb-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="857fb-192">На панели операций выберите **Сохранить**</span><span class="sxs-lookup"><span data-stu-id="857fb-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="857fb-193">На следующем рисунке показан пример настройки назначения группы выполнения.</span><span class="sxs-lookup"><span data-stu-id="857fb-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Настройка назначений группы выполнения](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="857fb-195">Настройка сейфов</span><span class="sxs-lookup"><span data-stu-id="857fb-195">Set up safes</span></span>

<span data-ttu-id="857fb-196">Чтобы настроить сейфы, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="857fb-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="857fb-197">На панели операций выберите вкладку **Настройка**, а затем выберите **Сейфы**.</span><span class="sxs-lookup"><span data-stu-id="857fb-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="857fb-198">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="857fb-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="857fb-199">Введите имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="857fb-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="857fb-200">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="857fb-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="857fb-201">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="857fb-201">Additional resources</span></span>

[<span data-ttu-id="857fb-202">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="857fb-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="857fb-203">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="857fb-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="857fb-204">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="857fb-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="857fb-205">Настройка канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="857fb-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)

