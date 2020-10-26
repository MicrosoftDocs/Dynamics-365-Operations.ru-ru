---
title: Управление источником данных для книги учета затрат
description: Эта процедура используется для управления источником данных главной книги для книги учета затрат.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88f5170610ea9b5634c4bf5da7079cacccdafe04
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977583"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="30375-103">Управление источником данных для книги учета затрат</span><span class="sxs-lookup"><span data-stu-id="30375-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30375-104">Эта процедура используется для управления источником данных главной книги для книги учета затрат.</span><span class="sxs-lookup"><span data-stu-id="30375-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="30375-105">Перед выполнением этой задачи не забудьте воспроизвести проводники по задачам "Создание книги учета затрат" и "Определение единиц управления затратами".</span><span class="sxs-lookup"><span data-stu-id="30375-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="30375-106">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="30375-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="30375-107">Перейдите в раздел "Учет затрат" > "Настройка главной книги" > "Книги учета затрат".</span><span class="sxs-lookup"><span data-stu-id="30375-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="30375-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="30375-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="30375-109">Щелкните "Фактические версии".</span><span class="sxs-lookup"><span data-stu-id="30375-109">Click Actual versions.</span></span>
4. <span data-ttu-id="30375-110">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="30375-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="30375-111">Щелкните "Главная книга".</span><span class="sxs-lookup"><span data-stu-id="30375-111">Click General ledger.</span></span>
6. <span data-ttu-id="30375-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="30375-112">Click New.</span></span>
7. <span data-ttu-id="30375-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="30375-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="30375-114">В поле "Поставщик данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30375-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="30375-115">В этом примере выберите "Dynamics 365 Finance — записи главной книги".</span><span class="sxs-lookup"><span data-stu-id="30375-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="30375-116">В поле "Аналитика элемента затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30375-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="30375-117">В этом примере выберите "Элементы затрат".</span><span class="sxs-lookup"><span data-stu-id="30375-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="30375-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="30375-118">Click Save.</span></span>
11. <span data-ttu-id="30375-119">Щелкните "Настройка поставщика данных".</span><span class="sxs-lookup"><span data-stu-id="30375-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="30375-120">В поле "Юридическое лицо" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30375-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="30375-121">В этом примере выберите USP2.</span><span class="sxs-lookup"><span data-stu-id="30375-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="30375-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="30375-122">Click New.</span></span>
14. <span data-ttu-id="30375-123">В поле "Слой разноски" выберите "Текущий".</span><span class="sxs-lookup"><span data-stu-id="30375-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="30375-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30375-124">Click OK.</span></span>

