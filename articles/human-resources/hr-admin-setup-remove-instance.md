---
title: Удаление экземпляра
description: В этой статье содержится пошаговое описание процесса удаления тестовой или производственной среды для Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17f299f81d1326dfb06c11a6125acc54b8ef2a6e
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431207"
---
# <a name="remove-an-instance"></a><span data-ttu-id="74db0-103">Удаление экземпляра</span><span class="sxs-lookup"><span data-stu-id="74db0-103">Remove an instance</span></span>

<span data-ttu-id="74db0-104">В этой статье содержится пошаговое описание процесса удаления тестовой или производственной среды для Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="74db0-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="74db0-105">Удаление тестовой среды</span><span class="sxs-lookup"><span data-stu-id="74db0-105">Remove a test drive environment</span></span>

<span data-ttu-id="74db0-106">Тестовые среды Human Resources подготавливаются с политикой срока действия 60 дней.</span><span class="sxs-lookup"><span data-stu-id="74db0-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="74db0-107">Тем не менее владельцы тестовых сред могут прекратить пробную эксплуатацию раньше, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="74db0-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="74db0-108">Перейдите к [Центру администрирования Power Apps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="74db0-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="74db0-109">Выберите **Среды**.</span><span class="sxs-lookup"><span data-stu-id="74db0-109">Select **Environments**.</span></span>
3. <span data-ttu-id="74db0-110">Выберите тестовую среду, имя которой построено по следующему шаблону: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="74db0-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="74db0-111">Выберите **Удалить** и подтвердите решение.</span><span class="sxs-lookup"><span data-stu-id="74db0-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="74db0-112">Существующая тестовая среда будет удалена.</span><span class="sxs-lookup"><span data-stu-id="74db0-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="74db0-113">При ее удалении вы можете зарегистрироваться на новую тестовую среду.</span><span class="sxs-lookup"><span data-stu-id="74db0-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="74db0-114">Удаление производственной среды</span><span class="sxs-lookup"><span data-stu-id="74db0-114">Remove a production environment</span></span>

<span data-ttu-id="74db0-115">В этой статье предполагается, что вы приобрели Human Resources в соответствии с соглашением поставщика облачных решений (CSP) или архитектуры предприятия (EA).</span><span class="sxs-lookup"><span data-stu-id="74db0-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="74db0-116">Так как в одна среда Human Resources содержится в одной среде Power Apps, существуют две возможности.</span><span class="sxs-lookup"><span data-stu-id="74db0-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="74db0-117">Первый вариант включает в себя удаление всей среды Power Apps; второй вариант включает в себя удаление только Human Resources.</span><span class="sxs-lookup"><span data-stu-id="74db0-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="74db0-118">Первый вариант предпочтителен, если среда Power Apps была создана специально в целях подготовки Human Resources, и вы только начали реализацию или не имеете никаких установленных интеграций.</span><span class="sxs-lookup"><span data-stu-id="74db0-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="74db0-119">Второй вариант подходит при наличии установившейся среды Power Apps, заполненной богатыми данными, которое используются в Power Apps и Power Automate.</span><span class="sxs-lookup"><span data-stu-id="74db0-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="74db0-120">Перед удалением среды Power Apps убедитесь, что она не используется для интеграции богатых данных вне Human Resources.</span><span class="sxs-lookup"><span data-stu-id="74db0-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="74db0-121">Также обратите внимание, что удаление сред Power Apps по умолчанию невозможно.</span><span class="sxs-lookup"><span data-stu-id="74db0-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="74db0-122">Чтобы удалить всю среду Power Apps, включая Human Resources и связанные приложения и потоки:</span><span class="sxs-lookup"><span data-stu-id="74db0-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="74db0-123">Перейдите к [Центру администрирования Power Apps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="74db0-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="74db0-124">Выберите **Среды**.</span><span class="sxs-lookup"><span data-stu-id="74db0-124">Select **Environments**.</span></span>
3. <span data-ttu-id="74db0-125">Выберите среду для удаления.</span><span class="sxs-lookup"><span data-stu-id="74db0-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="74db0-126">Выберите **Удалить** и подтвердите решение.</span><span class="sxs-lookup"><span data-stu-id="74db0-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="74db0-127">Дождитесь завершения удаления.</span><span class="sxs-lookup"><span data-stu-id="74db0-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="74db0-128">Выполните вход в [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) с помощью учетной записи, используемой для подписки на Human Resources.</span><span class="sxs-lookup"><span data-stu-id="74db0-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="74db0-129">Выберите проект Human Resources, который содержит среду.</span><span class="sxs-lookup"><span data-stu-id="74db0-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="74db0-130">В проекте LCS выберите плитку **Управление приложением Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="74db0-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="74db0-131">Выберите экземпляр для удаления.</span><span class="sxs-lookup"><span data-stu-id="74db0-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="74db0-132">Выберите **Удалить экземпляр** и подтвердите этот выбор.</span><span class="sxs-lookup"><span data-stu-id="74db0-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="74db0-133">Чтобы удалить среду Human Resources из существующей среды Power Apps, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="74db0-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="74db0-134">Обратите внимание, что временно необходимо обращаться в службу поддержки и связываться с группой Human Resources DevOps, пока эта функция не будет включена непосредственно в LCS.</span><span class="sxs-lookup"><span data-stu-id="74db0-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="74db0-135">Обратитесь в службу поддержки, чтобы инициировать запрос на удаление.</span><span class="sxs-lookup"><span data-stu-id="74db0-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="74db0-136">Группа поддержки инициирует запрос на удаление в группе Human Resources DevOps.</span><span class="sxs-lookup"><span data-stu-id="74db0-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="74db0-137">Продолжите после получения сообщения, что среда была удалена.</span><span class="sxs-lookup"><span data-stu-id="74db0-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="74db0-138">Выполните вход в LCS с помощью учетной записи, используемой для подписки на Human Resources.</span><span class="sxs-lookup"><span data-stu-id="74db0-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="74db0-139">Выберите проект Human Resources, который содержит среду.</span><span class="sxs-lookup"><span data-stu-id="74db0-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="74db0-140">В проекте LCS выберите плитку **Управление приложением Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="74db0-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="74db0-141">Выберите экземпляр, который вы хотите удалить, которой должен быть помечен статусом развертывания **Сбой**.</span><span class="sxs-lookup"><span data-stu-id="74db0-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="74db0-142">Выберите **Удалить экземпляр** и подтвердите этот выбор.</span><span class="sxs-lookup"><span data-stu-id="74db0-142">Select **Remove instance** and confirm your decision.</span></span> 
