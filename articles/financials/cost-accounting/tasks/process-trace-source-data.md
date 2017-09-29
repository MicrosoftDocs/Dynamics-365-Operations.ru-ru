--- 
title: "Обработка и трассировка исходных данных"
description: "Вся обработка данных выполняется посредством заданий."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7093338fd306e90df79a787f9de9861b3fe49dd5
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="c19d1-103">Обработка и трассировка исходных данных</span><span class="sxs-lookup"><span data-stu-id="c19d1-103">Process and trace source data</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c19d1-104">Вся обработка данных выполняется посредством заданий.</span><span class="sxs-lookup"><span data-stu-id="c19d1-104">All data processing is run by jobs.</span></span> <span data-ttu-id="c19d1-105">Для каждого задания и поставщика данных создается журнал для документирования того, что процесс был выполнен, и что были обработаны записи в текущем задании.</span><span class="sxs-lookup"><span data-stu-id="c19d1-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="c19d1-106">Эта процедура используется для настройки источника данных с последующим отслеживанием основания конкретной записи затрат.</span><span class="sxs-lookup"><span data-stu-id="c19d1-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="c19d1-107">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="c19d1-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="c19d1-108">Перед выполнением этой задачи не забудьте воспроизвести следующие проводники по задачам: "Создание книги учета затрат", "Определение единиц управления затратами" и "Управление источником данных для книги учета затрат".</span><span class="sxs-lookup"><span data-stu-id="c19d1-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="c19d1-109">Перейдите в раздел "Учет затрат" > "Настройка главной книги" > "Книги учета затрат".</span><span class="sxs-lookup"><span data-stu-id="c19d1-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="c19d1-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c19d1-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c19d1-111">Выберите ранее созданную книгу учета затрат.</span><span class="sxs-lookup"><span data-stu-id="c19d1-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="c19d1-112">Щелкните "Фактические версии".</span><span class="sxs-lookup"><span data-stu-id="c19d1-112">Click Actual versions.</span></span>
4. <span data-ttu-id="c19d1-113">На панели операций щелкните "Обработка исходный данных".</span><span class="sxs-lookup"><span data-stu-id="c19d1-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="c19d1-114">Щелкните "Журналы переноса записей главной книги".</span><span class="sxs-lookup"><span data-stu-id="c19d1-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="c19d1-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c19d1-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c19d1-116">Щелкните "Записи журнала".</span><span class="sxs-lookup"><span data-stu-id="c19d1-116">Click Journal entries.</span></span>
8. <span data-ttu-id="c19d1-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="c19d1-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="c19d1-118">Щелкните "Записи затрат".</span><span class="sxs-lookup"><span data-stu-id="c19d1-118">Click Cost entries.</span></span>
10. <span data-ttu-id="c19d1-119">Щелкните "Исходная запись".</span><span class="sxs-lookup"><span data-stu-id="c19d1-119">Click Source entry.</span></span>
11. <span data-ttu-id="c19d1-120">На панели операций щелкните "Обработка исходный данных".</span><span class="sxs-lookup"><span data-stu-id="c19d1-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="c19d1-121">Щелкните "Главная книга".</span><span class="sxs-lookup"><span data-stu-id="c19d1-121">Click General ledger.</span></span>
13. <span data-ttu-id="c19d1-122">В поле "Период финансового календаря" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c19d1-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="c19d1-123">В этом примере выберите "Fiscal 2017 Period 9".</span><span class="sxs-lookup"><span data-stu-id="c19d1-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="c19d1-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c19d1-124">Click OK.</span></span>


