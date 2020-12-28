---
title: Надстройка видимости запасов
description: В этом разделе описывается, как установить и настроить настройку отображения запасов для Dynamics 365 Supply Chain Management.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625073"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="3a658-103">Надстройка видимости запасов</span><span class="sxs-lookup"><span data-stu-id="3a658-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3a658-104">Надстройка для отображения запасов — это независимая и масштабируемая микрослужба, позволяющая осуществлять отслеживание запасов в наличии в реальном времени, обеспечивая таким образом глобальное представление отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="3a658-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="3a658-105">Вся информация, относящаяся к запасам в наличии, экспортируется в службу практически в реальном времени с помощью SQL-интеграции низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="3a658-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="3a658-106">Внешние системы обращаются к службе через API RESTful для запроса информации о наличии по заданным наборам аналитик, тем самым получая список доступных позиций в наличии.</span><span class="sxs-lookup"><span data-stu-id="3a658-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="3a658-107">Видимость запасов — это микрослужба, основанная на Common Data Service, что означает, что ее можно расширить путем создания приложений Power Apps и применения Power BI для предоставления настраиваемых функций в соответствии с потребностями бизнеса.</span><span class="sxs-lookup"><span data-stu-id="3a658-107">Inventory Visibility is a microservice built on the Common Data Service, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="3a658-108">Возможно также обновление индекса для выполнения складских запросов.</span><span class="sxs-lookup"><span data-stu-id="3a658-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="3a658-109">Видимость запасов предоставляет параметры конфигурации, которые позволяют ей интегрироваться с несколькими системами сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="3a658-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="3a658-110">Она поддерживает стандартизированную складскую аналитику, настраиваемую расширяемость и стандартизованные настраиваемые подсчитанные количества.</span><span class="sxs-lookup"><span data-stu-id="3a658-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="3a658-111">В этом разделе описывается, как установить и настроить настройку отображения запасов для Dynamics 365 Supply Chain Management и как использовать ее интерфейс программирования приложений (API).</span><span class="sxs-lookup"><span data-stu-id="3a658-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="3a658-112">Установка надстройки видимости запасов</span><span class="sxs-lookup"><span data-stu-id="3a658-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="3a658-113">Необходимо установить надстройку отображения запасов, используя Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3a658-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="3a658-114">LCS — это портал совместной работы, который предоставляет среду и набор регулярно обновленных служб, которые помогут управлять жизненным циклом приложений Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3a658-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="3a658-115">Дополнительные сведения см. в разделе [Ресурсы Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="3a658-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3a658-116">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="3a658-116">Prerequisites</span></span>

<span data-ttu-id="3a658-117">Перед установкой надстройки видимости запасов необходимо сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="3a658-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="3a658-118">Получите проект внедрения LCS с по крайней мере одной развернутой средой.</span><span class="sxs-lookup"><span data-stu-id="3a658-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="3a658-119">Создайте бета-версии ключей для предложения в LCS.</span><span class="sxs-lookup"><span data-stu-id="3a658-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="3a658-120">Активируйте ключи бета-версии для предложения для пользователя в LCS.</span><span class="sxs-lookup"><span data-stu-id="3a658-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="3a658-121">Свяжитесь с группой разработчиков Майкрософт продукта видимости запасов и предоставьте идентификатор среды, в которой необходимо развернуть надстройку отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="3a658-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="3a658-122">При возникновении каких-либо вопросов о необходимых условиях свяжитесь с группой разработчиков продукта для отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="3a658-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="3a658-123">Установка надстройки</span><span class="sxs-lookup"><span data-stu-id="3a658-123">Install the add-in</span></span>

