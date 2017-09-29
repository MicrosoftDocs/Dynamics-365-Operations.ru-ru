---
title: "Настройка предписания прямого дебетования SEPA"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8b50c2d585c7e0bcd8dc15aa70446cd7346ad33c
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="b4eb5-102">Настройка предписания прямого дебетования SEPA</span><span class="sxs-lookup"><span data-stu-id="b4eb5-102">Set up SEPA direct debit mandate</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="b4eb5-103">Прямое дебетование единой зоны платежей в евро (SEPA) позволяет кредитору снимать средства с банковского счета клиента, при условии что клиент предоставил кредитору подписанное предписание.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-103">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="b4eb5-104">Клиент подписывает предписание, которое дает кредитору право собирать платежи и поручает банку клиента осуществлять оплату.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-104">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="b4eb5-105">В этом разделе показан процесс настройки предписаний прямого дебетования SEPA.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-105">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b4eb5-106">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="b4eb5-106">Prerequisites</span></span>
<span data-ttu-id="b4eb5-107">В следующей таблице показаны обязательные компоненты, которые должны быть подготовлены до начала работы.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="b4eb5-108">Категория</span><span class="sxs-lookup"><span data-stu-id="b4eb5-108">Category</span></span>       | <span data-ttu-id="b4eb5-109">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="b4eb5-109">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4eb5-110">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="b4eb5-110">Country/region</span></span> | <span data-ttu-id="b4eb5-111">Основной адрес для юридического лица должен находиться в следующих странах/зонах: Австралия, Бельгия, Германия, Испания, Франция, Италия или Нидерланды.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-111">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="b4eb5-112">Настройка номерной серии для предписаний прямого дебетования Каждое предписание прямого дебетования должно иметь уникальный номер.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-112">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="b4eb5-113">Используйте страницу **Номерные серии**, чтобы создать номерную серию для предписаний прямого дебетования.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-113">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="b4eb5-114">Вы будете использовать этот идентификатор, чтобы назначать номерную серию системе предписаний прямого дебетования на странице **Параметры расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-114">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="b4eb5-115">Настройка параметров расчетов с клиентами для предписаний прямого дебетования Используйте страницу **Параметры расчетов с клиентами**, чтобы настроить параметры для предписаний прямого дебетования.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-115">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="b4eb5-116">Чтобы настроить параметры, на вкладке **Прямой дебет** измените параметры по умолчанию согласно требованиям.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-116">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="b4eb5-117">Затем на вкладке **Номерные серии** обновите поле **Код поручения на безакцептное списание** для отображения номерной серии, настроенной ранее.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-117">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="b4eb5-118">Настройка способа оплаты для предписаний прямого дебетования Необходимо настроить способ оплаты для предписаний прямого дебетования.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-118">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="b4eb5-119">Этот способ оплаты используется для запроса накладных для создания платежей прямого дебетования.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-119">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="b4eb5-120">Используйте страницу **Способ оплаты**, чтобы настроить способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-120">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="b4eb5-121">Чтобы настроить способ оплаты для предписаний прямого дебетования, выполните следующие дополнительные шаги для способа оплаты:</span><span class="sxs-lookup"><span data-stu-id="b4eb5-121">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="b4eb5-122">В поле **Тип платежа** выберите **Электронный платеж**.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-122">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="b4eb5-123">Необязательно: если ожидается, что каждый из ваших клиентов имеет несколько предписания, в поле **Период** выберите **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-123">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="b4eb5-124">Будет создан отдельный платеж для каждой накладной, и в каждом платеже будет использовано предписание, заданное для накладной.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-124">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="b4eb5-125">Выберите параметр **Требуется поручение**, чтобы создавать платежи с помощью предписаний прямого дебетования.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-125">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="b4eb5-126">Параметр **Требуется поручение** доступен, только если в поле **Тип платежа** выбрано значение **Электронный платеж**.</span><span class="sxs-lookup"><span data-stu-id="b4eb5-126">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="b4eb5-127">См. также</span><span class="sxs-lookup"><span data-stu-id="b4eb5-127">See Also</span></span>

[<span data-ttu-id="b4eb5-128">Обзор безакцептного списания</span><span class="sxs-lookup"><span data-stu-id="b4eb5-128">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="b4eb5-129">Создание поручения на безакцептное списание для клиента</span><span class="sxs-lookup"><span data-stu-id="b4eb5-129">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 


