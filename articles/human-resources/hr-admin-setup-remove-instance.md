---
title: Удаление экземпляра
description: В этой статье содержится пошаговое описание процесса удаления тестовой или производственной среды для Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72a5b99150e5ccdf9a542b569c94c64cb95923fd
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053619"
---
# <a name="remove-an-instance"></a><span data-ttu-id="6e07d-103">Удаление экземпляра</span><span class="sxs-lookup"><span data-stu-id="6e07d-103">Remove an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6e07d-104">В этой статье содержится пошаговое описание процесса удаления тестовой или производственной среды для Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e07d-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="6e07d-105">Удаление тестовой среды</span><span class="sxs-lookup"><span data-stu-id="6e07d-105">Remove a test drive environment</span></span>

<span data-ttu-id="6e07d-106">Тестовые среды Human Resources подготавливаются с политикой срока действия 60 дней.</span><span class="sxs-lookup"><span data-stu-id="6e07d-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="6e07d-107">Тем не менее владельцы тестовых сред могут прекратить пробную эксплуатацию раньше, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6e07d-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="6e07d-108">Перейдите к [Центру администрирования Power Apps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="6e07d-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="6e07d-109">Выберите **Среды**.</span><span class="sxs-lookup"><span data-stu-id="6e07d-109">Select **Environments**.</span></span>
3. <span data-ttu-id="6e07d-110">Выберите тестовую среду, имя которой построено по следующему шаблону: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="6e07d-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="6e07d-111">Выберите **Удалить** и подтвердите решение.</span><span class="sxs-lookup"><span data-stu-id="6e07d-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="6e07d-112">Существующая тестовая среда будет удалена.</span><span class="sxs-lookup"><span data-stu-id="6e07d-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="6e07d-113">При ее удалении вы можете зарегистрироваться на новую тестовую среду.</span><span class="sxs-lookup"><span data-stu-id="6e07d-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="6e07d-114">Удаление производственной среды</span><span class="sxs-lookup"><span data-stu-id="6e07d-114">Remove a production environment</span></span>

