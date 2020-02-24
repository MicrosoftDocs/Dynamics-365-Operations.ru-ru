---
title: Удаленные или исключенные функции Lifecycle Services (LCS)
description: В этом разделе описываются возможности, который удалены или которые планируется удалить из Lifecycle Services (LCS) Microsoft Dynamics.
author: AngelMarshall
manager: AnnBe
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 96ecd040ef8661765c0a3861d8e07fee3c241161
ms.sourcegitcommit: fb7d0efd97754f1ae0b5aa765d0eeb3f57b8078f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027988"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="4dfff-103">Удаленные или исключенные функции Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="4dfff-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4dfff-104">В этом разделе описываются возможности, который удалены или устарели для Lifecycle Services Microsoft Dynamics (LCS).</span><span class="sxs-lookup"><span data-stu-id="4dfff-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="4dfff-105">*Удаленная* функция больше недоступна в службе.</span><span class="sxs-lookup"><span data-stu-id="4dfff-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="4dfff-106">*Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.</span><span class="sxs-lookup"><span data-stu-id="4dfff-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="4dfff-107">Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании.</span><span class="sxs-lookup"><span data-stu-id="4dfff-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="4dfff-108">Объявления октября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="4dfff-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="4dfff-109">Блок-схемы в средстве моделирования бизнес-процессов</span><span class="sxs-lookup"><span data-stu-id="4dfff-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="4dfff-110"><strong>Причина устаревания/удаления</strong></span><span class="sxs-lookup"><span data-stu-id="4dfff-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="4dfff-111">Мы удаляем компонент блок-схем в средстве моделирования бизнес-процессов (BPM), поскольку устаревший дизайн вызвал малое использование.</span><span class="sxs-lookup"><span data-stu-id="4dfff-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4dfff-112"><strong>Заменена другой функцией?</strong></span><span class="sxs-lookup"><span data-stu-id="4dfff-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="4dfff-113">Нет</span><span class="sxs-lookup"><span data-stu-id="4dfff-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4dfff-114"><strong>Области действия</strong></span><span class="sxs-lookup"><span data-stu-id="4dfff-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="4dfff-115">Средство моделирования бизнес-процессов</span><span class="sxs-lookup"><span data-stu-id="4dfff-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4dfff-116"><strong>Состояние</strong></span><span class="sxs-lookup"><span data-stu-id="4dfff-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="4dfff-117">Устарело: компонент блок-схем в BPM, как ожидается, будет удален в 2020 году.</span><span class="sxs-lookup"><span data-stu-id="4dfff-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="4dfff-118">Следующие функции будут удалены:</span><span class="sxs-lookup"><span data-stu-id="4dfff-118">The following functionality will be removed:</span></span>
<ul>
<li><span data-ttu-id="4dfff-119">Существующие блок-схемы будут недоступны для просмотра и редактирования.</span><span class="sxs-lookup"><span data-stu-id="4dfff-119">Existing flowcharts will be unavailable for viewing or editing.</span></span> <span data-ttu-id="4dfff-120">Свойства формы, связанные с действиями блок-схем, также будут недоступны, так как вся вкладка <strong>Блок-схема</strong> будет удалена.</span><span class="sxs-lookup"><span data-stu-id="4dfff-120">The shape properties that are associated with flowchart activities will also be unavailable, because the whole <strong>Flowchart</strong> tab will be removed.</span></span> <span data-ttu-id="4dfff-121">Эти блок-схемы включают в себя как блок-схемы по умолчанию, которые автоматически создаются, так и настраиваемые блок-схемы, которые модифицируются на основе этих блок-схем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4dfff-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="4dfff-122">Старая функция анализа соответствия/несоответствия будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="4dfff-122">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="4dfff-123">Таким образом, список несоответствий не будет автоматически создан или доступен для экспорта.</span><span class="sxs-lookup"><span data-stu-id="4dfff-123">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="4dfff-124"><strong>Примечание:</strong> эта функция ранее была удалена и заменена на интеграции Microsoft Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="4dfff-124"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="4dfff-125">История версий блок-схем будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="4dfff-125">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
