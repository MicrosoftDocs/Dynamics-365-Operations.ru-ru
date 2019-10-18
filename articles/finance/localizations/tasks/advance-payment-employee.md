---
title: EEU-00047 Авансовый платеж сотруднику
description: Эта процедура демонстрирует, как настраивать и регистрировать проводки для подотчетного лица.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCashTable, LedgerJournalSetup, HcmWorkerGroup_RU, EmplPosting_RU, VendParameters, RCashPosting, BankParameters, PaymTerm, HcmWorker, HcmWorkerNewWorker, HcmWorkerAdvHolderTableListPage_RU, HcmWorkerAdvHolderTable_RU, PurchTable, PurchCreateOrder, HcmAdvHolderLookup_RU, InventItemIdLookupPurchase, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, EmplTrans_RU, EmplBalance_RU
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cfc03cb9dc35a27f99b740da181fe54aa2e684d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175204"
---
# <a name="eeu-00047-advance-payment-to-employee"></a><span data-ttu-id="435cd-103">EEU-00047 Авансовый платеж сотруднику</span><span class="sxs-lookup"><span data-stu-id="435cd-103">EEU-00047 Advance payment to employee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="435cd-104">Эта процедура демонстрирует, как настраивать и регистрировать проводки для подотчетного лица.</span><span class="sxs-lookup"><span data-stu-id="435cd-104">This procedure demonstrates how to set up and register transactions for an advance holder.</span></span> <span data-ttu-id="435cd-105">Эта процедура была создана с использованием компании с демонстрационными данными DEMF с основным адресом в Литве.</span><span class="sxs-lookup"><span data-stu-id="435cd-105">This procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="435cd-106">Эта задача работает только для юридических лиц с основным адресом в Польше, Литве, Латвии, Эстонии, Чехии или Венгрии.</span><span class="sxs-lookup"><span data-stu-id="435cd-106">This task only works for legal entities with a primary address in Poland, Lithuania, Latvia, Estonia, Czech Republic, or Hungary.</span></span> <span data-ttu-id="435cd-107">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="435cd-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-cash-account"></a><span data-ttu-id="435cd-108">Создать новый кассовый счет</span><span class="sxs-lookup"><span data-stu-id="435cd-108">Create a new cash account</span></span>
1. <span data-ttu-id="435cd-109">Перейдите в раздел "Управление банком и кассовыми операциями" > "Банковские счета" > "Кассы".</span><span class="sxs-lookup"><span data-stu-id="435cd-109">Go to Cash and bank management > Bank accounts > Cash accounts.</span></span>
2. <span data-ttu-id="435cd-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="435cd-110">Click New.</span></span>
3. <span data-ttu-id="435cd-111">В поле "Наличный расчет" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-111">In the Cash field, type a value.</span></span>
4. <span data-ttu-id="435cd-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="435cd-113">В поле "Группа номерных серий" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-113">In the Number sequence group field, enter or select a value.</span></span>
6. <span data-ttu-id="435cd-114">Разверните раздел "Проверка".</span><span class="sxs-lookup"><span data-stu-id="435cd-114">Expand the Validation section.</span></span>
7. <span data-ttu-id="435cd-115">В поле "Валюта" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-115">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="435cd-116">Выберите "Да" в поле "Отрицательная касса".</span><span class="sxs-lookup"><span data-stu-id="435cd-116">Select Yes in the Negative cash field.</span></span>
9. <span data-ttu-id="435cd-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-117">Click Save.</span></span>

