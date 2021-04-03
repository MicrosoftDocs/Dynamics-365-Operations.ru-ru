---
title: Мобильная рабочая область "Утверждения накладных"
description: В этом разделе содержится информация о мобильной рабочей области утверждения накладных.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3d90b89900b35bce648841aa9e49737a25309ce2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570085"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="d6f81-103">Мобильная рабочая область "Утверждения накладных"</span><span class="sxs-lookup"><span data-stu-id="d6f81-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6f81-104">В этом разделе содержится информация о мобильной рабочей области **Утверждения накладных**.</span><span class="sxs-lookup"><span data-stu-id="d6f81-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="d6f81-105">Эта рабочая область содержит список накладных, которые были назначены вам через процесс workflow-процесса заголовка накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="d6f81-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="d6f81-106">Эту мобильную рабочую область можно использовать с мобильным приложением Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d6f81-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="d6f81-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="d6f81-107">Overview</span></span>

<span data-ttu-id="d6f81-108">Мобильная рабочая область **Утверждения накладных** позволяет служащим и менеджерам по расчетам с поставщиками просматривать накладные, которые были назначены им как часть workflow-процесса заголовка накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="d6f81-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="d6f81-109">Можно просмотреть сведения о накладной и даже строку и сведения распределения, чтобы принять обоснованные решения.</span><span class="sxs-lookup"><span data-stu-id="d6f81-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="d6f81-110">Из рабочей области можно было предпринять действие, чтобы переместить накладную по workflow-процессу.</span><span class="sxs-lookup"><span data-stu-id="d6f81-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="d6f81-111">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="d6f81-111">Prerequisites</span></span>

<span data-ttu-id="d6f81-112">Перед использованием этой мобильной рабочей области должны быть выполнены следующие предварительные условия.</span><span class="sxs-lookup"><span data-stu-id="d6f81-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d6f81-113">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="d6f81-113">Prerequisite</span></span></th>
<th><span data-ttu-id="d6f81-114">Роль</span><span class="sxs-lookup"><span data-stu-id="d6f81-114">Role</span></span></th>
<th><span data-ttu-id="d6f81-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d6f81-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6f81-116">В организации должна быть развернута система Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="d6f81-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="d6f81-117">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="d6f81-117">System administrator</span></span></td>
<td><span data-ttu-id="d6f81-118">См. <a href="../deployment/deploy-demo-environment.md">Развертывание демонстрационной среды</a>.</span><span class="sxs-lookup"><span data-stu-id="d6f81-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6f81-119">Мобильная рабочая область <strong>Утверждения накладных</strong> должна быть публикована.</span><span class="sxs-lookup"><span data-stu-id="d6f81-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="d6f81-120">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="d6f81-120">System administrator</span></span></td>
<td><span data-ttu-id="d6f81-121">См. <a href="publish-mobile-workspace.md">Публикация мобильной рабочей области</a>.</span><span class="sxs-lookup"><span data-stu-id="d6f81-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="d6f81-122">Загрузите и установите мобильное приложение</span><span class="sxs-lookup"><span data-stu-id="d6f81-122">Download and install the mobile app</span></span>

<span data-ttu-id="d6f81-123">Загрузите и установите мобильное приложение Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="d6f81-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="d6f81-124">Для телефонов Android</span><span class="sxs-lookup"><span data-stu-id="d6f81-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="d6f81-125">Для iPhone</span><span class="sxs-lookup"><span data-stu-id="d6f81-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="d6f81-126">Войдите в систему в мобильном приложении</span><span class="sxs-lookup"><span data-stu-id="d6f81-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="d6f81-127">Запустите приложение на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="d6f81-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="d6f81-128">Введите ваш URL-адрес Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d6f81-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="d6f81-129">При первом входе появится запрос имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="d6f81-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="d6f81-130">Введите свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d6f81-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="d6f81-131">После входа будут показаны доступные рабочие области для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="d6f81-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="d6f81-132">Обратите внимание, что если позже системный администратор опубликует новую рабочую область, вам потребуется обновить список мобильных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="d6f81-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="d6f81-133">[![Потянуть для обновления](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="d6f81-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="d6f81-134">Утверждение накладных с помощью мобильной рабочей области утверждения накладных</span><span class="sxs-lookup"><span data-stu-id="d6f81-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="d6f81-135">На мобильном устройстве выберите рабочую область **Утверждения накладных**.</span><span class="sxs-lookup"><span data-stu-id="d6f81-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="d6f81-136">Выберите накладную, которая была назначена вам workflow-процессом заголовка накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="d6f81-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="d6f81-137">На странице **Сведения о накладной** изучите сведения заголовка накладной, например сведения о поставщике и дате.</span><span class="sxs-lookup"><span data-stu-id="d6f81-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="d6f81-138">Выберите строку накладной для просмотра более подробных сведений о ней в представлении **Сведения строки накладной**.</span><span class="sxs-lookup"><span data-stu-id="d6f81-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="d6f81-139">В представлении **Сведения строки накладной** выберите **Распределения** для отображения распределений строк.</span><span class="sxs-lookup"><span data-stu-id="d6f81-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="d6f81-140">Здесь можно просмотреть учет для строки накладной.</span><span class="sxs-lookup"><span data-stu-id="d6f81-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="d6f81-141">Отображаемые данные включают финансовые аналитики и счет ГК.</span><span class="sxs-lookup"><span data-stu-id="d6f81-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="d6f81-142">На странице **Сведения о накладной** выберите **Распределения** для отображения всех распределений.</span><span class="sxs-lookup"><span data-stu-id="d6f81-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="d6f81-143">Здесь можно просмотреть учет для всей накладной.</span><span class="sxs-lookup"><span data-stu-id="d6f81-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="d6f81-144">Отображаемые данные включают финансовые аналитики и счета ГК.</span><span class="sxs-lookup"><span data-stu-id="d6f81-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="d6f81-145">Выберите **Вложения** для просмотра любых примечаний или файлов, которые присоединены к накладной.</span><span class="sxs-lookup"><span data-stu-id="d6f81-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="d6f81-146">На странице **Сведения о накладной** выберите соответствующее действие workflow-процесса для выполнения процесса проверки.</span><span class="sxs-lookup"><span data-stu-id="d6f81-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="d6f81-147">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="d6f81-147">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]