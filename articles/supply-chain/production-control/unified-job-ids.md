---
title: Единая номерная серия для кодов заданий
description: Эта функция предоставляет одну унифицированную номерную серию, которая создает коды заданий для модулей контроля производства, управления производством, а также времени и посещаемости.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824950"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="657c6-103">Единая номерная серия для кодов заданий</span><span class="sxs-lookup"><span data-stu-id="657c6-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="657c6-104">Эта функция предоставляет одну унифицированную номерную серию, которая создает коды заданий для модулей контроля производства, управления производством, а также времени и посещаемости.</span><span class="sxs-lookup"><span data-stu-id="657c6-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="657c6-105">Ранее была возможность выбрать другую номерную серию для каждого из этих модулей, что может привести к конфликтующим кодам заданий, если две или более из этих последовательностей используют одинаковый формат.</span><span class="sxs-lookup"><span data-stu-id="657c6-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="657c6-106">Такой конфликт может привести к повреждению данных.</span><span class="sxs-lookup"><span data-stu-id="657c6-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="657c6-107">Включите эту функцию для своей системы</span><span class="sxs-lookup"><span data-stu-id="657c6-107">Turn on this feature for your system</span></span>

<span data-ttu-id="657c6-108">Если ваша система еще не содержит функцию, описанную в этом разделе, перейдите в [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) и включите функцию *Унифицированная номерная серия для кодов заданий*.</span><span class="sxs-lookup"><span data-stu-id="657c6-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="657c6-109">Настройка унифицированной номерной серии для кодов заданий</span><span class="sxs-lookup"><span data-stu-id="657c6-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="657c6-110">После включения этой функции существующие параметры номерной серии **Код задания**, расположенные на страницах параметров для модулей контроля производства, управления производством и времени и посещаемости, будут устаревшими и будет добавлено новое поле **Унифицированный код задания**.</span><span class="sxs-lookup"><span data-stu-id="657c6-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="657c6-111">Значение **Унифицированный код задания** совместно используется всеми тремя модулями, что гарантирует, что все модули ссылаются на одну и ту же номерную серию.</span><span class="sxs-lookup"><span data-stu-id="657c6-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="657c6-112">Таким образом, коды заданий будут уникальными во всех трех модулях, и конфликт никогда не будет происходить.</span><span class="sxs-lookup"><span data-stu-id="657c6-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="657c6-113">Чтобы настроить унифицированную номерную серию для кодов заданий:</span><span class="sxs-lookup"><span data-stu-id="657c6-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="657c6-114">Включите функцию, как описано в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="657c6-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="657c6-115">Либо определите номерную серию, которую хотите использовать для унифицированных кодов задания, либо создайте новую.</span><span class="sxs-lookup"><span data-stu-id="657c6-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="657c6-116">Дополнительные сведения см. в разделе [Обзор номерных серий](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="657c6-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="657c6-117">Перейдите на страницу **Параметры управления производством**, **Параметры модуля "Управление производством"** или **Параметры учета посещаемости и времени присутствия**.</span><span class="sxs-lookup"><span data-stu-id="657c6-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="657c6-118">Не важно, которую из них вы выберете, потому что при задании этого параметра на любой из этих страниц все остальные страницы обновятся автоматически.</span><span class="sxs-lookup"><span data-stu-id="657c6-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="657c6-119">Откройте вкладку **Номерные серии** на выбранной странице параметров.</span><span class="sxs-lookup"><span data-stu-id="657c6-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="657c6-120">Назначьте **Код номерной серии**, который вы идентифицировали ранее, строке **Унифицированные коды заданий** сетки.</span><span class="sxs-lookup"><span data-stu-id="657c6-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
