---
title: Конфигурации платежей для журналов операций розничной торговли
description: Эта процедура демонстрирует конфигурации способов оплаты Commerce в магазине, которые влияют на то, как создаются и разносятся журналы операций.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b1fc042bff4d801ae893b0370b67cd8e11ba95f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982324"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="4e5c9-103">Конфигурации платежей для журналов операций розничной торговли</span><span class="sxs-lookup"><span data-stu-id="4e5c9-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e5c9-104">Эта процедура демонстрирует конфигурации способов оплаты Commerce в магазине, которые влияют на то, как создаются и разносятся журналы операций.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="4e5c9-105">В данной записи используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="4e5c9-106">Перейдите в раздел Retail и Commerce > Каналы > Магазины > Все магазины.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="4e5c9-107">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4e5c9-108">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4e5c9-109">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="4e5c9-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="4e5c9-110">Щелкните "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="4e5c9-110">Click Payment methods.</span></span>
6. <span data-ttu-id="4e5c9-111">Разверните или сверните раздел "Разноска".</span><span class="sxs-lookup"><span data-stu-id="4e5c9-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="4e5c9-112">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="4e5c9-112">Click Edit.</span></span>
    * <span data-ttu-id="4e5c9-113">Выберите, следует ли суммы, полученные для этого способа оплаты, разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="4e5c9-114">Выберите счет, на который должны быть разнесены суммы, полученные через этот способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="4e5c9-115">Выберите счет для разноски возможных расхождений между общей полученной суммой транзакции и суммой, учтенной для данного способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="4e5c9-116">В этом поле можно ввести сумму для управления тем, когда сумма расхождений должна быть разнесена на другой счет расхождения.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="4e5c9-117">Это поле можно использовать, чтобы отслеживать большие расхождения.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="4e5c9-118">Выберите счет для разноски возможных расхождений между общей полученной суммой транзакции и учтенной суммой, когда она превышает значение, указанное в поле "Максимальная сумма расхождения".</span><span class="sxs-lookup"><span data-stu-id="4e5c9-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="4e5c9-119">Выберите "Да", чтобы разнести сумму инкассации на отдельный счет.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="4e5c9-120">В этом поле можно выбрать, следует ли суммы инкассации разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="4e5c9-121">Выберите счет для разноски сумм инкассации.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="4e5c9-122">Выберите тип банковской проводки, который будет использоваться при разноске суммы инкассации на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="4e5c9-123">Выберите "Да", чтобы разнести сумму сдачи наличных средств в сейф на отдельный счет.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="4e5c9-124">Выберите, следует ли суммы сдачи наличных средств в сейф разносить на счет ГК или на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="4e5c9-125">Выберите счет для разноски сумм сдачи наличных средств в сейф.</span><span class="sxs-lookup"><span data-stu-id="4e5c9-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="4e5c9-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4e5c9-126">Click Save.</span></span>

