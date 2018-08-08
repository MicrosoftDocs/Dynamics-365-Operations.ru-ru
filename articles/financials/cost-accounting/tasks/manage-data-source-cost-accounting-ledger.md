--- 
title: "Управление источником данных для книги учета затрат"
description: "Эта процедура используется для управления источником данных главной книги для книги учета затрат."
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: f53101d73bc69199fafb00de0fa1759d59ea4ce8
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="4c8be-103">Управление источником данных для книги учета затрат</span><span class="sxs-lookup"><span data-stu-id="4c8be-103">Manage a data source for the cost accounting ledger</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4c8be-104">Эта процедура используется для управления источником данных главной книги для книги учета затрат.</span><span class="sxs-lookup"><span data-stu-id="4c8be-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="4c8be-105">Перед выполнением этой задачи не забудьте воспроизвести проводники по задачам "Создание книги учета затрат" и "Определение единиц управления затратами".</span><span class="sxs-lookup"><span data-stu-id="4c8be-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="4c8be-106">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="4c8be-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="4c8be-107">Перейдите в раздел "Учет затрат" > "Настройка главной книги" > "Книги учета затрат".</span><span class="sxs-lookup"><span data-stu-id="4c8be-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="4c8be-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4c8be-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4c8be-109">Щелкните "Фактические версии".</span><span class="sxs-lookup"><span data-stu-id="4c8be-109">Click Actual versions.</span></span>
4. <span data-ttu-id="4c8be-110">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="4c8be-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="4c8be-111">Щелкните "Главная книга".</span><span class="sxs-lookup"><span data-stu-id="4c8be-111">Click General ledger.</span></span>
6. <span data-ttu-id="4c8be-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4c8be-112">Click New.</span></span>
7. <span data-ttu-id="4c8be-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4c8be-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="4c8be-114">В поле "Поставщик данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4c8be-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="4c8be-115">В данном примере выберите "Dynamics 365 for Finance and Operations  — записи главной книги".</span><span class="sxs-lookup"><span data-stu-id="4c8be-115">For this example, select Dynamics 365 for Finance and Operations - General ledger entries.</span></span>  
9. <span data-ttu-id="4c8be-116">В поле "Аналитика элемента затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4c8be-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="4c8be-117">В этом примере выберите "Элементы затрат".</span><span class="sxs-lookup"><span data-stu-id="4c8be-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="4c8be-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4c8be-118">Click Save.</span></span>
11. <span data-ttu-id="4c8be-119">Щелкните "Настройка поставщика данных".</span><span class="sxs-lookup"><span data-stu-id="4c8be-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="4c8be-120">В поле "Юридическое лицо" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4c8be-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="4c8be-121">В этом примере выберите USP2.</span><span class="sxs-lookup"><span data-stu-id="4c8be-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="4c8be-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4c8be-122">Click New.</span></span>
14. <span data-ttu-id="4c8be-123">В поле "Слой разноски" выберите "Текущий".</span><span class="sxs-lookup"><span data-stu-id="4c8be-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="4c8be-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4c8be-124">Click OK.</span></span>


