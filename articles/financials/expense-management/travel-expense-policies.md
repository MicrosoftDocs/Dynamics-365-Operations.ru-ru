---
title: "Определение политик расходов"
description: "Можно определить политики расходов, которым должны следовать ваши работники при вводе и отправке отчетов по расходам и заявок на командировку в Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: b0f9a5ca275944aeb27798a2f3377356319589c7
ms.contentlocale: ru-ru
ms.lasthandoff: 01/17/2018

---

# <a name="expense-policies"></a><span data-ttu-id="9ffe6-103">Политики расходов</span><span class="sxs-lookup"><span data-stu-id="9ffe6-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9ffe6-104">Вы можете определить политики, которым должны следовать работники при вводе и отправке отчетов о расходах и заявок на командировки.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="9ffe6-105">Использование политик расходов может помочь эффективно управлять расходами.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="9ffe6-106">Например, можно установить политику в отношении гостиничных расходов в Нью-Йорке, в соответствии с которой расходы на проживание в гостинице не должны превышать 250 USD в сутки.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="9ffe6-107">Если сотрудник отправит отчет о расходах или заявку на командировку, в котором стоимость суточного проживания превышает эту сумму, система уведомит работника о превышении суммы, установленной в политике расходов.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="9ffe6-108">Можно настроить сообщение, которое будут получать работники при определении политики.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="9ffe6-109">Можно определить три типа политик.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="9ffe6-110">Предупреждение — работник может отправить отчет о расходах или заявку на командировку, но расходы будут помечены для всех утверждающих лиц</span><span class="sxs-lookup"><span data-stu-id="9ffe6-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="9ffe6-111">и для последующей отчетности.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-111">for later reporting.</span></span> 
 - <span data-ttu-id="9ffe6-112">Ошибка. Перед отправкой отчета о расходах или заявки на командировку работник должен проверить расходы на соответствие политике.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="9ffe6-113">Обоснование. Перед отправкой отчета о расходах или заявки на командировку работник или руководитель должен ввести обоснование для превышения суммы политики.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="9ffe6-114">Также можно настроить диапазон дат, в пределах которого действуют политики расходов.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="9ffe6-115">Например, тарифы авиакомпаний для перелетов между Данией и Нью-Йорком в период массовых отпусков могут быть высокими.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="9ffe6-116">Можно определить правило расходов на перелеты, которое ограничивает стоимость авиабилетов до Нью-Йорка предельной суммой в 5000 датских крон, и указать, что это правило действует с 15 марта по 15 сентября.</span><span class="sxs-lookup"><span data-stu-id="9ffe6-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

