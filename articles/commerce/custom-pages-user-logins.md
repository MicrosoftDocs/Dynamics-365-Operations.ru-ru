---
title: Настройка специальных страниц для входа пользователей
description: В этом разделе описывается создание пользовательских страниц в Microsoft Dynamics 365 Commerce, которые обрабатывают настраиваемый вход для пользователей Azure Active Directory (Azure AD) клиентов "предприятие-покупатель" (B2C).
author: brianshook
manager: annbe
ms.date: 09/15/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0b54bf6234dcb87c84b21259c30ca5c321869adf
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817314"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="7b834-103">Настройка пользовательских страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="7b834-103">Set up custom pages for user sign-ins</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7b834-104">В этом разделе описывается создание пользовательских страниц в Microsoft Dynamics 365 Commerce, которые обрабатывают настраиваемый вход для пользователей Azure Active Directory (Azure AD) клиентов "предприятие-покупатель" (B2C).</span><span class="sxs-lookup"><span data-stu-id="7b834-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="7b834-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="7b834-105">Overview</span></span>

<span data-ttu-id="7b834-106">Для использования настраиваемых страниц, созданных в Dynamics 365 Commerce для управления потоками входа пользователей в систему, необходимо настроить политики Azure AD, на которые будут ссылаться в Commerce Environment.</span><span class="sxs-lookup"><span data-stu-id="7b834-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="7b834-107">Можно настроить политики Azure AD B2C "Регистрация и вход", "Редактирование профиля" и "Сброс пароля" с помощью приложения Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="7b834-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="7b834-108">На клиент и имена политик Azure AD B2C затем можно ссылаться в процессе подготовки, которая выполняется для среды Commerce с использованием Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7b834-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="7b834-109">Пользовательские страницы Commerce можно создавать с помощью модуля вход, регистрация, изменения профиля учетной записи или сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="7b834-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="7b834-110">URL-адреса страниц, опубликованные для этих пользовательских страниц, затем должны указываться в конфигурациях политик Azure AD B2C на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="7b834-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="7b834-111">Настройка политик B2C</span><span class="sxs-lookup"><span data-stu-id="7b834-111">Set up B2C policies</span></span>

