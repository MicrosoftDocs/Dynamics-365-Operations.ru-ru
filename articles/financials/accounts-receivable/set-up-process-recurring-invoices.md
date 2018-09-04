---
title: "Настройка и обработка периодических накладных"
description: "В этой статье описывается, как настроить и обработать повторяющиеся накладные. Можно использовать повторяющийся накладные, если необходимо выставлять накладные для клиентов на то же самое количества на регулярной основе."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 96a9075294c1f2a9cfde03be1aaaa26af90de4c2
ms.openlocfilehash: ac9e836b0baa24c40554844ea4f3288b80e0c654
ms.contentlocale: ru-ru
ms.lasthandoff: 09/04/2018

---

# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="2d55d-104">Настройка и обработка периодических накладных</span><span class="sxs-lookup"><span data-stu-id="2d55d-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d55d-105">В этой статье описывается, как настроить и обработать повторяющиеся накладные.</span><span class="sxs-lookup"><span data-stu-id="2d55d-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="2d55d-106">Можно использовать повторяющийся накладные, если необходимо выставлять накладные для клиентов на то же самое количества на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="2d55d-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="2d55d-107">Создание шаблона повторения накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="2d55d-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="2d55d-108">Чтобы выставлять накладные клиентам за те же услуги на регулярной основе, необходимо определить шаблон накладной с произвольным текстом, который можно повторно использовать для создания накладных.</span><span class="sxs-lookup"><span data-stu-id="2d55d-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="2d55d-109">Шаблон содержит следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="2d55d-109">This template contains the following information:</span></span>

-   <span data-ttu-id="2d55d-110">Сведения о заголовке, например налоговые группы, условия оплаты и способ оплаты</span><span class="sxs-lookup"><span data-stu-id="2d55d-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="2d55d-111">Сведения о строке, например описание услуги, счета выручки, цена за единицу и сумма накладной</span><span class="sxs-lookup"><span data-stu-id="2d55d-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="2d55d-112">Накладные расходы по отгрузке или обработке</span><span class="sxs-lookup"><span data-stu-id="2d55d-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="2d55d-113">Распределения по бухгалтерским счетам вместе со сведениями о финансовых аналитиках, например места возникновения затрат и бизнес-единицы</span><span class="sxs-lookup"><span data-stu-id="2d55d-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="2d55d-114">В сущности, вы создаете всю накладную и сохраняете ее как шаблон.</span><span class="sxs-lookup"><span data-stu-id="2d55d-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="2d55d-115">Шаблоны можно настроить на странице **Периодические накладные**.</span><span class="sxs-lookup"><span data-stu-id="2d55d-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="2d55d-116">Назначьте шаблон накладной с произвольным текстом клиенту и укажите параметры повторения.</span><span class="sxs-lookup"><span data-stu-id="2d55d-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="2d55d-117">После создания шаблона необходимо назначить шаблон клиентам, которым необходимо выставить накладные.</span><span class="sxs-lookup"><span data-stu-id="2d55d-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="2d55d-118">Кроме того, необходимо указать, когда и как часто будет использоваться накладная.</span><span class="sxs-lookup"><span data-stu-id="2d55d-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="2d55d-119">Шаблоны можно назначить на вкладке **Накладная** на странице **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="2d55d-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="2d55d-120">Добавьте шаблон в список и обновите следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="2d55d-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="2d55d-121">Дата начала и по желанию дата окончания для выставления периодических накладных</span><span class="sxs-lookup"><span data-stu-id="2d55d-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="2d55d-122">Частота выставления периодических накладных (например, каждый день или раз в месяц)</span><span class="sxs-lookup"><span data-stu-id="2d55d-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="2d55d-123">Максимальная сумма выставляемых накладных (если эта информация необходима)</span><span class="sxs-lookup"><span data-stu-id="2d55d-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="2d55d-124">Клиент может иметь несколько шаблонов с различной частотой.</span><span class="sxs-lookup"><span data-stu-id="2d55d-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="2d55d-125">Создание периодических накладных</span><span class="sxs-lookup"><span data-stu-id="2d55d-125">Generate the recurring invoices</span></span>
<span data-ttu-id="2d55d-126">На странице **Периодические накладные** имеется задача, которая обрабатывает шаблоны периодических накладных.</span><span class="sxs-lookup"><span data-stu-id="2d55d-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="2d55d-127">Укажите дату накладной и шаблон для создания накладных.</span><span class="sxs-lookup"><span data-stu-id="2d55d-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="2d55d-128">Накладные будут созданы, и им будет назначен один номер кода повторения для каждой обрабатываемой группы накладных.</span><span class="sxs-lookup"><span data-stu-id="2d55d-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

<a name="post-recurring-free-text-invoices"></a><span data-ttu-id="2d55d-129">Накладные с произвольным текстом повторения разноски</span><span class="sxs-lookup"><span data-stu-id="2d55d-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="2d55d-130">После создания периодических накладных коды повторения накладных будут отображаться в задаче разноски на странице **Периодические накладные**.</span><span class="sxs-lookup"><span data-stu-id="2d55d-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="2d55d-131">Можно просмотреть все накладные по коду повторения, перейдя по ссылке.</span><span class="sxs-lookup"><span data-stu-id="2d55d-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="2d55d-132">Во время предварительного просмотра накладных по коду повторения можно удалить отдельные накладные.</span><span class="sxs-lookup"><span data-stu-id="2d55d-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="2d55d-133">Параметры повторения клиента будут сброшены для этого шаблона, чтобы его можно было повторно создать позже.</span><span class="sxs-lookup"><span data-stu-id="2d55d-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="2d55d-134">Можно разнести одну, несколько или все накладные по коду повторения.</span><span class="sxs-lookup"><span data-stu-id="2d55d-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="2d55d-135">Если включены workflow-процессы, щелкните **Отправить** перед разноской накладных.</span><span class="sxs-lookup"><span data-stu-id="2d55d-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

<a name="print-recurring-free-text-invoices"></a><span data-ttu-id="2d55d-136">Печать периодических накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="2d55d-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="2d55d-137">После разноски периодических накладных можно напечатать накладные на странице списка накладных с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="2d55d-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="2d55d-138">Можно напечатать выбранные накладные или можно выбрать ряд накладных для печати.</span><span class="sxs-lookup"><span data-stu-id="2d55d-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>