## <a name="create-a-new-journal"></a><span data-ttu-id="435cd-118">Создание нового журнала.</span><span class="sxs-lookup"><span data-stu-id="435cd-118">Create a new journal</span></span>
1. <span data-ttu-id="435cd-119">Перейдите в раздел "Главная книга" > "Настройка журнала" > "Наименования журналов".</span><span class="sxs-lookup"><span data-stu-id="435cd-119">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="435cd-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="435cd-120">Click New.</span></span>
3. <span data-ttu-id="435cd-121">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="435cd-122">В поле "Серии ваучеров" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-122">In the Voucher series field, enter or select a value.</span></span>
5. <span data-ttu-id="435cd-123">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-123">Click Save.</span></span>
6. <span data-ttu-id="435cd-124">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="435cd-124">Click New.</span></span>
7. <span data-ttu-id="435cd-125">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-125">In the Name field, type a value.</span></span>
8. <span data-ttu-id="435cd-126">В поле "Тип журнала" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="435cd-126">In the Journal type field, select an option.</span></span>
9. <span data-ttu-id="435cd-127">В поле "Серии ваучеров" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-127">In the Voucher series field, enter or select a value.</span></span>
10. <span data-ttu-id="435cd-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-128">Click Save.</span></span>

## <a name="create-an-advance-holder-group"></a><span data-ttu-id="435cd-129">Создание группы подотчетных лиц</span><span class="sxs-lookup"><span data-stu-id="435cd-129">Create an advance holder group</span></span>
1. <span data-ttu-id="435cd-130">Перейдите в раздел "Расчеты с поставщиками" > "Настройка" > "Подотчетные лица" > "Группы подотчетных лиц".</span><span class="sxs-lookup"><span data-stu-id="435cd-130">Go to Accounts payable > Setup > Advance holders > Advance holder groups.</span></span>
2. <span data-ttu-id="435cd-131">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="435cd-131">Click New.</span></span>
3. <span data-ttu-id="435cd-132">В поле "Группа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-132">In the Group field, type a value.</span></span>
4. <span data-ttu-id="435cd-133">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="435cd-134">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-134">Click Save.</span></span>

## <a name="create-an-employee-posting-profile"></a><span data-ttu-id="435cd-135">Создание профиля разноски сотрудника</span><span class="sxs-lookup"><span data-stu-id="435cd-135">Create an employee posting profile</span></span>
1. <span data-ttu-id="435cd-136">Перейдите в раздел "Расчеты с поставщиками" > "Настройка" > "Подотчетные лица" >"Профили разноски по подотч. лицам".</span><span class="sxs-lookup"><span data-stu-id="435cd-136">Go to Accounts payable > Setup > Advance holders > Employee posting profiles.</span></span>
2. <span data-ttu-id="435cd-137">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="435cd-137">Click New.</span></span>
3. <span data-ttu-id="435cd-138">В поле "Профиль разноски" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-138">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="435cd-139">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-139">In the Description field, type a value.</span></span>
5. <span data-ttu-id="435cd-140">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="435cd-140">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="435cd-141">В поле "Допустимо для" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="435cd-141">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="435cd-142">В поле "Суммарный счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="435cd-142">In the Summary account field, specify the desired values.</span></span>
8. <span data-ttu-id="435cd-143">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-143">Click Save.</span></span>

## <a name="set-up-advance-holder-parameters"></a><span data-ttu-id="435cd-144">Настройка параметров подотчетных лиц</span><span class="sxs-lookup"><span data-stu-id="435cd-144">Set up advance holder parameters</span></span>
1. <span data-ttu-id="435cd-145">Перейдите в раздел "Расчеты с поставщиками" > "Настройка" > "Параметры расчетов с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="435cd-145">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="435cd-146">Выберите вкладку "Подотчетные лица".</span><span class="sxs-lookup"><span data-stu-id="435cd-146">Click the Advance holders tab.</span></span>
3. <span data-ttu-id="435cd-147">В поле "Профиль разноски" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-147">In the Posting profile field, enter or select a value.</span></span>
4. <span data-ttu-id="435cd-148">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-148">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="435cd-149">В поле "Наличный расчет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-149">In the Cash field, enter or select a value.</span></span>
6. <span data-ttu-id="435cd-150">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-150">In the Name field, enter or select a value.</span></span>
7. <span data-ttu-id="435cd-151">В поле "Тип счета" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="435cd-151">In the Account type field, select an option.</span></span>
8. <span data-ttu-id="435cd-152">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="435cd-152">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="435cd-153">Откройте вкладку Номерные серии.</span><span class="sxs-lookup"><span data-stu-id="435cd-153">Click the Number sequences tab.</span></span>
10. <span data-ttu-id="435cd-154">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-154">Click Save.</span></span>

