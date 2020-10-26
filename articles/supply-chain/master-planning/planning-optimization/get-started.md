---
title: Начало работы с оптимизацией планирования
description: Этот раздел описывает начало работы с функциями оптимизации планирования.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
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
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973484"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="79ce1-103">Начало работы с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="79ce1-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79ce1-104">Как было [объявлено ранее](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), оптимизация планирования запланирована для замены имеющейся встроенной подсистемы сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="79ce1-105">Если в настоящее время используется встроенный механизм планирования, следует сейчас начать планирование миграции на оптимизацию планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="79ce1-106">Важно начать процесс миграции немедленно, потому что операции могут пострадать при принудительном устаревании.</span><span class="sxs-lookup"><span data-stu-id="79ce1-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="79ce1-107">Чтобы избежать проблем в последнюю минуту, когда устаревание применяется принудительно, настоятельно рекомендуется выполнить миграцию до 1 декабря 2020 года.</span><span class="sxs-lookup"><span data-stu-id="79ce1-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="79ce1-108">Функции оптимизации планирования сейчас не поддерживают все возможности, доступные в механизме планирования, который встроен в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="79ce1-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="79ce1-109">Таким образом, важно оценить, будет ли набор функций, доступный в данный момент в оптимизации планирования, удовлетворять вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="79ce1-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="79ce1-110">Функция оптимизации планирования в настоящее время не включена по умолчанию в службах Dynamics Lifecycle Services (LCS), поэтому можно выполнить оценку до включения этой функции.</span><span class="sxs-lookup"><span data-stu-id="79ce1-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="79ce1-111">Необходимо запросить исключение из миграции на оптимизацию планирования, если ваш процесс сводного планирования не включает производство (спланированные производственные заказы, созданные с помощью сводного планированию) и вам требуется встроенный модуль планирования за пределами версии 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="79ce1-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="79ce1-112">Начиная с версии 10.0.16 в средах отображается сообщение об ошибке при запуске встроенного сводного планирования без создания спланированных производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="79ce1-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="79ce1-113">Оптимизация планирования должна использоваться для всех новых развертываний, в которых не создаются спланированные производственные заказы при сводном планировании.</span><span class="sxs-lookup"><span data-stu-id="79ce1-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="79ce1-114">Владельцы существующих сред, на которых запущены встроенные средства сводного планирования без создания спланированных производственных заказов, получат письма с подробными сведениями об этом процессе обработки исключения.</span><span class="sxs-lookup"><span data-stu-id="79ce1-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="79ce1-115">Рекомендуется работать с партнером, чтобы оценить и спланировать миграцию на оптимизацию планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="79ce1-116">Перед включением оптимизации планирования настоятельно рекомендуется оценить ее пригодность по анализу пригодности оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="79ce1-117">Дополнительные сведения см. в разделе [Анализ пригодности оптимизации планирования](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="79ce1-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="79ce1-118">Доступность</span><span class="sxs-lookup"><span data-stu-id="79ce1-118">Availability</span></span>
<span data-ttu-id="79ce1-119">Оптимизация планирования в настоящее время доступна в следующих регионах Azure: "США", "Канада", "Европа", "Соединенное Королевство" и "Австралия".</span><span class="sxs-lookup"><span data-stu-id="79ce1-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="79ce1-120">При попытке установить надстройку из другого региона LCS отобразит сообщение о том, что данный регион не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="79ce1-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="79ce1-121">Обратите внимание, что оптимизация планирования не поддерживает локальное развертывание Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="79ce1-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="79ce1-122">Лицензирование</span><span class="sxs-lookup"><span data-stu-id="79ce1-122">Licensing</span></span>

<span data-ttu-id="79ce1-123">Если вы можете запустить сводное планирование, используя текущую лицензию, вам не придется покупать дополнительную лицензию для начала использования оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="79ce1-124">Установка надстройки</span><span class="sxs-lookup"><span data-stu-id="79ce1-124">Install the add-in</span></span>

<span data-ttu-id="79ce1-125">Для использования оптимизации планирования установите надстройку оптимизации планирования для Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="79ce1-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="79ce1-126">Вы можете получить доступ к надстройке из проекта LCS и включить функцию оптимизации планирования из пользовательского интерфейса Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="79ce1-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="79ce1-127">Требование для оптимизации планирования — это среда с поддержкой LCS с высокой степенью доступности уровня 2 или выше (а не среда OneBox) с версией Dynamics 365 Supply Chain Management 10.0.7 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="79ce1-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="79ce1-128">При попытке установить надстройку в среде OneBox установка не будет завершена, и вам придется отменить установку.</span><span class="sxs-lookup"><span data-stu-id="79ce1-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="79ce1-129">Выполните вход в LCS и откройте нужную среду.</span><span class="sxs-lookup"><span data-stu-id="79ce1-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="79ce1-130">Перейдите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="79ce1-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="79ce1-131">Перейдите на экспресс-вкладку **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="79ce1-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="79ce1-132">Выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="79ce1-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="79ce1-133">Выберите **Оптимизация планирования**.</span><span class="sxs-lookup"><span data-stu-id="79ce1-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="79ce1-134">Следуйте указаниям руководства по установке и примите условия и положения.</span><span class="sxs-lookup"><span data-stu-id="79ce1-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="79ce1-135">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="79ce1-135">Select **Install**.</span></span>
1. <span data-ttu-id="79ce1-136">На экспресс-вкладке **Надстройки среды** необходимо убедиться, что оптимизация планирования установлена.</span><span class="sxs-lookup"><span data-stu-id="79ce1-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="79ce1-137">После нескольких минут **установка** должна быть изменена на **установлено** (возможно, потребуется обновить страницу).</span><span class="sxs-lookup"><span data-stu-id="79ce1-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="79ce1-138">После установки можно приступать к активации оптимизации планирования в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="79ce1-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="79ce1-139">Интеграция оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="79ce1-139">Planning Optimization integration</span></span>

<span data-ttu-id="79ce1-140">Чтобы настроить, следует ли использовать надстройку оптимизации планирования для сводного планирования, перейдите **Сводное планирование** \> **Настройка** \> **Параметры оптимизации планирования**.</span><span class="sxs-lookup"><span data-stu-id="79ce1-140">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="79ce1-141">Статус подключения</span><span class="sxs-lookup"><span data-stu-id="79ce1-141">Connection status</span></span>

<span data-ttu-id="79ce1-142">Состояние подключения показывает текущий статус подключения между Supply Chain Management и службой оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-142">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="79ce1-143">В следующей таблице показаны возможные значения.</span><span class="sxs-lookup"><span data-stu-id="79ce1-143">The following table shows the possible values.</span></span>

| <span data-ttu-id="79ce1-144">Статус подключения</span><span class="sxs-lookup"><span data-stu-id="79ce1-144">Connection status</span></span> | <span data-ttu-id="79ce1-145">Описание</span><span class="sxs-lookup"><span data-stu-id="79ce1-145">Description</span></span> | <span data-ttu-id="79ce1-146">Можно ли использовать оптимизацию планирования?</span><span class="sxs-lookup"><span data-stu-id="79ce1-146">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="79ce1-147">Подключено</span><span class="sxs-lookup"><span data-stu-id="79ce1-147">Connected</span></span> | <span data-ttu-id="79ce1-148">Между службой оптимизации планирования и Supply Chain Management было установлено подключение.</span><span class="sxs-lookup"><span data-stu-id="79ce1-148">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="79ce1-149">Да</span><span class="sxs-lookup"><span data-stu-id="79ce1-149">Yes</span></span> |
| <span data-ttu-id="79ce1-150">Включение подключения</span><span class="sxs-lookup"><span data-stu-id="79ce1-150">Enabling connection</span></span> | <span data-ttu-id="79ce1-151">В настоящее время выполняется запрос на включение подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-151">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="79ce1-152">Нет</span><span class="sxs-lookup"><span data-stu-id="79ce1-152">No</span></span> |
| <span data-ttu-id="79ce1-153">Отключено</span><span class="sxs-lookup"><span data-stu-id="79ce1-153">Disconnected</span></span> | <span data-ttu-id="79ce1-154">Нет подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-154">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="79ce1-155">Подключение можно включить из LCS, как описано ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="79ce1-155">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="79ce1-156">Нет</span><span class="sxs-lookup"><span data-stu-id="79ce1-156">No</span></span> |
| <span data-ttu-id="79ce1-157">Отключение подключения</span><span class="sxs-lookup"><span data-stu-id="79ce1-157">Disabling connection</span></span> | <span data-ttu-id="79ce1-158">В настоящее время выполняется запрос на отключение подключения к службе оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-158">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="79ce1-159">Нет</span><span class="sxs-lookup"><span data-stu-id="79ce1-159">No</span></span> |
| <span data-ttu-id="79ce1-160">Получение статуса</span><span class="sxs-lookup"><span data-stu-id="79ce1-160">Getting status</span></span> | <span data-ttu-id="79ce1-161">Система ожидает сведения о состоянии службы оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-161">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="79ce1-162">Нет</span><span class="sxs-lookup"><span data-stu-id="79ce1-162">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="79ce1-163">Параметр "Использовать оптимизацию планирования"</span><span class="sxs-lookup"><span data-stu-id="79ce1-163">The Use Planning Optimization option</span></span>

<span data-ttu-id="79ce1-164">Параметр **Использовать оптимизацию планирования** определяет, какой механизм планирования используется для сводного планирования:</span><span class="sxs-lookup"><span data-stu-id="79ce1-164">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="79ce1-165">**Да** — оптимизация планирования используется для сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-165">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="79ce1-166">**Нет** — для сводного планирования используется встроенный механизм планирования Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="79ce1-166">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="79ce1-167">Если существующие пакетные задания планирования, созданные для встроенного механизма планирования Supply Chain Management, запускаются, а параметр **Использовать оптимизацию планирования** задан как **Да**, эти задания не будут работать</span><span class="sxs-lookup"><span data-stu-id="79ce1-167">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="79ce1-168">Интеграции с настройкой</span><span class="sxs-lookup"><span data-stu-id="79ce1-168">Integration with the setup</span></span>

<span data-ttu-id="79ce1-169">Если предварительный просмотр оптимизации планирования включен, сводное планирование выполняется с помощью надстройки оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-169">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="79ce1-170">В этом случае затронуты результаты и функции сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="79ce1-170">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79ce1-171">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="79ce1-171">Additional resources</span></span>

[<span data-ttu-id="79ce1-172">Условия для предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="79ce1-172">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="79ce1-173">Обзор оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="79ce1-173">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="79ce1-174">Анализ пригодности оптимизации планирования</span><span class="sxs-lookup"><span data-stu-id="79ce1-174">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="79ce1-175">Просмотр журнала плана и журналов планирования</span><span class="sxs-lookup"><span data-stu-id="79ce1-175">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="79ce1-176">Применение фильтров к плану</span><span class="sxs-lookup"><span data-stu-id="79ce1-176">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="79ce1-177">Отмена задания планирования</span><span class="sxs-lookup"><span data-stu-id="79ce1-177">Cancel a planning job</span></span>](cancel-planning-job.md)
