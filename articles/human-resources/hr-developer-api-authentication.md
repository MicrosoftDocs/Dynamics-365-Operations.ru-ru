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
# <a name="authentication"></a>Аутентификация

В этой статье приводятся общие сведения об аутентификации в API Microsoft Dynamics 365 Human Resources.

## <a name="overview"></a>Обзор

API данных для Human Resources является реализацией OData. Дополнительные сведения см. в разделе [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).

Приложение должно пройти аутентификацию как авторизованный вызывающий объект, прежде чем API будет обслуживать запросы из вашего приложения.

## <a name="fundamentals"></a>Основы

Для вызова API данных приложение должно получить маркер доступа от платформы удостоверений Майкрософт. Маркер доступа содержит сведения о приложении и разрешение на вызов ресурсов в Human Resources.

### <a name="access-token"></a>Маркер доступа

Маркеры доступа, выдаваемые платформой удостоверений Майкрософт, представляют собой веб-маркеры JavaScript JSON base64 (JWT). Они содержат информацию (заявки), которую API данных (и другие веб-интерфейсы API, защищенные платформой удостоверений Майкрософт) используют для проверки вызывающего объекта и проверки наличия у вызывающего объектов необходимых разрешений на выполнение запрашиваемой операции. Во время вызова маркеры доступа можно рассматривать как непрозрачные. Следует всегда передавать маркеры доступа по безопасному каналу, такому как TLS и HTTPS.

Ниже приводится пример маркера доступа, выданного платформой удостоверений Майкрософт.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Для вызова API данных маркер доступа прикрепляются как заголовок носителя в заголовке авторизации в HTTP-запросе. Рассмотрим пример:

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Регистрация нового приложения на портале Azure

1. Выполните вход на [Портал Microsoft Azure](https://portal.azure.com) с рабочей или учебной учетной записью или личной учетной записью Майкрософт.

2. Если учетная запись позволяет получить доступ к нескольким клиентам, выберите учетную запись в верхнем правом углу и настройте свой сеанс портала для нужного клиента Azure Active Directory (Azure AD).

3. В левой области выберите службу **Azure Active Directory**, а затем выберите **Регистрация приложений \> Новая регистрация**.

4. Когда появится страница **Регистрация приложения**, введите регистрационную информацию приложения:

    - **Имя**: введите понятное имя приложения, которое будет отображаться пользователям приложения.
    - **Поддерживаемые типы учетных записей**: выберите типы учетных записей, которые должны поддерживаться вашим приложением.

        | Поддерживаемые типы счетов | Описание |
        |-------------------------|-------------|
        | Учетные записи только в данном каталоге организации | Этот параметр выбирается при создании бизнес-приложения. Этот параметр доступен только в том случае, если приложение регистрируется в каталоге.<p>Этот параметр сопоставлен с **Только один клиент Azure AD**.</p><p>Этот параметр используется по умолчанию, если только вы не регистрируете приложение вне каталога. В этом случае параметром по умолчанию является **Несколько клиентов Azure AD и личные учетные записи Майкрософт**.</p> |
        | Учетные записи в любом каталоге организации | Этот параметр выбирается для целей всех бизнес- и образовательных клиентов.<p>Этот параметр сопоставлен с **Только несколько клиентов Azure AD**.</p><p>Если вы зарегистрировали приложение как **Только один клиент Azure AD**, вы можете использовать колонку **Аутентификация**, чтобы обновить до **Только несколько клиентов Azure AD**, а затем обратно на **Только один клиентAzure AD**.</p> |
        | Учетные записи в любом организационном каталоге и личные учетные записи Майкрософт | Этот параметр предназначен для самого широкого набора клиентов.<p>Этот параметр сопоставлен с **Несколько клиентов Azure AD и личные учетные записи Майкрософт**.</p><p>Если вы зарегистрировали приложение как **Несколько клиентов Azure AD и личные учетные записи Майкрософт**, вы не сможете изменить этот параметр в пользовательском интерфейсе. Вместо этого необходимо изменить поддерживаемые типы учетных записей с помощью редактора манифестов приложений.</p> |

    - **URI перенаправления (необязательно)** — выберите тип создаваемого приложения: **веб-приложение** или **общедоступный клиент (мобильный и классический)**. Затем введите URI перенаправления (или URL-адрес ответа) для приложения.

        - Для веб-приложений укажите базовый URL-адрес приложения. Например, `http://localhost:31544` может быть URL-адресом для веб-приложения, которое выполняется на локальном компьютере. Пользователи затем используют этот URL-адрес для входа в приложение веб-клиента.
        - Для общедоступных клиентских приложений необходимо предоставить URI, который Azure AD будет использоваться для возврата ответов маркеров. Введите конкретное значение, которое относится к приложению, например `myapp://auth`.

        Чтобы просмотреть отдельные примеры для веб-приложений или собственных приложений, см. краткие руководства для [платформы удостоверений Майкрософт (раньше Azure Active Directory для разработчиков)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).

5. В **Разрешения API** выберите **Добавить разрешение**. Затем на вкладке **Используемые в моей организации API** найдите **Dynamics 365 Human Resources** и добавьте разрешение **user\_impersonation** в свое приложение. Код приложения для Human Resources — f9be0c49-aa22-4ec6-911a-c5da515226ff. Этот код используется для проверки правильности выбора приложения.

6. Выберите **Регистр**.

   [![Регистрация нового приложения на портале Azure](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD назначает уникальный код приложения (код клиента) вашему приложению и открывает страницу **Обзор** для вашего приложения. Чтобы добавить дополнительные возможности в приложение, можно выбрать другие параметры конфигурации, такие как параметры фирменной символики, а также для сертификатов и секретности.

## <a name="retrieving-an-access-token"></a>Получение маркера доступа

Особенности получения маркера доступа для вызова API данных Human Resources будет зависеть от того, какие технологии используются вами при разработке клиентского приложения. Например, вы можете выполнять [тестирование с помощью сторонней служебной программы](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (например, Postman), разработку консольного приложения или веб-службы C# или создание клиента JavaScript/TypeScript.

Пример клиентского приложения C#:
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

После получения маркера доступа вы передадите маркер в заголовке авторизации как маркер носителя с каждым запросом, отправляемым в API данных, как описано выше.
