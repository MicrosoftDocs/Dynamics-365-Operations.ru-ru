---
title: Начало работы с оптимизацией планирования
description: Этот раздел описывает начало работы с функциями оптимизации планирования.
author: ChristianRytt
manager: tfehr
ms.date: 02/10/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4f9124e824a0b6d5035b2567cb19c2c494390d55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213523"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="46683-103">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="46683-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46683-104">Функции оптимизации планирования сейчас не поддерживают все возможности, доступные в механизме планирования, который встроен в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="46683-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="46683-105">Таким образом, важно оценить, будет ли набор функций, доступный в данный момент в оптимизации планирования, удовлетворять вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="46683-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="46683-106">По умолчанию функции оптимизации планирования не включены в Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="46683-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="46683-107">Таким образом, имеется возможность выполнить оценку до включения.</span><span class="sxs-lookup"><span data-stu-id="46683-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="46683-108">В конечном итоге, оптимизация планирования заменит существующий встроенный механизм планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="46683-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="46683-109">Перед включением оптимизации планирования настоятельно рекомендуется оценить ее пригодность по анализу пригодности оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="46683-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="46683-110">Дополнительные сведения см. в разделе [Анализ пригодности оптимизации планирования](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="46683-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="46683-111">Лицензирование</span><span class="sxs-lookup"><span data-stu-id="46683-111">Licensing</span></span>

<span data-ttu-id="46683-112">Если вы можете запустить сводное планирование, используя текущую лицензию, вам не придется покупать дополнительную лицензию для начала использования оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="46683-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="46683-113">Установка надстройки</span><span class="sxs-lookup"><span data-stu-id="46683-113">Install the add-in</span></span>

