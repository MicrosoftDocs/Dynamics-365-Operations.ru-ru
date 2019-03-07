---
title: Определение сборов по платежам для клиентов
description: Создайте сборы по платежам для платежей клиентов.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5acb202d46ef39376a01ca592f60926786d11186
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "354836"
---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="5b278-103">Определение сборов по платежам для клиентов</span><span class="sxs-lookup"><span data-stu-id="5b278-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b278-104">Создайте сборы по платежам для платежей клиентов.</span><span class="sxs-lookup"><span data-stu-id="5b278-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="5b278-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="5b278-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="5b278-106">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Сборы по платежам".</span><span class="sxs-lookup"><span data-stu-id="5b278-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="5b278-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="5b278-107">Click New.</span></span>
3. <span data-ttu-id="5b278-108">В поле "Код сбора" введите код сбора.</span><span class="sxs-lookup"><span data-stu-id="5b278-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="5b278-109">Код сбора отображается в журналах платежей, поэтому присвойте ему описательное имя, чтобы пользователи понимали, какой сбор оценивается.</span><span class="sxs-lookup"><span data-stu-id="5b278-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="5b278-110">В поле "Имя" введите имя сбора.</span><span class="sxs-lookup"><span data-stu-id="5b278-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="5b278-111">В поле "Описание сборов" введите описание сбора.</span><span class="sxs-lookup"><span data-stu-id="5b278-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="5b278-112">Укажите, будет ли сбор сниматься со счета клиента или счета ГК.</span><span class="sxs-lookup"><span data-stu-id="5b278-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="5b278-113">Если сбор оценивается для клиента, выберите "Клиент".</span><span class="sxs-lookup"><span data-stu-id="5b278-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="5b278-114">Если сбор оценивается в организации как расход, выберите "Главная книга".</span><span class="sxs-lookup"><span data-stu-id="5b278-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="5b278-115">Для выполнения этой задачи выберите "Клиент".</span><span class="sxs-lookup"><span data-stu-id="5b278-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="5b278-116">Выберите тип журнала, в котором может использоваться этот сбор по платежам.</span><span class="sxs-lookup"><span data-stu-id="5b278-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="5b278-117">Если эти сборы используются для платежей клиентов, типом журнала, скорее всего, будет "Клиентский платеж".</span><span class="sxs-lookup"><span data-stu-id="5b278-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="5b278-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5b278-118">Click Save.</span></span>
9. <span data-ttu-id="5b278-119">Щелкните "Настройка сборов по платежам".</span><span class="sxs-lookup"><span data-stu-id="5b278-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="5b278-120">Настройка сборов по платежам используется для определения критериев времени оценки сборов по платежам.</span><span class="sxs-lookup"><span data-stu-id="5b278-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="5b278-121">Например, можно указать, что сбор будет рассчитываться, если используется банковский счет USMF OPER и способом оплаты является чек.</span><span class="sxs-lookup"><span data-stu-id="5b278-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="5b278-122">Выберите значение "Таблица", "Группа" или "Все", чтобы определить, какие банковские счета будут оцениваться для этого сбора.</span><span class="sxs-lookup"><span data-stu-id="5b278-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="5b278-123">Если выбрать значение "Все", все банковские счета могут быть оценены для этого сбора.</span><span class="sxs-lookup"><span data-stu-id="5b278-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="5b278-124">Если выбрать значение "Таблица", только выбранный банковский счет может быть оценен для этого сбора.</span><span class="sxs-lookup"><span data-stu-id="5b278-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="5b278-125">Если выбрать значение "Группа", только банковские счета в выбранной банковской группе могут быть оценены для этого сбора.</span><span class="sxs-lookup"><span data-stu-id="5b278-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="5b278-126">Выбор банковскую группу или банковский счет.</span><span class="sxs-lookup"><span data-stu-id="5b278-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="5b278-127">Если выбрать значение "Таблица", в результатах поиска отобразятся банковские счета.</span><span class="sxs-lookup"><span data-stu-id="5b278-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="5b278-128">Если выбрать значение "Группа", в результатах поиска отобразятся банковские группы.</span><span class="sxs-lookup"><span data-stu-id="5b278-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="5b278-129">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="5b278-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="5b278-130">Выберите способ оплаты, для которого будет оцениваться этот сбор.</span><span class="sxs-lookup"><span data-stu-id="5b278-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="5b278-131">Например, можно оценить сбор для клиентов, если они отправляют платежи в виде чека, а не электронного платежа.</span><span class="sxs-lookup"><span data-stu-id="5b278-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="5b278-132">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5b278-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="5b278-133">При необходимости введите валюту платежа.</span><span class="sxs-lookup"><span data-stu-id="5b278-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="5b278-134">Валюта платежа используется в качестве дополнительных критериев для указания того, будет ли оцениваться сбор.</span><span class="sxs-lookup"><span data-stu-id="5b278-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="5b278-135">Например, ваш банк может взимать дополнительный сбор для платежей, получаемых в долларах США, поскольку обычно операции в банке выполняются только в евро.</span><span class="sxs-lookup"><span data-stu-id="5b278-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="5b278-136">Выберите значение сбора: процент, сумма или интервал.</span><span class="sxs-lookup"><span data-stu-id="5b278-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="5b278-137">Введите процент или сумму сбора.</span><span class="sxs-lookup"><span data-stu-id="5b278-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="5b278-138">Если в поле "Процент/Сумма" выбрано значение "Процент", то вводимое здесь значение будет процентом.</span><span class="sxs-lookup"><span data-stu-id="5b278-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="5b278-139">Если в поле "Процент/Сумма" выбрано значение "Сумма", то вводимое здесь значение будет суммой.</span><span class="sxs-lookup"><span data-stu-id="5b278-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="5b278-140">Если в поле "Процент/Сумма" выбрано значение "Интервал", используйте вкладку "Интервал" для определения уровней.</span><span class="sxs-lookup"><span data-stu-id="5b278-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="5b278-141">В поле "Валюта сбора" выберите валюту сбора.</span><span class="sxs-lookup"><span data-stu-id="5b278-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="5b278-142">Это валюта, в которой будут создаваться сборы.</span><span class="sxs-lookup"><span data-stu-id="5b278-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="5b278-143">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5b278-143">Click Save.</span></span>

