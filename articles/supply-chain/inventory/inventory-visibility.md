---
title: Надстройка видимости запасов
description: В этом разделе описывается, как установить и настроить настройку отображения запасов для Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e294ada8dd3e764987aa363adb2614416986575b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821137"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="ef80e-103">Надстройка видимости запасов</span><span class="sxs-lookup"><span data-stu-id="ef80e-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="ef80e-104">Надстройка для отображения запасов — это независимая и масштабируемая микрослужба, позволяющая осуществлять отслеживание запасов в наличии в реальном времени, обеспечивая таким образом глобальное представление отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="ef80e-105">Вся информация, относящаяся к запасам в наличии, экспортируется в службу практически в реальном времени с помощью SQL-интеграции низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="ef80e-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="ef80e-106">Внешние системы обращаются к службе через API RESTful для запроса информации о наличии по заданным наборам аналитик, тем самым получая список доступных позиций в наличии.</span><span class="sxs-lookup"><span data-stu-id="ef80e-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="ef80e-107">Видимость запасов — это микрослужба, основанная на Microsoft Dataverse, что означает, что ее можно расширить путем создания приложений Power Apps и применения Power BI для предоставления настраиваемых функций в соответствии с потребностями бизнеса.</span><span class="sxs-lookup"><span data-stu-id="ef80e-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="ef80e-108">Возможно также обновление индекса для выполнения складских запросов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="ef80e-109">Видимость запасов предоставляет параметры конфигурации, которые позволяют ей интегрироваться с несколькими системами сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="ef80e-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="ef80e-110">Она поддерживает стандартизированную складскую аналитику, настраиваемую расширяемость и стандартизованные настраиваемые подсчитанные количества.</span><span class="sxs-lookup"><span data-stu-id="ef80e-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="ef80e-111">В этом разделе описывается, как установить и настроить настройку отображения запасов для Dynamics 365 Supply Chain Management и как использовать ее интерфейс программирования приложений (API).</span><span class="sxs-lookup"><span data-stu-id="ef80e-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="ef80e-112">Установка надстройки видимости запасов</span><span class="sxs-lookup"><span data-stu-id="ef80e-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="ef80e-113">Необходимо установить надстройку отображения запасов, используя Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ef80e-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ef80e-114">LCS — это портал совместной работы, который предоставляет среду и набор регулярно обновленных служб, которые помогут управлять жизненным циклом приложений Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ef80e-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="ef80e-115">Дополнительные сведения см. в разделе [Ресурсы Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="ef80e-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ef80e-116">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="ef80e-116">Prerequisites</span></span>

<span data-ttu-id="ef80e-117">Перед установкой надстройки видимости запасов необходимо сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="ef80e-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="ef80e-118">Получите проект внедрения LCS с по крайней мере одной развернутой средой.</span><span class="sxs-lookup"><span data-stu-id="ef80e-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="ef80e-119">Убедитесь, что необходимые условия для настройки надстроек в [Обзор надстроек](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md), обеспечены.</span><span class="sxs-lookup"><span data-stu-id="ef80e-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="ef80e-120">Для контроля запасов не требуется связывание с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="ef80e-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="ef80e-121">Для получения следующих трех необходимых файлов обратитесь к специалистам по контролю запасов по адресу [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ef80e-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="ef80e-122">`Inventory Visibility Integration.zip` (если версия Supply Chain Management, которую вы используете, более ранняя, чем версия 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="ef80e-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="ef80e-123">Поддерживаемые в настоящее время страны и регионы включают Канаду, США и Европейский союз (ЕС).</span><span class="sxs-lookup"><span data-stu-id="ef80e-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="ef80e-124">При возникновении каких-либо вопросов о необходимых условиях свяжитесь с группой разработчиков продукта для отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="ef80e-125">Настройка Dataverse</span><span class="sxs-lookup"><span data-stu-id="ef80e-125">Set up Dataverse</span></span>

<span data-ttu-id="ef80e-126">Чтобы настроить Dataverse, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="ef80e-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="ef80e-127">Добавление участника-службы в клиент:</span><span class="sxs-lookup"><span data-stu-id="ef80e-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="ef80e-128">Установите модуль Azure AD PowerShell v2, как описано в подразделе [Установка Azure Active Directory PowerShell для Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="ef80e-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="ef80e-129">Выполните следующую команду PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ef80e-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="ef80e-130">Создайте пользователя приложения для контроля запасов в Dataverse:</span><span class="sxs-lookup"><span data-stu-id="ef80e-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="ef80e-131">Откройте URL-адрес своей среды Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ef80e-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="ef80e-132">Перейдите **Дополнительные параметры \> Система \> Безопасность \> Пользователи** и создайте пользователя приложения.</span><span class="sxs-lookup"><span data-stu-id="ef80e-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="ef80e-133">Используйте меню вида для изменения вида страницы на **Пользователи приложения**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="ef80e-134">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-134">Select **New**.</span></span> <span data-ttu-id="ef80e-135">Задайте код приложения как *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="ef80e-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="ef80e-136">(Код объекта будет автоматически загружен после сохранения изменений.) Можно настроить имя.</span><span class="sxs-lookup"><span data-stu-id="ef80e-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="ef80e-137">Например, можно изменить его на *Контроль запасов*.</span><span class="sxs-lookup"><span data-stu-id="ef80e-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="ef80e-138">Закончив, выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="ef80e-139">Выберите **Назначить роль**, а затем выберите **Системный администратор**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="ef80e-140">Если имеется роль с именем **Пользователь Common Data Service**, выберите ее.</span><span class="sxs-lookup"><span data-stu-id="ef80e-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="ef80e-141">Дополнительные сведения см. в разделе [Создание пользователя приложения](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="ef80e-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="ef80e-142">Импортируйте файл `Inventory Visibility Dataverse Solution.zip`, который включает в себя соответствующие записи конфигурации Dataverse и Power Apps:</span><span class="sxs-lookup"><span data-stu-id="ef80e-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="ef80e-143">Перейдите на страницу **Решения**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="ef80e-144">Выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-144">Select **Import**.</span></span>

1. <span data-ttu-id="ef80e-145">Импортируйте поток триггеров обновления конфигурации:</span><span class="sxs-lookup"><span data-stu-id="ef80e-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="ef80e-146">Перейдите на страницу Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="ef80e-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="ef80e-147">Убедитесь, что подключение с именем *Dataverse (устар.)* существует.</span><span class="sxs-lookup"><span data-stu-id="ef80e-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="ef80e-148">(Если оно не существует, создайте его.)</span><span class="sxs-lookup"><span data-stu-id="ef80e-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="ef80e-149">Импортируйте файл формата `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="ef80e-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="ef80e-150">После импорта триггер появится в разделе **Мои потоки**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="ef80e-151">Инициализируйте четыре следующие переменные на основе информации о среде:</span><span class="sxs-lookup"><span data-stu-id="ef80e-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="ef80e-152">Идентификатор клиента Azure</span><span class="sxs-lookup"><span data-stu-id="ef80e-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="ef80e-153">Идентификатор клиента приложения Azure</span><span class="sxs-lookup"><span data-stu-id="ef80e-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="ef80e-154">Секрет клиента приложения Azure</span><span class="sxs-lookup"><span data-stu-id="ef80e-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="ef80e-155">Конечная точка контроля запасов</span><span class="sxs-lookup"><span data-stu-id="ef80e-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="ef80e-156">Дополнительные сведения об этой переменной см. в разделе [Настройка интеграции контроля запасов](#setup-inventory-visibility-integration) далее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="ef80e-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="ef80e-157">![Триггер конфигурации](media/configuration-trigger.png "Триггер конфигурации")</span><span class="sxs-lookup"><span data-stu-id="ef80e-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="ef80e-158">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="ef80e-159">Установка надстройки</span><span class="sxs-lookup"><span data-stu-id="ef80e-159">Install the add-in</span></span>

<span data-ttu-id="ef80e-160">Чтобы установить надстройку видимости запасов, необходимо сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="ef80e-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="ef80e-161">Выполните вход на портал [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="ef80e-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="ef80e-162">На домашней странице выберите проект, в котором развернута среда.</span><span class="sxs-lookup"><span data-stu-id="ef80e-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="ef80e-163">На странице проекта выберите среду, в которой требуется установить надстройку.</span><span class="sxs-lookup"><span data-stu-id="ef80e-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="ef80e-164">На странице среды прокрутите вниз до появления раздела **Надстройки среды** в разделе **Интеграция Power Platform**, где можно найти имя среды Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ef80e-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="ef80e-165">В разделе **Надстройки сред** выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="ef80e-166">![Страница среды в LCS](media/inventory-visibility-environment.png "Страница среды в LCS")</span><span class="sxs-lookup"><span data-stu-id="ef80e-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="ef80e-167">Выберите ссылку **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="ef80e-168">Откроется список доступных надстроек.</span><span class="sxs-lookup"><span data-stu-id="ef80e-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="ef80e-169">Выберите **Контроль запасов** в списке.</span><span class="sxs-lookup"><span data-stu-id="ef80e-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="ef80e-170">Введите значения для следующих полей для вашей среды:</span><span class="sxs-lookup"><span data-stu-id="ef80e-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="ef80e-171">**Код приложения AAD (клиента)**</span><span class="sxs-lookup"><span data-stu-id="ef80e-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="ef80e-172">**Код арендатора AAD**</span><span class="sxs-lookup"><span data-stu-id="ef80e-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="ef80e-173">![Страница настройки надстройки](media/inventory-visibility-setup.png "Страница настройки надстройки")</span><span class="sxs-lookup"><span data-stu-id="ef80e-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="ef80e-174">Примите условия, установив флажок **Условия**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="ef80e-175">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-175">Select **Install**.</span></span> <span data-ttu-id="ef80e-176">Статус надстройки будет отображаться как **Установка**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="ef80e-177">После завершения обновите страницу, чтобы увидеть статус, измененный на **Установлено**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="ef80e-178">Удаление надстройки</span><span class="sxs-lookup"><span data-stu-id="ef80e-178">Uninstall the add-in</span></span>

<span data-ttu-id="ef80e-179">Чтобы удалить надстройку, выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="ef80e-180">При обновлении LCS надстройка для контроля запасов будет удалена.</span><span class="sxs-lookup"><span data-stu-id="ef80e-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="ef80e-181">Процесс удаления приведет к удалению регистрации надстройки, а также запуску задания для очистки всех бизнес-данных, хранящихся в службе.</span><span class="sxs-lookup"><span data-stu-id="ef80e-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="ef80e-182">Потребление данных запасов в наличии из Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ef80e-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="ef80e-183">Развертывание пакета интеграции контроля запасов</span><span class="sxs-lookup"><span data-stu-id="ef80e-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="ef80e-184">Если используется Supply Chain Management версии 10.0.17 или более ранней, обратитесь в службу поддержки контроля запасов по адресу [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) для получения пакетного файла.</span><span class="sxs-lookup"><span data-stu-id="ef80e-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="ef80e-185">Затем разверните пакет в LCS.</span><span class="sxs-lookup"><span data-stu-id="ef80e-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="ef80e-186">Если во время развертывания возникает ошибка несоответствия версий, необходимо вручную импортировать проект X++ в среду разработки.</span><span class="sxs-lookup"><span data-stu-id="ef80e-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="ef80e-187">Затем создайте развертываемый пакет в среде разработки и разверните его в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="ef80e-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="ef80e-188">Этот код включен в Supply Chain Management 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="ef80e-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="ef80e-189">Если вы используете эту версию или более позднюю, развертывание не требуется.</span><span class="sxs-lookup"><span data-stu-id="ef80e-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="ef80e-190">Убедитесь, что в среде Supply Chain Management включены следующие функции.</span><span class="sxs-lookup"><span data-stu-id="ef80e-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="ef80e-191">(По умолчанию они включены.)</span><span class="sxs-lookup"><span data-stu-id="ef80e-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="ef80e-192">Описание функции</span><span class="sxs-lookup"><span data-stu-id="ef80e-192">Feature description</span></span> | <span data-ttu-id="ef80e-193">Версия кода</span><span class="sxs-lookup"><span data-stu-id="ef80e-193">Code version</span></span> | <span data-ttu-id="ef80e-194">Переключить класс</span><span class="sxs-lookup"><span data-stu-id="ef80e-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="ef80e-195">Включение и отключение использования складских аналитик в таблице InventSum</span><span class="sxs-lookup"><span data-stu-id="ef80e-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="ef80e-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="ef80e-196">10.0.11</span></span> | <span data-ttu-id="ef80e-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="ef80e-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="ef80e-198">Включение и отключение использования складских аналитик в таблице InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="ef80e-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="ef80e-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="ef80e-199">10.0.12</span></span> | <span data-ttu-id="ef80e-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="ef80e-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="ef80e-201">Настройка интеграции Видимости запасов</span><span class="sxs-lookup"><span data-stu-id="ef80e-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="ef80e-202">В Supply Chain Management откройте рабочую область **[Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** и включите функцию **Интеграция контроля запасов**.</span><span class="sxs-lookup"><span data-stu-id="ef80e-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="ef80e-203">Перейдите **Управление запасами \> Настройка \> Параметры интеграции контроля запасов** и введите URL-адрес среды, в которой выполняется контроль запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="ef80e-204">Найдите свой регион Azure среды, а затем введите URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="ef80e-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="ef80e-205">URL-адрес имеет следующую форму:</span><span class="sxs-lookup"><span data-stu-id="ef80e-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="ef80e-206">Например, если вы находитесь в Европе, у вашей среды будет один из следующих URL-адресов:</span><span class="sxs-lookup"><span data-stu-id="ef80e-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="ef80e-207">В настоящее время доступны следующие регионы.</span><span class="sxs-lookup"><span data-stu-id="ef80e-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="ef80e-208">Регион Azure</span><span class="sxs-lookup"><span data-stu-id="ef80e-208">Azure region</span></span> | <span data-ttu-id="ef80e-209">Краткое название региона</span><span class="sxs-lookup"><span data-stu-id="ef80e-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="ef80e-210">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="ef80e-210">Australia east</span></span> | <span data-ttu-id="ef80e-211">eau</span><span class="sxs-lookup"><span data-stu-id="ef80e-211">eau</span></span> |
    | <span data-ttu-id="ef80e-212">Юго-восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="ef80e-212">Australia southeast</span></span> | <span data-ttu-id="ef80e-213">seau</span><span class="sxs-lookup"><span data-stu-id="ef80e-213">seau</span></span> |
    | <span data-ttu-id="ef80e-214">Центральная Канада</span><span class="sxs-lookup"><span data-stu-id="ef80e-214">Canada central</span></span> | <span data-ttu-id="ef80e-215">cca</span><span class="sxs-lookup"><span data-stu-id="ef80e-215">cca</span></span> |
    | <span data-ttu-id="ef80e-216">Восточная Канада</span><span class="sxs-lookup"><span data-stu-id="ef80e-216">Canada east</span></span> | <span data-ttu-id="ef80e-217">eca</span><span class="sxs-lookup"><span data-stu-id="ef80e-217">eca</span></span> |
    | <span data-ttu-id="ef80e-218">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="ef80e-218">North Europe</span></span> | <span data-ttu-id="ef80e-219">neu</span><span class="sxs-lookup"><span data-stu-id="ef80e-219">neu</span></span> |
    | <span data-ttu-id="ef80e-220">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="ef80e-220">West Europe</span></span> | <span data-ttu-id="ef80e-221">weu</span><span class="sxs-lookup"><span data-stu-id="ef80e-221">weu</span></span> |
    | <span data-ttu-id="ef80e-222">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="ef80e-222">East US</span></span> | <span data-ttu-id="ef80e-223">eus</span><span class="sxs-lookup"><span data-stu-id="ef80e-223">eus</span></span> |
    | <span data-ttu-id="ef80e-224">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="ef80e-224">West US</span></span> | <span data-ttu-id="ef80e-225">wus</span><span class="sxs-lookup"><span data-stu-id="ef80e-225">wus</span></span> |

1. <span data-ttu-id="ef80e-226">Перейдите **Управление запасами \> Периодические операции \> Интеграция контроля запасов** и включите задание.</span><span class="sxs-lookup"><span data-stu-id="ef80e-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="ef80e-227">Все события изменения запасов из модуля Supply Chain Management будут разнесены в контроль запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="ef80e-228">Открытый API-интерфейс надстройки контроля запасов</span><span class="sxs-lookup"><span data-stu-id="ef80e-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="ef80e-229">Открытый интерфейс REST API надстройки контроля запасов представляет несколько определенных конечных точек интеграции.</span><span class="sxs-lookup"><span data-stu-id="ef80e-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="ef80e-230">Он поддерживает три основных типа взаимодействий:</span><span class="sxs-lookup"><span data-stu-id="ef80e-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="ef80e-231">Разноска изменений запасов в наличии в надстройку из внешней системы</span><span class="sxs-lookup"><span data-stu-id="ef80e-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="ef80e-232">Запрос текущих количеств в наличии из внешней системы</span><span class="sxs-lookup"><span data-stu-id="ef80e-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="ef80e-233">Автоматическая синхронизация с запасами в наличии в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ef80e-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="ef80e-234">Автоматическая синхронизация не является частью общедоступного API.</span><span class="sxs-lookup"><span data-stu-id="ef80e-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="ef80e-235">Вместо этого она обрабатывается в фоновом режиме для сред, в которых включена надстройка контроля запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="ef80e-236">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="ef80e-236">Authentication</span></span>

<span data-ttu-id="ef80e-237">Маркер безопасности платформы используется для вызова надстройки контроля запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="ef80e-238">Таким образом, необходимо создать *Маркер Azure Active Directory (Azure AD)* с помощью приложения Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ef80e-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="ef80e-239">Затем необходимо использовать маркер Azure AD, чтобы получить *маркер доступа* из службы безопасности.</span><span class="sxs-lookup"><span data-stu-id="ef80e-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="ef80e-240">Получите маркер службы безопасности, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ef80e-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="ef80e-241">Выполните вход на портал Azure и используйте его, чтобы найти `clientId` и `clientSecret` для вашего приложения Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ef80e-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="ef80e-242">Получите токен Azure Active Directory (`aadToken`), отправив HTTP-запрос со следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="ef80e-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="ef80e-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="ef80e-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="ef80e-244">**Метод** - `GET`</span><span class="sxs-lookup"><span data-stu-id="ef80e-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="ef80e-245">**Содержимое основной части (данные формы)**:</span><span class="sxs-lookup"><span data-stu-id="ef80e-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="ef80e-246">ключ</span><span class="sxs-lookup"><span data-stu-id="ef80e-246">key</span></span> | <span data-ttu-id="ef80e-247">значение</span><span class="sxs-lookup"><span data-stu-id="ef80e-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="ef80e-248">client_id</span><span class="sxs-lookup"><span data-stu-id="ef80e-248">client_id</span></span> | <span data-ttu-id="ef80e-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="ef80e-249">${aadAppId}</span></span> |
        | <span data-ttu-id="ef80e-250">client_secret</span><span class="sxs-lookup"><span data-stu-id="ef80e-250">client_secret</span></span> | <span data-ttu-id="ef80e-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="ef80e-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="ef80e-252">grant_type</span><span class="sxs-lookup"><span data-stu-id="ef80e-252">grant_type</span></span> | <span data-ttu-id="ef80e-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="ef80e-253">client_credentials</span></span> |
        | <span data-ttu-id="ef80e-254">ресурс</span><span class="sxs-lookup"><span data-stu-id="ef80e-254">resource</span></span> | <span data-ttu-id="ef80e-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="ef80e-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="ef80e-256">Вы должны получить токен `aadToken` в ответе, который напоминает следующий пример:</span><span class="sxs-lookup"><span data-stu-id="ef80e-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="ef80e-257">Сформулируйте запрос JSON, похожий на следующий:</span><span class="sxs-lookup"><span data-stu-id="ef80e-257">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="ef80e-258">Где:</span><span class="sxs-lookup"><span data-stu-id="ef80e-258">Where:</span></span>
    - <span data-ttu-id="ef80e-259">Значение `client_assertion` должно быть токеном `aadToken`, полученным на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="ef80e-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="ef80e-260">Значение `context` должно быть идентификатором среды, в которой требуется развернуть надстройку.</span><span class="sxs-lookup"><span data-stu-id="ef80e-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="ef80e-261">Установите все остальные значения, как показано в примере.</span><span class="sxs-lookup"><span data-stu-id="ef80e-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="ef80e-262">Отправьте запрос HTTP со следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="ef80e-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="ef80e-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="ef80e-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="ef80e-264">**Метод** - `POST`</span><span class="sxs-lookup"><span data-stu-id="ef80e-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="ef80e-265">**Заголовок HTTP** — включает версию API (ключ равен `Api-Version`, значение равно `1.0`)</span><span class="sxs-lookup"><span data-stu-id="ef80e-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="ef80e-266">**Основное содержимое** — включает запрос JSON, созданный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="ef80e-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="ef80e-267">В ответе вы получите `access_token`.</span><span class="sxs-lookup"><span data-stu-id="ef80e-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="ef80e-268">Это то, что требуется в качестве маркера носителя для вызова API отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="ef80e-269">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="ef80e-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="ef80e-270">Настройка интерфейса API для отображения запасов</span><span class="sxs-lookup"><span data-stu-id="ef80e-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="ef80e-271">Перед использованием службы необходимо выполнить конфигурации, описанные в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="ef80e-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="ef80e-272">Конфигурация может различаться в зависимости от сведений о среде.</span><span class="sxs-lookup"><span data-stu-id="ef80e-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="ef80e-273">В основном она включает четыре части:</span><span class="sxs-lookup"><span data-stu-id="ef80e-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="ef80e-274">Секционирование</span><span class="sxs-lookup"><span data-stu-id="ef80e-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="ef80e-275">Конфигурации аналитик</span><span class="sxs-lookup"><span data-stu-id="ef80e-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="ef80e-276">Индексация</span><span class="sxs-lookup"><span data-stu-id="ef80e-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="ef80e-277">Пользовательское измерение</span><span class="sxs-lookup"><span data-stu-id="ef80e-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="ef80e-278">Секционирование</span><span class="sxs-lookup"><span data-stu-id="ef80e-278">Partitioning</span></span>

<span data-ttu-id="ef80e-279">Секционирование может значительно повлиять на производительность API отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="ef80e-280">Рекомендуется определить схему, позволяющую выполнять небольшие группирования данных, сохраняя при этом возможность осмысленных запросов данных.</span><span class="sxs-lookup"><span data-stu-id="ef80e-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="ef80e-281">`organizationId` (`dataAreaId` в Supply Chain Management) всегда будет частью секционирования, и по умолчанию для отображения запасов устанавливается секционирование по аналитикам, таким как *Сайт + Местоположение*.</span><span class="sxs-lookup"><span data-stu-id="ef80e-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="ef80e-282">Это означает, что служба должна всегда запрашиваться с этими аналитиками, определенными в фильтрах.</span><span class="sxs-lookup"><span data-stu-id="ef80e-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="ef80e-283">*Сайт* и *Местоположение* — это две общих аналитики по умолчанию в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="ef80e-284">В Supply Chain Management эти аналитики называются *Сайт* (`InventSiteId`) и *Склад* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="ef80e-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="ef80e-285">Конфигурации аналитик</span><span class="sxs-lookup"><span data-stu-id="ef80e-285">Dimension configurations</span></span>

<span data-ttu-id="ef80e-286">Видимость запасов представляет список основных аналитик по умолчанию для включения интеграции нескольких источников в систему.</span><span class="sxs-lookup"><span data-stu-id="ef80e-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="ef80e-287">В следующей таблице перечислены складские аналитики, которые будут именами аналитик по умолчанию в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="ef80e-288">Тип аналитики</span><span class="sxs-lookup"><span data-stu-id="ef80e-288">Dimension type</span></span> | <span data-ttu-id="ef80e-289">Имя аналитики</span><span class="sxs-lookup"><span data-stu-id="ef80e-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="ef80e-290">Продукт</span><span class="sxs-lookup"><span data-stu-id="ef80e-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="ef80e-291">Продукт</span><span class="sxs-lookup"><span data-stu-id="ef80e-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="ef80e-292">Продукт</span><span class="sxs-lookup"><span data-stu-id="ef80e-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="ef80e-293">Продукт</span><span class="sxs-lookup"><span data-stu-id="ef80e-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="ef80e-294">Отслеживание</span><span class="sxs-lookup"><span data-stu-id="ef80e-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="ef80e-295">Отслеживание</span><span class="sxs-lookup"><span data-stu-id="ef80e-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="ef80e-296">Расположение</span><span class="sxs-lookup"><span data-stu-id="ef80e-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="ef80e-297">Расположение</span><span class="sxs-lookup"><span data-stu-id="ef80e-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="ef80e-298">Статус запасов</span><span class="sxs-lookup"><span data-stu-id="ef80e-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="ef80e-299">Зависит от склада</span><span class="sxs-lookup"><span data-stu-id="ef80e-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="ef80e-300">Зависит от склада</span><span class="sxs-lookup"><span data-stu-id="ef80e-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="ef80e-301">Зависит от склада</span><span class="sxs-lookup"><span data-stu-id="ef80e-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="ef80e-302">Тип аналитики, приведенный в предыдущей таблице, используется только для справки.</span><span class="sxs-lookup"><span data-stu-id="ef80e-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="ef80e-303">Нет необходимости определять тип аналитики в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="ef80e-304">Если имеется настраиваемая аналитика, которая должна перетекать в значение по умолчанию при потреблении видимостью запасов, можно настроить имя **настраиваемой аналитики** в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="ef80e-305">Внешние системы получают доступ к видимости запасов через интерфейсы API RESTful, которые позволяют запрашивать информацию о наличии по данным наборам аналитик.</span><span class="sxs-lookup"><span data-stu-id="ef80e-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="ef80e-306">Для интеграции видимость запасов позволяет настроить *источник данных внешнего канала* и исходную аналитику на *целевые аналитики* в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="ef80e-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="ef80e-307">Целевые аналитики должны быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="ef80e-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="ef80e-308">Аналитики по умолчанию в видимости запасов</span><span class="sxs-lookup"><span data-stu-id="ef80e-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="ef80e-309">Настраиваемые аналитики</span><span class="sxs-lookup"><span data-stu-id="ef80e-309">Custom dimensions</span></span>

<span data-ttu-id="ef80e-310">Целью настройки аналитики является стандартизация интеграции нескольких систем для запроса по аналитикам и события разноски с аналитиками.</span><span class="sxs-lookup"><span data-stu-id="ef80e-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="ef80e-311">Индексация</span><span class="sxs-lookup"><span data-stu-id="ef80e-311">Indexing</span></span>

<span data-ttu-id="ef80e-312">В большинстве случаев запрос запасов в наличии будет не только на самом высоком уровне "итога", но может потребоваться просмотреть результаты агрегирования на основе складских аналитик.</span><span class="sxs-lookup"><span data-stu-id="ef80e-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="ef80e-313">Видимость запасов обеспечивает гибкость, позволяя настраивать индексы, которые основаны на аналитике или комбинации аналитик.</span><span class="sxs-lookup"><span data-stu-id="ef80e-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="ef80e-314">В настоящее время для индексов можно настроить не более пяти.</span><span class="sxs-lookup"><span data-stu-id="ef80e-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="ef80e-315">Необходимо тщательно продумать, какая аналитика или комбинация аналитик будет использоваться, перед реализацией, чтобы обеспечить, что она будут удовлетворять вашим деловым потребностям.</span><span class="sxs-lookup"><span data-stu-id="ef80e-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="ef80e-316">Например, если требуется запросить продукты следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ef80e-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="ef80e-317">Запрос агрегированного наличия продуктов по аналитикам *Цвет* и *Размер*.</span><span class="sxs-lookup"><span data-stu-id="ef80e-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="ef80e-318">В некоторых случаях требуется только выполнить запрос по продукту в целом.</span><span class="sxs-lookup"><span data-stu-id="ef80e-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="ef80e-319">Можно определить два индекса следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ef80e-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="ef80e-320">Пустая скобка будет агрегирована на основе идентификатора продукта в секции.</span><span class="sxs-lookup"><span data-stu-id="ef80e-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="ef80e-321">Индексация определяет способ группировки результатов в зависимости от настройки запроса `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="ef80e-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="ef80e-322">В этом случае, если никакие значения `groupBy` не определены, будут выведены итоги по `productid`.</span><span class="sxs-lookup"><span data-stu-id="ef80e-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="ef80e-323">В противном случае, если определить `groupBy` как `groupBy=ColorId&groupBy=SizeId`, будет возвращено несколько строк, в зависимости от различных комбинаций цвета и размера в системе.</span><span class="sxs-lookup"><span data-stu-id="ef80e-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="ef80e-324">Критерии запроса можно разместить в теле запроса.</span><span class="sxs-lookup"><span data-stu-id="ef80e-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="ef80e-325">Вот пример запроса для комбинации цвета и размера продукта.</span><span class="sxs-lookup"><span data-stu-id="ef80e-325">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="ef80e-326">Пользовательское измерение</span><span class="sxs-lookup"><span data-stu-id="ef80e-326">Custom measurement</span></span>

<span data-ttu-id="ef80e-327">Количества измерений по умолчанию связаны с Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ef80e-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="ef80e-328">Однако, возможно, потребуется количество, состоящее из комбинации измерений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef80e-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="ef80e-329">Чтобы сделать это, можно задать конфигурацию настраиваемых количеств, которая будет добавлена к выходным данным запросов запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="ef80e-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="ef80e-330">Функциональность просто позволяют определить набор мер, которые будут добавлены, и/или набор мер, которые будут вычтены, чтобы сформировать настраиваемое измерение.</span><span class="sxs-lookup"><span data-stu-id="ef80e-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="ef80e-331">Например, со следующим условием запроса вы настроите пользовательское количество измерения как `MyCustomAvailableforReservation` для потребления системой потребления.</span><span class="sxs-lookup"><span data-stu-id="ef80e-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="ef80e-332">Система потребления</span><span class="sxs-lookup"><span data-stu-id="ef80e-332">Consumption system</span></span> | <span data-ttu-id="ef80e-333">Рассчитанные меры</span><span class="sxs-lookup"><span data-stu-id="ef80e-333">Calculated measurers</span></span> | <span data-ttu-id="ef80e-334">Иcточник данных</span><span class="sxs-lookup"><span data-stu-id="ef80e-334">Data source</span></span> | <span data-ttu-id="ef80e-335">Модификатор</span><span class="sxs-lookup"><span data-stu-id="ef80e-335">Modifier</span></span> | <span data-ttu-id="ef80e-336">Тип расчета модификатора</span><span class="sxs-lookup"><span data-stu-id="ef80e-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="ef80e-337">Сложение</span><span class="sxs-lookup"><span data-stu-id="ef80e-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="ef80e-338">Сложение</span><span class="sxs-lookup"><span data-stu-id="ef80e-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="ef80e-339">Вычитание</span><span class="sxs-lookup"><span data-stu-id="ef80e-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="ef80e-340">Сложение</span><span class="sxs-lookup"><span data-stu-id="ef80e-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="ef80e-341">Вычитание</span><span class="sxs-lookup"><span data-stu-id="ef80e-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="ef80e-342">Сложение</span><span class="sxs-lookup"><span data-stu-id="ef80e-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="ef80e-343">Сложение</span><span class="sxs-lookup"><span data-stu-id="ef80e-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="ef80e-344">Вычитание</span><span class="sxs-lookup"><span data-stu-id="ef80e-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="ef80e-345">Вычитание</span><span class="sxs-lookup"><span data-stu-id="ef80e-345">Subtraction</span></span> |

<span data-ttu-id="ef80e-346">При этом запрос настраиваемого количества измерения возвратит следующий результат.</span><span class="sxs-lookup"><span data-stu-id="ef80e-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="ef80e-347">Выходные данные `MyCustomAvailableforReservation` основаны на параметрах расчета в настраиваемых измерениях следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ef80e-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="ef80e-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="ef80e-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="ef80e-349">Разноска изменений запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="ef80e-349">Posting on-hand changes</span></span>

<span data-ttu-id="ef80e-350">Точный URL-адрес, на который будет разнесено событие, будет зависеть от географического региона.</span><span class="sxs-lookup"><span data-stu-id="ef80e-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="ef80e-351">Он будет иметь вид:</span><span class="sxs-lookup"><span data-stu-id="ef80e-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="ef80e-352">После аутентификации этот URL-адрес может использоваться вместе с методом HTTP `POST` для отправки в службу событий изменения запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="ef80e-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="ef80e-353">Специальный заголовок используется для связи с службами Dynamics 365 с помощью запросов HTTP, в которых указывается идентификатор среды экземпляра Supply Chain Management, с которым связаны данные.</span><span class="sxs-lookup"><span data-stu-id="ef80e-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="ef80e-354">Пример:</span><span class="sxs-lookup"><span data-stu-id="ef80e-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="ef80e-355">Пример 1 разноски запроса изменений запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="ef80e-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="ef80e-356">В этом примере показан сценарий, в котором будет настроена конфигурация аналитики в Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ef80e-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="ef80e-357">Следующий запрос используется для настройки сопоставления измерений в Power Apps:</span><span class="sxs-lookup"><span data-stu-id="ef80e-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="ef80e-358">Теперь можно указать `dimensionDataSource` и использовать пользовательские измерения в запросах.</span><span class="sxs-lookup"><span data-stu-id="ef80e-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="ef80e-359">Система будет автоматически преобразовывать пользовательские измерения в базовые измерения.</span><span class="sxs-lookup"><span data-stu-id="ef80e-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="ef80e-360">Пример 2 разноски запроса изменений запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="ef80e-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="ef80e-361">В этом примере показан сценарий, в котором не настроены сопоставления для конфигурации аналитик в Power Apps, поэтому при разноске должны использоваться также базовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="ef80e-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="ef80e-362">Все аналитики должны быть базовыми аналитиками, если поле `dimensionDataSource` имеет значение NULL, является пустым или пробелом.</span><span class="sxs-lookup"><span data-stu-id="ef80e-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="ef80e-363">Свойства полей документов JSON</span><span class="sxs-lookup"><span data-stu-id="ef80e-363">JSON document field properties</span></span>

<span data-ttu-id="ef80e-364">Поля из примеров запросов JSON, приведенных выше, имеют свойства, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ef80e-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="ef80e-365">FieldID</span><span class="sxs-lookup"><span data-stu-id="ef80e-365">Field ID</span></span> | <span data-ttu-id="ef80e-366">описание</span><span class="sxs-lookup"><span data-stu-id="ef80e-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="ef80e-367">Уникальный код для конкретного события изменения.</span><span class="sxs-lookup"><span data-stu-id="ef80e-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="ef80e-368">Этот код используется, чтобы гарантировать, что при возникновении ошибки при обмене данными с службой во время разноски повторная отправка события не приведет к тому, что в системе дважды будет учитываться одно и то же событие.</span><span class="sxs-lookup"><span data-stu-id="ef80e-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="ef80e-369">Идентификатор организации, связанной с событием.</span><span class="sxs-lookup"><span data-stu-id="ef80e-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="ef80e-370">Это сопоставляется с организациями Supply Chain Management или идентификаторами областей данных.</span><span class="sxs-lookup"><span data-stu-id="ef80e-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="ef80e-371">Идентификатор рассматриваемого продукта.</span><span class="sxs-lookup"><span data-stu-id="ef80e-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="ef80e-372">Количество, для которого должны быть изменены запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="ef80e-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="ef80e-373">Если, например, 10 новых бубликов были добавлены на полку, это значение было бы равно 10.</span><span class="sxs-lookup"><span data-stu-id="ef80e-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="ef80e-374">Если 3 бублика были удалены с полки или проданы, это значение было бы равно -3.</span><span class="sxs-lookup"><span data-stu-id="ef80e-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="ef80e-375">Источник данных для аналитик, используемых в разноске события изменения и запроса.</span><span class="sxs-lookup"><span data-stu-id="ef80e-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="ef80e-376">Если указан источник данных, можно использовать настраиваемые аналитики из указанного источника данных.</span><span class="sxs-lookup"><span data-stu-id="ef80e-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="ef80e-377">С помощью конфигурации аналитик видимость запасов может сопоставлять пользовательские аналитики с общими аналитиками по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef80e-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="ef80e-378">Если параметр `dimensionDataSource` не указан, в запросах могут использоваться только общие аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef80e-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="ef80e-379">Динамический набор пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="ef80e-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="ef80e-380">Это будет сопоставляться с некоторыми аналитиками в Supply Chain Management, но можно также добавить настраиваемые аналитики(например, *Источник*), которые могут обозначать, когда событие поступает из Supply Chain Management или из внешней системы.</span><span class="sxs-lookup"><span data-stu-id="ef80e-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="ef80e-381">Запрос текущих запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="ef80e-381">Querying current on-hand</span></span>

<span data-ttu-id="ef80e-382">Конечная точка для запроса текущих запасов в наличии будет иметь похожий URL-адрес:</span><span class="sxs-lookup"><span data-stu-id="ef80e-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="ef80e-383">Запрос будет выполняться с использованием метода HTTP `POST`.</span><span class="sxs-lookup"><span data-stu-id="ef80e-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="ef80e-384">Пример 1 запроса текущих запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="ef80e-384">Current on-hand query example 1</span></span>

<span data-ttu-id="ef80e-385">В этом примере показан сценарий, в котором вы уже выполнили настройку конфигурации аналитики в Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ef80e-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="ef80e-386">Следующий запрос используется для настройки сопоставления измерений в Power Apps:</span><span class="sxs-lookup"><span data-stu-id="ef80e-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="ef80e-387">Теперь можно указать `dimensionDataSource` и использовать пользовательские измерения в запросах.</span><span class="sxs-lookup"><span data-stu-id="ef80e-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="ef80e-388">Система будет автоматически преобразовывать пользовательские измерения в базовые измерения.</span><span class="sxs-lookup"><span data-stu-id="ef80e-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="ef80e-389">Можно указать `DimensionDataSource` в поле `filters` и указать настраиваемые аналитики в обоих полях `filters` и `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="ef80e-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="ef80e-390">Система будет автоматически преобразовывать пользовательские измерения в базовые измерения.</span><span class="sxs-lookup"><span data-stu-id="ef80e-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="ef80e-391">Пример 2 запроса текущих запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="ef80e-391">Current on-hand query example 2</span></span>

<span data-ttu-id="ef80e-392">В этом примере показан сценарий, в котором не настроены сопоставления для конфигурации аналитик в Power Apps, поэтому при разноске должны использоваться также базовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="ef80e-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="ef80e-393">Все аналитики должны быть базовыми аналитиками, если поле `dimensionDataSource` в разделе `filters` имеет значение NULL, является пустым или пробелом.</span><span class="sxs-lookup"><span data-stu-id="ef80e-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="ef80e-394">Пример возвращаемого результата</span><span class="sxs-lookup"><span data-stu-id="ef80e-394">Example return result</span></span>

<span data-ttu-id="ef80e-395">Запросы, показанные в предыдущих примерах, могут вернуть результат, подобный этому.</span><span class="sxs-lookup"><span data-stu-id="ef80e-395">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="ef80e-396">Обратите внимание, что поля количества структурированы как словарь мер и связанные с ними значений.</span><span class="sxs-lookup"><span data-stu-id="ef80e-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
