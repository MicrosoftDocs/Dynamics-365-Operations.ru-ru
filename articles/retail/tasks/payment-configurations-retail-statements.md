--- 
title: "Настройка параметров метода оплаты, влияющих на розничные отчеты"
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ba21db9ee97dc4d851c77a906927ef513940b743
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---
# <a name="configure-payment-method-settings-that-affect-retail-statements"></a><span data-ttu-id="51c6b-103">Настройка параметров метода оплаты, влияющих на розничные отчеты</span><span class="sxs-lookup"><span data-stu-id="51c6b-103">Configure payment method settings that affect retail statements</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="51c6b-104">Эта процедура демонстрирует конфигурации способов оплаты в розничном магазине, которые влияют на то, как создаются и разносятся журналы операций розницы.</span><span class="sxs-lookup"><span data-stu-id="51c6b-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="51c6b-105">В данной записи используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="51c6b-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="51c6b-106">Перейдите в раздел Розничная торговля и коммерция > Каналы > Магазины розничной торговли > Все розничные магазины.</span><span class="sxs-lookup"><span data-stu-id="51c6b-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="51c6b-107">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="51c6b-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="51c6b-108">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="51c6b-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="51c6b-109">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="51c6b-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="51c6b-110">Щелкните "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="51c6b-110">Click Payment methods.</span></span>
6. <span data-ttu-id="51c6b-111">Разверните или сверните раздел "Разноска".</span><span class="sxs-lookup"><span data-stu-id="51c6b-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="51c6b-112">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="51c6b-112">Click Edit.</span></span>
    * <span data-ttu-id="51c6b-113">Выберите, следует ли суммы, полученные для этого способа оплаты, разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="51c6b-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="51c6b-114">Выберите счет, на который должны быть разнесены суммы, полученные через этот способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="51c6b-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="51c6b-115">Выберите счет для разноски возможных расхождений между общей полученной суммой транзакции и суммой, учтенной для данного способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="51c6b-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="51c6b-116">В этом поле можно ввести сумму для управления тем, когда сумма расхождений должна быть разнесена на другой счет расхождения.</span><span class="sxs-lookup"><span data-stu-id="51c6b-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="51c6b-117">Это поле можно использовать, чтобы отслеживать большие расхождения.</span><span class="sxs-lookup"><span data-stu-id="51c6b-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="51c6b-118">Выберите счет для разноски возможных расхождений между общей полученной суммой транзакции и учтенной суммой, когда она превышает значение, указанное в поле "Максимальная сумма расхождения".</span><span class="sxs-lookup"><span data-stu-id="51c6b-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="51c6b-119">Выберите "Да", чтобы разнести сумму инкассации на отдельный счет.</span><span class="sxs-lookup"><span data-stu-id="51c6b-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="51c6b-120">В этом поле можно выбрать, следует ли суммы инкассации разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="51c6b-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="51c6b-121">Выберите счет для разноски сумм инкассации.</span><span class="sxs-lookup"><span data-stu-id="51c6b-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="51c6b-122">Выберите тип банковской проводки, который будет использоваться при разноске суммы инкассации на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="51c6b-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="51c6b-123">Выберите "Да", чтобы разнести сумму сдачи наличных средств в сейф на отдельный счет.</span><span class="sxs-lookup"><span data-stu-id="51c6b-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="51c6b-124">Выберите, следует ли суммы сдачи наличных средств в сейф разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="51c6b-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="51c6b-125">Выберите счет для разноски сумм сдачи наличных средств в сейф.</span><span class="sxs-lookup"><span data-stu-id="51c6b-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="51c6b-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="51c6b-126">Click Save.</span></span>


