---
title: Аутентификация
description: В этой статье приводятся общие сведения об аутентификации в API Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 963bec2b817c59e3b5860c5ff5885e165ec8656a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115568"
---
# <a name="authentication"></a><span data-ttu-id="12cb5-103">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="12cb5-103">Authentication</span></span>

<span data-ttu-id="12cb5-104">В этой статье приводятся общие сведения об аутентификации в API Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="12cb5-104">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="12cb5-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="12cb5-105">Overview</span></span>

<span data-ttu-id="12cb5-106">API данных для Human Resources является реализацией OData.</span><span class="sxs-lookup"><span data-stu-id="12cb5-106">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="12cb5-107">Дополнительные сведения см. в разделе [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="12cb5-107">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="12cb5-108">Приложение должно пройти аутентификацию как авторизованный вызывающий объект, прежде чем API будет обслуживать запросы из вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="12cb5-108">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="12cb5-109">Основы</span><span class="sxs-lookup"><span data-stu-id="12cb5-109">Fundamentals</span></span>

<span data-ttu-id="12cb5-110">Для вызова API данных приложение должно получить маркер доступа от платформы удостоверений Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="12cb5-110">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="12cb5-111">Маркер доступа содержит сведения о приложении и разрешение на вызов ресурсов в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="12cb5-111">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="12cb5-112">Маркер доступа</span><span class="sxs-lookup"><span data-stu-id="12cb5-112">Access token</span></span>

<span data-ttu-id="12cb5-113">Маркеры доступа, выдаваемые платформой удостоверений Майкрософт, представляют собой веб-маркеры JavaScript JSON base64 (JWT).</span><span class="sxs-lookup"><span data-stu-id="12cb5-113">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="12cb5-114">Они содержат информацию (заявки), которую API данных (и другие веб-интерфейсы API, защищенные платформой удостоверений Майкрософт) используют для проверки вызывающего объекта и проверки наличия у вызывающего объектов необходимых разрешений на выполнение запрашиваемой операции.</span><span class="sxs-lookup"><span data-stu-id="12cb5-114">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="12cb5-115">Во время вызова маркеры доступа можно рассматривать как непрозрачные.</span><span class="sxs-lookup"><span data-stu-id="12cb5-115">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="12cb5-116">Следует всегда передавать маркеры доступа по безопасному каналу, такому как TLS и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="12cb5-116">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="12cb5-117">Ниже приводится пример маркера доступа, выданного платформой удостоверений Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="12cb5-117">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="12cb5-118">Для вызова API данных маркер доступа прикрепляются как заголовок носителя в заголовке авторизации в HTTP-запросе.</span><span class="sxs-lookup"><span data-stu-id="12cb5-118">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="12cb5-119">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="12cb5-119">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="12cb5-120">Регистрация нового приложения на портале Azure</span><span class="sxs-lookup"><span data-stu-id="12cb5-120">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="12cb5-121">Выполните вход на [Портал Microsoft Azure](https://portal.azure.com) с рабочей или учебной учетной записью или личной учетной записью Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="12cb5-121">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="12cb5-122">Если учетная запись позволяет получить доступ к нескольким клиентам, выберите учетную запись в верхнем правом углу и настройте свой сеанс портала для нужного клиента Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="12cb5-122">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="12cb5-123">В левой области выберите службу **Azure Active Directory**, а затем выберите **Регистрация приложений \> Новая регистрация**.</span><span class="sxs-lookup"><span data-stu-id="12cb5-123">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="12cb5-124">Когда появится страница **Регистрация приложения**, введите регистрационную информацию приложения:</span><span class="sxs-lookup"><span data-stu-id="12cb5-124">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="12cb5-125">**Имя**: введите понятное имя приложения, которое будет отображаться пользователям приложения.</span><span class="sxs-lookup"><span data-stu-id="12cb5-125">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="12cb5-126">**Поддерживаемые типы учетных записей**: выберите типы учетных записей, которые должны поддерживаться вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="12cb5-126">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="12cb5-127">Поддерживаемые типы счетов</span><span class="sxs-lookup"><span data-stu-id="12cb5-127">Supported account types</span></span> | <span data-ttu-id="12cb5-128">Описание</span><span class="sxs-lookup"><span data-stu-id="12cb5-128">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="12cb5-129">Учетные записи только в данном каталоге организации</span><span class="sxs-lookup"><span data-stu-id="12cb5-129">Accounts in this organizational directory only</span></span> | <span data-ttu-id="12cb5-130">Этот параметр выбирается при создании бизнес-приложения.</span><span class="sxs-lookup"><span data-stu-id="12cb5-130">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="12cb5-131">Этот параметр доступен только в том случае, если приложение регистрируется в каталоге.</span><span class="sxs-lookup"><span data-stu-id="12cb5-131">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="12cb5-132">Этот параметр сопоставлен с **Только один клиент Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="12cb5-132">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="12cb5-133">Этот параметр используется по умолчанию, если только вы не регистрируете приложение вне каталога.</span><span class="sxs-lookup"><span data-stu-id="12cb5-133">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="12cb5-134">В этом случае параметром по умолчанию является **Несколько клиентов Azure AD и личные учетные записи Майкрософт**.</span><span class="sxs-lookup"><span data-stu-id="12cb5-134">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="12cb5-135">Учетные записи в любом каталоге организации</span><span class="sxs-lookup"><span data-stu-id="12cb5-135">Accounts in any organizational directory</span></span> | <span data-ttu-id="12cb5-136">Этот параметр выбирается для целей всех бизнес- и образовательных клиентов.</span><span class="sxs-lookup"><span data-stu-id="12cb5-136">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="12cb5-137">Этот параметр сопоставлен с **Только несколько клиентов Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="12cb5-137">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="12cb5-138">Если вы зарегистрировали приложение как **Только один клиент Azure AD**, вы можете использовать колонку **Аутентификация**, чтобы обновить до **Только несколько клиентов Azure AD**, а затем обратно на **Только один клиентAzure AD**.</span><span class="sxs-lookup"><span data-stu-id="12cb5-138">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="12cb5-139">Учетные записи в любом организационном каталоге и личные учетные записи Майкрософт</span><span class="sxs-lookup"><span data-stu-id="12cb5-139">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="12cb5-140">Этот параметр предназначен для самого широкого набора клиентов.</span><span class="sxs-lookup"><span data-stu-id="12cb5-140">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="12cb5-141">Этот параметр сопоставлен с **Несколько клиентов Azure AD и личные учетные записи Майкрософт**.</span><span class="sxs-lookup"><span data-stu-id="12cb5-141">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="12cb5-142">Если вы зарегистрировали приложение как **Несколько клиентов Azure AD и личные учетные записи Майкрософт**, вы не сможете изменить этот параметр в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="12cb5-142">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="12cb5-143">Вместо этого необходимо изменить поддерживаемые типы учетных записей с помощью редактора манифестов приложений.</span><span class="sxs-lookup"><span data-stu-id="12cb5-143">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="12cb5-144">**URI перенаправления (необязательно)** — выберите тип создаваемого приложения: **веб-приложение** или **общедоступный клиент (мобильный и классический)**.</span><span class="sxs-lookup"><span data-stu-id="12cb5-144">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="12cb5-145">Затем введите URI перенаправления (или URL-адрес ответа) для приложения.</span><span class="sxs-lookup"><span data-stu-id="12cb5-145">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="12cb5-146">Для веб-приложений укажите базовый URL-адрес приложения.</span><span class="sxs-lookup"><span data-stu-id="12cb5-146">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="12cb5-147">Например, `http://localhost:31544` может быть URL-адресом для веб-приложения, которое выполняется на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="12cb5-147">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="12cb5-148">Пользователи затем используют этот URL-адрес для входа в приложение веб-клиента.</span><span class="sxs-lookup"><span data-stu-id="12cb5-148">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="12cb5-149">Для общедоступных клиентских приложений необходимо предоставить URI, который Azure AD будет использоваться для возврата ответов маркеров.</span><span class="sxs-lookup"><span data-stu-id="12cb5-149">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="12cb5-150">Введите конкретное значение, которое относится к приложению, например `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="12cb5-150">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="12cb5-151">Чтобы просмотреть отдельные примеры для веб-приложений или собственных приложений, см. краткие руководства для [платформы удостоверений Майкрософт (раньше Azure Active Directory для разработчиков)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="12cb5-151">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="12cb5-152">В **Разрешения API** выберите **Добавить разрешение**.</span><span class="sxs-lookup"><span data-stu-id="12cb5-152">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="12cb5-153">Затем на вкладке **Используемые в моей организации API** найдите **Dynamics 365 Human Resources** и добавьте разрешение **user\_impersonation** в свое приложение.</span><span class="sxs-lookup"><span data-stu-id="12cb5-153">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="12cb5-154">Код приложения для Human Resources — f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="12cb5-154">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="12cb5-155">Этот код используется для проверки правильности выбора приложения.</span><span class="sxs-lookup"><span data-stu-id="12cb5-155">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="12cb5-156">Выберите **Регистр**.</span><span class="sxs-lookup"><span data-stu-id="12cb5-156">Select **Register**.</span></span>

   <span data-ttu-id="12cb5-157">[![Регистрация нового приложения на портале Azure](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="12cb5-157">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="12cb5-158">Azure AD назначает уникальный код приложения (код клиента) вашему приложению и открывает страницу **Обзор** для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="12cb5-158">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="12cb5-159">Чтобы добавить дополнительные возможности в приложение, можно выбрать другие параметры конфигурации, такие как параметры фирменной символики, а также для сертификатов и секретности.</span><span class="sxs-lookup"><span data-stu-id="12cb5-159">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="12cb5-160">Получение маркера доступа</span><span class="sxs-lookup"><span data-stu-id="12cb5-160">Retrieving an access token</span></span>

<span data-ttu-id="12cb5-161">Особенности получения маркера доступа для вызова API данных Human Resources будет зависеть от того, какие технологии используются вами при разработке клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="12cb5-161">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="12cb5-162">Например, вы можете выполнять [тестирование с помощью сторонней служебной программы](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (например, Postman), разработку консольного приложения или веб-службы C# или создание клиента JavaScript/TypeScript.</span><span class="sxs-lookup"><span data-stu-id="12cb5-162">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="12cb5-163">Пример клиентского приложения C#:</span><span class="sxs-lookup"><span data-stu-id="12cb5-163">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="12cb5-164">После получения маркера доступа вы передадите маркер в заголовке авторизации как маркер носителя с каждым запросом, отправляемым в API данных, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="12cb5-164">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>