<span data-ttu-id="6e07d-115">В этой статье предполагается, что вы приобрели Human Resources в соответствии с соглашением поставщика облачных решений (CSP) или архитектуры предприятия (EA).</span><span class="sxs-lookup"><span data-stu-id="6e07d-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="6e07d-116">Так как в одна среда Human Resources содержится в одной среде Power Apps, существуют две возможности.</span><span class="sxs-lookup"><span data-stu-id="6e07d-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="6e07d-117">Первый вариант включает в себя удаление всей среды Power Apps; второй вариант включает в себя удаление только Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e07d-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="6e07d-118">Первый вариант предпочтителен, если среда Power Apps была создана специально в целях подготовки Human Resources, и вы только начали реализацию или не имеете никаких установленных интеграций.</span><span class="sxs-lookup"><span data-stu-id="6e07d-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="6e07d-119">Второй вариант подходит при наличии установившейся среды Power Apps, заполненной богатыми данными, которое используются в Power Apps и Power Automate.</span><span class="sxs-lookup"><span data-stu-id="6e07d-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="6e07d-120">Перед удалением среды Power Apps убедитесь, что она не используется для интеграции богатых данных вне Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e07d-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="6e07d-121">Также обратите внимание, что удаление сред Power Apps по умолчанию невозможно.</span><span class="sxs-lookup"><span data-stu-id="6e07d-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="6e07d-122">Чтобы удалить всю среду Power Apps, включая Human Resources и связанные приложения и потоки:</span><span class="sxs-lookup"><span data-stu-id="6e07d-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="6e07d-123">Перейдите к [Центру администрирования Power Apps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="6e07d-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="6e07d-124">Выберите **Среды**.</span><span class="sxs-lookup"><span data-stu-id="6e07d-124">Select **Environments**.</span></span>
3. <span data-ttu-id="6e07d-125">Выберите среду для удаления.</span><span class="sxs-lookup"><span data-stu-id="6e07d-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="6e07d-126">Выберите **Удалить** и подтвердите решение.</span><span class="sxs-lookup"><span data-stu-id="6e07d-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="6e07d-127">Дождитесь завершения удаления.</span><span class="sxs-lookup"><span data-stu-id="6e07d-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="6e07d-128">Выполните вход в [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) с помощью учетной записи, используемой для подписки на Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e07d-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="6e07d-129">Выберите проект Human Resources, который содержит среду.</span><span class="sxs-lookup"><span data-stu-id="6e07d-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="6e07d-130">В проекте LCS выберите плитку **Управление приложением Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="6e07d-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="6e07d-131">Выберите экземпляр для удаления.</span><span class="sxs-lookup"><span data-stu-id="6e07d-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="6e07d-132">Выберите **Удалить экземпляр** и подтвердите этот выбор.</span><span class="sxs-lookup"><span data-stu-id="6e07d-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="6e07d-133">Чтобы удалить среду Human Resources из существующей среды Power Apps, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6e07d-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="6e07d-134">Обратите внимание, что временно необходимо обращаться в службу поддержки и связываться с группой Human Resources DevOps, пока эта функция не будет включена непосредственно в LCS.</span><span class="sxs-lookup"><span data-stu-id="6e07d-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="6e07d-135">Обратитесь в службу поддержки, чтобы инициировать запрос на удаление.</span><span class="sxs-lookup"><span data-stu-id="6e07d-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="6e07d-136">Группа поддержки инициирует запрос на удаление в группе Human Resources DevOps.</span><span class="sxs-lookup"><span data-stu-id="6e07d-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="6e07d-137">Продолжите после получения сообщения, что среда была удалена.</span><span class="sxs-lookup"><span data-stu-id="6e07d-137">Continue after you receive word that the environment has been removed.</span></span>
4. <span data-ttu-id="6e07d-138">Выполните вход в LCS с помощью учетной записи, используемой для подписки на Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e07d-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="6e07d-139">Выберите проект Human Resources, который содержит среду.</span><span class="sxs-lookup"><span data-stu-id="6e07d-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="6e07d-140">В проекте LCS выберите плитку **Управление приложением Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="6e07d-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="6e07d-141">Выберите экземпляр, который вы хотите удалить, которой должен быть помечен статусом развертывания **Удалено**.</span><span class="sxs-lookup"><span data-stu-id="6e07d-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Deleted**.</span></span>
8. <span data-ttu-id="6e07d-142">Выберите **Удалить экземпляр** и подтвердите этот выбор.</span><span class="sxs-lookup"><span data-stu-id="6e07d-142">Select **Remove instance** and confirm your decision.</span></span> 

## <a name="recover-a-soft-deleted-environment"></a><span data-ttu-id="6e07d-143">Восстановление среды с мягким удалением</span><span class="sxs-lookup"><span data-stu-id="6e07d-143">Recover a soft-deleted environment</span></span>

<span data-ttu-id="6e07d-144">При удалении среды Power Apps, к которой подключена среда Human Resources, статус среды Human Resources в Lifecycle Services будет **мягко удален**.</span><span class="sxs-lookup"><span data-stu-id="6e07d-144">If you delete the Power Apps environment that your Human Resources environment is connected to, the status of the Human Resources environment in Lifecycle Services will be **Soft deleted**.</span></span> <span data-ttu-id="6e07d-145">В этом случае пользователи не смогут подключаться к Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e07d-145">In this case, users can't connect to Human Resources.</span></span>

<span data-ttu-id="6e07d-146">Чтобы восстановить среду:</span><span class="sxs-lookup"><span data-stu-id="6e07d-146">To restore the environment:</span></span>

1. <span data-ttu-id="6e07d-147">Следуйте указаниям раздела [Восстановление среды Power Apps](/power-platform/admin/recover-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6e07d-147">Follow the instructions in [Recover the Power Apps environment](/power-platform/admin/recover-environment.md).</span></span>

2. <span data-ttu-id="6e07d-148">Обратитесь в службу поддержки, чтобы восстановить среду Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e07d-148">Contact Support to restore the Human Resources environment.</span></span> <span data-ttu-id="6e07d-149">Для получения дополнительных см. [Получение поддержки](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="6e07d-149">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

> [!Warning]
> <span data-ttu-id="6e07d-150">Среды Power Apps сохраняются только в течение семи дней после удаления.</span><span class="sxs-lookup"><span data-stu-id="6e07d-150">Power Apps environments are only saved for seven days after deletion.</span></span> <span data-ttu-id="6e07d-151">Среду следует восстанавливать в течение семи дней.</span><span class="sxs-lookup"><span data-stu-id="6e07d-151">You must recover the environment within the seven day period.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]