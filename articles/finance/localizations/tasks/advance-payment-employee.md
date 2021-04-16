---
title: EEU-00047 Авансовый платеж сотруднику
description: Эта процедура демонстрирует, как настраивать и регистрировать проводки для подотчетного лица.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RCashTable, LedgerJournalSetup, HcmWorkerGroup_RU, EmplPosting_RU, VendParameters, RCashPosting, BankParameters, PaymTerm, HcmWorker, HcmWorkerNewWorker, HcmWorkerAdvHolderTableListPage_RU, HcmWorkerAdvHolderTable_RU, PurchTable, PurchCreateOrder, HcmAdvHolderLookup_RU, InventItemIdLookupPurchase, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, EmplTrans_RU, EmplBalance_RU
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cfdbdf30c9900b792c57a26e4a4d4f4a8830cebc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832543"
---
# <a name="eeu-00047-advance-payment-to-employee"></a><span data-ttu-id="4745a-103">EEU-00047 Авансовый платеж сотруднику</span><span class="sxs-lookup"><span data-stu-id="4745a-103">EEU-00047 Advance payment to employee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4745a-104">Эта процедура демонстрирует, как настраивать и регистрировать проводки для подотчетного лица.</span><span class="sxs-lookup"><span data-stu-id="4745a-104">This procedure demonstrates how to set up and register transactions for an advance holder.</span></span> <span data-ttu-id="4745a-105">Эта процедура была создана с использованием компании с демонстрационными данными DEMF с основным адресом в Литве.</span><span class="sxs-lookup"><span data-stu-id="4745a-105">This procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="4745a-106">Эта задача работает только для юридических лиц с основным адресом в Польше, Литве, Латвии, Эстонии, Чехии или Венгрии.</span><span class="sxs-lookup"><span data-stu-id="4745a-106">This task only works for legal entities with a primary address in Poland, Lithuania, Latvia, Estonia, Czech Republic, or Hungary.</span></span> <span data-ttu-id="4745a-107">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="4745a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-cash-account"></a><span data-ttu-id="4745a-108">Создать новый кассовый счет</span><span class="sxs-lookup"><span data-stu-id="4745a-108">Create a new cash account</span></span>
1. <span data-ttu-id="4745a-109">Перейдите в раздел "Управление банком и кассовыми операциями" > "Банковские счета" > "Кассы".</span><span class="sxs-lookup"><span data-stu-id="4745a-109">Go to Cash and bank management > Bank accounts > Cash accounts.</span></span>
2. <span data-ttu-id="4745a-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4745a-110">Click New.</span></span>
3. <span data-ttu-id="4745a-111">В поле "Наличный расчет" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-111">In the Cash field, type a value.</span></span>
4. <span data-ttu-id="4745a-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4745a-113">В поле "Группа номерных серий" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-113">In the Number sequence group field, enter or select a value.</span></span>
6. <span data-ttu-id="4745a-114">Разверните раздел "Проверка".</span><span class="sxs-lookup"><span data-stu-id="4745a-114">Expand the Validation section.</span></span>
7. <span data-ttu-id="4745a-115">В поле "Валюта" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-115">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="4745a-116">Выберите "Да" в поле "Отрицательная касса".</span><span class="sxs-lookup"><span data-stu-id="4745a-116">Select Yes in the Negative cash field.</span></span>
9. <span data-ttu-id="4745a-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-117">Click Save.</span></span>

