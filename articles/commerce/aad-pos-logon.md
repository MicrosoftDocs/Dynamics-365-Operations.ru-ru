---
title: Настройка аутентификации Azure Active Directory для входа на POS-терминал
description: В этой теме объясняется, как настроить Azure Active Directory как метод аутентификации в POS-терминале Microsoft Dynamics 365 Commerce.
author: boycezhu
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 34a7946a56a58655bc9ae23e060fc50ab01f2c6e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937466"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="2e4b4-103">Настройка аутентификации Azure Active Directory для входа на POS-терминал</span><span class="sxs-lookup"><span data-stu-id="2e4b4-103">Configure Azure Active Directory authentication for POS sign-in</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2e4b4-104">В этой теме объясняется, как настроить Azure Active Directory (Azure AD) как метод аутентификации в POS-терминале Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-104">This topic explains how to configure Azure Active Directory (Azure AD) as the authentication method in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="2e4b4-105">Розничные продавцы, использующие Dynamics 365 Commerce с другими облачными службами Майкрософт, такими как Microsoft Azure, Microsoft 365 и Microsoft Teams обычно хотят использовать Azure AD для централизованного управления учетными данными пользователя для безопасного и надежного входа в систему между приложениями.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-105">Retailers who use Dynamics 365 Commerce along with other Microsoft cloud services such as Microsoft Azure, Microsoft 365, and Microsoft Teams typically want to use Azure AD for centralized management of user credentials for a secure and seamless sign-in experience across applications.</span></span> <span data-ttu-id="2e4b4-106">Чтобы использовать аутентификацию Azure AD для Commerce POS, необходимо сначала настроить Azure AD как метод аутентификации в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-106">To use Azure AD authentication for Commerce POS, you must first configure Azure AD as the authentication method in Commerce headquarters.</span></span>

## <a name="configure-pos-authentication-method"></a><span data-ttu-id="2e4b4-107">Настройка метода аутентификации POS</span><span class="sxs-lookup"><span data-stu-id="2e4b4-107">Configure POS authentication method</span></span>

<span data-ttu-id="2e4b4-108">Чтобы настроить метод аутентификации POS в Commerce Headquarters, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-108">To configure the POS authentication method in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="2e4b4-109">Перейдите **Retail и Commerce \> Настройка канала \> Настройка POS \> Профили POS \> Профили функциональности** и выберите изменяемый профиль функциональности.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-109">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**, and select a functionality profile to change.</span></span>
1. <span data-ttu-id="2e4b4-110">В разделе **Вход в POS для персонала** на экспресс-вкладке **Функции** выберите нужный метод аутентификации из раскрывающегося списка **Метод аутентификации при входе**.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-110">In the **POS staff logon** section of the **Functions** FastTab, select a desired authentication method option from the **Logon authentication method** drop-down list.</span></span>

    <span data-ttu-id="2e4b4-111">Есть три варианта **Метода аутентификации для входа в систему**:</span><span class="sxs-lookup"><span data-stu-id="2e4b4-111">The **Logon authentication method** has three options:</span></span>
    
    - <span data-ttu-id="2e4b4-112">**Идентификатор персонала и пароль** — этот параметр по умолчанию требует, чтобы пользователи POS вводили код персонала и пароль для входа в POS, а также для доступа к функции переопределения менеджера.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-112">**Personnel ID and Password** - This default option requires POS users to enter a personnel ID and password to sign in to the POS and to access manager override functionality.</span></span>
    - <span data-ttu-id="2e4b4-113">**Azure AD без единого входа** — этот параметр требует, чтобы пользователи POS использовали учетные данные Azure AD для входа в POS и доступа к функции переопределения менеджера.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-113">**Azure AD without single sign-on** - This option requires POS users to use Azure AD credentials to sign in to the POS and access manager override functionality.</span></span> <span data-ttu-id="2e4b4-114">После обновления или повторного открытия клиента POS пользователь POS должен предоставить учетные данные Azure AD для повторного входа в систему.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-114">When the POS client is refreshed or reopened, the POS user must provide Azure AD credentials to sign in again.</span></span>
    - <span data-ttu-id="2e4b4-115">**Azure AD с единым входом** — когда этот параметр выбран, пользователи POS могут входить в Cloud POS (CPOS), используя активные учетные данные Azure AD, используемые другими веб-приложениями в том же веб-браузере, или входить в Modern POS (MPOS), используя учетные данные Azure AD, зарегистрированные в Windows.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-115">**Azure AD with single sign-on** - When this option is selected, POS users are able to sign in to Cloud POS (CPOS) using active Azure AD credentials that are being used by other web applications in the same web browser, or sign in to Modern POS (MPOS) using Azure AD credentials signed in to Windows.</span></span> <span data-ttu-id="2e4b4-116">Оба метода позволяют выполнять вход без необходимости ввода учетных данных Azure AD на экране входа в POS.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-116">Both methods allow sign-in without needing to enter Azure AD credentials on the POS sign-in screen.</span></span> <span data-ttu-id="2e4b4-117">Однако для доступа к функциям переопределения менеджера в POS все равно потребуется выполнить вход с использованием учетных данных Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-117">However, accessing the POS manager override functionality will still require sign-in using Azure AD credentials.</span></span>

