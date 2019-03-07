---
title: Настройка поручения прямого дебетования SEPA
description: Прямое дебетование единой зоны платежей в евро (SEPA) позволяет кредитору снимать средства с банковского счета клиента, при условии что клиент предоставил кредитору подписанное предписание.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 757f3f6e0c5443054d2d6bd21381d9f692e1b9a5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "334826"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="3f8a8-103">Настройка поручения прямого дебетования SEPA</span><span class="sxs-lookup"><span data-stu-id="3f8a8-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f8a8-104">Прямое дебетование единой зоны платежей в евро (SEPA) позволяет кредитору снимать средства с банковского счета клиента, при условии что клиент предоставил кредитору подписанное предписание.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="3f8a8-105">Клиент подписывает предписание, которое дает кредитору право собирать платежи и поручает банку клиента осуществлять оплату.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="3f8a8-106">В этом разделе показан процесс настройки предписаний прямого дебетования SEPA.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3f8a8-107">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="3f8a8-107">Prerequisites</span></span>
<span data-ttu-id="3f8a8-108">В следующей таблице показаны обязательные компоненты, которые должны быть подготовлены до начала работы.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="3f8a8-109">Категория</span><span class="sxs-lookup"><span data-stu-id="3f8a8-109">Category</span></span>       | <span data-ttu-id="3f8a8-110">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="3f8a8-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f8a8-111">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="3f8a8-111">Country/region</span></span> | <span data-ttu-id="3f8a8-112">Основной адрес для юридического лица должен находиться в следующих странах/зонах: Австралия, Бельгия, Германия, Испания, Франция, Италия или Нидерланды.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="3f8a8-113">Настройка номерной серии для предписаний прямого дебетования Каждое предписание прямого дебетования должно иметь уникальный номер.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="3f8a8-114">Используйте страницу **Номерные серии**, чтобы создать номерную серию для предписаний прямого дебетования.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="3f8a8-115">Вы будете использовать этот идентификатор, чтобы назначать номерную серию системе предписаний прямого дебетования на странице **Параметры расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="3f8a8-116">Настройка параметров расчетов с клиентами для предписаний прямого дебетования Используйте страницу **Параметры расчетов с клиентами**, чтобы настроить параметры для предписаний прямого дебетования.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="3f8a8-117">Чтобы настроить параметры, на вкладке **Прямой дебет** измените параметры по умолчанию согласно требованиям.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="3f8a8-118">Затем на вкладке **Номерные серии** обновите поле **Код поручения на безакцептное списание** для отображения номерной серии, настроенной ранее.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="3f8a8-119">Настройка способа оплаты для предписаний прямого дебетования Необходимо настроить способ оплаты для предписаний прямого дебетования.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="3f8a8-120">Этот способ оплаты используется для запроса накладных для создания платежей прямого дебетования.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="3f8a8-121">Используйте страницу **Способ оплаты**, чтобы настроить способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="3f8a8-122">Чтобы настроить способ оплаты для предписаний прямого дебетования, выполните следующие дополнительные шаги для способа оплаты:</span><span class="sxs-lookup"><span data-stu-id="3f8a8-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="3f8a8-123">В поле **Тип платежа** выберите **Электронный платеж**.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="3f8a8-124">Необязательно: если ожидается, что каждый из ваших клиентов имеет несколько предписания, в поле **Период** выберите **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="3f8a8-125">Будет создан отдельный платеж для каждой накладной, и в каждом платеже будет использовано предписание, заданное для накладной.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="3f8a8-126">Выберите параметр **Требуется поручение**, чтобы создавать платежи с помощью предписаний прямого дебетования.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="3f8a8-127">Параметр **Требуется поручение** доступен, только если в поле **Тип платежа** выбрано значение **Электронный платеж**.</span><span class="sxs-lookup"><span data-stu-id="3f8a8-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="3f8a8-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3f8a8-128">Additional resources</span></span>

[<span data-ttu-id="3f8a8-129">Обзор безакцептного списания</span><span class="sxs-lookup"><span data-stu-id="3f8a8-129">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="3f8a8-130">Создание поручения на безакцептное списание для клиента</span><span class="sxs-lookup"><span data-stu-id="3f8a8-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 

