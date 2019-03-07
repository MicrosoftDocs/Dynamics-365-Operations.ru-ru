---
title: Что нового и что изменилось в Dynamics 365 for Talent Core HR (16 октября 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7da597a682006cddb44ff9354813b07c15c1a449
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "305999"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-19-2018"></a><span data-ttu-id="9f39e-103">Что нового и что изменилось в Dynamics 365 for Talent Core HR (19 октября 2018 г.)</span><span class="sxs-lookup"><span data-stu-id="9f39e-103">What's new or changed in Dynamics 365 for Talent Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="9f39e-104">**Сборка 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="9f39e-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="9f39e-105">В этой теме описываются новые и измененные компоненты Core HR.</span><span class="sxs-lookup"><span data-stu-id="9f39e-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="9f39e-106">Разрешить руководителям обновлять запросы на отгулы</span><span class="sxs-lookup"><span data-stu-id="9f39e-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="9f39e-107">Запросы на отгулы сотрудников могут требовать обновления после их утверждения через workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="9f39e-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="9f39e-108">Во многих случаях менеджер делает эти обновления от имени сотрудника.</span><span class="sxs-lookup"><span data-stu-id="9f39e-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="9f39e-109">Эта новая функция позволяет менеджерам обновлять отгул или отменять запросы отгулов от имени своих сотрудников.</span><span class="sxs-lookup"><span data-stu-id="9f39e-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="9f39e-110">Эта возможность управляется параметром **Работать от имени**, который можно установить на странице **Параметры управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="9f39e-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="9f39e-111">Разрешить отделу кадров обновлять запросы на отгулы</span><span class="sxs-lookup"><span data-stu-id="9f39e-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="9f39e-112">Аналогично функции выше, запросы сотрудников на отгул может потребоваться обновить в отделе кадров после того как они были утверждены ранее через workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="9f39e-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="9f39e-113">Эта возможность позволяет пользователям отдела кадров обновлять запросы отгулов.</span><span class="sxs-lookup"><span data-stu-id="9f39e-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="9f39e-114">Возможность включается в рабочей области **Люди** и на странице **Работник** с помощью нового параметра **Просмотреть отгул**.</span><span class="sxs-lookup"><span data-stu-id="9f39e-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="9f39e-115">На этих страницах пользователи отдела кадров могут просматривать запросы и обновлять проводки отгулов, подобно тому как менеджеры могут выполнять эти действия.</span><span class="sxs-lookup"><span data-stu-id="9f39e-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="9f39e-116">Полномочия безопасности, которые контролируют доступ к этой функции, следующие:</span><span class="sxs-lookup"><span data-stu-id="9f39e-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="9f39e-117">Полномочия: ведение процессов отпусков и отсутствия для определенных работников.</span><span class="sxs-lookup"><span data-stu-id="9f39e-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="9f39e-118">Привилегия: ведение запросов на отпуск и отсутствие для всех работников.</span><span class="sxs-lookup"><span data-stu-id="9f39e-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="9f39e-119">Другие изменения</span><span class="sxs-lookup"><span data-stu-id="9f39e-119">Other changes</span></span>
<span data-ttu-id="9f39e-120">В данном выпуске были сделаны следующие обновления:</span><span class="sxs-lookup"><span data-stu-id="9f39e-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="9f39e-121">Изменения в действия приема на работу работника, чтобы они больше не "застревали" в состоянии **Workflow-процесс завершен**.</span><span class="sxs-lookup"><span data-stu-id="9f39e-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="9f39e-122">Теперь можно создать запись о приеме на работу, не указывая дату приема на работу.</span><span class="sxs-lookup"><span data-stu-id="9f39e-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="9f39e-123">Дата регистрации Dynamics 365 Talent для участия в курсах, отображается функцией самообслуживания сотрудников, теперь учитывает смещение часового пояса в этой дате.</span><span class="sxs-lookup"><span data-stu-id="9f39e-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="9f39e-124">Файлы Excel можно импортировать несколько раз без ошибок с помощью **Сущности сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="9f39e-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="9f39e-125">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="9f39e-125">Known issue</span></span>

- <span data-ttu-id="9f39e-126">**Проблема**: при добавлении нового вложения для работника кнопки **Создать** и **Изменить** неактивны.</span><span class="sxs-lookup"><span data-stu-id="9f39e-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="9f39e-127">**Временное решение:** перед открытием страницы вложения убедитесь, что информационные панели на странице **Рабочий** закрыты.</span><span class="sxs-lookup"><span data-stu-id="9f39e-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="9f39e-128">Если информационные панели закрыты при загрузке страницы **Работник**, кнопки вложений будут активны.</span><span class="sxs-lookup"><span data-stu-id="9f39e-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="9f39e-129">(Эта проблема будет исправлена в следующем обновлении платформы.)</span><span class="sxs-lookup"><span data-stu-id="9f39e-129">(This issue will be fixed in the next platform update.)</span></span>