1. <span data-ttu-id="2e4b4-118">Перейдите **Retail и Commerce > ИТ Retail и Commerce > График распределения** и выполните задание **1070 (Конфигурация канала)**, чтобы синхронизировать последние настройки профиля функциональности с клиентами POS.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-118">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule** and run the **1070 (Channel configuration)** job to synchronize the latest functionality profile settings to POS clients.</span></span>

> [!NOTE]
> - <span data-ttu-id="2e4b4-119">Параметр метода аутентификации **Azure AD без единого входа** заменяет параметр **Azure Active Directory** в Commerce версии 10.0.18 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-119">The **Azure AD without single sign-on** authentication method option replaces the **Azure Active Directory** option in Commerce version 10.0.18 and earlier.</span></span>
> - <span data-ttu-id="2e4b4-120">Аутентификация Azure AD требует наличия активного подключения к Интернету и не будет работать, если POS находится вне сети.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-120">Azure AD authentication requires an active internet connection, and won't function when the POS is offline.</span></span>

## <a name="associate-azure-ad-accounts-with-pos-users"></a><span data-ttu-id="2e4b4-121">Связывание учётных записей Azure AD с пользователями POS</span><span class="sxs-lookup"><span data-stu-id="2e4b4-121">Associate Azure AD accounts with POS users</span></span>

<span data-ttu-id="2e4b4-122">Для использования Azure AD в качестве метода аутентификации POS необходимо связать учетные записи Azure AD с пользователями POS в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-122">To use Azure AD as the POS authentication method, you must associate Azure AD accounts with POS users in Commerce headquarters.</span></span> 

<span data-ttu-id="2e4b4-123">Чтобы связать учетные записи Azure AD с пользователями POS в Commerce Headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-123">To associate Azure AD accounts with POS users in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="2e4b4-124">Перейдите **Retail и Commerce > Сотрудники > Работники** и откройте запись работника.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-124">Go to **Retail and Commerce > Employees > Workers** and open a worker record.</span></span>
1. <span data-ttu-id="2e4b4-125">В области действий выберите вкладку **Commerce**, затем в **Внешнее удостоверение** выберите **Связать существующее удостоверение**.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-125">On the Action Pane, select the **Commerce** tab, then under **External identity** select **Associate existing identity**.</span></span> 
1. <span data-ttu-id="2e4b4-126">В диалоговом окне **Использовать существующее внешнее удостоверение** выберите **Поиск по электронной почте**, введите адрес электронной почты Azure AD, затем выберите **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-126">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="2e4b4-127">Выберите возвращенную учетную запись Azure AD, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-127">Select the Azure AD account that is returned, then select **OK**.</span></span>

<span data-ttu-id="2e4b4-128">После этапов настройки выше будут заполнены поля **Псевдоним**, **UPN** и **Внешний подкод** на вкладке **Commerce** на странице сведений о работнике.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-128">After the configuration steps above, the **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

