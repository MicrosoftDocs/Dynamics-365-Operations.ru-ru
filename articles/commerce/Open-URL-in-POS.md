---
title: Открытие URL-адреса в POS
description: В этой теме приведен обзор усовершенствований, внесенных в функциональность поиска продукта и клиента в Dynamics 365 Commerce.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 91d10ac383ed860a69d2d62f4a246c5ca8690b3c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206807"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="e0743-103">Открытие URL-адреса в POS</span><span class="sxs-lookup"><span data-stu-id="e0743-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e0743-104">В этой теме описывается, как можно настроить кнопку в POS-терминале розничной торговли, чтобы открыть URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="e0743-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="e0743-105">Эта функция не требует настройки кода, и ее может настроить пользователь, не имеющий роли разработчика.</span><span class="sxs-lookup"><span data-stu-id="e0743-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="e0743-106">Эта функция позволяет настроить кнопку в POS-терминале, используя конструктор сетки кнопок, для открытия URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="e0743-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="e0743-107">В настоящее время это поддерживается в следующих конфигурациях:</span><span class="sxs-lookup"><span data-stu-id="e0743-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="e0743-108">Открыть в новом окне.</span><span class="sxs-lookup"><span data-stu-id="e0743-108">Open in new window.</span></span>
- <span data-ttu-id="e0743-109">Открыть в POS.</span><span class="sxs-lookup"><span data-stu-id="e0743-109">Open within POS.</span></span>
- <span data-ttu-id="e0743-110">Открыть в исходном приложении.</span><span class="sxs-lookup"><span data-stu-id="e0743-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="e0743-111">Открыть в новом окне</span><span class="sxs-lookup"><span data-stu-id="e0743-111">Open in new window</span></span>

<span data-ttu-id="e0743-112">Эта конфигурация определяет, следует ли открывать URL-адрес в новом окне или внутри приложения.</span><span class="sxs-lookup"><span data-stu-id="e0743-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="e0743-113">Если настроено открытие URL-адреса веб в пределах приложения, боковая панель переходов и верхняя панель POS являются видимыми и доступными для взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="e0743-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="e0743-114">Если настроено открытие в новом окне, URL-адрес будет открыт в новом окне приложения на Modern POS для Windows, и в новой вкладке браузера во всех остальных клиентах POS.</span><span class="sxs-lookup"><span data-stu-id="e0743-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="e0743-115">Чтобы активировать эту возможность, необходимо настроить URL-адрес с выбранным параметром **Открыть в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="e0743-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="e0743-116">Открыть в POS</span><span class="sxs-lookup"><span data-stu-id="e0743-116">Open within POS</span></span>

<span data-ttu-id="e0743-117">Открытие URL адреса веб в POS-терминале в настоящее время поддерживается только для Modern POS в среде Windows.</span><span class="sxs-lookup"><span data-stu-id="e0743-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="e0743-118">На других клиентах эта возможность находится на стадии разработки и планируется к выпуску в будущих обновлениях.</span><span class="sxs-lookup"><span data-stu-id="e0743-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="e0743-119">Чтобы активировать эту возможность, необходимо настроить URL-адрес с невыбранным параметром **Открыть в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="e0743-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="e0743-120">Открыть в исходном приложении</span><span class="sxs-lookup"><span data-stu-id="e0743-120">Open a native app</span></span>

