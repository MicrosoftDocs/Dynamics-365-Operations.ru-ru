---
title: Открытие URL-адреса в POS
description: В этой теме приведен обзор усовершенствований, внесенных в функциональность поиска продукта и клиента в Microsoft Dynamics 365 for Retail.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b07406b4e218b45bdde87c4a579814fe0edbc286
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "327098"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="c07a0-103">Открытие URL-адреса в POS</span><span class="sxs-lookup"><span data-stu-id="c07a0-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c07a0-104">В этой теме описывается, как можно настроить кнопку в POS-терминале розничной торговли, чтобы открыть URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="c07a0-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="c07a0-105">Эта функция не требует настройки кода, и ее может настроить пользователь, не имеющий роли разработчика.</span><span class="sxs-lookup"><span data-stu-id="c07a0-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> <span data-ttu-id="c07a0-106">Эта возможность доступна как часть выпуска Dynamics 365 for Finance and Operations версии 8.1.3 (сборка 8.1.227.10014) или более новой.</span><span class="sxs-lookup"><span data-stu-id="c07a0-106">This feature is available as part of the Dynamics 365 for Finance and Operations version 8.1.3 release (build 8.1.227.10014) and later.</span></span> 

<span data-ttu-id="c07a0-107">Эта функция позволяет настроить кнопку в POS-терминале, используя конструктор сетки кнопок, для открытия URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="c07a0-107">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="c07a0-108">В настоящее время это поддерживается в следующих конфигурациях:</span><span class="sxs-lookup"><span data-stu-id="c07a0-108">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="c07a0-109">Открыть в новом окне.</span><span class="sxs-lookup"><span data-stu-id="c07a0-109">Open in new window.</span></span>
- <span data-ttu-id="c07a0-110">Открыть в POS.</span><span class="sxs-lookup"><span data-stu-id="c07a0-110">Open within POS.</span></span>
- <span data-ttu-id="c07a0-111">Открыть в исходном приложении.</span><span class="sxs-lookup"><span data-stu-id="c07a0-111">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="c07a0-112">Открыть в новом окне</span><span class="sxs-lookup"><span data-stu-id="c07a0-112">Open in new window</span></span>

<span data-ttu-id="c07a0-113">Эта конфигурация определяет, следует ли открывать URL-адрес в новом окне или внутри приложения.</span><span class="sxs-lookup"><span data-stu-id="c07a0-113">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="c07a0-114">Если настроено открытие URL-адреса веб в пределах приложения, боковая панель переходов и верхняя панель POS являются видимыми и доступными для взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="c07a0-114">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="c07a0-115">Если настроено открытие в новом окне, URL-адрес будет открыт в новом окне приложения на Modern POS для Windows, и в новой вкладке браузера во всех остальных клиентах POS.</span><span class="sxs-lookup"><span data-stu-id="c07a0-115">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="c07a0-116">Чтобы активировать эту возможность, необходимо настроить URL-адрес с выбранным параметром **Открыть в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="c07a0-116">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="c07a0-117">Открыть в POS</span><span class="sxs-lookup"><span data-stu-id="c07a0-117">Open within POS</span></span>

<span data-ttu-id="c07a0-118">Открытие URL адреса веб в POS-терминале в настоящее время поддерживается только для Modern POS в среде Windows.</span><span class="sxs-lookup"><span data-stu-id="c07a0-118">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="c07a0-119">На других клиентах эта возможность находится на стадии разработки и планируется к выпуску в будущих обновлениях.</span><span class="sxs-lookup"><span data-stu-id="c07a0-119">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="c07a0-120">Чтобы активировать эту возможность, необходимо настроить URL-адрес с невыбранным параметром **Открыть в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="c07a0-120">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="c07a0-121">Открыть в исходном приложении</span><span class="sxs-lookup"><span data-stu-id="c07a0-121">Open a native app</span></span>

