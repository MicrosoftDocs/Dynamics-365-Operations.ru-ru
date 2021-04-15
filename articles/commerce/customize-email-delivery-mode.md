---
title: Настройка транзакционных писем по способу доставки
description: В этом разделе описывается, как настроить пользовательские шаблоны электронной почты для особых типов уведомлений и способов поставки в Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 411e694b33e0443a336f6a8cdad78714630e4bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799381"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="03e4f-103">Настройка транзакционных писем по режиму доставки</span><span class="sxs-lookup"><span data-stu-id="03e4f-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03e4f-104">В этом разделе описывается, как настроить пользовательские шаблоны электронной почты для особых типов уведомлений и способов поставки в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="03e4f-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="03e4f-105">Транзакционные сообщения электронной почты можно теперь настроить для комбинации типа уведомлений (например, **Заказ создан**, **Заказ упакован** или **По заказу выставлен счет**) и способ поставки (например, доставка за ночь, получение в магазине или получение в окне выдачи).</span><span class="sxs-lookup"><span data-stu-id="03e4f-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="03e4f-106">Пользовательские транзакционные письма позволяют розничным продавцам предоставлять своим клиентам варианты выполнения заказов, которые адаптированы к режиму доставки заказов.</span><span class="sxs-lookup"><span data-stu-id="03e4f-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="03e4f-107">Например, событие "заказ упакован" можно настроить таким образом, чтобы оно предоставляло инструкции по получению в окне выдачи для клиентов, которые выбирают получение в окне выдачи.</span><span class="sxs-lookup"><span data-stu-id="03e4f-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="03e4f-108">Кроме того, оно может предоставлять информацию о перевозчике и доставке для клиентов, которые выбирают доставку заказов на свой адрес.</span><span class="sxs-lookup"><span data-stu-id="03e4f-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="03e4f-109">Чтобы использовать функциональные возможности настроенных транзакционных сообщений электронной почты, необходимо сначала включить функцию **Настройка шаблонов транзакционных писем по режиму доставки**, перейдя в раздел **Рабочая область \> Управление функциями** в модуле Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="03e4f-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="03e4f-110">Сообщения электронной почты можно настроить по способу поставки для следующих типов уведомлений:</span><span class="sxs-lookup"><span data-stu-id="03e4f-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="03e4f-111">**Отмена заказов** — этот тип уведомлений электронной почты является новым.</span><span class="sxs-lookup"><span data-stu-id="03e4f-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="03e4f-112">**Заказ создан**</span><span class="sxs-lookup"><span data-stu-id="03e4f-112">**Order created**</span></span>
- <span data-ttu-id="03e4f-113">**Заказ подтвержден**</span><span class="sxs-lookup"><span data-stu-id="03e4f-113">**Order confirmed**</span></span>
- <span data-ttu-id="03e4f-114">**По заказу выставлен счет** — этот тип уведомлений электронной почты является новым.</span><span class="sxs-lookup"><span data-stu-id="03e4f-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="03e4f-115">Он может использоваться вместо типа уведомлений **Заказ отгружен**, который будет отправлять уведомление для любого события выставления счета, которое имеет способ поставки (не самовывоз, прямое получение или электронный способ поставки).</span><span class="sxs-lookup"><span data-stu-id="03e4f-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="03e4f-116">**Заказ скомплектован**</span><span class="sxs-lookup"><span data-stu-id="03e4f-116">**Order picked**</span></span>
- <span data-ttu-id="03e4f-117">**Заказ упакован**</span><span class="sxs-lookup"><span data-stu-id="03e4f-117">**Order packed**</span></span>
- <span data-ttu-id="03e4f-118">**Заказ готов к отправке** — этот тип уведомления можно настроить по режиму доставки только в том случае, если включена функция **Поддержка нескольких режимов доставки для самовывоза**.</span><span class="sxs-lookup"><span data-stu-id="03e4f-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="03e4f-119">В этом случае этот тип уведомления функционально эквивалентен типу уведомлений **Заказ упакован**.</span><span class="sxs-lookup"><span data-stu-id="03e4f-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="03e4f-120">**Ошибка платежа**</span><span class="sxs-lookup"><span data-stu-id="03e4f-120">**Payment failed**</span></span>
- <span data-ttu-id="03e4f-121">**Заказ на замену создан**</span><span class="sxs-lookup"><span data-stu-id="03e4f-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="03e4f-122">Настройка шаблонов электронной почты для различных способов поставки</span><span class="sxs-lookup"><span data-stu-id="03e4f-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="03e4f-123">В рамках этой процедуры предполагается, что вы уже создали новые настраиваемые шаблоны электронной почты и добавили их на страницу **Шаблоны электронной почты организации**.</span><span class="sxs-lookup"><span data-stu-id="03e4f-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="03e4f-124">Сведения о создании и отправке шаблонов электронной почты см. в разделе [Создание шаблонов электронной почты для транзакционных событий](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="03e4f-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="03e4f-125">Чтобы настроить шаблоны электронной почты для конкретных режимов доставки в Commerce Headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="03e4f-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="03e4f-126">Перейти в раздел **Профиль уведомлений по электронной почте Commerce**.</span><span class="sxs-lookup"><span data-stu-id="03e4f-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="03e4f-127">В разделе **Параметры уведомлений о событии розничной торговли** выберите существующий тип уведомлений.</span><span class="sxs-lookup"><span data-stu-id="03e4f-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="03e4f-128">Пока тип уведомления все еще выбран, выберите **Настройка режимов доставки**.</span><span class="sxs-lookup"><span data-stu-id="03e4f-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="03e4f-129">В диалоговом окне **Режимы доставки** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="03e4f-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="03e4f-130">В новой строке в поле **Режим доставки** выберите режим доставки.</span><span class="sxs-lookup"><span data-stu-id="03e4f-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="03e4f-131">В поле **Код электронной почты** выберите шаблон электронной почты, который будет сопоставлен данному способу поставки.</span><span class="sxs-lookup"><span data-stu-id="03e4f-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="03e4f-132">Установите флажок **Активно**.</span><span class="sxs-lookup"><span data-stu-id="03e4f-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="03e4f-133">Повторите шаги с 4 по 7, чтобы добавить дополнительные способы поставки.</span><span class="sxs-lookup"><span data-stu-id="03e4f-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="03e4f-134">Закончив, выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="03e4f-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="03e4f-135">При наличии нескольких режимов поставки по строкам заказа на продажу будет использоваться шаблон по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="03e4f-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="03e4f-136">Шаблон по умолчанию — это шаблон, который сопоставляется с типом уведомления на странице **Профиль уведомлений по электронной почте Commerce**.</span><span class="sxs-lookup"><span data-stu-id="03e4f-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="03e4f-137">Если заказ на продажу имеет режим поставки, который не был настроен для настраиваемого шаблона электронной почты, будет использоваться шаблон электронной почты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="03e4f-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03e4f-138">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="03e4f-138">Additional resources</span></span>

[<span data-ttu-id="03e4f-139">Создание заказов центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="03e4f-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="03e4f-140">Изменение режима доставки в POS</span><span class="sxs-lookup"><span data-stu-id="03e4f-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]