## <a name="create-a-new-journal"></a><span data-ttu-id="4745a-118">Создание нового журнала.</span><span class="sxs-lookup"><span data-stu-id="4745a-118">Create a new journal</span></span>
1. <span data-ttu-id="4745a-119">Перейдите в раздел "Главная книга" > "Настройка журнала" > "Наименования журналов".</span><span class="sxs-lookup"><span data-stu-id="4745a-119">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="4745a-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4745a-120">Click New.</span></span>
3. <span data-ttu-id="4745a-121">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="4745a-122">В поле "Серии ваучеров" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-122">In the Voucher series field, enter or select a value.</span></span>
5. <span data-ttu-id="4745a-123">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-123">Click Save.</span></span>
6. <span data-ttu-id="4745a-124">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4745a-124">Click New.</span></span>
7. <span data-ttu-id="4745a-125">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-125">In the Name field, type a value.</span></span>
8. <span data-ttu-id="4745a-126">В поле "Тип журнала" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="4745a-126">In the Journal type field, select an option.</span></span>
9. <span data-ttu-id="4745a-127">В поле "Серии ваучеров" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-127">In the Voucher series field, enter or select a value.</span></span>
10. <span data-ttu-id="4745a-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-128">Click Save.</span></span>

## <a name="create-an-advance-holder-group"></a><span data-ttu-id="4745a-129">Создание группы подотчетных лиц</span><span class="sxs-lookup"><span data-stu-id="4745a-129">Create an advance holder group</span></span>
1. <span data-ttu-id="4745a-130">Перейдите в раздел "Расчеты с поставщиками" > "Настройка" > "Подотчетные лица" > "Группы подотчетных лиц".</span><span class="sxs-lookup"><span data-stu-id="4745a-130">Go to Accounts payable > Setup > Advance holders > Advance holder groups.</span></span>
2. <span data-ttu-id="4745a-131">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4745a-131">Click New.</span></span>
3. <span data-ttu-id="4745a-132">В поле "Группа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-132">In the Group field, type a value.</span></span>
4. <span data-ttu-id="4745a-133">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4745a-134">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-134">Click Save.</span></span>

## <a name="create-an-employee-posting-profile"></a><span data-ttu-id="4745a-135">Создание профиля разноски сотрудника</span><span class="sxs-lookup"><span data-stu-id="4745a-135">Create an employee posting profile</span></span>
1. <span data-ttu-id="4745a-136">Перейдите в раздел "Расчеты с поставщиками" > "Настройка" > "Подотчетные лица" >"Профили разноски по подотч. лицам".</span><span class="sxs-lookup"><span data-stu-id="4745a-136">Go to Accounts payable > Setup > Advance holders > Employee posting profiles.</span></span>
2. <span data-ttu-id="4745a-137">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4745a-137">Click New.</span></span>
3. <span data-ttu-id="4745a-138">В поле "Профиль разноски" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-138">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="4745a-139">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-139">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4745a-140">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4745a-140">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="4745a-141">В поле "Допустимо для" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="4745a-141">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="4745a-142">В поле "Суммарный счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="4745a-142">In the Summary account field, specify the desired values.</span></span>
8. <span data-ttu-id="4745a-143">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-143">Click Save.</span></span>

## <a name="set-up-advance-holder-parameters"></a><span data-ttu-id="4745a-144">Настройка параметров подотчетных лиц</span><span class="sxs-lookup"><span data-stu-id="4745a-144">Set up advance holder parameters</span></span>
1. <span data-ttu-id="4745a-145">Перейдите в раздел "Расчеты с поставщиками" > "Настройка" > "Параметры расчетов с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="4745a-145">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="4745a-146">Выберите вкладку "Подотчетные лица".</span><span class="sxs-lookup"><span data-stu-id="4745a-146">Click the Advance holders tab.</span></span>
3. <span data-ttu-id="4745a-147">В поле "Профиль разноски" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-147">In the Posting profile field, enter or select a value.</span></span>
4. <span data-ttu-id="4745a-148">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-148">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="4745a-149">В поле "Наличный расчет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-149">In the Cash field, enter or select a value.</span></span>
6. <span data-ttu-id="4745a-150">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-150">In the Name field, enter or select a value.</span></span>
7. <span data-ttu-id="4745a-151">В поле "Тип счета" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="4745a-151">In the Account type field, select an option.</span></span>
8. <span data-ttu-id="4745a-152">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="4745a-152">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="4745a-153">Откройте вкладку Номерные серии.</span><span class="sxs-lookup"><span data-stu-id="4745a-153">Click the Number sequences tab.</span></span>
10. <span data-ttu-id="4745a-154">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-154">Click Save.</span></span>

