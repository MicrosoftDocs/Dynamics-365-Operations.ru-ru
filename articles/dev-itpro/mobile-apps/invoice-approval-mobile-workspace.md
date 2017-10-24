---
title: "Мобильная рабочая область \"Утверждения накладных\""
description: "В этом разделе содержится информация о мобильной рабочей области утверждения накладных. Эта рабочая область содержит список накладных, которые были назначены вам через процесс workflow-процесса заголовка накладной поставщика."
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: 190f48f4d5e304902b701f74f2cbefcbe7b36b15
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="9e162-104">Мобильная рабочая область "Утверждения накладных"</span><span class="sxs-lookup"><span data-stu-id="9e162-104">Invoice approvals mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9e162-105">В этом разделе содержится информация о мобильной рабочей области **Утверждения накладных**.</span><span class="sxs-lookup"><span data-stu-id="9e162-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="9e162-106">Эта рабочая область содержит список накладных, которые были назначены вам через процесс workflow-процесса заголовка накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="9e162-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="9e162-107">Эту мобильную рабочую область можно использовать с мобильным приложением Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="9e162-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="9e162-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="9e162-108">Overview</span></span>

<span data-ttu-id="9e162-109">Мобильная рабочая область **Утверждения накладных** позволяет служащим и менеджерам по расчетам с поставщиками просматривать накладные, которые были назначены им как часть workflow-процесса заголовка накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="9e162-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="9e162-110">Можно просмотреть сведения о накладной и даже строку и сведения распределения, чтобы принять обоснованные решения.</span><span class="sxs-lookup"><span data-stu-id="9e162-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="9e162-111">Из рабочей области можно было предпринять действие, чтобы переместить накладную по workflow-процессу.</span><span class="sxs-lookup"><span data-stu-id="9e162-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="9e162-112">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="9e162-112">Prerequisites</span></span>

<span data-ttu-id="9e162-113">Перед использованием этой мобильной рабочей области должны быть выполнены следующие предварительные условия.</span><span class="sxs-lookup"><span data-stu-id="9e162-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9e162-114">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="9e162-114">Prerequisite</span></span></th>
<th><span data-ttu-id="9e162-115">Роль</span><span class="sxs-lookup"><span data-stu-id="9e162-115">Role</span></span></th>
<th><span data-ttu-id="9e162-116">описание</span><span class="sxs-lookup"><span data-stu-id="9e162-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9e162-117">В организации должна быть развернута система Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.).</span><span class="sxs-lookup"><span data-stu-id="9e162-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="9e162-118">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="9e162-118">System administrator</span></span></td>
<td><span data-ttu-id="9e162-119">См. <a href="../deployment/deploy-demo-environment.md">Развертывание демонстрационной среды</a>.</span><span class="sxs-lookup"><span data-stu-id="9e162-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9e162-120">Мобильная рабочая область <strong>Утверждения накладных</strong> должна быть публикована.</span><span class="sxs-lookup"><span data-stu-id="9e162-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="9e162-121">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="9e162-121">System administrator</span></span></td>
<td><span data-ttu-id="9e162-122">См. <a href="publish-mobile-workspace.md">Публикация мобильной рабочей области</a>.</span><span class="sxs-lookup"><span data-stu-id="9e162-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="9e162-123">Загрузите и установите мобильное приложение</span><span class="sxs-lookup"><span data-stu-id="9e162-123">Download and install the mobile app</span></span>

<span data-ttu-id="9e162-124">Загрузите и установите мобильное приложение Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="9e162-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="9e162-125">Для ОС Android</span><span class="sxs-lookup"><span data-stu-id="9e162-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="9e162-126">Для iPhone</span><span class="sxs-lookup"><span data-stu-id="9e162-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="9e162-127">Войдите в систему в мобильном приложении</span><span class="sxs-lookup"><span data-stu-id="9e162-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="9e162-128">Запустите приложение на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="9e162-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="9e162-129">Введите URL-адрес Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9e162-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="9e162-130">При первом входе появится запрос имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="9e162-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="9e162-131">Введите свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="9e162-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="9e162-132">После входа будут показаны доступные рабочие области для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="9e162-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="9e162-133">Обратите внимание, что если позже системный администратор опубликует новую рабочую область, вам потребуется обновить список мобильных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="9e162-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="9e162-134">[![Потянуть для обновления](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="9e162-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="9e162-135">Утверждение накладных с помощью мобильной рабочей области утверждения накладных</span><span class="sxs-lookup"><span data-stu-id="9e162-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="9e162-136">На мобильном устройстве выберите рабочую область **Утверждения накладных**.</span><span class="sxs-lookup"><span data-stu-id="9e162-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="9e162-137">Выберите накладную, которая была назначена вам workflow-процессом заголовка накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="9e162-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="9e162-138">На странице **Сведения о накладной** изучите сведения заголовка накладной, например сведения о поставщике и дате.</span><span class="sxs-lookup"><span data-stu-id="9e162-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="9e162-139">Выберите строку накладной для просмотра более подробных сведений о ней в представлении **Сведения строки накладной**.</span><span class="sxs-lookup"><span data-stu-id="9e162-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="9e162-140">В представлении **Сведения строки накладной** выберите **Распределения** для отображения распределений строк.</span><span class="sxs-lookup"><span data-stu-id="9e162-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="9e162-141">Здесь можно просмотреть учет для строки накладной.</span><span class="sxs-lookup"><span data-stu-id="9e162-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="9e162-142">Отображаемые данные включают финансовые аналитики и счет ГК.</span><span class="sxs-lookup"><span data-stu-id="9e162-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="9e162-143">На странице **Сведения о накладной** выберите **Распределения** для отображения всех распределений.</span><span class="sxs-lookup"><span data-stu-id="9e162-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="9e162-144">Здесь можно просмотреть учет для всей накладной.</span><span class="sxs-lookup"><span data-stu-id="9e162-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="9e162-145">Отображаемые данные включают финансовые аналитики и счета ГК.</span><span class="sxs-lookup"><span data-stu-id="9e162-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="9e162-146">Выберите **Вложения** для просмотра любых примечаний или файлов, которые присоединены к накладной.</span><span class="sxs-lookup"><span data-stu-id="9e162-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="9e162-147">На странице **Сведения о накладной** выберите соответствующее действие workflow-процесса для выполнения процесса проверки.</span><span class="sxs-lookup"><span data-stu-id="9e162-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="9e162-148">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="9e162-148">Select **Done**.</span></span>

