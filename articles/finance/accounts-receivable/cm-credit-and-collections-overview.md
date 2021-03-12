---
title: Обзор кредита и сбора задолженностей
description: В этом разделе представлен обзор функций для кредитования и сборов.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ade76b822904f49135e07dfe0a39d2227dd1dd77
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992996"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="4c39d-103">Обзор кредита и сбора задолженностей</span><span class="sxs-lookup"><span data-stu-id="4c39d-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c39d-104">Можно управлять кредитными лимитами для клиентов и выполнять мероприятия по сборам, когда они становятся необходимыми.</span><span class="sxs-lookup"><span data-stu-id="4c39d-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="4c39d-105">Управление кредитом</span><span class="sxs-lookup"><span data-stu-id="4c39d-105">Credit management</span></span>

<span data-ttu-id="4c39d-106">Управление кредитованием клиента позволяет управлять кредитными лимитами и управлять потоком заказов на продажу с помощью процесса разноски на основе созданных вами правил кредита.</span><span class="sxs-lookup"><span data-stu-id="4c39d-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="4c39d-107">Процесс управления кредитованием может включать любые из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="4c39d-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="4c39d-108">Обновление атрибутов кредита для клиентов, чтобы предоставить дополнительную информацию о кредитоспособности.</span><span class="sxs-lookup"><span data-stu-id="4c39d-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="4c39d-109">Создание кредитных лимитов для клиентов через корректировки кредитного лимита.</span><span class="sxs-lookup"><span data-stu-id="4c39d-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="4c39d-110">Создание временных кредитных лимитов для клиентов через корректировки кредитного лимита.</span><span class="sxs-lookup"><span data-stu-id="4c39d-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="4c39d-111">Таким образом можно временно увеличить или уменьшить кредитные лимиты клиентов в зависимости от бизнес-требований.</span><span class="sxs-lookup"><span data-stu-id="4c39d-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="4c39d-112">Добавление сведений, которые могут влиять на кредитный лимит, таких как сведения о страховании и гарантиях.</span><span class="sxs-lookup"><span data-stu-id="4c39d-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="4c39d-113">Создание кредитных групп клиентов, которые связывают клиентов друг с другом, чтобы они совместно использовали один кредитный лимит.</span><span class="sxs-lookup"><span data-stu-id="4c39d-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="4c39d-114">Определение показателей риска для клиентов, а затем использование отчетов, чтобы автоматически создать кредитные лимиты для этих клиентов с помощью корректировок кредитного лимита.</span><span class="sxs-lookup"><span data-stu-id="4c39d-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="4c39d-115">Создание правил блокировки, которые блокируют заказ в ходе одного или нескольких процессов разноски, на основе таких факторов, как риск, условия оплаты, кредитные лимиты, просроченные суммы и процент используемого кредитного лимита.</span><span class="sxs-lookup"><span data-stu-id="4c39d-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="4c39d-116">Управление списком заказов на продажу, которые должны быть заблокированы, просмотр причин блокировки и вариантов смягчения.</span><span class="sxs-lookup"><span data-stu-id="4c39d-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="4c39d-117">Выпуск заказов на продажу с целью продолжения процесса разноски.</span><span class="sxs-lookup"><span data-stu-id="4c39d-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="4c39d-118">Настройка workflow-процесса для управления утверждением изменений кредитного лимита и выпуска заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="4c39d-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="4c39d-119">Управление сборами</span><span class="sxs-lookup"><span data-stu-id="4c39d-119">Collections management</span></span>

<span data-ttu-id="4c39d-120">На странице **Сборы** осуществляется централизованное управление сведениями по сбору задолженностей.</span><span class="sxs-lookup"><span data-stu-id="4c39d-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="4c39d-121">Менеджеры по сбору могут централизованно использовать его для управления сборами задолженностей.</span><span class="sxs-lookup"><span data-stu-id="4c39d-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="4c39d-122">Агенты по сбору задолженностей могут начинать обработку сборов по спискам клиентов, которые создаются с помощью заранее определенных критериев по сборам, или на странице **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="4c39d-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="4c39d-123">Перед началом настройки или работы со сборами следует понять следующие основные принципы.</span><span class="sxs-lookup"><span data-stu-id="4c39d-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="4c39d-124">Снимки распределения по срокам клиента содержат сведения о сальдо с распределением по срокам на определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="4c39d-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="4c39d-125">Клиентские пулы сборов помогают организовать работу.</span><span class="sxs-lookup"><span data-stu-id="4c39d-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="4c39d-126">У агентов по сбору задолженностей могут быть собственные клиентские пулы.</span><span class="sxs-lookup"><span data-stu-id="4c39d-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="4c39d-127">На страницах списков упорядочены сборы, клиенты, мероприятия и обращения.</span><span class="sxs-lookup"><span data-stu-id="4c39d-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="4c39d-128">Вся информация о сборах для клиента находится на одной странице, и действие можно выполнить с этой страницы.</span><span class="sxs-lookup"><span data-stu-id="4c39d-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="4c39d-129">Отказ, восстановление или реверсирование процента и сборов можно выполнить за один шаг.</span><span class="sxs-lookup"><span data-stu-id="4c39d-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="4c39d-130">Создание проводок списания можно выполнить за один шаг.</span><span class="sxs-lookup"><span data-stu-id="4c39d-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="4c39d-131">Обработка платежей с недостаточным финансированием может быть выполнена за один шаг.</span><span class="sxs-lookup"><span data-stu-id="4c39d-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="4c39d-132">Описание этих концепций см. в разделе [Основные понятия управления сборами](./cm-collections-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="4c39d-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c39d-133">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4c39d-133">Additional resources</span></span>

[<span data-ttu-id="4c39d-134">Настройка параметров управления кредитами клиентов</span><span class="sxs-lookup"><span data-stu-id="4c39d-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="4c39d-135">Информация о настройке управления кредитами клиентов</span><span class="sxs-lookup"><span data-stu-id="4c39d-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="4c39d-136">Добавление сведений об управлении кредитом для клиента</span><span class="sxs-lookup"><span data-stu-id="4c39d-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="4c39d-137">Кредитные группы клиентов</span><span class="sxs-lookup"><span data-stu-id="4c39d-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="4c39d-138">Корректировки кредитного лимита клиента</span><span class="sxs-lookup"><span data-stu-id="4c39d-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="4c39d-139">Удержания по кредитам для заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="4c39d-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="4c39d-140">Периодические задачи управления кредитами клиента</span><span class="sxs-lookup"><span data-stu-id="4c39d-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)
