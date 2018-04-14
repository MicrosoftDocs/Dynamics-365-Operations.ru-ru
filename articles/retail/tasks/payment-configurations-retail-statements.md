--- 
title: "Конфигурации платежей для журналов операций розничной торговли"
description: "Эта процедура демонстрирует конфигурации способов оплаты в розничном магазине, которые влияют на то, как создаются и разносятся журналы операций розницы."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: df936a3d6753b428a7010a6db83fecb5478c9873
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="0b989-103">Конфигурации платежей для журналов операций розничной торговли</span><span class="sxs-lookup"><span data-stu-id="0b989-103">Payment configurations for Retail statements</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0b989-104">Эта процедура демонстрирует конфигурации способов оплаты в розничном магазине, которые влияют на то, как создаются и разносятся журналы операций розницы.</span><span class="sxs-lookup"><span data-stu-id="0b989-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="0b989-105">В данной записи используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="0b989-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="0b989-106">Перейдите в раздел Розничная торговля и коммерция > Каналы > Магазины розничной торговли > Все розничные магазины.</span><span class="sxs-lookup"><span data-stu-id="0b989-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="0b989-107">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="0b989-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0b989-108">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="0b989-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0b989-109">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="0b989-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="0b989-110">Щелкните "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="0b989-110">Click Payment methods.</span></span>
6. <span data-ttu-id="0b989-111">Разверните или сверните раздел "Разноска".</span><span class="sxs-lookup"><span data-stu-id="0b989-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="0b989-112">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="0b989-112">Click Edit.</span></span>
    * <span data-ttu-id="0b989-113">Выберите, следует ли суммы, полученные для этого способа оплаты, разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="0b989-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="0b989-114">Выберите счет, на который должны быть разнесены суммы, полученные через этот способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="0b989-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="0b989-115">Выберите счет для разноски возможных расхождений между общей полученной суммой транзакции и суммой, учтенной для данного способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="0b989-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="0b989-116">В этом поле можно ввести сумму для управления тем, когда сумма расхождений должна быть разнесена на другой счет расхождения.</span><span class="sxs-lookup"><span data-stu-id="0b989-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="0b989-117">Это поле можно использовать, чтобы отслеживать большие расхождения.</span><span class="sxs-lookup"><span data-stu-id="0b989-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="0b989-118">Выберите счет для разноски возможных расхождений между общей полученной суммой транзакции и учтенной суммой, когда она превышает значение, указанное в поле "Максимальная сумма расхождения".</span><span class="sxs-lookup"><span data-stu-id="0b989-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="0b989-119">Выберите "Да", чтобы разнести сумму инкассации на отдельный счет.</span><span class="sxs-lookup"><span data-stu-id="0b989-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="0b989-120">В этом поле можно выбрать, следует ли суммы инкассации разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="0b989-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="0b989-121">Выберите счет для разноски сумм инкассации.</span><span class="sxs-lookup"><span data-stu-id="0b989-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="0b989-122">Выберите тип банковской проводки, который будет использоваться при разноске суммы инкассации на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="0b989-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="0b989-123">Выберите "Да", чтобы разнести сумму сдачи наличных средств в сейф на отдельный счет.</span><span class="sxs-lookup"><span data-stu-id="0b989-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="0b989-124">Выберите, следует ли суммы сдачи наличных средств в сейф разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="0b989-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="0b989-125">Выберите счет для разноски сумм сдачи наличных средств в сейф.</span><span class="sxs-lookup"><span data-stu-id="0b989-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="0b989-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0b989-126">Click Save.</span></span>


