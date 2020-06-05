---
title: Определение политик расходов
description: Можно определить политики расходов, которым должны следовать ваши работники при вводе и отправке отчетов по расходам и заявок на командировку в Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389723"
---
# <a name="define-expense-policies"></a><span data-ttu-id="e285b-103">Определение политик расходов</span><span class="sxs-lookup"><span data-stu-id="e285b-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e285b-104">Вы можете определить политики, которым должны следовать работники при вводе и отправке отчетов о расходах и заявок на командировки.</span><span class="sxs-lookup"><span data-stu-id="e285b-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="e285b-105">Использование политик расходов может помочь эффективно управлять расходами.</span><span class="sxs-lookup"><span data-stu-id="e285b-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="e285b-106">Например, можно установить политику в отношении гостиничных расходов в Нью-Йорке, в соответствии с которой расходы на проживание в гостинице не должны превышать 250 USD в сутки.</span><span class="sxs-lookup"><span data-stu-id="e285b-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="e285b-107">Если работник отправит отчет о расходах или заявку на командировку, в которой стоимость суточного проживания превышает эту сумму, система уведомит</span><span class="sxs-lookup"><span data-stu-id="e285b-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="e285b-108">работника о превышении суммы, установленной в политике расходов.</span><span class="sxs-lookup"><span data-stu-id="e285b-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="e285b-109">Можно настроить сообщение, которое будут получать работники</span><span class="sxs-lookup"><span data-stu-id="e285b-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="e285b-110">при определении политики.</span><span class="sxs-lookup"><span data-stu-id="e285b-110">define the policy.</span></span>      
        
<span data-ttu-id="e285b-111">Можно определить три типа политик.</span><span class="sxs-lookup"><span data-stu-id="e285b-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="e285b-112">Предупреждение — работник может отправить отчет о расходах или заявку на командировку, но расходы будут помечены для всех утверждающих лиц</span><span class="sxs-lookup"><span data-stu-id="e285b-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="e285b-113">и для последующей отчетности.</span><span class="sxs-lookup"><span data-stu-id="e285b-113">for later reporting.</span></span>        

- <span data-ttu-id="e285b-114">Ошибка. Перед отправкой отчета о расходах или заявки на командировку работник должен проверить расходы на соответствие политике.</span><span class="sxs-lookup"><span data-stu-id="e285b-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="e285b-115">Обоснование. Перед отправкой отчета о расходах или заявки на командировку работник или руководитель должен ввести обоснование для превышения суммы политики.</span><span class="sxs-lookup"><span data-stu-id="e285b-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="e285b-116">Рекомендации по политикам</span><span class="sxs-lookup"><span data-stu-id="e285b-116">Policy tips</span></span>
<span data-ttu-id="e285b-117">Вот несколько советов, которые помогут создавать новые политики для управления расходами.</span><span class="sxs-lookup"><span data-stu-id="e285b-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="e285b-118">Политики действуют с определенной даты и не вступят в силу, если политика создана с датой, которая позже даты возникновения расхода.</span><span class="sxs-lookup"><span data-stu-id="e285b-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="e285b-119">Например, если сегодня создается новая политика, ограничивающая расходы на питание максимальной суммой 50 долларов США, то все существующие расходы, введенные по вчерашний день, не будут проверяться относительно этой политики.</span><span class="sxs-lookup"><span data-stu-id="e285b-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="e285b-120">При создании политики для категории расходов, которая может быть детализирована, следует добавить условие для типа строки расходов.</span><span class="sxs-lookup"><span data-stu-id="e285b-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="e285b-121">Некоторые политики, такие как требование чека, могут не иметь смысла для детализированных строк и должны применяться только к строке заголовка или к недетализированной строке.</span><span class="sxs-lookup"><span data-stu-id="e285b-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="e285b-122">Политики управления расходами по умолчанию оцениваются относительно объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e285b-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="e285b-123">Для внутрихолдинговых сценариев можно настроить политику для оценки относительно целевого объекта (заимствующего объекта).</span><span class="sxs-lookup"><span data-stu-id="e285b-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="e285b-124">Чтобы выполнить политики для целевого объекта, включите функцию "оценивать политику расходов относительно заимствующего объекта" в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="e285b-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="e285b-125">Когда следует выполнять оценку политик</span><span class="sxs-lookup"><span data-stu-id="e285b-125">When to evaluate policies</span></span>

<span data-ttu-id="e285b-126">В параметрах управления расходами имеется параметр выбора времени оценки политик управления расходами: при сохранении строки или при отправке отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="e285b-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="e285b-127">Если выбирается оценка при сохранении строки, это гарантирует, что пользователи будут иметь более ранний одновременный просмотр всех тех действий, которые необходимо выполнить для заполнения отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="e285b-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="e285b-128">В противном случае можно отложить оценку политики и сэкономить время, если проверка выполняется в конце, во время отправки в рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="e285b-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