## <a name="set-up-a-cash-posting-profile"></a><span data-ttu-id="435cd-155">Настройка профиля разноски кассы</span><span class="sxs-lookup"><span data-stu-id="435cd-155">Set up a cash posting profile</span></span>
1. <span data-ttu-id="435cd-156">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Профили разноски кассы".</span><span class="sxs-lookup"><span data-stu-id="435cd-156">Go to Cash and bank management > Setup > Cash posting profiles.</span></span>
2. <span data-ttu-id="435cd-157">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="435cd-157">Click New.</span></span>
3. <span data-ttu-id="435cd-158">В поле "Разноска кассы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-158">In the Cash posting field, type a value.</span></span>
4. <span data-ttu-id="435cd-159">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="435cd-160">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="435cd-160">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="435cd-161">В поле "Допустимо для" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="435cd-161">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="435cd-162">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="435cd-162">In the Main account field, specify the desired values.</span></span>
8. <span data-ttu-id="435cd-163">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-163">Click Save.</span></span>

## <a name="set-up-cash-and-bank-parameters"></a><span data-ttu-id="435cd-164">Настройка параметров банка и кассовых операций</span><span class="sxs-lookup"><span data-stu-id="435cd-164">Set up cash and bank parameters</span></span>
1. <span data-ttu-id="435cd-165">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Параметры управления банком и кассовыми операциями".</span><span class="sxs-lookup"><span data-stu-id="435cd-165">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="435cd-166">Перейдите на вкладку "Наличный расчет".</span><span class="sxs-lookup"><span data-stu-id="435cd-166">Click the Cash tab.</span></span>
3. <span data-ttu-id="435cd-167">В поле "Наличный расчет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-167">In the Cash field, enter or select a value.</span></span>
4. <span data-ttu-id="435cd-168">В поле "Разноска кассы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-168">In the Cash posting field, enter or select a value.</span></span>
5. <span data-ttu-id="435cd-169">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="435cd-169">Click Save.</span></span>
6. <span data-ttu-id="435cd-170">Откройте вкладку Номерные серии.</span><span class="sxs-lookup"><span data-stu-id="435cd-170">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="435cd-171">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="435cd-171">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="435cd-172">В поле "Код номерной серии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-172">In the Number sequence code field, enter or select a value.</span></span>
9. <span data-ttu-id="435cd-173">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="435cd-173">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="435cd-174">В поле "Код номерной серии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-174">In the Number sequence code field, enter or select a value.</span></span>
11. <span data-ttu-id="435cd-175">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-175">Click Save.</span></span>

## <a name="set-up-terms-of-payment"></a><span data-ttu-id="435cd-176">Настройка условий оплаты</span><span class="sxs-lookup"><span data-stu-id="435cd-176">Set up terms of payment</span></span>
1. <span data-ttu-id="435cd-177">Перейдите в раздел "Расчеты с поставщиками" > "Настройка платежей" > "Условия оплаты".</span><span class="sxs-lookup"><span data-stu-id="435cd-177">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="435cd-178">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="435cd-178">Click Edit.</span></span>
3. <span data-ttu-id="435cd-179">Выберите "Да" в поле "От подотчетного лица".</span><span class="sxs-lookup"><span data-stu-id="435cd-179">Select Yes in the From advance holder field.</span></span>
4. <span data-ttu-id="435cd-180">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-180">Click Save.</span></span>

