---
title: Вы получаете ошибку при запуске встроенной подсистемы сводного планирования
description: При запуске встроенной подсистемы сводного планирования вы получаете сообщение об ошибке.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294165"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="46128-103">Вы получаете ошибку при запуске встроенной подсистемы сводного планирования</span><span class="sxs-lookup"><span data-stu-id="46128-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="46128-104">Код ошибки: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="46128-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="46128-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="46128-105">Symptoms</span></span>

<span data-ttu-id="46128-106">При запуске сводного планирования с помощью устаревшей подсистемы сводного планирования вы получаете следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="46128-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="46128-107">Это сообщение об ошибке выводится из-за того, что встроенный механизм сводного планирования использовался для сценариев, поддерживаемых оптимизацией планирования.</span><span class="sxs-lookup"><span data-stu-id="46128-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="46128-108">Сейчас следует выполнить миграцию на оптимизацию планирования, поскольку текущее встроенное сводное планирование будет устаревшим.</span><span class="sxs-lookup"><span data-stu-id="46128-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="46128-109">Обратите внимание, что выполнение этого сводного планирования успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="46128-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="46128-110">В случае, когда миграция имеет сильную зависимость от ожидающих функций, может быть запрошено исключение для продолжения использования встроенного механизма сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="46128-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="46128-111">Заполните следующую анкету, чтобы приступить к работе, и, если требуется, запросить исключение из миграции на оптимизацию планирования.</span><span class="sxs-lookup"><span data-stu-id="46128-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="46128-112">Миграция оптимизации планирования и анкета об исключениях</span><span class="sxs-lookup"><span data-stu-id="46128-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="46128-113">Причина</span><span class="sxs-lookup"><span data-stu-id="46128-113">Cause</span></span>

<span data-ttu-id="46128-114">Если вы используете планирование и не используете функции управления производством, следует рассмотреть возможность перехода на оптимизацию планирования.</span><span class="sxs-lookup"><span data-stu-id="46128-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="46128-115">Встроенная подсистема сводного планирования в настоящее время устаревает.</span><span class="sxs-lookup"><span data-stu-id="46128-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="46128-116">Поэтому, если вы хотите продолжать использовать ее без получения сообщения об ошибке, вы должны подать заявку на исключение от корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="46128-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="46128-117">Решение</span><span class="sxs-lookup"><span data-stu-id="46128-117">Resolution</span></span>

<span data-ttu-id="46128-118">Для получения дополнительной информации о том, как перейти к оптимизации планирования или как подать заявку на исключение, чтобы продолжать использовать устаревающую подсистему сводного планирования, см. [Миграция на оптимизацию планирования для сводного планирования](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span><span class="sxs-lookup"><span data-stu-id="46128-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
