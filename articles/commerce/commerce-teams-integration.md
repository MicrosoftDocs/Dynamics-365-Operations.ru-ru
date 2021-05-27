---
title: Обзор интеграции Dynamics 365 Commerce и Microsoft Teams
description: В этой теме представлен обзор интеграции Microsoft Dynamics 365 Commerce и Microsoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c22af9bf76818dd682b4147c3677cd1715e4cbf8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021997"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="239fb-103">Обзор интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="239fb-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="239fb-104">В этой теме представлен обзор интеграции Microsoft Dynamics 365 Commerce и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="239fb-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="239fb-105">Dynamics 365 Commerce интегрируется с Teams, чтобы помочь клиентам и их сотрудникам повысить производительность за счет синхронизации управления задачами между двумя приложениями.</span><span class="sxs-lookup"><span data-stu-id="239fb-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="239fb-106">Бесшовное управление задачами, которое предоставляет интеграция Commerce и Teams, позволяет менеджерам магазинов и сотрудникам создавать списки задач, назначать задачи нескольким магазинам и отслеживать статус задач по магазинам из любого из этих приложений.</span><span class="sxs-lookup"><span data-stu-id="239fb-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="239fb-107">Интеграция Commerce и Teams доступна в выпуске Commerce версии 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="239fb-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="239fb-108">Ключевые возможности</span><span class="sxs-lookup"><span data-stu-id="239fb-108">Key features</span></span>

<span data-ttu-id="239fb-109">Вот некоторые из основных функций, обеспечиваемых интеграцией Commerce и Microsoft Teams:</span><span class="sxs-lookup"><span data-stu-id="239fb-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="239fb-110">Подготовьте Teams, используя хорошо определенную информацию из Commerce, такую как организационная структура и сведения о магазинах, работниках, разрешениях и контексте бизнеса.</span><span class="sxs-lookup"><span data-stu-id="239fb-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="239fb-111">Без труда синхронизируйте текущие изменения (например, добавление новых магазинов или приемов новых сотрудников) между Commerce и Teams, но сохраняйте Commerce в качестве основного источника данных организационной структуры.</span><span class="sxs-lookup"><span data-stu-id="239fb-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="239fb-112">Интеграция управления задачами между Commerce и Teams помогает работникам магазинов, менеджерам магазинов, региональным менеджерам и менеджерам по взаимодействию управлять задачами из любого из этих приложений.</span><span class="sxs-lookup"><span data-stu-id="239fb-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="239fb-113">Необходимые условия для использования функций интеграции</span><span class="sxs-lookup"><span data-stu-id="239fb-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="239fb-114">Прежде чем можно будет приступить к использованию функций интеграции Microsoft Teams, должны быть выполнены следующие условия:</span><span class="sxs-lookup"><span data-stu-id="239fb-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="239fb-115">Стандартная лицензия Microsoft 365 бизнес (Эта лицензия содержит Teams.)</span><span class="sxs-lookup"><span data-stu-id="239fb-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="239fb-116">Учетные записи Azure Active Directory (Azure AD) для всех менеджеров и работников магазинов</span><span class="sxs-lookup"><span data-stu-id="239fb-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="239fb-117">Системы POS-терминалов, настроенные с проверкой подлинности Azure AD</span><span class="sxs-lookup"><span data-stu-id="239fb-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="239fb-118">Концептуальная архитектура</span><span class="sxs-lookup"><span data-stu-id="239fb-118">Conceptual architecture</span></span>

<span data-ttu-id="239fb-119">На следующем рисунке показана концептуальная архитектура интеграции Dynamics 365 Commerce и Microsoft Teams, в качестве примера используется магазин в Сан-Франциско.</span><span class="sxs-lookup"><span data-stu-id="239fb-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="239fb-120">Teams и приложение POS-терминала Commerce используют Microsoft Planner в качестве репозитория, чтобы задачи, опубликованные из Teams, отображались в приложении POS-терминала, а задачи, созданные менеджером магазина в приложении POS-терминала, были представлены в Teams, что приводит к бесшовному управлению задачами между приложениями.</span><span class="sxs-lookup"><span data-stu-id="239fb-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Архитектура интеграции Commerce и Teams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="239fb-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="239fb-122">Additional resources</span></span>

[<span data-ttu-id="239fb-123">Включение интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="239fb-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="239fb-124">Подготовка Microsoft Teams из Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="239fb-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="239fb-125">Синхронизация управления задачами между Microsoft Teams и Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="239fb-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="239fb-126">Управление ролями пользователей в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="239fb-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="239fb-127">Сопоставление магазинов и рабочих групп, если имеются готовые рабочие группы в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="239fb-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="239fb-128">Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="239fb-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
