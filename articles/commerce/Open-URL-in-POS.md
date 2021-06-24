---
title: Открытие URL-адреса в POS
description: В этой теме приведен обзор усовершенствований, внесенных в функциональность поиска продукта и клиента в Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 43f28d9b7acb05a83544b04f6786dfe91f2d9f18
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193211"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="f79de-103">Открытие URL-адреса в POS</span><span class="sxs-lookup"><span data-stu-id="f79de-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f79de-104">В этой теме описывается, как можно настроить кнопку в POS-терминале Dynamics 365 Commerce, чтобы открыть URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f79de-104">This topic describes how you can configure a button in Dynamics 365 Commerce point of sale (POS) to open a URL.</span></span> <span data-ttu-id="f79de-105">Эта функция не требует настройки кода, и ее может настроить пользователь, не имеющий роли разработчика.</span><span class="sxs-lookup"><span data-stu-id="f79de-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="f79de-106">Эта функция позволяет настроить кнопку в POS-терминале, используя конструктор сетки кнопок, для открытия URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f79de-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="f79de-107">В настоящее время это поддерживается в следующих конфигурациях:</span><span class="sxs-lookup"><span data-stu-id="f79de-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="f79de-108">Открыть в новом окне.</span><span class="sxs-lookup"><span data-stu-id="f79de-108">Open in new window.</span></span>
- <span data-ttu-id="f79de-109">Открыть в POS.</span><span class="sxs-lookup"><span data-stu-id="f79de-109">Open within POS.</span></span>
- <span data-ttu-id="f79de-110">Открыть в исходном приложении.</span><span class="sxs-lookup"><span data-stu-id="f79de-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="f79de-111">Открыть в новом окне</span><span class="sxs-lookup"><span data-stu-id="f79de-111">Open in new window</span></span>

<span data-ttu-id="f79de-112">Эта конфигурация определяет, следует ли открывать URL-адрес в новом окне или внутри приложения.</span><span class="sxs-lookup"><span data-stu-id="f79de-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="f79de-113">Если настроено открытие URL-адреса веб в пределах приложения, боковая панель переходов и верхняя панель POS являются видимыми и доступными для взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="f79de-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="f79de-114">Если настроено открытие в новом окне, URL-адрес будет открыт в новом окне приложения на Modern POS для Windows, и в новой вкладке браузера во всех остальных клиентах POS.</span><span class="sxs-lookup"><span data-stu-id="f79de-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="f79de-115">Чтобы активировать эту возможность, необходимо настроить URL-адрес с выбранным параметром **Открыть в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="f79de-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="f79de-116">Открыть в POS</span><span class="sxs-lookup"><span data-stu-id="f79de-116">Open within POS</span></span>

<span data-ttu-id="f79de-117">Открытие URL адреса веб в POS-терминале в настоящее время поддерживается только для Modern POS в среде Windows.</span><span class="sxs-lookup"><span data-stu-id="f79de-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="f79de-118">На других клиентах эта возможность находится на стадии разработки и планируется к выпуску в будущих обновлениях.</span><span class="sxs-lookup"><span data-stu-id="f79de-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="f79de-119">Чтобы активировать эту возможность, необходимо настроить URL-адрес с невыбранным параметром **Открыть в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="f79de-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="f79de-120">Открыть в исходном приложении</span><span class="sxs-lookup"><span data-stu-id="f79de-120">Open a native app</span></span>

