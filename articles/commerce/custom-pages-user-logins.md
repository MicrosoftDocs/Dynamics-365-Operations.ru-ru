---
title: Настройка пользовательских страниц для входа пользователей
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3328fad5328ae1954a6749f9a5eebcb71c723698
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477956"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="a5516-103">Настройка пользовательских страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="a5516-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a5516-104">В этом разделе описывается создание пользовательских страниц в Microsoft Dynamics 365 Commerce, которые обрабатывают настраиваемый вход для пользователей Azure Active Directory (Azure AD) клиентов "предприятие-покупатель" (B2C).</span><span class="sxs-lookup"><span data-stu-id="a5516-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="a5516-105">Для использования настраиваемых страниц, созданных в Dynamics 365 Commerce для управления потоками входа пользователей в систему, необходимо настроить политики Azure AD, на которые будут ссылаться в Commerce Environment.</span><span class="sxs-lookup"><span data-stu-id="a5516-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="a5516-106">Можно настроить политики Azure AD B2C "Регистрация и вход", "Редактирование профиля" и "Сброс пароля" с помощью приложения Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a5516-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="a5516-107">На клиент и имена политик Azure AD B2C затем можно ссылаться в процессе подготовки, которая выполняется для среды Commerce с использованием Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a5516-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="a5516-108">Пользовательские страницы Commerce можно создавать с помощью модуля вход, регистрация, изменения профиля учетной записи или сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="a5516-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="a5516-109">URL-адреса страниц, опубликованные для этих пользовательских страниц, затем должны указываться в конфигурациях политик Azure AD B2C на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="a5516-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="a5516-110">Настройка политик B2C</span><span class="sxs-lookup"><span data-stu-id="a5516-110">Set up B2C policies</span></span>