<span data-ttu-id="46683-114">Для использования оптимизации планирования установите надстройку оптимизации планирования для Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="46683-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="46683-115">Вы можете получить доступ к надстройке из проекта LCS и включить функцию оптимизации планирования из пользовательского интерфейса Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="46683-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="46683-116">Требование для оптимизации планирования — это среда с поддержкой LCS с высокой степенью доступности (а не среда OneBox) с версии Dynamics 365 Supply Chain Management 10.0.7 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="46683-116">The requirement for Planning Optimization is an LCS enabled high-availability environment (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span>

1. <span data-ttu-id="46683-117">Выполните вход в LCS и откройте нужную среду.</span><span class="sxs-lookup"><span data-stu-id="46683-117">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="46683-118">Перейдите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="46683-118">Go to **Full details**.</span></span>
1. <span data-ttu-id="46683-119">Перейдите на экспресс-вкладку **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="46683-119">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="46683-120">Выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="46683-120">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="46683-121">Выберите **Оптимизация планирования**.</span><span class="sxs-lookup"><span data-stu-id="46683-121">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="46683-122">Следуйте указаниям руководства по установке и примите условия и положения.</span><span class="sxs-lookup"><span data-stu-id="46683-122">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="46683-123">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="46683-123">Select **Install**.</span></span>
1. <span data-ttu-id="46683-124">На экспресс-вкладке **Надстройки среды** необходимо убедиться, что оптимизация планирования установлена.</span><span class="sxs-lookup"><span data-stu-id="46683-124">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="46683-125">После нескольких минут **установка** должна быть изменена на **установлено** (возможно, потребуется обновить страницу).</span><span class="sxs-lookup"><span data-stu-id="46683-125">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="46683-126">После установки можно приступать к активации оптимизации планирования в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="46683-126">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="46683-127">Интеграция оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="46683-127">Planning Optimization integration</span></span>

<span data-ttu-id="46683-128">Чтобы настроить, следует ли использовать надстройку оптимизации планирования для сводного планирования, перейдите **Сводное планирование** \> **Настройка** \> **Параметры оптимизации планирования**.</span><span class="sxs-lookup"><span data-stu-id="46683-128">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="46683-129">Статус подключения</span><span class="sxs-lookup"><span data-stu-id="46683-129">Connection status</span></span>

<span data-ttu-id="46683-130">Состояние подключения показывает текущий статус подключения между Supply Chain Management и службой оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="46683-130">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="46683-131">В следующей таблице показаны возможные значения.</span><span class="sxs-lookup"><span data-stu-id="46683-131">The following table shows the possible values.</span></span>

| <span data-ttu-id="46683-132">Статус подключения</span><span class="sxs-lookup"><span data-stu-id="46683-132">Connection status</span></span> | <span data-ttu-id="46683-133">Описание</span><span class="sxs-lookup"><span data-stu-id="46683-133">Description</span></span> | <span data-ttu-id="46683-134">Можно ли использовать оптимизацию планирования?</span><span class="sxs-lookup"><span data-stu-id="46683-134">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="46683-135">Подключено</span><span class="sxs-lookup"><span data-stu-id="46683-135">Connected</span></span> | <span data-ttu-id="46683-136">Между службой оптимизации планирования и Supply Chain Management было установлено подключение.</span><span class="sxs-lookup"><span data-stu-id="46683-136">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="46683-137">Да</span><span class="sxs-lookup"><span data-stu-id="46683-137">Yes</span></span> |
| <span data-ttu-id="46683-138">Включение подключения</span><span class="sxs-lookup"><span data-stu-id="46683-138">Enabling connection</span></span> | <span data-ttu-id="46683-139">В настоящее время выполняется запрос на включение подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="46683-139">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="46683-140">Нет</span><span class="sxs-lookup"><span data-stu-id="46683-140">No</span></span> |
| <span data-ttu-id="46683-141">Отключено</span><span class="sxs-lookup"><span data-stu-id="46683-141">Disconnected</span></span> | <span data-ttu-id="46683-142">Нет подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="46683-142">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="46683-143">Подключение можно включить из LCS, как описано ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="46683-143">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="46683-144">Нет</span><span class="sxs-lookup"><span data-stu-id="46683-144">No</span></span> |
| <span data-ttu-id="46683-145">Отключение подключения</span><span class="sxs-lookup"><span data-stu-id="46683-145">Disabling connection</span></span> | <span data-ttu-id="46683-146">В настоящее время выполняется запрос на отключение подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="46683-146">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="46683-147">Нет</span><span class="sxs-lookup"><span data-stu-id="46683-147">No</span></span> |
| <span data-ttu-id="46683-148">Получение статуса</span><span class="sxs-lookup"><span data-stu-id="46683-148">Getting status</span></span> | <span data-ttu-id="46683-149">Система ожидает сведения о состоянии службы оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="46683-149">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="46683-150">Нет</span><span class="sxs-lookup"><span data-stu-id="46683-150">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="46683-151">Параметр "Использовать оптимизацию планирования"</span><span class="sxs-lookup"><span data-stu-id="46683-151">The Use Planning Optimization option</span></span>

<span data-ttu-id="46683-152">Параметр **Использовать оптимизацию планирования** определяет, какой механизм планирования используется для сводного планирования:</span><span class="sxs-lookup"><span data-stu-id="46683-152">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="46683-153">**Да** — оптимизация планирования используется для сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="46683-153">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="46683-154">**Нет** — для сводного планирования используется встроенный механизм планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="46683-154">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="46683-155">Если существующие пакетные задания планирования, созданные для встроенного механизма планирования Supply Chain Management, запускаются, а параметр **Использовать оптимизацию планирования** задан как **Да**, эти задания не будут работать</span><span class="sxs-lookup"><span data-stu-id="46683-155">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="46683-156">Интеграции с настройкой</span><span class="sxs-lookup"><span data-stu-id="46683-156">Integration with the setup</span></span>

<span data-ttu-id="46683-157">Если предварительный просмотр оптимизации планирования включен, сводное планирование выполняется с помощью надстройки оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="46683-157">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="46683-158">В этом случае затронуты результаты и функции сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="46683-158">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="46683-159">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="46683-159">Related resources</span></span>

[<span data-ttu-id="46683-160">Условия для предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="46683-160">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="46683-161">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="46683-161">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="46683-162">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="46683-162">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="46683-163">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="46683-163">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="46683-164">Применение фильтров к плану</span><span class="sxs-lookup"><span data-stu-id="46683-164">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="46683-165">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="46683-165">Cancel a planning job</span></span>](cancel-planning-job.md)
