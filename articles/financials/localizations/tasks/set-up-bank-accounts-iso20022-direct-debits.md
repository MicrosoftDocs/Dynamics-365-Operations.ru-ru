---
title: Настройка клиентов и банковских счетов клиентов для безакцептного списания ISO20022
description: В этой задаче описывается настройка банковского счета клиента и поручения на безакцептное списание клиента, которые необходимы для создания файла платежа клиента, такого как прямое дебетование ISO20022.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7d7d79b1d496223b027d800beca105ecaa0bd4c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "342669"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="f4c60-103">Настройка клиентов и банковских счетов клиентов для безакцептного списания ISO20022</span><span class="sxs-lookup"><span data-stu-id="f4c60-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4c60-104">В этой задаче описывается настройка банковского счета клиента и поручения на безакцептное списание клиента, которые необходимы для создания файла платежа клиента, такого как прямое дебетование ISO20022.</span><span class="sxs-lookup"><span data-stu-id="f4c60-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="f4c60-105">В зависимости от настроенных форматов платежей клиентов, дополнительные сведения, не рассматриваемые в этой процедуре, могут потребоваться для клиента или банковского счета клиента.</span><span class="sxs-lookup"><span data-stu-id="f4c60-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="f4c60-106">Эта задача была создана с использованием компании с демонстрационными данными DEMF с основным адресом юридического лица в Германии.</span><span class="sxs-lookup"><span data-stu-id="f4c60-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="f4c60-107">Это четвертая процедура из пяти, которые демонстрируют процесс платежа клиентов с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f4c60-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="f4c60-108">Настройка банковского счета клиента</span><span class="sxs-lookup"><span data-stu-id="f4c60-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="f4c60-109">Перейдите в раздел "Расчеты с клиентами" > "Клиенты" > "Все клиенты".</span><span class="sxs-lookup"><span data-stu-id="f4c60-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="f4c60-110">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="f4c60-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f4c60-111">Например, отфильтруйте поле "Счет" по значению "DE-010".</span><span class="sxs-lookup"><span data-stu-id="f4c60-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="f4c60-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f4c60-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f4c60-113">В области действий щелкните "Клиент".</span><span class="sxs-lookup"><span data-stu-id="f4c60-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="f4c60-114">Щелкните "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="f4c60-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="f4c60-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f4c60-115">Click New.</span></span>
7. <span data-ttu-id="f4c60-116">В поле "Банковский счет" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f4c60-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="f4c60-117">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f4c60-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f4c60-118">Например, введите "Банк EUR".</span><span class="sxs-lookup"><span data-stu-id="f4c60-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="f4c60-119">В поле "Банковские группы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f4c60-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="f4c60-120">В поле "IBAN" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f4c60-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="f4c60-121">Например, введите "DE36200400000628808808".</span><span class="sxs-lookup"><span data-stu-id="f4c60-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="f4c60-122">В поле "SWIFT-код" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f4c60-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="f4c60-123">Например, введите "COBADEFFXXX".</span><span class="sxs-lookup"><span data-stu-id="f4c60-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="f4c60-124">Обратите внимание, что SWIFT\BIC не является обязательным для многих форматов платежей, однако рекомендуется, чтобы этот код был зарегистрирован для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="f4c60-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="f4c60-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f4c60-125">Click Save.</span></span>
13. <span data-ttu-id="f4c60-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f4c60-126">Close the page.</span></span>
14. <span data-ttu-id="f4c60-127">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="f4c60-127">Click Edit.</span></span>
15. <span data-ttu-id="f4c60-128">Разверните раздел "Значения платежа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="f4c60-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="f4c60-129">В поле "Банковский счет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f4c60-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="f4c60-130">Добавление поручения на безакцептное списание</span><span class="sxs-lookup"><span data-stu-id="f4c60-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="f4c60-131">Разверните раздел "Поручения на безакцептное списание".</span><span class="sxs-lookup"><span data-stu-id="f4c60-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="f4c60-132">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f4c60-132">Click Add.</span></span>
3. <span data-ttu-id="f4c60-133">В поле "Банковский счет кредитора" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f4c60-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="f4c60-134">Например, выберите DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="f4c60-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="f4c60-135">В поле "Дата подписи" введите дату.</span><span class="sxs-lookup"><span data-stu-id="f4c60-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="f4c60-136">Щелкните "Да", чтобы подтвердить обновление даты.</span><span class="sxs-lookup"><span data-stu-id="f4c60-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="f4c60-137">В поле "Место подписания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f4c60-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="f4c60-138">В поле "Ожидаемое количество платежей" введите число.</span><span class="sxs-lookup"><span data-stu-id="f4c60-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="f4c60-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f4c60-139">Click OK.</span></span>
9. <span data-ttu-id="f4c60-140">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f4c60-140">Click Save.</span></span>

