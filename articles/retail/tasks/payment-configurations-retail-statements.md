--- 
title: "Конфигурации платежей для журналов операций розничной торговли"
description: "Эта процедура демонстрирует конфигурации способов оплаты в розничном магазине, которые влияют на то, как создаются и разносятся журналы операций розницы."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f12d8ac9be11b92eaef4acce094ae183906278d4
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="85953-103">Конфигурации платежей для журналов операций розничной торговли</span><span class="sxs-lookup"><span data-stu-id="85953-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="85953-104">Эта процедура демонстрирует конфигурации способов оплаты в розничном магазине, которые влияют на то, как создаются и разносятся журналы операций розницы.</span><span class="sxs-lookup"><span data-stu-id="85953-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="85953-105">В данной записи используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="85953-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="85953-106">Перейдите в раздел Розничная торговля и коммерция > Каналы > Магазины розничной торговли > Все розничные магазины.</span><span class="sxs-lookup"><span data-stu-id="85953-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="85953-107">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="85953-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="85953-108">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="85953-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="85953-109">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="85953-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="85953-110">Щелкните "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="85953-110">Click Payment methods.</span></span>
6. <span data-ttu-id="85953-111">Разверните или сверните раздел "Разноска".</span><span class="sxs-lookup"><span data-stu-id="85953-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="85953-112">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="85953-112">Click Edit.</span></span>
    * <span data-ttu-id="85953-113">Выберите, следует ли суммы, полученные для этого способа оплаты, разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="85953-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="85953-114">Выберите счет, на который должны быть разнесены суммы, полученные через этот способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="85953-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="85953-115">Выберите счет для разноски возможных расхождений между общей полученной суммой транзакции и суммой, учтенной для данного способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="85953-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="85953-116">В этом поле можно ввести сумму для управления тем, когда сумма расхождений должна быть разнесена на другой счет расхождения.</span><span class="sxs-lookup"><span data-stu-id="85953-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="85953-117">Это поле можно использовать, чтобы отслеживать большие расхождения.</span><span class="sxs-lookup"><span data-stu-id="85953-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="85953-118">Выберите счет для разноски возможных расхождений между общей полученной суммой транзакции и учтенной суммой, когда она превышает значение, указанное в поле "Максимальная сумма расхождения".</span><span class="sxs-lookup"><span data-stu-id="85953-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="85953-119">Выберите "Да", чтобы разнести сумму инкассации на отдельный счет.</span><span class="sxs-lookup"><span data-stu-id="85953-119">Select "Yes" to post bank drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="85953-120">В этом поле можно выбрать, следует ли суммы инкассации разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="85953-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="85953-121">Выберите счет для разноски сумм инкассации.</span><span class="sxs-lookup"><span data-stu-id="85953-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="85953-122">Выберите тип банковской проводки, который будет использоваться при разноске суммы инкассации на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="85953-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="85953-123">Выберите "Да", чтобы разнести сумму сдачи наличных средств в сейф на отдельный счет.</span><span class="sxs-lookup"><span data-stu-id="85953-123">Select "Yes" to post safe drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="85953-124">Выберите, следует ли суммы сдачи наличных средств в сейф разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="85953-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="85953-125">Выберите счет для разноски сумм сдачи наличных средств в сейф.</span><span class="sxs-lookup"><span data-stu-id="85953-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="85953-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="85953-126">Click Save.</span></span>

