---
title: Управление пользователями и ролями электронной коммерции
description: В этой теме объясняется, как предоставить пользователям доступ к среде разработки для сайта Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a2235a43fd69adddeaba4c29305435db0fa39d64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255927"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="7b68b-103">Управление пользователями и ролями электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="7b68b-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7b68b-104">В этой теме объясняется, как предоставить пользователям доступ к среде разработки для сайта Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7b68b-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="7b68b-105">Чтобы помочь управлять доступом пользователей и предоставлять пользователям разрешения на выполнение определенных задач, в среде разработки сайтов используются группы безопасности, создаваемые в Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="7b68b-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="7b68b-106">Прежде всего, назначьте новую или существующую группу безопасности из Azure AD каждой роли в среде разработки.</span><span class="sxs-lookup"><span data-stu-id="7b68b-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="7b68b-107">Затем вы предоставляете или отменяет разрешения для отдельных пользователей, добавляя этих пользователей в соответствующую группу безопасности или удаляя их из группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="7b68b-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="7b68b-108">Обзор ролей в среде разработки</span><span class="sxs-lookup"><span data-stu-id="7b68b-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="7b68b-109">Среда разработки Dynamics 365 for Commerce поддерживает следующие роли.</span><span class="sxs-lookup"><span data-stu-id="7b68b-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="7b68b-110">Роль</span><span class="sxs-lookup"><span data-stu-id="7b68b-110">Role</span></span>                 | <span data-ttu-id="7b68b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7b68b-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="7b68b-112">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="7b68b-112">System Administrator</span></span> | <span data-ttu-id="7b68b-113">Пользователи, имеющие эту роль, имеют все привилегии для всех инструментов и для всех оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="7b68b-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="7b68b-114">Они также могут создавать сайты.</span><span class="sxs-lookup"><span data-stu-id="7b68b-114">They can also create sites.</span></span> |
| <span data-ttu-id="7b68b-115">Администратор</span><span class="sxs-lookup"><span data-stu-id="7b68b-115">Administrator</span></span>   | <span data-ttu-id="7b68b-116">Пользователи, имеющие эту роль, имеют все привилегии для всех инструментов, оценок и отзывов в определенной структуре сайта.</span><span class="sxs-lookup"><span data-stu-id="7b68b-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="7b68b-117">Веб-производитель</span><span class="sxs-lookup"><span data-stu-id="7b68b-117">Web Producer</span></span>         | <span data-ttu-id="7b68b-118">Пользователи, имеющие эту роль, могут создавать страницы, фрагменты и шаблоны, отправлять активы и управлять ими, а также расширять продукты и категории.</span><span class="sxs-lookup"><span data-stu-id="7b68b-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="7b68b-119">Читатель</span><span class="sxs-lookup"><span data-stu-id="7b68b-119">Reader</span></span>               | <span data-ttu-id="7b68b-120">Пользователи, имеющие эту роль, могут просматривать страницы, шаблоны, активы, фрагменты, макеты и параметры, но не могут вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="7b68b-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="7b68b-121">Модератор оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="7b68b-121">RnR Moderator</span></span>        | <span data-ttu-id="7b68b-122">Пользователи, имеющие эту роль, могут модерировать отзывы по продукту.</span><span class="sxs-lookup"><span data-stu-id="7b68b-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="7b68b-123">Роль системного администратора</span><span class="sxs-lookup"><span data-stu-id="7b68b-123">System Administrator role</span></span>

<span data-ttu-id="7b68b-124">При подготовке Dynamics 365 Commerce в среде Microsoft Dynamics Lifecycle Services (LCS) необходимо предоставить группу безопасности для роли **Системный администратор**.</span><span class="sxs-lookup"><span data-stu-id="7b68b-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="7b68b-125">Эта роль затем автоматически применяется ко всем сайтам, созданным в настраиваемой среде.</span><span class="sxs-lookup"><span data-stu-id="7b68b-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="7b68b-126">Группу безопасности для этой роли можно обновить только в LCS.</span><span class="sxs-lookup"><span data-stu-id="7b68b-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="7b68b-127">На странице **Администрирование сайта** для всех сайтов она доступна только для чтения и предназначена только для информационных целей.</span><span class="sxs-lookup"><span data-stu-id="7b68b-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="7b68b-128">Роль администратора</span><span class="sxs-lookup"><span data-stu-id="7b68b-128">Administrator role</span></span>

<span data-ttu-id="7b68b-129">При создании нового сайта в Commerce вам будет предложено предоставить группу безопасности для роли **Администратор**.</span><span class="sxs-lookup"><span data-stu-id="7b68b-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="7b68b-130">Сведения о разрешениях, предоставляемых данной ролью, см. в таблице выше в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="7b68b-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="7b68b-131">Добавление и обновление групп безопасности</span><span class="sxs-lookup"><span data-stu-id="7b68b-131">Add or update security groups</span></span>

<span data-ttu-id="7b68b-132">После создания сайта только пользователи, которые находятся в группах безопасности, связанных с ролями **Системный администратор** и **Администратор**, могут получить доступ к среде разработки для этого сайта.</span><span class="sxs-lookup"><span data-stu-id="7b68b-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="7b68b-133">Чтобы назначить пользователей для ролей **Веб-производитель**, **Модератор оценок и отзывов** и **Читатель**, необходимо назначить этим ролям группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="7b68b-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="7b68b-134">Чтобы добавить группу безопасности к роли или обновить группу безопасности, которая в настоящее время назначена роли, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b68b-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="7b68b-135">Перейдите на сайт, который требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="7b68b-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="7b68b-136">В области **Управление сайтом** откройте страницу **Безопасность**.</span><span class="sxs-lookup"><span data-stu-id="7b68b-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="7b68b-137">Выберите роль для изменения.</span><span class="sxs-lookup"><span data-stu-id="7b68b-137">Select the role to modify.</span></span>
1. <span data-ttu-id="7b68b-138">Добавьте группы безопасности в роли или удалите группы безопасности из ролей.</span><span class="sxs-lookup"><span data-stu-id="7b68b-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b68b-139">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7b68b-139">Additional resources</span></span>

[<span data-ttu-id="7b68b-140">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="7b68b-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="7b68b-141">Особенности поисковой оптимизации (SEO) для вашего сайта</span><span class="sxs-lookup"><span data-stu-id="7b68b-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="7b68b-142">Управление политикой безопасности содержимого (CSP)</span><span class="sxs-lookup"><span data-stu-id="7b68b-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]