---
title: Управление ремонтом
description: Можно систематизировать проблемы по группам с предложениями решений, успешно реализованных в прошлом.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32202344f77352cd3f9c1a807d14192a9bf0d9e6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "349293"
---
# <a name="repair-management"></a><span data-ttu-id="459f4-103">Управление ремонтом</span><span class="sxs-lookup"><span data-stu-id="459f4-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="459f4-104">Для управления ремонтом можно систематично группировать проблемы.</span><span class="sxs-lookup"><span data-stu-id="459f4-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="459f4-105">Это облегчит подбор решений, которые успешно применялись в прошлом.</span><span class="sxs-lookup"><span data-stu-id="459f4-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="459f4-106">Следует настроить признаки, параметры диагностики и решений.</span><span class="sxs-lookup"><span data-stu-id="459f4-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="459f4-107">Все эти параметры можно применять в дальнейшем при получении аналогичной номенклатуры для ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="459f4-108">Можно также создать этапы ремонта, чтобы отслеживать стадии выполнения ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="459f4-109">Настройка управления ремонтом</span><span class="sxs-lookup"><span data-stu-id="459f4-109">Setting up repair management</span></span>

<span data-ttu-id="459f4-110">Используйте следующие формы настройки для ввода информации, которая будет использоваться для определения признаков неисправностей, диагностики и решения при ремонте.</span><span class="sxs-lookup"><span data-stu-id="459f4-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

1.  <span data-ttu-id="459f4-111">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Ремонт** \> **Условия**.</span><span class="sxs-lookup"><span data-stu-id="459f4-111">Click **Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>

2.  <span data-ttu-id="459f4-112">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Ремонт** \> **Области симптомов**.</span><span class="sxs-lookup"><span data-stu-id="459f4-112">Click **Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>

3.  <span data-ttu-id="459f4-113">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Ремонт** \> **Области диагностики**.</span><span class="sxs-lookup"><span data-stu-id="459f4-113">Click **Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>

4.  <span data-ttu-id="459f4-114">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Ремонт** \> **Решения**.</span><span class="sxs-lookup"><span data-stu-id="459f4-114">Click **Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>

5.  <span data-ttu-id="459f4-115">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Ремонт** \> **Этапы ремонта**.</span><span class="sxs-lookup"><span data-stu-id="459f4-115">Click **Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="459f4-116">Признаки и условия</span><span class="sxs-lookup"><span data-stu-id="459f4-116">Symptoms and conditions</span></span>

<span data-ttu-id="459f4-117">Признаками называются характеристики, которыми клиент описывает проблему.</span><span class="sxs-lookup"><span data-stu-id="459f4-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="459f4-118">Признаки включают замечания клиента, которые определяют необходимость в ремонте.</span><span class="sxs-lookup"><span data-stu-id="459f4-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="459f4-119">Можно настроить области проявления признаков, коды признаков и условия.</span><span class="sxs-lookup"><span data-stu-id="459f4-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="459f4-120">Область признака включает область неисправности, а код признака — признак неисправности.</span><span class="sxs-lookup"><span data-stu-id="459f4-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="459f4-121">Условие описывает ситуацию или среду возникновения проблемы.</span><span class="sxs-lookup"><span data-stu-id="459f4-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="459f4-122">**Пример**</span><span class="sxs-lookup"><span data-stu-id="459f4-122">**Example**</span></span>

<span data-ttu-id="459f4-123">Компьютер приносят для ремонта, поскольку произошел сбой жесткого диска после продолжительного периода использования.</span><span class="sxs-lookup"><span data-stu-id="459f4-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="459f4-124">Сбой жесткого диска приводит к ошибке синего экрана.</span><span class="sxs-lookup"><span data-stu-id="459f4-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="459f4-125">Техник, который получает компьютер, вводит следующие признаки и условия:</span><span class="sxs-lookup"><span data-stu-id="459f4-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="459f4-126">Областью признака является жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="459f4-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="459f4-127">Кодом признака является ошибка синего экрана.</span><span class="sxs-lookup"><span data-stu-id="459f4-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="459f4-128">Условие заключается в том, что происходит сбой жесткого диска после продолжительного периода использования.</span><span class="sxs-lookup"><span data-stu-id="459f4-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="459f4-129">Диагностика и решения</span><span class="sxs-lookup"><span data-stu-id="459f4-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="459f4-130">Поля диагностики и решения - это операторы с точки зрения ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="459f4-131">Эти шаги технический специалист выполняет для исследования проблемы.</span><span class="sxs-lookup"><span data-stu-id="459f4-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="459f4-132">Область диагностики охватывает операцию, которая необходима для решения проблемы.</span><span class="sxs-lookup"><span data-stu-id="459f4-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="459f4-133">Диагностический код - это метод работы с проблемой, а решением может быть ремонт элемента, его замена или отмена заказа клиентом.</span><span class="sxs-lookup"><span data-stu-id="459f4-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="459f4-134">Например, если компьютер был отремонтирован, область диагностики может быть "дефектная деталь", код диагностики может быть "установка новой видеокарты", а решение — "заменена".</span><span class="sxs-lookup"><span data-stu-id="459f4-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="459f4-135">Этапы ремонта</span><span class="sxs-lookup"><span data-stu-id="459f4-135">Repair stages</span></span>

