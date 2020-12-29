---
title: Удаленные или исключенные функции Lifecycle Services (LCS)
description: В этом разделе описываются возможности, который удалены или которые планируется удалить из Lifecycle Services (LCS) Microsoft Dynamics.
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: abf7a1a0a75ac3098efeeab3df65481999b69acc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687886"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="4586b-103">Удаленные или исключенные функции Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="4586b-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4586b-104">В этом разделе описываются возможности, который удалены или устарели для Lifecycle Services Microsoft Dynamics (LCS).</span><span class="sxs-lookup"><span data-stu-id="4586b-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="4586b-105">*Удаленная* функция больше недоступна в службе.</span><span class="sxs-lookup"><span data-stu-id="4586b-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="4586b-106">*Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.</span><span class="sxs-lookup"><span data-stu-id="4586b-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="4586b-107">Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании.</span><span class="sxs-lookup"><span data-stu-id="4586b-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="4586b-108">Объявления октября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="4586b-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="4586b-109">Блок-схемы в средстве моделирования бизнес-процессов</span><span class="sxs-lookup"><span data-stu-id="4586b-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="4586b-110"><strong>Причина устаревания/удаления</strong></span><span class="sxs-lookup"><span data-stu-id="4586b-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="4586b-111">Мы удаляем компонент блок-схем в средстве моделирования бизнес-процессов (BPM), поскольку устаревший дизайн вызвал малое использование.</span><span class="sxs-lookup"><span data-stu-id="4586b-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4586b-112"><strong>Заменена другой функцией?</strong></span><span class="sxs-lookup"><span data-stu-id="4586b-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="4586b-113">Нет</span><span class="sxs-lookup"><span data-stu-id="4586b-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4586b-114"><strong>Области действия</strong></span><span class="sxs-lookup"><span data-stu-id="4586b-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="4586b-115">Средство моделирования бизнес-процессов</span><span class="sxs-lookup"><span data-stu-id="4586b-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4586b-116"><strong>Состояние</strong></span><span class="sxs-lookup"><span data-stu-id="4586b-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="4586b-117">Устарело: компонент блок-схем в BPM, как ожидается, будет удален в 2020 году.</span><span class="sxs-lookup"><span data-stu-id="4586b-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="4586b-118">Следующие функции будут недоступны:</span><span class="sxs-lookup"><span data-stu-id="4586b-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="4586b-119">Все блок-схемы будут доступны только для чтения, и они недоступны для редактирования.</span><span class="sxs-lookup"><span data-stu-id="4586b-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="4586b-120">Свойства формы, связанные с действиями в блок-схеме, также будут недоступны.</span><span class="sxs-lookup"><span data-stu-id="4586b-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="4586b-121">Эти блок-схемы включают в себя как блок-схемы по умолчанию, которые автоматически создаются, так и настраиваемые блок-схемы, которые модифицируются на основе этих блок-схем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4586b-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="4586b-122">Шаги процесса будут доступны только для чтения, и они недоступны для редактирования.</span><span class="sxs-lookup"><span data-stu-id="4586b-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="4586b-123">Старая функция анализа соответствия/несоответствия будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="4586b-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="4586b-124">Таким образом, список несоответствий не будет автоматически создан или доступен для экспорта.</span><span class="sxs-lookup"><span data-stu-id="4586b-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="4586b-125"><strong>Примечание:</strong> эта функция ранее была удалена и заменена на интеграции Microsoft Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="4586b-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="4586b-126">История версий блок-схем будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="4586b-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