<span data-ttu-id="2e4b4-129">Необходимо выполнить задание **1060 (персонал)** в **Retail и Commerce > ИТ Retail и Commerce > График распределения**, чтобы синхронизировать данные последних пользователей POS и учетных записей Azure AD в канал.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-129">You must run the **1060 (Staff)** job in **Retail and Commerce > Retail and Commerce IT > Distribution schedule** to synchronize the latest POS user and Azure AD account data to the channel.</span></span>

> [!NOTE]
> <span data-ttu-id="2e4b4-130">После обновления информации о сотруднике, например пароля, разрешения POS, связанной учетной записи Azure AD или адресной книги сотрудника в Commerce Headquarters, настоятельно рекомендуется выполнить задание **1060 (персонал)** для синхронизации последней информации о работнике с каналом.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-130">As a best practice, after worker information such as password, POS permission, associated Azure AD account, or employee address book is updated in Commerce headquarters, it is highly recommended to run the **1060 (Staff)** job to synchronize the latest worker information to the channel.</span></span> <span data-ttu-id="2e4b4-131">Затем клиент POS может выбрать правильные данные для проверок аутентификации пользователя и авторизации.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-131">The POS client can then fetch the correct data for user authentication and authorization checks.</span></span>

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a><span data-ttu-id="2e4b4-132">Регистр блокировки POS и выход с аутентификацией Azure AD</span><span class="sxs-lookup"><span data-stu-id="2e4b4-132">POS lock register and sign-out with Azure AD authentication</span></span>

<span data-ttu-id="2e4b4-133">При настройке POS для использования метода аутентификации Azure AD происходит следующее:</span><span class="sxs-lookup"><span data-stu-id="2e4b4-133">The following occurs when POS is configured to use the Azure AD authentication method:</span></span>

- <span data-ttu-id="2e4b4-134">Функция **Блокировать регистр** будет недоступна в приложении POS.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-134">The **Lock register** function will not be available in the POS application.</span></span> 
- <span data-ttu-id="2e4b4-135">Функция **Автоматически блокировать** ведет себя так же, как функция **Автоматический выход из системы**.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-135">The **Automatically lock** function will behave the same as the **Automatically logoff** function.</span></span>
- <span data-ttu-id="2e4b4-136">Если пользователь POS выбирает **Выход из системы**, пользователю будет предложено войти в систему, используя учетные данные Azure AD при следующем запуске POS независимо от того, активирована ли функция единого входа.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-136">If the POS user selects **Log off**, the user will be asked to sign in with Azure AD credentials the next time the POS launches, regardless of whether single sign-in is enabled.</span></span>

## <a name="manager-override-functionality-with-azure-ad-authentication"></a><span data-ttu-id="2e4b4-137">Функции переопределения менеджера с аутентификацией Azure AD</span><span class="sxs-lookup"><span data-stu-id="2e4b4-137">Manager override functionality with Azure AD authentication</span></span>

<span data-ttu-id="2e4b4-138">Когда POS настроен на использование аутентификации Azure AD, функция переопределения менеджера открывает диалоговое окно, запрашивающее учетные данные Azure AD пользователя-менеджера.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-138">When the POS is configured to use Azure AD authentication, the manager override functionality will open a dialog box that prompts for the manager user's Azure AD credentials.</span></span> <span data-ttu-id="2e4b4-139">После утверждения входа менеджера учетные данные Azure AD менеджера будут удалены, а учетные данные Azure AD предыдущего пользователя будут использоваться для последующих операций с POS.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-139">After manager sign-in is approved, the manager's Azure AD credentials will be dropped and the previous user's Azure AD credentials will be used for subsequent POS operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="2e4b4-140">В Commerce версии 10.0.18 и более ранних версиях функция переопределения менеджера не поддерживается Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-140">In Commerce versions 10.0.18 and earlier, the manager override function does not support Azure AD.</span></span> <span data-ttu-id="2e4b4-141">Идентификатор персонала и пароль требуются, даже если POS настроен на использование метода аутентификации Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-141">A personnel ID and password are required even if the POS is configured to use the Azure AD authentication method.</span></span>
> - <span data-ttu-id="2e4b4-142">При использовании СPOS с веб-браузером Safari на устройстве Apple iOS необходимо сначала отключить **Блокировать всплывающие окна** в параметрах Safari, чтобы функция переопределения работала с аутентификацией Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-142">When using CPOS with the Safari web browser on an Apple iOS device, you must first turn off **Block Pop-ups** in Safari settings for the manager override functionality to work with Azure AD authentication.</span></span> 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a><span data-ttu-id="2e4b4-143">Рекомендации по безопасности для аутентификации POS на основе Azure AD на общих устройствах</span><span class="sxs-lookup"><span data-stu-id="2e4b4-143">Security best practices for Azure AD-based POS authentication on shared devices</span></span>

