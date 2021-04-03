---
title: Управление ремонтом
description: Можно систематизировать проблемы по группам с предложениями решений, успешно реализованных в прошлом.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 265709f298d9310d5d647eaa029ece778d2e226e
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470649"
---
# <a name="repair-management"></a><span data-ttu-id="66162-103">Управление ремонтом</span><span class="sxs-lookup"><span data-stu-id="66162-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="66162-104">Для управления ремонтом можно систематично группировать проблемы.</span><span class="sxs-lookup"><span data-stu-id="66162-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="66162-105">Это облегчит подбор решений, которые успешно применялись в прошлом.</span><span class="sxs-lookup"><span data-stu-id="66162-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="66162-106">Следует настроить признаки, параметры диагностики и решений.</span><span class="sxs-lookup"><span data-stu-id="66162-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="66162-107">Все эти параметры можно применять в дальнейшем при получении аналогичной номенклатуры для ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="66162-108">Можно также создать этапы ремонта, чтобы отслеживать стадии выполнения ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="66162-109">Настройка управления ремонтом</span><span class="sxs-lookup"><span data-stu-id="66162-109">Setting up repair management</span></span>

<span data-ttu-id="66162-110">Используйте следующие формы настройки для ввода информации, которая будет использоваться для определения признаков неисправностей, диагностики и решения при ремонте.</span><span class="sxs-lookup"><span data-stu-id="66162-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

- <span data-ttu-id="66162-111">**Управление сервисным обслуживанием** \> **Настройка** \> **Ремонт** \> **Условия**.</span><span class="sxs-lookup"><span data-stu-id="66162-111">**Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>
- <span data-ttu-id="66162-112">**Управление сервисным обслуживанием** \> **Настройка** \> **Ремонт** \> **Области симптомов**.</span><span class="sxs-lookup"><span data-stu-id="66162-112">**Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>
-  <span data-ttu-id="66162-113">**Управление сервисным обслуживанием** \> **Настройка** \> **Ремонт** \> **Области диагностики**.</span><span class="sxs-lookup"><span data-stu-id="66162-113">**Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>
- <span data-ttu-id="66162-114">**Управление сервисным обслуживанием** \> **Настройка** \> **Ремонт** \> **Решения**.</span><span class="sxs-lookup"><span data-stu-id="66162-114">**Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>
- <span data-ttu-id="66162-115">**Управление сервисным обслуживанием** \> **Настройка** \> **Ремонт** \> **Этапы ремонта**.</span><span class="sxs-lookup"><span data-stu-id="66162-115">**Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="66162-116">Признаки и условия</span><span class="sxs-lookup"><span data-stu-id="66162-116">Symptoms and conditions</span></span>

<span data-ttu-id="66162-117">Признаками называются характеристики, которыми клиент описывает проблему.</span><span class="sxs-lookup"><span data-stu-id="66162-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="66162-118">Признаки включают замечания клиента, которые определяют необходимость в ремонте.</span><span class="sxs-lookup"><span data-stu-id="66162-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="66162-119">Можно настроить области проявления признаков, коды признаков и условия.</span><span class="sxs-lookup"><span data-stu-id="66162-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="66162-120">Область признака включает область неисправности, а код признака — признак неисправности.</span><span class="sxs-lookup"><span data-stu-id="66162-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="66162-121">Условие описывает ситуацию или среду возникновения проблемы.</span><span class="sxs-lookup"><span data-stu-id="66162-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="66162-122">**Пример**</span><span class="sxs-lookup"><span data-stu-id="66162-122">**Example**</span></span>

<span data-ttu-id="66162-123">Компьютер приносят для ремонта, поскольку произошел сбой жесткого диска после продолжительного периода использования.</span><span class="sxs-lookup"><span data-stu-id="66162-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="66162-124">Сбой жесткого диска приводит к ошибке синего экрана.</span><span class="sxs-lookup"><span data-stu-id="66162-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="66162-125">Техник, который получает компьютер, вводит следующие признаки и условия:</span><span class="sxs-lookup"><span data-stu-id="66162-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="66162-126">Областью признака является жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="66162-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="66162-127">Кодом признака является ошибка синего экрана.</span><span class="sxs-lookup"><span data-stu-id="66162-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="66162-128">Условие заключается в том, что происходит сбой жесткого диска после продолжительного периода использования.</span><span class="sxs-lookup"><span data-stu-id="66162-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="66162-129">Диагностика и решения</span><span class="sxs-lookup"><span data-stu-id="66162-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="66162-130">Поля диагностики и решения - это операторы с точки зрения ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="66162-131">Эти шаги технический специалист выполняет для исследования проблемы.</span><span class="sxs-lookup"><span data-stu-id="66162-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="66162-132">Область диагностики охватывает операцию, которая необходима для решения проблемы.</span><span class="sxs-lookup"><span data-stu-id="66162-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="66162-133">Диагностический код - это метод работы с проблемой, а решением может быть ремонт элемента, его замена или отмена заказа клиентом.</span><span class="sxs-lookup"><span data-stu-id="66162-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="66162-134">Например, если компьютер был отремонтирован, область диагностики может быть "дефектная деталь", код диагностики может быть "установка новой видеокарты", а решение — "заменена".</span><span class="sxs-lookup"><span data-stu-id="66162-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="66162-135">Этапы ремонта</span><span class="sxs-lookup"><span data-stu-id="66162-135">Repair stages</span></span>

