---
title: Начало работы с оптимизацией планирования
description: Этот раздел описывает начало работы с функциями оптимизации планирования.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
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
ms.openlocfilehash: 04b39469ccf4f088bb33bdfc73ce40eece6f5f2e
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887272"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="16d0f-103">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="16d0f-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="16d0f-104">Функции оптимизации планирования сейчас не поддерживают все возможности, доступные в механизме планирования, который встроен в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="16d0f-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="16d0f-105">Таким образом, важно оценить, будет ли набор функций, доступный в данный момент в оптимизации планирования, удовлетворять вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="16d0f-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="16d0f-106">По умолчанию функции оптимизации планирования не включены в Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="16d0f-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="16d0f-107">Таким образом, имеется возможность выполнить оценку до включения.</span><span class="sxs-lookup"><span data-stu-id="16d0f-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="16d0f-108">В конечном итоге, оптимизация планирования заменит существующий встроенный механизм планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="16d0f-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="16d0f-109">Перед включением оптимизации планирования настоятельно рекомендуется оценить ее пригодность по анализу пригодности оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="16d0f-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="16d0f-110">Дополнительные сведения см. в разделе [Анализ пригодности оптимизации планирования](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="16d0f-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="16d0f-111">Доступность</span><span class="sxs-lookup"><span data-stu-id="16d0f-111">Availability</span></span>
<span data-ttu-id="16d0f-112">Оптимизация планирования в настоящее время доступна в следующих регионах Azure: "США", "Канада", "Европа", "Соединенное Королевство" и "Австралия".</span><span class="sxs-lookup"><span data-stu-id="16d0f-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="16d0f-113">При попытке установить надстройку из другого региона LCS отобразит сообщение о том, что данный регион не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="16d0f-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="16d0f-114">Обратите внимание, что оптимизация планирования не поддерживает локальное развертывание Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="16d0f-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="16d0f-115">Лицензирование</span><span class="sxs-lookup"><span data-stu-id="16d0f-115">Licensing</span></span>

<span data-ttu-id="16d0f-116">Если вы можете запустить сводное планирование, используя текущую лицензию, вам не придется покупать дополнительную лицензию для начала использования оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="16d0f-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="16d0f-117">Установка надстройки</span><span class="sxs-lookup"><span data-stu-id="16d0f-117">Install the add-in</span></span>

<span data-ttu-id="16d0f-118">Для использования оптимизации планирования установите надстройку оптимизации планирования для Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="16d0f-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="16d0f-119">Вы можете получить доступ к надстройке из проекта LCS и включить функцию оптимизации планирования из пользовательского интерфейса Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="16d0f-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="16d0f-120">Требование для оптимизации планирования — это среда с поддержкой LCS с высокой степенью доступности уровня 2 или выше (а не среда OneBox) с версией Dynamics 365 Supply Chain Management 10.0.7 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="16d0f-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="16d0f-121">При попытке установить надстройку в среде OneBox установка не будет завершена, и вам придется отменить установку.</span><span class="sxs-lookup"><span data-stu-id="16d0f-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="16d0f-122">Выполните вход в LCS и откройте нужную среду.</span><span class="sxs-lookup"><span data-stu-id="16d0f-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="16d0f-123">Перейдите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="16d0f-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="16d0f-124">Перейдите на экспресс-вкладку **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="16d0f-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="16d0f-125">Выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="16d0f-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="16d0f-126">Выберите **Оптимизация планирования**.</span><span class="sxs-lookup"><span data-stu-id="16d0f-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="16d0f-127">Следуйте указаниям руководства по установке и примите условия и положения.</span><span class="sxs-lookup"><span data-stu-id="16d0f-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="16d0f-128">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="16d0f-128">Select **Install**.</span></span>
1. <span data-ttu-id="16d0f-129">На экспресс-вкладке **Надстройки среды** необходимо убедиться, что оптимизация планирования установлена.</span><span class="sxs-lookup"><span data-stu-id="16d0f-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="16d0f-130">После нескольких минут **установка** должна быть изменена на **установлено** (возможно, потребуется обновить страницу).</span><span class="sxs-lookup"><span data-stu-id="16d0f-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="16d0f-131">После установки можно приступать к активации оптимизации планирования в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="16d0f-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="16d0f-132">Интеграция оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="16d0f-132">Planning Optimization integration</span></span>

<span data-ttu-id="16d0f-133">Чтобы настроить, следует ли использовать надстройку оптимизации планирования для сводного планирования, перейдите **Сводное планирование** \> **Настройка** \> **Параметры оптимизации планирования**.</span><span class="sxs-lookup"><span data-stu-id="16d0f-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="16d0f-134">Статус подключения</span><span class="sxs-lookup"><span data-stu-id="16d0f-134">Connection status</span></span>

<span data-ttu-id="16d0f-135">Состояние подключения показывает текущий статус подключения между Supply Chain Management и службой оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="16d0f-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="16d0f-136">В следующей таблице показаны возможные значения.</span><span class="sxs-lookup"><span data-stu-id="16d0f-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="16d0f-137">Статус подключения</span><span class="sxs-lookup"><span data-stu-id="16d0f-137">Connection status</span></span> | <span data-ttu-id="16d0f-138">Описание</span><span class="sxs-lookup"><span data-stu-id="16d0f-138">Description</span></span> | <span data-ttu-id="16d0f-139">Можно ли использовать оптимизацию планирования?</span><span class="sxs-lookup"><span data-stu-id="16d0f-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="16d0f-140">Подключено</span><span class="sxs-lookup"><span data-stu-id="16d0f-140">Connected</span></span> | <span data-ttu-id="16d0f-141">Между службой оптимизации планирования и Supply Chain Management было установлено подключение.</span><span class="sxs-lookup"><span data-stu-id="16d0f-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="16d0f-142">Да</span><span class="sxs-lookup"><span data-stu-id="16d0f-142">Yes</span></span> |
| <span data-ttu-id="16d0f-143">Включение подключения</span><span class="sxs-lookup"><span data-stu-id="16d0f-143">Enabling connection</span></span> | <span data-ttu-id="16d0f-144">В настоящее время выполняется запрос на включение подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="16d0f-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="16d0f-145">Нет</span><span class="sxs-lookup"><span data-stu-id="16d0f-145">No</span></span> |
| <span data-ttu-id="16d0f-146">Отключено</span><span class="sxs-lookup"><span data-stu-id="16d0f-146">Disconnected</span></span> | <span data-ttu-id="16d0f-147">Нет подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="16d0f-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="16d0f-148">Подключение можно включить из LCS, как описано ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="16d0f-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="16d0f-149">Нет</span><span class="sxs-lookup"><span data-stu-id="16d0f-149">No</span></span> |
| <span data-ttu-id="16d0f-150">Отключение подключения</span><span class="sxs-lookup"><span data-stu-id="16d0f-150">Disabling connection</span></span> | <span data-ttu-id="16d0f-151">В настоящее время выполняется запрос на отключение подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="16d0f-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="16d0f-152">Нет</span><span class="sxs-lookup"><span data-stu-id="16d0f-152">No</span></span> |
| <span data-ttu-id="16d0f-153">Получение статуса</span><span class="sxs-lookup"><span data-stu-id="16d0f-153">Getting status</span></span> | <span data-ttu-id="16d0f-154">Система ожидает сведения о состоянии службы оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="16d0f-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="16d0f-155">Нет</span><span class="sxs-lookup"><span data-stu-id="16d0f-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="16d0f-156">Параметр "Использовать оптимизацию планирования"</span><span class="sxs-lookup"><span data-stu-id="16d0f-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="16d0f-157">Параметр **Использовать оптимизацию планирования** определяет, какой механизм планирования используется для сводного планирования:</span><span class="sxs-lookup"><span data-stu-id="16d0f-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="16d0f-158">**Да** — оптимизация планирования используется для сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="16d0f-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="16d0f-159">**Нет** — для сводного планирования используется встроенный механизм планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="16d0f-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="16d0f-160">Если существующие пакетные задания планирования, созданные для встроенного механизма планирования Supply Chain Management, запускаются, а параметр **Использовать оптимизацию планирования** задан как **Да**, эти задания не будут работать</span><span class="sxs-lookup"><span data-stu-id="16d0f-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="16d0f-161">Интеграции с настройкой</span><span class="sxs-lookup"><span data-stu-id="16d0f-161">Integration with the setup</span></span>

<span data-ttu-id="16d0f-162">Если предварительный просмотр оптимизации планирования включен, сводное планирование выполняется с помощью надстройки оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="16d0f-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="16d0f-163">В этом случае затронуты результаты и функции сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="16d0f-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16d0f-164">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="16d0f-164">Additional resources</span></span>

[<span data-ttu-id="16d0f-165">Условия для предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="16d0f-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="16d0f-166">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="16d0f-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="16d0f-167">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="16d0f-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="16d0f-168">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="16d0f-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="16d0f-169">Применение фильтров к плану</span><span class="sxs-lookup"><span data-stu-id="16d0f-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="16d0f-170">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="16d0f-170">Cancel a planning job</span></span>](cancel-planning-job.md)
