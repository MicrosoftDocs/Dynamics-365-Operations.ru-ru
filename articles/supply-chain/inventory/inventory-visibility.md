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
ms.openlocfilehash: d09c7be5de75511b10d7a69d4b8ac12917b0dbe8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910433"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="71045-103">Надстройка видимости запасов</span><span class="sxs-lookup"><span data-stu-id="71045-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="71045-104">Надстройка для отображения запасов — это независимая и масштабируемая микрослужба, позволяющая осуществлять отслеживание запасов в наличии в реальном времени, обеспечивая таким образом глобальное представление отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="71045-105">Вся информация, относящаяся к запасам в наличии, экспортируется в службу практически в реальном времени с помощью SQL-интеграции низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="71045-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="71045-106">Внешние системы обращаются к службе через API RESTful для запроса информации о наличии по заданным наборам аналитик, тем самым получая список доступных позиций в наличии.</span><span class="sxs-lookup"><span data-stu-id="71045-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="71045-107">Видимость запасов — это микрослужба, основанная на Microsoft Dataverse, что означает, что ее можно расширить путем создания приложений Power Apps и применения Power BI для предоставления настраиваемых функций в соответствии с потребностями бизнеса.</span><span class="sxs-lookup"><span data-stu-id="71045-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="71045-108">Возможно также обновление индекса для выполнения складских запросов.</span><span class="sxs-lookup"><span data-stu-id="71045-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="71045-109">Видимость запасов предоставляет параметры конфигурации, которые позволяют ей интегрироваться с несколькими системами сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="71045-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="71045-110">Она поддерживает стандартизированную складскую аналитику, настраиваемую расширяемость и стандартизованные настраиваемые подсчитанные количества.</span><span class="sxs-lookup"><span data-stu-id="71045-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="71045-111">В этом разделе описывается, как установить и настроить настройку отображения запасов для Dynamics 365 Supply Chain Management и как использовать ее интерфейс программирования приложений (API).</span><span class="sxs-lookup"><span data-stu-id="71045-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="71045-112">Установка надстройки видимости запасов</span><span class="sxs-lookup"><span data-stu-id="71045-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="71045-113">Необходимо установить надстройку отображения запасов, используя Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="71045-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="71045-114">LCS — это портал совместной работы, который предоставляет среду и набор регулярно обновленных служб, которые помогут управлять жизненным циклом приложений Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="71045-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="71045-115">Дополнительные сведения см. в разделе [Ресурсы Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="71045-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="71045-116">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="71045-116">Prerequisites</span></span>

<span data-ttu-id="71045-117">Перед установкой надстройки видимости запасов необходимо сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="71045-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="71045-118">Получите проект внедрения LCS с по крайней мере одной развернутой средой.</span><span class="sxs-lookup"><span data-stu-id="71045-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="71045-119">Убедитесь, что необходимые условия для настройки надстроек в [Обзор надстроек](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md), обеспечены.</span><span class="sxs-lookup"><span data-stu-id="71045-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="71045-120">Для контроля запасов не требуется связывание с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="71045-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="71045-121">Для получения следующих трех необходимых файлов обратитесь к специалистам по контролю запасов по адресу [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="71045-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="71045-122">`Inventory Visibility Integration.zip` (если версия Supply Chain Management, которую вы используете, более ранняя, чем версия 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="71045-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="71045-123">Следуйте инструкциям, приведенным в [Быстрое начало: регистрация приложения на платформе Microsoft Identity](/azure/active-directory/develop/quickstart-register-app) для регистрации приложения и добавления секрета клиента в AAD в рамках подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="71045-123">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
    - [<span data-ttu-id="71045-124">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="71045-124">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
    - [<span data-ttu-id="71045-125">Добавить секрет клиента</span><span class="sxs-lookup"><span data-stu-id="71045-125">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
    - <span data-ttu-id="71045-126">**Код приложения (клиент)**, **Секрет клиента** и **Код клиента** будут использоваться в следующих шагах.</span><span class="sxs-lookup"><span data-stu-id="71045-126">The **Application(Client) Id**, **Client Secret** and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="71045-127">Поддерживаемые в настоящее время страны и регионы включают Канаду, США и Европейский союз (ЕС).</span><span class="sxs-lookup"><span data-stu-id="71045-127">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="71045-128">При возникновении каких-либо вопросов о необходимых условиях свяжитесь с группой разработчиков продукта для отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-128">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="71045-129">Настройка Dataverse</span><span class="sxs-lookup"><span data-stu-id="71045-129">Set up Dataverse</span></span>

<span data-ttu-id="71045-130">Чтобы настроить Dataverse, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="71045-130">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="71045-131">Добавление участника-службы в клиент:</span><span class="sxs-lookup"><span data-stu-id="71045-131">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="71045-132">Установите модуль Azure AD PowerShell v2, как описано в подразделе [Установка Azure Active Directory PowerShell для Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="71045-132">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="71045-133">Выполните следующую команду PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71045-133">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="71045-134">Создайте пользователя приложения для контроля запасов в Dataverse:</span><span class="sxs-lookup"><span data-stu-id="71045-134">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="71045-135">Откройте URL-адрес своей среды Dataverse.</span><span class="sxs-lookup"><span data-stu-id="71045-135">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="71045-136">Перейдите **Дополнительные параметры \> Система \> Безопасность \> Пользователи** и создайте пользователя приложения.</span><span class="sxs-lookup"><span data-stu-id="71045-136">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="71045-137">Используйте меню вида для изменения вида страницы на **Пользователи приложения**.</span><span class="sxs-lookup"><span data-stu-id="71045-137">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="71045-138">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="71045-138">Select **New**.</span></span> <span data-ttu-id="71045-139">Задайте код приложения как *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="71045-139">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="71045-140">(Код объекта будет автоматически загружен после сохранения изменений.) Можно настроить имя.</span><span class="sxs-lookup"><span data-stu-id="71045-140">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="71045-141">Например, можно изменить его на *Контроль запасов*.</span><span class="sxs-lookup"><span data-stu-id="71045-141">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="71045-142">Закончив, выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="71045-142">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="71045-143">Выберите **Назначить роль**, а затем выберите **Системный администратор**.</span><span class="sxs-lookup"><span data-stu-id="71045-143">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="71045-144">Если имеется роль с именем **Пользователь Common Data Service**, выберите ее.</span><span class="sxs-lookup"><span data-stu-id="71045-144">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="71045-145">Дополнительные сведения см. в разделе [Создание пользователя приложения](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="71045-145">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="71045-146">Если языком по умолчанию в Dataverse является не **Английский**, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="71045-146">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="71045-147">Переход к **Дополнительные параметры \> Администрирование \> Языки**,</span><span class="sxs-lookup"><span data-stu-id="71045-147">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="71045-148">Выберите **Английский (LanguageCode=1033)** и нажмите кнопку **применить**.</span><span class="sxs-lookup"><span data-stu-id="71045-148">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="71045-149">Импортируйте файл `Inventory Visibility Dataverse Solution.zip`, который включает в себя соответствующие записи конфигурации Dataverse и Power Apps:</span><span class="sxs-lookup"><span data-stu-id="71045-149">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="71045-150">Перейдите на страницу **Решения**.</span><span class="sxs-lookup"><span data-stu-id="71045-150">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="71045-151">Выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="71045-151">Select **Import**.</span></span>

1. <span data-ttu-id="71045-152">Импортируйте поток триггеров обновления конфигурации:</span><span class="sxs-lookup"><span data-stu-id="71045-152">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="71045-153">Перейдите на страницу Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="71045-153">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="71045-154">Убедитесь, что подключение с именем *Dataverse (устар.)* существует.</span><span class="sxs-lookup"><span data-stu-id="71045-154">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="71045-155">(Если оно не существует, создайте его.)</span><span class="sxs-lookup"><span data-stu-id="71045-155">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="71045-156">Импортируйте файл формата `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="71045-156">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="71045-157">После импорта триггер появится в разделе **Мои потоки**.</span><span class="sxs-lookup"><span data-stu-id="71045-157">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="71045-158">Инициализируйте четыре следующие переменные на основе информации о среде:</span><span class="sxs-lookup"><span data-stu-id="71045-158">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="71045-159">Идентификатор клиента Azure</span><span class="sxs-lookup"><span data-stu-id="71045-159">Azure Tenant ID</span></span>
        - <span data-ttu-id="71045-160">Идентификатор клиента приложения Azure</span><span class="sxs-lookup"><span data-stu-id="71045-160">Azure Application Client ID</span></span>
        - <span data-ttu-id="71045-161">Секрет клиента приложения Azure</span><span class="sxs-lookup"><span data-stu-id="71045-161">Azure Application Client Secret</span></span>
        - <span data-ttu-id="71045-162">Конечная точка контроля запасов</span><span class="sxs-lookup"><span data-stu-id="71045-162">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="71045-163">Дополнительные сведения об этой переменной см. в разделе [Настройка интеграции контроля запасов](#setup-inventory-visibility-integration) далее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="71045-163">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="71045-164">![Триггер конфигурации](media/configuration-trigger.png "Триггер конфигурации")</span><span class="sxs-lookup"><span data-stu-id="71045-164">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="71045-165">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="71045-165">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="71045-166">Установка надстройки</span><span class="sxs-lookup"><span data-stu-id="71045-166">Install the add-in</span></span>

<span data-ttu-id="71045-167">Чтобы установить надстройку видимости запасов, необходимо сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="71045-167">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="71045-168">Выполните вход на портал [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="71045-168">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="71045-169">На домашней странице выберите проект, в котором развернута среда.</span><span class="sxs-lookup"><span data-stu-id="71045-169">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="71045-170">На странице проекта выберите среду, в которой требуется установить надстройку.</span><span class="sxs-lookup"><span data-stu-id="71045-170">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="71045-171">На странице среды прокрутите вниз до появления раздела **Надстройки среды** в разделе **Интеграция Power Platform**, где можно найти имя среды Dataverse.</span><span class="sxs-lookup"><span data-stu-id="71045-171">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="71045-172">В разделе **Надстройки сред** выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="71045-172">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="71045-173">![Страница среды в LCS](media/inventory-visibility-environment.png "Страница среды в LCS")</span><span class="sxs-lookup"><span data-stu-id="71045-173">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="71045-174">Выберите ссылку **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="71045-174">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="71045-175">Откроется список доступных надстроек.</span><span class="sxs-lookup"><span data-stu-id="71045-175">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="71045-176">Выберите **Контроль запасов** в списке.</span><span class="sxs-lookup"><span data-stu-id="71045-176">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="71045-177">Введите значения для следующих полей для вашей среды:</span><span class="sxs-lookup"><span data-stu-id="71045-177">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="71045-178">**Код приложения AAD (клиента)**</span><span class="sxs-lookup"><span data-stu-id="71045-178">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="71045-179">**Код арендатора AAD**</span><span class="sxs-lookup"><span data-stu-id="71045-179">**AAD tenant ID**</span></span>

    <span data-ttu-id="71045-180">![Страница настройки надстройки](media/inventory-visibility-setup.png "Страница настройки надстройки")</span><span class="sxs-lookup"><span data-stu-id="71045-180">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="71045-181">Примите условия, установив флажок **Условия**.</span><span class="sxs-lookup"><span data-stu-id="71045-181">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="71045-182">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="71045-182">Select **Install**.</span></span> <span data-ttu-id="71045-183">Статус надстройки будет отображаться как **Установка**.</span><span class="sxs-lookup"><span data-stu-id="71045-183">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="71045-184">После завершения обновите страницу, чтобы увидеть статус, измененный на **Установлено**.</span><span class="sxs-lookup"><span data-stu-id="71045-184">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="71045-185">Удаление надстройки</span><span class="sxs-lookup"><span data-stu-id="71045-185">Uninstall the add-in</span></span>

<span data-ttu-id="71045-186">Чтобы удалить надстройку, выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="71045-186">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="71045-187">При обновлении LCS надстройка для контроля запасов будет удалена.</span><span class="sxs-lookup"><span data-stu-id="71045-187">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="71045-188">Процесс удаления приведет к удалению регистрации надстройки, а также запуску задания для очистки всех бизнес-данных, хранящихся в службе.</span><span class="sxs-lookup"><span data-stu-id="71045-188">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="71045-189">Потребление данных запасов в наличии из Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="71045-189">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="71045-190">Развертывание пакета интеграции контроля запасов</span><span class="sxs-lookup"><span data-stu-id="71045-190">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="71045-191">Если используется Supply Chain Management версии 10.0.17 или более ранней, обратитесь в службу поддержки контроля запасов по адресу [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) для получения пакетного файла.</span><span class="sxs-lookup"><span data-stu-id="71045-191">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="71045-192">Затем разверните пакет в LCS.</span><span class="sxs-lookup"><span data-stu-id="71045-192">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="71045-193">Если во время развертывания возникает ошибка несоответствия версий, необходимо вручную импортировать проект X++ в среду разработки.</span><span class="sxs-lookup"><span data-stu-id="71045-193">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="71045-194">Затем создайте развертываемый пакет в среде разработки и разверните его в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="71045-194">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="71045-195">Этот код включен в Supply Chain Management 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="71045-195">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="71045-196">Если вы используете эту версию или более позднюю, развертывание не требуется.</span><span class="sxs-lookup"><span data-stu-id="71045-196">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="71045-197">Убедитесь, что в среде Supply Chain Management включены следующие функции.</span><span class="sxs-lookup"><span data-stu-id="71045-197">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="71045-198">(По умолчанию они включены.)</span><span class="sxs-lookup"><span data-stu-id="71045-198">(By default, they are turned on.)</span></span>

| <span data-ttu-id="71045-199">Описание функции</span><span class="sxs-lookup"><span data-stu-id="71045-199">Feature description</span></span> | <span data-ttu-id="71045-200">Версия кода</span><span class="sxs-lookup"><span data-stu-id="71045-200">Code version</span></span> | <span data-ttu-id="71045-201">Переключить класс</span><span class="sxs-lookup"><span data-stu-id="71045-201">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="71045-202">Включение и отключение использования складских аналитик в таблице InventSum</span><span class="sxs-lookup"><span data-stu-id="71045-202">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="71045-203">10.0.11</span><span class="sxs-lookup"><span data-stu-id="71045-203">10.0.11</span></span> | <span data-ttu-id="71045-204">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="71045-204">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="71045-205">Включение и отключение использования складских аналитик в таблице InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="71045-205">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="71045-206">10.0.12</span><span class="sxs-lookup"><span data-stu-id="71045-206">10.0.12</span></span> | <span data-ttu-id="71045-207">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="71045-207">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="71045-208">Настройка интеграции Видимости запасов</span><span class="sxs-lookup"><span data-stu-id="71045-208">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="71045-209">В Supply Chain Management откройте рабочую область **[Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** и включите функцию **Интеграция контроля запасов**.</span><span class="sxs-lookup"><span data-stu-id="71045-209">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="71045-210">Перейдите **Управление запасами \> Настройка \> Параметры интеграции контроля запасов** и введите URL-адрес среды, в которой выполняется контроль запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-210">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="71045-211">Найдите свой регион Azure среды, а затем введите URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="71045-211">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="71045-212">URL-адрес имеет следующую форму:</span><span class="sxs-lookup"><span data-stu-id="71045-212">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="71045-213">Например, если вы находитесь в Европе, у вашей среды будет один из следующих URL-адресов:</span><span class="sxs-lookup"><span data-stu-id="71045-213">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="71045-214">В настоящее время доступны следующие регионы.</span><span class="sxs-lookup"><span data-stu-id="71045-214">The following regions are currently available.</span></span>

    | <span data-ttu-id="71045-215">Регион Azure</span><span class="sxs-lookup"><span data-stu-id="71045-215">Azure region</span></span> | <span data-ttu-id="71045-216">Краткое название региона</span><span class="sxs-lookup"><span data-stu-id="71045-216">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="71045-217">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="71045-217">Australia east</span></span> | <span data-ttu-id="71045-218">eau</span><span class="sxs-lookup"><span data-stu-id="71045-218">eau</span></span> |
    | <span data-ttu-id="71045-219">Юго-восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="71045-219">Australia southeast</span></span> | <span data-ttu-id="71045-220">seau</span><span class="sxs-lookup"><span data-stu-id="71045-220">seau</span></span> |
    | <span data-ttu-id="71045-221">Центральная Канада</span><span class="sxs-lookup"><span data-stu-id="71045-221">Canada central</span></span> | <span data-ttu-id="71045-222">cca</span><span class="sxs-lookup"><span data-stu-id="71045-222">cca</span></span> |
    | <span data-ttu-id="71045-223">Восточная Канада</span><span class="sxs-lookup"><span data-stu-id="71045-223">Canada east</span></span> | <span data-ttu-id="71045-224">eca</span><span class="sxs-lookup"><span data-stu-id="71045-224">eca</span></span> |
    | <span data-ttu-id="71045-225">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="71045-225">North Europe</span></span> | <span data-ttu-id="71045-226">neu</span><span class="sxs-lookup"><span data-stu-id="71045-226">neu</span></span> |
    | <span data-ttu-id="71045-227">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="71045-227">West Europe</span></span> | <span data-ttu-id="71045-228">weu</span><span class="sxs-lookup"><span data-stu-id="71045-228">weu</span></span> |
    | <span data-ttu-id="71045-229">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="71045-229">East US</span></span> | <span data-ttu-id="71045-230">eus</span><span class="sxs-lookup"><span data-stu-id="71045-230">eus</span></span> |
    | <span data-ttu-id="71045-231">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="71045-231">West US</span></span> | <span data-ttu-id="71045-232">wus</span><span class="sxs-lookup"><span data-stu-id="71045-232">wus</span></span> |

1. <span data-ttu-id="71045-233">Перейдите **Управление запасами \> Периодические операции \> Интеграция контроля запасов** и включите задание.</span><span class="sxs-lookup"><span data-stu-id="71045-233">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="71045-234">Все события изменения запасов из модуля Supply Chain Management будут разнесены в контроль запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-234">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="71045-235">Открытый API-интерфейс надстройки контроля запасов</span><span class="sxs-lookup"><span data-stu-id="71045-235">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="71045-236">Открытый интерфейс REST API надстройки контроля запасов представляет несколько определенных конечных точек интеграции.</span><span class="sxs-lookup"><span data-stu-id="71045-236">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="71045-237">Он поддерживает три основных типа взаимодействий:</span><span class="sxs-lookup"><span data-stu-id="71045-237">It supports three main interaction types:</span></span>

- <span data-ttu-id="71045-238">Разноска изменений запасов в наличии в надстройку из внешней системы</span><span class="sxs-lookup"><span data-stu-id="71045-238">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="71045-239">Запрос текущих количеств в наличии из внешней системы</span><span class="sxs-lookup"><span data-stu-id="71045-239">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="71045-240">Автоматическая синхронизация с запасами в наличии в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="71045-240">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="71045-241">Автоматическая синхронизация не является частью общедоступного API.</span><span class="sxs-lookup"><span data-stu-id="71045-241">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="71045-242">Вместо этого она обрабатывается в фоновом режиме для сред, в которых включена надстройка контроля запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-242">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="71045-243">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="71045-243">Authentication</span></span>

<span data-ttu-id="71045-244">Маркер безопасности платформы используется для вызова надстройки контроля запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-244">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="71045-245">Таким образом, необходимо создать *Маркер Azure Active Directory (Azure AD)* с помощью приложения Azure AD.</span><span class="sxs-lookup"><span data-stu-id="71045-245">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="71045-246">Затем необходимо использовать маркер Azure AD, чтобы получить *маркер доступа* из службы безопасности.</span><span class="sxs-lookup"><span data-stu-id="71045-246">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="71045-247">Получите маркер службы безопасности, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="71045-247">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="71045-248">Выполните вход на портал Azure и используйте его, чтобы найти `clientId` и `clientSecret` для вашего приложения Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="71045-248">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="71045-249">Получите токен Azure Active Directory (`aadToken`), отправив HTTP-запрос со следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="71045-249">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="71045-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="71045-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="71045-251">**Метод** - `GET`</span><span class="sxs-lookup"><span data-stu-id="71045-251">**Method** - `GET`</span></span>
    - <span data-ttu-id="71045-252">**Содержимое основной части (данные формы)**:</span><span class="sxs-lookup"><span data-stu-id="71045-252">**Body content (form data)**:</span></span>

        | <span data-ttu-id="71045-253">ключ</span><span class="sxs-lookup"><span data-stu-id="71045-253">key</span></span> | <span data-ttu-id="71045-254">значение</span><span class="sxs-lookup"><span data-stu-id="71045-254">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="71045-255">client_id</span><span class="sxs-lookup"><span data-stu-id="71045-255">client_id</span></span> | <span data-ttu-id="71045-256">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="71045-256">${aadAppId}</span></span> |
        | <span data-ttu-id="71045-257">client_secret</span><span class="sxs-lookup"><span data-stu-id="71045-257">client_secret</span></span> | <span data-ttu-id="71045-258">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="71045-258">${aadAppSecret}</span></span> |
        | <span data-ttu-id="71045-259">grant_type</span><span class="sxs-lookup"><span data-stu-id="71045-259">grant_type</span></span> | <span data-ttu-id="71045-260">client_credentials</span><span class="sxs-lookup"><span data-stu-id="71045-260">client_credentials</span></span> |
        | <span data-ttu-id="71045-261">ресурс</span><span class="sxs-lookup"><span data-stu-id="71045-261">resource</span></span> | <span data-ttu-id="71045-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="71045-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="71045-263">Вы должны получить токен `aadToken` в ответе, который напоминает следующий пример:</span><span class="sxs-lookup"><span data-stu-id="71045-263">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="71045-264">Сформулируйте запрос JSON, похожий на следующий:</span><span class="sxs-lookup"><span data-stu-id="71045-264">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="71045-265">Где:</span><span class="sxs-lookup"><span data-stu-id="71045-265">Where:</span></span>
    - <span data-ttu-id="71045-266">Значение `client_assertion` должно быть токеном `aadToken`, полученным на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="71045-266">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="71045-267">Значение `context` должно быть идентификатором среды, в которой требуется развернуть надстройку.</span><span class="sxs-lookup"><span data-stu-id="71045-267">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="71045-268">Установите все остальные значения, как показано в примере.</span><span class="sxs-lookup"><span data-stu-id="71045-268">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="71045-269">Отправьте запрос HTTP со следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="71045-269">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="71045-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="71045-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="71045-271">**Метод** - `POST`</span><span class="sxs-lookup"><span data-stu-id="71045-271">**Method** - `POST`</span></span>
    - <span data-ttu-id="71045-272">**Заголовок HTTP** — включает версию API (ключ равен `Api-Version`, значение равно `1.0`)</span><span class="sxs-lookup"><span data-stu-id="71045-272">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="71045-273">**Основное содержимое** — включает запрос JSON, созданный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="71045-273">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="71045-274">В ответе вы получите `access_token`.</span><span class="sxs-lookup"><span data-stu-id="71045-274">You will get an `access_token` in response.</span></span> <span data-ttu-id="71045-275">Это то, что требуется в качестве маркера носителя для вызова API отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-275">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="71045-276">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="71045-276">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="71045-277">Образец запроса</span><span class="sxs-lookup"><span data-stu-id="71045-277">Sample Request</span></span>

<span data-ttu-id="71045-278">Для справки, вот образец http-запроса, для отправки этого запроса можно использовать любые инструменты или язык кодирования, например ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="71045-278">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="71045-279">Настройка интерфейса API для отображения запасов</span><span class="sxs-lookup"><span data-stu-id="71045-279">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="71045-280">Перед использованием службы необходимо выполнить конфигурации, описанные в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="71045-280">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="71045-281">Конфигурация может различаться в зависимости от сведений о среде.</span><span class="sxs-lookup"><span data-stu-id="71045-281">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="71045-282">В основном она включает четыре части:</span><span class="sxs-lookup"><span data-stu-id="71045-282">It primarily includes four parts:</span></span>

- [<span data-ttu-id="71045-283">Секционирование</span><span class="sxs-lookup"><span data-stu-id="71045-283">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="71045-284">Конфигурации аналитик</span><span class="sxs-lookup"><span data-stu-id="71045-284">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="71045-285">Индексация</span><span class="sxs-lookup"><span data-stu-id="71045-285">Indexing</span></span>](#indexing)
- [<span data-ttu-id="71045-286">Пользовательское измерение</span><span class="sxs-lookup"><span data-stu-id="71045-286">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="71045-287">Секционирование</span><span class="sxs-lookup"><span data-stu-id="71045-287">Partitioning</span></span>

<span data-ttu-id="71045-288">Секционирование может значительно повлиять на производительность API отображения запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-288">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="71045-289">Рекомендуется определить схему, позволяющую выполнять небольшие группирования данных, сохраняя при этом возможность осмысленных запросов данных.</span><span class="sxs-lookup"><span data-stu-id="71045-289">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="71045-290">`organizationId` (`dataAreaId` в Supply Chain Management) всегда будет частью секционирования, и по умолчанию для отображения запасов устанавливается секционирование по аналитикам, таким как *Сайт + Местоположение*.</span><span class="sxs-lookup"><span data-stu-id="71045-290">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="71045-291">Это означает, что служба должна всегда запрашиваться с этими аналитиками, определенными в фильтрах.</span><span class="sxs-lookup"><span data-stu-id="71045-291">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="71045-292">*Сайт* и *Местоположение* — это две общих аналитики по умолчанию в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-292">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="71045-293">В Supply Chain Management эти аналитики называются *Сайт* (`InventSiteId`) и *Склад* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="71045-293">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="71045-294">Конфигурации аналитик</span><span class="sxs-lookup"><span data-stu-id="71045-294">Dimension configurations</span></span>

<span data-ttu-id="71045-295">Видимость запасов представляет список основных аналитик по умолчанию для включения интеграции нескольких источников в систему.</span><span class="sxs-lookup"><span data-stu-id="71045-295">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="71045-296">В следующей таблице перечислены складские аналитики, которые будут именами аналитик по умолчанию в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-296">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="71045-297">Тип аналитики</span><span class="sxs-lookup"><span data-stu-id="71045-297">Dimension type</span></span> | <span data-ttu-id="71045-298">Имя аналитики</span><span class="sxs-lookup"><span data-stu-id="71045-298">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="71045-299">Продукт</span><span class="sxs-lookup"><span data-stu-id="71045-299">Product</span></span> | `ColorId` |
| <span data-ttu-id="71045-300">Продукт</span><span class="sxs-lookup"><span data-stu-id="71045-300">Product</span></span> | `SizeId` |
| <span data-ttu-id="71045-301">Продукт</span><span class="sxs-lookup"><span data-stu-id="71045-301">Product</span></span> | `StyleId` |
| <span data-ttu-id="71045-302">Продукт</span><span class="sxs-lookup"><span data-stu-id="71045-302">Product</span></span> | `ConfigId` |
| <span data-ttu-id="71045-303">Отслеживание</span><span class="sxs-lookup"><span data-stu-id="71045-303">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="71045-304">Отслеживание</span><span class="sxs-lookup"><span data-stu-id="71045-304">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="71045-305">Расположение</span><span class="sxs-lookup"><span data-stu-id="71045-305">Location</span></span> | `LocationId` |
| <span data-ttu-id="71045-306">Расположение</span><span class="sxs-lookup"><span data-stu-id="71045-306">Location</span></span> | `SiteId` |
| <span data-ttu-id="71045-307">Статус запасов</span><span class="sxs-lookup"><span data-stu-id="71045-307">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="71045-308">Зависит от склада</span><span class="sxs-lookup"><span data-stu-id="71045-308">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="71045-309">Зависит от склада</span><span class="sxs-lookup"><span data-stu-id="71045-309">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="71045-310">Зависит от склада</span><span class="sxs-lookup"><span data-stu-id="71045-310">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="71045-311">Тип аналитики, приведенный в предыдущей таблице, используется только для справки.</span><span class="sxs-lookup"><span data-stu-id="71045-311">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="71045-312">Нет необходимости определять тип аналитики в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-312">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="71045-313">Если имеется настраиваемая аналитика, которая должна перетекать в значение по умолчанию при потреблении видимостью запасов, можно настроить имя **настраиваемой аналитики** в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-313">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="71045-314">Внешние системы получают доступ к видимости запасов через интерфейсы API RESTful, которые позволяют запрашивать информацию о наличии по данным наборам аналитик.</span><span class="sxs-lookup"><span data-stu-id="71045-314">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="71045-315">Для интеграции видимость запасов позволяет настроить *источник данных внешнего канала* и исходную аналитику на *целевые аналитики* в видимости запасов.</span><span class="sxs-lookup"><span data-stu-id="71045-315">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="71045-316">Целевые аналитики должны быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="71045-316">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="71045-317">Аналитики по умолчанию в видимости запасов</span><span class="sxs-lookup"><span data-stu-id="71045-317">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="71045-318">Настраиваемые аналитики</span><span class="sxs-lookup"><span data-stu-id="71045-318">Custom dimensions</span></span>

<span data-ttu-id="71045-319">Целью настройки аналитики является стандартизация интеграции нескольких систем для запроса по аналитикам и события разноски с аналитиками.</span><span class="sxs-lookup"><span data-stu-id="71045-319">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="71045-320">Индексация</span><span class="sxs-lookup"><span data-stu-id="71045-320">Indexing</span></span>

<span data-ttu-id="71045-321">В большинстве случаев запрос запасов в наличии будет не только на самом высоком уровне "итога", но может потребоваться просмотреть результаты агрегирования на основе складских аналитик.</span><span class="sxs-lookup"><span data-stu-id="71045-321">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="71045-322">Видимость запасов обеспечивает гибкость, позволяя настраивать индексы, которые основаны на аналитике или комбинации аналитик.</span><span class="sxs-lookup"><span data-stu-id="71045-322">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="71045-323">В настоящее время для индексов можно настроить не более пяти.</span><span class="sxs-lookup"><span data-stu-id="71045-323">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="71045-324">Необходимо тщательно продумать, какая аналитика или комбинация аналитик будет использоваться, перед реализацией, чтобы обеспечить, что она будут удовлетворять вашим деловым потребностям.</span><span class="sxs-lookup"><span data-stu-id="71045-324">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="71045-325">Например, если требуется запросить продукты следующим образом:</span><span class="sxs-lookup"><span data-stu-id="71045-325">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="71045-326">Запрос агрегированного наличия продуктов по аналитикам *Цвет* и *Размер*.</span><span class="sxs-lookup"><span data-stu-id="71045-326">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="71045-327">В некоторых случаях требуется только выполнить запрос по продукту в целом.</span><span class="sxs-lookup"><span data-stu-id="71045-327">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="71045-328">Можно определить два индекса следующим образом:</span><span class="sxs-lookup"><span data-stu-id="71045-328">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="71045-329">Пустая скобка будет агрегирована на основе идентификатора продукта в секции.</span><span class="sxs-lookup"><span data-stu-id="71045-329">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="71045-330">Индексация определяет способ группировки результатов в зависимости от настройки запроса `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="71045-330">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="71045-331">В этом случае, если никакие значения `groupBy` не определены, будут выведены итоги по `productid`.</span><span class="sxs-lookup"><span data-stu-id="71045-331">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="71045-332">В противном случае, если определить `groupBy` как `groupBy=ColorId&groupBy=SizeId`, будет возвращено несколько строк, в зависимости от различных комбинаций цвета и размера в системе.</span><span class="sxs-lookup"><span data-stu-id="71045-332">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="71045-333">Критерии запроса можно разместить в теле запроса.</span><span class="sxs-lookup"><span data-stu-id="71045-333">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="71045-334">Вот пример запроса для комбинации цвета и размера продукта.</span><span class="sxs-lookup"><span data-stu-id="71045-334">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
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

<span data-ttu-id="71045-335">Для поля `filters` в настоящее время только `ProductId` поддерживает несколько значений.</span><span class="sxs-lookup"><span data-stu-id="71045-335">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="71045-336">Если `ProductId` является пустым массивом, будут запрашиваться все продукты.</span><span class="sxs-lookup"><span data-stu-id="71045-336">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="71045-337">Пользовательское измерение</span><span class="sxs-lookup"><span data-stu-id="71045-337">Custom measurement</span></span>

<span data-ttu-id="71045-338">Количества измерений по умолчанию связаны с Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="71045-338">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="71045-339">Однако, возможно, потребуется количество, состоящее из комбинации измерений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71045-339">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="71045-340">Чтобы сделать это, можно задать конфигурацию настраиваемых количеств, которая будет добавлена к выходным данным запросов запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="71045-340">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="71045-341">Функциональность просто позволяют определить набор мер, которые будут добавлены, и/или набор мер, которые будут вычтены, чтобы сформировать настраиваемое измерение.</span><span class="sxs-lookup"><span data-stu-id="71045-341">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="71045-342">Например, со следующим условием запроса вы настроите пользовательское количество измерения как `MyCustomAvailableforReservation` для потребления системой потребления.</span><span class="sxs-lookup"><span data-stu-id="71045-342">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="71045-343">Система потребления</span><span class="sxs-lookup"><span data-stu-id="71045-343">Consumption system</span></span> | <span data-ttu-id="71045-344">Рассчитанные меры</span><span class="sxs-lookup"><span data-stu-id="71045-344">Calculated measurers</span></span> | <span data-ttu-id="71045-345">Иcточник данных</span><span class="sxs-lookup"><span data-stu-id="71045-345">Data source</span></span> | <span data-ttu-id="71045-346">Модификатор</span><span class="sxs-lookup"><span data-stu-id="71045-346">Modifier</span></span> | <span data-ttu-id="71045-347">Тип расчета модификатора</span><span class="sxs-lookup"><span data-stu-id="71045-347">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="71045-348">Сложение</span><span class="sxs-lookup"><span data-stu-id="71045-348">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="71045-349">Сложение</span><span class="sxs-lookup"><span data-stu-id="71045-349">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="71045-350">Вычитание</span><span class="sxs-lookup"><span data-stu-id="71045-350">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="71045-351">Сложение</span><span class="sxs-lookup"><span data-stu-id="71045-351">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="71045-352">Вычитание</span><span class="sxs-lookup"><span data-stu-id="71045-352">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="71045-353">Сложение</span><span class="sxs-lookup"><span data-stu-id="71045-353">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="71045-354">Сложение</span><span class="sxs-lookup"><span data-stu-id="71045-354">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="71045-355">Вычитание</span><span class="sxs-lookup"><span data-stu-id="71045-355">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="71045-356">Вычитание</span><span class="sxs-lookup"><span data-stu-id="71045-356">Subtraction</span></span> |

<span data-ttu-id="71045-357">При этом запрос настраиваемого количества измерения возвратит следующий результат.</span><span class="sxs-lookup"><span data-stu-id="71045-357">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="71045-358">Выходные данные `MyCustomAvailableforReservation` основаны на параметрах расчета в настраиваемых измерениях следующим образом:</span><span class="sxs-lookup"><span data-stu-id="71045-358">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="71045-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="71045-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="71045-360">Разноска изменений запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="71045-360">Posting on-hand changes</span></span>

<span data-ttu-id="71045-361">Точный URL-адрес, на который будет разнесено событие, будет зависеть от географического региона.</span><span class="sxs-lookup"><span data-stu-id="71045-361">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="71045-362">Он будет иметь вид:</span><span class="sxs-lookup"><span data-stu-id="71045-362">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="71045-363">После аутентификации этот URL-адрес может использоваться вместе с методом HTTP `POST` для отправки в службу событий изменения запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="71045-363">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="71045-364">Специальный заголовок используется для связи с службами Dynamics 365 с помощью запросов HTTP, в которых указывается идентификатор среды экземпляра Supply Chain Management, с которым связаны данные.</span><span class="sxs-lookup"><span data-stu-id="71045-364">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="71045-365">Пример:</span><span class="sxs-lookup"><span data-stu-id="71045-365">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="71045-366">Пример 1 разноски запроса изменений запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="71045-366">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="71045-367">В этом примере показан сценарий, в котором будет настроена конфигурация аналитики в Power Apps.</span><span class="sxs-lookup"><span data-stu-id="71045-367">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="71045-368">Следующий запрос используется для настройки сопоставления измерений в Power Apps:</span><span class="sxs-lookup"><span data-stu-id="71045-368">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="71045-369">Теперь можно указать `dimensionDataSource` и использовать пользовательские измерения в запросах.</span><span class="sxs-lookup"><span data-stu-id="71045-369">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="71045-370">Система будет автоматически преобразовывать пользовательские измерения в базовые измерения.</span><span class="sxs-lookup"><span data-stu-id="71045-370">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="71045-371">Пример 2 разноски запроса изменений запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="71045-371">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="71045-372">В этом примере показан сценарий, в котором не настроены сопоставления для конфигурации аналитик в Power Apps, поэтому при разноске должны использоваться также базовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="71045-372">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="71045-373">Все аналитики должны быть базовыми аналитиками, если поле `dimensionDataSource` имеет значение NULL, является пустым или пробелом.</span><span class="sxs-lookup"><span data-stu-id="71045-373">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="71045-374">Свойства полей документов JSON</span><span class="sxs-lookup"><span data-stu-id="71045-374">JSON document field properties</span></span>

<span data-ttu-id="71045-375">Поля из примеров запросов JSON, приведенных выше, имеют свойства, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="71045-375">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="71045-376">FieldID</span><span class="sxs-lookup"><span data-stu-id="71045-376">Field ID</span></span> | <span data-ttu-id="71045-377">описание</span><span class="sxs-lookup"><span data-stu-id="71045-377">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="71045-378">Уникальный код для конкретного события изменения.</span><span class="sxs-lookup"><span data-stu-id="71045-378">A unique ID for the specific change event.</span></span> <span data-ttu-id="71045-379">Этот код используется, чтобы гарантировать, что при возникновении ошибки при обмене данными с службой во время разноски повторная отправка события не приведет к тому, что в системе дважды будет учитываться одно и то же событие.</span><span class="sxs-lookup"><span data-stu-id="71045-379">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="71045-380">Идентификатор организации, связанной с событием.</span><span class="sxs-lookup"><span data-stu-id="71045-380">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="71045-381">Это сопоставляется с организациями Supply Chain Management или идентификаторами областей данных.</span><span class="sxs-lookup"><span data-stu-id="71045-381">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="71045-382">Идентификатор рассматриваемого продукта.</span><span class="sxs-lookup"><span data-stu-id="71045-382">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="71045-383">Количество, для которого должны быть изменены запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="71045-383">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="71045-384">Если, например, 10 новых бубликов были добавлены на полку, это значение было бы равно 10.</span><span class="sxs-lookup"><span data-stu-id="71045-384">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="71045-385">Если 3 бублика были удалены с полки или проданы, это значение было бы равно -3.</span><span class="sxs-lookup"><span data-stu-id="71045-385">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="71045-386">Источник данных для аналитик, используемых в разноске события изменения и запроса.</span><span class="sxs-lookup"><span data-stu-id="71045-386">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="71045-387">Если указан источник данных, можно использовать настраиваемые аналитики из указанного источника данных.</span><span class="sxs-lookup"><span data-stu-id="71045-387">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="71045-388">С помощью конфигурации аналитик видимость запасов может сопоставлять пользовательские аналитики с общими аналитиками по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71045-388">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="71045-389">Если параметр `dimensionDataSource` не указан, в запросах могут использоваться только общие аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71045-389">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="71045-390">Динамический набор пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="71045-390">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="71045-391">Это будет сопоставляться с некоторыми аналитиками в Supply Chain Management, но можно также добавить настраиваемые аналитики(например, *Источник*), которые могут обозначать, когда событие поступает из Supply Chain Management или из внешней системы.</span><span class="sxs-lookup"><span data-stu-id="71045-391">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="71045-392">Запрос текущих запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="71045-392">Querying current on-hand</span></span>

<span data-ttu-id="71045-393">Конечная точка для запроса текущих запасов в наличии будет иметь похожий URL-адрес:</span><span class="sxs-lookup"><span data-stu-id="71045-393">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="71045-394">Запрос будет выполняться с использованием метода HTTP `POST`.</span><span class="sxs-lookup"><span data-stu-id="71045-394">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="71045-395">Пример 1 запроса текущих запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="71045-395">Current on-hand query example 1</span></span>

<span data-ttu-id="71045-396">В этом примере показан сценарий, в котором вы уже выполнили настройку конфигурации аналитики в Power Apps.</span><span class="sxs-lookup"><span data-stu-id="71045-396">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="71045-397">Следующий запрос используется для настройки сопоставления измерений в Power Apps:</span><span class="sxs-lookup"><span data-stu-id="71045-397">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="71045-398">Теперь можно указать `dimensionDataSource` и использовать пользовательские измерения в запросах.</span><span class="sxs-lookup"><span data-stu-id="71045-398">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="71045-399">Система будет автоматически преобразовывать пользовательские измерения в базовые измерения.</span><span class="sxs-lookup"><span data-stu-id="71045-399">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="71045-400">Можно указать `DimensionDataSource` в поле `filters` и указать настраиваемые аналитики в обоих полях `filters` и `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="71045-400">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="71045-401">Система будет автоматически преобразовывать пользовательские измерения в базовые измерения.</span><span class="sxs-lookup"><span data-stu-id="71045-401">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="71045-402">Пример 2 запроса текущих запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="71045-402">Current on-hand query example 2</span></span>

<span data-ttu-id="71045-403">В этом примере показан сценарий, в котором не настроены сопоставления для конфигурации аналитик в Power Apps, поэтому при разноске должны использоваться также базовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="71045-403">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="71045-404">Все аналитики должны быть базовыми аналитиками, если поле `dimensionDataSource` в разделе `filters` имеет значение NULL, является пустым или пробелом.</span><span class="sxs-lookup"><span data-stu-id="71045-404">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="71045-405">Пример возвращаемого результата</span><span class="sxs-lookup"><span data-stu-id="71045-405">Example return result</span></span>

<span data-ttu-id="71045-406">Запросы, показанные в предыдущих примерах, могут вернуть результат, подобный этому.</span><span class="sxs-lookup"><span data-stu-id="71045-406">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="71045-407">Обратите внимание, что поля количества структурированы как словарь мер и связанные с ними значений.</span><span class="sxs-lookup"><span data-stu-id="71045-407">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]