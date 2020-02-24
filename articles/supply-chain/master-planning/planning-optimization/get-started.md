---
title: Начало работы с оптимизацией планирования
description: Этот раздел описывает начало работы с функциями оптимизации планирования.
author: ChristianRytt
manager: AnnBe
ms.date: 01/17/2020
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
ms.openlocfilehash: 3e0371c6addc0412dc2fc105891b012941e92a06
ms.sourcegitcommit: e5a3c85a322a9216b8f176536d664fef40ae0bec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2020
ms.locfileid: "2971472"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="ca084-103">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="ca084-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="ca084-104">Функции оптимизации планирования сейчас не поддерживают все возможности, доступные в механизме планирования, который встроен в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ca084-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ca084-105">Таким образом, важно оценить, будет ли набор функций, доступный в данный момент в оптимизации планирования, удовлетворять вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="ca084-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="ca084-106">По умолчанию функции оптимизации планирования не включены в Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ca084-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="ca084-107">Таким образом, имеется возможность выполнить оценку до включения.</span><span class="sxs-lookup"><span data-stu-id="ca084-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="ca084-108">В конечном итоге, оптимизация планирования заменит существующий встроенный механизм планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ca084-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="ca084-109">Перед включением оптимизации планирования настоятельно рекомендуется оценить ее пригодность по анализу пригодности оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="ca084-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="ca084-110">Дополнительные сведения см. в разделе [Анализ пригодности оптимизации планирования](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ca084-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="ca084-111">Лицензирование</span><span class="sxs-lookup"><span data-stu-id="ca084-111">Licensing</span></span>

<span data-ttu-id="ca084-112">Если вы можете запустить сводное планирование, используя текущую лицензию, вам не придется покупать дополнительную лицензию для начала использования оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="ca084-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="ca084-113">Установка надстройки</span><span class="sxs-lookup"><span data-stu-id="ca084-113">Install the add-in</span></span>

<span data-ttu-id="ca084-114">Для использования оптимизации планирования установите надстройку оптимизации планирования для Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ca084-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ca084-115">Вы можете получить доступ к надстройке из проекта LCS и включить функцию оптимизации планирования из пользовательского интерфейса Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ca084-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="ca084-116">Выполните вход в LCS и откройте нужную среду.</span><span class="sxs-lookup"><span data-stu-id="ca084-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="ca084-117">Перейдите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="ca084-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="ca084-118">Перейдите на экспресс-вкладку **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="ca084-118">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="ca084-119">Выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="ca084-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="ca084-120">Выберите **Оптимизация планирования**.</span><span class="sxs-lookup"><span data-stu-id="ca084-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="ca084-121">Следуйте указаниям руководства по установке и примите условия и положения.</span><span class="sxs-lookup"><span data-stu-id="ca084-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="ca084-122">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="ca084-122">Select **Install**.</span></span>
1. <span data-ttu-id="ca084-123">На экспресс-вкладке **Надстройки среды** необходимо убедиться, что оптимизация планирования установлена.</span><span class="sxs-lookup"><span data-stu-id="ca084-123">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="ca084-124">После нескольких минут **установка** должна быть изменена на **установлено** (возможно, потребуется обновить страницу).</span><span class="sxs-lookup"><span data-stu-id="ca084-124">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="ca084-125">После установки можно приступать к активации оптимизации планирования в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ca084-125">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="ca084-126">Интеграция оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="ca084-126">Planning Optimization integration</span></span>

<span data-ttu-id="ca084-127">Чтобы настроить, следует ли использовать надстройку оптимизации планирования для сводного планирования, перейдите **Сводное планирование** \> **Настройка** \> **Параметры оптимизации планирования**.</span><span class="sxs-lookup"><span data-stu-id="ca084-127">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="ca084-128">Статус подключения</span><span class="sxs-lookup"><span data-stu-id="ca084-128">Connection status</span></span>

<span data-ttu-id="ca084-129">Состояние подключения показывает текущий статус подключения между Supply Chain Management и службой оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="ca084-129">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="ca084-130">В следующей таблице показаны возможные значения.</span><span class="sxs-lookup"><span data-stu-id="ca084-130">The following table shows the possible values.</span></span>

