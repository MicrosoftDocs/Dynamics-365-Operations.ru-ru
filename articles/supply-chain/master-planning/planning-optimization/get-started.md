---
title: Начало работы с оптимизацией планирования
description: Этот раздел описывает начало работы с функциями оптимизации планирования.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774035"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="57a14-103">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="57a14-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="57a14-104">Функции оптимизации планирования сейчас не поддерживают все возможности, доступные в механизме планирования, который встроен в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="57a14-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="57a14-105">Таким образом, важно оценить, будет ли набор функций, доступный в данный момент в оптимизации планирования, удовлетворять вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="57a14-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="57a14-106">По умолчанию функции оптимизации планирования не включены в Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="57a14-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="57a14-107">Таким образом, имеется возможность выполнить оценку до включения.</span><span class="sxs-lookup"><span data-stu-id="57a14-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="57a14-108">В конечном итоге, оптимизация планирования заменит существующий встроенный механизм планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="57a14-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="57a14-109">Перед включением оптимизации планирования настоятельно рекомендуется оценить ее пригодность по анализу пригодности оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="57a14-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="57a14-110">Дополнительные сведения см. в разделе [Анализ пригодности оптимизации планирования](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="57a14-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="57a14-111">Лицензирование</span><span class="sxs-lookup"><span data-stu-id="57a14-111">Licensing</span></span>

<span data-ttu-id="57a14-112">Если вы можете запустить сводное планирование, используя текущую лицензию, вам не придется покупать дополнительную лицензию для начала использования оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="57a14-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="57a14-113">Установка надстройки</span><span class="sxs-lookup"><span data-stu-id="57a14-113">Install the add-in</span></span>

<span data-ttu-id="57a14-114">Для использования оптимизации планирования установите надстройку оптимизации планирования для Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="57a14-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="57a14-115">Вы можете получить доступ к надстройке из проекта LCS и включить функцию оптимизации планирования из пользовательского интерфейса Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="57a14-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="57a14-116">Выполните вход в LCS и откройте нужную среду.</span><span class="sxs-lookup"><span data-stu-id="57a14-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="57a14-117">Перейдите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="57a14-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="57a14-118">Выберите **Поддержка** или перейдите на экспресс-вкладку **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="57a14-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="57a14-119">Выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="57a14-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="57a14-120">Выберите **Оптимизация планирования**.</span><span class="sxs-lookup"><span data-stu-id="57a14-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="57a14-121">Следуйте указаниям руководства по установке и примите условия и положения.</span><span class="sxs-lookup"><span data-stu-id="57a14-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="57a14-122">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="57a14-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="57a14-123">Интеграция оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="57a14-123">Planning Optimization integration</span></span>

<span data-ttu-id="57a14-124">Чтобы настроить, следует ли использовать надстройку оптимизации планирования для сводного планирования, перейдите **Сводное планирование** \> **Настройка** \> **Интеграция оптимизации планирования** \> **Параметры интеграции**.</span><span class="sxs-lookup"><span data-stu-id="57a14-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="57a14-125">Статус подключения</span><span class="sxs-lookup"><span data-stu-id="57a14-125">Connection status</span></span>

<span data-ttu-id="57a14-126">Состояние подключения показывает текущий статус подключения между Supply Chain Management и службой оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="57a14-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="57a14-127">В следующей таблице показаны возможные значения.</span><span class="sxs-lookup"><span data-stu-id="57a14-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="57a14-128">Статус подключения</span><span class="sxs-lookup"><span data-stu-id="57a14-128">Connection status</span></span> | <span data-ttu-id="57a14-129">Описание</span><span class="sxs-lookup"><span data-stu-id="57a14-129">Description</span></span> | <span data-ttu-id="57a14-130">Можно ли использовать оптимизацию планирования?</span><span class="sxs-lookup"><span data-stu-id="57a14-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="57a14-131">Подключено</span><span class="sxs-lookup"><span data-stu-id="57a14-131">Connected</span></span> | <span data-ttu-id="57a14-132">Между службой оптимизации планирования и Supply Chain Management было установлено подключение.</span><span class="sxs-lookup"><span data-stu-id="57a14-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="57a14-133">Да</span><span class="sxs-lookup"><span data-stu-id="57a14-133">Yes</span></span> |
| <span data-ttu-id="57a14-134">Включение подключения</span><span class="sxs-lookup"><span data-stu-id="57a14-134">Enabling connection</span></span> | <span data-ttu-id="57a14-135">В настоящее время выполняется запрос на включение подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="57a14-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="57a14-136">Нет</span><span class="sxs-lookup"><span data-stu-id="57a14-136">No</span></span> |
| <span data-ttu-id="57a14-137">Отключено</span><span class="sxs-lookup"><span data-stu-id="57a14-137">Disconnected</span></span> | <span data-ttu-id="57a14-138">Нет подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="57a14-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="57a14-139">Подключение можно включить из LCS, как описано ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="57a14-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="57a14-140">Нет</span><span class="sxs-lookup"><span data-stu-id="57a14-140">No</span></span> |
| <span data-ttu-id="57a14-141">Отключение подключения</span><span class="sxs-lookup"><span data-stu-id="57a14-141">Disabling connection</span></span> | <span data-ttu-id="57a14-142">В настоящее время выполняется запрос на отключение подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="57a14-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="57a14-143">Нет</span><span class="sxs-lookup"><span data-stu-id="57a14-143">No</span></span> |
| <span data-ttu-id="57a14-144">Получение статуса</span><span class="sxs-lookup"><span data-stu-id="57a14-144">Getting status</span></span> | <span data-ttu-id="57a14-145">Система ожидает сведения о состоянии службы оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="57a14-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="57a14-146">Нет</span><span class="sxs-lookup"><span data-stu-id="57a14-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="57a14-147">Параметр "Использовать оптимизацию планирования"</span><span class="sxs-lookup"><span data-stu-id="57a14-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="57a14-148">Параметр **Использовать оптимизацию планирования** определяет, какой механизм планирования используется для сводного планирования:</span><span class="sxs-lookup"><span data-stu-id="57a14-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="57a14-149">**Да** — оптимизация планирования используется для сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="57a14-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="57a14-150">**Нет** — для сводного планирования используется встроенный механизм планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="57a14-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="57a14-151">Если существующие пакетные задания планирования, созданные для встроенного механизма планирования Supply Chain Management, запускаются, а параметр **Использовать оптимизацию планирования** задан как **Да**, эти задания не будут работать</span><span class="sxs-lookup"><span data-stu-id="57a14-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="57a14-152">Интеграции с настройкой</span><span class="sxs-lookup"><span data-stu-id="57a14-152">Integration with the setup</span></span>

<span data-ttu-id="57a14-153">Если предварительный просмотр оптимизации планирования включен, сводное планирование выполняется с помощью надстройки оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="57a14-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="57a14-154">В этом случае затронуты результаты и функции сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="57a14-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="57a14-155">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="57a14-155">Related resources</span></span>

[<span data-ttu-id="57a14-156">Условия для предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="57a14-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="57a14-157">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="57a14-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="57a14-158">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="57a14-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="57a14-159">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="57a14-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="57a14-160">Применение фильтров к плану</span><span class="sxs-lookup"><span data-stu-id="57a14-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="57a14-161">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="57a14-161">Cancel a planning job</span></span>](cancel-planning-job.md)