<span data-ttu-id="a5516-111">После настройки клиента Azure AD B2C и связывания его со средой Commerce перейдите на страницу **Azure AD B2C** на портале Azure, затем в меню в разделе **Политики** выберите пункт **Потоки пользователей (политики)**.</span><span class="sxs-lookup"><span data-stu-id="a5516-111">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Команда "Потоки пользователей (политики)" в меню](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="a5516-113">Теперь можно настроить потоки входа пользователей "Регистрация и вход", "Изменение профиля" и "Сброс пароля".</span><span class="sxs-lookup"><span data-stu-id="a5516-113">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="a5516-114">Настройка политику "Регистрация и вход"</span><span class="sxs-lookup"><span data-stu-id="a5516-114">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="a5516-115">Чтобы настроить политику "Регистрация и вход", выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5516-115">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="a5516-116">Выберите **Создать поток пользователей**, затем на вкладке **Рекомендуется** выберите политику **Регистрация и вход**.</span><span class="sxs-lookup"><span data-stu-id="a5516-116">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="a5516-117">Введите имя политики (например, **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="a5516-117">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="a5516-118">В разделе **Поставщики удостоверений** выберите поставщиков удостоверений, которые будут использоваться для этой политики.</span><span class="sxs-lookup"><span data-stu-id="a5516-118">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="a5516-119">Как минимум должна быть выбрана **Регистрация по электронной почте**.</span><span class="sxs-lookup"><span data-stu-id="a5516-119">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="a5516-120">В столбце **Собрать атрибут** установите флажки для **Адрес электронной почты**, **Имя** и **Фамилия**.</span><span class="sxs-lookup"><span data-stu-id="a5516-120">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="a5516-121">В столбце **Вернуть утверждение** установите флажки для **Адреса электронной почты**, **Имя**, **Поставщик удостоверений**, **Фамилия** и **Идентификаторов объектов пользователей**.</span><span class="sxs-lookup"><span data-stu-id="a5516-121">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Выбранные атрибуты и утверждения](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="a5516-123">Выберите **ОК**, чтобы создать политику.</span><span class="sxs-lookup"><span data-stu-id="a5516-123">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="a5516-124">Дважды щелкните имя новой политики, затем в области переходов выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a5516-124">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="a5516-125">Установите для параметра **Включить JavaScript с принудительным применением макета страницы (предварительная версия)** значение **Вкл.**</span><span class="sxs-lookup"><span data-stu-id="a5516-125">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Страница свойств для новой политики](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="a5516-127">В среде Commerce будет полностью указана ссылка на имя политики.</span><span class="sxs-lookup"><span data-stu-id="a5516-127">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="a5516-128">(В ссылку будет включен префикс **B2C\_1\_**.) После создания политик они не могут быть переименованы.</span><span class="sxs-lookup"><span data-stu-id="a5516-128">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="a5516-129">Если вы заменяете существующую политику для среды Commerce, вы можете удалить исходную политику и построить новую политику с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="a5516-129">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="a5516-130">В качестве альтернативы, если среда уже была подготовлена, можно представить новое имя политики с помощью запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="a5516-130">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="a5516-131">Вы вернетесь к этой политике, чтобы завершить настройку после создания пользовательских страници</span><span class="sxs-lookup"><span data-stu-id="a5516-131">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="a5516-132">Пока закройте политику, чтобы вернуться на страницу **Потоки пользователей (политики)** на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="a5516-132">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="a5516-133">Настройка политики "Изменение профиля"</span><span class="sxs-lookup"><span data-stu-id="a5516-133">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="a5516-134">Чтобы настроить политику "Изменение профиля", выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5516-134">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="a5516-135">Выберите **Создать поток пользователей**, затем на вкладке **Рекомендуется** выберите политику **Изменение профиля**.</span><span class="sxs-lookup"><span data-stu-id="a5516-135">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="a5516-136">Введите имя политики (например, **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="a5516-136">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="a5516-137">В разделе **Поставщики удостоверений** выберите поставщиков удостоверений, которые будут использоваться для этой политики.</span><span class="sxs-lookup"><span data-stu-id="a5516-137">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="a5516-138">Необходимо выбрать, по меньшей мере, **Локальная учетная запись для входа**.</span><span class="sxs-lookup"><span data-stu-id="a5516-138">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="a5516-139">В столбце **Собрать атрибут** установите флажки для **Адреса электронной почты** и **Фамилия**.</span><span class="sxs-lookup"><span data-stu-id="a5516-139">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="a5516-140">В столбце **Вернуть утверждение** установите флажки для **Адреса электронной почты**, **Имя**, **Поставщик удостоверений**, **Фамилия** и **Идентификаторов объектов пользователей**.</span><span class="sxs-lookup"><span data-stu-id="a5516-140">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="a5516-141">Выберите **ОК**, чтобы создать политику.</span><span class="sxs-lookup"><span data-stu-id="a5516-141">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="a5516-142">Дважды щелкните имя новой политики, затем в области переходов выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a5516-142">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="a5516-143">Установите для параметра **Включить JavaScript с принудительным применением макета страницы (предварительная версия)** значение **Вкл.**</span><span class="sxs-lookup"><span data-stu-id="a5516-143">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="a5516-144">Вы вернетесь к этой политике, чтобы завершить настройку после создания пользовательских страници</span><span class="sxs-lookup"><span data-stu-id="a5516-144">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="a5516-145">Пока закройте политику, чтобы вернуться на страницу **Потоки пользователей (политики)** на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="a5516-145">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="a5516-146">Настройте политику "Сброс пароля"</span><span class="sxs-lookup"><span data-stu-id="a5516-146">Configure the "Password reset" policy</span></span>

<span data-ttu-id="a5516-147">Чтобы настроить политику "Сброс пароля", выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5516-147">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="a5516-148">Выберите **Создать поток пользователей**, затем на вкладке **Предварительный просмотр** выберите политику **Сброс пароля v1.1**.</span><span class="sxs-lookup"><span data-stu-id="a5516-148">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Политика сброса пароля v1.1, выбранная на вкладке "Предварительный просмотр"](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="a5516-150">Введите имя политики (например, **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="a5516-150">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="a5516-151">В разделе **Поставщики удостоверений** выберите **Сбросить пароль, используя адрес электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="a5516-151">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="a5516-152">В столбце **Вернуть утверждение** установите флажки для **Адреса электронной почты**, **Имя**, **Фамилия** и **Идентификаторов объектов пользователей**.</span><span class="sxs-lookup"><span data-stu-id="a5516-152">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Выбранные утверждения](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="a5516-154">Выберите **ОК**, чтобы создать политику.</span><span class="sxs-lookup"><span data-stu-id="a5516-154">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="a5516-155">Дважды щелкните имя новой политики, затем в области переходов выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a5516-155">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="a5516-156">Установите для параметра **Включить JavaScript с принудительным применением макета страницы (предварительная версия)** значение **Вкл.**</span><span class="sxs-lookup"><span data-stu-id="a5516-156">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="a5516-157">Вы вернетесь к этой политике, чтобы завершить настройку после создания пользовательских страници</span><span class="sxs-lookup"><span data-stu-id="a5516-157">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="a5516-158">Пока закройте политику, чтобы вернуться на страницу **Потоки пользователей (политики)** на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="a5516-158">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="a5516-159">Создание пользовательских страниц</span><span class="sxs-lookup"><span data-stu-id="a5516-159">Build the custom pages</span></span>

<span data-ttu-id="a5516-160">Чтобы создать пользовательские страницы для обработки входа пользователей, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5516-160">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="a5516-161">В инструментах разработки Commerce перейдите на ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="a5516-161">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="a5516-162">Создайте следующие пять шаблонов и пять страниц:</span><span class="sxs-lookup"><span data-stu-id="a5516-162">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="a5516-163">Шаблон и страница **Вход**, использующие модуль входа.</span><span class="sxs-lookup"><span data-stu-id="a5516-163">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="a5516-164">Шаблон и страница **Регистрация**, использующие модуль регистрации.</span><span class="sxs-lookup"><span data-stu-id="a5516-164">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="a5516-165">Шаблон и страница **Сброс пароля**, использующие модуль сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="a5516-165">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="a5516-166">Шаблон и страница **Проверка сброса пароля**, использующие модуль проверки сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="a5516-166">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="a5516-167">Шаблон и страница **Изменение профиля**, использующие модуль изменения профиля учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a5516-167">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="a5516-168">При создании страниц необходимо следовать следующим указаниям:</span><span class="sxs-lookup"><span data-stu-id="a5516-168">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="a5516-169">Для каждой страницы или модуля используйте макет и стиль, которые наилучшим образом подходят для требований бизнеса.</span><span class="sxs-lookup"><span data-stu-id="a5516-169">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="a5516-170">Опубликуйте все страницы и URL-адреса, которые должны использоваться в настройке Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a5516-170">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="a5516-171">После публикации страниц и URL-адресов необходимо собрать URL-адреса, которые должны использоваться для конфигураций политик Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a5516-171">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="a5516-172">Суффикс **?preloadscripts=true** добавляется к каждому URL-адресу, когда он используется.</span><span class="sxs-lookup"><span data-stu-id="a5516-172">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5516-173">Не используйте повторно универсальные верхние и нижние колонтитулы, имеющие относительные ссылки.</span><span class="sxs-lookup"><span data-stu-id="a5516-173">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="a5516-174">Так как эти страницы будут размещаться в домене Azure AD B2C при их использовании, для всех ссылок должны использоваться только абсолютные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="a5516-174">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="a5516-175">Настройка политик Azure AD B2C со сведениями настраиваемой страницы</span><span class="sxs-lookup"><span data-stu-id="a5516-175">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="a5516-176">На портале Azure вернитесь на страницу **Azure AD B2C**, затем в меню в разделе **Политики** выберите **Потоки пользователей (политики)**.</span><span class="sxs-lookup"><span data-stu-id="a5516-176">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="a5516-177">Обновление политики "Регистрация и вход" со сведениями настраиваемой страницы</span><span class="sxs-lookup"><span data-stu-id="a5516-177">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="a5516-178">Чтобы обновить политику "Регистрация и вход" со сведениями настраиваемой страницы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5516-178">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="a5516-179">В политике **Вход и регистрация**, настроенной ранее, в области переходов выберите **Макеты страниц**.</span><span class="sxs-lookup"><span data-stu-id="a5516-179">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="a5516-180">Выберите макет **Единая страница регистрации или входа**.</span><span class="sxs-lookup"><span data-stu-id="a5516-180">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="a5516-181">Установите для параметра **Использовать пользовательское содержимое страницы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a5516-181">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="a5516-182">В поле **URI пользовательской страницы** введите полный URL-адрес входа.</span><span class="sxs-lookup"><span data-stu-id="a5516-182">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="a5516-183">Включите суффикс **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="a5516-183">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="a5516-184">Например, введите ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="a5516-184">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="a5516-185">В поле **Версия макета страницы (предварительная версия)** выберите **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="a5516-185">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="a5516-186">Выберите макет **Страница регистрации локальной учетной записи**.</span><span class="sxs-lookup"><span data-stu-id="a5516-186">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="a5516-187">Установите для параметра **Использовать пользовательское содержимое страницы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a5516-187">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="a5516-188">В поле **URI пользовательской страницы** введите полный URL-адрес регистрации.</span><span class="sxs-lookup"><span data-stu-id="a5516-188">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="a5516-189">Включите суффикс **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="a5516-189">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="a5516-190">Например, введите ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="a5516-190">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="a5516-191">В поле **Версия макета страницы (предварительная версия)** выберите **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="a5516-191">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="a5516-192">В разделе **Атрибуты пользователя** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a5516-192">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="a5516-193">Для атрибутов **Адреса электронной почты**, **Имя** и **Фамилия** выберите **Нет** в поле **Требуется проверка**.</span><span class="sxs-lookup"><span data-stu-id="a5516-193">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="a5516-194">Для атрибутов **Имя** и **Фамилия** выберите **Нет** в поле **Необязательно**.</span><span class="sxs-lookup"><span data-stu-id="a5516-194">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Конфигурация политики страницы регистрации локальной учетной записи](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="a5516-196">Обновление политики "Изменение профиля" со сведениями настраиваемой страницы</span><span class="sxs-lookup"><span data-stu-id="a5516-196">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="a5516-197">Чтобы обновить политику "Изменение профиля" со сведениями настраиваемой страницы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5516-197">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="a5516-198">В политике **Изменение профиля**, настроенной ранее, в области переходов выберите **Макеты страниц**.</span><span class="sxs-lookup"><span data-stu-id="a5516-198">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="a5516-199">Выберите макет **Страница изменения профиля**.</span><span class="sxs-lookup"><span data-stu-id="a5516-199">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="a5516-200">Установите для параметра **Использовать пользовательское содержимое страницы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a5516-200">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="a5516-201">В поле **URI пользовательской страницы** введите полный URL-адрес редактирования профиля.</span><span class="sxs-lookup"><span data-stu-id="a5516-201">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="a5516-202">Включите суффикс **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="a5516-202">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="a5516-203">Например, введите ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="a5516-203">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="a5516-204">В поле **Версия макета страницы (предварительная версия)** выберите **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="a5516-204">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="a5516-205">В разделе **Атрибуты пользователя** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a5516-205">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="a5516-206">Для атрибутов **Адреса электронной почты** и **Имя** выберите **Нет** в поле **Требуется проверка**.</span><span class="sxs-lookup"><span data-stu-id="a5516-206">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="a5516-207">Для атрибутов **Имя** и **Фамилия** выберите **Нет** в поле **Необязательно**.</span><span class="sxs-lookup"><span data-stu-id="a5516-207">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="a5516-208">Обновление политики "Сброс пароля" со сведениями настраиваемой страницы</span><span class="sxs-lookup"><span data-stu-id="a5516-208">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="a5516-209">Чтобы обновить политику "Сброс пароля" со сведениями настраиваемой страницы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5516-209">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="a5516-210">В политике **Сброс пароля**, настроенной ранее, в области переходов выберите **Макеты страниц**.</span><span class="sxs-lookup"><span data-stu-id="a5516-210">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="a5516-211">Выберите макет **Страница создания пароля**.</span><span class="sxs-lookup"><span data-stu-id="a5516-211">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="a5516-212">Установите для параметра **Использовать пользовательское содержимое страницы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a5516-212">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="a5516-213">В поле **URI пользовательской страницы** введите полный URL-адрес сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="a5516-213">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="a5516-214">Включите суффикс **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="a5516-214">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="a5516-215">Например, введите ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="a5516-215">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="a5516-216">В поле **Версия макета страницы (предварительная версия)** выберите **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="a5516-216">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="a5516-217">Выберите макет **Страница проверки учетной записи**.</span><span class="sxs-lookup"><span data-stu-id="a5516-217">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="a5516-218">Установите для параметра **Использовать пользовательское содержимое страницы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a5516-218">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="a5516-219">В поле **URI пользовательской страницы** введите полный URL-адрес проверки сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="a5516-219">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="a5516-220">Включите суффикс **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="a5516-220">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="a5516-221">Например, введите ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="a5516-221">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="a5516-222">В поле **Версия макета страницы (предварительная версия)** выберите **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="a5516-222">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="a5516-223">Настройка текстовых строк по умолчанию для подписей и описаний</span><span class="sxs-lookup"><span data-stu-id="a5516-223">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="a5516-224">В библиотеке модулей модули входа предварительно заполнены текстовыми строками по умолчанию для подписей и описаний.</span><span class="sxs-lookup"><span data-stu-id="a5516-224">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="a5516-225">Эти строки можно настроить в пакете разработки программного обеспечения (SDK), обновив значения в файле global.json для модуля входа.</span><span class="sxs-lookup"><span data-stu-id="a5516-225">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="a5516-226">Например, текст по умолчанию для ссылки забытого пароля — **Забыли пароль?**.</span><span class="sxs-lookup"><span data-stu-id="a5516-226">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="a5516-227">Ниже показан этот текст по умолчанию на странице входа.</span><span class="sxs-lookup"><span data-stu-id="a5516-227">The following shows this default text on the sign-in page.</span></span>

![Текст по умолчанию для ссылки забытого пароля на странице входа](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="a5516-229">Однако в файле global.json для библиотеке модулей в модуле входа можно изменить текст на **Не помните пароль?**, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="a5516-229">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Обновленный текст ссылки в файле global.json модуля входа](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="a5516-231">После обновления файла global.json и публикации изменений новый текст ссылки появляется в модуле входа как в Commerce, так и на опубликованной странице входа.</span><span class="sxs-lookup"><span data-stu-id="a5516-231">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5516-232">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a5516-232">Additional resources</span></span>

[<span data-ttu-id="a5516-233">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="a5516-233">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a5516-234">Развертывание нового клиента электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="a5516-234">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a5516-235">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="a5516-235">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a5516-236">Связывание сайта Dynamics 365 Commerce с интернет-каналом</span><span class="sxs-lookup"><span data-stu-id="a5516-236">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a5516-237">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="a5516-237">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a5516-238">Пакетная отправка перенаправлений URL-адресов</span><span class="sxs-lookup"><span data-stu-id="a5516-238">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a5516-239">Настройка клиента B2C в Commerce</span><span class="sxs-lookup"><span data-stu-id="a5516-239">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a5516-240">Настройка нескольких клиентов B2C в среде Commerce</span><span class="sxs-lookup"><span data-stu-id="a5516-240">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a5516-241">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="a5516-241">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a5516-242">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="a5516-242">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
