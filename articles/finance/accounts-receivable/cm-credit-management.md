---
title: Управление кредитованием клиента
description: ''
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
ms.openlocfilehash: 11da8b7fb59bc8f3e2568ada27db753cc815b9c2
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015368"
---
# <a name="customer-credit-management-overview"></a><span data-ttu-id="f7f2d-102">Обзор управления кредитованием клиента</span><span class="sxs-lookup"><span data-stu-id="f7f2d-102">Customer credit management overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f7f2d-103">Управление кредитованием клиента позволяет управлять кредитными лимитами и управлять потоком заказов на продажу с помощью процесса разноски на основе созданных вами правил кредита.</span><span class="sxs-lookup"><span data-stu-id="f7f2d-103">Customer credit management allows you to manage credit limits and control the flow of sales orders through the posting process based on credit rules that you create.</span></span> 

<span data-ttu-id="f7f2d-104">Процесс управления кредитованием может включать некоторые или все из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="f7f2d-104">The process for using credit management can include some or all of the following steps:</span></span>
- <span data-ttu-id="f7f2d-105">Обновление атрибутов кредита для клиентов, чтобы предоставить дополнительную информацию о кредитоспособности</span><span class="sxs-lookup"><span data-stu-id="f7f2d-105">Update customers with credit attributes that provide additional information about their credit worthiness</span></span> 
- <span data-ttu-id="f7f2d-106">Создание кредитных лимитов для клиентов через корректировки кредитного лимита</span><span class="sxs-lookup"><span data-stu-id="f7f2d-106">Create credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="f7f2d-107">Создание временных кредитных лимитов для клиентов, используя корректировки кредитного лимита, когда требуется временно увеличить или уменьшить кредитный лимит в зависимости от потребностей бизнеса</span><span class="sxs-lookup"><span data-stu-id="f7f2d-107">Create temporary credit limits for customers using credit limit adjustments when you want to increase or decrease their credit limit temporarily based on business needs</span></span>
- <span data-ttu-id="f7f2d-108">Добавление дополнительных сведений, которые могут влиять на кредитный лимит, таких как сведения о страховании и гарантиях</span><span class="sxs-lookup"><span data-stu-id="f7f2d-108">Add additional information that can affect the credit limit such as insurance and guarantees</span></span>
- <span data-ttu-id="f7f2d-109">Создание кредитных групп клиентов, которые связывают клиентов друг с другом, чтобы они могли совместно использовать один кредитный лимит</span><span class="sxs-lookup"><span data-stu-id="f7f2d-109">Create customer credit groups that link customers together so they can share a single credit limit</span></span>
- <span data-ttu-id="f7f2d-110">Определение показателей риска для клиентов, а затем использование отчетов, чтобы автоматически создать кредитные лимиты для этих клиентов с помощью корректировок кредитного лимита</span><span class="sxs-lookup"><span data-stu-id="f7f2d-110">Assign risk scores to customers and then use those scores to automatically generate credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="f7f2d-111">Создание правил блокировки, которые блокируют заказ в ходе одного или нескольких процессов разноски, на основе таких факторов, как риск, условия оплаты, кредитные лимиты, просроченные суммы и процент используемого кредитного лимита</span><span class="sxs-lookup"><span data-stu-id="f7f2d-111">Create blocking rules that will place an order on hold during one or more posting processes based on factors such as risk, payment terms, credit limits, overdue amounts, and percentage of credit limit used</span></span>
- <span data-ttu-id="f7f2d-112">Управление списком заказов на продажу, которые должны быть заблокированы, просмотр причин блокировки и вариантов смягчения</span><span class="sxs-lookup"><span data-stu-id="f7f2d-112">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate the issues</span></span>
- <span data-ttu-id="f7f2d-113">Выпуск заказов на продажу и разрешение продолжения процесса разноски</span><span class="sxs-lookup"><span data-stu-id="f7f2d-113">Release sales orders and allow it to continue through the posting process</span></span>
- <span data-ttu-id="f7f2d-114">Настройка workflow-процесса для управления утверждением изменений кредитного лимита и выпуска заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="f7f2d-114">Set up workflow to manage the approval of credit limit changes and sales order releases</span></span>


<a name="additional-resources"></a><span data-ttu-id="f7f2d-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f7f2d-115">Additional resources</span></span>
--------
[<span data-ttu-id="f7f2d-116">Настройка параметров управления кредитами клиентов</span><span class="sxs-lookup"><span data-stu-id="f7f2d-116">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="f7f2d-117">Информация о настройке управления кредитами клиентов</span><span class="sxs-lookup"><span data-stu-id="f7f2d-117">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="f7f2d-118">Добавление сведений об управлении кредитом для клиента</span><span class="sxs-lookup"><span data-stu-id="f7f2d-118">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="f7f2d-119">Кредитные группы клиентов</span><span class="sxs-lookup"><span data-stu-id="f7f2d-119">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="f7f2d-120">Корректировки кредитного лимита клиента</span><span class="sxs-lookup"><span data-stu-id="f7f2d-120">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="f7f2d-121">Удержания по кредитам для заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="f7f2d-121">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="f7f2d-122">Периодические задачи управления кредитами клиента</span><span class="sxs-lookup"><span data-stu-id="f7f2d-122">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


