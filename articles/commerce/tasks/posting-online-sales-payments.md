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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415280"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="c2a48-103">Разноска интерактивных продаж и платежей</span><span class="sxs-lookup"><span data-stu-id="c2a48-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2a48-104">Эта процедура содержите инструкции по настройке и запуску регулярного пакетного задания для создания заказов на продажу и платежей для проводок интернета-магазина.</span><span class="sxs-lookup"><span data-stu-id="c2a48-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="c2a48-105">Разноска интернет-продаж и платежей выполняется в два этапа.</span><span class="sxs-lookup"><span data-stu-id="c2a48-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="c2a48-106">Извлечение данных транзакций Commerce интернет-торговли в головной офис.</span><span class="sxs-lookup"><span data-stu-id="c2a48-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="c2a48-107">Синхронизация заказов для создания заказов на продажу в головном отделении.</span><span class="sxs-lookup"><span data-stu-id="c2a48-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="c2a48-108">Извлечение данных транзакций интернет-торговли может выполнять либо вручную путем запуска P-задания, либо путем создания повторяющегося пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="c2a48-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="c2a48-109">Запуск P-задания вручную</span><span class="sxs-lookup"><span data-stu-id="c2a48-109">Manually running the P-job</span></span>

1. <span data-ttu-id="c2a48-110">Перейдите в раздел Все рабочие области > ИТ Retail и Commerce.</span><span class="sxs-lookup"><span data-stu-id="c2a48-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="c2a48-111">Щелкните "График распределения".</span><span class="sxs-lookup"><span data-stu-id="c2a48-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="c2a48-112">Выберите P-0001.</span><span class="sxs-lookup"><span data-stu-id="c2a48-112">Select P-0001.</span></span>
4. <span data-ttu-id="c2a48-113">Если необходимо, скорректируйте группы баз данных каналов.</span><span class="sxs-lookup"><span data-stu-id="c2a48-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="c2a48-114">Щелкните Запустить сейчас.</span><span class="sxs-lookup"><span data-stu-id="c2a48-114">Click Run now.</span></span>
6. <span data-ttu-id="c2a48-115">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="c2a48-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="c2a48-116">Планирование повторяющегося P-задания</span><span class="sxs-lookup"><span data-stu-id="c2a48-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="c2a48-117">Перейдите в раздел Все рабочие области > ИТ Retail и Commerce.</span><span class="sxs-lookup"><span data-stu-id="c2a48-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="c2a48-118">Щелкните "График распределения".</span><span class="sxs-lookup"><span data-stu-id="c2a48-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="c2a48-119">Выберите P-0001.</span><span class="sxs-lookup"><span data-stu-id="c2a48-119">Select P-0001.</span></span>
4. <span data-ttu-id="c2a48-120">Щелкните "Создать пакетное задание".</span><span class="sxs-lookup"><span data-stu-id="c2a48-120">Click Create batch job.</span></span>
5. <span data-ttu-id="c2a48-121">Щелкните "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="c2a48-121">Click Run in the background.</span></span>
5. <span data-ttu-id="c2a48-122">Включите пакетную обработку.</span><span class="sxs-lookup"><span data-stu-id="c2a48-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="c2a48-123">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="c2a48-123">Click Recurrence..</span></span>
7. <span data-ttu-id="c2a48-124">Выберите параметр "Дата завершения не указана".</span><span class="sxs-lookup"><span data-stu-id="c2a48-124">Select the No end date option.</span></span>
8. <span data-ttu-id="c2a48-125">В поле "Счетчик" введите интервал между запусками в минутах.</span><span class="sxs-lookup"><span data-stu-id="c2a48-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="c2a48-126">Обычно это будет 5–10.</span><span class="sxs-lookup"><span data-stu-id="c2a48-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="c2a48-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c2a48-127">Click OK.</span></span>
10. <span data-ttu-id="c2a48-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c2a48-128">Click OK.</span></span>

<span data-ttu-id="c2a48-129">Заказы могут быть синхронизированы либо путем запуска задания "Синхронизировать заказы" вручную, либо путем создания повторяющегося пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="c2a48-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="c2a48-130">Запуск синхронизации заказов вручную</span><span class="sxs-lookup"><span data-stu-id="c2a48-130">Manually running order synchronization</span></span> 

