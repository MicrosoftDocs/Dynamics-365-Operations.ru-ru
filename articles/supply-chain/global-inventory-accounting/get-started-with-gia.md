---
title: Начало глобального учета запасов
description: В этой теме описывается, как начать работу с глобальным учетом запасов.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301706"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="ee649-103">Начало глобального учета запасов</span><span class="sxs-lookup"><span data-stu-id="ee649-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="ee649-104">Глобальный учет запасов позволяет выполнить несколько учетов запасов в настроенных книгах глобального учета запасов.</span><span class="sxs-lookup"><span data-stu-id="ee649-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="ee649-105">Каждую книгу глобального учета запасов следует связать с *соглашением*.</span><span class="sxs-lookup"><span data-stu-id="ee649-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="ee649-106">Соглашение — это совокупность следующих типов политик учета:</span><span class="sxs-lookup"><span data-stu-id="ee649-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="ee649-107">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="ee649-107">Cost object</span></span>
- <span data-ttu-id="ee649-108">Базис входящих измерений</span><span class="sxs-lookup"><span data-stu-id="ee649-108">Input measurement basis</span></span>
- <span data-ttu-id="ee649-109">Предположение потока затрат</span><span class="sxs-lookup"><span data-stu-id="ee649-109">Cost flow assumption</span></span>
- <span data-ttu-id="ee649-110">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="ee649-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="ee649-111">Даже после включения глобального учета запасов можно по-прежнему выполнить учет запасов в Microsoft Dynamics 365 Supply Chain Management, как обычно.</span><span class="sxs-lookup"><span data-stu-id="ee649-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="ee649-112">Глобальный учет запасов является надстройкой.</span><span class="sxs-lookup"><span data-stu-id="ee649-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="ee649-113">Чтобы сделать ее функции доступными, необходимо установить ее из Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ee649-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ee649-114">Ее можно оценить в тестовой среде, прежде чем включать ее в производственной среде.</span><span class="sxs-lookup"><span data-stu-id="ee649-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="ee649-115">Глобальный учет запасов в настоящее время не поддерживает все функции управления затратами, встроенные в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ee649-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="ee649-116">Таким образом, важно оценить, будет ли набор функций, доступный в данный момент, удовлетворять вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="ee649-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="ee649-117">Как получить общедоступную предварительную версию глобального учета запасов</span><span class="sxs-lookup"><span data-stu-id="ee649-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee649-118">Для использования глобального учета запасов необходимо иметь среду с поддержкой LCS с высокой доступностью (не среду OneBox).</span><span class="sxs-lookup"><span data-stu-id="ee649-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="ee649-119">Кроме того, используется Supply Chain Management версии 10.0.19 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ee649-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="ee649-120">Чтобы зарегистрироваться на общедоступную предварительную версию глобального учета запасов, отправьте ваш код среды LCS по электронной почте [рабочей группе глобального учета запасов](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ee649-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="ee649-121">После утверждения программы рабочая группа отправит вам сообщение электронной почты с ключом бета-версии глобального учета данных и конечными точками служб.</span><span class="sxs-lookup"><span data-stu-id="ee649-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="ee649-122">После получения ключа бета-версии можно [установить надстройку](#install).</span><span class="sxs-lookup"><span data-stu-id="ee649-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="ee649-123">Лицензирование</span><span class="sxs-lookup"><span data-stu-id="ee649-123">Licensing</span></span>

<span data-ttu-id="ee649-124">Глобальный учет запасов лицензируется вместе со стандартными функциями учета запасов, которые доступны для Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ee649-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="ee649-125">Вам не придется покупать дополнительную лицензию для использования глобального учета запасов.</span><span class="sxs-lookup"><span data-stu-id="ee649-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ee649-126">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="ee649-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="ee649-127">Настройка интеграции Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="ee649-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="ee649-128">Перед включением функций надстройки необходимо выполнить интегрирование с Microsoft Power Platform, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ee649-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="ee649-129">Откройте среду LCS, в которую необходимо добавить службу.</span><span class="sxs-lookup"><span data-stu-id="ee649-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="ee649-130">Перейдите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="ee649-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="ee649-131">В разделе **Интеграция Power Platform** выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="ee649-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="ee649-132">В диалоговом окне **Настройка среды Power Platform** установите флажок, а затем выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="ee649-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="ee649-133">Обычно программа установки занимает от 60 до 90 минут.</span><span class="sxs-lookup"><span data-stu-id="ee649-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="ee649-134">После завершения настройки среды Microsoft Power Platform страница отобразит название среды.</span><span class="sxs-lookup"><span data-stu-id="ee649-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="ee649-135">Кроме того, в разделе **Интеграция Power Platform** отображается сообщение "Настройка среды Power Platform завершена".</span><span class="sxs-lookup"><span data-stu-id="ee649-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="ee649-136">Для глобального учета запасов не требуется приложение с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="ee649-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="ee649-137">Дополнительные сведения см. в разделе [Настройка после развертывания среды](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="ee649-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="ee649-138">Настройка Dataverse</span><span class="sxs-lookup"><span data-stu-id="ee649-138">Set up Dataverse</span></span>

<span data-ttu-id="ee649-139">Перед настройкой Dataverse добавьте в свой клиент принципы служб глобального учета запасов, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ee649-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="ee649-140">Установите модуль Azure AD для Windows PowerShell v2, как описано в подразделе [Установка Azure Active Directory PowerShell для Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="ee649-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="ee649-141">Выполните следующую команду PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ee649-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="ee649-142">Затем создайте пользователей приложения для глобального учета запасов в Dataverse в соответствии с приведенными ниже указаниями.</span><span class="sxs-lookup"><span data-stu-id="ee649-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="ee649-143">Откройте URL-адрес своей среды Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ee649-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="ee649-144">Перейдите **Дополнительные параметры \> Система \> Безопасность \> Пользователи** и создайте пользователя приложения.</span><span class="sxs-lookup"><span data-stu-id="ee649-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="ee649-145">Используйте поле **Вид** для изменения вида страницы на *Пользователи приложения*.</span><span class="sxs-lookup"><span data-stu-id="ee649-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="ee649-146">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ee649-146">Select **New**.</span></span>
1. <span data-ttu-id="ee649-147">Задайте в поле **Код приложения** значение *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span><span class="sxs-lookup"><span data-stu-id="ee649-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="ee649-148">Выберите **Назначить роль**, а затем выберите *Системный администратор*.</span><span class="sxs-lookup"><span data-stu-id="ee649-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="ee649-149">Если имеется роль с именем *Пользователь Common Data Service*, выберите ее.</span><span class="sxs-lookup"><span data-stu-id="ee649-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="ee649-150">Повторите описанные выше шаги, но задайте для поля **Код приложения** значение *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span><span class="sxs-lookup"><span data-stu-id="ee649-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="ee649-151">Дополнительные сведения см. в разделе [Создание пользователя приложения](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="ee649-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="ee649-152">Если установленный по умолчанию язык Dataverse не является английским, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ee649-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="ee649-153">Переход к **Дополнительные параметры \> Администрирование \> Языки**.</span><span class="sxs-lookup"><span data-stu-id="ee649-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="ee649-154">Выберите *Английский* (*LanguageCode=1033*) и затем выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="ee649-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="ee649-155">Установка надстройки</span><span class="sxs-lookup"><span data-stu-id="ee649-155">Install the add-in</span></span>

<span data-ttu-id="ee649-156">Выполните следующие действия, чтобы установить надстройку, чтобы можно было использовать глобальный учет запасов.</span><span class="sxs-lookup"><span data-stu-id="ee649-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="ee649-157">[Зарегистрируйтесь](#sign-up), чтобы получить общедоступную предварительную версию глобального учета запасов.</span><span class="sxs-lookup"><span data-stu-id="ee649-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="ee649-158">Войдите в [LCS](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="ee649-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="ee649-159">Перейдите к разделу **Управление компонентами предварительной версии**.</span><span class="sxs-lookup"><span data-stu-id="ee649-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="ee649-160">Выберите знак "плюс (**+**).</span><span class="sxs-lookup"><span data-stu-id="ee649-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="ee649-161">В поле **Код** введите свой дополнительный ключ бета-тестера для глобального учета запасов.</span><span class="sxs-lookup"><span data-stu-id="ee649-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="ee649-162">(Вы должны получить свой ключ бета-версии по электронной почте, когда вы зарегистрировались.)</span><span class="sxs-lookup"><span data-stu-id="ee649-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="ee649-163">Выберите **Разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="ee649-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="ee649-164">Откройте среду LCS, в которую необходимо добавить службу.</span><span class="sxs-lookup"><span data-stu-id="ee649-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="ee649-165">Перейдите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="ee649-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="ee649-166">Перейдите в раздел **Интеграция Power Platform** и выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="ee649-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="ee649-167">В диалоговом окне **Настройка среды Power Platform** установите флажок, а затем выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="ee649-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="ee649-168">Обычно программа установки занимает от 60 до 90 минут.</span><span class="sxs-lookup"><span data-stu-id="ee649-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="ee649-169">После завершения настройки среды Microsoft Power Platform на экспресс-вкладке **Надстройки среды** выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="ee649-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="ee649-170">Выберите **Глобальный учет запасов**.</span><span class="sxs-lookup"><span data-stu-id="ee649-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="ee649-171">Следуйте указаниям руководства по установке и примите условия и положения.</span><span class="sxs-lookup"><span data-stu-id="ee649-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="ee649-172">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="ee649-172">Select **Install**.</span></span>
1. <span data-ttu-id="ee649-173">На экспресс-вкладке **Надстройки среды** должно быть видно, что устанавливается глобальный учет запасов.</span><span class="sxs-lookup"><span data-stu-id="ee649-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="ee649-174">Через несколько минут этот статус должен измениться с *Устанавливается* на *Установлено*.</span><span class="sxs-lookup"><span data-stu-id="ee649-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="ee649-175">(Возможно, потребуется обновить страницу, чтобы увидеть это изменение.) На этом этапе глобальный учет запасов готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="ee649-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="ee649-176">Настройка интеграции</span><span class="sxs-lookup"><span data-stu-id="ee649-176">Set up the integration</span></span>

<span data-ttu-id="ee649-177">Выполните следующие действия, чтобы настроить интеграцию между глобальным учетом запасов и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ee649-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="ee649-178">Войдите в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ee649-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="ee649-179">Перейдите в раздел **Администрирование системы \> Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="ee649-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="ee649-180">Выберите **Проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="ee649-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="ee649-181">На вкладке **Все** выполните поиск функции с именем *Глобальный учет запасов*.</span><span class="sxs-lookup"><span data-stu-id="ee649-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="ee649-182">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="ee649-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="ee649-183">Перейдите к **Глобальный учет запасов \> Настройка \> Параметры глобального учета запасов \> Параметры интеграции**.</span><span class="sxs-lookup"><span data-stu-id="ee649-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="ee649-184">В полях **Конечная точка службы данных** и **Конечная точка глобального учета запасов** введите URL-адреса из электронного письма, отправленного рабочей группой глобального учета запасов при регистрации на предварительную версию.</span><span class="sxs-lookup"><span data-stu-id="ee649-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="ee649-185">Теперь глобальный учет запасов готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="ee649-185">Global Inventory Accounting is now ready to use.</span></span>
