---
title: Мобильная рабочая область "Утверждения накладных"
description: В этом разделе содержится информация о мобильной рабочей области утверждения накладных. Эта рабочая область содержит список накладных, которые были назначены вам через процесс workflow-процесса заголовка накладной поставщика.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ff726670e0fd7566a74e6def73555a7c53b86f97
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "327006"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="43c06-104">Мобильная рабочая область "Утверждения накладных"</span><span class="sxs-lookup"><span data-stu-id="43c06-104">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43c06-105">В этом разделе содержится информация о мобильной рабочей области **Утверждения накладных**.</span><span class="sxs-lookup"><span data-stu-id="43c06-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="43c06-106">Эта рабочая область содержит список накладных, которые были назначены вам через процесс workflow-процесса заголовка накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="43c06-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="43c06-107">Эту мобильную рабочую область можно использовать с мобильным приложением Microsoft Dynamics 365 for Unified Operations Mobile.</span><span class="sxs-lookup"><span data-stu-id="43c06-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="43c06-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="43c06-108">Overview</span></span>

<span data-ttu-id="43c06-109">Мобильная рабочая область **Утверждения накладных** позволяет служащим и менеджерам по расчетам с поставщиками просматривать накладные, которые были назначены им как часть workflow-процесса заголовка накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="43c06-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="43c06-110">Можно просмотреть сведения о накладной и даже строку и сведения распределения, чтобы принять обоснованные решения.</span><span class="sxs-lookup"><span data-stu-id="43c06-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="43c06-111">Из рабочей области можно было предпринять действие, чтобы переместить накладную по workflow-процессу.</span><span class="sxs-lookup"><span data-stu-id="43c06-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="43c06-112">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="43c06-112">Prerequisites</span></span>

<span data-ttu-id="43c06-113">Перед использованием этой мобильной рабочей области должны быть выполнены следующие предварительные условия.</span><span class="sxs-lookup"><span data-stu-id="43c06-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="43c06-114">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="43c06-114">Prerequisite</span></span></th>
<th><span data-ttu-id="43c06-115">Роль</span><span class="sxs-lookup"><span data-stu-id="43c06-115">Role</span></span></th>
<th><span data-ttu-id="43c06-116">описание</span><span class="sxs-lookup"><span data-stu-id="43c06-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43c06-117">В организации должна быть развернута система Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="43c06-117">Microsoft Dynamics 365 for Finance and Operations must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="43c06-118">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="43c06-118">System administrator</span></span></td>
<td><span data-ttu-id="43c06-119">См. <a href="../deployment/deploy-demo-environment.md">Развертывание демонстрационной среды</a>.</span><span class="sxs-lookup"><span data-stu-id="43c06-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="43c06-120">Мобильная рабочая область <strong>Утверждения накладных</strong> должна быть публикована.</span><span class="sxs-lookup"><span data-stu-id="43c06-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="43c06-121">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="43c06-121">System administrator</span></span></td>
<td><span data-ttu-id="43c06-122">См. <a href="publish-mobile-workspace.md">Публикация мобильной рабочей области</a>.</span><span class="sxs-lookup"><span data-stu-id="43c06-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="43c06-123">Загрузите и установите мобильное приложение</span><span class="sxs-lookup"><span data-stu-id="43c06-123">Download and install the mobile app</span></span>

<span data-ttu-id="43c06-124">Загрузите и установите мобильное приложение Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="43c06-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="43c06-125">Для телефонов Android</span><span class="sxs-lookup"><span data-stu-id="43c06-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="43c06-126">Для iPhone</span><span class="sxs-lookup"><span data-stu-id="43c06-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="43c06-127">Войдите в систему в мобильном приложении</span><span class="sxs-lookup"><span data-stu-id="43c06-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="43c06-128">Запустите приложение на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="43c06-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="43c06-129">Введите ваш URL-адрес Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="43c06-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="43c06-130">При первом входе появится запрос имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="43c06-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="43c06-131">Введите свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="43c06-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="43c06-132">После входа будут показаны доступные рабочие области для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="43c06-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="43c06-133">Обратите внимание, что если позже системный администратор опубликует новую рабочую область, вам потребуется обновить список мобильных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="43c06-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="43c06-134">[![Потянуть для обновления](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="43c06-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="43c06-135">Утверждение накладных с помощью мобильной рабочей области утверждения накладных</span><span class="sxs-lookup"><span data-stu-id="43c06-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="43c06-136">На мобильном устройстве выберите рабочую область **Утверждения накладных**.</span><span class="sxs-lookup"><span data-stu-id="43c06-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="43c06-137">Выберите накладную, которая была назначена вам workflow-процессом заголовка накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="43c06-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="43c06-138">На странице **Сведения о накладной** изучите сведения заголовка накладной, например сведения о поставщике и дате.</span><span class="sxs-lookup"><span data-stu-id="43c06-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="43c06-139">Выберите строку накладной для просмотра более подробных сведений о ней в представлении **Сведения строки накладной**.</span><span class="sxs-lookup"><span data-stu-id="43c06-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="43c06-140">В представлении **Сведения строки накладной** выберите **Распределения** для отображения распределений строк.</span><span class="sxs-lookup"><span data-stu-id="43c06-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="43c06-141">Здесь можно просмотреть учет для строки накладной.</span><span class="sxs-lookup"><span data-stu-id="43c06-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="43c06-142">Отображаемые данные включают финансовые аналитики и счет ГК.</span><span class="sxs-lookup"><span data-stu-id="43c06-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="43c06-143">На странице **Сведения о накладной** выберите **Распределения** для отображения всех распределений.</span><span class="sxs-lookup"><span data-stu-id="43c06-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="43c06-144">Здесь можно просмотреть учет для всей накладной.</span><span class="sxs-lookup"><span data-stu-id="43c06-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="43c06-145">Отображаемые данные включают финансовые аналитики и счета ГК.</span><span class="sxs-lookup"><span data-stu-id="43c06-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="43c06-146">Выберите **Вложения** для просмотра любых примечаний или файлов, которые присоединены к накладной.</span><span class="sxs-lookup"><span data-stu-id="43c06-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="43c06-147">На странице **Сведения о накладной** выберите соответствующее действие workflow-процесса для выполнения процесса проверки.</span><span class="sxs-lookup"><span data-stu-id="43c06-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="43c06-148">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="43c06-148">Select **Done**.</span></span>
