---
title: Включение проверки подлинности Azure Active Directory для входа в POS-терминал
description: В этой теме объясняется, как настроить взаимодействие входа в систему для POS-терминала Microsoft Dynamics 365 Commerce, чтобы использовать проверку подлинности Azure Active Directory.
author: boycezhu
manager: annbe
ms.date: 03/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: f030e8382627191dd32d855e15432fc85dca4bbd
ms.sourcegitcommit: 1789a78de1cbeac19d96767812df653a191c67e9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "3100388"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="e96cd-103">Включение проверки подлинности Azure Active Directory для входа в POS-терминал</span><span class="sxs-lookup"><span data-stu-id="e96cd-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e96cd-104">Многие клиенты, использующие Microsoft Dynamics 365 Commerce, также используют другие облачные службы Microsoft, и могут использовать Azure Active Directory (Azure AD) для управления учетными данными пользователей для этих служб.</span><span class="sxs-lookup"><span data-stu-id="e96cd-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="e96cd-105">В этих случаях клиенты могут захотеть использовать одну и ту же учетную запись Azure AD в разных приложениях.</span><span class="sxs-lookup"><span data-stu-id="e96cd-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="e96cd-106">В этой теме объясняется, как настроить взаимодействие входа в систему для POS-терминала Commerce, чтобы использовать проверку подлинности Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e96cd-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="e96cd-107">Настройка проверки подлинности Azure AD</span><span class="sxs-lookup"><span data-stu-id="e96cd-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="e96cd-108">Чтобы сделать Azure AD доступным в качестве метода проверки подлинности для входа в POS-терминал в магазине, необходимо настроить параметры профиля функциональности магазина, затем применить эти настройки к POS-клиентам.</span><span class="sxs-lookup"><span data-stu-id="e96cd-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="e96cd-109">Чтобы настроить профиль функциональности, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e96cd-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="e96cd-110">Перейдите в раздел **Retail и Commerce** \> **Настройка канала** \> **Настройка POS** \> **Профили POS** \> **Профили функциональности**.</span><span class="sxs-lookup"><span data-stu-id="e96cd-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="e96cd-111">Выберите профиль функциональности для изменения.</span><span class="sxs-lookup"><span data-stu-id="e96cd-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="e96cd-112">На экспресс-вкладке **Функции** в разделе **Вход в POS для персонала** измените значение поля **Метод проверки подлинности при входе** с **Код персонала и пароль** на **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="e96cd-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="e96cd-113">По умолчанию все профили функциональности используют **Идентификатор персонала и пароль** в качестве метода проверки подлинности для POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="e96cd-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="e96cd-114">Поэтому необходимо изменить значение поля **Метод проверки подлинности при входе**, если необходимо использовать Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e96cd-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="e96cd-115">Данное изменение повлияет на все розничные магазины, связанные с выбранным профилем функциональности.</span><span class="sxs-lookup"><span data-stu-id="e96cd-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="e96cd-116">Чтобы применить настройки к клиентам POS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e96cd-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="e96cd-117">Перейдите в раздел **Retail и Commerce** \> **ИТ Retail и Commerce** \> **График распределения**.</span><span class="sxs-lookup"><span data-stu-id="e96cd-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="e96cd-118">Запустите график распределения **1070** (**Конфигурация канала**).</span><span class="sxs-lookup"><span data-stu-id="e96cd-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="e96cd-119">Для проверки подлинности Azure AD требуется подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="e96cd-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="e96cd-120">Она не работает, когда POS-терминал работает в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="e96cd-120">It won't work when POS is in offline mode.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="e96cd-121">Связывание учетной записи Azure AD с работником</span><span class="sxs-lookup"><span data-stu-id="e96cd-121">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="e96cd-122">Прежде чем работник магазина сможет использовать учетную запись Azure AD для входа в приложение POS, эта учетная запись Azure AD должна быть связана с этим сотрудником.</span><span class="sxs-lookup"><span data-stu-id="e96cd-122">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="e96cd-123">Чтобы связать учетную запись Azure AD с работником, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e96cd-123">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="e96cd-124">Перейдите в раздел **Retail и Commerce** \> **Сотрудники** \> **Работники**.</span><span class="sxs-lookup"><span data-stu-id="e96cd-124">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="e96cd-125">Откройте страницу сведений о работнике.</span><span class="sxs-lookup"><span data-stu-id="e96cd-125">Open the details page for a worker.</span></span>
1. <span data-ttu-id="e96cd-126">В область действий на вкладке **Commerce** в группе **Внешнее удостоверение** выберите **Связать существующее удостоверение**.</span><span class="sxs-lookup"><span data-stu-id="e96cd-126">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="e96cd-127">В диалоговом окне **Использовать существующее внешнее удостоверение** выберите **Поиск по электронной почте**, введите адрес электронной почты Azure AD, затем выберите **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="e96cd-127">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="e96cd-128">Выберите возвращенную учетную запись Azure AD, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e96cd-128">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="e96cd-129">Будут заполнены поля **Псевдоним**, **UPN** и **Внешний подкод** на вкладке **Commerce** на странице сведений о работнике.</span><span class="sxs-lookup"><span data-stu-id="e96cd-129">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e96cd-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e96cd-130">Additional resources</span></span>

[<span data-ttu-id="e96cd-131">Настройка функциональности расширенного входа для MPOS и Cloud POS</span><span class="sxs-lookup"><span data-stu-id="e96cd-131">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="e96cd-132">Создание профиля функциональности розничной торговли</span><span class="sxs-lookup"><span data-stu-id="e96cd-132">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="e96cd-133">Настройка работника</span><span class="sxs-lookup"><span data-stu-id="e96cd-133">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