## <a name="set-up-a-cash-posting-profile"></a><span data-ttu-id="4745a-155">Настройка профиля разноски кассы</span><span class="sxs-lookup"><span data-stu-id="4745a-155">Set up a cash posting profile</span></span>
1. <span data-ttu-id="4745a-156">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Профили разноски кассы".</span><span class="sxs-lookup"><span data-stu-id="4745a-156">Go to Cash and bank management > Setup > Cash posting profiles.</span></span>
2. <span data-ttu-id="4745a-157">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4745a-157">Click New.</span></span>
3. <span data-ttu-id="4745a-158">В поле "Разноска кассы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-158">In the Cash posting field, type a value.</span></span>
4. <span data-ttu-id="4745a-159">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4745a-160">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4745a-160">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="4745a-161">В поле "Допустимо для" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="4745a-161">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="4745a-162">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="4745a-162">In the Main account field, specify the desired values.</span></span>
8. <span data-ttu-id="4745a-163">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-163">Click Save.</span></span>

## <a name="set-up-cash-and-bank-parameters"></a><span data-ttu-id="4745a-164">Настройка параметров банка и кассовых операций</span><span class="sxs-lookup"><span data-stu-id="4745a-164">Set up cash and bank parameters</span></span>
1. <span data-ttu-id="4745a-165">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Параметры управления банком и кассовыми операциями".</span><span class="sxs-lookup"><span data-stu-id="4745a-165">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="4745a-166">Перейдите на вкладку "Наличный расчет".</span><span class="sxs-lookup"><span data-stu-id="4745a-166">Click the Cash tab.</span></span>
3. <span data-ttu-id="4745a-167">В поле "Наличный расчет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-167">In the Cash field, enter or select a value.</span></span>
4. <span data-ttu-id="4745a-168">В поле "Разноска кассы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-168">In the Cash posting field, enter or select a value.</span></span>
5. <span data-ttu-id="4745a-169">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="4745a-169">Click Save.</span></span>
6. <span data-ttu-id="4745a-170">Откройте вкладку Номерные серии.</span><span class="sxs-lookup"><span data-stu-id="4745a-170">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="4745a-171">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4745a-171">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="4745a-172">В поле "Код номерной серии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-172">In the Number sequence code field, enter or select a value.</span></span>
9. <span data-ttu-id="4745a-173">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4745a-173">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="4745a-174">В поле "Код номерной серии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-174">In the Number sequence code field, enter or select a value.</span></span>
11. <span data-ttu-id="4745a-175">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-175">Click Save.</span></span>

## <a name="set-up-terms-of-payment"></a><span data-ttu-id="4745a-176">Настройка условий оплаты</span><span class="sxs-lookup"><span data-stu-id="4745a-176">Set up terms of payment</span></span>
1. <span data-ttu-id="4745a-177">Перейдите в раздел "Расчеты с поставщиками" > "Настройка платежей" > "Условия оплаты".</span><span class="sxs-lookup"><span data-stu-id="4745a-177">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="4745a-178">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="4745a-178">Click Edit.</span></span>
3. <span data-ttu-id="4745a-179">Выберите "Да" в поле "От подотчетного лица".</span><span class="sxs-lookup"><span data-stu-id="4745a-179">Select Yes in the From advance holder field.</span></span>
4. <span data-ttu-id="4745a-180">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-180">Click Save.</span></span>