<span data-ttu-id="2e4b4-144">Многие розничные компании настраивают свою среду розничной торговли таким образом, что у нескольких пользователей был доступ к приложению POS с общего физического устройства.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-144">Many retailers set up their retail store environment in a way that multiple users need to access the POS application from a shared physical device.</span></span> <span data-ttu-id="2e4b4-145">В этом контексте, в то время как единый вход предоставляет удобный и удобный механизм аутентификации, он может также создать брешь в системе безопасности, когда текущий пользователь POS может не знать, что учетные данные другого пользователя используются для выполнения транзакций или операций в POS.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-145">In that context, while single sign-in provides a convenient and seamless authentication experience, it may also create a security loophole where the current POS user may not realize that another user's credentials are being used to perform transactions or operations in the POS.</span></span> <span data-ttu-id="2e4b4-146">Прежде чем настроить POS для использования метода аутентификации Azure AD, настоятельно рекомендуется просмотреть политику безопасности и параметры входа общего устройства, чтобы определить, какой вариант подходит лучше.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-146">Before you configure the POS to use the Azure AD authentication method, it is highly recommended to review your security policy and the shared device's sign-in settings to decide which option is the best fit.</span></span>

- <span data-ttu-id="2e4b4-147">Если в розничной среде используется общая учетная запись (например, локальная учетная запись) для входа в систему физического устройства, рекомендуется использовать вариант **Azure AD без единого входа в систему**.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-147">If your retail environment uses a shared account (for example, a local account) for physical device sign-in, it's recommended to use the **Azure AD without single sign-on** option.</span></span> <span data-ttu-id="2e4b4-148">Это гарантирует, что каждый пользователь POS будет явно предоставлять учетные данные Azure AD для входа в POS.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-148">This ensures that each POS user explicitly provides Azure AD credentials to sign in to the POS.</span></span>
- <span data-ttu-id="2e4b4-149">Если розничной среде требуется, чтобы сотрудники использовали собственные учетные записи Azure AD для входа в POS и физическое устройство размещения, рекомендуется использовать вариант **Azure AD с единым входом**.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-149">If your retail environment requires employees to use their own Azure AD accounts to sign in to the POS and its hosting physical device, it's recommended to use the **Azure AD with single sign-on** option.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e4b4-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2e4b4-150">Additional resources</span></span>

[<span data-ttu-id="2e4b4-151">Настройка работника</span><span class="sxs-lookup"><span data-stu-id="2e4b4-151">Configure a worker</span></span>](tasks/worker.md)

[<span data-ttu-id="2e4b4-152">Создание профиля функциональности розничной торговли</span><span class="sxs-lookup"><span data-stu-id="2e4b4-152">Create a retail functionality profile</span></span>](retail-functionality-profile.md)


[<span data-ttu-id="2e4b4-153">Настройка функциональности расширенного входа для MPOS и Cloud POS</span><span class="sxs-lookup"><span data-stu-id="2e4b4-153">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="2e4b4-154">Рекомендации по безопасности для работы с Cloud POS в общих средах</span><span class="sxs-lookup"><span data-stu-id="2e4b4-154">Security best practices for Cloud POS in shared environments</span></span>](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
