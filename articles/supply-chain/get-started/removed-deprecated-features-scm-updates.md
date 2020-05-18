---
title: Удаленные или устаревшие функции Dynamics 365 Supply Chain Management
description: В этом разделе описываются возможности, который удалены или которые планируется удалить в Dynamics 365 Supply Chain Management.
author: kamaybac
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7502cd16129431d41d152508fb3b49ff85a5a9f8
ms.sourcegitcommit: f1db998ecfccca660eb15cc2739b12c8463fa54d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331256"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="e3b58-103">Удаленные или устаревшие функции Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e3b58-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3b58-104">Этот раздел будет обновлен в соответствии с документированием новых удаленных или устаревших функций для Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e3b58-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="e3b58-105">*Удаленная* функция больше недоступна в продукте.</span><span class="sxs-lookup"><span data-stu-id="e3b58-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="e3b58-106">*Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.</span><span class="sxs-lookup"><span data-stu-id="e3b58-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="e3b58-107">Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании.</span><span class="sxs-lookup"><span data-stu-id="e3b58-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="e3b58-108">Подробные сведения об объектах в приложениях Finance and Operations можно найти в документе [Технический справочник по отчетам](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="e3b58-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="e3b58-109">Можно сравнить различные версии этих отчетов, чтобы получить сведения об объектах, которые были изменены или были исключены в каждой версии приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e3b58-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="e3b58-110">Функции, удаленные или устаревшие в выпуске Supply Chain Management 10.0.11</span><span class="sxs-lookup"><span data-stu-id="e3b58-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="e3b58-111">Для сценариев распределения используйте встроенный механизм сводного планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e3b58-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="e3b58-112">**Причина устаревания/удаления**</span><span class="sxs-lookup"><span data-stu-id="e3b58-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="e3b58-113">Для повышения производительности и минимизации нагрузки на базу данных SQL во время сводного планирования, встроенный механизм сводного планирования Supply Chain Management заменяется оптимизацией планирования.</span><span class="sxs-lookup"><span data-stu-id="e3b58-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="e3b58-114">Оптимизация планирования позволяет быстро планировать даже в рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="e3b58-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="e3b58-115">Это позволяет планировщикам быстро реагировать на изменения в параметрах спроса или планирования.</span><span class="sxs-lookup"><span data-stu-id="e3b58-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="e3b58-116">**Заменена другой функцией?**</span><span class="sxs-lookup"><span data-stu-id="e3b58-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="e3b58-117">Да, оптимизация планирования заменит существующий встроенный механизм сводного планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e3b58-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="e3b58-118">**Затрагиваемые области продукта**</span><span class="sxs-lookup"><span data-stu-id="e3b58-118">**Product areas affected**</span></span>         | <span data-ttu-id="e3b58-119">Supply Chain Management — сводное планирование</span><span class="sxs-lookup"><span data-stu-id="e3b58-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="e3b58-120">**Вариант развертывания**</span><span class="sxs-lookup"><span data-stu-id="e3b58-120">**Deployment option**</span></span>              | <span data-ttu-id="e3b58-121">Только облако.</span><span class="sxs-lookup"><span data-stu-id="e3b58-121">Cloud only.</span></span> <span data-ttu-id="e3b58-122">Оптимизация планирования не поддерживается в локальном развертывании.</span><span class="sxs-lookup"><span data-stu-id="e3b58-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="e3b58-123">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e3b58-123">**Status**</span></span>                         | <span data-ttu-id="e3b58-124">Устарело.</span><span class="sxs-lookup"><span data-stu-id="e3b58-124">Deprecated.</span></span> <span data-ttu-id="e3b58-125">В апреле 2021 сценарии распределения больше не будут поддерживаться встроенным механизмом сводного планирования Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e3b58-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="e3b58-126">Для сценариев распределения клиенты должны использовать оптимизацию планирования при расчетах сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="e3b58-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="e3b58-127">Дополнительные сведения см. в разделе [Документация оптимизации планирования](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="e3b58-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="e3b58-128">Клиенты с локальным развертыванием Dynamics 365 Supply Chain Management могут и дальше использовать механизм сводного планирования Supply Chain Management для сценариев распределения после апреля 2021 года.</span><span class="sxs-lookup"><span data-stu-id="e3b58-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="e3b58-129">Однако эти функции больше не будут улучшаться.</span><span class="sxs-lookup"><span data-stu-id="e3b58-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="e3b58-130">Предыдущие объявления об удаленных или устаревших функциях</span><span class="sxs-lookup"><span data-stu-id="e3b58-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="e3b58-131">Для получения дополнительных сведений о функциях, которые были удалены или устарели в предыдущих выпусках, см [Удаленные или устаревшие функции в предыдущих выпусках](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="e3b58-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
