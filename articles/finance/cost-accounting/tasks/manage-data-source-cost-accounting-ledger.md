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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7246d42b42404f0f1215bbf14b8ad168fe12691c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990725"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="ddc31-103">Управление источником данных для книги учета затрат</span><span class="sxs-lookup"><span data-stu-id="ddc31-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ddc31-104">Эта процедура используется для управления источником данных главной книги для книги учета затрат.</span><span class="sxs-lookup"><span data-stu-id="ddc31-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="ddc31-105">Перед выполнением этой задачи не забудьте воспроизвести проводники по задачам "Создание книги учета затрат" и "Определение единиц управления затратами".</span><span class="sxs-lookup"><span data-stu-id="ddc31-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="ddc31-106">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="ddc31-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="ddc31-107">Перейдите в раздел "Учет затрат" > "Настройка главной книги" > "Книги учета затрат".</span><span class="sxs-lookup"><span data-stu-id="ddc31-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="ddc31-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ddc31-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ddc31-109">Щелкните "Фактические версии".</span><span class="sxs-lookup"><span data-stu-id="ddc31-109">Click Actual versions.</span></span>
4. <span data-ttu-id="ddc31-110">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="ddc31-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="ddc31-111">Щелкните "Главная книга".</span><span class="sxs-lookup"><span data-stu-id="ddc31-111">Click General ledger.</span></span>
6. <span data-ttu-id="ddc31-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ddc31-112">Click New.</span></span>
7. <span data-ttu-id="ddc31-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddc31-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="ddc31-114">В поле "Поставщик данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ddc31-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="ddc31-115">В этом примере выберите "Dynamics 365 Finance — записи главной книги".</span><span class="sxs-lookup"><span data-stu-id="ddc31-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="ddc31-116">В поле "Аналитика элемента затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ddc31-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="ddc31-117">В этом примере выберите "Элементы затрат".</span><span class="sxs-lookup"><span data-stu-id="ddc31-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="ddc31-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ddc31-118">Click Save.</span></span>
11. <span data-ttu-id="ddc31-119">Щелкните "Настройка поставщика данных".</span><span class="sxs-lookup"><span data-stu-id="ddc31-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="ddc31-120">В поле "Юридическое лицо" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ddc31-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="ddc31-121">В этом примере выберите USP2.</span><span class="sxs-lookup"><span data-stu-id="ddc31-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="ddc31-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ddc31-122">Click New.</span></span>
14. <span data-ttu-id="ddc31-123">В поле "Слой разноски" выберите "Текущий".</span><span class="sxs-lookup"><span data-stu-id="ddc31-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="ddc31-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ddc31-124">Click OK.</span></span>