| <span data-ttu-id="ca084-131">Статус подключения</span><span class="sxs-lookup"><span data-stu-id="ca084-131">Connection status</span></span> | <span data-ttu-id="ca084-132">Описание</span><span class="sxs-lookup"><span data-stu-id="ca084-132">Description</span></span> | <span data-ttu-id="ca084-133">Можно ли использовать оптимизацию планирования?</span><span class="sxs-lookup"><span data-stu-id="ca084-133">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="ca084-134">Подключено</span><span class="sxs-lookup"><span data-stu-id="ca084-134">Connected</span></span> | <span data-ttu-id="ca084-135">Между службой оптимизации планирования и Supply Chain Management было установлено подключение.</span><span class="sxs-lookup"><span data-stu-id="ca084-135">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="ca084-136">Да</span><span class="sxs-lookup"><span data-stu-id="ca084-136">Yes</span></span> |
| <span data-ttu-id="ca084-137">Включение подключения</span><span class="sxs-lookup"><span data-stu-id="ca084-137">Enabling connection</span></span> | <span data-ttu-id="ca084-138">В настоящее время выполняется запрос на включение подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="ca084-138">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="ca084-139">Нет</span><span class="sxs-lookup"><span data-stu-id="ca084-139">No</span></span> |
| <span data-ttu-id="ca084-140">Отключено</span><span class="sxs-lookup"><span data-stu-id="ca084-140">Disconnected</span></span> | <span data-ttu-id="ca084-141">Нет подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="ca084-141">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="ca084-142">Подключение можно включить из LCS, как описано ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ca084-142">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="ca084-143">Нет</span><span class="sxs-lookup"><span data-stu-id="ca084-143">No</span></span> |
| <span data-ttu-id="ca084-144">Отключение подключения</span><span class="sxs-lookup"><span data-stu-id="ca084-144">Disabling connection</span></span> | <span data-ttu-id="ca084-145">В настоящее время выполняется запрос на отключение подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="ca084-145">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="ca084-146">Нет</span><span class="sxs-lookup"><span data-stu-id="ca084-146">No</span></span> |
| <span data-ttu-id="ca084-147">Получение статуса</span><span class="sxs-lookup"><span data-stu-id="ca084-147">Getting status</span></span> | <span data-ttu-id="ca084-148">Система ожидает сведения о состоянии службы оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="ca084-148">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="ca084-149">Нет</span><span class="sxs-lookup"><span data-stu-id="ca084-149">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="ca084-150">Параметр "Использовать оптимизацию планирования"</span><span class="sxs-lookup"><span data-stu-id="ca084-150">The Use Planning Optimization option</span></span>

<span data-ttu-id="ca084-151">Параметр **Использовать оптимизацию планирования** определяет, какой механизм планирования используется для сводного планирования:</span><span class="sxs-lookup"><span data-stu-id="ca084-151">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="ca084-152">**Да** — оптимизация планирования используется для сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="ca084-152">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="ca084-153">**Нет** — для сводного планирования используется встроенный механизм планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ca084-153">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="ca084-154">Если существующие пакетные задания планирования, созданные для встроенного механизма планирования Supply Chain Management, запускаются, а параметр **Использовать оптимизацию планирования** задан как **Да**, эти задания не будут работать</span><span class="sxs-lookup"><span data-stu-id="ca084-154">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="ca084-155">Интеграции с настройкой</span><span class="sxs-lookup"><span data-stu-id="ca084-155">Integration with the setup</span></span>

<span data-ttu-id="ca084-156">Если предварительный просмотр оптимизации планирования включен, сводное планирование выполняется с помощью надстройки оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="ca084-156">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="ca084-157">В этом случае затронуты результаты и функции сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="ca084-157">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="ca084-158">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ca084-158">Related resources</span></span>

[<span data-ttu-id="ca084-159">Условия для предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="ca084-159">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="ca084-160">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="ca084-160">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="ca084-161">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="ca084-161">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="ca084-162">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="ca084-162">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="ca084-163">Применение фильтров к плану</span><span class="sxs-lookup"><span data-stu-id="ca084-163">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="ca084-164">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="ca084-164">Cancel a planning job</span></span>](cancel-planning-job.md)
