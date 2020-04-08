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
ms.openlocfilehash: e3bac0cab764436a618fa570901c84ab720dbc86
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140792"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="4afd6-103">Разноска интерактивных продаж и платежей</span><span class="sxs-lookup"><span data-stu-id="4afd6-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4afd6-104">Эта процедура содержите инструкции по настройке и запуску регулярного пакетного задания для создания заказов на продажу и платежей для проводок интернета-магазина.</span><span class="sxs-lookup"><span data-stu-id="4afd6-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="4afd6-105">Разноска интернет-продаж и платежей выполняется в два этапа.</span><span class="sxs-lookup"><span data-stu-id="4afd6-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="4afd6-106">Извлечение данных транзакций Commerce интернет-торговли в головной офис.</span><span class="sxs-lookup"><span data-stu-id="4afd6-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="4afd6-107">Синхронизация заказов для создания заказов на продажу в головном отделении.</span><span class="sxs-lookup"><span data-stu-id="4afd6-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="4afd6-108">Извлечение данных транзакций интернет-торговли может выполнять либо вручную путем запуска P-задания, либо путем создания повторяющегося пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="4afd6-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="4afd6-109">Запуск P-задания вручную</span><span class="sxs-lookup"><span data-stu-id="4afd6-109">Manually running the P-job</span></span>

1. <span data-ttu-id="4afd6-110">Перейдите в раздел Все рабочие области > ИТ Retail и Commerce.</span><span class="sxs-lookup"><span data-stu-id="4afd6-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="4afd6-111">Щелкните "График распределения".</span><span class="sxs-lookup"><span data-stu-id="4afd6-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="4afd6-112">Выберите P-0001.</span><span class="sxs-lookup"><span data-stu-id="4afd6-112">Select P-0001.</span></span>
4. <span data-ttu-id="4afd6-113">Если необходимо, скорректируйте группы баз данных каналов.</span><span class="sxs-lookup"><span data-stu-id="4afd6-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="4afd6-114">Щелкните Запустить сейчас.</span><span class="sxs-lookup"><span data-stu-id="4afd6-114">Click Run now.</span></span>
6. <span data-ttu-id="4afd6-115">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="4afd6-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="4afd6-116">Планирование повторяющегося P-задания</span><span class="sxs-lookup"><span data-stu-id="4afd6-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="4afd6-117">Перейдите в раздел Все рабочие области > ИТ Retail и Commerce.</span><span class="sxs-lookup"><span data-stu-id="4afd6-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="4afd6-118">Щелкните "График распределения".</span><span class="sxs-lookup"><span data-stu-id="4afd6-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="4afd6-119">Выберите P-0001.</span><span class="sxs-lookup"><span data-stu-id="4afd6-119">Select P-0001.</span></span>
4. <span data-ttu-id="4afd6-120">Щелкните "Создать пакетное задание".</span><span class="sxs-lookup"><span data-stu-id="4afd6-120">Click Create batch job.</span></span>
5. <span data-ttu-id="4afd6-121">Щелкните "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="4afd6-121">Click Run in the background.</span></span>
5. <span data-ttu-id="4afd6-122">Включите пакетную обработку.</span><span class="sxs-lookup"><span data-stu-id="4afd6-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="4afd6-123">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="4afd6-123">Click Recurrence..</span></span>
7. <span data-ttu-id="4afd6-124">Выберите параметр "Дата завершения не указана".</span><span class="sxs-lookup"><span data-stu-id="4afd6-124">Select the No end date option.</span></span>
8. <span data-ttu-id="4afd6-125">В поле "Счетчик" введите интервал между запусками в минутах.</span><span class="sxs-lookup"><span data-stu-id="4afd6-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="4afd6-126">Обычно это будет 5–10.</span><span class="sxs-lookup"><span data-stu-id="4afd6-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="4afd6-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4afd6-127">Click OK.</span></span>
10. <span data-ttu-id="4afd6-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4afd6-128">Click OK.</span></span>

<span data-ttu-id="4afd6-129">Заказы могут быть синхронизированы либо путем запуска задания "Синхронизировать заказы" вручную, либо путем создания повторяющегося пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="4afd6-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="4afd6-130">Запуск синхронизации заказов вручную</span><span class="sxs-lookup"><span data-stu-id="4afd6-130">Manually running order synchronization</span></span> 

