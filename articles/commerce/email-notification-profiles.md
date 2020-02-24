---
title: Настройка профиля уведомлений по электронной почте
description: В этом разделе описывается, как создать профиль уведомления по электронной почте в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: feb28b9c801786f63282c4189d3eeb6d53ed07e1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003150"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="fd6dc-103">Настройка профиля уведомлений по электронной почте</span><span class="sxs-lookup"><span data-stu-id="fd6dc-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fd6dc-104">В этом разделе описывается, как создать профиль уведомления по электронной почте в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fd6dc-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="fd6dc-105">Overview</span></span>

<span data-ttu-id="fd6dc-106">Перед созданием каналов необходимо настроить профиль, чтобы гарантировать, что уведомления электронной почты могут быть отправлены для различных событий, таких как создание заказа, статус доставки заказа и сбой оплаты.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="fd6dc-107">Дополнительные сведения о настройке электронной почты см. в разделе [Настройка и отправка сообщений электронной почты](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span><span class="sxs-lookup"><span data-stu-id="fd6dc-107">For additional email configuration information, see [Configure and send email](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="fd6dc-108">Создание профиля уведомлений по электронной почте</span><span class="sxs-lookup"><span data-stu-id="fd6dc-108">Create an email notification profile</span></span>

<span data-ttu-id="fd6dc-109">Чтобы создать профиль уведомлений по электронной почте, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="fd6dc-110">В области переходов выберите **Модули \> Retail и Commerce \> Настройка Headquarters \> Профиль уведомлений по электронной почте Retail**.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Retail Email notification profile**.</span></span>
1. <span data-ttu-id="fd6dc-111">В области операций щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="fd6dc-112">В поле **Профиль уведомления по электронной почте** введите имя, определяющее профиль.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="fd6dc-113">В поле **Описание** введите соответствующее описание.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="fd6dc-114">Установите для переключателя **Активно** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="fd6dc-115">Создание шаблона сообщения эл. почты</span><span class="sxs-lookup"><span data-stu-id="fd6dc-115">Create an email template</span></span>

<span data-ttu-id="fd6dc-116">Прежде чем можно будет создать уведомление по электронной почте, необходимо создать шаблон электронной почты организации, содержащий сведения об электронной почте отправителей и шаблон электронной почты.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="fd6dc-117">Чтобы создать шаблон электронной почты, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="fd6dc-118">В области переходов выберите **Модули \> Retail и Commerce \> Настройка Headquarters \> Параметры \> Шаблоны электронной почты организации**.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="fd6dc-119">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fd6dc-120">В поле **Код электронной почты** введите код, который идентифицирует этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="fd6dc-121">В поле **Имя отправителя** введите имя отправителя.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="fd6dc-122">В поле **Описание электронной почты** введите значимое описание.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="fd6dc-123">В **Электронная почта отправителя** введите адрес электронной почты отправителей.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="fd6dc-124">В разделе **Общие** внесите все необязательные сведения (например, приоритет электронной почты).</span><span class="sxs-lookup"><span data-stu-id="fd6dc-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="fd6dc-125">Разверните раздел **Содержание сообщения электронной почты** и выберите **Создать**, чтобы создать содержимое шаблона.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="fd6dc-126">Для каждого элемента содержимого выберите язык и введите строку темы сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="fd6dc-127">Если сообщение электронной почты будет иметь тело, убедитесь, что установлен флажок **Имеется тело сообщения**.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="fd6dc-128">На панели операций выберите **Сообщение электронной почты**, чтобы предоставить шаблон тела сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="fd6dc-129">На следующем рисунке показан пример настроек шаблона электронной почты.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-129">The following image shows some example email template settings.</span></span>

![Параметры шаблонов электронной почты](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="fd6dc-131">Создание события эл. почты</span><span class="sxs-lookup"><span data-stu-id="fd6dc-131">Create an email event</span></span>

<span data-ttu-id="fd6dc-132">Чтобы создать событие электронной почты, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="fd6dc-133">В области переходов выберите **Модули \> Retail и Commerce \> Настройка Headquarters \> Профиль уведомлений по электронной почте Retail**.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Retail Email notification profile**.</span></span>
1. <span data-ttu-id="fd6dc-134">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="fd6dc-135">Выбор кода шаблона электронной почты из раскрывающегося списка **Код электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="fd6dc-136">Выберите подходящий **Тип уведомления по электронной почте** в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="fd6dc-137">Установите флажок **Активно**.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="fd6dc-138">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="fd6dc-139">На следующем рисунке показан пример настроек уведомления по электронной почте для Retail.</span><span class="sxs-lookup"><span data-stu-id="fd6dc-139">The following image shows some example retail event notification settings.</span></span>

![Параметры уведомлений о событии розничной торговли](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="fd6dc-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fd6dc-141">Additional resources</span></span>

[<span data-ttu-id="fd6dc-142">Настройка и отправка электронной почты</span><span class="sxs-lookup"><span data-stu-id="fd6dc-142">Configure and send email</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email)

[<span data-ttu-id="fd6dc-143">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="fd6dc-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="fd6dc-144">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="fd6dc-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="fd6dc-145">Обзор организаций и организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="fd6dc-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
