---
title: Пользователи Attract не могут подавать заявления на вакансии на портале вакансий
description: В этой теме объясняется, как устранить проблему, когда пользователи Attract не могут подавать заявления на вакансии на портале вакансий.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462318"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="ab774-103">Пользователи Attract не могут подавать заявления на вакансии на портале вакансий</span><span class="sxs-lookup"><span data-stu-id="ab774-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="ab774-104">Расход</span><span class="sxs-lookup"><span data-stu-id="ab774-104">Issue</span></span>

<span data-ttu-id="ab774-105">Пользователи Attract не могут подавать заявления на вакансии на портале вакансий.</span><span class="sxs-lookup"><span data-stu-id="ab774-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="ab774-106">При попытке подать заявление на вакансию, которая была создана в Dynamics 365 Talent: Attract, браузер загружает страницу непрерывно и не выполняет действие.</span><span class="sxs-lookup"><span data-stu-id="ab774-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="ab774-107">Причина</span><span class="sxs-lookup"><span data-stu-id="ab774-107">Cause</span></span>

<span data-ttu-id="ab774-108">Эта проблема возникает, когда рабочая группа отношений Talent не имеет роли пользователя Talent.</span><span class="sxs-lookup"><span data-stu-id="ab774-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="ab774-109">Приказ</span><span class="sxs-lookup"><span data-stu-id="ab774-109">Resolution</span></span>

<span data-ttu-id="ab774-110">Назначьте роль пользователя Talent рабочей группе отношений Talent.</span><span class="sxs-lookup"><span data-stu-id="ab774-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="ab774-111">Выполните вход в [центр администрирования Power Platform](https://admin.powerplatform.microsoft.com) с любыми из следующих учетных данных администратора:</span><span class="sxs-lookup"><span data-stu-id="ab774-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="ab774-112">Администратор Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ab774-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="ab774-113">Глобальный администратор</span><span class="sxs-lookup"><span data-stu-id="ab774-113">Global admin</span></span>
   - <span data-ttu-id="ab774-114">Администратор Power Platform</span><span class="sxs-lookup"><span data-stu-id="ab774-114">Power Platform admin</span></span>

2. <span data-ttu-id="ab774-115">В области переходов выберите **Среды**, затем выберите среду, в которой требуется назначить роль пользователя Talent рабочей группе отношений Talent.</span><span class="sxs-lookup"><span data-stu-id="ab774-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Выбор среды](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="ab774-117">На панели **Среда** выберите **URL-адрес среды** и выполните вход на портал администрирования среды (например, https:<orgname>.crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="ab774-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="ab774-118">Выберите **Параметры**, выберите **Система**, а затем выберите **Безопасность**.</span><span class="sxs-lookup"><span data-stu-id="ab774-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Переход к разделу безопасности](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="ab774-120">Выберите **Группы**.</span><span class="sxs-lookup"><span data-stu-id="ab774-120">Select **Teams**.</span></span>

   ![Выберите "Группы"](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="ab774-122">Выполните поиск **Рабочая группа отношений Talent** в поле поиска, затем выберите рабочую группу из результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="ab774-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="ab774-123">Выберите **УПРАВЛЕНИЕ РОЛЯМИ** на ленте.</span><span class="sxs-lookup"><span data-stu-id="ab774-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="ab774-124">В диалоговом окне **Управление ролями рабочей группы** выберите **Пользователь Talent** из списка доступных ролей, затем выберите **ОК**, чтобы применить роль.</span><span class="sxs-lookup"><span data-stu-id="ab774-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Применение роли](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="ab774-126">Проверьте свои изменения:</span><span class="sxs-lookup"><span data-stu-id="ab774-126">Test your changes:</span></span>

   1. <span data-ttu-id="ab774-127">Войдите на портал вакансий из нового окна браузера.</span><span class="sxs-lookup"><span data-stu-id="ab774-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="ab774-128">Подайте заявление на вакансию на портале вакансий.</span><span class="sxs-lookup"><span data-stu-id="ab774-128">Apply for the job from the career portal.</span></span> 