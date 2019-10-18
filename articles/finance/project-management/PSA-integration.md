---
title: Обзор Project Service Automation
description: В этом разделе содержится информация о решении интеграции Dynamics 365 Project Service Automation с Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250561"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="c1a12-103">Обзор Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c1a12-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c1a12-104">Решение интеграции Project Service Automation с Finance использует интеграцию данных для синхронизации данных между экземплярами Dynamics 365 Finance и Dynamics 365 Project Service Automation с помощью Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c1a12-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="c1a12-105">Шаблоны интеграции, доступные с функцией интеграции данных, позволяют передавать данные по проектам, контрактам проекта, строкам контракта проекта, этапам строк контракта проекта, задачам проекта, категориям транзакции расходов, оценкам часов и оценкам расходов из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="c1a12-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c1a12-106">При использовании версии 7.3.0 необходимо установить KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="c1a12-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="c1a12-107">После этого можно будет интегрировать проекты с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="c1a12-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="c1a12-108">Если при использовании версии 7.3.0 вы переносите проводки по сборам из Project Service Automation, чтобы включить эти расходы в накладную проекта необходимо установить KB 4345320.</span><span class="sxs-lookup"><span data-stu-id="c1a12-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="c1a12-109">Если вы используете версию 8.0, вы можете использовать интеграция задач проекта, категории транзакции расходов, оценки часов, оценки затрат и блокировку функциональности.</span><span class="sxs-lookup"><span data-stu-id="c1a12-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="c1a12-110">При использовании версии 8.0.1 или новее можно выполнить синхронизацию фактических данных.</span><span class="sxs-lookup"><span data-stu-id="c1a12-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="c1a12-111">Перед интеграцией Project Service Automation с Finance необходимо настроить параметры интеграции Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c1a12-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="c1a12-112">Для получения дополнительных сведений см. раздел [Параметры интеграции Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c1a12-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="c1a12-113">Эта интеграция обеспечивает прямую синхронизацию в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="c1a12-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="c1a12-114">Поддержка контрактов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="c1a12-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a12-115">Создание проектов в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="c1a12-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a12-116">Поддержка строк контрактов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="c1a12-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a12-117">Поддержка промежуточных этапов строк контрактов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="c1a12-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a12-118">Поддержка задач по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="c1a12-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a12-119">Поддержка категорий транзакции расходов в Finance и их синхронизация непосредственно из Finance в Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c1a12-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="c1a12-120">Создание оценок часов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="c1a12-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a12-121">Создание оценок расходов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="c1a12-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a12-122">Создание фактических данных проекта по времени, расходам и сборам в Project Service Automation и создание проводок по проекту в журнале интеграции Project Service Automation, чтобы из можно было разнести в Finance.</span><span class="sxs-lookup"><span data-stu-id="c1a12-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="c1a12-123">Синхронизация данных</span><span class="sxs-lookup"><span data-stu-id="c1a12-123">Data synchronization</span></span>

<span data-ttu-id="c1a12-124">На следующем рисунке показано, как данные синхронизируются в рамках интеграции между Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="c1a12-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="c1a12-125">Не все шаблоны в данный момент доступны.</span><span class="sxs-lookup"><span data-stu-id="c1a12-125">Not all templates are currently available.</span></span> <span data-ttu-id="c1a12-126">Шаблоны освобождаются сразу после их завершения.</span><span class="sxs-lookup"><span data-stu-id="c1a12-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="c1a12-127">[![Параметры интеграции Project Service Automation с Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="c1a12-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="c1a12-128">Системные требования для Finance</span><span class="sxs-lookup"><span data-stu-id="c1a12-128">System requirements for Finance</span></span>

<span data-ttu-id="c1a12-129">Чтобы использовать решение интеграции Project Service Automation в Finance, необходимо установить , Enterprise edition 7.3 с обновлением платформы Platform update 12 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c1a12-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="c1a12-130">Требования к системе для Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c1a12-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="c1a12-131">Чтобы использовать решение интеграции Project Service Automation с Finance, необходимо установить следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="c1a12-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="c1a12-132">Dynamics 365 Project Service Automation версии 9.0.0.0 или более новая версия</span><span class="sxs-lookup"><span data-stu-id="c1a12-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="c1a12-133">Решение "Перспективный клиент в наличные деньги" Dynamics 365 Sales, версия 1.14.0.0 (v14) или выше</span><span class="sxs-lookup"><span data-stu-id="c1a12-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="c1a12-134">Решение для интеграции Project Service Automation с Finance для Dynamics 365 Project Service Automation версии 1.0.0.0 или новее</span><span class="sxs-lookup"><span data-stu-id="c1a12-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="c1a12-135">Установите решение интеграции Project Service Automation с Finance в вашем экземпляре Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c1a12-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="c1a12-136">Загрузите решение интеграции Project Service Automation с Finance из [центра загрузки Майкрософт](https://www.microsoft.com/download/details.aspx?id=57016) и следуйте указаниям, включенным в решение.</span><span class="sxs-lookup"><span data-stu-id="c1a12-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
