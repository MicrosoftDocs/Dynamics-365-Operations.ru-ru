---
title: Закрытие ГК в конце периода
description: В этом разделе описаны задачи, которые обычно выполняются при закрытии периода для главной книги.
author: aprilolson
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9781a439469b54e5449382fbdd04447a7f4a079
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821921"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="012ba-103">Закрытие ГК в конце периода</span><span class="sxs-lookup"><span data-stu-id="012ba-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="012ba-104">В этом разделе описаны задачи, которые обычно выполняются при закрытии периода для главной книги.</span><span class="sxs-lookup"><span data-stu-id="012ba-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="012ba-105">В главной книге можно выполнять процедуры закрытия для периода или года.</span><span class="sxs-lookup"><span data-stu-id="012ba-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="012ba-106">Процессы закрытия подготавливают систему к новому периоду.</span><span class="sxs-lookup"><span data-stu-id="012ba-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="012ba-107">Чтобы подготовить систему к новому году, необходимо выполнить процесс закрытия на конец года.</span><span class="sxs-lookup"><span data-stu-id="012ba-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="012ba-108">Каждая организация имеет разные процессы и шаги, выполняемые на конец периода.</span><span class="sxs-lookup"><span data-stu-id="012ba-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="012ba-109">Ниже приведены некоторые необязательные шаги для окончания периода.</span><span class="sxs-lookup"><span data-stu-id="012ba-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="012ba-110">Завершите все задачи для всех других модулей, например Расчеты с поставщиками, Расчеты с клиентами и Запасы.</span><span class="sxs-lookup"><span data-stu-id="012ba-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="012ba-111">Проверьте, что все журналы разнесены.</span><span class="sxs-lookup"><span data-stu-id="012ba-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="012ba-112">Выполните переоценку в иностранной валюте для создания любых сумм внереализационной прибыли или убытков.</span><span class="sxs-lookup"><span data-stu-id="012ba-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="012ba-113">Сопоставьте проводки для каждого счета ГК.</span><span class="sxs-lookup"><span data-stu-id="012ba-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="012ba-114">Обработайте все требуемые распределения.</span><span class="sxs-lookup"><span data-stu-id="012ba-114">Process any required allocations.</span></span>
-   <span data-ttu-id="012ba-115">Вручную разнесите корректировки на конец периода.</span><span class="sxs-lookup"><span data-stu-id="012ba-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="012ba-116">Учтите в субкниге проводки и просмотрите отчет **Журнал ГК**.</span><span class="sxs-lookup"><span data-stu-id="012ba-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="012ba-117">Выполните консолидацию, используя консолидированную компанию или финансовую отчетность.</span><span class="sxs-lookup"><span data-stu-id="012ba-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="012ba-118">Создайте финансовые отчеты на конец периода с помощью финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="012ba-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="012ba-119">Задайте для периодов ГК статус **Заблокировано**, чтобы было невозможно выполнить разноску.</span><span class="sxs-lookup"><span data-stu-id="012ba-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="012ba-120">Также можно ограничить период определенной группой пользователей, пока выполняются действия на конец периода, для более эффективного управления.</span><span class="sxs-lookup"><span data-stu-id="012ba-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="012ba-121">Не рекомендуется задавать для периодов статус **Закрытый на постоянной основе**, поскольку невозможно повторно открыть период, который был закрыт.</span><span class="sxs-lookup"><span data-stu-id="012ba-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="012ba-122">Рабочая область закрытия финансового периода может использоваться для организации и отслеживания задач, необходимых для различных процессов на конец периода.</span><span class="sxs-lookup"><span data-stu-id="012ba-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="012ba-123">Дополнительные сведения см. в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="012ba-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="012ba-124">Рабочая область закрытия финансового периода</span><span class="sxs-lookup"><span data-stu-id="012ba-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="012ba-125">Закрытие на конец года</span><span class="sxs-lookup"><span data-stu-id="012ba-125">Year-end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="012ba-126">Массовое закрытие финансовых периодов</span><span class="sxs-lookup"><span data-stu-id="012ba-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]