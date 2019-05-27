---
title: Установка способов оплаты для клиентов
description: Создайте способ оплаты для платежей клиентов.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab035c6268b701c78da32d589e99ece38c31781d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546809"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="ee02d-103">Установка способов оплаты для клиентов</span><span class="sxs-lookup"><span data-stu-id="ee02d-103">Establish customer method of payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee02d-104">Создайте способ оплаты для платежей клиентов.</span><span class="sxs-lookup"><span data-stu-id="ee02d-104">Create a method of payment for customer payments.</span></span> <span data-ttu-id="ee02d-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="ee02d-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ee02d-106">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="ee02d-106">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="ee02d-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ee02d-107">Click New.</span></span>
3. <span data-ttu-id="ee02d-108">В поле "Способ оплаты" введите код способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="ee02d-108">In the Method of payment field, enter an ID for the method of payment.</span></span>
    * <span data-ttu-id="ee02d-109">Код способа оплаты отображается в накладных и платежах, поэтому присвойте ему довольно описательное имя, чтобы пользователи понимали, какой тип платежа записывается и для какого банковского счета.</span><span class="sxs-lookup"><span data-stu-id="ee02d-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="ee02d-110">В поле "Описание" введите описание.</span><span class="sxs-lookup"><span data-stu-id="ee02d-110">In the Description field, enter a description.</span></span>
5. <span data-ttu-id="ee02d-111">Выберите, какой статус оплаты требуется для разноски платежей.</span><span class="sxs-lookup"><span data-stu-id="ee02d-111">Select what payment status is required in order for payments to be posted.</span></span>
    * <span data-ttu-id="ee02d-112">При создании платежа клиента платеж можно разнести, только если статус оплаты совпадает со статусом оплаты, определенным здесь.</span><span class="sxs-lookup"><span data-stu-id="ee02d-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="ee02d-113">Выберите способ создания платежей клиентов для накладных.</span><span class="sxs-lookup"><span data-stu-id="ee02d-113">Select how customers payments should be created for invoices.</span></span>
    * <span data-ttu-id="ee02d-114">Этот параметр используется только при выполнении предложения по оплате.</span><span class="sxs-lookup"><span data-stu-id="ee02d-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="ee02d-115">Предложение по оплате можно использовать для платежей клиентов при прямом дебетовании и извлечении средств с банковских счетов клиентов.</span><span class="sxs-lookup"><span data-stu-id="ee02d-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="ee02d-116">Выберите тип платежа.</span><span class="sxs-lookup"><span data-stu-id="ee02d-116">Select the type of payment.</span></span>
    * <span data-ttu-id="ee02d-117">Тип платежа поможет определить, будет ли выполняться проверка платежа.</span><span class="sxs-lookup"><span data-stu-id="ee02d-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="ee02d-118">Выберите, куда будут разноситься платежи типа счета.</span><span class="sxs-lookup"><span data-stu-id="ee02d-118">Select what account type payments will post to.</span></span>
    * <span data-ttu-id="ee02d-119">Обычно в качестве значения этого параметра выбирают "Банк".</span><span class="sxs-lookup"><span data-stu-id="ee02d-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="ee02d-120">Выберите банковский счет, на который будет записываться этот платеж.</span><span class="sxs-lookup"><span data-stu-id="ee02d-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="ee02d-121">Введите тип банковской проводки, чтобы определить тип платежа, используемого банком.</span><span class="sxs-lookup"><span data-stu-id="ee02d-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span>
    * <span data-ttu-id="ee02d-122">Тип банковской проводки используется в процессе банковской выверки и упрощает выверку.</span><span class="sxs-lookup"><span data-stu-id="ee02d-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="ee02d-123">Укажите, будет ли этот платеж временно разноситься на промежуточный счет.</span><span class="sxs-lookup"><span data-stu-id="ee02d-123">Select whether this payment will temporarily post to a bridging account.</span></span>
    * <span data-ttu-id="ee02d-124">Если вы хотите выделить резервное время для того, чтобы платеж прошел клиринг в банке, используйте функцию "Промежуточный счет".</span><span class="sxs-lookup"><span data-stu-id="ee02d-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="ee02d-125">Платеж временно разносится на счет ГК до клиринга в банке, после чего платеж будет помещен на банковский счет, указанный здесь.</span><span class="sxs-lookup"><span data-stu-id="ee02d-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="ee02d-126">Введите счет ГК, используемый для разноски на промежуточный счет.</span><span class="sxs-lookup"><span data-stu-id="ee02d-126">Enter the main account used for the bridging posting.</span></span>
    * <span data-ttu-id="ee02d-127">Это счет ГК, на который временно разносится платеж при использовании промежуточного счета.</span><span class="sxs-lookup"><span data-stu-id="ee02d-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="ee02d-128">Используйте вкладку "Формат файла", чтобы определить настройки для электронных платежей.</span><span class="sxs-lookup"><span data-stu-id="ee02d-128">Use the File format tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="ee02d-129">Используйте вкладку "Контроль платежей", чтобы определить обязательные поля.</span><span class="sxs-lookup"><span data-stu-id="ee02d-129">Use the Payment control tab to define fields that are mandatory.</span></span>
    * <span data-ttu-id="ee02d-130">Например, если необходимо депонировать все платежи с этим способом оплаты, можно выбрать этот параметр на этой вкладке.</span><span class="sxs-lookup"><span data-stu-id="ee02d-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="ee02d-131">Используйте вкладку "Атрибуты оплаты", чтобы определить атрибуты оплаты для использования с данным способом оплаты.</span><span class="sxs-lookup"><span data-stu-id="ee02d-131">Use the Payment atrributes tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="ee02d-132">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ee02d-132">Click Save.</span></span>