## <a name="create-a-new-worker"></a><span data-ttu-id="435cd-181">Создание нового работника</span><span class="sxs-lookup"><span data-stu-id="435cd-181">Create a new worker</span></span>
1. <span data-ttu-id="435cd-182">Перейдите в раздел "Управление персоналом" > "Работники" > "Работники".</span><span class="sxs-lookup"><span data-stu-id="435cd-182">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="435cd-183">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="435cd-183">Click New.</span></span>
3. <span data-ttu-id="435cd-184">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-184">In the First name field, type a value.</span></span>
4. <span data-ttu-id="435cd-185">В поле "Фамилия" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-185">In the Last name field, type a value.</span></span>
5. <span data-ttu-id="435cd-186">В поле "Код работника" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-186">In the Worker ID field, type a value.</span></span>
6. <span data-ttu-id="435cd-187">Щелкните "Нанять нового работника".</span><span class="sxs-lookup"><span data-stu-id="435cd-187">Click Hire new worker.</span></span>
7. <span data-ttu-id="435cd-188">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-188">Click Save.</span></span>

## <a name="set-up-a-worker-as-an-advance-holder"></a><span data-ttu-id="435cd-189">Настройка работника как подотчетного лица</span><span class="sxs-lookup"><span data-stu-id="435cd-189">Set up a worker as an advance holder</span></span>
1. <span data-ttu-id="435cd-190">Перейдите в раздел "Расчеты с поставщиками" > "Подотчетные лица" > "Подотчетные лица".</span><span class="sxs-lookup"><span data-stu-id="435cd-190">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="435cd-191">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="435cd-191">Click Edit.</span></span>
3. <span data-ttu-id="435cd-192">В поле "Группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-192">In the Group field, enter or select a value.</span></span>
4. <span data-ttu-id="435cd-193">Выберите "Да" в поле "Подотчетное лицо".</span><span class="sxs-lookup"><span data-stu-id="435cd-193">Select Yes in the Advance holder field.</span></span>
5. <span data-ttu-id="435cd-194">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-194">Click Save.</span></span>

## <a name="create-and-post-a-purchase-order-invoice"></a><span data-ttu-id="435cd-195">Создание и разноска накладной по заказу на покупку</span><span class="sxs-lookup"><span data-stu-id="435cd-195">Create and post a purchase order invoice</span></span>
1. <span data-ttu-id="435cd-196">Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="435cd-196">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="435cd-197">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="435cd-197">Click New.</span></span>
3. <span data-ttu-id="435cd-198">В поле "Счет поставщика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-198">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="435cd-199">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="435cd-199">Click OK.</span></span>
5. <span data-ttu-id="435cd-200">В поле "Строки или заголовок" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="435cd-200">In the Lines or header field, select an option.</span></span>
6. <span data-ttu-id="435cd-201">Разверните раздел "Цена и скидка".</span><span class="sxs-lookup"><span data-stu-id="435cd-201">Expand the Price and discount section.</span></span>
7. <span data-ttu-id="435cd-202">В поле "Условия оплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-202">In the Terms of payment field, enter or select a value.</span></span>
8. <span data-ttu-id="435cd-203">В поле "Подотчетное лицо" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-203">In the Advance holder field, enter or select a value.</span></span>
9. <span data-ttu-id="435cd-204">В поле "Строки или заголовок" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="435cd-204">In the Lines or header field, select an option.</span></span>
10. <span data-ttu-id="435cd-205">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="435cd-205">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="435cd-206">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-206">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="435cd-207">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="435cd-207">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="435cd-208">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="435cd-208">In the Unit price field, enter a number.</span></span>
14. <span data-ttu-id="435cd-209">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435cd-209">Click Save.</span></span>
15. <span data-ttu-id="435cd-210">В области действий щелкните "Покупка".</span><span class="sxs-lookup"><span data-stu-id="435cd-210">On the Action Pane, click Purchase.</span></span>
16. <span data-ttu-id="435cd-211">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="435cd-211">Click Confirm.</span></span>
17. <span data-ttu-id="435cd-212">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="435cd-212">On the Action Pane, click Invoice.</span></span>
18. <span data-ttu-id="435cd-213">Щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="435cd-213">Click Invoice.</span></span>
19. <span data-ttu-id="435cd-214">Щелкните "По умолчанию из: количество поступающих продуктов", чтобы открыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="435cd-214">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
20. <span data-ttu-id="435cd-215">В поле "Количество по умолчанию для строк" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="435cd-215">In the Default quantity for lines field, select an option.</span></span>
21. <span data-ttu-id="435cd-216">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="435cd-216">Click OK.</span></span>
22. <span data-ttu-id="435cd-217">В поле "Число" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-217">In the Number field, type a value.</span></span>
23. <span data-ttu-id="435cd-218">В поле "Описание накладной" введите значение.</span><span class="sxs-lookup"><span data-stu-id="435cd-218">In the Invoice description field, type a value.</span></span>
24. <span data-ttu-id="435cd-219">В поле "Дата накладной" введите дату.</span><span class="sxs-lookup"><span data-stu-id="435cd-219">In the Invoice date field, enter a date.</span></span>
25. <span data-ttu-id="435cd-220">В поле "Дата зачета НДС" введите дату.</span><span class="sxs-lookup"><span data-stu-id="435cd-220">In the Date of VAT register field, enter a date.</span></span>
26. <span data-ttu-id="435cd-221">В поле "Дата получения документа" введите дату.</span><span class="sxs-lookup"><span data-stu-id="435cd-221">In the Receive document date field, enter a date.</span></span>
27. <span data-ttu-id="435cd-222">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="435cd-222">Click Post.</span></span>

