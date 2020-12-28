---
title: Настройка параметров электронной почты в Attract
description: В этой теме объясняется, как задать настройки для сообщений электронной почты, которые отправляется Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: e641e3f0d1873d91be1a1dc9bc22eb734a2b21d5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462322"
---
# <a name="configure-email-settings-in-attract"></a><span data-ttu-id="6423e-103">Настройка параметров электронной почты в Attract</span><span class="sxs-lookup"><span data-stu-id="6423e-103">Configure email settings in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6423e-104">Ваша торговая марка устанавливает доверие и помогает создать отношения с кандидатами еще до того, как они подадут заявление на ваши вакансии.</span><span class="sxs-lookup"><span data-stu-id="6423e-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="6423e-105">Положительное впечатление от торговой марки привлекает лучшие кадры и увеличивает лояльность существующих сотрудников.</span><span class="sxs-lookup"><span data-stu-id="6423e-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="6423e-106">Microsoft Dynamics 365 Talent: Attract позволяет настроить сообщения электронной почты, чтобы они соответствовали торговой марке компании.</span><span class="sxs-lookup"><span data-stu-id="6423e-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="6423e-107">Таким образом, можно обеспечить согласованное взаимодействие с кандидатами на должности в процессе обработки заявлений.</span><span class="sxs-lookup"><span data-stu-id="6423e-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="6423e-108">С помощью Attract можно выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6423e-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="6423e-109">Настройте параметры сообщений электронной почты таким образом, чтобы использовалась учетная запись службы электронной почты Microsoft Exchange компании.</span><span class="sxs-lookup"><span data-stu-id="6423e-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="6423e-110">Таким образом кандидаты знают, что сообщения электронной почты поступают от компании.</span><span class="sxs-lookup"><span data-stu-id="6423e-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="6423e-111">Например, можно задать настройки таким образом, чтобы кандидаты получали сообщения электронной почты с адреса `recruiting@contoso.com`, а не с адреса `contoso@microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="6423e-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="6423e-112">Создайте согласованный фирменный стиль для всех сообщений электронной почты, задав глобальный верхний и нижний колонтитулы для шаблонов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6423e-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="6423e-113">Чтобы настроить Attract, чтобы использовать учетную запись службы электронной почты компании для отправки сообщений электронной почты, необходима надстройка Comprehensive hiring.</span><span class="sxs-lookup"><span data-stu-id="6423e-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="6423e-114">Подключение учетной записи службы электронной почты</span><span class="sxs-lookup"><span data-stu-id="6423e-114">Connect an email service account</span></span>

<span data-ttu-id="6423e-115">Путем подключения учетной записи службы электронной почты компании можно создать фирменное взаимодействие по электронной почте для ваших кандидатов на работу.</span><span class="sxs-lookup"><span data-stu-id="6423e-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="6423e-116">Если вы не подключаете учетную запись компании, в Attract используется учетная запись службы электронной почты Майкрософт по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6423e-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="6423e-117">Выберите **Параметры** (символ шестеренки в верхнем правом углу), затем выберите **Центр администрирования**.</span><span class="sxs-lookup"><span data-stu-id="6423e-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="6423e-118">На вкладке **Параметры электронной почты** в разделе **Учетные записи службы электронной почты** выберите **Подключить учетную запись компании**.</span><span class="sxs-lookup"><span data-stu-id="6423e-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![Подключение учетной записи службы электронной почты компании в Attract](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="6423e-120">Дополнительные сведения о создании общей учетной записи электронной почты см. в разделе [Общие почтовые ящики в Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="6423e-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="6423e-121">В окне входа в Microsoft выполните вход, используя учетные данные вашей организации.</span><span class="sxs-lookup"><span data-stu-id="6423e-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="6423e-122">Если вы еще не настроили учетную запись службы электронной почты или хотите добавить новую, выберите **Добавить новую учетную запись службы**, затем введите данные электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6423e-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="6423e-123">Если вы уже настроили учетную запись службы электронной почты, которую вы хотите использовать, выберите ее.</span><span class="sxs-lookup"><span data-stu-id="6423e-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="6423e-124">Когда учетная запись службы электронной почты успешно настроена, она отображается в списке **Учетные записи службы электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="6423e-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="6423e-125">Отключение учетной записи службы электронной почты</span><span class="sxs-lookup"><span data-stu-id="6423e-125">Disconnect an email service account</span></span>

