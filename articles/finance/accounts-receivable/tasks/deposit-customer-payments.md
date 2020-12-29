---
title: Внесение платежей клиентов
description: Депонируйте платежи клиента.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447195"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="cbec0-103">Внесение платежей клиентов</span><span class="sxs-lookup"><span data-stu-id="cbec0-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cbec0-104">Депонируйте платежи клиента.</span><span class="sxs-lookup"><span data-stu-id="cbec0-104">Deposit customer payments.</span></span> <span data-ttu-id="cbec0-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="cbec0-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="cbec0-106">Выберите **Область перехода > Модули > Расчеты с клиентами > Платежи > Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="cbec0-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-107">Select **New**.</span></span>
3. <span data-ttu-id="cbec0-108">В поле **Имя** выберите **CustPay** в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="cbec0-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="cbec0-109">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-109">Select **Lines**.</span></span>
5. <span data-ttu-id="cbec0-110">В поле **Счет** выберите клиента, для которого записывается платеж.</span><span class="sxs-lookup"><span data-stu-id="cbec0-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="cbec0-111">В поле **Кредит** введите сумму платежа.</span><span class="sxs-lookup"><span data-stu-id="cbec0-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="cbec0-112">Можно оставить сумму незаполненной, чтобы система рассчитывала ее путем выбора оплаченных накладных.</span><span class="sxs-lookup"><span data-stu-id="cbec0-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="cbec0-113">В поле **Ссылка на платеж** введите значение.</span><span class="sxs-lookup"><span data-stu-id="cbec0-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="cbec0-114">Ссылкой на платеж может быть номер чека для вводимого платежа.</span><span class="sxs-lookup"><span data-stu-id="cbec0-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="cbec0-115">Ссылка на платеж требуется для включения платежа в бланк депозита.</span><span class="sxs-lookup"><span data-stu-id="cbec0-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="cbec0-116">Установите флажок "Использовать бланк депозита".</span><span class="sxs-lookup"><span data-stu-id="cbec0-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="cbec0-117">Если платеж должен быть включен в депозит, измените значение этого параметра на "Да".</span><span class="sxs-lookup"><span data-stu-id="cbec0-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="cbec0-118">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-118">Select **New**.</span></span>
10. <span data-ttu-id="cbec0-119">В поле **Счет** выберите клиента для следующего платежа.</span><span class="sxs-lookup"><span data-stu-id="cbec0-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="cbec0-120">В поле **Кредит** введите сумму платежа.</span><span class="sxs-lookup"><span data-stu-id="cbec0-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="cbec0-121">В поле **Ссылка на платеж** введите значение.</span><span class="sxs-lookup"><span data-stu-id="cbec0-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="cbec0-122">Установите флажок **Использовать бланк депозита**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="cbec0-123">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-123">Select **Post**.</span></span> <span data-ttu-id="cbec0-124">Платежи необходимо разнести до создания бланка депозита.</span><span class="sxs-lookup"><span data-stu-id="cbec0-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="cbec0-125">Это гарантирует, что платежи не изменятся после создания бланка депозита.</span><span class="sxs-lookup"><span data-stu-id="cbec0-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="cbec0-126">Выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-126">Select **Functions**.</span></span>
16. <span data-ttu-id="cbec0-127">Выберите **Бланк депозита**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="cbec0-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-128">Select **OK**.</span></span> <span data-ttu-id="cbec0-129">Первая страница используется для создания бланка депозита.</span><span class="sxs-lookup"><span data-stu-id="cbec0-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="cbec0-130">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-130">Select **OK**.</span></span> <span data-ttu-id="cbec0-131">Второй этап — печать бланка депозита, но этот шаг не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="cbec0-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