<span data-ttu-id="c2a48-131">Выполните следующие действия, чтобы один раз запустить задание "Синхронизировать заказы" вручную.</span><span class="sxs-lookup"><span data-stu-id="c2a48-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="c2a48-132">Перейдите "Все рабочие области > Финансовая информация магазина".</span><span class="sxs-lookup"><span data-stu-id="c2a48-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="c2a48-133">Щелкните "Синхронизация заказов".</span><span class="sxs-lookup"><span data-stu-id="c2a48-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="c2a48-134">В поле "Организационная иерархия" выберите "Магазины по регионам".</span><span class="sxs-lookup"><span data-stu-id="c2a48-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="c2a48-135">Выберите конкретный интернет-магазин или узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="c2a48-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="c2a48-136">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="c2a48-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="c2a48-137">Щелкните вкладку "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="c2a48-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="c2a48-138">Отключение пакетной обработки</span><span class="sxs-lookup"><span data-stu-id="c2a48-138">Disable Batch processing</span></span>
6. <span data-ttu-id="c2a48-139">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="c2a48-139">Click Recurrence.</span></span>
7. <span data-ttu-id="c2a48-140">Выбор параметра "Окончание после"</span><span class="sxs-lookup"><span data-stu-id="c2a48-140">Select End After option</span></span>
8. <span data-ttu-id="c2a48-141">В поле "Окончание после" введите 1.</span><span class="sxs-lookup"><span data-stu-id="c2a48-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="c2a48-142">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c2a48-142">Click OK.</span></span>
10. <span data-ttu-id="c2a48-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c2a48-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="c2a48-144">Планирование повторяющейся синхронизации заказов</span><span class="sxs-lookup"><span data-stu-id="c2a48-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="c2a48-145">Эта процедура содержите инструкции по настройке и запуску регулярного пакетного задания для создания заказов на продажу и платежей для проводок интернета-магазина.</span><span class="sxs-lookup"><span data-stu-id="c2a48-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="c2a48-146">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="c2a48-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="c2a48-147">Перейдите "Все рабочие области > Финансовая информация магазина".</span><span class="sxs-lookup"><span data-stu-id="c2a48-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="c2a48-148">Щелкните "Синхронизация заказов".</span><span class="sxs-lookup"><span data-stu-id="c2a48-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="c2a48-149">В поле "Организационная иерархия" выберите "Магазины по регионам".</span><span class="sxs-lookup"><span data-stu-id="c2a48-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="c2a48-150">Выберите конкретный интернет-магазин или узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="c2a48-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="c2a48-151">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="c2a48-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="c2a48-152">Щелкните вкладку "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="c2a48-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="c2a48-153">Включите пакетную обработку</span><span class="sxs-lookup"><span data-stu-id="c2a48-153">Enable Batch processing</span></span>
6. <span data-ttu-id="c2a48-154">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="c2a48-154">Click Recurrence.</span></span>
7. <span data-ttu-id="c2a48-155">Выберите параметр "Дата завершения не указана".</span><span class="sxs-lookup"><span data-stu-id="c2a48-155">Select the No end date option.</span></span>
8. <span data-ttu-id="c2a48-156">В поле "Счетчик" введите интервал между запусками в минутах.</span><span class="sxs-lookup"><span data-stu-id="c2a48-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="c2a48-157">Обычно это будет 2–20</span><span class="sxs-lookup"><span data-stu-id="c2a48-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="c2a48-158">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c2a48-158">Click OK.</span></span>
10. <span data-ttu-id="c2a48-159">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c2a48-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="c2a48-160">Информационные объекты, включенные в процесс</span><span class="sxs-lookup"><span data-stu-id="c2a48-160">Data entities involved in the process</span></span>

- <span data-ttu-id="c2a48-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="c2a48-161">RetailTransactionTable</span></span>
- <span data-ttu-id="c2a48-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="c2a48-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="c2a48-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="c2a48-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="c2a48-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="c2a48-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="c2a48-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="c2a48-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="c2a48-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="c2a48-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="c2a48-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="c2a48-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="c2a48-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="c2a48-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="c2a48-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="c2a48-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="c2a48-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="c2a48-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="c2a48-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="c2a48-171">RetailTransactionAttributeTrans</span></span>
