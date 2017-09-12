--- 
title: "Определение сборов по платежам поставщиков"
description: "Настройте сборы по платежам поставщику."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f62d07ffa1ee4a525f0f266922bc88e5ac8d5ada
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="a11c9-103">Определение сборов по платежам поставщиков</span><span class="sxs-lookup"><span data-stu-id="a11c9-103">Define vendor payment fees</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a11c9-104">Настройте сборы по платежам поставщику.</span><span class="sxs-lookup"><span data-stu-id="a11c9-104">Set up vendor payment fees.</span></span> <span data-ttu-id="a11c9-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="a11c9-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a11c9-106">Перейдите в раздел "Расчеты с поставщиками" > "Настройка платежей" > "Сборы по платежам".</span><span class="sxs-lookup"><span data-stu-id="a11c9-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="a11c9-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a11c9-107">Click New.</span></span>
3. <span data-ttu-id="a11c9-108">В поле "Код сбора" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a11c9-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="a11c9-109">Код сбора должен описывать ситуации, когда этот сбор будет использоваться, например "Сбор_EFT".</span><span class="sxs-lookup"><span data-stu-id="a11c9-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="a11c9-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a11c9-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a11c9-111">В поле "Описание сборов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a11c9-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="a11c9-112">Добавьте описание, чтобы предоставить дополнительные сведения о том, когда оценивается сбор.</span><span class="sxs-lookup"><span data-stu-id="a11c9-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="a11c9-113">В поле "Накладные расходы" выберите значение "Поставщик" или "Главная книга".</span><span class="sxs-lookup"><span data-stu-id="a11c9-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="a11c9-114">Главная книга используется, когда сбор будет списан в расход в организации.</span><span class="sxs-lookup"><span data-stu-id="a11c9-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="a11c9-115">Поставщик используется, когда сбор будет оценен для поставщика.</span><span class="sxs-lookup"><span data-stu-id="a11c9-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="a11c9-116">Введите счет ГК, для которого сбор будет списан в расход.</span><span class="sxs-lookup"><span data-stu-id="a11c9-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="a11c9-117">Этот параметр доступен только в случае, если выбрано значение "Главная книга" для параметра "Накладные расходы".</span><span class="sxs-lookup"><span data-stu-id="a11c9-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="a11c9-118">Выберите журнал, в котором может использоваться этот сбор.</span><span class="sxs-lookup"><span data-stu-id="a11c9-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="a11c9-119">Для сборов по платежам поставщику можно выбрать журнал "Выплата поставщику".</span><span class="sxs-lookup"><span data-stu-id="a11c9-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="a11c9-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a11c9-120">Click Save.</span></span>
10. <span data-ttu-id="a11c9-121">Щелкните "Настройка сборов по платежам".</span><span class="sxs-lookup"><span data-stu-id="a11c9-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="a11c9-122">Перейдите к настройке сборов по платежам, чтобы указать, когда сбор должен использоваться по умолчанию в выбранном журнале.</span><span class="sxs-lookup"><span data-stu-id="a11c9-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="a11c9-123">Выберите значение "Таблица", "Группа" или "Все".</span><span class="sxs-lookup"><span data-stu-id="a11c9-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="a11c9-124">Значение "Таблица" используется для выбора одного банковского счета, значение "Группа" используется для выбора банковской группы, значение "Все" используется для указания того, что данная настройка сборов применяется ко всем банковским счетам.</span><span class="sxs-lookup"><span data-stu-id="a11c9-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="a11c9-125">Выбор банковскую группу или банковский счет.</span><span class="sxs-lookup"><span data-stu-id="a11c9-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="a11c9-126">В результатах поиска отобразится банковская группа, если выбрано значение "Группа", или банковские счета, если выбрано значение "Таблица".</span><span class="sxs-lookup"><span data-stu-id="a11c9-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="a11c9-127">Выберите способ оплаты, для которого будет оцениваться этот сбор.</span><span class="sxs-lookup"><span data-stu-id="a11c9-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="a11c9-128">Выберите спецификацию оплаты для выбранного способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="a11c9-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="a11c9-129">Спецификация оплаты используется при использовании электронного платежа как способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="a11c9-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="a11c9-130">Выберите значение сбора: процент, сумма или интервал.</span><span class="sxs-lookup"><span data-stu-id="a11c9-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="a11c9-131">Введите процент или сумму сбора.</span><span class="sxs-lookup"><span data-stu-id="a11c9-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="a11c9-132">Если для параметра "Сбор" задано значение "Процент", введите процент.</span><span class="sxs-lookup"><span data-stu-id="a11c9-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="a11c9-133">Если для параметра "Сбор" задано значение "Сумма", введите сумму сбора.</span><span class="sxs-lookup"><span data-stu-id="a11c9-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="a11c9-134">Если для параметра "Сбор" задано значение "Интервал", воспользуйтесь вкладкой "Интервал", чтобы определить многоуровневые сборы.</span><span class="sxs-lookup"><span data-stu-id="a11c9-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="a11c9-135">В поле "Валюта сбора" выберите валюту, в которой будет оцениваться сбор.</span><span class="sxs-lookup"><span data-stu-id="a11c9-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="a11c9-136">Эта валюта используется для сбора.</span><span class="sxs-lookup"><span data-stu-id="a11c9-136">This currency is for the fee.</span></span> <span data-ttu-id="a11c9-137">Валюта платежа используется для определения того, когда должно оцениваться правило сбора на основании валюты платежа.</span><span class="sxs-lookup"><span data-stu-id="a11c9-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="a11c9-138">Например, ваш банк может взимать сбор при осуществлении платежа в евро, но все другие платежи не оцениваются как сбор.</span><span class="sxs-lookup"><span data-stu-id="a11c9-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="a11c9-139">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a11c9-139">Click Save.</span></span>


