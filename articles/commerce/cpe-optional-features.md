---
title: Настройка дополнительных функций среды предварительной версии Dynamics 365 Commerce
description: В этой теме объясняется, как настроить дополнительные функции для среды предварительного просмотра Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b17f8e9b0d8a9a62714d0073561e66642b2eaf9
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057748"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="20bf2-103">Настройка дополнительных функций среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="20bf2-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="20bf2-104">В этой теме объясняется, как настроить дополнительные функции для среды предварительного просмотра Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="20bf2-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="20bf2-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="20bf2-105">Prerequisites</span></span>

<span data-ttu-id="20bf2-106">Если необходимо оценить возможности обработки электронной почты по проводкам, необходимо обеспечить соблюдение следующих условий:</span><span class="sxs-lookup"><span data-stu-id="20bf2-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="20bf2-107">Имеется доступный сервер электронной почты (Simple Mail Transfer Protocol, \[SMTP\]-сервер), который может использоваться в подписке Microsoft Azure, в которой пользователь подготовил среду предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="20bf2-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="20bf2-108">Имеется полное доменное имя (FQDN)/IP-адрес сервера, номер порта SMTP и сведения об аутентификации.</span><span class="sxs-lookup"><span data-stu-id="20bf2-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="20bf2-109">Если вы хотите оценить функции управления цифровыми активами, получив новые изображения многоканального взаимодействия, у вас должно быть имя клиента своей системы управления контентом (CMS).</span><span class="sxs-lookup"><span data-stu-id="20bf2-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="20bf2-110">Инструкции по поиску этого имени приведены позже в этой теме.</span><span class="sxs-lookup"><span data-stu-id="20bf2-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="20bf2-111">>>>(В: где найти инструкции?)</span><span class="sxs-lookup"><span data-stu-id="20bf2-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="20bf2-112">Настройка серверной части изображений</span><span class="sxs-lookup"><span data-stu-id="20bf2-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="20bf2-113">Поиск базового URL-адреса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="20bf2-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="20bf2-114">Прежде чем вы сможете завершить эту процедуру, вы должны завершить шаги в разделе [Настройка сайта в Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="20bf2-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="20bf2-115">Войдите в инструмент управления сайтом Commerce, используя URL-адрес, который вы записали при инициализации электронной коммерции во время подготовки (см. [Инициализация электронной коммерции](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="20bf2-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="20bf2-116">Откройте сайт **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="20bf2-117">Выберите **Активы** в меню слева.</span><span class="sxs-lookup"><span data-stu-id="20bf2-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="20bf2-118">Выберите любой один актив изображения.</span><span class="sxs-lookup"><span data-stu-id="20bf2-118">Select any single image asset.</span></span>
1. <span data-ttu-id="20bf2-119">В инспекторе свойств справа найдите свойство **Общедоступный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="20bf2-120">Значение — это URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="20bf2-120">The value is a URL.</span></span> <span data-ttu-id="20bf2-121">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="20bf2-121">Here is an example:</span></span>

    <span data-ttu-id="20bf2-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="20bf2-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="20bf2-123">Замените последний идентификатор в URL-адресе (**MA1nQC** в предыдущем выше) следующей строкой: **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="20bf2-124">Вот как выглядит URL-адрес примера после этого изменения:</span><span class="sxs-lookup"><span data-stu-id="20bf2-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="20bf2-125">Этот URL-адрес является базовым URL-адресом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="20bf2-125">This URL is your media base URL.</span></span> <span data-ttu-id="20bf2-126">Запишите его.</span><span class="sxs-lookup"><span data-stu-id="20bf2-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="20bf2-127">Обновление базового URL-адреса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="20bf2-127">Update the media base URL</span></span>

1. <span data-ttu-id="20bf2-128">Войдите в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="20bf2-128">Sign in to Dynamics 365 Commerce.</span></span>
1. <span data-ttu-id="20bf2-129">Используя меню в левой части, перейдите к пункту **Модули \> Retail и commerce \> Настройка канала \> Профили канала**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-129">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="20bf2-130">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-130">Select **Edit**.</span></span>
1. <span data-ttu-id="20bf2-131">В пункте **Свойства профиля** замените значение свойства для пункта **Базовый URL-адрес сервера мультимедиа** значением базового URL-адрес мультимедиа, созданным ранее.</span><span class="sxs-lookup"><span data-stu-id="20bf2-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="20bf2-132">Выберите другой канал из списка слева в области канала **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="20bf2-133">В разделе **Свойства профиля** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="20bf2-134">Для добавленного свойства выберите **Базовый URL-адрес сервера мультимедиа** в качестве ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="20bf2-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="20bf2-135">Как значение свойства введите базовый URL-адрес мультимедиа, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="20bf2-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="20bf2-136">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="20bf2-137">Настройка сервера электронной почты</span><span class="sxs-lookup"><span data-stu-id="20bf2-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="20bf2-138">Вводимый SMTP-сервер или служба электронной почты должны быть доступны в подписке Azure, используемой для среды.</span><span class="sxs-lookup"><span data-stu-id="20bf2-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="20bf2-139">Вход в Commerce.</span><span class="sxs-lookup"><span data-stu-id="20bf2-139">Sign in to Commerce.</span></span>
1. <span data-ttu-id="20bf2-140">Используя меню в левой части, перейдите к пункту **Модули \> Администрирование системы \> Настройка \> Эл. почта \> Параметры электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="20bf2-141">На вкладке **Параметры SMTP** в поле **Сервер исходящей почты** введите FQDN или IP-адрес вашего сервера SMTP или службы электронной почты.</span><span class="sxs-lookup"><span data-stu-id="20bf2-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="20bf2-142">В поле **Номер порта SMTP** введите номер порта.</span><span class="sxs-lookup"><span data-stu-id="20bf2-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="20bf2-143">(Если вы не используете Secure Sockets Layer \[SSL\], номер порта по умолчанию **25**.)</span><span class="sxs-lookup"><span data-stu-id="20bf2-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="20bf2-144">Если требуется аутентификация, введите значения в полях **Имя пользователя** и **Пароль**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="20bf2-145">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-145">Select **Save**.</span></span>
1. <span data-ttu-id="20bf2-146">Выберите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="20bf2-147">На вкладке **Тестовое сообщение электронной почты** в поле **Поставщик электронной почты** выберите **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="20bf2-148">В поле **Кому отправить** введите адрес электронной почты, по которому необходимо доставить проверочное сообщение.</span><span class="sxs-lookup"><span data-stu-id="20bf2-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="20bf2-149">Выберите **Отправить тестовое сообщение электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="20bf2-150">Настройка шаблонов электронной почты</span><span class="sxs-lookup"><span data-stu-id="20bf2-150">Configure email templates</span></span>

<span data-ttu-id="20bf2-151">Для каждого события, по которому необходимо отправить электронную почту, необходимо обновить шаблон электронной почты с помощью действительного адреса электронной почты отправителя.</span><span class="sxs-lookup"><span data-stu-id="20bf2-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="20bf2-152">Вход в Commerce.</span><span class="sxs-lookup"><span data-stu-id="20bf2-152">Sign in to Commerce.</span></span>
1. <span data-ttu-id="20bf2-153">Используя меню в левой части, перейдите к пункту **Модули \> Администрирование организации \> Настройка \> Шаблоны сообщений электронной почты организации**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="20bf2-154">Выберите **Показать список**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-154">Select **Show list**.</span></span>
1. <span data-ttu-id="20bf2-155">Для каждого шаблона в списке выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="20bf2-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="20bf2-156">В поле **Электронная почта отправителя** введите адрес электронной почты отправителя.</span><span class="sxs-lookup"><span data-stu-id="20bf2-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="20bf2-157">Дополнительно: в поле **Имя отправителя** введите имя, которое должно быть использовано в качестве имени отправителя.</span><span class="sxs-lookup"><span data-stu-id="20bf2-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="20bf2-158">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="20bf2-159">Настройка шаблонов электронной почты</span><span class="sxs-lookup"><span data-stu-id="20bf2-159">Customize email templates</span></span>

<span data-ttu-id="20bf2-160">Возможно, вы захотите настроить шаблоны электронной почты таким образом, чтобы они использовали различные изображения.</span><span class="sxs-lookup"><span data-stu-id="20bf2-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="20bf2-161">Или вы можете обновить ссылки в шаблонах, чтобы они переходили к вашей среде предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="20bf2-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="20bf2-162">В этой процедуре объясняется, как загрузить шаблоны по умолчанию, настроить их и обновить шаблоны в системе.</span><span class="sxs-lookup"><span data-stu-id="20bf2-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="20bf2-163">В веб-браузере загрузите [ZIP-файл шаблонов электронной почты по умолчанию для предварительной версии Microsoft Dynamics 365 Commerce](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="20bf2-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="20bf2-164">Этот файл содержит следующие HTML-документы:</span><span class="sxs-lookup"><span data-stu-id="20bf2-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="20bf2-165">Шаблон подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="20bf2-165">Order confirmation template</span></span>
    - <span data-ttu-id="20bf2-166">Шаблон выдачи подарочной карты</span><span class="sxs-lookup"><span data-stu-id="20bf2-166">Issue gift card template</span></span>
    - <span data-ttu-id="20bf2-167">Шаблон создания заказа</span><span class="sxs-lookup"><span data-stu-id="20bf2-167">New order template</span></span>
    - <span data-ttu-id="20bf2-168">Шаблон заказа на упаковку</span><span class="sxs-lookup"><span data-stu-id="20bf2-168">Pack order template</span></span>
    - <span data-ttu-id="20bf2-169">Шаблон заказа на комплектацию</span><span class="sxs-lookup"><span data-stu-id="20bf2-169">Pick order template</span></span>

1. <span data-ttu-id="20bf2-170">Настройте шаблоны с помощью текстового редактора или текста HTML.</span><span class="sxs-lookup"><span data-stu-id="20bf2-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="20bf2-171">См. список [поддерживаемых токенов](#supported-tokens-in-the-email-template) позже в этой теме.</span><span class="sxs-lookup"><span data-stu-id="20bf2-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="20bf2-172">Вход в Commerce.</span><span class="sxs-lookup"><span data-stu-id="20bf2-172">Sign in to Commerce.</span></span>
1. <span data-ttu-id="20bf2-173">Используя меню в левой части, перейдите к пункту **Модули \> Администрирование организации \> Настройка \> Шаблоны сообщений электронной почты организации**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="20bf2-174">Разверните список слева, чтобы просмотреть все шаблоны.</span><span class="sxs-lookup"><span data-stu-id="20bf2-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="20bf2-175">Для каждого шаблона, который вы хотите настроить, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="20bf2-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="20bf2-176">Выберите шаблон из списка.</span><span class="sxs-lookup"><span data-stu-id="20bf2-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="20bf2-177">В разделе **Содержимое сообщения электронной почты** выберите нужную языковую версию из списка.</span><span class="sxs-lookup"><span data-stu-id="20bf2-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="20bf2-178">(Язык по умолчанию — **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="20bf2-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="20bf2-179">В **Содержимое сообщения электронной почты**, выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="20bf2-180">Отображается панель **Отправка шаблона сообщения электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="20bf2-181">Выберите **Обзор** и найдите HTML-файл с настраиваемым контентом.</span><span class="sxs-lookup"><span data-stu-id="20bf2-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="20bf2-182">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-182">Select **Upload**.</span></span> <span data-ttu-id="20bf2-183">Шаблон отправляется в систему, и будет показан предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="20bf2-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="20bf2-184">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-184">Select **OK**.</span></span>
    1. <span data-ttu-id="20bf2-185">Необязательно: настройте свойство **Тема** шаблона.</span><span class="sxs-lookup"><span data-stu-id="20bf2-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="20bf2-186">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="20bf2-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="20bf2-187">Поддерживаемые маркеры в шаблоне электронной почты</span><span class="sxs-lookup"><span data-stu-id="20bf2-187">Supported tokens in the email template</span></span>

<span data-ttu-id="20bf2-188">Эти токены будут заменены во время обработки электронной почты фактическими значениями, которые применяются к клиенту и его заказу.</span><span class="sxs-lookup"><span data-stu-id="20bf2-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="20bf2-189">Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="20bf2-189">Sales order</span></span>

<span data-ttu-id="20bf2-190">Следующие маркеры применяются ко всему заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="20bf2-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="20bf2-191">Наименование маркера</span><span class="sxs-lookup"><span data-stu-id="20bf2-191">Name of the token</span></span> | <span data-ttu-id="20bf2-192">Маркер</span><span class="sxs-lookup"><span data-stu-id="20bf2-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="20bf2-193">Номер приказа</span><span class="sxs-lookup"><span data-stu-id="20bf2-193">Order number</span></span>      | <span data-ttu-id="20bf2-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="20bf2-194">%salesid%</span></span> |
| <span data-ttu-id="20bf2-195">Имя клиента</span><span class="sxs-lookup"><span data-stu-id="20bf2-195">Customer's name</span></span>   | <span data-ttu-id="20bf2-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="20bf2-196">%customername%</span></span> |
| <span data-ttu-id="20bf2-197">Адрес поставки</span><span class="sxs-lookup"><span data-stu-id="20bf2-197">Delivery address</span></span>  | <span data-ttu-id="20bf2-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="20bf2-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="20bf2-199">Адрес выставления счета</span><span class="sxs-lookup"><span data-stu-id="20bf2-199">Billing address</span></span>   | <span data-ttu-id="20bf2-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="20bf2-200">%customeraddress%</span></span> |
| <span data-ttu-id="20bf2-201">Дата заказа</span><span class="sxs-lookup"><span data-stu-id="20bf2-201">Order date</span></span>        | <span data-ttu-id="20bf2-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="20bf2-202">%shipdate%</span></span> |
| <span data-ttu-id="20bf2-203">Способ поставки</span><span class="sxs-lookup"><span data-stu-id="20bf2-203">Delivery mode</span></span>     | <span data-ttu-id="20bf2-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="20bf2-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="20bf2-205">Скидка</span><span class="sxs-lookup"><span data-stu-id="20bf2-205">Discount</span></span>          | <span data-ttu-id="20bf2-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="20bf2-206">%discount%</span></span> |
| <span data-ttu-id="20bf2-207">Налог</span><span class="sxs-lookup"><span data-stu-id="20bf2-207">Sales tax</span></span>         | <span data-ttu-id="20bf2-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="20bf2-208">%tax%</span></span> |
| <span data-ttu-id="20bf2-209">Итог по заказу</span><span class="sxs-lookup"><span data-stu-id="20bf2-209">Order total</span></span>       | <span data-ttu-id="20bf2-210">%total%</span><span class="sxs-lookup"><span data-stu-id="20bf2-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="20bf2-211">Строка продажи</span><span class="sxs-lookup"><span data-stu-id="20bf2-211">Sales line</span></span>

<span data-ttu-id="20bf2-212">Следующие маркеры заменяются значениями для каждого продукта в заказе.</span><span class="sxs-lookup"><span data-stu-id="20bf2-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="20bf2-213">Поместите токен **Список продуктов — начало** в начало HTML-блока, который повторяется для каждого продукта, и поместите токен **Список продуктов — конец** в конец блока.</span><span class="sxs-lookup"><span data-stu-id="20bf2-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="20bf2-214">Наименование маркера</span><span class="sxs-lookup"><span data-stu-id="20bf2-214">Name of the token</span></span>      | <span data-ttu-id="20bf2-215">Маркер</span><span class="sxs-lookup"><span data-stu-id="20bf2-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="20bf2-216">Список продуктов — начало</span><span class="sxs-lookup"><span data-stu-id="20bf2-216">Product list - start</span></span>   | <span data-ttu-id="20bf2-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="20bf2-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="20bf2-218">Список продуктов — конец</span><span class="sxs-lookup"><span data-stu-id="20bf2-218">Product list - end</span></span>     | <span data-ttu-id="20bf2-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="20bf2-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="20bf2-220">Наименование продукта</span><span class="sxs-lookup"><span data-stu-id="20bf2-220">Product name</span></span>           | <span data-ttu-id="20bf2-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="20bf2-221">%lineproductname%</span></span> |
| <span data-ttu-id="20bf2-222">Описание</span><span class="sxs-lookup"><span data-stu-id="20bf2-222">Description</span></span>            | <span data-ttu-id="20bf2-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="20bf2-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="20bf2-224">Количество</span><span class="sxs-lookup"><span data-stu-id="20bf2-224">Quantity</span></span>               | <span data-ttu-id="20bf2-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="20bf2-225">%linequantity%</span></span> |
| <span data-ttu-id="20bf2-226">Цена за единицу в строке</span><span class="sxs-lookup"><span data-stu-id="20bf2-226">Line unit price</span></span>        | <span data-ttu-id="20bf2-227">%lineprice% (verify)</span><span class="sxs-lookup"><span data-stu-id="20bf2-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="20bf2-228">Итого по номенклатуре строки</span><span class="sxs-lookup"><span data-stu-id="20bf2-228">line item total</span></span>        | <span data-ttu-id="20bf2-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="20bf2-229">%linenetamount%</span></span> |
| <span data-ttu-id="20bf2-230">скидка по строке</span><span class="sxs-lookup"><span data-stu-id="20bf2-230">line discount</span></span>          | <span data-ttu-id="20bf2-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="20bf2-231">%linediscount%</span></span> |
| <span data-ttu-id="20bf2-232">Дата отгрузки</span><span class="sxs-lookup"><span data-stu-id="20bf2-232">Ship date</span></span>              | <span data-ttu-id="20bf2-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="20bf2-233">%lineshipdate%</span></span> |
| <span data-ttu-id="20bf2-234">Способ закупки</span><span class="sxs-lookup"><span data-stu-id="20bf2-234">Procurement method</span></span>     | <span data-ttu-id="20bf2-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="20bf2-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="20bf2-236">адрес поставки</span><span class="sxs-lookup"><span data-stu-id="20bf2-236">delivery address</span></span>       | <span data-ttu-id="20bf2-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="20bf2-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="20bf2-238">Единица измерения продаж для строки</span><span class="sxs-lookup"><span data-stu-id="20bf2-238">Sales unit of the line</span></span> | <span data-ttu-id="20bf2-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="20bf2-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="20bf2-240">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="20bf2-240">Additional resources</span></span>

[<span data-ttu-id="20bf2-241">Обзор среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="20bf2-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="20bf2-242">Обеспечение среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="20bf2-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="20bf2-243">Настройка среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="20bf2-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="20bf2-244">Вопросы и ответы по среде предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="20bf2-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="20bf2-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="20bf2-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="20bf2-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="20bf2-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="20bf2-247">Портал Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="20bf2-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="20bf2-248">Веб-сайт Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="20bf2-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
