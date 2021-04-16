---
title: Включение интеграции Dynamics 365 Commerce и Microsoft Teams
description: В этом разделе описывается, как включить интеграцию Microsoft Dynamics 365 Commerce и Microsoft Teams.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842731"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="db78e-103">Включение интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="db78e-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="db78e-104">В этом разделе описывается, как включить интеграцию Microsoft Dynamics 365 Commerce и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="db78e-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="db78e-105">Чтобы подготовить в Teams сведения из Dynamics 365 Commerce и синхронизировать функции управления задачами между Teams и приложением POS-терминала, необходимо включить функции интеграции в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="db78e-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="db78e-106">При включении интеграции Teams вы соглашаетесь с предоставлением общего доступа к данным с Teams.</span><span class="sxs-lookup"><span data-stu-id="db78e-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="db78e-107">Данные, которые совместно используются с Teams, могут находиться не в той стране, в которой находятся ваши данные Commerce, и к ним могут применяться другие стандарты соответствия нормативам.</span><span class="sxs-lookup"><span data-stu-id="db78e-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="db78e-108">Дополнительные сведения см. в [Центре управления безопасностью Майкрософт](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="db78e-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="db78e-109">Сведения о политиках конфиденциальности корпорации Майкрософт см. в [заявлении о конфиденциальности Майкрософт](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="db78e-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="db78e-110">Включение интеграции Teams</span><span class="sxs-lookup"><span data-stu-id="db78e-110">Enable Teams integration</span></span>

<span data-ttu-id="db78e-111">Прежде чем можно будет включить интеграцию Microsoft Teams с Commerce, необходимо зарегистрировать приложение Teams с вашим клиентом на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="db78e-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="db78e-112">Чтобы зарегистрировать приложение Teams с вашим клиентом на портале Azure, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="db78e-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="db78e-113">Следуйте указаниям из раздела [Краткое руководство: регистрация приложения на платформе удостоверений Майкрософт](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app), чтобы зарегистрировать приложение Teams с вашим клиентом на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="db78e-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="db78e-114">Скопируйте значение **ИД приложения (клиента)** со страницы **Обзор** для зарегистрированного приложения.</span><span class="sxs-lookup"><span data-stu-id="db78e-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="db78e-115">Это значение будет использоваться, чтобы включить интеграцию Teams в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="db78e-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="db78e-116">Скопируйте значение сертификата, которое был введено при [добавлении сертификата](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="db78e-116">Copy the certificate value that was entered when you [added a certificate](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="db78e-117">Этот сертификат называется также открытым ключом или ключом приложения.</span><span class="sxs-lookup"><span data-stu-id="db78e-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="db78e-118">Это значение будет использоваться, чтобы включить интеграцию Teams в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="db78e-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="db78e-119">Чтобы включить интеграцию Teams в Commerce Headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="db78e-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="db78e-120">Выберите **Retail и Commerce \> Настройка канала \> Конфигурация интеграции Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="db78e-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="db78e-121">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="db78e-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="db78e-122">Для параметра **Включить интеграцию Microsoft Teams** задайте значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="db78e-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="db78e-123">В полях **Код приложения** и **Ключ приложения** введите значения, полученные при регистрации приложения Teams на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="db78e-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="db78e-124">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="db78e-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="db78e-125">На следующем рисунке показан пример настройки интеграции Teams в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="db78e-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Настройка интеграции Teams в Commerce Headquarters](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="db78e-127">Отключение интеграции Teams</span><span class="sxs-lookup"><span data-stu-id="db78e-127">Disable Teams integration</span></span>

<span data-ttu-id="db78e-128">Чтобы отключить интеграцию Microsoft Teams в Commerce Headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="db78e-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="db78e-129">Выберите **Retail и Commerce \> Настройка канала \> Конфигурация интеграции Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="db78e-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="db78e-130">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="db78e-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="db78e-131">Для параметра **Включить интеграцию Microsoft Teams** задайте значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="db78e-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="db78e-132">Удалите значения из полей **Код приложения** и **Ключ приложения**.</span><span class="sxs-lookup"><span data-stu-id="db78e-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="db78e-133">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="db78e-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="db78e-134">После отключения интеграции Teams с Commerce POS-терминалы больше не будут показывать задачи, опубликованные из приложения Teams.</span><span class="sxs-lookup"><span data-stu-id="db78e-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db78e-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="db78e-135">Additional resources</span></span>

[<span data-ttu-id="db78e-136">Обзор интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="db78e-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="db78e-137">Подготовка Microsoft Teams из Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="db78e-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="db78e-138">Синхронизация управления задачами между Microsoft Teams и Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="db78e-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="db78e-139">Управление ролями пользователей в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="db78e-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="db78e-140">Сопоставление магазинов и рабочих групп, если имеются готовые рабочие группы в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="db78e-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="db78e-141">Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="db78e-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
