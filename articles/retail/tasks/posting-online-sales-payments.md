---
title: Разноска интерактивных продаж и платежей
description: Эта процедура содержите инструкции по настройке и запуску регулярного пакетного задания для создания заказов на продажу и платежей для проводок интернета-магазина.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d42b585a61214628980cd45a859215443ed55b5
ms.sourcegitcommit: c461758290d7ddc19f0b60701368937c35ef78b0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864161"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="209a3-103">Разноска интерактивных продаж и платежей</span><span class="sxs-lookup"><span data-stu-id="209a3-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="209a3-104">Эта процедура содержите инструкции по настройке и запуску регулярного пакетного задания для создания заказов на продажу и платежей для проводок интернета-магазина.</span><span class="sxs-lookup"><span data-stu-id="209a3-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="209a3-105">Разноска интернет-продаж и платежей выполняется в два этапа.</span><span class="sxs-lookup"><span data-stu-id="209a3-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="209a3-106">Извлечение данных транзакций розничной интернет-торговли в головной офис.</span><span class="sxs-lookup"><span data-stu-id="209a3-106">Pulling the online retail transaction data in HQ.</span></span>
- <span data-ttu-id="209a3-107">Синхронизация заказов для создания заказов на продажу в головном отделении.</span><span class="sxs-lookup"><span data-stu-id="209a3-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="209a3-108">Извлечение данных транзакций розничной интернет-торговли может выполнять либо вручную путем запуска P-задания, либо путем создания повторяющегося пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="209a3-108">Pulling the online retail transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="209a3-109">Запуск P-задания вручную</span><span class="sxs-lookup"><span data-stu-id="209a3-109">Manually running the P-job</span></span>

1. <span data-ttu-id="209a3-110">Перейдите в раздел "Все рабочие области" > "ИТ розничной торговли".</span><span class="sxs-lookup"><span data-stu-id="209a3-110">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="209a3-111">Щелкните "График распределения".</span><span class="sxs-lookup"><span data-stu-id="209a3-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="209a3-112">Выберите P-0001.</span><span class="sxs-lookup"><span data-stu-id="209a3-112">Select P-0001.</span></span>
4. <span data-ttu-id="209a3-113">Если необходимо, скорректируйте группы баз данных каналов.</span><span class="sxs-lookup"><span data-stu-id="209a3-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="209a3-114">Щелкните Запустить сейчас.</span><span class="sxs-lookup"><span data-stu-id="209a3-114">Click Run now.</span></span>
6. <span data-ttu-id="209a3-115">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="209a3-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="209a3-116">Планирование повторяющегося P-задания</span><span class="sxs-lookup"><span data-stu-id="209a3-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="209a3-117">Перейдите в раздел "Все рабочие области" > "ИТ розничной торговли".</span><span class="sxs-lookup"><span data-stu-id="209a3-117">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="209a3-118">Щелкните "График распределения".</span><span class="sxs-lookup"><span data-stu-id="209a3-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="209a3-119">Выберите P-0001.</span><span class="sxs-lookup"><span data-stu-id="209a3-119">Select P-0001.</span></span>
4. <span data-ttu-id="209a3-120">Щелкните "Создать пакетное задание".</span><span class="sxs-lookup"><span data-stu-id="209a3-120">Click Create batch job.</span></span>
5. <span data-ttu-id="209a3-121">Щелкните "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="209a3-121">Click Run in the background.</span></span>
5. <span data-ttu-id="209a3-122">Включите пакетную обработку.</span><span class="sxs-lookup"><span data-stu-id="209a3-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="209a3-123">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="209a3-123">Click Recurrence..</span></span>
7. <span data-ttu-id="209a3-124">Выберите параметр "Дата завершения не указана".</span><span class="sxs-lookup"><span data-stu-id="209a3-124">Select the No end date option.</span></span>
8. <span data-ttu-id="209a3-125">В поле "Счетчик" введите интервал между запусками в минутах.</span><span class="sxs-lookup"><span data-stu-id="209a3-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="209a3-126">Обычно это будет 5–10.</span><span class="sxs-lookup"><span data-stu-id="209a3-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="209a3-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="209a3-127">Click OK.</span></span>
10. <span data-ttu-id="209a3-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="209a3-128">Click OK.</span></span>

