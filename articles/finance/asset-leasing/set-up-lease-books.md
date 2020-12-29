---
title: Настройка книг аренды
description: В этой теме описываются сведения, поддерживаемые в книгах аренды. В книгах аренды содержатся учетные политики, определяющие способ учета аренды в системе.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4447400"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="d1fc8-104">Настройка книг аренды</span><span class="sxs-lookup"><span data-stu-id="d1fc8-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1fc8-105">В книгах аренды содержатся учетные политики, определяющие способ учета аренды в системе.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="d1fc8-106">В дополнение к учету на основе денежных средств, аренда активов поддерживают следующие стандарты:</span><span class="sxs-lookup"><span data-stu-id="d1fc8-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="d1fc8-107">Общепринятые принципы учета в США (US GAAP)</span><span class="sxs-lookup"><span data-stu-id="d1fc8-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="d1fc8-108">Тема 842 кодификации бухгалтерских стандартов (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="d1fc8-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="d1fc8-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="d1fc8-109">ASC 840</span></span>
- <span data-ttu-id="d1fc8-110">Международный стандарт финансовой отчетности 16 (МСФО 16)</span><span class="sxs-lookup"><span data-stu-id="d1fc8-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="d1fc8-111">Международный бухгалтерский стандарт 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="d1fc8-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="d1fc8-112">Чтобы создать книгу аренды, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="d1fc8-113">Перейдите в раздел **Аренда активов \> Настройка \> Книги аренды**.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="d1fc8-114">Выберите **Создать**, чтобы добавить книгу.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="d1fc8-115">Задайте следующие поля.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-115">Set the following fields.</span></span>

    | <span data-ttu-id="d1fc8-116">Наименование</span><span class="sxs-lookup"><span data-stu-id="d1fc8-116">Name</span></span>                                     | <span data-ttu-id="d1fc8-117">описание</span><span class="sxs-lookup"><span data-stu-id="d1fc8-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="d1fc8-118">Слой разноски</span><span class="sxs-lookup"><span data-stu-id="d1fc8-118">Posting layer</span></span>                            | <span data-ttu-id="d1fc8-119">Выберите слой разноски для использования.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-119">Select the posting layer to use.</span></span> <span data-ttu-id="d1fc8-120">Каждая книга, прикрепленная к аренде, настраивается для конкретного слоя разноски.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="d1fc8-121">У каждого слоя разноски имеются различающиеся цели разноски.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="d1fc8-122">Тип аренды</span><span class="sxs-lookup"><span data-stu-id="d1fc8-122">Lease type</span></span>                               | <span data-ttu-id="d1fc8-123">Выберите, должна ли аренда быть классифицирована автоматически или должна ли она быть предопределенной в качестве финансовой или операционной аренды.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="d1fc8-124">Платформа учета</span><span class="sxs-lookup"><span data-stu-id="d1fc8-124">Accounting framework</span></span>                     | <span data-ttu-id="d1fc8-125">Выберите платформу, связанную с книгой.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="d1fc8-126">Настройка срока аренды или срока службы</span><span class="sxs-lookup"><span data-stu-id="d1fc8-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="d1fc8-127">Система будет классифицировать аренду как финансовую, если тип аренды установлен **Автоматически** и если срок аренды относительно срока службы актива больше или равен проценту, введенному в это поле.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="d1fc8-128">Настройка текущей стоимости/реальной стоимости актива</span><span class="sxs-lookup"><span data-stu-id="d1fc8-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="d1fc8-129">Введите целое число, чтобы определить пороговое значение, которое определит тип аренды.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="d1fc8-130">Если текущая стоимость будущих минимальных арендных платежей превышает значение, определяемое пользователем в настройке книги, и если для классификации аренды книги установлено значение "Автоматически", то система будет классифицировать аренду как финансовую аренду.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="d1fc8-131">Порог краткосрочной аренды</span><span class="sxs-lookup"><span data-stu-id="d1fc8-131">Short-term threshold</span></span>                     | <span data-ttu-id="d1fc8-132">Введите количество месяцев для использования в качестве порога краткосрочных аренд.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="d1fc8-133">Если срок аренды меньше или равен числу месяцев, введенному здесь, система будет классифицировать аренду как краткосрочную аренду, и будет применен договор отложенной ренты.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="d1fc8-134">Порог аренды малоценного актива</span><span class="sxs-lookup"><span data-stu-id="d1fc8-134">Low value threshold</span></span>                      | <span data-ttu-id="d1fc8-135">Введите сумму для использования в качестве порогового значения для аренд с низкой стоимостью.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="d1fc8-136">Если реальная стоимость актива меньше или равен значению, введенному здесь, система будет классифицировать аренду как аренду малоценного актива, и будет применен договор отложенной ренты.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="d1fc8-137">Оплата поставщику</span><span class="sxs-lookup"><span data-stu-id="d1fc8-137">Pay to vendor</span></span>                            | <span data-ttu-id="d1fc8-138">Установите для этого параметра значение **Да**, чтобы разрешить разноску платежей по аренде в качестве накладной для счета поставщика, указанного в каждой аренде.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="d1fc8-139">При разноске платежа по аренде счет поставщика будет кредитоваться.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="d1fc8-140">Если этот параметр имеет значение **Нет**, счет, указанный для типа разноски **Платеж по аренде** на странице **Параметры разноски аренды**, будет кредитоваться вместо этого.</span><span class="sxs-lookup"><span data-stu-id="d1fc8-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
