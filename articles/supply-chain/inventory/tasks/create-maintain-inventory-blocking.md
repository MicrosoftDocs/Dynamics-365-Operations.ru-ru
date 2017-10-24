---
title: "Создание и ведение блокировки запасов"
description: "В этой процедуре показано, как блокировать запасы во избежание резервирования физических запасов в наличии другими исходящими документами-источниками."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-maintain-inventory-blocking"></a><span data-ttu-id="435f9-103">Создание и ведение блокировки запасов</span><span class="sxs-lookup"><span data-stu-id="435f9-103">Create and maintain inventory blocking</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="435f9-104">В этой процедуре показано, как блокировать запасы во избежание резервирования физических запасов в наличии другими исходящими документами-источниками.</span><span class="sxs-lookup"><span data-stu-id="435f9-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="435f9-105">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF и приведенные значения-примеры.</span><span class="sxs-lookup"><span data-stu-id="435f9-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="435f9-106">Перед началом процедуры необходимо иметь номенклатуру с физическими запасами в наличии.</span><span class="sxs-lookup"><span data-stu-id="435f9-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="435f9-107">Создание блокировки запасов</span><span class="sxs-lookup"><span data-stu-id="435f9-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="435f9-108">Перейдите в раздел "Управление запасами" > "Периодические задачи" > "Блокировка запасов".</span><span class="sxs-lookup"><span data-stu-id="435f9-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="435f9-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="435f9-109">Click New.</span></span>
3. <span data-ttu-id="435f9-110">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="435f9-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="435f9-111">Выберите в списке нужную номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="435f9-111">In the list, select the item you want to choose.</span></span>
    * <span data-ttu-id="435f9-112">Выберите код номенклатуры с физическими запасами в наличии, которые требуется заблокировать.</span><span class="sxs-lookup"><span data-stu-id="435f9-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="435f9-113">При использовании USMF можно выбрать номенклатуру M9201.</span><span class="sxs-lookup"><span data-stu-id="435f9-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="435f9-114">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="435f9-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="435f9-115">При использовании номенклатуры M9201 необходимо выбрать меньше 200.</span><span class="sxs-lookup"><span data-stu-id="435f9-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="435f9-116">Переключите развертывание раздела "Складские аналитики".</span><span class="sxs-lookup"><span data-stu-id="435f9-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="435f9-117">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="435f9-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="435f9-118">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="435f9-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="435f9-119">При использовании номенклатуры M9201 можно выбрать склад 51.</span><span class="sxs-lookup"><span data-stu-id="435f9-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="435f9-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435f9-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="435f9-121">Обновление условий блокировки запасов</span><span class="sxs-lookup"><span data-stu-id="435f9-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="435f9-122">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="435f9-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="435f9-123">Обновите поле количества запасов, чтобы отразить блокируемое количество.</span><span class="sxs-lookup"><span data-stu-id="435f9-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="435f9-124">В поле "Ожидаемая дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="435f9-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="435f9-125">Есть смысл указать, когда ожидается, что заблокированные запасы будут доступны для резервирования, путем назначения ожидаемой даты.</span><span class="sxs-lookup"><span data-stu-id="435f9-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="435f9-126">Если для блокировки запасов выбран вариант "Ожидаемые приходы" (это происходит по умолчанию при создании блокировки вручную), эта дата будет присутствовать в ожидаемой проводке.</span><span class="sxs-lookup"><span data-stu-id="435f9-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="435f9-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="435f9-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="435f9-128">Снятие блокировки запасов</span><span class="sxs-lookup"><span data-stu-id="435f9-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="435f9-129">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="435f9-129">Click Delete.</span></span>
2. <span data-ttu-id="435f9-130">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="435f9-130">Click Yes.</span></span>
3. <span data-ttu-id="435f9-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="435f9-131">Close the page.</span></span>