<span data-ttu-id="3a658-124">Чтобы установить надстройку видимости запасов, необходимо сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="3a658-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="3a658-125">Выполните вход на портал [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="3a658-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="3a658-126">На домашней странице выберите проект, в котором развернута среда.</span><span class="sxs-lookup"><span data-stu-id="3a658-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="3a658-127">На странице проекта выберите среду, в которой требуется установить надстройку.</span><span class="sxs-lookup"><span data-stu-id="3a658-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="3a658-128">На странице среды прокрутите вниз, чтобы увидеть раздел **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="3a658-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="3a658-129">Если раздел не отображается, убедитесь, что все необходимые для него ключи бета-версии были полностью обработаны.</span><span class="sxs-lookup"><span data-stu-id="3a658-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="3a658-130">В разделе **Надстройки сред** выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="3a658-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="3a658-131">![Страница среды в LCS](media/inventory-visibility-environment.png "Страница среды в LCS")</span><span class="sxs-lookup"><span data-stu-id="3a658-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="3a658-132">Выберите ссылку **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="3a658-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="3a658-133">Откроется список доступных надстроек.</span><span class="sxs-lookup"><span data-stu-id="3a658-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="3a658-134">Выберите **Складская служба** из списка.</span><span class="sxs-lookup"><span data-stu-id="3a658-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="3a658-135">(Обратите внимание, что сейчас она может быть указана как **Надстройка для отображения запасов для Dynamics 365 Supply Chain Management**.)</span><span class="sxs-lookup"><span data-stu-id="3a658-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="3a658-136">Введите значения для следующих полей для вашей среды:</span><span class="sxs-lookup"><span data-stu-id="3a658-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="3a658-137">**Код приложения AAD**</span><span class="sxs-lookup"><span data-stu-id="3a658-137">**AAD application ID**</span></span>
    - <span data-ttu-id="3a658-138">**Код арендатора AAD**</span><span class="sxs-lookup"><span data-stu-id="3a658-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="3a658-139">![Страница настройки надстройки](media/inventory-visibility-setup.png "Страница настройки надстройки")</span><span class="sxs-lookup"><span data-stu-id="3a658-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="3a658-140">Примите условия, установив флажок **Условия**.</span><span class="sxs-lookup"><span data-stu-id="3a658-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="3a658-141">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="3a658-141">Select **Install**.</span></span> <span data-ttu-id="3a658-142">Статус надстройки будет отображаться как **Установка**.</span><span class="sxs-lookup"><span data-stu-id="3a658-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="3a658-143">После завершения обновите страницу, чтобы увидеть статус, измененный на **Установлено**.</span><span class="sxs-lookup"><span data-stu-id="3a658-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="3a658-144">Получение маркера службы безопасности</span><span class="sxs-lookup"><span data-stu-id="3a658-144">Get a security service token</span></span>

<span data-ttu-id="3a658-145">Чтобы получить маркер службы безопасности, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3a658-145">To get a security service token, do the following:</span></span>

1. <span data-ttu-id="3a658-146">Получите `aadToken` и вызовите конечную точку: https://securityservice.operations365.dynamics.com/token.</span><span class="sxs-lookup"><span data-stu-id="3a658-146">Get your `aadToken` and call the endpoint: https://securityservice.operations365.dynamics.com/token.</span></span>
1. <span data-ttu-id="3a658-147">Замените `client_assertion` в основном тексте на `aadToken`.</span><span class="sxs-lookup"><span data-stu-id="3a658-147">Replace the `client_assertion` in the body with your `aadToken`.</span></span>
1. <span data-ttu-id="3a658-148">Замените контекст в основном тексте средой, в которой требуется развернуть надстройку.</span><span class="sxs-lookup"><span data-stu-id="3a658-148">Replace the context in the body with the environment where you want to deploy the add-in.</span></span>
1. <span data-ttu-id="3a658-149">Замените область в основном тексте следующим:</span><span class="sxs-lookup"><span data-stu-id="3a658-149">Replace the scope in the body with the following:</span></span>

    - <span data-ttu-id="3a658-150">Область для MCK — "https://inventoryservice.operations365.dynamics.cn/.default"</span><span class="sxs-lookup"><span data-stu-id="3a658-150">Scope for MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span></span>  
    <span data-ttu-id="3a658-151">(Код приложения и код клиента Azure Active Directory для MCK можно найти в `appsettings.mck.json`.)</span><span class="sxs-lookup"><span data-stu-id="3a658-151">(You can find the Azure Active Directory application ID and tenant ID for MCK in `appsettings.mck.json`.)</span></span>
    - <span data-ttu-id="3a658-152">Область для PROD — "https://inventoryservice.operations365.dynamics.com/.default"</span><span class="sxs-lookup"><span data-stu-id="3a658-152">Scope for PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span></span>  
    <span data-ttu-id="3a658-153">(Код приложения и код клиента Azure Active Directory для PROD можно найти в `appsettings.prod.json`.)</span><span class="sxs-lookup"><span data-stu-id="3a658-153">(You can find the Azure Active Directory application ID and tenant ID for PROD in `appsettings.prod.json`.)</span></span>

    <span data-ttu-id="3a658-154">Результат должен быть похож на следующий пример.</span><span class="sxs-lookup"><span data-stu-id="3a658-154">The result should resemble the following example.</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. <span data-ttu-id="3a658-155">В ответе вы получите `access_token`.</span><span class="sxs-lookup"><span data-stu-id="3a658-155">You will get an `access_token` in response.</span></span> <span data-ttu-id="3a658-156">Это то, что требуется в качестве маркера носителя для вызова API отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="3a658-156">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="3a658-157">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="3a658-157">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="3a658-158">Удаление надстройки</span><span class="sxs-lookup"><span data-stu-id="3a658-158">Uninstall the add-in</span></span>

