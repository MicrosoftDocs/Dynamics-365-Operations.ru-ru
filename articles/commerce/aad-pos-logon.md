---
title: Включение проверки подлинности Azure Active Directory для входа в POS-терминал
description: В этой теме объясняется, как настроить взаимодействие входа в систему для POS-терминала Microsoft Dynamics 365 Commerce, чтобы использовать проверку подлинности Azure Active Directory.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 234d19bb6659af07c65763e05671742b9581e244
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206687"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="f9f6a-103">Включение проверки подлинности Azure Active Directory для входа на POS-терминал</span><span class="sxs-lookup"><span data-stu-id="f9f6a-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="f9f6a-104">Многие клиенты, использующие Microsoft Dynamics 365 Commerce, также используют другие облачные службы Microsoft, и могут использовать Azure Active Directory (Azure AD) для управления учетными данными пользователей для этих служб.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="f9f6a-105">В этих случаях клиенты могут захотеть использовать одну и ту же учетную запись Azure AD в разных приложениях.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="f9f6a-106">В этой теме объясняется, как настроить взаимодействие входа в систему для POS-терминала Commerce, чтобы использовать проверку подлинности Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="f9f6a-107">Настройка проверки подлинности Azure AD</span><span class="sxs-lookup"><span data-stu-id="f9f6a-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="f9f6a-108">Чтобы сделать Azure AD доступным в качестве метода проверки подлинности для входа в POS-терминал в магазине, необходимо настроить параметры профиля функциональности магазина, затем применить эти настройки к POS-клиентам.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="f9f6a-109">Чтобы настроить профиль функциональности, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="f9f6a-110">Перейдите в раздел **Retail и Commerce** \> **Настройка канала** \> **Настройка POS** \> **Профили POS** \> **Профили функциональности**.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="f9f6a-111">Выберите профиль функциональности для изменения.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="f9f6a-112">На экспресс-вкладке **Функции** в разделе **Вход в POS для персонала** измените значение поля **Метод проверки подлинности при входе** с **Код персонала и пароль** на **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="f9f6a-113">По умолчанию все профили функциональности используют **Идентификатор персонала и пароль** в качестве метода проверки подлинности для POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="f9f6a-114">Поэтому необходимо изменить значение поля **Метод проверки подлинности при входе**, если необходимо использовать Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="f9f6a-115">Данное изменение повлияет на все розничные магазины, связанные с выбранным профилем функциональности.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="f9f6a-116">Чтобы применить настройки к клиентам POS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="f9f6a-117">Перейдите в раздел **Retail и Commerce** \> **ИТ Retail и Commerce** \> **График распределения**.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="f9f6a-118">Запустите график распределения **1070** (**Конфигурация канала**).</span><span class="sxs-lookup"><span data-stu-id="f9f6a-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="f9f6a-119">Для проверки подлинности Azure AD требуется подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="f9f6a-120">Она не работает, когда POS-терминал работает в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="f9f6a-121">В настоящее время функция **Переопределение менеджера** не поддерживает Azure AD как метод аутентификации.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="f9f6a-122">Код оператора и пароль требуются, даже если Azure AD настроен в качестве метода аутентификации для входа в POS-терминал.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="f9f6a-123">Связывание учетной записи Azure AD с работником</span><span class="sxs-lookup"><span data-stu-id="f9f6a-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="f9f6a-124">Прежде чем работник магазина сможет использовать учетную запись Azure AD для входа в приложение POS, эта учетная запись Azure AD должна быть связана с этим сотрудником.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="f9f6a-125">Чтобы связать учетную запись Azure AD с работником, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="f9f6a-126">Перейдите в раздел **Retail и Commerce** \> **Сотрудники** \> **Работники**.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="f9f6a-127">Откройте страницу сведений о работнике.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="f9f6a-128">В область действий на вкладке **Commerce** в группе **Внешнее удостоверение** выберите **Связать существующее удостоверение**.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="f9f6a-129">В диалоговом окне **Использовать существующее внешнее удостоверение** выберите **Поиск по электронной почте**, введите адрес электронной почты Azure AD, затем выберите **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="f9f6a-130">Выберите возвращенную учетную запись Azure AD, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="f9f6a-131">Будут заполнены поля **Псевдоним**, **UPN** и **Внешний подкод** на вкладке **Commerce** на странице сведений о работнике.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="f9f6a-132">После обновления записи работника, например, если связана новая учетная запись Azure AD, изменяется пароль или адресная книга сотрудника обновляется, рекомендуется использовать план распределения **1060** (**Персонал**), чтобы синхронизировать последние сведения о персонале с каналом.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="f9f6a-133">Таким образом, приложение POS может выбрать правильные данные для аутентификации пользователя и авторизации.</span><span class="sxs-lookup"><span data-stu-id="f9f6a-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9f6a-134">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f9f6a-134">Additional resources</span></span>

[<span data-ttu-id="f9f6a-135">Настройка функциональности расширенного входа для MPOS и Cloud POS</span><span class="sxs-lookup"><span data-stu-id="f9f6a-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="f9f6a-136">Создание профиля функциональности розничной торговли</span><span class="sxs-lookup"><span data-stu-id="f9f6a-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="f9f6a-137">Настройка работника</span><span class="sxs-lookup"><span data-stu-id="f9f6a-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)


[!INCLUDE[footer-include](../includes/footer-banner.md)]