---
title: Настройка профиля уведомлений по электронной почте
description: В этом разделе описывается, как создать профиль уведомления по электронной почте в Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555315"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="ccb2f-103">Настройка профиля уведомлений по электронной почте</span><span class="sxs-lookup"><span data-stu-id="ccb2f-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ccb2f-104">В этом разделе описывается, как создать профиль уведомления по электронной почте в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ccb2f-105">При создании каналов можно настроить профиль уведомлений по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="ccb2f-106">Таким образом, сообщения электронной почты могут отправляться клиентам для различных событий проводок, таких как создание заказа, статус доставки заказа и сбой оплаты.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="ccb2f-107">Дополнительные сведения о настройке электронной почты см. в разделе [Настройка и отправка сообщений электронной почты](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ccb2f-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="ccb2f-108">Создание профиля уведомлений по электронной почте</span><span class="sxs-lookup"><span data-stu-id="ccb2f-108">Create an email notification profile</span></span>

<span data-ttu-id="ccb2f-109">Чтобы создать профиль уведомлений по электронной почте, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="ccb2f-110">В области переходов выберите **Модули \> Retail и Commerce \> Настройка Headquarters \> Профиль уведомлений по электронной почте Commerce**.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="ccb2f-111">В области операций щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="ccb2f-112">В поле **Профиль уведомления по электронной почте** введите имя, определяющее профиль.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="ccb2f-113">В поле **Описание** введите соответствующее описание.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="ccb2f-114">Установите для переключателя **Активно** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="ccb2f-115">Создание шаблона сообщения эл. почты</span><span class="sxs-lookup"><span data-stu-id="ccb2f-115">Create an email template</span></span>

<span data-ttu-id="ccb2f-116">Прежде чем можно будет включить тип уведомления электронной почты, необходимо создать шаблон сообщения электронной почты организации в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="ccb2f-117">Этот шаблон определяет тему сообщения электронной почты, отправителя, язык по умолчанию и текст сообщения электронной почты для каждого языка, который требуется поддерживать.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="ccb2f-118">Чтобы создать шаблон электронной почты, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="ccb2f-119">В области переходов выберите **Модули \> Retail и Commerce \> Настройка Headquarters \> Параметры \> Шаблоны электронной почты организации**.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="ccb2f-120">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ccb2f-121">В поле **Код электронной почты** введите код, который идентифицирует этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="ccb2f-122">В поле **Имя отправителя** введите имя отправителя.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="ccb2f-123">В поле **Описание электронной почты** введите значимое описание.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="ccb2f-124">В **Электронная почта отправителя** введите адрес электронной почты отправителей.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="ccb2f-125">В разделе **Общие** выберите язык по умолчанию для шаблона сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="ccb2f-126">Язык по умолчанию будет использоваться, если для указанного языка не существует локализованного шаблона.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="ccb2f-127">Разверните раздел **Содержание сообщения электронной почты** и выберите **Создать**, чтобы создать содержимое шаблона.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="ccb2f-128">Для каждого элемента содержимого выберите язык и введите строку темы сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="ccb2f-129">Если сообщение электронной почты будет иметь тело, убедитесь, что установлен флажок **Имеется тело сообщения**.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="ccb2f-130">На панели операций выберите **Сообщение электронной почты**, чтобы предоставить шаблон тела сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="ccb2f-131">На следующем рисунке показан пример настроек шаблона электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-131">The following image shows some example email template settings.</span></span>

![Параметры шаблонов электронной почты](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="ccb2f-133">Создание события эл. почты</span><span class="sxs-lookup"><span data-stu-id="ccb2f-133">Create an email event</span></span>

<span data-ttu-id="ccb2f-134">Чтобы создать событие электронной почты, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="ccb2f-135">В области переходов выберите **Модули \> Retail и Commerce \> Настройка Headquarters \> Профиль уведомлений по электронной почте Commerce**.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="ccb2f-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="ccb2f-137">Выбор кода шаблона электронной почты из раскрывающегося списка **Код электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="ccb2f-138">Выберите подходящий **Тип уведомления по электронной почте** в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="ccb2f-139">Установите флажок **Активно**.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="ccb2f-140">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ccb2f-141">На следующем рисунке показан пример настроек уведомления по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-141">The following image shows some example event notification settings.</span></span>

![Параметры уведомлений о событии](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="ccb2f-143">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="ccb2f-143">Next steps</span></span>

<span data-ttu-id="ccb2f-144">Перед отправкой почты необходимо настроить службу исходящей почты и настроить пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="ccb2f-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="ccb2f-145">Дополнительные сведения см. в разделе [Настройка и отправка сообщений электронной почты](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ccb2f-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="ccb2f-146">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ccb2f-146">Additional resources</span></span>

[<span data-ttu-id="ccb2f-147">Настройка и отправка электронной почты</span><span class="sxs-lookup"><span data-stu-id="ccb2f-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ccb2f-148">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="ccb2f-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ccb2f-149">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="ccb2f-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ccb2f-150">Обзор организаций и организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="ccb2f-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