<span data-ttu-id="3a658-159">Чтобы удалить надстройку, выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="3a658-159">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="3a658-160">Обновите LCS, и надстройка для отображения запасов будет удалена.</span><span class="sxs-lookup"><span data-stu-id="3a658-160">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="3a658-161">Процесс удаления приведет к удалению регистрации надстройки, а также запуску задания для очистки всех бизнес-данных, хранящихся в службе.</span><span class="sxs-lookup"><span data-stu-id="3a658-161">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="3a658-162">Открытый API-интерфейс надстройки видимости запасов</span><span class="sxs-lookup"><span data-stu-id="3a658-162">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="3a658-163">Открытый интерфейс REST API надстройки отображения запасов представляет несколько определенных конечных точек интеграции.</span><span class="sxs-lookup"><span data-stu-id="3a658-163">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="3a658-164">Он поддерживает три основных типа взаимодействий:</span><span class="sxs-lookup"><span data-stu-id="3a658-164">It supports three main interaction types:</span></span>

- <span data-ttu-id="3a658-165">Разноска изменений запасов в наличии в надстройку из внешней системы.</span><span class="sxs-lookup"><span data-stu-id="3a658-165">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="3a658-166">Запрос текущих количеств в наличии из внешней системы.</span><span class="sxs-lookup"><span data-stu-id="3a658-166">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="3a658-167">Автоматическая синхронизация с запасами в наличии в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3a658-167">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="3a658-168">Автоматическая синхронизация не является частью общедоступного интерфейса API, но вместо этого обрабатывается в фоновом режиме для сред, в которых включена надстройка для отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="3a658-168">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="3a658-169">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="3a658-169">Authentication</span></span>

<span data-ttu-id="3a658-170">Маркер безопасности платформы используется для вызова надстройки для отображения запасов, поэтому необходимо создать маркер Azure Active Directory с помощью приложения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3a658-170">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="3a658-171">Дополнительные сведения о том, как получить маркер безопасности, см. в разделе [Установка надстройки для отображения запасов](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="3a658-171">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="3a658-172">Настройка интерфейса API для отображения запасов</span><span class="sxs-lookup"><span data-stu-id="3a658-172">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="3a658-173">Перед использованием службы необходимо выполнить конфигурации, описанные в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="3a658-173">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="3a658-174">Конфигурация может различаться в зависимости от сведений о среде.</span><span class="sxs-lookup"><span data-stu-id="3a658-174">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="3a658-175">В основном она включает четыре части:</span><span class="sxs-lookup"><span data-stu-id="3a658-175">It primarily includes four parts:</span></span>