<span data-ttu-id="6423e-126">Если требуется прекратить использование домена компании в сообщениях электронной почты в Attract, можно отключить учетную запись службы электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6423e-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="6423e-127">Выберите **Параметры** (символ шестеренки в верхнем правом углу), затем выберите **Центр администрирования**.</span><span class="sxs-lookup"><span data-stu-id="6423e-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="6423e-128">На вкладке **Параметры электронной почты** в разделе **Учетные записи службы электронной почты** нажмите кнопку **Дополнительно** (три вертикальные точки) рядом с учетной записью службы электронной почты, которую необходимо отключить.</span><span class="sxs-lookup"><span data-stu-id="6423e-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="6423e-129">Выберите **Отключить учетную запись электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="6423e-129">Select **Disconnect email account**.</span></span>

    ![Отключение учетной записи службы электронной почты компании](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="6423e-131">При появлении запроса на подтверждение операции выберите **Отключить.**</span><span class="sxs-lookup"><span data-stu-id="6423e-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Подтверждение отключения учетной записи службы электронной почты компании](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="6423e-133">Если вы не подключили другую учетную запись службы электронной почты, письма, отправленные из Attract, будут использовать учетную запись службы электронной почты Майкрософт по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6423e-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="6423e-134">Настройка параметров шаблонов электронной почты</span><span class="sxs-lookup"><span data-stu-id="6423e-134">Configure email template settings</span></span>

<span data-ttu-id="6423e-135">Вы можете отправить изображение эмблемы компании и другую информацию в виде фирменного заголовка для своих сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6423e-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="6423e-136">Можно также предоставить ссылки на политику конфиденциальности и условия использования в нижних колонтитулах сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6423e-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="6423e-137">Вы должны соблюдать все действующее законодательство своей страны или региона, а также законодательство страны или региона получателя сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6423e-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="6423e-138">Эти законы включают в себя правила защиты от нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="6423e-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="6423e-139">Выберите **Параметры** (символ шестеренки в верхнем правом углу), затем выберите **Центр администрирования**.</span><span class="sxs-lookup"><span data-stu-id="6423e-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="6423e-140">На вкладке **Параметры электронной почты** в разделе **Параметры шаблонов электронной почты** перетащите изображение, которое требуется использовать в качестве заголовка электронной почты, в поле изображения, или щелкните в поле изображения, чтобы найти файл.</span><span class="sxs-lookup"><span data-stu-id="6423e-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="6423e-141">Чтобы заменить существующее изображение, необходимо сначала выбрать **Удалить** рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="6423e-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="6423e-142">Изображение должно быть файлом JPEG, JPG, PNG или SVG.</span><span class="sxs-lookup"><span data-stu-id="6423e-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="6423e-143">Рекомендуемый размер для изображений составляет от 25 до 800 пикселей в ширину, и от 25 до 150 пикселей в высоту.</span><span class="sxs-lookup"><span data-stu-id="6423e-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="6423e-144">Максимальный размер файла для заголовка — 1 мегабайт (МБ).</span><span class="sxs-lookup"><span data-stu-id="6423e-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Добавление изображения для заголовка сообщений электронной почты компании](./media/attract-admin-email-header.png)

3. <span data-ttu-id="6423e-146">В поле **Ваша политика конфиденциальности в отношении переписки** укажите ссылку на политику конфиденциальности компании.</span><span class="sxs-lookup"><span data-stu-id="6423e-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="6423e-147">В поле **Ваши условия в отношении переписки** предоставьте ссылку на условия использования, принятые в вашей компании.</span><span class="sxs-lookup"><span data-stu-id="6423e-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Добавление ссылок на политику конфиденциальности компании и условия использования для нижнего колонтитула сообщений электронной почты](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="6423e-149">Выберите **Сохранить** для сохранения своих настроек шаблонов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6423e-149">Select **Save** to save your email template settings.</span></span>
