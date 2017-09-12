--- 
title: "Обработка журнала распределения ГК"
description: "Страница \"Обработать запрос на распределение\" используется для создания журнала распределения, который можно просмотреть и утвердить перед разноской в главную книгу или можно сразу же разнести в главную книгу."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7d299657758b1e1322aef07bfe8c71f7bf00b0ca
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="1f494-103">Обработка журнала распределения ГК</span><span class="sxs-lookup"><span data-stu-id="1f494-103">Process ledger allocation journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f494-104">Страница "Обработать запрос на распределение" используется для создания журнала распределения, который можно просмотреть и утвердить перед разноской в главную книгу или можно сразу же разнести в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="1f494-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="1f494-105">Прежде чем создавать журнал распределений, должно быть как минимум одно активное правило распределения книги учета.</span><span class="sxs-lookup"><span data-stu-id="1f494-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="1f494-106">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="1f494-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1f494-107">Перейдите в раздел "Главная книга" > "Распределения" > "Обработка запроса на распределение".</span><span class="sxs-lookup"><span data-stu-id="1f494-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="1f494-108">В поле "Правило" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="1f494-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="1f494-109">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="1f494-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="1f494-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="1f494-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1f494-111">В поле "Состояние на дату" введите дату.</span><span class="sxs-lookup"><span data-stu-id="1f494-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="1f494-112">"Состояние на дату" очень важно, когда книга учета является источником данных для правила.</span><span class="sxs-lookup"><span data-stu-id="1f494-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="1f494-113">Эта дата определяет, какие сальдо главной книги необходимо включить для распределения.</span><span class="sxs-lookup"><span data-stu-id="1f494-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="1f494-114">В поле "Нулевое исходное значение" выберите "Стоп".</span><span class="sxs-lookup"><span data-stu-id="1f494-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="1f494-115">При этом будет остановлен процесс распределения и отобразится сообщение, указывающее на выбор нулевой исходной суммы.</span><span class="sxs-lookup"><span data-stu-id="1f494-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="1f494-116">В поле "Параметры предложения" выберите "Только предложение".</span><span class="sxs-lookup"><span data-stu-id="1f494-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="1f494-117">Выберите предложение только для просмотра и при необходимости утвердите результат в журналах распределения до разноски распределения в главной книге.</span><span class="sxs-lookup"><span data-stu-id="1f494-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="1f494-118">В поле "Дата разноски ГК" введите дату.</span><span class="sxs-lookup"><span data-stu-id="1f494-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="1f494-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1f494-119">Click OK.</span></span>
9. <span data-ttu-id="1f494-120">Перейдите в раздел "Главная книга" > "Распределения" > "Журналы распределений".</span><span class="sxs-lookup"><span data-stu-id="1f494-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="1f494-121">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="1f494-121">Click Lines.</span></span>
11. <span data-ttu-id="1f494-122">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="1f494-122">Click Post.</span></span>
12. <span data-ttu-id="1f494-123">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="1f494-123">Click Post.</span></span>