<span data-ttu-id="209a3-129">Заказы могут быть синхронизированы либо путем запуска задания "Синхронизировать заказы" вручную, либо путем создания повторяющегося пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="209a3-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="209a3-130">Запуск синхронизации заказов вручную</span><span class="sxs-lookup"><span data-stu-id="209a3-130">Manually running order synchronization</span></span> 

<span data-ttu-id="209a3-131">Выполните следующие действия, чтобы один раз запустить задание "Синхронизировать заказы" вручную.</span><span class="sxs-lookup"><span data-stu-id="209a3-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="209a3-132">Перейдите в раздел "Все рабочие области" > "Финансовая информация розничного магазина".</span><span class="sxs-lookup"><span data-stu-id="209a3-132">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="209a3-133">Щелкните "Синхронизация заказов".</span><span class="sxs-lookup"><span data-stu-id="209a3-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="209a3-134">В поле "Организационная иерархия" выберите "Розничные магазины по регионам".</span><span class="sxs-lookup"><span data-stu-id="209a3-134">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="209a3-135">Выберите конкретный интернет-магазин или узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="209a3-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="209a3-136">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="209a3-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="209a3-137">Щелкните вкладку "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="209a3-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="209a3-138">Отключение пакетной обработки</span><span class="sxs-lookup"><span data-stu-id="209a3-138">Disable Batch processing</span></span>
6. <span data-ttu-id="209a3-139">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="209a3-139">Click Recurrence.</span></span>
7. <span data-ttu-id="209a3-140">Выбор параметра "Окончание после"</span><span class="sxs-lookup"><span data-stu-id="209a3-140">Select End After option</span></span>
8. <span data-ttu-id="209a3-141">В поле "Окончание после" введите 1.</span><span class="sxs-lookup"><span data-stu-id="209a3-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="209a3-142">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="209a3-142">Click OK.</span></span>
10. <span data-ttu-id="209a3-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="209a3-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="209a3-144">Планирование повторяющейся синхронизации заказов</span><span class="sxs-lookup"><span data-stu-id="209a3-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="209a3-145">Эта процедура содержите инструкции по настройке и запуску регулярного пакетного задания для создания заказов на продажу и платежей для проводок интернета-магазина.</span><span class="sxs-lookup"><span data-stu-id="209a3-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="209a3-146">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="209a3-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="209a3-147">Перейдите в раздел "Все рабочие области" > "Финансовая информация розничного магазина".</span><span class="sxs-lookup"><span data-stu-id="209a3-147">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="209a3-148">Щелкните "Синхронизация заказов".</span><span class="sxs-lookup"><span data-stu-id="209a3-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="209a3-149">В поле "Организационная иерархия" выберите "Розничные магазины по регионам".</span><span class="sxs-lookup"><span data-stu-id="209a3-149">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="209a3-150">Выберите конкретный интернет-магазин или узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="209a3-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="209a3-151">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="209a3-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="209a3-152">Щелкните вкладку "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="209a3-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="209a3-153">Включите пакетную обработку</span><span class="sxs-lookup"><span data-stu-id="209a3-153">Enable Batch processing</span></span>
6. <span data-ttu-id="209a3-154">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="209a3-154">Click Recurrence.</span></span>
7. <span data-ttu-id="209a3-155">Выберите параметр "Дата завершения не указана".</span><span class="sxs-lookup"><span data-stu-id="209a3-155">Select the No end date option.</span></span>
8. <span data-ttu-id="209a3-156">В поле "Счетчик" введите интервал между запусками в минутах.</span><span class="sxs-lookup"><span data-stu-id="209a3-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="209a3-157">Обычно это будет 2–20</span><span class="sxs-lookup"><span data-stu-id="209a3-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="209a3-158">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="209a3-158">Click OK.</span></span>
10. <span data-ttu-id="209a3-159">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="209a3-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="209a3-160">Информационные объекты, включенные в процесс</span><span class="sxs-lookup"><span data-stu-id="209a3-160">Data entities involved in the process</span></span>

- <span data-ttu-id="209a3-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="209a3-161">RetailTransactionTable</span></span>
- <span data-ttu-id="209a3-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="209a3-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="209a3-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="209a3-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="209a3-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="209a3-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="209a3-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="209a3-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="209a3-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="209a3-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="209a3-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="209a3-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="209a3-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="209a3-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="209a3-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="209a3-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="209a3-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="209a3-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="209a3-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="209a3-171">RetailTransactionAttributeTrans</span></span>
