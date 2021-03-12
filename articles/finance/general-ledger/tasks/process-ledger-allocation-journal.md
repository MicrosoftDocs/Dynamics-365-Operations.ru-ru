---
title: Обработка журнала распределения ГК
description: В этой теме объясняется, как обрабатывать запросы распределения в Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a7e8c3ef6fa85daec2a191b433b1ec4ece441ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968487"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="09bd8-103">Обработка журнала распределения ГК</span><span class="sxs-lookup"><span data-stu-id="09bd8-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09bd8-104">В этой теме объясняется, как обрабатывать запросы распределения.</span><span class="sxs-lookup"><span data-stu-id="09bd8-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="09bd8-105">Страница "Обработать запрос на распределение" используется для создания журнала распределения, который можно просмотреть и утвердить перед разноской в главную книгу или можно сразу же разнести в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="09bd8-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="09bd8-106">Прежде чем создавать журнал распределений, должно быть как минимум одно активное правило распределения книги учета.</span><span class="sxs-lookup"><span data-stu-id="09bd8-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="09bd8-107">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="09bd8-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="09bd8-108">В области переходов выберите **Модули > Главная книга > Распределения > Обработать запрос на распределение**.</span><span class="sxs-lookup"><span data-stu-id="09bd8-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="09bd8-109">В поле **Правило** выберите требуемую запись в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="09bd8-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="09bd8-110">В поле **Состояние на дату** введите дату.</span><span class="sxs-lookup"><span data-stu-id="09bd8-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="09bd8-111">**Состояние на дату** очень важно, когда книга учета является источником данных для правила.</span><span class="sxs-lookup"><span data-stu-id="09bd8-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="09bd8-112">Эта дата определяет, какие сальдо главной книги необходимо включить для распределения.</span><span class="sxs-lookup"><span data-stu-id="09bd8-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="09bd8-113">В поле **Нулевое исходное значение** выберите **Стоп**.</span><span class="sxs-lookup"><span data-stu-id="09bd8-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="09bd8-114">При этом будет остановлен процесс распределения и отобразится сообщение, указывающее на выбор нулевой исходной суммы.</span><span class="sxs-lookup"><span data-stu-id="09bd8-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="09bd8-115">В поле **Параметры предложения** выберите **Только предложение**.</span><span class="sxs-lookup"><span data-stu-id="09bd8-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="09bd8-116">Выберите **Только предложение** для просмотра и при необходимости утвердите результат в журналах распределения до разноски распределения в главной книге.</span><span class="sxs-lookup"><span data-stu-id="09bd8-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="09bd8-117">В поле "Дата разноски ГК" введите дату.</span><span class="sxs-lookup"><span data-stu-id="09bd8-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="09bd8-118">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="09bd8-118">Select **OK**.</span></span>
7. <span data-ttu-id="09bd8-119">В области переходов выберите **Модули > Главная книга > Распределения > Журналы распределения**.</span><span class="sxs-lookup"><span data-stu-id="09bd8-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="09bd8-120">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="09bd8-120">Select **Lines**.</span></span>
9. <span data-ttu-id="09bd8-121">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="09bd8-121">Select **Post**.</span></span>
10. <span data-ttu-id="09bd8-122">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="09bd8-122">Select **Post**.</span></span>

