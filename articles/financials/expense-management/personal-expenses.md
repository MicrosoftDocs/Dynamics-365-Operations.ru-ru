---
title: "Личные расходы в отчете о расходах"
description: "В этом разделе рассматриваются два метода обработки личных расходов сотрудника в Microsoft Dynamics 365 for Finance and Operations."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 27698b02795b709a167235537d8b1ca871bdd371
ms.contentlocale: ru-ru
ms.lasthandoff: 03/13/2018

---

# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="d1ceb-103">Личные расходы в отчете о расходах</span><span class="sxs-lookup"><span data-stu-id="d1ceb-103">Personal expenses on an expense report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d1ceb-104">Во время командировок работники могут иногда расплачиваться за личные расходы по корпоративным кредитным картам.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="d1ceb-105">Если процедура для обработки личных расходов не определена, процесс утверждения отчетов о расходах может быть нарушен, когда работники представляют детализированные отчеты о расходах.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="d1ceb-106">В Microsoft Dynamics 365 for Finance and Operations предусмотрены два метода обработки личных расходов сотрудника:</span><span class="sxs-lookup"><span data-stu-id="d1ceb-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="d1ceb-107">**Оплачивается сотрудником** — организация не оплачивает личные расходы, которые отображаются в счете по корпоративной кредитной карте.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="d1ceb-108">Организация вместо этого создает отчет, в котором личные и корпоративные расходы, оплаченные по корпоративной кредитной карте, показаны вместе.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="d1ceb-109">**Оплачивается компанией** — организация оплачивает весь счет по корпоративной кредитной карте целиком, а затем дебетует личные расходы со счета работника.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="d1ceb-110">Можно выбрать метод, который используется в вашей организации, на странице **Параметры управления расходами**.</span><span class="sxs-lookup"><span data-stu-id="d1ceb-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>

