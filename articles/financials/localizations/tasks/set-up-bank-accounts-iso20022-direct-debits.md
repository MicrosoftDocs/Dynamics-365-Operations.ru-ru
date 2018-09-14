--- 
title: "Настройка клиентов и банковских счетов клиентов для безакцептного списания ISO20022"
description: "В этой задаче описывается настройка банковского счета клиента и поручения на безакцептное списание клиента, которые необходимы для создания файла платежа клиента, такого как прямое дебетование ISO20022."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e7d7d79b1d496223b027d800beca105ecaa0bd4c
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="95c4c-103">Настройка клиентов и банковских счетов клиентов для безакцептного списания ISO20022</span><span class="sxs-lookup"><span data-stu-id="95c4c-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95c4c-104">В этой задаче описывается настройка банковского счета клиента и поручения на безакцептное списание клиента, которые необходимы для создания файла платежа клиента, такого как прямое дебетование ISO20022.</span><span class="sxs-lookup"><span data-stu-id="95c4c-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="95c4c-105">В зависимости от настроенных форматов платежей клиентов, дополнительные сведения, не рассматриваемые в этой процедуре, могут потребоваться для клиента или банковского счета клиента.</span><span class="sxs-lookup"><span data-stu-id="95c4c-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="95c4c-106">Эта задача была создана с использованием компании с демонстрационными данными DEMF с основным адресом юридического лица в Германии.</span><span class="sxs-lookup"><span data-stu-id="95c4c-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="95c4c-107">Это четвертая процедура из пяти, которые демонстрируют процесс платежа клиентов с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="95c4c-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="95c4c-108">Настройка банковского счета клиента</span><span class="sxs-lookup"><span data-stu-id="95c4c-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="95c4c-109">Перейдите в раздел "Расчеты с клиентами" > "Клиенты" > "Все клиенты".</span><span class="sxs-lookup"><span data-stu-id="95c4c-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="95c4c-110">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="95c4c-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="95c4c-111">Например, отфильтруйте поле "Счет" по значению "DE-010".</span><span class="sxs-lookup"><span data-stu-id="95c4c-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="95c4c-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="95c4c-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="95c4c-113">В области действий щелкните "Клиент".</span><span class="sxs-lookup"><span data-stu-id="95c4c-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="95c4c-114">Щелкните "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="95c4c-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="95c4c-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="95c4c-115">Click New.</span></span>
7. <span data-ttu-id="95c4c-116">В поле "Банковский счет" введите значение.</span><span class="sxs-lookup"><span data-stu-id="95c4c-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="95c4c-117">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="95c4c-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="95c4c-118">Например, введите "Банк EUR".</span><span class="sxs-lookup"><span data-stu-id="95c4c-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="95c4c-119">В поле "Банковские группы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="95c4c-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="95c4c-120">В поле "IBAN" введите значение.</span><span class="sxs-lookup"><span data-stu-id="95c4c-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="95c4c-121">Например, введите "DE36200400000628808808".</span><span class="sxs-lookup"><span data-stu-id="95c4c-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="95c4c-122">В поле "SWIFT-код" введите значение.</span><span class="sxs-lookup"><span data-stu-id="95c4c-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="95c4c-123">Например, введите "COBADEFFXXX".</span><span class="sxs-lookup"><span data-stu-id="95c4c-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="95c4c-124">Обратите внимание, что SWIFT\BIC не является обязательным для многих форматов платежей, однако рекомендуется, чтобы этот код был зарегистрирован для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="95c4c-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="95c4c-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="95c4c-125">Click Save.</span></span>
13. <span data-ttu-id="95c4c-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="95c4c-126">Close the page.</span></span>
14. <span data-ttu-id="95c4c-127">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="95c4c-127">Click Edit.</span></span>
15. <span data-ttu-id="95c4c-128">Разверните раздел "Значения платежа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="95c4c-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="95c4c-129">В поле "Банковский счет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="95c4c-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="95c4c-130">Добавление поручения на безакцептное списание</span><span class="sxs-lookup"><span data-stu-id="95c4c-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="95c4c-131">Разверните раздел "Поручения на безакцептное списание".</span><span class="sxs-lookup"><span data-stu-id="95c4c-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="95c4c-132">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="95c4c-132">Click Add.</span></span>
3. <span data-ttu-id="95c4c-133">В поле "Банковский счет кредитора" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="95c4c-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="95c4c-134">Например, выберите DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="95c4c-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="95c4c-135">В поле "Дата подписи" введите дату.</span><span class="sxs-lookup"><span data-stu-id="95c4c-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="95c4c-136">Щелкните "Да", чтобы подтвердить обновление даты.</span><span class="sxs-lookup"><span data-stu-id="95c4c-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="95c4c-137">В поле "Место подписания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="95c4c-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="95c4c-138">В поле "Ожидаемое количество платежей" введите число.</span><span class="sxs-lookup"><span data-stu-id="95c4c-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="95c4c-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="95c4c-139">Click OK.</span></span>
9. <span data-ttu-id="95c4c-140">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="95c4c-140">Click Save.</span></span>


