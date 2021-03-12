---
title: Назначение ролей пользователей аренды
description: В этой теме описываются роли безопасности, которые используются в аренде активов. Здесь также объясняется, как назначить пользователей для этих ролей.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: df23e219f5bd859b0072785dfd5f7a0ec63f540e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995401"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="efff2-104">Назначение ролей пользователей аренды</span><span class="sxs-lookup"><span data-stu-id="efff2-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efff2-105">В этой теме описываются роли безопасности, которые используются в аренде активов.</span><span class="sxs-lookup"><span data-stu-id="efff2-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="efff2-106">Здесь также объясняется, как назначить пользователей для этих ролей.</span><span class="sxs-lookup"><span data-stu-id="efff2-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="efff2-107">Три роли пользователей регулируют доступ в аренде активов.</span><span class="sxs-lookup"><span data-stu-id="efff2-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="efff2-108">Одна роль подходит для обслуживания аренд, одна подходит для просмотра аренд, и одна подходит для выполнения обязанностей клерка по аренде.</span><span class="sxs-lookup"><span data-stu-id="efff2-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="efff2-109">Каждая роль обладает определенными разрешениями для всех страниц аренды, и каждая из них позволяет пользователям просматривать, создавать, изменять и удалять аренды в соответствии с должностными обязанностями.</span><span class="sxs-lookup"><span data-stu-id="efff2-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="efff2-110">Роль</span><span class="sxs-lookup"><span data-stu-id="efff2-110">Role</span></span>           | <span data-ttu-id="efff2-111">описание</span><span class="sxs-lookup"><span data-stu-id="efff2-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="efff2-112">Обслуживание аренды</span><span class="sxs-lookup"><span data-stu-id="efff2-112">Maintain Lease</span></span> | <span data-ttu-id="efff2-113">Пользователи с этой ролью могут добавлять, изменять, удалять и просматривать аренды.</span><span class="sxs-lookup"><span data-stu-id="efff2-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="efff2-114">Эта роль предназначена для ежедневных пользователей, чьи задачи включают создание и разноску записей ежемесячных журналов и добавление новых аренд.</span><span class="sxs-lookup"><span data-stu-id="efff2-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="efff2-115">Эта роль предоставляет доступ ко всем функциям аренды активов.</span><span class="sxs-lookup"><span data-stu-id="efff2-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="efff2-116">Просмотр аренды</span><span class="sxs-lookup"><span data-stu-id="efff2-116">View Lease</span></span>     | <span data-ttu-id="efff2-117">Пользователи с этой ролью могут только просматривать записи аренды, расписания и выполнять отчеты.</span><span class="sxs-lookup"><span data-stu-id="efff2-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="efff2-118">Они не могут создавать новые аренды, изменять существующие аренды или создавать записи в журнале для аренды.</span><span class="sxs-lookup"><span data-stu-id="efff2-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="efff2-119">Роль предназначена для пользователей, которые только должны просматривать аренды, расписания аренд и проводки, происходящие по отношению к этим арендам.</span><span class="sxs-lookup"><span data-stu-id="efff2-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="efff2-120">Менеджер по аренде</span><span class="sxs-lookup"><span data-stu-id="efff2-120">Lease Clerk</span></span>    | <span data-ttu-id="efff2-121">Пользователи, имеющие эту роль, могут только создавать новые аренды.</span><span class="sxs-lookup"><span data-stu-id="efff2-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="efff2-122">Они не могут редактировать или удалять существующие аренды, просматривать расписания аренды или разносить записи журнала по аренде.</span><span class="sxs-lookup"><span data-stu-id="efff2-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="efff2-123">Эта роль предназначена для пользователей, обязанности которых заключаются в вводе данных.</span><span class="sxs-lookup"><span data-stu-id="efff2-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="efff2-124">Выполните следующие действия, чтобы назначить пользователей для ролей, которые используются в аренде активов.</span><span class="sxs-lookup"><span data-stu-id="efff2-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="efff2-125">Перейдите в раздел **Администрирование системы \> Контроль доступа \> Назначить пользователей ролям**.</span><span class="sxs-lookup"><span data-stu-id="efff2-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="efff2-126">Выберите роль **Обслуживание аренды**, **Менеджер по аренде** или **Просмотр аренды**, а затем выберите **Вручную назначить или исключить пользователей**.</span><span class="sxs-lookup"><span data-stu-id="efff2-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="efff2-127">Выберите пользователя, которого нужно назначить этой роли, а затем выберите **Назначить роли**.</span><span class="sxs-lookup"><span data-stu-id="efff2-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>