<span data-ttu-id="4afd6-131">Выполните следующие действия, чтобы один раз запустить задание "Синхронизировать заказы" вручную.</span><span class="sxs-lookup"><span data-stu-id="4afd6-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="4afd6-132">Перейдите "Все рабочие области > Финансовая информация магазина".</span><span class="sxs-lookup"><span data-stu-id="4afd6-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="4afd6-133">Щелкните "Синхронизация заказов".</span><span class="sxs-lookup"><span data-stu-id="4afd6-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="4afd6-134">В поле "Организационная иерархия" выберите "Магазины по регионам".</span><span class="sxs-lookup"><span data-stu-id="4afd6-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="4afd6-135">Выберите конкретный интернет-магазин или узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="4afd6-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="4afd6-136">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="4afd6-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="4afd6-137">Щелкните вкладку "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="4afd6-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="4afd6-138">Отключение пакетной обработки</span><span class="sxs-lookup"><span data-stu-id="4afd6-138">Disable Batch processing</span></span>
6. <span data-ttu-id="4afd6-139">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="4afd6-139">Click Recurrence.</span></span>
7. <span data-ttu-id="4afd6-140">Выбор параметра "Окончание после"</span><span class="sxs-lookup"><span data-stu-id="4afd6-140">Select End After option</span></span>
8. <span data-ttu-id="4afd6-141">В поле "Окончание после" введите 1.</span><span class="sxs-lookup"><span data-stu-id="4afd6-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="4afd6-142">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4afd6-142">Click OK.</span></span>
10. <span data-ttu-id="4afd6-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4afd6-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="4afd6-144">Планирование повторяющейся синхронизации заказов</span><span class="sxs-lookup"><span data-stu-id="4afd6-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="4afd6-145">Эта процедура содержите инструкции по настройке и запуску регулярного пакетного задания для создания заказов на продажу и платежей для проводок интернета-магазина.</span><span class="sxs-lookup"><span data-stu-id="4afd6-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="4afd6-146">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="4afd6-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4afd6-147">Перейдите "Все рабочие области > Финансовая информация магазина".</span><span class="sxs-lookup"><span data-stu-id="4afd6-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="4afd6-148">Щелкните "Синхронизация заказов".</span><span class="sxs-lookup"><span data-stu-id="4afd6-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="4afd6-149">В поле "Организационная иерархия" выберите "Магазины по регионам".</span><span class="sxs-lookup"><span data-stu-id="4afd6-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="4afd6-150">Выберите конкретный интернет-магазин или узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="4afd6-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="4afd6-151">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="4afd6-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="4afd6-152">Щелкните вкладку "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="4afd6-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="4afd6-153">Включите пакетную обработку</span><span class="sxs-lookup"><span data-stu-id="4afd6-153">Enable Batch processing</span></span>
6. <span data-ttu-id="4afd6-154">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="4afd6-154">Click Recurrence.</span></span>
7. <span data-ttu-id="4afd6-155">Выберите параметр "Дата завершения не указана".</span><span class="sxs-lookup"><span data-stu-id="4afd6-155">Select the No end date option.</span></span>
8. <span data-ttu-id="4afd6-156">В поле "Счетчик" введите интервал между запусками в минутах.</span><span class="sxs-lookup"><span data-stu-id="4afd6-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="4afd6-157">Обычно это будет 2–20</span><span class="sxs-lookup"><span data-stu-id="4afd6-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="4afd6-158">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4afd6-158">Click OK.</span></span>
10. <span data-ttu-id="4afd6-159">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4afd6-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="4afd6-160">Информационные объекты, включенные в процесс</span><span class="sxs-lookup"><span data-stu-id="4afd6-160">Data entities involved in the process</span></span>

- <span data-ttu-id="4afd6-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="4afd6-161">RetailTransactionTable</span></span>
- <span data-ttu-id="4afd6-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="4afd6-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="4afd6-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="4afd6-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="4afd6-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="4afd6-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="4afd6-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="4afd6-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="4afd6-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="4afd6-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="4afd6-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="4afd6-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="4afd6-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="4afd6-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="4afd6-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="4afd6-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="4afd6-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="4afd6-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="4afd6-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="4afd6-171">RetailTransactionAttributeTrans</span></span>