<span data-ttu-id="e0743-121">Эта функция также позволяет указывать URL-адреса вне веб, чтобы открыть исходное приложение.</span><span class="sxs-lookup"><span data-stu-id="e0743-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="e0743-122">Например, можно указать URL-адрес протоколов, таких как MailTo, SIP, IM или MSTEAMS, который затем может быть обработан соответствующим собственным приложением на главном устройстве.</span><span class="sxs-lookup"><span data-stu-id="e0743-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="e0743-123">Чтобы активировать эту возможность, необходимо настроить URL-адрес с выбранным параметром **Открыть в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="e0743-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="e0743-124">Для компьютеров Windows см. раздел [Экспорт или импорт ассоциаций приложений по умолчанию](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) для задания ассоциаций протоколов по умолчанию, если компьютер настраивается с помощью системы обслуживания образов развертывания и управления ими (DISM).</span><span class="sxs-lookup"><span data-stu-id="e0743-124">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="e0743-125">При использовании MDM, например Intune, для управления вашим компьютером, см. раздел [Политика CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="e0743-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="e0743-126">Если вы являетесь разработчиком, создающим пользовательский веб-сайт, см. раздел [Запуск приложения по умолчанию для URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="e0743-126">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="e0743-127">Удобное открытие в исходном приложении</span><span class="sxs-lookup"><span data-stu-id="e0743-127">Open a native app seamlessly</span></span>

<span data-ttu-id="e0743-128">Windows, iOS и Android также позволяют открывать приложения более эффективно на основании ассоциации протокола приложения.</span><span class="sxs-lookup"><span data-stu-id="e0743-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="e0743-129">Если приложение еще не настроено для обработки открытия из веб-браузера, может потребоваться, чтобы это сделал разработчик.</span><span class="sxs-lookup"><span data-stu-id="e0743-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="e0743-130">Для Windows см. раздел [Включить приложения для веб-сайтов с помощью обработчиков URI приложения](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="e0743-130">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="e0743-131">Для iOS см. раздел [Универсальные ссылки для разработчиков](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="e0743-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="e0743-132">Для Android см. раздел [Обработка ссылок приложения Android](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="e0743-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="e0743-133">Клиент</span><span class="sxs-lookup"><span data-stu-id="e0743-133">Client</span></span>                | <span data-ttu-id="e0743-134">Открыть в новом окне</span><span class="sxs-lookup"><span data-stu-id="e0743-134">Open in new window</span></span> | <span data-ttu-id="e0743-135">Открыть в исходном приложении</span><span class="sxs-lookup"><span data-stu-id="e0743-135">Open native app</span></span> | <span data-ttu-id="e0743-136">Открыть в POS</span><span class="sxs-lookup"><span data-stu-id="e0743-136">Open within POS</span></span> | <span data-ttu-id="e0743-137">Подробно</span><span class="sxs-lookup"><span data-stu-id="e0743-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="e0743-138">Modern POS в Windows</span><span class="sxs-lookup"><span data-stu-id="e0743-138">Modern POS on Windows</span></span> | <span data-ttu-id="e0743-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="e0743-139">✓\*</span></span>                | <span data-ttu-id="e0743-140">✓</span><span class="sxs-lookup"><span data-stu-id="e0743-140">✓</span></span>               | <span data-ttu-id="e0743-141">✓</span><span class="sxs-lookup"><span data-stu-id="e0743-141">✓</span></span>              | <span data-ttu-id="e0743-142">\* Открывается в новом окне Modern POS</span><span class="sxs-lookup"><span data-stu-id="e0743-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="e0743-143">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="e0743-143">Cloud POS</span></span>             | <span data-ttu-id="e0743-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="e0743-144">✓\*</span></span>                | <span data-ttu-id="e0743-145">✓</span><span class="sxs-lookup"><span data-stu-id="e0743-145">✓</span></span>               | <span data-ttu-id="e0743-146">Х</span><span class="sxs-lookup"><span data-stu-id="e0743-146">X</span></span>              | <span data-ttu-id="e0743-147">\* Открывается в новой вкладке браузера</span><span class="sxs-lookup"><span data-stu-id="e0743-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="e0743-148">Modern POS в iOS</span><span class="sxs-lookup"><span data-stu-id="e0743-148">Modern POS on iOS</span></span>     | <span data-ttu-id="e0743-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="e0743-149">✓\*</span></span>                | <span data-ttu-id="e0743-150">✓</span><span class="sxs-lookup"><span data-stu-id="e0743-150">✓</span></span>               | <span data-ttu-id="e0743-151">Х</span><span class="sxs-lookup"><span data-stu-id="e0743-151">X</span></span>              | <span data-ttu-id="e0743-152">\* Открывается в новой вкладке браузера</span><span class="sxs-lookup"><span data-stu-id="e0743-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="e0743-153">Modern POS в Android</span><span class="sxs-lookup"><span data-stu-id="e0743-153">Modern POS on Android</span></span> | <span data-ttu-id="e0743-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="e0743-154">✓\*</span></span>                | <span data-ttu-id="e0743-155">✓</span><span class="sxs-lookup"><span data-stu-id="e0743-155">✓</span></span>               | <span data-ttu-id="e0743-156">Х</span><span class="sxs-lookup"><span data-stu-id="e0743-156">X</span></span>              | <span data-ttu-id="e0743-157">\* Открывается в новой вкладке браузера</span><span class="sxs-lookup"><span data-stu-id="e0743-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="e0743-158">Перед началом</span><span class="sxs-lookup"><span data-stu-id="e0743-158">Before you begin</span></span>

<span data-ttu-id="e0743-159">Перед началом просмотрите порядок настройки в разделе [Макеты экрана POS](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="e0743-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="e0743-160">Открытие URL-адреса в POS</span><span class="sxs-lookup"><span data-stu-id="e0743-160">Open URL in POS</span></span>

<span data-ttu-id="e0743-161">Чтобы настроить URL-адрес для открытия в POS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0743-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="e0743-162">В головном офисе откройте **Retail и Commerce \> Настройка канала \> Настройка POS \> POS \> Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="e0743-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="e0743-163">Выберите **Сетка кнопок \> Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="e0743-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="e0743-164">Создайте новую кнопку.</span><span class="sxs-lookup"><span data-stu-id="e0743-164">Create a new button.</span></span>
4. <span data-ttu-id="e0743-165">Выберите свойства **Кнопка**.</span><span class="sxs-lookup"><span data-stu-id="e0743-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="e0743-166">Выберите **Открыть URL-адрес** в качестве действия.</span><span class="sxs-lookup"><span data-stu-id="e0743-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="e0743-167">Введите URL-адрес, который требуется использовать.</span><span class="sxs-lookup"><span data-stu-id="e0743-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="e0743-168">Настройте, требуется ли открывать URL-адрес в новом окне.</span><span class="sxs-lookup"><span data-stu-id="e0743-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]