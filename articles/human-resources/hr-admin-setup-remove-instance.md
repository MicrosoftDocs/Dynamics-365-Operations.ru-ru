---
title: Удаление экземпляра
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010287"
---
# <a name="remove-an-instance"></a><span data-ttu-id="ed5c2-102">Удаление экземпляра</span><span class="sxs-lookup"><span data-stu-id="ed5c2-102">Remove an instance</span></span>

<span data-ttu-id="ed5c2-103">В этой статье содержится пошаговое описание процесса удаления тестовой или производственной среды для Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="ed5c2-104">Удаление тестовой среды</span><span class="sxs-lookup"><span data-stu-id="ed5c2-104">Remove a test drive environment</span></span>

<span data-ttu-id="ed5c2-105">Тестовые среды Human Resources подготавливаются с политикой срока действия 60 дней.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="ed5c2-106">Тем не менее владельцы тестовых сред могут прекратить пробную эксплуатацию раньше, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="ed5c2-107">Перейдите к [Центру администрирования Power Apps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ed5c2-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="ed5c2-108">Выберите **Среды**.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-108">Select **Environments**.</span></span>
3. <span data-ttu-id="ed5c2-109">Выберите тестовую среду, имя которой построено по следующему шаблону: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="ed5c2-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="ed5c2-110">Выберите **Удалить** и подтвердите решение.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="ed5c2-111">Существующая тестовая среда будет удалена.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="ed5c2-112">При ее удалении вы можете зарегистрироваться на новую тестовую среду.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="ed5c2-113">Удаление производственной среды</span><span class="sxs-lookup"><span data-stu-id="ed5c2-113">Remove a production environment</span></span>

<span data-ttu-id="ed5c2-114">В этой статье предполагается, что вы приобрели Human Resources в соответствии с соглашением поставщика облачных решений (CSP) или архитектуры предприятия (EA).</span><span class="sxs-lookup"><span data-stu-id="ed5c2-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="ed5c2-115">Так как в одна среда Human Resources содержится в одной среде Power Apps, существуют две возможности.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="ed5c2-116">Первый вариант включает в себя удаление всей среды Power Apps; второй вариант включает в себя удаление только Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="ed5c2-117">Первый вариант предпочтителен, если среда Power Apps была создана специально в целях подготовки Human Resources, и вы только начали реализацию или не имеете никаких установленных интеграций.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="ed5c2-118">Второй вариант подходит при наличии установившейся среды Power Apps, заполненной богатыми данными, которое используются в Power Apps и Power Automate.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="ed5c2-119">Перед удалением среды Power Apps убедитесь, что она не используется для интеграции богатых данных вне Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="ed5c2-120">Также обратите внимание, что удаление сред Power Apps по умолчанию невозможно.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="ed5c2-121">Чтобы удалить всю среду Power Apps, включая Human Resources и связанные приложения и потоки:</span><span class="sxs-lookup"><span data-stu-id="ed5c2-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="ed5c2-122">Перейдите к [Центру администрирования Power Apps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ed5c2-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="ed5c2-123">Выберите **Среды**.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-123">Select **Environments**.</span></span>
3. <span data-ttu-id="ed5c2-124">Выберите среду для удаления.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="ed5c2-125">Выберите **Удалить** и подтвердите решение.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="ed5c2-126">Дождитесь завершения удаления.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="ed5c2-127">Выполните вход в [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) с помощью учетной записи, используемой для подписки на Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="ed5c2-128">Выберите проект Human Resources, который содержит среду.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="ed5c2-129">В проекте LCS выберите плитку **Управление приложением Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="ed5c2-130">Выберите экземпляр для удаления.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="ed5c2-131">Выберите **Удалить экземпляр** и подтвердите этот выбор.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="ed5c2-132">Чтобы удалить среду Human Resources из существующей среды Power Apps, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="ed5c2-133">Обратите внимание, что временно необходимо обращаться в службу поддержки и связываться с группой Human Resources DevOps, пока эта функция не будет включена непосредственно в LCS.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="ed5c2-134">Обратитесь в службу поддержки, чтобы инициировать запрос на удаление.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="ed5c2-135">Группа поддержки инициирует запрос на удаление в группе Human Resources DevOps.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="ed5c2-136">Продолжите после получения сообщения, что среда была удалена.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="ed5c2-137">Выполните вход в LCS с помощью учетной записи, используемой для подписки на Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="ed5c2-138">Выберите проект Human Resources, который содержит среду.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="ed5c2-139">В проекте LCS выберите плитку **Управление приложением Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="ed5c2-140">Выберите экземпляр, который вы хотите удалить, которой должен быть помечен статусом развертывания **Сбой**.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="ed5c2-141">Выберите **Удалить экземпляр** и подтвердите этот выбор.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-141">Select **Remove instance** and confirm your decision.</span></span> 