<span data-ttu-id="459f4-136">Этапы ремонта определяют ход процесса ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="459f4-137">Этап ремонта имеет параметр исполнения **Завершено**, который указывает на завершение строки ремонта и регистрацию даты и времени окончания.</span><span class="sxs-lookup"><span data-stu-id="459f4-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="459f4-138">Использование функции управления ремонтом</span><span class="sxs-lookup"><span data-stu-id="459f4-138">Applying repair management</span></span>

<span data-ttu-id="459f4-139">Для применения функции управления ремонтом к номенклатуре необходимо, чтобы для номенклатуры в заказе на обслуживание была настроена связь заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="459f4-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="459f4-140">В этом случае в заказе на обслуживание можно создать строку ремонта с информацией о текущей проблеме.</span><span class="sxs-lookup"><span data-stu-id="459f4-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="459f4-141">В строке ремонта можно определить объект обслуживания, поступивший на ремонт, и внести информацию о признаках, диагностике и исполнении.</span><span class="sxs-lookup"><span data-stu-id="459f4-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="459f4-142">Также можно создать примечание для строки ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="459f4-143">Строки ремонта можно создавать для каждого шага процесса ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="459f4-144">Создание строки ремонта в заказе на обслуживание</span><span class="sxs-lookup"><span data-stu-id="459f4-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="459f4-145">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="459f4-145">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="459f4-146">Выберите заказ на обслуживание с объектом обслуживания, требующим ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="459f4-147">Щелкните **Ремонт** \> **Строки ремонта**, чтобы открыть форму **Строки ремонта**.</span><span class="sxs-lookup"><span data-stu-id="459f4-147">Click **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="459f4-148">Нажмите CTRL+N, чтобы создать новую строку</span><span class="sxs-lookup"><span data-stu-id="459f4-148">Press CTRL+N to create a new line.</span></span>

5.  <span data-ttu-id="459f4-149">Выберите объект обслуживания.</span><span class="sxs-lookup"><span data-stu-id="459f4-149">Select a service object.</span></span> <span data-ttu-id="459f4-150">Можно выбрать любой объект обслуживания, у которого настроена объектная связь в заказе на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="459f4-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="459f4-151">Выберите в строке ремонта предопределенные признаки, диагностику и значения исполнения, связанные со строкой ремонта, и при необходимости перейдите на вкладку **Примечание** для создания примечания к строке ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then click the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="459f4-152">Нажмите CTRL+S, чтобы сохранить новую строку ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-152">Press CTRL+S to save the new repair line.</span></span> <span data-ttu-id="459f4-153">Поле **Дата и время создания** на вкладке **Общие** формы **Строки ремонта** обновляется значением времени сохранения.</span><span class="sxs-lookup"><span data-stu-id="459f4-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="459f4-154">Отслеживание хода выполнения ремонта и устранения проблемы</span><span class="sxs-lookup"><span data-stu-id="459f4-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="459f4-155">Для строки ремонта можно создать этапы ремонта, чтобы отслеживать ход выполнения ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="459f4-156">Когда ремонт завершен, можно закрыть строку ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="459f4-157">Установите для ремонта этап с включенным свойством **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="459f4-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="459f4-158">Текущая дата и время регистрируются в строке ремонта как время завершения.</span><span class="sxs-lookup"><span data-stu-id="459f4-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="459f4-159">Закрытие строки ремонта для решенной проблемы</span><span class="sxs-lookup"><span data-stu-id="459f4-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="459f4-160">Откройте форму **Строки ремонта**.</span><span class="sxs-lookup"><span data-stu-id="459f4-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="459f4-161">Выполните описанную выше процедуру создания строки ремонта.</span><span class="sxs-lookup"><span data-stu-id="459f4-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="459f4-162">Выберите строку ремонта с проблемой, которую следует закрыть.</span><span class="sxs-lookup"><span data-stu-id="459f4-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="459f4-163">В поле **Этап ремонта** выберите этап с включенным свойством **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="459f4-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  