## <a name="create-a-new-worker"></a><span data-ttu-id="4745a-181">Создание нового работника</span><span class="sxs-lookup"><span data-stu-id="4745a-181">Create a new worker</span></span>
1. <span data-ttu-id="4745a-182">Перейдите в раздел "Управление персоналом" > "Работники" > "Работники".</span><span class="sxs-lookup"><span data-stu-id="4745a-182">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="4745a-183">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4745a-183">Click New.</span></span>
3. <span data-ttu-id="4745a-184">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-184">In the First name field, type a value.</span></span>
4. <span data-ttu-id="4745a-185">В поле "Фамилия" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-185">In the Last name field, type a value.</span></span>
5. <span data-ttu-id="4745a-186">В поле "Код работника" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-186">In the Worker ID field, type a value.</span></span>
6. <span data-ttu-id="4745a-187">Щелкните "Нанять нового работника".</span><span class="sxs-lookup"><span data-stu-id="4745a-187">Click Hire new worker.</span></span>
7. <span data-ttu-id="4745a-188">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-188">Click Save.</span></span>

## <a name="set-up-a-worker-as-an-advance-holder"></a><span data-ttu-id="4745a-189">Настройка работника как подотчетного лица</span><span class="sxs-lookup"><span data-stu-id="4745a-189">Set up a worker as an advance holder</span></span>
1. <span data-ttu-id="4745a-190">Перейдите в раздел "Расчеты с поставщиками" > "Подотчетные лица" > "Подотчетные лица".</span><span class="sxs-lookup"><span data-stu-id="4745a-190">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="4745a-191">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="4745a-191">Click Edit.</span></span>
3. <span data-ttu-id="4745a-192">В поле "Группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-192">In the Group field, enter or select a value.</span></span>
4. <span data-ttu-id="4745a-193">Выберите "Да" в поле "Подотчетное лицо".</span><span class="sxs-lookup"><span data-stu-id="4745a-193">Select Yes in the Advance holder field.</span></span>
5. <span data-ttu-id="4745a-194">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-194">Click Save.</span></span>

## <a name="create-and-post-a-purchase-order-invoice"></a><span data-ttu-id="4745a-195">Создание и разноска накладной по заказу на покупку</span><span class="sxs-lookup"><span data-stu-id="4745a-195">Create and post a purchase order invoice</span></span>
1. <span data-ttu-id="4745a-196">Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="4745a-196">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="4745a-197">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4745a-197">Click New.</span></span>
3. <span data-ttu-id="4745a-198">В поле "Счет поставщика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-198">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="4745a-199">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="4745a-199">Click OK.</span></span>
5. <span data-ttu-id="4745a-200">В поле "Строки или заголовок" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="4745a-200">In the Lines or header field, select an option.</span></span>
6. <span data-ttu-id="4745a-201">Разверните раздел "Цена и скидка".</span><span class="sxs-lookup"><span data-stu-id="4745a-201">Expand the Price and discount section.</span></span>
7. <span data-ttu-id="4745a-202">В поле "Условия оплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-202">In the Terms of payment field, enter or select a value.</span></span>
8. <span data-ttu-id="4745a-203">В поле "Подотчетное лицо" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-203">In the Advance holder field, enter or select a value.</span></span>
9. <span data-ttu-id="4745a-204">В поле "Строки или заголовок" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="4745a-204">In the Lines or header field, select an option.</span></span>
10. <span data-ttu-id="4745a-205">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4745a-205">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="4745a-206">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-206">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="4745a-207">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="4745a-207">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="4745a-208">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="4745a-208">In the Unit price field, enter a number.</span></span>
14. <span data-ttu-id="4745a-209">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4745a-209">Click Save.</span></span>
15. <span data-ttu-id="4745a-210">В области действий щелкните "Покупка".</span><span class="sxs-lookup"><span data-stu-id="4745a-210">On the Action Pane, click Purchase.</span></span>
16. <span data-ttu-id="4745a-211">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="4745a-211">Click Confirm.</span></span>
17. <span data-ttu-id="4745a-212">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="4745a-212">On the Action Pane, click Invoice.</span></span>
18. <span data-ttu-id="4745a-213">Щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="4745a-213">Click Invoice.</span></span>
19. <span data-ttu-id="4745a-214">Щелкните "По умолчанию из: количество поступающих продуктов", чтобы открыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4745a-214">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
20. <span data-ttu-id="4745a-215">В поле "Количество по умолчанию для строк" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="4745a-215">In the Default quantity for lines field, select an option.</span></span>
21. <span data-ttu-id="4745a-216">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="4745a-216">Click OK.</span></span>
22. <span data-ttu-id="4745a-217">В поле "Число" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-217">In the Number field, type a value.</span></span>
23. <span data-ttu-id="4745a-218">В поле "Описание накладной" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4745a-218">In the Invoice description field, type a value.</span></span>
24. <span data-ttu-id="4745a-219">В поле "Дата накладной" введите дату.</span><span class="sxs-lookup"><span data-stu-id="4745a-219">In the Invoice date field, enter a date.</span></span>
25. <span data-ttu-id="4745a-220">В поле "Дата зачета НДС" введите дату.</span><span class="sxs-lookup"><span data-stu-id="4745a-220">In the Date of VAT register field, enter a date.</span></span>
26. <span data-ttu-id="4745a-221">В поле "Дата получения документа" введите дату.</span><span class="sxs-lookup"><span data-stu-id="4745a-221">In the Receive document date field, enter a date.</span></span>
27. <span data-ttu-id="4745a-222">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="4745a-222">Click Post.</span></span>

