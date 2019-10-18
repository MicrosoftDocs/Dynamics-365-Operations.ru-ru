---
title: Создание платежей для клиента с поручениями на безакцептное списание
description: В этой процедуре демонстрируется создание файла платежа прямого дебетования ISO20022 для клиента, для которого настроено прямое дебетование и накладная, подлежащая оплате.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 129c5291a29994f91ef325aa9b9a3b54a0e958d6
ms.sourcegitcommit: 807dec193cd163c9f5d949e744cfde40f2eb24b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2019
ms.locfileid: "2468963"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="1906a-103">Создание платежей для клиента с поручениями на безакцептное списание</span><span class="sxs-lookup"><span data-stu-id="1906a-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1906a-104">В этой процедуре демонстрируется создание файла платежа прямого дебетования ISO20022 для клиента, для которого настроено прямое дебетование и накладная, подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="1906a-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="1906a-105">Создание и разноска накладной не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="1906a-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="1906a-106">Вместо задания накладной, подлежащей оплате, можно выбрать поручение в журнале перед созданием файла платежа для поддержки сценарий предоплаты клиента.</span><span class="sxs-lookup"><span data-stu-id="1906a-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="1906a-107">В качестве компании с демонстрационными данными для создания этой процедуры используется DEMF.</span><span class="sxs-lookup"><span data-stu-id="1906a-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="1906a-108">Это пятая процедура из пяти, которые демонстрируют процесс платежа клиентов с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="1906a-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="1906a-109">Перед выполнением этой задачи необходимо выполнить предыдущие задачи.</span><span class="sxs-lookup"><span data-stu-id="1906a-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="1906a-110">Сначала следует импортировать конфигурации электронной отчетности по платежам клиентов, настроить метод платежей и настроить компанию и сведения о клиенте.</span><span class="sxs-lookup"><span data-stu-id="1906a-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="1906a-111">Разноска накладной с произвольным текстом со сведениями прямого дебетования</span><span class="sxs-lookup"><span data-stu-id="1906a-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="1906a-112">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Все накладные с произвольным текстом".</span><span class="sxs-lookup"><span data-stu-id="1906a-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="1906a-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1906a-113">Click New.</span></span>
3. <span data-ttu-id="1906a-114">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1906a-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="1906a-115">Например, выберите DE-010.</span><span class="sxs-lookup"><span data-stu-id="1906a-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="1906a-116">В поле "Способ оплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1906a-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="1906a-117">Например,</span><span class="sxs-lookup"><span data-stu-id="1906a-117">For example.</span></span> <span data-ttu-id="1906a-118">выберите "Электронно".</span><span class="sxs-lookup"><span data-stu-id="1906a-118">select Electronic.</span></span>  
5. <span data-ttu-id="1906a-119">В поле код предписания прямого дебетования введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1906a-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="1906a-120">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="1906a-120">Click Add line.</span></span>
7. <span data-ttu-id="1906a-121">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1906a-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="1906a-122">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="1906a-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="1906a-123">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="1906a-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="1906a-124">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="1906a-124">Click Post.</span></span>
11. <span data-ttu-id="1906a-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1906a-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="1906a-126">Создание платежа</span><span class="sxs-lookup"><span data-stu-id="1906a-126">Create a payment</span></span>
1. <span data-ttu-id="1906a-127">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="1906a-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="1906a-128">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1906a-128">Click New.</span></span>
3. <span data-ttu-id="1906a-129">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1906a-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="1906a-130">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="1906a-130">Click Lines.</span></span>
5. <span data-ttu-id="1906a-131">Щелкните "Предложение по оплате".</span><span class="sxs-lookup"><span data-stu-id="1906a-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="1906a-132">Щелкните "Создать предложение по оплате".</span><span class="sxs-lookup"><span data-stu-id="1906a-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="1906a-133">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="1906a-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="1906a-134">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="1906a-134">Click Filter.</span></span>
9. <span data-ttu-id="1906a-135">В списке выберите строку для таблицы "Проводки клиента" и поля "Способ оплаты".</span><span class="sxs-lookup"><span data-stu-id="1906a-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="1906a-136">Можно применить любые критерии выбора проводки клиента для оплаты.</span><span class="sxs-lookup"><span data-stu-id="1906a-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="1906a-137">В этом примере для фильтрации проводок используется способ оплаты "Электронно".</span><span class="sxs-lookup"><span data-stu-id="1906a-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="1906a-138">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1906a-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="1906a-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1906a-139">Click OK.</span></span>
12. <span data-ttu-id="1906a-140">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1906a-140">Click OK.</span></span>
13. <span data-ttu-id="1906a-141">Щелкните "Создать платежи".</span><span class="sxs-lookup"><span data-stu-id="1906a-141">Click Create payments.</span></span>
