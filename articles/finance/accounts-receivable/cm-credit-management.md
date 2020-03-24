---
title: Управление кредитованием клиента
description: Управление кредитованием клиента позволяет управлять кредитными лимитами и управлять потоком заказов на продажу с помощью процесса разноски на основе созданных вами правил кредита.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e7d3325587d7cfc876e8f8c7b9207d44046ccd4
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124285"
---
# <a name="customer-credit-management-overview"></a><span data-ttu-id="9adba-103">Обзор управления кредитованием клиента</span><span class="sxs-lookup"><span data-stu-id="9adba-103">Customer credit management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9adba-104">Управление кредитованием клиента позволяет управлять кредитными лимитами и управлять потоком заказов на продажу с помощью процесса разноски на основе созданных вами правил кредита.</span><span class="sxs-lookup"><span data-stu-id="9adba-104">Customer credit management allows you to manage credit limits and control the flow of sales orders through the posting process based on credit rules that you create.</span></span> 

<span data-ttu-id="9adba-105">Процесс управления кредитованием может включать некоторые или все из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="9adba-105">The process for using credit management can include some or all of the following steps:</span></span>
- <span data-ttu-id="9adba-106">Обновление атрибутов кредита для клиентов, чтобы предоставить дополнительную информацию о кредитоспособности</span><span class="sxs-lookup"><span data-stu-id="9adba-106">Update customers with credit attributes that provide additional information about their credit worthiness</span></span> 
- <span data-ttu-id="9adba-107">Создание кредитных лимитов для клиентов через корректировки кредитного лимита</span><span class="sxs-lookup"><span data-stu-id="9adba-107">Create credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="9adba-108">Создание временных кредитных лимитов для клиентов, используя корректировки кредитного лимита, когда требуется временно увеличить или уменьшить кредитный лимит в зависимости от потребностей бизнеса</span><span class="sxs-lookup"><span data-stu-id="9adba-108">Create temporary credit limits for customers using credit limit adjustments when you want to increase or decrease their credit limit temporarily based on business needs</span></span>
- <span data-ttu-id="9adba-109">Добавление дополнительных сведений, которые могут влиять на кредитный лимит, таких как сведения о страховании и гарантиях</span><span class="sxs-lookup"><span data-stu-id="9adba-109">Add additional information that can affect the credit limit such as insurance and guarantees</span></span>
- <span data-ttu-id="9adba-110">Создание кредитных групп клиентов, которые связывают клиентов друг с другом, чтобы они могли совместно использовать один кредитный лимит</span><span class="sxs-lookup"><span data-stu-id="9adba-110">Create customer credit groups that link customers together so they can share a single credit limit</span></span>
- <span data-ttu-id="9adba-111">Определение показателей риска для клиентов, а затем использование отчетов, чтобы автоматически создать кредитные лимиты для этих клиентов с помощью корректировок кредитного лимита</span><span class="sxs-lookup"><span data-stu-id="9adba-111">Assign risk scores to customers and then use those scores to automatically generate credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="9adba-112">Создание правил блокировки, которые блокируют заказ в ходе одного или нескольких процессов разноски, на основе таких факторов, как риск, условия оплаты, кредитные лимиты, просроченные суммы и процент используемого кредитного лимита</span><span class="sxs-lookup"><span data-stu-id="9adba-112">Create blocking rules that will place an order on hold during one or more posting processes based on factors such as risk, payment terms, credit limits, overdue amounts, and percentage of credit limit used</span></span>
- <span data-ttu-id="9adba-113">Управление списком заказов на продажу, которые должны быть заблокированы, просмотр причин блокировки и вариантов смягчения</span><span class="sxs-lookup"><span data-stu-id="9adba-113">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate the issues</span></span>
- <span data-ttu-id="9adba-114">Выпуск заказов на продажу и разрешение продолжения процесса разноски</span><span class="sxs-lookup"><span data-stu-id="9adba-114">Release sales orders and allow it to continue through the posting process</span></span>
- <span data-ttu-id="9adba-115">Настройка workflow-процесса для управления утверждением изменений кредитного лимита и выпуска заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="9adba-115">Set up workflow to manage the approval of credit limit changes and sales order releases</span></span>


<a name="additional-resources"></a><span data-ttu-id="9adba-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9adba-116">Additional resources</span></span>
--------
[<span data-ttu-id="9adba-117">Настройка параметров управления кредитами клиентов</span><span class="sxs-lookup"><span data-stu-id="9adba-117">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="9adba-118">Информация о настройке управления кредитами клиентов</span><span class="sxs-lookup"><span data-stu-id="9adba-118">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="9adba-119">Добавление сведений об управлении кредитом для клиента</span><span class="sxs-lookup"><span data-stu-id="9adba-119">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="9adba-120">Кредитные группы клиентов</span><span class="sxs-lookup"><span data-stu-id="9adba-120">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="9adba-121">Корректировки кредитного лимита клиента</span><span class="sxs-lookup"><span data-stu-id="9adba-121">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="9adba-122">Удержания по кредитам для заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="9adba-122">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="9adba-123">Периодические задачи управления кредитами клиента</span><span class="sxs-lookup"><span data-stu-id="9adba-123">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


