---
title: Удаление сред Talent
description: В этом разделе содержится пошаговое описание процесса удаления тестовой или производственной среды для Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: d608ee3ad90d23279557e5e9be4d398ffac3a266
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010623"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="0f2a1-103">Удаление сред Talent</span><span class="sxs-lookup"><span data-stu-id="0f2a1-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0f2a1-104">В этом разделе содержится пошаговое описание процесса удаления тестовой или производственной среды для Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="0f2a1-105">Удаление тестовой среды</span><span class="sxs-lookup"><span data-stu-id="0f2a1-105">Removing a test drive environment</span></span>

<span data-ttu-id="0f2a1-106">Тестовые среды Talent подготавливаются с политикой срока действия 60 дней.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="0f2a1-107">Тем не менее владельцы тестовых сред могут прекратить пробную эксплуатацию раньше, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="0f2a1-108">Перейдите к [Центру администрирования PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="0f2a1-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="0f2a1-109">Выберите **Среды**.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-109">Select **Environments**.</span></span>
3. <span data-ttu-id="0f2a1-110">Выберите тестовую среду, имя которой построено по следующему шаблону: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="0f2a1-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="0f2a1-111">Выберите **Удалить** и подтвердите решение.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="0f2a1-112">Существующая тестовая среда будет удалена.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="0f2a1-113">При ее удалении вы можете зарегистрироваться на новую тестовую среду.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="0f2a1-114">Удаление производственной среды</span><span class="sxs-lookup"><span data-stu-id="0f2a1-114">Removing a production environment</span></span>

<span data-ttu-id="0f2a1-115">В этом разделе предполагается, что вы приобрели Talent в соответствии с соглашением поставщика облачных решений (CSP) или архитектуры предприятия (EA).</span><span class="sxs-lookup"><span data-stu-id="0f2a1-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="0f2a1-116">Так как в одна среда Talent "содержится" в одной среде PowerApps, существуют две возможности.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="0f2a1-117">Первый вариант включает в себя удаление всей среды PowerApps; второй вариант включает в себя удаление только Talent.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="0f2a1-118">Первый вариант предпочтителен, если среда PowerApps была создана специально в целях подготовки Talent, и вы только начали реализацию или не имеете никаких установленных интеграций.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="0f2a1-119">Второй вариант подходит при наличии установившейся среды PowerApps, заполненной богатыми данными, которое используются в PowerApps и Flows.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="0f2a1-120">Перед удалением среды PowerApps убедитесь, что она не используется для интеграции богатых данных вне Talent.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="0f2a1-121">Также обратите внимание, что удаление сред PowerApps по умолчанию невозможно.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="0f2a1-122">Чтобы удалить всю среду PowerApps, включая Talent и связанные приложения и потоки:</span><span class="sxs-lookup"><span data-stu-id="0f2a1-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="0f2a1-123">Перейдите к [Центру администрирования PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="0f2a1-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="0f2a1-124">Выберите **Среды**.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-124">Select **Environments**.</span></span>
3. <span data-ttu-id="0f2a1-125">Выберите среду для удаления.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="0f2a1-126">Выберите **Удалить** и подтвердите решение.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="0f2a1-127">Дождитесь завершения удаления.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="0f2a1-128">Выполните вход в [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) с помощью учетной записи, используемой для подписки на Talent.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="0f2a1-129">Выберите проект Talent, который содержит среду.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="0f2a1-130">В проекте LCS выберите плитку **Управление приложением Talent**.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="0f2a1-131">Выберите экземпляр для удаления.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="0f2a1-132">Выберите **Удалить экземпляр** и подтвердите этот выбор.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="0f2a1-133">Чтобы удалить среду Talent из существующей среды PowerApps, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="0f2a1-134">Обратите внимание, что временно необходимо обращаться в службу поддержки и связываться с группой Talent DevOps, пока эта функция не будет включена непосредственно в LCS.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="0f2a1-135">Обратитесь в службу поддержки, чтобы инициировать запрос на удаление.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="0f2a1-136">Группа поддержки инициирует запрос на удаление в группе Talent DevOps.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="0f2a1-137">Продолжите после получения сообщения, что среда была удалена.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="0f2a1-138">Выполните вход в LCS с помощью учетной записи, используемой для подписки на Talent.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="0f2a1-139">Выберите проект Talent, который содержит среду.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="0f2a1-140">В проекте LCS выберите плитку **Управление приложением Talent**.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="0f2a1-141">Выберите экземпляр, который вы хотите удалить, которой должен быть помечен статусом развертывания **Сбой**.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="0f2a1-142">Выберите **Удалить экземпляр** и подтвердите этот выбор.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-142">Select **Remove instance** and confirm your decision.</span></span> 

