---
title: Устранение неполадок в оптимизации планирования
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе с оптимизацией планирования.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c3dd0bf262f65aac2359c05ff954bdfbd294353f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435818"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="4111a-103">Устранение неполадок в оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="4111a-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4111a-104">В этом разделе описывается устранение общих проблем, которые могут встретиться при работе с оптимизацией планирования.</span><span class="sxs-lookup"><span data-stu-id="4111a-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="4111a-105">Установка надстройки оптимизации планирования не завершена</span><span class="sxs-lookup"><span data-stu-id="4111a-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="4111a-106">Оптимизация планирования требует включенной Lifecycle Services (LCS), среды с высокой степенью доступности уровня 2 или выше (а не среда OneBox) с версией Dynamics 365 Supply Chain Management 10.0.7 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="4111a-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="4111a-107">При попытке установить надстройку в среде OneBox установка не будет завершена.</span><span class="sxs-lookup"><span data-stu-id="4111a-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="4111a-108">**Исправление**: отмените установку и используйте среду с высокой степенью доступности, уровень 2 или более высокий (не среда OneBox).</span><span class="sxs-lookup"><span data-stu-id="4111a-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="4111a-109">Планирование пакетных заданий при включении оптимизации планирования не выполняется</span><span class="sxs-lookup"><span data-stu-id="4111a-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="4111a-110">При включении оптимизации планирования встроенный механизм сводного планирования автоматически отключается.</span><span class="sxs-lookup"><span data-stu-id="4111a-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="4111a-111">Пакетные задания сводного планирования, созданные для встроенного механизма планирования Supply Chain Management не будут выполняться, если они запускаются, пока оптимизация планирования включена.</span><span class="sxs-lookup"><span data-stu-id="4111a-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="4111a-112">Возможно появление сообщения об ошибке, такого как *Эта операция привела к включению режима сводного планирования, который не поддерживается при включении оптимизации планирования*.</span><span class="sxs-lookup"><span data-stu-id="4111a-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="4111a-113">**Исправление**: отменяет все пакетные задания сводного планирования, которые были созданы для встроенного механизма планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4111a-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="4111a-114">Результаты оптимизации планирования отличаются от предыдущих результатов</span><span class="sxs-lookup"><span data-stu-id="4111a-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="4111a-115">Оптимизация планирования отличается от структуры сводного планирования в некоторых областях.</span><span class="sxs-lookup"><span data-stu-id="4111a-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="4111a-116">Это также может быть вызвано ожидающими функциями.</span><span class="sxs-lookup"><span data-stu-id="4111a-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="4111a-117">**Исправление**: запустите анализ соответствия оптимизации планирования и затем проанализируйте результаты, ссылаясь на соответствующую документацию для понимания воздействия.</span><span class="sxs-lookup"><span data-stu-id="4111a-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="4111a-118">Дополнительные сведения см. в разделе [Анализ пригодности оптимизации планирования](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4111a-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a><span data-ttu-id="4111a-119">Сводное планирование не учитывает временные границы покрытия</span><span class="sxs-lookup"><span data-stu-id="4111a-119">Master planning doesn't respect the coverage time fence</span></span>

<span data-ttu-id="4111a-120">Это обусловлено ожидаемой функцией оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="4111a-120">This is caused by a pending feature for Planning Optimization.</span></span>

<span data-ttu-id="4111a-121">**Исправление**: до тех пор, пока не будет доступна ожидаемая функция, отфильтруйте или удалите спланированные заказы для удаления предложений по поставкам за пределами временной границы покрытия.</span><span class="sxs-lookup"><span data-stu-id="4111a-121">**Fix**: Until the pending feature is available, filter or delete planned orders to remove supply suggestions outside of the coverage time fence.</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="4111a-122">Невозможно включить оптимизацию планирования</span><span class="sxs-lookup"><span data-stu-id="4111a-122">Can't enable Planning Optimization</span></span>

<span data-ttu-id="4111a-123">**Статус подключения** должен быть **Подключено**, прежде чем можно будет настроить **использование оптимизации планирования** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="4111a-123">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="4111a-124">Дополнительные сведения см. в разделе [Начало работы с оптимизацией планирования](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="4111a-124">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="4111a-125">**Исправление**: Убедитесь, что надстройка оптимизации планирования была успешно установлена.</span><span class="sxs-lookup"><span data-stu-id="4111a-125">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="4111a-126">Во время CTP выводится сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="4111a-126">Error message is shown during CTP</span></span>

<span data-ttu-id="4111a-127">При попытке выполнить "доступно для заказа с учетом производства" (CTP) из заказа на продажу, если включена оптимизация планирования, будет выведено следующее сообщение об ошибке: *Эта операция запускает сводное планирование, которое не поддерживается, если активирована оптимизация планирования*.</span><span class="sxs-lookup"><span data-stu-id="4111a-127">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="4111a-128">Это связано с ожидаемой функцией, которая планируется как часть поддержки производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="4111a-128">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="4111a-129">**Исправление:** Избегайте расчетов CTP, если оптимизация планирования включена, пока не будет доступна поддержка CTP.</span><span class="sxs-lookup"><span data-stu-id="4111a-129">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4111a-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4111a-130">Additional resources</span></span>

[<span data-ttu-id="4111a-131">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="4111a-131">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="4111a-132">Анализ соответствия оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="4111a-132">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