<span data-ttu-id="f79de-121">Эта функция также позволяет указывать URL-адреса вне веб, чтобы открыть исходное приложение.</span><span class="sxs-lookup"><span data-stu-id="f79de-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="f79de-122">Например, можно указать URL-адрес протоколов, таких как MailTo, SIP, IM или MSTEAMS, который затем может быть обработан соответствующим собственным приложением на главном устройстве.</span><span class="sxs-lookup"><span data-stu-id="f79de-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="f79de-123">Чтобы активировать эту возможность, необходимо настроить URL-адрес с выбранным параметром **Открыть в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="f79de-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="f79de-124">Для компьютеров Windows см. раздел [Экспорт или импорт ассоциаций приложений по умолчанию](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) для задания ассоциаций протоколов по умолчанию, если компьютер настраивается с помощью системы обслуживания образов развертывания и управления ими (DISM).</span><span class="sxs-lookup"><span data-stu-id="f79de-124">For Windows computers, see [Export or Import Default Application Associations](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="f79de-125">При использовании MDM, например Intune, для управления вашим компьютером, см. раздел [Политика CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="f79de-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="f79de-126">Если вы являетесь разработчиком, создающим пользовательский веб-сайт, см. раздел [Запуск приложения по умолчанию для URI](/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="f79de-126">If you are a developer building a custom website, see [Launch the default app for a URI](/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="f79de-127">Удобное открытие в исходном приложении</span><span class="sxs-lookup"><span data-stu-id="f79de-127">Open a native app seamlessly</span></span>

<span data-ttu-id="f79de-128">Windows, iOS и Android также позволяют открывать приложения более эффективно на основании ассоциации протокола приложения.</span><span class="sxs-lookup"><span data-stu-id="f79de-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="f79de-129">Если приложение еще не настроено для обработки открытия из веб-браузера, может потребоваться, чтобы это сделал разработчик.</span><span class="sxs-lookup"><span data-stu-id="f79de-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="f79de-130">Для Windows см. раздел [Включить приложения для веб-сайтов с помощью обработчиков URI приложения](/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="f79de-130">For Windows, see [Enable apps for websites using app URI handlers](/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="f79de-131">Для iOS см. раздел [Универсальные ссылки для разработчиков](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="f79de-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="f79de-132">Для Android см. раздел [Обработка ссылок приложения Android](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="f79de-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="f79de-133">Клиент</span><span class="sxs-lookup"><span data-stu-id="f79de-133">Client</span></span>                | <span data-ttu-id="f79de-134">Открыть в новом окне</span><span class="sxs-lookup"><span data-stu-id="f79de-134">Open in new window</span></span> | <span data-ttu-id="f79de-135">Открыть в исходном приложении</span><span class="sxs-lookup"><span data-stu-id="f79de-135">Open native app</span></span> | <span data-ttu-id="f79de-136">Открыть в POS</span><span class="sxs-lookup"><span data-stu-id="f79de-136">Open within POS</span></span> | <span data-ttu-id="f79de-137">Подробно</span><span class="sxs-lookup"><span data-stu-id="f79de-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="f79de-138">Modern POS в Windows</span><span class="sxs-lookup"><span data-stu-id="f79de-138">Modern POS on Windows</span></span> | <span data-ttu-id="f79de-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="f79de-139">✓\*</span></span>                | <span data-ttu-id="f79de-140">✓</span><span class="sxs-lookup"><span data-stu-id="f79de-140">✓</span></span>               | <span data-ttu-id="f79de-141">✓</span><span class="sxs-lookup"><span data-stu-id="f79de-141">✓</span></span>              | <span data-ttu-id="f79de-142">\* Открывается в новом окне Modern POS</span><span class="sxs-lookup"><span data-stu-id="f79de-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="f79de-143">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="f79de-143">Cloud POS</span></span>             | <span data-ttu-id="f79de-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="f79de-144">✓\*</span></span>                | <span data-ttu-id="f79de-145">✓</span><span class="sxs-lookup"><span data-stu-id="f79de-145">✓</span></span>               | <span data-ttu-id="f79de-146">Х</span><span class="sxs-lookup"><span data-stu-id="f79de-146">X</span></span>              | <span data-ttu-id="f79de-147">\* Открывается в новой вкладке браузера</span><span class="sxs-lookup"><span data-stu-id="f79de-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="f79de-148">Modern POS в iOS</span><span class="sxs-lookup"><span data-stu-id="f79de-148">Modern POS on iOS</span></span>     | <span data-ttu-id="f79de-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="f79de-149">✓\*</span></span>                | <span data-ttu-id="f79de-150">✓</span><span class="sxs-lookup"><span data-stu-id="f79de-150">✓</span></span>               | <span data-ttu-id="f79de-151">Х</span><span class="sxs-lookup"><span data-stu-id="f79de-151">X</span></span>              | <span data-ttu-id="f79de-152">\* Открывается в новой вкладке браузера</span><span class="sxs-lookup"><span data-stu-id="f79de-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="f79de-153">Modern POS в Android</span><span class="sxs-lookup"><span data-stu-id="f79de-153">Modern POS on Android</span></span> | <span data-ttu-id="f79de-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="f79de-154">✓\*</span></span>                | <span data-ttu-id="f79de-155">✓</span><span class="sxs-lookup"><span data-stu-id="f79de-155">✓</span></span>               | <span data-ttu-id="f79de-156">Х</span><span class="sxs-lookup"><span data-stu-id="f79de-156">X</span></span>              | <span data-ttu-id="f79de-157">\* Открывается в новой вкладке браузера</span><span class="sxs-lookup"><span data-stu-id="f79de-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="f79de-158">Перед началом</span><span class="sxs-lookup"><span data-stu-id="f79de-158">Before you begin</span></span>

<span data-ttu-id="f79de-159">Перед началом просмотрите порядок настройки в разделе [Макеты экрана POS](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="f79de-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="f79de-160">Открытие URL-адреса в POS</span><span class="sxs-lookup"><span data-stu-id="f79de-160">Open URL in POS</span></span>

<span data-ttu-id="f79de-161">Чтобы настроить URL-адрес для открытия в POS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f79de-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="f79de-162">В головном офисе откройте **Retail и Commerce \> Настройка канала \> Настройка POS \> POS \> Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="f79de-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="f79de-163">Выберите **Сетка кнопок \> Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="f79de-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="f79de-164">Создайте новую кнопку.</span><span class="sxs-lookup"><span data-stu-id="f79de-164">Create a new button.</span></span>
4. <span data-ttu-id="f79de-165">Выберите свойства **Кнопка**.</span><span class="sxs-lookup"><span data-stu-id="f79de-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="f79de-166">Выберите **Открыть URL-адрес** в качестве действия.</span><span class="sxs-lookup"><span data-stu-id="f79de-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="f79de-167">Введите URL-адрес, который требуется использовать.</span><span class="sxs-lookup"><span data-stu-id="f79de-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="f79de-168">Настройте, требуется ли открывать URL-адрес в новом окне.</span><span class="sxs-lookup"><span data-stu-id="f79de-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