## <a name="balance-and-close-advance-holders-transactions"></a><span data-ttu-id="4745a-223">Балансировка и закрытие проводок по подотчетным лицам</span><span class="sxs-lookup"><span data-stu-id="4745a-223">Balance and close advance holders transactions</span></span>
1. <span data-ttu-id="4745a-224">Перейдите в раздел "Расчеты с поставщиками" > "Подотчетные лица" > "Подотчетные лица".</span><span class="sxs-lookup"><span data-stu-id="4745a-224">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="4745a-225">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="4745a-225">Click Transactions.</span></span>
3. <span data-ttu-id="4745a-226">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4745a-226">Close the page.</span></span>
4. <span data-ttu-id="4745a-227">Щелкните "Сальдо".</span><span class="sxs-lookup"><span data-stu-id="4745a-227">Click Balance.</span></span>
5. <span data-ttu-id="4745a-228">Щелкните "Закрытие через банк".</span><span class="sxs-lookup"><span data-stu-id="4745a-228">Click Close via bank.</span></span>
6. <span data-ttu-id="4745a-229">Выберите значение "Да" в поле "Автоматически".</span><span class="sxs-lookup"><span data-stu-id="4745a-229">Select Yes in the Automatic field.</span></span>
7. <span data-ttu-id="4745a-230">В поле "Сумма для переноса."</span><span class="sxs-lookup"><span data-stu-id="4745a-230">In the Amount to be transferred.</span></span> <span data-ttu-id="4745a-231">введите число.</span><span class="sxs-lookup"><span data-stu-id="4745a-231">field, enter a number.</span></span>
8. <span data-ttu-id="4745a-232">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4745a-232">Click OK.</span></span>
9. <span data-ttu-id="4745a-233">Щелкните "Закрытие через кассу".</span><span class="sxs-lookup"><span data-stu-id="4745a-233">Click Close via cash.</span></span>
10. <span data-ttu-id="4745a-234">Выберите значение "Да" в поле "Автоматически".</span><span class="sxs-lookup"><span data-stu-id="4745a-234">Select Yes in the Automatic field.</span></span>
11. <span data-ttu-id="4745a-235">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4745a-235">Click OK.</span></span>
12. <span data-ttu-id="4745a-236">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4745a-236">Close the page.</span></span>
13. <span data-ttu-id="4745a-237">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="4745a-237">Click Transactions.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]