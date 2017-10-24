---
title: "Установка и настройка Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing"
description: "В этом разделе описывается, как установить и настроить Microsoft Dynamics 365 for Finance and Operations — Warehousing."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 31e77b27d4bf95c997817b3a053b33119562adf8
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a><span data-ttu-id="8290b-103">Установка и настройка Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing</span><span class="sxs-lookup"><span data-stu-id="8290b-103">Install and configure Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8290b-104">В этом разделе описывается, как установить и настроить Microsoft Dynamics 365 for Finance and Operations — Warehousing.</span><span class="sxs-lookup"><span data-stu-id="8290b-104">This topic describes how to install and configure Microsoft Dynamics 365 for Finance and Operations - Warehousing.</span></span>

<span data-ttu-id="8290b-105">Finance and Operations — Warehousing представляет собой приложение, доступное в магазине Google Play и в Магазине Windows.</span><span class="sxs-lookup"><span data-stu-id="8290b-105">Finance and Operations - Warehousing is an application available on Google Play Store and Windows Store.</span></span> <span data-ttu-id="8290b-106">Для текущей версии Finance and Operations это приложение предоставляется в качестве отдельного компонента, что означает самостоятельное развертывание на устройствах, используемые для складских задач.</span><span class="sxs-lookup"><span data-stu-id="8290b-106">For the current version of Finance and Operations, this app is provided as a standalone component, which means self-deployment on devices used for warehouse tasks.</span></span> <span data-ttu-id="8290b-107">Чтобы использовать приложение в среде Finance and Operations, необходимо загрузить приложение на каждое устройство и настроить его для подключения к среде Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8290b-107">In order to use the app in your Finance and Operations environment, you must download the app on each device and configure it to connect to your Finance and Operations environment.</span></span> <span data-ttu-id="8290b-108">В этом разделе описывается, как установить приложение на устройствах.</span><span class="sxs-lookup"><span data-stu-id="8290b-108">This topic describes how to install the app on your devices.</span></span> <span data-ttu-id="8290b-109">Также объясняется, как настроить приложение для подключения к среде Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8290b-109">It also explains how to configure the app to connect to your Finance and Operations environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8290b-110">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="8290b-110">Prerequisites</span></span>
<span data-ttu-id="8290b-111">Приложение доступно в операционных системах Android и Windows.</span><span class="sxs-lookup"><span data-stu-id="8290b-111">The app is available on Android and Windows operating systems.</span></span> <span data-ttu-id="8290b-112">Чтобы использовать это приложение, на устройстве должна быть установлена одна из следующих поддерживаемых операционных систем.</span><span class="sxs-lookup"><span data-stu-id="8290b-112">To use this app, you must have one of the following supported operating systems installed on your devices.</span></span> <span data-ttu-id="8290b-113">Также необходимо иметь одну из следующих поддерживаемых версий Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8290b-113">You must also have one of the following supported versions of Finance and Operations.</span></span> <span data-ttu-id="8290b-114">Используйте сведения из следующей таблицы для оценки, готовы ли ваши аппаратная и программная среды для поддержки установки.</span><span class="sxs-lookup"><span data-stu-id="8290b-114">Use the information in the following table to evaluate if your hardware and software environment is ready to support the installation.</span></span>

| <span data-ttu-id="8290b-115">Платформа</span><span class="sxs-lookup"><span data-stu-id="8290b-115">Platform</span></span>                    | <span data-ttu-id="8290b-116">Версия</span><span class="sxs-lookup"><span data-stu-id="8290b-116">Version</span></span>                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8290b-117">Android</span><span class="sxs-lookup"><span data-stu-id="8290b-117">Android</span></span>                     | <span data-ttu-id="8290b-118">4.4, 5.0, 6.0</span><span class="sxs-lookup"><span data-stu-id="8290b-118">4.4, 5.0, 6.0</span></span>                                                                                                                                                               |
| <span data-ttu-id="8290b-119">Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="8290b-119">Windows (UWP)</span></span>               | <span data-ttu-id="8290b-120">Windows 10 (все версии)</span><span class="sxs-lookup"><span data-stu-id="8290b-120">Windows 10 (all versions)</span></span>                                                                                                                                                   |
| <span data-ttu-id="8290b-121">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8290b-121">Finance and Operations</span></span> | <span data-ttu-id="8290b-122">Microsoft Finance and Operations версии 1611</span><span class="sxs-lookup"><span data-stu-id="8290b-122">Microsoft Finance and Operations version 1611</span></span> <br><span data-ttu-id="8290b-123">–или–</span><span class="sxs-lookup"><span data-stu-id="8290b-123">-or-</span></span> <br><span data-ttu-id="8290b-124">Microsoft Dynamics Dynamics AX версии 7.0/7.0.1 и платформа Microsoft Dynamics AX с обновлением 2 и исправлением КБ 3210014</span><span class="sxs-lookup"><span data-stu-id="8290b-124">Microsoft Dynamics Dynamics AX version 7.0/7.0.1 and Microsoft Dynamics AX platform update 2 with hotfix KB 3210014</span></span> |

