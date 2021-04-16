---
title: Настройка дополнительных функций ознакомительной среды Dynamics 365 Commerce
description: В этой теме объясняется, как настроить дополнительные функции для ознакомительной среды Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6bc968c2659380bb8c92292ee19e3a7ec8a20a2b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795915"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="309bf-103">Настройка дополнительных функций среды оценки Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="309bf-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="309bf-104">В этой теме объясняется, как настроить дополнительные функции для ознакомительной среды Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="309bf-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="309bf-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="309bf-105">Prerequisites</span></span>

<span data-ttu-id="309bf-106">Если необходимо оценить возможности обработки электронной почты по проводкам, необходимо обеспечить соблюдение следующих условий:</span><span class="sxs-lookup"><span data-stu-id="309bf-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="309bf-107">Имеется доступный сервер электронной почты (Simple Mail Transfer Protocol, \[SMTP\]-сервер), который может использоваться в подписке Microsoft Azure, в которой пользователь подготовил ознакомительную среду.</span><span class="sxs-lookup"><span data-stu-id="309bf-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="309bf-108">Имеется полное доменное имя (FQDN)/IP-адрес сервера, номер порта SMTP и сведения об аутентификации.</span><span class="sxs-lookup"><span data-stu-id="309bf-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="309bf-109">Настройка серверной части изображений</span><span class="sxs-lookup"><span data-stu-id="309bf-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="309bf-110">Поиск базового URL-адреса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="309bf-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="309bf-111">Прежде чем вы сможете завершить эту процедуру, вы должны завершить шаги в разделе [Настройка сайта в Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="309bf-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="309bf-112">Войдите в конструктор сайтов Commerce, используя URL-адрес, который вы записали при инициализации электронной коммерции во время подготовки (см. [Инициализация электронной коммерции](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="309bf-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="309bf-113">Откройте сайт **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="309bf-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="309bf-114">Выберите **Библиотека мультимедиа** в меню слева.</span><span class="sxs-lookup"><span data-stu-id="309bf-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="309bf-115">Выберите любой один актив изображения.</span><span class="sxs-lookup"><span data-stu-id="309bf-115">Select any single image asset.</span></span>
1. <span data-ttu-id="309bf-116">В инспекторе свойств справа найдите свойство **Общедоступный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="309bf-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="309bf-117">Значение — это URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="309bf-117">The value is a URL.</span></span> <span data-ttu-id="309bf-118">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="309bf-118">Here is an example:</span></span>

    <span data-ttu-id="309bf-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="309bf-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="309bf-120">Замените последний идентификатор в URL-адресе (**MA1nQC** в предыдущем выше) следующей строкой: **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="309bf-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="309bf-121">Вот как выглядит URL-адрес примера после этого изменения:</span><span class="sxs-lookup"><span data-stu-id="309bf-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="309bf-122">Этот URL-адрес является базовым URL-адресом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="309bf-122">This URL is your media base URL.</span></span> <span data-ttu-id="309bf-123">Запишите его.</span><span class="sxs-lookup"><span data-stu-id="309bf-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="309bf-124">Обновление базового URL-адреса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="309bf-124">Update the media base URL</span></span>

1. <span data-ttu-id="309bf-125">Войдите в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="309bf-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="309bf-126">Используя меню в левой части, перейдите к пункту **Модули \> Retail и commerce \> Настройка канала \> Профили канала**.</span><span class="sxs-lookup"><span data-stu-id="309bf-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="309bf-127">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="309bf-127">Select **Edit**.</span></span>
1. <span data-ttu-id="309bf-128">В пункте **Свойства профиля** замените значение свойства для пункта **Базовый URL-адрес сервера мультимедиа** значением базового URL-адрес мультимедиа, созданным ранее.</span><span class="sxs-lookup"><span data-stu-id="309bf-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="309bf-129">Выберите канал с именем **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="309bf-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="309bf-130">В разделе **Свойства профиля** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="309bf-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="309bf-131">Для добавленного свойства выберите **Базовый URL-адрес сервера мультимедиа** в качестве ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="309bf-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="309bf-132">Как значение свойства введите базовый URL-адрес мультимедиа, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="309bf-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="309bf-133">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="309bf-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="309bf-134">Настройка и тестирование сервера электронной почты</span><span class="sxs-lookup"><span data-stu-id="309bf-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="309bf-135">Вводимый SMTP-сервер или служба электронной почты должны быть доступны в подписке Azure, используемой для среды.</span><span class="sxs-lookup"><span data-stu-id="309bf-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="309bf-136">Войдите в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="309bf-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="309bf-137">Используйте меню в левой части, чтобы перейти к пункту **Модули \> Retail and Commerce \> Настройка центрального офиса \> Параметры \> Параметры электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="309bf-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="309bf-138">На вкладке **Параметры SMTP** в поле **Сервер исходящей почты** введите FQDN или IP-адрес вашего сервера SMTP или службы электронной почты.</span><span class="sxs-lookup"><span data-stu-id="309bf-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="309bf-139">В поле **Номер порта SMTP** введите номер порта.</span><span class="sxs-lookup"><span data-stu-id="309bf-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="309bf-140">(Если вы не используете Secure Sockets Layer \[SSL\], номер порта по умолчанию **25**.)</span><span class="sxs-lookup"><span data-stu-id="309bf-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="309bf-141">Если требуется аутентификация, введите значения в полях **Имя пользователя** и **Пароль**.</span><span class="sxs-lookup"><span data-stu-id="309bf-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="309bf-142">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="309bf-142">Select **Save**.</span></span>
1. <span data-ttu-id="309bf-143">Выберите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="309bf-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="309bf-144">На вкладке **Тестовое сообщение электронной почты** в поле **Поставщик электронной почты** выберите **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="309bf-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="309bf-145">В поле **Кому отправить** введите адрес электронной почты, по которому необходимо доставить проверочное сообщение.</span><span class="sxs-lookup"><span data-stu-id="309bf-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="309bf-146">Выберите **Отправить тестовое сообщение электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="309bf-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="309bf-147">Настройка шаблонов электронной почты</span><span class="sxs-lookup"><span data-stu-id="309bf-147">Configure email templates</span></span>

<span data-ttu-id="309bf-148">Для каждого события, по которому необходимо отправить электронную почту, необходимо обновить шаблон электронной почты с помощью действительного адреса электронной почты отправителя.</span><span class="sxs-lookup"><span data-stu-id="309bf-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="309bf-149">Войдите в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="309bf-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="309bf-150">Используйте меню в левой части, чтобы перейти к пункту **Модули \> Retail and Commerce \> Настройка центрального офиса \> Параметры \> Шаблоны электронной почты организации**.</span><span class="sxs-lookup"><span data-stu-id="309bf-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="309bf-151">Выберите **Показать список**.</span><span class="sxs-lookup"><span data-stu-id="309bf-151">Select **Show list**.</span></span>
1. <span data-ttu-id="309bf-152">Для каждого шаблона в списке выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="309bf-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="309bf-153">В поле **Электронная почта отправителя** введите адрес электронной почты отправителя.</span><span class="sxs-lookup"><span data-stu-id="309bf-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="309bf-154">Дополнительно: в поле **Имя отправителя** введите имя, которое должно быть использовано в качестве имени отправителя.</span><span class="sxs-lookup"><span data-stu-id="309bf-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="309bf-155">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="309bf-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="309bf-156">Настройка шаблонов электронной почты</span><span class="sxs-lookup"><span data-stu-id="309bf-156">Customize email templates</span></span>

<span data-ttu-id="309bf-157">Возможно, вы захотите настроить шаблоны электронной почты таким образом, чтобы они использовали различные изображения.</span><span class="sxs-lookup"><span data-stu-id="309bf-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="309bf-158">Или вы можете обновить ссылки в шаблонах, чтобы они переходили к вашей ознакомительной среде.</span><span class="sxs-lookup"><span data-stu-id="309bf-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="309bf-159">В этой процедуре объясняется, как загрузить шаблоны по умолчанию, настроить их и обновить шаблоны в системе.</span><span class="sxs-lookup"><span data-stu-id="309bf-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="309bf-160">В веб-браузере загрузите [ZIP-файл шаблонов электронной почты по умолчанию для ознакомительной версии Microsoft Dynamics 365 Commerce](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="309bf-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="309bf-161">Этот файл содержит следующие HTML-документы:</span><span class="sxs-lookup"><span data-stu-id="309bf-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="309bf-162">Шаблон подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="309bf-162">Order confirmation template</span></span>
    - <span data-ttu-id="309bf-163">Шаблон выдачи подарочной карты</span><span class="sxs-lookup"><span data-stu-id="309bf-163">Issue gift card template</span></span>
    - <span data-ttu-id="309bf-164">Шаблон создания заказа</span><span class="sxs-lookup"><span data-stu-id="309bf-164">New order template</span></span>
    - <span data-ttu-id="309bf-165">Шаблон заказа на упаковку</span><span class="sxs-lookup"><span data-stu-id="309bf-165">Pack order template</span></span>
    - <span data-ttu-id="309bf-166">Шаблон заказа на комплектацию</span><span class="sxs-lookup"><span data-stu-id="309bf-166">Pick order template</span></span>

1. <span data-ttu-id="309bf-167">Настройте шаблоны с помощью текстового редактора или текста HTML.</span><span class="sxs-lookup"><span data-stu-id="309bf-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="309bf-168">См. список [поддерживаемых токенов](#supported-tokens-in-the-email-template) позже в этой теме.</span><span class="sxs-lookup"><span data-stu-id="309bf-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="309bf-169">Вход в Commerce.</span><span class="sxs-lookup"><span data-stu-id="309bf-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="309bf-170">Используя меню в левой части, перейдите к пункту **Модули \> Администрирование организации \> Настройка \> Шаблоны сообщений электронной почты организации**.</span><span class="sxs-lookup"><span data-stu-id="309bf-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="309bf-171">Разверните список слева, чтобы просмотреть все шаблоны.</span><span class="sxs-lookup"><span data-stu-id="309bf-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="309bf-172">Для каждого шаблона, который вы хотите настроить, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="309bf-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="309bf-173">Выберите шаблон из списка.</span><span class="sxs-lookup"><span data-stu-id="309bf-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="309bf-174">В разделе **Содержимое сообщения электронной почты** выберите нужную языковую версию из списка.</span><span class="sxs-lookup"><span data-stu-id="309bf-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="309bf-175">(Язык по умолчанию — **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="309bf-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="309bf-176">В **Содержимое сообщения электронной почты**, выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="309bf-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="309bf-177">Отображается панель **Отправка шаблона сообщения электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="309bf-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="309bf-178">Выберите **Обзор** и найдите HTML-файл с настраиваемым контентом.</span><span class="sxs-lookup"><span data-stu-id="309bf-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="309bf-179">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="309bf-179">Select **Upload**.</span></span> <span data-ttu-id="309bf-180">Шаблон отправляется в систему, и будет показан предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="309bf-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="309bf-181">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="309bf-181">Select **OK**.</span></span>
    1. <span data-ttu-id="309bf-182">Необязательно: настройте свойство **Тема** шаблона.</span><span class="sxs-lookup"><span data-stu-id="309bf-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="309bf-183">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="309bf-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="309bf-184">Поддерживаемые маркеры в шаблоне электронной почты</span><span class="sxs-lookup"><span data-stu-id="309bf-184">Supported tokens in the email template</span></span>

<span data-ttu-id="309bf-185">Эти токены будут заменены во время обработки электронной почты фактическими значениями, которые применяются к клиенту и его заказу.</span><span class="sxs-lookup"><span data-stu-id="309bf-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="309bf-186">Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="309bf-186">Sales order</span></span>

<span data-ttu-id="309bf-187">Следующие маркеры применяются ко всему заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="309bf-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="309bf-188">Наименование маркера</span><span class="sxs-lookup"><span data-stu-id="309bf-188">Name of the token</span></span> | <span data-ttu-id="309bf-189">Маркер</span><span class="sxs-lookup"><span data-stu-id="309bf-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="309bf-190">Порядковый номер</span><span class="sxs-lookup"><span data-stu-id="309bf-190">Order number</span></span>      | <span data-ttu-id="309bf-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="309bf-191">%salesid%</span></span> |
| <span data-ttu-id="309bf-192">Имя клиента</span><span class="sxs-lookup"><span data-stu-id="309bf-192">Customer's name</span></span>   | <span data-ttu-id="309bf-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="309bf-193">%customername%</span></span> |
| <span data-ttu-id="309bf-194">Адрес доставки</span><span class="sxs-lookup"><span data-stu-id="309bf-194">Delivery address</span></span>  | <span data-ttu-id="309bf-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="309bf-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="309bf-196">Адрес выставления счета</span><span class="sxs-lookup"><span data-stu-id="309bf-196">Billing address</span></span>   | <span data-ttu-id="309bf-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="309bf-197">%customeraddress%</span></span> |
| <span data-ttu-id="309bf-198">Кассовый ордер за дату</span><span class="sxs-lookup"><span data-stu-id="309bf-198">Order date</span></span>        | <span data-ttu-id="309bf-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="309bf-199">%shipdate%</span></span> |
| <span data-ttu-id="309bf-200">Способ поставки</span><span class="sxs-lookup"><span data-stu-id="309bf-200">Delivery mode</span></span>     | <span data-ttu-id="309bf-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="309bf-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="309bf-202">Скидка</span><span class="sxs-lookup"><span data-stu-id="309bf-202">Discount</span></span>          | <span data-ttu-id="309bf-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="309bf-203">%discount%</span></span> |
| <span data-ttu-id="309bf-204">Налог</span><span class="sxs-lookup"><span data-stu-id="309bf-204">Sales tax</span></span>         | <span data-ttu-id="309bf-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="309bf-205">%tax%</span></span> |
| <span data-ttu-id="309bf-206">Итог по заказу</span><span class="sxs-lookup"><span data-stu-id="309bf-206">Order total</span></span>       | <span data-ttu-id="309bf-207">%total%</span><span class="sxs-lookup"><span data-stu-id="309bf-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="309bf-208">Строка продаж</span><span class="sxs-lookup"><span data-stu-id="309bf-208">Sales line</span></span>

<span data-ttu-id="309bf-209">Следующие маркеры заменяются значениями для каждого продукта в заказе.</span><span class="sxs-lookup"><span data-stu-id="309bf-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="309bf-210">Поместите токен **Список продуктов — начало** в начало HTML-блока, который повторяется для каждого продукта, и поместите токен **Список продуктов — конец** в конец блока.</span><span class="sxs-lookup"><span data-stu-id="309bf-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="309bf-211">Наименование маркера</span><span class="sxs-lookup"><span data-stu-id="309bf-211">Name of the token</span></span>      | <span data-ttu-id="309bf-212">Маркер</span><span class="sxs-lookup"><span data-stu-id="309bf-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="309bf-213">Список продуктов — начало</span><span class="sxs-lookup"><span data-stu-id="309bf-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="309bf-214">Список продуктов — конец</span><span class="sxs-lookup"><span data-stu-id="309bf-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="309bf-215">Наименование продукта:</span><span class="sxs-lookup"><span data-stu-id="309bf-215">Product name</span></span>           | <span data-ttu-id="309bf-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="309bf-216">%lineproductname%</span></span> |
| <span data-ttu-id="309bf-217">описание</span><span class="sxs-lookup"><span data-stu-id="309bf-217">Description</span></span>            | <span data-ttu-id="309bf-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="309bf-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="309bf-219">Количество</span><span class="sxs-lookup"><span data-stu-id="309bf-219">Quantity</span></span>               | <span data-ttu-id="309bf-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="309bf-220">%linequantity%</span></span> |
| <span data-ttu-id="309bf-221">Цена за единицу в строке</span><span class="sxs-lookup"><span data-stu-id="309bf-221">Line unit price</span></span>        | <span data-ttu-id="309bf-222">%lineprice% (проверить)</span><span class="sxs-lookup"><span data-stu-id="309bf-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="309bf-223">Итого по номенклатуре строки</span><span class="sxs-lookup"><span data-stu-id="309bf-223">line item total</span></span>        | <span data-ttu-id="309bf-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="309bf-224">%linenetamount%</span></span> |
| <span data-ttu-id="309bf-225">скидка по строке</span><span class="sxs-lookup"><span data-stu-id="309bf-225">line discount</span></span>          | <span data-ttu-id="309bf-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="309bf-226">%linediscount%</span></span> |
| <span data-ttu-id="309bf-227">Дата отгрузки</span><span class="sxs-lookup"><span data-stu-id="309bf-227">Ship date</span></span>              | <span data-ttu-id="309bf-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="309bf-228">%lineshipdate%</span></span> |
| <span data-ttu-id="309bf-229">Способ закупки</span><span class="sxs-lookup"><span data-stu-id="309bf-229">Procurement method</span></span>     | <span data-ttu-id="309bf-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="309bf-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="309bf-231">адрес поставки</span><span class="sxs-lookup"><span data-stu-id="309bf-231">delivery address</span></span>       | <span data-ttu-id="309bf-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="309bf-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="309bf-233">Единица измерения продаж для строки</span><span class="sxs-lookup"><span data-stu-id="309bf-233">Sales unit of the line</span></span> | <span data-ttu-id="309bf-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="309bf-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="309bf-235">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="309bf-235">Additional resources</span></span>

[<span data-ttu-id="309bf-236">Обзор ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="309bf-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="309bf-237">Подготовка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="309bf-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="309bf-238">Настройка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="309bf-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="309bf-239">Настройка BOPIS в ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="309bf-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="309bf-240">Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="309bf-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="309bf-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="309bf-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="309bf-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="309bf-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="309bf-243">Портал Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="309bf-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="309bf-244">Веб-сайт Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="309bf-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]