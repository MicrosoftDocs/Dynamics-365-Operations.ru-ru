--- 
title: "Внесение платежей клиентов"
description: "Депонируйте платежи клиента."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: f1f8ddb4b18e4e06fe0a7307ceadf8063d8eba07
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="deposit-customer-payments"></a><span data-ttu-id="b57cf-103">Внесение платежей клиентов</span><span class="sxs-lookup"><span data-stu-id="b57cf-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b57cf-104">Депонируйте платежи клиента.</span><span class="sxs-lookup"><span data-stu-id="b57cf-104">Deposit customer payments.</span></span> <span data-ttu-id="b57cf-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="b57cf-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b57cf-106">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="b57cf-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="b57cf-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b57cf-107">Click New.</span></span>
3. <span data-ttu-id="b57cf-108">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b57cf-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b57cf-109">Выберите журнал платежей.</span><span class="sxs-lookup"><span data-stu-id="b57cf-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="b57cf-110">Выберите Строки.</span><span class="sxs-lookup"><span data-stu-id="b57cf-110">Click Lines.</span></span>
6. <span data-ttu-id="b57cf-111">В поле "Счет" выберите клиента, для которого записывается платеж.</span><span class="sxs-lookup"><span data-stu-id="b57cf-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="b57cf-112">В поле "Кредит" введите сумму платежа.</span><span class="sxs-lookup"><span data-stu-id="b57cf-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="b57cf-113">Можно оставить сумму незаполненной, чтобы система рассчитывала ее путем выбора оплаченных накладных.</span><span class="sxs-lookup"><span data-stu-id="b57cf-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="b57cf-114">В поле "Ссылка на платеж" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b57cf-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="b57cf-115">Ссылкой на платеж может быть номер чека для вводимого платежа.</span><span class="sxs-lookup"><span data-stu-id="b57cf-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="b57cf-116">Ссылка на платеж требуется для включения платежа в бланк депозита.</span><span class="sxs-lookup"><span data-stu-id="b57cf-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="b57cf-117">Установите флажок "Использовать бланк депозита".</span><span class="sxs-lookup"><span data-stu-id="b57cf-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="b57cf-118">Если платеж должен быть включен в депозит, измените значение этого параметра на "Да".</span><span class="sxs-lookup"><span data-stu-id="b57cf-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="b57cf-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b57cf-119">Click New.</span></span>
11. <span data-ttu-id="b57cf-120">В поле "Счет" выберите клиента для следующего платежа.</span><span class="sxs-lookup"><span data-stu-id="b57cf-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="b57cf-121">В поле "Кредит" введите сумму платежа.</span><span class="sxs-lookup"><span data-stu-id="b57cf-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="b57cf-122">В поле "Ссылка на платеж" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b57cf-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="b57cf-123">Установите флажок "Использовать бланк депозита".</span><span class="sxs-lookup"><span data-stu-id="b57cf-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="b57cf-124">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="b57cf-124">Click Post.</span></span>
    * <span data-ttu-id="b57cf-125">Платежи необходимо разнести до создания бланка депозита.</span><span class="sxs-lookup"><span data-stu-id="b57cf-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="b57cf-126">Это гарантирует, что платежи не изменятся после создания бланка депозита.</span><span class="sxs-lookup"><span data-stu-id="b57cf-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="b57cf-127">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="b57cf-127">Click Functions.</span></span>
17. <span data-ttu-id="b57cf-128">Щелкните "Бланк депозита".</span><span class="sxs-lookup"><span data-stu-id="b57cf-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="b57cf-129">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b57cf-129">Click OK.</span></span>
    * <span data-ttu-id="b57cf-130">Первая страница используется для создания бланка депозита.</span><span class="sxs-lookup"><span data-stu-id="b57cf-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="b57cf-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b57cf-131">Click OK.</span></span>
    * <span data-ttu-id="b57cf-132">Второй этап — печать бланка депозита, но этот шаг не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b57cf-132">The second step is to print the deposit slip, but this step is not required.</span></span>  