<span data-ttu-id="7b834-112">После настройки клиента Azure AD B2C и связывания его со средой Commerce перейдите на страницу **Azure AD B2C** на портале Azure, затем в меню в разделе **Политики** выберите пункт **Потоки пользователей (политики)**.</span><span class="sxs-lookup"><span data-stu-id="7b834-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Команда "Потоки пользователей (политики)" в меню](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="7b834-114">Теперь можно настроить потоки входа пользователей "Регистрация и вход", "Изменение профиля" и "Сброс пароля".</span><span class="sxs-lookup"><span data-stu-id="7b834-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="7b834-115">Настройка политику "Регистрация и вход"</span><span class="sxs-lookup"><span data-stu-id="7b834-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="7b834-116">Чтобы настроить политику "Регистрация и вход", выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b834-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="7b834-117">Выберите **Создать поток пользователей**, затем на вкладке **Рекомендуется** выберите политику **Регистрация и вход**.</span><span class="sxs-lookup"><span data-stu-id="7b834-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="7b834-118">Введите имя политики (например, **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="7b834-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="7b834-119">В разделе **Поставщики удостоверений** выберите поставщиков удостоверений, которые будут использоваться для этой политики.</span><span class="sxs-lookup"><span data-stu-id="7b834-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="7b834-120">Как минимум должна быть выбрана **Регистрация по электронной почте**.</span><span class="sxs-lookup"><span data-stu-id="7b834-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="7b834-121">В столбце **Собрать атрибут** установите флажки для **Адрес электронной почты**, **Имя** и **Фамилия**.</span><span class="sxs-lookup"><span data-stu-id="7b834-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="7b834-122">В столбце **Вернуть утверждение** установите флажки для **Адреса электронной почты**, **Имя**, **Поставщик удостоверений**, **Фамилия** и **Идентификаторов объектов пользователей**.</span><span class="sxs-lookup"><span data-stu-id="7b834-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Выбранные атрибуты и утверждения](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="7b834-124">Выберите **ОК**, чтобы создать политику.</span><span class="sxs-lookup"><span data-stu-id="7b834-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="7b834-125">Дважды щелкните имя новой политики, затем в области переходов выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="7b834-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="7b834-126">Установите для параметра **Включить JavaScript с принудительным применением макета страницы (предварительная версия)** значение **Вкл.**</span><span class="sxs-lookup"><span data-stu-id="7b834-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Страница свойств для новой политики](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="7b834-128">В среде Commerce будет полностью указана ссылка на имя политики.</span><span class="sxs-lookup"><span data-stu-id="7b834-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="7b834-129">(В ссылку будет включен префикс **B2C\_1\_**.) После создания политик они не могут быть переименованы.</span><span class="sxs-lookup"><span data-stu-id="7b834-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="7b834-130">Если вы заменяете существующую политику для среды Commerce, вы можете удалить исходную политику и построить новую политику с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="7b834-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="7b834-131">В качестве альтернативы, если среда уже была подготовлена, можно представить новое имя политики с помощью запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="7b834-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="7b834-132">Вы вернетесь к этой политике, чтобы завершить настройку после создания пользовательских страници</span><span class="sxs-lookup"><span data-stu-id="7b834-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="7b834-133">Пока закройте политику, чтобы вернуться на страницу **Потоки пользователей (политики)** на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="7b834-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="7b834-134">Настройка политики "Изменение профиля"</span><span class="sxs-lookup"><span data-stu-id="7b834-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="7b834-135">Чтобы настроить политику "Изменение профиля", выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b834-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="7b834-136">Выберите **Создать поток пользователей**, затем на вкладке **Рекомендуется** выберите политику **Изменение профиля**.</span><span class="sxs-lookup"><span data-stu-id="7b834-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="7b834-137">Введите имя политики (например, **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="7b834-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="7b834-138">В разделе **Поставщики удостоверений** выберите поставщиков удостоверений, которые будут использоваться для этой политики.</span><span class="sxs-lookup"><span data-stu-id="7b834-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="7b834-139">Необходимо выбрать, по меньшей мере, **Локальная учетная запись для входа**.</span><span class="sxs-lookup"><span data-stu-id="7b834-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="7b834-140">В столбце **Собрать атрибут** установите флажки для **Адреса электронной почты** и **Фамилия**.</span><span class="sxs-lookup"><span data-stu-id="7b834-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="7b834-141">В столбце **Вернуть утверждение** установите флажки для **Адреса электронной почты**, **Имя**, **Поставщик удостоверений**, **Фамилия** и **Идентификаторов объектов пользователей**.</span><span class="sxs-lookup"><span data-stu-id="7b834-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="7b834-142">Выберите **ОК**, чтобы создать политику.</span><span class="sxs-lookup"><span data-stu-id="7b834-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="7b834-143">Дважды щелкните имя новой политики, затем в области переходов выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="7b834-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="7b834-144">Установите для параметра **Включить JavaScript с принудительным применением макета страницы (предварительная версия)** значение **Вкл.**</span><span class="sxs-lookup"><span data-stu-id="7b834-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="7b834-145">Вы вернетесь к этой политике, чтобы завершить настройку после создания пользовательских страници</span><span class="sxs-lookup"><span data-stu-id="7b834-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="7b834-146">Пока закройте политику, чтобы вернуться на страницу **Потоки пользователей (политики)** на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="7b834-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="7b834-147">Настройте политику "Сброс пароля"</span><span class="sxs-lookup"><span data-stu-id="7b834-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="7b834-148">Чтобы настроить политику "Сброс пароля", выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b834-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="7b834-149">Выберите **Создать поток пользователей**, затем на вкладке **Предварительный просмотр** выберите политику **Сброс пароля v1.1**.</span><span class="sxs-lookup"><span data-stu-id="7b834-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Политика сброса пароля v1.1, выбранная на вкладке "Предварительный просмотр"](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="7b834-151">Введите имя политики (например, **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="7b834-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="7b834-152">В разделе **Поставщики удостоверений** выберите **Сбросить пароль, используя адрес электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="7b834-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="7b834-153">В столбце **Вернуть утверждение** установите флажки для **Адреса электронной почты**, **Имя**, **Фамилия** и **Идентификаторов объектов пользователей**.</span><span class="sxs-lookup"><span data-stu-id="7b834-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Выбранные утверждения](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="7b834-155">Выберите **ОК**, чтобы создать политику.</span><span class="sxs-lookup"><span data-stu-id="7b834-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="7b834-156">Дважды щелкните имя новой политики, затем в области переходов выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="7b834-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="7b834-157">Установите для параметра **Включить JavaScript с принудительным применением макета страницы (предварительная версия)** значение **Вкл.**</span><span class="sxs-lookup"><span data-stu-id="7b834-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="7b834-158">Вы вернетесь к этой политике, чтобы завершить настройку после создания пользовательских страници</span><span class="sxs-lookup"><span data-stu-id="7b834-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="7b834-159">Пока закройте политику, чтобы вернуться на страницу **Потоки пользователей (политики)** на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="7b834-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="7b834-160">Создание пользовательских страниц</span><span class="sxs-lookup"><span data-stu-id="7b834-160">Build the custom pages</span></span>

<span data-ttu-id="7b834-161">Чтобы создать пользовательские страницы для обработки входа пользователей, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b834-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="7b834-162">В инструментах разработки Commerce перейдите на ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="7b834-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="7b834-163">Создайте следующие пять шаблонов и пять страниц:</span><span class="sxs-lookup"><span data-stu-id="7b834-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="7b834-164">Шаблон и страница **Вход**, использующие модуль входа.</span><span class="sxs-lookup"><span data-stu-id="7b834-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="7b834-165">Шаблон и страница **Регистрация**, использующие модуль регистрации.</span><span class="sxs-lookup"><span data-stu-id="7b834-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="7b834-166">Шаблон и страница **Сброс пароля**, использующие модуль сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="7b834-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="7b834-167">Шаблон и страница **Проверка сброса пароля**, использующие модуль проверки сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="7b834-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="7b834-168">Шаблон и страница **Изменение профиля**, использующие модуль изменения профиля учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7b834-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="7b834-169">При создании страниц необходимо следовать следующим указаниям:</span><span class="sxs-lookup"><span data-stu-id="7b834-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="7b834-170">Для каждой страницы или модуля используйте макет и стиль, которые наилучшим образом подходят для требований бизнеса.</span><span class="sxs-lookup"><span data-stu-id="7b834-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="7b834-171">Опубликуйте все страницы и URL-адреса, которые должны использоваться в настройке Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="7b834-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="7b834-172">После публикации страниц и URL-адресов необходимо собрать URL-адреса, которые должны использоваться для конфигураций политик Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="7b834-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="7b834-173">Суффикс **?preloadscripts=true** добавляется к каждому URL-адресу, когда он используется.</span><span class="sxs-lookup"><span data-stu-id="7b834-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b834-174">Не используйте повторно универсальные верхние и нижние колонтитулы, имеющие относительные ссылки.</span><span class="sxs-lookup"><span data-stu-id="7b834-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="7b834-175">Так как эти страницы будут размещаться в домене Azure AD B2C при их использовании, для всех ссылок должны использоваться только абсолютные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7b834-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="7b834-176">Настройка политик Azure AD B2C со сведениями настраиваемой страницы</span><span class="sxs-lookup"><span data-stu-id="7b834-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="7b834-177">На портале Azure вернитесь на страницу **Azure AD B2C**, затем в меню в разделе **Политики** выберите **Потоки пользователей (политики)**.</span><span class="sxs-lookup"><span data-stu-id="7b834-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="7b834-178">Обновление политики "Регистрация и вход" со сведениями настраиваемой страницы</span><span class="sxs-lookup"><span data-stu-id="7b834-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="7b834-179">Чтобы обновить политику "Регистрация и вход" со сведениями настраиваемой страницы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b834-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="7b834-180">В политике **Вход и регистрация**, настроенной ранее, в области переходов выберите **Макеты страниц**.</span><span class="sxs-lookup"><span data-stu-id="7b834-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="7b834-181">Выберите макет **Единая страница регистрации или входа**.</span><span class="sxs-lookup"><span data-stu-id="7b834-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="7b834-182">Установите для параметра **Использовать пользовательское содержимое страницы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="7b834-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7b834-183">В поле **URI пользовательской страницы** введите полный URL-адрес входа.</span><span class="sxs-lookup"><span data-stu-id="7b834-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="7b834-184">Включите суффикс **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="7b834-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7b834-185">Например, введите ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="7b834-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7b834-186">В поле **Версия макета страницы (предварительная версия)** выберите **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="7b834-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7b834-187">Выберите макет **Страница регистрации локальной учетной записи**.</span><span class="sxs-lookup"><span data-stu-id="7b834-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="7b834-188">Установите для параметра **Использовать пользовательское содержимое страницы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="7b834-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7b834-189">В поле **URI пользовательской страницы** введите полный URL-адрес регистрации.</span><span class="sxs-lookup"><span data-stu-id="7b834-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="7b834-190">Включите суффикс **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="7b834-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7b834-191">Например, введите ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="7b834-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7b834-192">В поле **Версия макета страницы (предварительная версия)** выберите **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="7b834-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7b834-193">В разделе **Атрибуты пользователя** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7b834-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="7b834-194">Для атрибутов **Адреса электронной почты**, **Имя** и **Фамилия** выберите **Нет** в поле **Требуется проверка**.</span><span class="sxs-lookup"><span data-stu-id="7b834-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="7b834-195">Для атрибутов **Имя** и **Фамилия** выберите **Нет** в поле **Необязательно**.</span><span class="sxs-lookup"><span data-stu-id="7b834-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Конфигурация политики страницы регистрации локальной учетной записи](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="7b834-197">Обновление политики "Изменение профиля" со сведениями настраиваемой страницы</span><span class="sxs-lookup"><span data-stu-id="7b834-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="7b834-198">Чтобы обновить политику "Изменение профиля" со сведениями настраиваемой страницы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b834-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="7b834-199">В политике **Изменение профиля**, настроенной ранее, в области переходов выберите **Макеты страниц**.</span><span class="sxs-lookup"><span data-stu-id="7b834-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="7b834-200">Выберите макет **Страница изменения профиля**.</span><span class="sxs-lookup"><span data-stu-id="7b834-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="7b834-201">Установите для параметра **Использовать пользовательское содержимое страницы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="7b834-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7b834-202">В поле **URI пользовательской страницы** введите полный URL-адрес редактирования профиля.</span><span class="sxs-lookup"><span data-stu-id="7b834-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="7b834-203">Включите суффикс **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="7b834-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7b834-204">Например, введите ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="7b834-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7b834-205">В поле **Версия макета страницы (предварительная версия)** выберите **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="7b834-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7b834-206">В разделе **Атрибуты пользователя** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7b834-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="7b834-207">Для атрибутов **Адреса электронной почты** и **Имя** выберите **Нет** в поле **Требуется проверка**.</span><span class="sxs-lookup"><span data-stu-id="7b834-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="7b834-208">Для атрибутов **Имя** и **Фамилия** выберите **Нет** в поле **Необязательно**.</span><span class="sxs-lookup"><span data-stu-id="7b834-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="7b834-209">Обновление политики "Сброс пароля" со сведениями настраиваемой страницы</span><span class="sxs-lookup"><span data-stu-id="7b834-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="7b834-210">Чтобы обновить политику "Сброс пароля" со сведениями настраиваемой страницы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b834-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="7b834-211">В политике **Сброс пароля**, настроенной ранее, в области переходов выберите **Макеты страниц**.</span><span class="sxs-lookup"><span data-stu-id="7b834-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="7b834-212">Выберите макет **Страница создания пароля**.</span><span class="sxs-lookup"><span data-stu-id="7b834-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="7b834-213">Установите для параметра **Использовать пользовательское содержимое страницы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="7b834-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7b834-214">В поле **URI пользовательской страницы** введите полный URL-адрес сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="7b834-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="7b834-215">Включите суффикс **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="7b834-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7b834-216">Например, введите ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="7b834-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7b834-217">В поле **Версия макета страницы (предварительная версия)** выберите **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="7b834-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7b834-218">Выберите макет **Страница проверки учетной записи**.</span><span class="sxs-lookup"><span data-stu-id="7b834-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="7b834-219">Установите для параметра **Использовать пользовательское содержимое страницы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="7b834-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7b834-220">В поле **URI пользовательской страницы** введите полный URL-адрес проверки сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="7b834-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="7b834-221">Включите суффикс **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="7b834-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7b834-222">Например, введите ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="7b834-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7b834-223">В поле **Версия макета страницы (предварительная версия)** выберите **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="7b834-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="7b834-224">Настройка текстовых строк по умолчанию для подписей и описаний</span><span class="sxs-lookup"><span data-stu-id="7b834-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="7b834-225">В библиотеке модулей модули входа предварительно заполнены текстовыми строками по умолчанию для подписей и описаний.</span><span class="sxs-lookup"><span data-stu-id="7b834-225">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="7b834-226">Эти строки можно настроить в пакете разработки программного обеспечения (SDK), обновив значения в файле global.json для модуля входа.</span><span class="sxs-lookup"><span data-stu-id="7b834-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="7b834-227">Например, текст по умолчанию для ссылки забытого пароля — **Забыли пароль?**.</span><span class="sxs-lookup"><span data-stu-id="7b834-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="7b834-228">Ниже показан этот текст по умолчанию на странице входа.</span><span class="sxs-lookup"><span data-stu-id="7b834-228">The following shows this default text on the sign-in page.</span></span>

![Текст по умолчанию для ссылки забытого пароля на странице входа](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="7b834-230">Однако в файле global.json для библиотеке модулей в модуле входа можно изменить текст на **Не помните пароль?**, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="7b834-230">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Обновленный текст ссылки в файле global.json модуля входа](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="7b834-232">После обновления файла global.json и публикации изменений новый текст ссылки появляется в модуле входа как в Commerce, так и на опубликованной странице входа.</span><span class="sxs-lookup"><span data-stu-id="7b834-232">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b834-233">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7b834-233">Additional resources</span></span>

[<span data-ttu-id="7b834-234">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="7b834-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="7b834-235">Развертывание нового сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="7b834-235">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="7b834-236">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="7b834-236">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="7b834-237">Связывание веб-сайта с каналом</span><span class="sxs-lookup"><span data-stu-id="7b834-237">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="7b834-238">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="7b834-238">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="7b834-239">Пакетная отправка перенаправлений URL-адресов</span><span class="sxs-lookup"><span data-stu-id="7b834-239">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="7b834-240">Настройка клиента B2C в Commerce</span><span class="sxs-lookup"><span data-stu-id="7b834-240">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="7b834-241">Настройка нескольких клиентов B2C в среде Commerce</span><span class="sxs-lookup"><span data-stu-id="7b834-241">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="7b834-242">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="7b834-242">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="7b834-243">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="7b834-243">Enable location-based store detection</span></span>](enable-store-detection.md)