- [<span data-ttu-id="3a658-176">Секционирование</span><span class="sxs-lookup"><span data-stu-id="3a658-176">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="3a658-177">Конфигурации аналитик</span><span class="sxs-lookup"><span data-stu-id="3a658-177">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="3a658-178">Индексация</span><span class="sxs-lookup"><span data-stu-id="3a658-178">Indexing</span></span>](#indexing)
- [<span data-ttu-id="3a658-179">Пользовательское измерение</span><span class="sxs-lookup"><span data-stu-id="3a658-179">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="3a658-180">Секционирование</span><span class="sxs-lookup"><span data-stu-id="3a658-180">Partitioning</span></span>

<span data-ttu-id="3a658-181">Секционирование может значительно повлиять на производительность API отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="3a658-181">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="3a658-182">Рекомендуется определить схему, позволяющую выполнять небольшие группирования данных, сохраняя при этом возможность осмысленных запросов данных.</span><span class="sxs-lookup"><span data-stu-id="3a658-182">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="3a658-183">`organizationId` (`dataAreaId` в Supply Chain Management) всегда будет частью секционирования, и по умолчанию для отображения запасов устанавливается секционирование по аналитикам, таким как *Сайт + Местоположение*.</span><span class="sxs-lookup"><span data-stu-id="3a658-183">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="3a658-184">Это означает, что служба должна всегда запрашиваться с этими аналитиками, определенными в фильтрах.</span><span class="sxs-lookup"><span data-stu-id="3a658-184">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="3a658-185">*Сайт* и *Местоположение* — это две общих аналитики по умолчанию в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="3a658-185">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="3a658-186">В Supply Chain Management эти аналитики называются *Сайт* (`InventSiteId`) и *Склад* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="3a658-186">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="3a658-187">Конфигурации аналитик</span><span class="sxs-lookup"><span data-stu-id="3a658-187">Dimension configurations</span></span>

<span data-ttu-id="3a658-188">Видимость запасов представляет список основных аналитик по умолчанию для включения интеграции нескольких источников в систему.</span><span class="sxs-lookup"><span data-stu-id="3a658-188">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="3a658-189">В следующей таблице перечислены складские аналитики, которые будут именами аналитик по умолчанию в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="3a658-189">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="3a658-190">Тип аналитики</span><span class="sxs-lookup"><span data-stu-id="3a658-190">Dimension type</span></span> | <span data-ttu-id="3a658-191">Имя аналитики</span><span class="sxs-lookup"><span data-stu-id="3a658-191">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="3a658-192">Продукт</span><span class="sxs-lookup"><span data-stu-id="3a658-192">Product</span></span> | `ColorId` |
| <span data-ttu-id="3a658-193">Продукт</span><span class="sxs-lookup"><span data-stu-id="3a658-193">Product</span></span> | `SizeId` |
| <span data-ttu-id="3a658-194">Продукт</span><span class="sxs-lookup"><span data-stu-id="3a658-194">Product</span></span> | `StyleId` |
| <span data-ttu-id="3a658-195">Продукт</span><span class="sxs-lookup"><span data-stu-id="3a658-195">Product</span></span> | `ConfigId` |
| <span data-ttu-id="3a658-196">Отслеживание</span><span class="sxs-lookup"><span data-stu-id="3a658-196">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="3a658-197">Отслеживание</span><span class="sxs-lookup"><span data-stu-id="3a658-197">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="3a658-198">Расположение</span><span class="sxs-lookup"><span data-stu-id="3a658-198">Location</span></span> | `LocationId` |
| <span data-ttu-id="3a658-199">Расположение</span><span class="sxs-lookup"><span data-stu-id="3a658-199">Location</span></span> | `SiteId` |
| <span data-ttu-id="3a658-200">Статус запасов</span><span class="sxs-lookup"><span data-stu-id="3a658-200">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="3a658-201">Зависит от склада</span><span class="sxs-lookup"><span data-stu-id="3a658-201">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="3a658-202">Зависит от склада</span><span class="sxs-lookup"><span data-stu-id="3a658-202">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="3a658-203">Зависит от склада</span><span class="sxs-lookup"><span data-stu-id="3a658-203">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="3a658-204">Тип аналитики, приведенный в предыдущей таблице, используется только для справки.</span><span class="sxs-lookup"><span data-stu-id="3a658-204">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="3a658-205">Нет необходимости определять тип аналитики в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="3a658-205">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="3a658-206">Если имеется настраиваемая аналитика, которая должна перетекать в значение по умолчанию при потреблении видимостью запасов, можно настроить имя **настраиваемой аналитики** в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="3a658-206">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="3a658-207">Внешние системы получают доступ к видимости запасов через интерфейсы API RESTful, которые позволяют запрашивать информацию о наличии по данным наборам аналитик.</span><span class="sxs-lookup"><span data-stu-id="3a658-207">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="3a658-208">Для интеграции видимость запасов позволяет настроить *источник данных внешнего канала* и исходную аналитику на *целевые аналитики* в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="3a658-208">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="3a658-209">Целевые аналитики должны быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="3a658-209">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="3a658-210">Аналитики по умолчанию в видимости запасов</span><span class="sxs-lookup"><span data-stu-id="3a658-210">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="3a658-211">Настраиваемые аналитики</span><span class="sxs-lookup"><span data-stu-id="3a658-211">Custom dimensions</span></span>

<span data-ttu-id="3a658-212">Целью настройки аналитики является стандартизация интеграции нескольких систем для запроса по аналитикам и события разноски с аналитиками.</span><span class="sxs-lookup"><span data-stu-id="3a658-212">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="3a658-213">Индексация</span><span class="sxs-lookup"><span data-stu-id="3a658-213">Indexing</span></span>

<span data-ttu-id="3a658-214">В большинстве случаев запрос запасов в наличии будет не только на самом высоком уровне "итога", но может потребоваться просмотреть результаты агрегирования на основе складских аналитик.</span><span class="sxs-lookup"><span data-stu-id="3a658-214">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="3a658-215">Видимость запасов обеспечивает гибкость, позволяя настраивать индексы, которые основаны на аналитике или комбинации аналитик.</span><span class="sxs-lookup"><span data-stu-id="3a658-215">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="3a658-216">В настоящее время для индексов можно настроить не более пяти.</span><span class="sxs-lookup"><span data-stu-id="3a658-216">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="3a658-217">Необходимо тщательно продумать, какая аналитика или комбинация аналитик будет использоваться, перед реализацией, чтобы обеспечить, что она будут удовлетворять вашим деловым потребностям.</span><span class="sxs-lookup"><span data-stu-id="3a658-217">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="3a658-218">Например, если требуется запросить продукты следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3a658-218">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="3a658-219">Запрос агрегированного наличия продуктов по аналитикам *Цвет* и *Размер*.</span><span class="sxs-lookup"><span data-stu-id="3a658-219">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="3a658-220">В некоторых случаях требуется только выполнить запрос по продукту в целом.</span><span class="sxs-lookup"><span data-stu-id="3a658-220">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="3a658-221">Можно определить два индекса следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3a658-221">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="3a658-222">Пустая скобка будет агрегирована на основе идентификатора продукта в секции.</span><span class="sxs-lookup"><span data-stu-id="3a658-222">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="3a658-223">Индексация определяет способ группировки результатов в зависимости от настройки запроса `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="3a658-223">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="3a658-224">В этом случае, если никакие значения `groupBy` не определены, будут выведены итоги по `productid`.</span><span class="sxs-lookup"><span data-stu-id="3a658-224">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="3a658-225">В противном случае, если определить `groupBy` как `groupBy=ColorId&groupBy=SizeId`, будет возвращено несколько строк, в зависимости от различных комбинаций цвета и размера в системе.</span><span class="sxs-lookup"><span data-stu-id="3a658-225">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="3a658-226">Критерии запроса можно разместить в теле запроса.</span><span class="sxs-lookup"><span data-stu-id="3a658-226">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="3a658-227">Вот пример запроса для комбинации цвета и размера продукта.</span><span class="sxs-lookup"><span data-stu-id="3a658-227">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="3a658-228">Пользовательское измерение</span><span class="sxs-lookup"><span data-stu-id="3a658-228">Custom measurement</span></span>

<span data-ttu-id="3a658-229">Количества измерений по умолчанию связаны с Supply Chain Management, однако можно иметь количество, состоящее из комбинации измерений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3a658-229">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="3a658-230">Чтобы сделать это, можно задать конфигурацию настраиваемых количеств, которая будет добавлена к выходным данным запросов запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="3a658-230">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="3a658-231">Функциональность просто позволяют определить набор мер, которые будут добавлены, и/или набор мер, которые будут вычтены, чтобы сформировать настраиваемое измерение.</span><span class="sxs-lookup"><span data-stu-id="3a658-231">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="3a658-232">Например, со следующим условием запроса вы настроите пользовательское количество измерения как `MyCustomAvailableforReservation` для потребления системой потребления.</span><span class="sxs-lookup"><span data-stu-id="3a658-232">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="3a658-233">Система потребления</span><span class="sxs-lookup"><span data-stu-id="3a658-233">Consumption system</span></span> | <span data-ttu-id="3a658-234">Рассчитанные меры</span><span class="sxs-lookup"><span data-stu-id="3a658-234">Calculated measurers</span></span> | <span data-ttu-id="3a658-235">Иcточник данных</span><span class="sxs-lookup"><span data-stu-id="3a658-235">Data source</span></span> | <span data-ttu-id="3a658-236">Модификатор</span><span class="sxs-lookup"><span data-stu-id="3a658-236">Modifier</span></span> | <span data-ttu-id="3a658-237">Тип расчета модификатора</span><span class="sxs-lookup"><span data-stu-id="3a658-237">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="3a658-238">Сложение</span><span class="sxs-lookup"><span data-stu-id="3a658-238">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="3a658-239">Сложение</span><span class="sxs-lookup"><span data-stu-id="3a658-239">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="3a658-240">Вычитание</span><span class="sxs-lookup"><span data-stu-id="3a658-240">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="3a658-241">Сложение</span><span class="sxs-lookup"><span data-stu-id="3a658-241">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="3a658-242">Вычитание</span><span class="sxs-lookup"><span data-stu-id="3a658-242">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="3a658-243">Сложение</span><span class="sxs-lookup"><span data-stu-id="3a658-243">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="3a658-244">Сложение</span><span class="sxs-lookup"><span data-stu-id="3a658-244">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="3a658-245">Вычитание</span><span class="sxs-lookup"><span data-stu-id="3a658-245">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="3a658-246">Вычитание</span><span class="sxs-lookup"><span data-stu-id="3a658-246">Subtraction</span></span> |

<span data-ttu-id="3a658-247">При этом запрос настраиваемого количества измерения возвратит следующий результат.</span><span class="sxs-lookup"><span data-stu-id="3a658-247">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="3a658-248">Выходные данные `MyCustomAvailableforReservation` основаны на параметрах расчета в настраиваемых измерениях следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3a658-248">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="3a658-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="3a658-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="3a658-250">Разноска изменений запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="3a658-250">Posting on-hand changes</span></span>

<span data-ttu-id="3a658-251">Точный URL-адрес, на который будет разнесено событие, будет зависеть от географического региона.</span><span class="sxs-lookup"><span data-stu-id="3a658-251">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="3a658-252">Он будет иметь вид:</span><span class="sxs-lookup"><span data-stu-id="3a658-252">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="3a658-253">После аутентификации этот URL-адрес может использоваться вместе с методом HTTP `POST` для отправки в службу событий изменения запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="3a658-253">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="3a658-254">Специальный заголовок используется для связи с службами Dynamics 365 с помощью запросов HTTP, в которых указывается идентификатор среды экземпляра Supply Chain Management, с которым связаны данные.</span><span class="sxs-lookup"><span data-stu-id="3a658-254">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="3a658-255">Пример:</span><span class="sxs-lookup"><span data-stu-id="3a658-255">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="3a658-256">Пример 1 разноски запроса изменений запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="3a658-256">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="3a658-257">В этом примере показан сценарий, в котором будет настроена конфигурация аналитики в Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3a658-257">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="3a658-258">Следующий запрос используется для настройки сопоставления измерений в Power Apps:</span><span class="sxs-lookup"><span data-stu-id="3a658-258">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="3a658-259">Теперь можно указать `dimensionDataSource` и использовать пользовательские измерения в запросах.</span><span class="sxs-lookup"><span data-stu-id="3a658-259">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="3a658-260">Система будет автоматически преобразовывать пользовательские измерения в базовые измерения.</span><span class="sxs-lookup"><span data-stu-id="3a658-260">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="3a658-261">Пример 2 разноски запроса изменений запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="3a658-261">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="3a658-262">В этом примере показан сценарий, в котором не настроены сопоставления для конфигурации аналитик в Power Apps, поэтому при разноске должны использоваться также базовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="3a658-262">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="3a658-263">Все аналитики должны быть базовыми аналитиками, если поле `dimensionDataSource` имеет значение NULL, является пустым или пробелом.</span><span class="sxs-lookup"><span data-stu-id="3a658-263">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="3a658-264">Свойства полей документов JSON</span><span class="sxs-lookup"><span data-stu-id="3a658-264">JSON document field properties</span></span>

<span data-ttu-id="3a658-265">Поля из примеров запросов JSON, приведенных выше, имеют свойства, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3a658-265">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="3a658-266">FieldID</span><span class="sxs-lookup"><span data-stu-id="3a658-266">Field ID</span></span> | <span data-ttu-id="3a658-267">описание</span><span class="sxs-lookup"><span data-stu-id="3a658-267">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="3a658-268">Уникальный код для конкретного события изменения.</span><span class="sxs-lookup"><span data-stu-id="3a658-268">A unique ID for the specific change event.</span></span> <span data-ttu-id="3a658-269">Этот код используется, чтобы гарантировать, что при возникновении ошибки при обмене данными с службой во время разноски повторная отправка события не приведет к тому, что в системе дважды будет учитываться одно и то же событие.</span><span class="sxs-lookup"><span data-stu-id="3a658-269">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="3a658-270">Идентификатор организации, связанной с событием.</span><span class="sxs-lookup"><span data-stu-id="3a658-270">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="3a658-271">Это сопоставляется с организациями Supply Chain Management или идентификаторами областей данных.</span><span class="sxs-lookup"><span data-stu-id="3a658-271">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="3a658-272">Идентификатор рассматриваемого продукта.</span><span class="sxs-lookup"><span data-stu-id="3a658-272">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="3a658-273">Количество, для которого должны быть изменены запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="3a658-273">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="3a658-274">Если, например, 10 новых бубликов были добавлены на полку, это значение было бы равно 10.</span><span class="sxs-lookup"><span data-stu-id="3a658-274">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="3a658-275">Если 3 бублика были удалены с полки или проданы, это значение было бы равно -3.</span><span class="sxs-lookup"><span data-stu-id="3a658-275">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="3a658-276">Источник данных для аналитик, используемых в разноске события изменения и запроса.</span><span class="sxs-lookup"><span data-stu-id="3a658-276">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="3a658-277">Если указан источник данных, можно использовать настраиваемые аналитики из указанного источника данных.</span><span class="sxs-lookup"><span data-stu-id="3a658-277">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="3a658-278">С помощью конфигурации аналитик видимость запасов может сопоставлять пользовательские аналитики с общими аналитиками по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3a658-278">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="3a658-279">Если параметр `dimensionDataSource` не указан, в запросах могут использоваться только общие аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3a658-279">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="3a658-280">Динамический набор пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="3a658-280">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="3a658-281">Это будет сопоставляться с некоторыми аналитиками в Supply Chain Management, но можно также добавить настраиваемые аналитики(например, *Источник*), которые могут обозначать, когда событие поступает из Supply Chain Management или из внешней системы.</span><span class="sxs-lookup"><span data-stu-id="3a658-281">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="3a658-282">Запрос текущих запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="3a658-282">Querying current on-hand</span></span>

<span data-ttu-id="3a658-283">Конечная точка для запроса текущих запасов в наличии будет иметь похожий URL-адрес:</span><span class="sxs-lookup"><span data-stu-id="3a658-283">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="3a658-284">Запрос будет выполняться с использованием метода HTTP `POST`.</span><span class="sxs-lookup"><span data-stu-id="3a658-284">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="3a658-285">Пример 1 запроса текущих запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="3a658-285">Current on-hand query example 1</span></span>

<span data-ttu-id="3a658-286">В этом примере показан сценарий, в котором вы уже выполнили настройку конфигурации аналитики в Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3a658-286">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="3a658-287">Следующий запрос используется для настройки сопоставления измерений в Power Apps:</span><span class="sxs-lookup"><span data-stu-id="3a658-287">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="3a658-288">Теперь можно указать `dimensionDataSource` и использовать пользовательские измерения в запросах.</span><span class="sxs-lookup"><span data-stu-id="3a658-288">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="3a658-289">Система будет автоматически преобразовывать пользовательские измерения в базовые измерения.</span><span class="sxs-lookup"><span data-stu-id="3a658-289">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="3a658-290">Можно указать `DimensionDataSource` в поле `filters` и указать настраиваемые аналитики в обоих полях `filters` и `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="3a658-290">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="3a658-291">Система будет автоматически преобразовывать пользовательские измерения в базовые измерения.</span><span class="sxs-lookup"><span data-stu-id="3a658-291">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="3a658-292">Пример 2 запроса текущих запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="3a658-292">Current on-hand query example 2</span></span>

<span data-ttu-id="3a658-293">В этом примере показан сценарий, в котором не настроены сопоставления для конфигурации аналитик в Power Apps, поэтому при разноске должны использоваться также базовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="3a658-293">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="3a658-294">Все аналитики должны быть базовыми аналитиками, если поле `dimensionDataSource` в разделе `filters` имеет значение NULL, является пустым или пробелом.</span><span class="sxs-lookup"><span data-stu-id="3a658-294">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="3a658-295">Пример возвращаемого результата</span><span class="sxs-lookup"><span data-stu-id="3a658-295">Example return result</span></span>

<span data-ttu-id="3a658-296">Запросы, показанные в предыдущих примерах, могут вернуть результат, подобный этому.</span><span class="sxs-lookup"><span data-stu-id="3a658-296">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="3a658-297">Обратите внимание, что поля количества структурированы как словарь мер и связанные с ними значений.</span><span class="sxs-lookup"><span data-stu-id="3a658-297">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
