---
title: Project Service Automation
description: "Это решение использует интеграцию данных для синхронизации данных между экземплярами Microsoft Dynamics 365 for Finance and Operations, и Microsoft Dynamics 365 for Project Service Automation с помощью Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: ru-ru
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="18db2-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="18db2-103">Project Service Automation</span></span>

<span data-ttu-id="18db2-104">Решение Project Service Automation в Finance and Operations integration использует интеграцию данных для синхронизации данных между экземплярами Microsoft Dynamics 365 for Finance and Operations и Microsoft Dynamics 365 for Project Service Automation с помощью Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="18db2-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="18db2-105">Шаблоны интеграции, доступные с функцией интеграции данных, позволяют передавать данные по проектам, контрактам проекта, строкам контракта проекта, этапам строк контракта проекта, задачам проекта, категориям транзакции расходов, оценкам часов и оценкам расходов из Project Service Automation в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18db2-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="18db2-106">При использовании Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, необходимо установить пакеты обновления KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="18db2-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="18db2-107">Это позволит интегрировать проекты с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="18db2-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="18db2-108">Если вы используете Dynamics 365 для Finance and Operations версии 8.0, вы можете использовать интеграция задач проекта, категории транзакции расходов, оценки часов, оценки затрат и блокировку функциональности.</span><span class="sxs-lookup"><span data-stu-id="18db2-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="18db2-109">При использовании Dynamics 365 for Finance and Operations версии 8.0.1 можно выполнить синхронизацию фактических данных.</span><span class="sxs-lookup"><span data-stu-id="18db2-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="18db2-110">При использовании Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, после установки обновлений КБ 4132657 и 4132660 КБ, можно использовать шаблоны для интеграции задачи проекта, категорий транзакций расходов, оценок часов, оценок расходов и фактических данных и для настройки функции блокировки.</span><span class="sxs-lookup"><span data-stu-id="18db2-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="18db2-111">Если необходимо сбросить распределения по бухгалтерским счетам, рекомендуется также установить КБ 4131710.</span><span class="sxs-lookup"><span data-stu-id="18db2-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="18db2-112">Перед интеграцией Project Service Automation with Finance and Operations необходимо конфигурировать параметры интеграции Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="18db2-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="18db2-113">Для получения дополнительных сведений см. параметры интеграции Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="18db2-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="18db2-114">Эта интеграция обеспечивает прямую синхронизацию в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="18db2-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="18db2-115">Поддержка контрактов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18db2-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="18db2-116">Создание проектов в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18db2-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="18db2-117">Поддержка строк контракта по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18db2-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="18db2-118">Поддержка этапов строк контракта по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18db2-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="18db2-119">Поддержка задач по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18db2-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="18db2-120">Поддержка категорий транзакции расходов в Finance and Operations и их синхронизация непосредственно из Finance and Operations в Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="18db2-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="18db2-121">Создание оценок часов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18db2-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="18db2-122">Создание оценок расходов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18db2-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="18db2-123">Синхронизация данных</span><span class="sxs-lookup"><span data-stu-id="18db2-123">Data synchronization</span></span>
<span data-ttu-id="18db2-124">На следующем рисунке показано, как данные синхронизируются в рамках интеграции между Project Service Automation и Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18db2-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="18db2-125">Не все шаблоны в данный момент доступны.</span><span class="sxs-lookup"><span data-stu-id="18db2-125">Not all templates are currently available.</span></span> <span data-ttu-id="18db2-126">Шаблоны освобождаются сразу после их завершения.</span><span class="sxs-lookup"><span data-stu-id="18db2-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="18db2-127">[![Интеграция Project Service Automation с Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="18db2-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="18db2-128">Системные требования для Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18db2-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="18db2-129">Чтобы использовать решение интеграции Project Service Automation в Finance and Operations, необходимо установить Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 с обновлениями платформы 12 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="18db2-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="18db2-130">Требования к системе для Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="18db2-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="18db2-131">Чтобы использовать решение интеграции Project Service Automation в Finance and Operations необходимо установить следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="18db2-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="18db2-132">Microsoft Dynamics 365 for Project Service Automation версии 9.0.0.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="18db2-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="18db2-133">Решение "Перспективный клиент в наличные деньги" Dynamics 365 for Sales, версия 1.14.0.0 (v14) или выше.</span><span class="sxs-lookup"><span data-stu-id="18db2-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="18db2-134">Решение Project Service Automation в Operations для Dynamics 365 for Project Service Automation версии 1.0.0.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="18db2-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="18db2-135">Установите решение интеграции Project Service Automation в Finance and Operations в вашем экземпляре Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="18db2-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