<span data-ttu-id="66162-136">Этапы ремонта определяют ход процесса ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="66162-137">Этап ремонта имеет параметр исполнения **Завершено**, который указывает на завершение строки ремонта и регистрацию даты и времени окончания.</span><span class="sxs-lookup"><span data-stu-id="66162-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="66162-138">Использование функции управления ремонтом</span><span class="sxs-lookup"><span data-stu-id="66162-138">Applying repair management</span></span>

<span data-ttu-id="66162-139">Для применения функции управления ремонтом к номенклатуре необходимо, чтобы для номенклатуры в заказе на обслуживание была настроена связь заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="66162-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="66162-140">В этом случае в заказе на обслуживание можно создать строку ремонта с информацией о текущей проблеме.</span><span class="sxs-lookup"><span data-stu-id="66162-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="66162-141">В строке ремонта можно определить объект обслуживания, поступивший на ремонт, и внести информацию о признаках, диагностике и исполнении.</span><span class="sxs-lookup"><span data-stu-id="66162-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="66162-142">Также можно создать примечание для строки ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="66162-143">Строки ремонта можно создавать для каждого шага процесса ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="66162-144">Создание строки ремонта в заказе на обслуживание</span><span class="sxs-lookup"><span data-stu-id="66162-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="66162-145">Перейдите **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="66162-145">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="66162-146">Выберите заказ на обслуживание с объектом обслуживания, требующим ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="66162-147">Выберите **Ремонт** \> **Строки ремонта**, чтобы открыть форму **Строки ремонта**.</span><span class="sxs-lookup"><span data-stu-id="66162-147">Select **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="66162-148">Выберите **Создать** для создания новой строки.</span><span class="sxs-lookup"><span data-stu-id="66162-148">Select **New** to create a new line.</span></span>

5.  <span data-ttu-id="66162-149">Выберите объект обслуживания.</span><span class="sxs-lookup"><span data-stu-id="66162-149">Select a service object.</span></span> <span data-ttu-id="66162-150">Можно выбрать любой объект обслуживания, у которого настроена объектная связь в заказе на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="66162-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="66162-151">Выберите в строке ремонта предопределенные признаки, диагностику и значения исполнения, связанные со строкой ремонта, и при необходимости выберите вкладку **Примечание** для создания примечания к строке ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then select the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="66162-152">Выберите **Сохранить**, чтобы сохранить новую строку ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-152">Select **Save** to save the new repair line.</span></span> <span data-ttu-id="66162-153">Поле **Дата и время создания** на вкладке **Общие** формы **Строки ремонта** обновляется значением времени сохранения.</span><span class="sxs-lookup"><span data-stu-id="66162-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="66162-154">Отслеживание хода выполнения ремонта и устранения проблемы</span><span class="sxs-lookup"><span data-stu-id="66162-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="66162-155">Для строки ремонта можно создать этапы ремонта, чтобы отслеживать ход выполнения ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="66162-156">Когда ремонт завершен, можно закрыть строку ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="66162-157">Установите для ремонта этап с включенным свойством **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="66162-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="66162-158">Текущая дата и время регистрируются в строке ремонта как время завершения.</span><span class="sxs-lookup"><span data-stu-id="66162-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="66162-159">Закрытие строки ремонта для решенной проблемы</span><span class="sxs-lookup"><span data-stu-id="66162-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="66162-160">Откройте форму **Строки ремонта**.</span><span class="sxs-lookup"><span data-stu-id="66162-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="66162-161">Выполните описанную выше процедуру создания строки ремонта.</span><span class="sxs-lookup"><span data-stu-id="66162-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="66162-162">Выберите строку ремонта с проблемой, которую следует закрыть.</span><span class="sxs-lookup"><span data-stu-id="66162-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="66162-163">В поле **Этап ремонта** выберите этап с включенным свойством **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="66162-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]