## <a name="balance-and-close-advance-holders-transactions"></a><span data-ttu-id="435cd-223">Балансировка и закрытие проводок по подотчетным лицам</span><span class="sxs-lookup"><span data-stu-id="435cd-223">Balance and close advance holders transactions</span></span>
1. <span data-ttu-id="435cd-224">Перейдите в раздел "Расчеты с поставщиками" > "Подотчетные лица" > "Подотчетные лица".</span><span class="sxs-lookup"><span data-stu-id="435cd-224">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="435cd-225">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="435cd-225">Click Transactions.</span></span>
3. <span data-ttu-id="435cd-226">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="435cd-226">Close the page.</span></span>
4. <span data-ttu-id="435cd-227">Щелкните "Сальдо".</span><span class="sxs-lookup"><span data-stu-id="435cd-227">Click Balance.</span></span>
5. <span data-ttu-id="435cd-228">Щелкните "Закрытие через банк".</span><span class="sxs-lookup"><span data-stu-id="435cd-228">Click Close via bank.</span></span>
6. <span data-ttu-id="435cd-229">Выберите значение "Да" в поле "Автоматически".</span><span class="sxs-lookup"><span data-stu-id="435cd-229">Select Yes in the Automatic field.</span></span>
7. <span data-ttu-id="435cd-230">В поле "Сумма для переноса."</span><span class="sxs-lookup"><span data-stu-id="435cd-230">In the Amount to be transferred.</span></span> <span data-ttu-id="435cd-231">введите число.</span><span class="sxs-lookup"><span data-stu-id="435cd-231">field, enter a number.</span></span>
8. <span data-ttu-id="435cd-232">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="435cd-232">Click OK.</span></span>
9. <span data-ttu-id="435cd-233">Щелкните "Закрытие через кассу".</span><span class="sxs-lookup"><span data-stu-id="435cd-233">Click Close via cash.</span></span>
10. <span data-ttu-id="435cd-234">Выберите значение "Да" в поле "Автоматически".</span><span class="sxs-lookup"><span data-stu-id="435cd-234">Select Yes in the Automatic field.</span></span>
11. <span data-ttu-id="435cd-235">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="435cd-235">Click OK.</span></span>
12. <span data-ttu-id="435cd-236">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="435cd-236">Close the page.</span></span>
13. <span data-ttu-id="435cd-237">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="435cd-237">Click Transactions.</span></span>