## <a name="get-the-app"></a><span data-ttu-id="8290b-125">Получение приложения</span><span class="sxs-lookup"><span data-stu-id="8290b-125">Get the app</span></span>
-   <span data-ttu-id="8290b-126">Windows (UWP): [Finance and Operations — Warehousing в Магазине Windows](https://www.microsoft.com/store/apps/9p1bffd5tstm)</span><span class="sxs-lookup"><span data-stu-id="8290b-126">Windows (UWP): [Finance and Operations - Warehousing on the Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)</span></span>
-   <span data-ttu-id="8290b-127">Android:</span><span class="sxs-lookup"><span data-stu-id="8290b-127">Android:</span></span>
    - [<span data-ttu-id="8290b-128">Finance and Operations — Warehousing в магазине Google Play</span><span class="sxs-lookup"><span data-stu-id="8290b-128">Finance and Operations - Warehousing on the Google Play Store</span></span>](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [<span data-ttu-id="8290b-129">Finance and Operations — Warehousing в Zebra App Gallery</span><span class="sxs-lookup"><span data-stu-id="8290b-129">Finance and Operations - Warehousing on the Zebra App Gallery</span></span>](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-active-directory"></a><span data-ttu-id="8290b-130">Создание приложения веб-службы в Active Directory</span><span class="sxs-lookup"><span data-stu-id="8290b-130">Create a web service application in Active Directory</span></span>
<span data-ttu-id="8290b-131">Чтобы приложение могло взаимодействовать с определенным сервером Finance and Operations, необходимо зарегистрировать приложение веб-службы в Azure Active Directory для владельца Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8290b-131">To enable the app to interact with a specific Finance and Operations server, you must register a web service application in a Azure Active Directory for the Finance and Operations tenant.</span></span> <span data-ttu-id="8290b-132">По соображениям безопасности рекомендуется создавать приложения веб-службы для каждого устройства, которое используется.</span><span class="sxs-lookup"><span data-stu-id="8290b-132">For security reasons, we recommend that you create a web service application for each device that you use.</span></span> <span data-ttu-id="8290b-133">Чтобы создать приложение веб-службы в Azure Active Directory (Azure AD), выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="8290b-133">To create a web service application in Azure Active Directory (Azure AD), complete the following steps:</span></span>

1.  <span data-ttu-id="8290b-134">В веб-браузере перейдите к <https://manage.windowsazure.com>.</span><span class="sxs-lookup"><span data-stu-id="8290b-134">In a web browser, go to <https://manage.windowsazure.com>.</span></span>
2.  <span data-ttu-id="8290b-135">Введите имя и пароль пользователя, который имеет доступ к подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="8290b-135">Enter the name and password for the user who has access to the Azure subscription.</span></span>
3.  <span data-ttu-id="8290b-136">На портале Azure в левой области навигации щелкните **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-пример-active-directory](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-136">In Azure Portal, in the left navigation pane, click **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)</span></span>
4.  <span data-ttu-id="8290b-137">В сетке выберите экземпляр службы каталогов Active Directory, используемый Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8290b-137">In the grid, select the Active Directory instance that is used by Finance and Operations.</span></span>
5.  <span data-ttu-id="8290b-138">На верхней панели инструментов щелкните **Приложения**.</span><span class="sxs-lookup"><span data-stu-id="8290b-138">On the top toolbar, click **Applications**.</span></span> <span data-ttu-id="8290b-139">[![wh-02-приложения-active-directory](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-139">[![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)</span></span>
6.  <span data-ttu-id="8290b-140">В нижней области нажмите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="8290b-140">In the bottom pane, click **Add**.</span></span> <span data-ttu-id="8290b-141">Запускается мастер **Добавление приложения**.</span><span class="sxs-lookup"><span data-stu-id="8290b-141">The **Add application** wizard starts.</span></span>
7.  <span data-ttu-id="8290b-142">Введите имя приложения и выберите **Веб-приложение и/или веб-интерфейс API**.</span><span class="sxs-lookup"><span data-stu-id="8290b-142">Enter a name for the application and select **Web application and/or web API**.</span></span> <span data-ttu-id="8290b-143">[![wh-03-добавить-приложение-active-directory](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-143">[![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)</span></span>
8.  <span data-ttu-id="8290b-144">Введите URL-адрес входа в систему, являющийся URL-адресом вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="8290b-144">Enter the sign-on URL, which is your web app URL.</span></span> <span data-ttu-id="8290b-145">Этот URL-адрес совпадает с URL-адресом развертывания, но в конец добавляется oauth.</span><span class="sxs-lookup"><span data-stu-id="8290b-145">This URL is the same as your deployment URL, but oauth is added to the end.</span></span> <span data-ttu-id="8290b-146">Введите App ID URI, это значение является обязательным, но не требуется для аутентификации.</span><span class="sxs-lookup"><span data-stu-id="8290b-146">Enter the App ID URI, this value is mandatory, but isn’t required for the authentication.</span></span> <span data-ttu-id="8290b-147">Убедитесь, что этот App ID URI является тестовым URI как https://contosooperations/wmapp, так как использование URL-адреса развертывания может привести к проблемам входа в другие приложения AAD, такие как надстройки Excel.</span><span class="sxs-lookup"><span data-stu-id="8290b-147">Make sure that this App ID URI is a mock URI like https://contosooperations/wmapp, since using the URL of your deployment can cause sign-in issues in other AAD applications such as the Excel Add-in.</span></span> <span data-ttu-id="8290b-148">[![WH-04-AD-add-properties3](./media/WH-04-AD-add-properties3.png)](./media/WH-04-AD-add-properties3.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-148">[![WH-04-AD-add-properties3](./media/WH-04-AD-add-properties3.png)](./media/WH-04-AD-add-properties3.png)</span></span>
9.  <span data-ttu-id="8290b-149">Перейдите на вкладку **Настройка**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-149">Go to the **Configure** tab. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)</span></span>
10. <span data-ttu-id="8290b-150">Прокрутите экран вниз до раздела **Разрешения для других приложений**.</span><span class="sxs-lookup"><span data-stu-id="8290b-150">Scroll down until you see the **Permissions to other applications** section.</span></span> <span data-ttu-id="8290b-151">Щелкните **Добавить приложение**.</span><span class="sxs-lookup"><span data-stu-id="8290b-151">Click **Add application**.</span></span> <span data-ttu-id="8290b-152">[![wh-06-добавление-разрешений-приложения-ad](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-152">[![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)</span></span>
11. <span data-ttu-id="8290b-153">Выберите **Microsoft Dynamics ERP** в списке.</span><span class="sxs-lookup"><span data-stu-id="8290b-153">Select **Microsoft Dynamics ERP** in the list.</span></span> <span data-ttu-id="8290b-154">Нажмите кнопку **Полная проверка** в правом углу страницы.</span><span class="sxs-lookup"><span data-stu-id="8290b-154">Click the **Complete check** button in the right corner of the page.</span></span> <span data-ttu-id="8290b-155">[![wh-07-выбор-разрешений-ad](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-155">[![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)</span></span>
12. <span data-ttu-id="8290b-156">В списке **Делегирование разрешений** установите все флажки.</span><span class="sxs-lookup"><span data-stu-id="8290b-156">In the **Delegate Permissions** list, select all the check boxes.</span></span> <span data-ttu-id="8290b-157">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8290b-157">Click **Save**.</span></span> <span data-ttu-id="8290b-158">[![wh-08-делегирование-разрешений-ad](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-158">[![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)</span></span>
13. <span data-ttu-id="8290b-159">Запишите следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="8290b-159">Make a note of the following information:</span></span>
    -   <span data-ttu-id="8290b-160">**Код клиента** — при прокрутке страницы вверх вы увидите **Код клиента**.</span><span class="sxs-lookup"><span data-stu-id="8290b-160">**Client ID** - As you scroll up the page, you will see **Client ID** displayed.</span></span>
    -   <span data-ttu-id="8290b-161">**Ключ** — в разделе **Ключи** создайте ключ, выбрав продолжительность, и скопируйте ключ.</span><span class="sxs-lookup"><span data-stu-id="8290b-161">**Key** - In the **Keys** section, create a key by selecting duration, and copy the key.</span></span> <span data-ttu-id="8290b-162">Этот ключ будет позже называется **Секрет клиента**.</span><span class="sxs-lookup"><span data-stu-id="8290b-162">This key will later be referred to as the **Client secret**.</span></span>

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a><span data-ttu-id="8290b-163">Создание и настройка учетной записи пользователя в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8290b-163">Create and configure a user account in Finance and Operations</span></span>
<span data-ttu-id="8290b-164">Чтобы включить Finance and Operations для использования приложения Azure AD, необходимо выполнить следующие шаги по настройке:</span><span class="sxs-lookup"><span data-stu-id="8290b-164">To enable Finance and Operations to use your Azure AD application, you need to complete the following configuration steps:</span></span>

1.  <span data-ttu-id="8290b-165">Создайте новую учетную запись пользователя в Azure Active Directory для владельца Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8290b-165">Create a new user account in Azure Active Directory for the Finance and Operations tenant.</span></span> <span data-ttu-id="8290b-166">Эта учетная запись пользователя предназначена для доступа к определенной пользовательской службе складского приложения, которую предоставляет сервер Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8290b-166">The purpose of this user account is to access the specific custom service of the warehousing app, which the Finance and Operations server exposes.</span></span> <span data-ttu-id="8290b-167">После выполнения этого шага у вас будут учетные данные пользователя WMDP, состоящие из адреса электронной почты WMDP и пароля WMDP.</span><span class="sxs-lookup"><span data-stu-id="8290b-167">After completing this step, you will have WMDP user credentials, which consist of a WMDP email address and a WMDP password.</span></span> <span data-ttu-id="8290b-168">Чтобы получить сведения об основных шагах для добавления пользователей в Azure AD и Finance and Operations, см. в этом учебнике: [Оформление подписки на Finance and Operations](../../dev-itpro/dev-tools/sign-up-preview-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="8290b-168">To learn about the basic steps for adding users to Azure AD and Finance and Operations, refer to this tutorial: [Sign up for a Finance and Operations subscription](../../dev-itpro/dev-tools/sign-up-preview-subscription.md).</span></span>
2.  <span data-ttu-id="8290b-169">Создайте пользователя Finance and Operations, который соответствует учетным данным пользователя складского приложения.</span><span class="sxs-lookup"><span data-stu-id="8290b-169">Create a Finance and Operations user that corresponds to the warehousing app user credentials.</span></span>
    1.  <span data-ttu-id="8290b-170">В Finance and Operations перейдите к **Администрирование системы** &gt; **Общее** &gt; **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="8290b-170">In Finance and Operations, go to **System administration** &gt; **Common** &gt; **Users**.</span></span>
    2.  <span data-ttu-id="8290b-171">Создайте нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="8290b-171">Create a new user.</span></span>
    3.  <span data-ttu-id="8290b-172">Назначьте пользователя складского мобильного устройства, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="8290b-172">Assign the Warehouse mobile device user, as shown in the following screenshot.</span></span> <span data-ttu-id="8290b-173">[![wh-09-добавление-роли-безопасности-пользователя](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-173">[![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)</span></span>

3.  <span data-ttu-id="8290b-174">Свяжите приложения Azure Active Directory с пользователем складского приложения.</span><span class="sxs-lookup"><span data-stu-id="8290b-174">Associate your Azure Active Directory application with the warehousing app user.</span></span>
    1.  <span data-ttu-id="8290b-175">В Finance and Operations перейдите к **Администрирование системы** &gt; **Настройка** &gt; **Приложения Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="8290b-175">In Finance and Operations, go to **System administration** &gt; **Setup** &gt; **Azure Active Directory applications**.</span></span>
    2.  <span data-ttu-id="8290b-176">Создайте новую строку.</span><span class="sxs-lookup"><span data-stu-id="8290b-176">Create a new line.</span></span>
    3.  <span data-ttu-id="8290b-177">Введите **Код клиента** (полученный в предыдущем разделе), присвойте ему имя, затем выберите ранее созданного пользователя.</span><span class="sxs-lookup"><span data-stu-id="8290b-177">Enter the **Client ID** (obtained in the last section), give it a name, and select the previously created user.</span></span> <span data-ttu-id="8290b-178">Рекомендуется пометить все устройства, чтобы можно было легко удалять их доступ к Finance and Operations, с этой страницы в случае, если они будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="8290b-178">We recommend that you tag all your devices so that you can easily remove their access to Finance and Operations from this page in case they are lost.</span></span> <span data-ttu-id="8290b-179">[![wh-10-форма-приложений-ad](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-179">[![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)</span></span>

## <a name="configure-the-application"></a><span data-ttu-id="8290b-180">Настройка приложения</span><span class="sxs-lookup"><span data-stu-id="8290b-180">Configure the application</span></span>
<span data-ttu-id="8290b-181">Необходимо настроить приложение на устройстве для подключения к серверу Finance and Operations через приложение Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8290b-181">You must configure the app on the device to connect to the Finance and Operations server through the Azure AD application.</span></span> <span data-ttu-id="8290b-182">Для этого необходимо выполнить следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="8290b-182">To do this, complete the following steps.</span></span>

1.  <span data-ttu-id="8290b-183">В приложении перейдите к пункту **Параметры подключения**.</span><span class="sxs-lookup"><span data-stu-id="8290b-183">In the app, go to **Connection settings**.</span></span>
2.  <span data-ttu-id="8290b-184">Очистите поле **Демонстрационный режим**.</span><span class="sxs-lookup"><span data-stu-id="8290b-184">Clear the **Demo mode** field.</span></span> <br><span data-ttu-id="8290b-185">[![wh-11-демо-режим-в-настройках-подключения-приложения](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-185">[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)</span></span>
3.  <span data-ttu-id="8290b-186">Введите следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="8290b-186">Enter the following information:</span></span> 
    + <span data-ttu-id="8290b-187">**Код клиента Azure Active Directory** — код клиента, который получен на шаге 13 в разделе "Создание приложения веб-службы в Active Directory".</span><span class="sxs-lookup"><span data-stu-id="8290b-187">**Azure Active directory client ID** - The client ID is obtained in step 13 in "Create a web service application in Active Directory".</span></span> 
    + <span data-ttu-id="8290b-188">**Секрет клиента Azure Active Directory** — секрет клиента, который получен на шаге 13 в разделе "Создание приложения веб-службы в Active Directory".</span><span class="sxs-lookup"><span data-stu-id="8290b-188">**Azure Active directory client secret** - The client secret is obtained in step 13 in "Create a web service application in Active Directory".</span></span> 
    + <span data-ttu-id="8290b-189">**Ресурс Azure Active Directory** — ресурс Azure AD Directory описывает корневой URL-адрес Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8290b-189">**Azure Active directory resource** - The Azure AD directory resource depicts the Finance and Operations root URL.</span></span> <span data-ttu-id="8290b-190">**Примечание**. Не завершайте это поле символом прямой косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="8290b-190">**Note**: Do not end this field with a forward slash character (/).</span></span> 
    + <span data-ttu-id="8290b-191">**Владелец Azure Active Directory** – владелец Azure AD Directory, используемый с сервером Finance and Operations: https://login.windows.net/код-вашего-владельца-AD.</span><span class="sxs-lookup"><span data-stu-id="8290b-191">**Azure Active directory tenant** - The Azure AD directory tenant used with the Finance and Operations server: https://login.windows.net/your-AD-tenant-ID.</span></span> <span data-ttu-id="8290b-192">Например: https://login.windows.net/contosooperations.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="8290b-192">For example: https://login.windows.net/contosooperations.onmicrosoft.com.</span></span>
    <br><span data-ttu-id="8290b-193">**Примечание**. Не завершайте это поле символом прямой косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="8290b-193">**Note**: Do not end this field with a forward slash character (/).</span></span> 
    + <span data-ttu-id="8290b-194">**Компания** — введите юридическое лицо в Finance and Operations, к которому должно подключаться приложение.</span><span class="sxs-lookup"><span data-stu-id="8290b-194">**Company** - Enter the legal entity in Finance and Operations to which you want the application to connect.</span></span> <br><span data-ttu-id="8290b-195">[![wh-12-настройки-подключения-приложения](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-195">[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)</span></span>
4.  <span data-ttu-id="8290b-196">Нажмите кнопку **Назад** в левом верхнем углу приложения.</span><span class="sxs-lookup"><span data-stu-id="8290b-196">Select the **Back** button in the top-left corner of the application.</span></span> <span data-ttu-id="8290b-197">Теперь приложение подключится к серверу Finance and Operations, и на дисплее появится экран входа для работника склада.</span><span class="sxs-lookup"><span data-stu-id="8290b-197">The application will now connect to your Finance and Operations server and the log-in screen for the warehouse worker will display.</span></span> <br><span data-ttu-id="8290b-198">[![wh-13-экран-входа](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)</span><span class="sxs-lookup"><span data-stu-id="8290b-198">[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)</span></span>

## <a name="remove-access-for-a-device"></a><span data-ttu-id="8290b-199">Удаление доступа для устройства</span><span class="sxs-lookup"><span data-stu-id="8290b-199">Remove access for a device</span></span>
<span data-ttu-id="8290b-200">Если устройство было потеряно или взломано, необходимо удалить доступ к Finance and Operations для устройства.</span><span class="sxs-lookup"><span data-stu-id="8290b-200">In case of a lost or compromised device, you must remove access to Finance and Operations for the device.</span></span> <span data-ttu-id="8290b-201">Следующие шаги описывают рекомендуемый процесс удаления доступа.</span><span class="sxs-lookup"><span data-stu-id="8290b-201">The following steps describe the recommended process to remove access.</span></span>

1.  <span data-ttu-id="8290b-202">В Finance and Operations перейдите к **Администрирование системы** &gt; **Настройка** &gt; **Приложения Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="8290b-202">In Finance and Operations, go to **System administration** &gt; **Setup** &gt; **Azure Active Directory applications**.</span></span>
2.  <span data-ttu-id="8290b-203">Удалите строку, которая соответствует устройству, для которого необходимо удалить доступ.</span><span class="sxs-lookup"><span data-stu-id="8290b-203">Delete the line that corresponds to the device to which you want to remove access.</span></span> <span data-ttu-id="8290b-204">Запишите **Код клиента**, используемый для удаленного устройства.</span><span class="sxs-lookup"><span data-stu-id="8290b-204">Note down the **Client ID** used for the removed device.</span></span>
3.  <span data-ttu-id="8290b-205">Войдите на классический портал Azure по адресу <https://manage.windowsazure.com>.</span><span class="sxs-lookup"><span data-stu-id="8290b-205">Sign in the Azure classic portal at <https://manage.windowsazure.com>.</span></span>
4.  <span data-ttu-id="8290b-206">Щелкните значок **Active Directory** в левом меню, затем щелкните нужный каталог.</span><span class="sxs-lookup"><span data-stu-id="8290b-206">Click the **Active Directory** icon on the left menu, and then click the desired directory.</span></span>
5.  <span data-ttu-id="8290b-207">В верхнем меню щелкните **Приложения**, затем щелкните приложение, которое требуется настроить.</span><span class="sxs-lookup"><span data-stu-id="8290b-207">On the top menu, click **Applications**, and then click the application you want to configure.</span></span> <span data-ttu-id="8290b-208">Откроется страница **Быстрый запуск** с единым входом и другими сведениями о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8290b-208">The **Quick Start** page will appear with single sign-on and other configuration information.</span></span>
6.  <span data-ttu-id="8290b-209">Щелкните вкладку **Конфигурация**, прокрутите экран вниз и убедитесь, что **Код клиента** приложения совпадает с указанным на шаге 2 в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="8290b-209">Click the **Configure** tab, scroll down and ensure that the **Client ID** of the application is the same as in step 2 in this section.</span></span>
7.  <span data-ttu-id="8290b-210">Щелкните кнопку **Удалить** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="8290b-210">Click the **Delete** button in the command bar.</span></span>
8.  <span data-ttu-id="8290b-211">Нажмите **Да** в сообщение с запросом подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8290b-211">Click **Yes** in the confirmation message.</span></span>