<span data-ttu-id="c07a0-122">Эта функция также позволяет указывать URL-адреса вне веб, чтобы открыть исходное приложение.</span><span class="sxs-lookup"><span data-stu-id="c07a0-122">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="c07a0-123">Например, можно указать URL-адрес протоколов, таких как MailTo, SIP, IM или MSTEAMS, который затем может быть обработан соответствующим собственным приложением на главном устройстве.</span><span class="sxs-lookup"><span data-stu-id="c07a0-123">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="c07a0-124">Чтобы активировать эту возможность, необходимо настроить URL-адрес с выбранным параметром **Открыть в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="c07a0-124">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="c07a0-125">Для компьютеров Windows см. раздел [Экспорт или импорт ассоциаций приложений по умолчанию](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) для задания ассоциаций протоколов по умолчанию, если компьютер настраивается с помощью системы обслуживания образов развертывания и управления ими (DISM).</span><span class="sxs-lookup"><span data-stu-id="c07a0-125">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="c07a0-126">При использовании MDM, например Intune, для управления вашим компьютером, см. раздел [Политика CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="c07a0-126">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="c07a0-127">Если вы являетесь разработчиком, создающим пользовательский веб-сайт, см. раздел [Запуск приложения по умолчанию для URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="c07a0-127">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="c07a0-128">Удобное открытие в исходном приложении</span><span class="sxs-lookup"><span data-stu-id="c07a0-128">Open a native app seamlessly</span></span>

<span data-ttu-id="c07a0-129">Windows, iOS и Android также позволяют открывать приложения более эффективно на основании ассоциации протокола приложения.</span><span class="sxs-lookup"><span data-stu-id="c07a0-129">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="c07a0-130">Если приложение еще не настроено для обработки открытия из веб-браузера, может потребоваться, чтобы это сделал разработчик.</span><span class="sxs-lookup"><span data-stu-id="c07a0-130">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="c07a0-131">Для Windows см. раздел [Включить приложения для веб-сайтов с помощью обработчиков URI приложения](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="c07a0-131">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="c07a0-132">Для iOS см. раздел [Универсальные ссылки для разработчиков](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="c07a0-132">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="c07a0-133">Для Android см. раздел [Обработка ссылок приложения Android](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="c07a0-133">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="c07a0-134">Клиент</span><span class="sxs-lookup"><span data-stu-id="c07a0-134">Client</span></span>                | <span data-ttu-id="c07a0-135">Открыть в новом окне</span><span class="sxs-lookup"><span data-stu-id="c07a0-135">Open in new window</span></span> | <span data-ttu-id="c07a0-136">Открыть в исходном приложении</span><span class="sxs-lookup"><span data-stu-id="c07a0-136">Open native app</span></span> | <span data-ttu-id="c07a0-137">Открыть в POS</span><span class="sxs-lookup"><span data-stu-id="c07a0-137">Open within POS</span></span> | <span data-ttu-id="c07a0-138">Подробно</span><span class="sxs-lookup"><span data-stu-id="c07a0-138">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="c07a0-139">Modern POS в Windows</span><span class="sxs-lookup"><span data-stu-id="c07a0-139">Modern POS on Windows</span></span> | <span data-ttu-id="c07a0-140">✓\*</span><span class="sxs-lookup"><span data-stu-id="c07a0-140">✓\*</span></span>                | <span data-ttu-id="c07a0-141">✓</span><span class="sxs-lookup"><span data-stu-id="c07a0-141">✓</span></span>               | <span data-ttu-id="c07a0-142">✓</span><span class="sxs-lookup"><span data-stu-id="c07a0-142">✓</span></span>              | <span data-ttu-id="c07a0-143">\* Открывается в новом окне Modern POS</span><span class="sxs-lookup"><span data-stu-id="c07a0-143">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="c07a0-144">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="c07a0-144">Cloud POS</span></span>             | <span data-ttu-id="c07a0-145">✓\*</span><span class="sxs-lookup"><span data-stu-id="c07a0-145">✓\*</span></span>                | <span data-ttu-id="c07a0-146">✓</span><span class="sxs-lookup"><span data-stu-id="c07a0-146">✓</span></span>               | <span data-ttu-id="c07a0-147">Х</span><span class="sxs-lookup"><span data-stu-id="c07a0-147">X</span></span>              | <span data-ttu-id="c07a0-148">\* Открывается в новой вкладке браузера</span><span class="sxs-lookup"><span data-stu-id="c07a0-148">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="c07a0-149">Modern POS в iOS</span><span class="sxs-lookup"><span data-stu-id="c07a0-149">Modern POS on iOS</span></span>     | <span data-ttu-id="c07a0-150">✓\*</span><span class="sxs-lookup"><span data-stu-id="c07a0-150">✓\*</span></span>                | <span data-ttu-id="c07a0-151">✓</span><span class="sxs-lookup"><span data-stu-id="c07a0-151">✓</span></span>               | <span data-ttu-id="c07a0-152">Х</span><span class="sxs-lookup"><span data-stu-id="c07a0-152">X</span></span>              | <span data-ttu-id="c07a0-153">\* Открывается в новой вкладке браузера</span><span class="sxs-lookup"><span data-stu-id="c07a0-153">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="c07a0-154">Modern POS в Android</span><span class="sxs-lookup"><span data-stu-id="c07a0-154">Modern POS on Android</span></span> | <span data-ttu-id="c07a0-155">✓\*</span><span class="sxs-lookup"><span data-stu-id="c07a0-155">✓\*</span></span>                | <span data-ttu-id="c07a0-156">✓</span><span class="sxs-lookup"><span data-stu-id="c07a0-156">✓</span></span>               | <span data-ttu-id="c07a0-157">Х</span><span class="sxs-lookup"><span data-stu-id="c07a0-157">X</span></span>              | <span data-ttu-id="c07a0-158">\* Открывается в новой вкладке браузера</span><span class="sxs-lookup"><span data-stu-id="c07a0-158">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="c07a0-159">Перед началом</span><span class="sxs-lookup"><span data-stu-id="c07a0-159">Before you begin</span></span>

<span data-ttu-id="c07a0-160">Перед началом просмотрите порядок настройки в разделе [Макеты экрана POS](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="c07a0-160">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="c07a0-161">Открытие URL-адреса в POS</span><span class="sxs-lookup"><span data-stu-id="c07a0-161">Open URL in POS</span></span>

<span data-ttu-id="c07a0-162">Чтобы настроить URL-адрес для открытия в POS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c07a0-162">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="c07a0-163">В головном офисе откройте **Розничная торговля \> Настройка канала \> Настройка POS \> POS \> Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="c07a0-163">In head office, go to **Retail \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="c07a0-164">Выберите **Сетка кнопок \> Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="c07a0-164">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="c07a0-165">Создайте новую кнопку.</span><span class="sxs-lookup"><span data-stu-id="c07a0-165">Create a new button.</span></span>
4. <span data-ttu-id="c07a0-166">Выберите свойства **Кнопка**.</span><span class="sxs-lookup"><span data-stu-id="c07a0-166">Select **Button** properties.</span></span>
5. <span data-ttu-id="c07a0-167">Выберите **Открыть URL-адрес** в качестве действия.</span><span class="sxs-lookup"><span data-stu-id="c07a0-167">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="c07a0-168">Введите URL-адрес, который требуется использовать.</span><span class="sxs-lookup"><span data-stu-id="c07a0-168">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="c07a0-169">Настройте, требуется ли открывать URL-адрес в новом окне.</span><span class="sxs-lookup"><span data-stu-id="c07a0-169">Configure whether to open the URL in a new window.</span></span>
