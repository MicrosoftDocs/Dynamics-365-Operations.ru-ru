---
title: Создание и ведение блокировки запасов
description: В этой процедуре показано, как блокировать запасы во избежание резервирования физических запасов в наличии другими исходящими документами-источниками.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5fb3c7fc5dbeb6263357113d2a9348afc5b1ac9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212755"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="e2c81-103">Создание и ведение блокировки запасов</span><span class="sxs-lookup"><span data-stu-id="e2c81-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2c81-104">В этой процедуре показано, как блокировать запасы во избежание резервирования физических запасов в наличии другими исходящими документами-источниками.</span><span class="sxs-lookup"><span data-stu-id="e2c81-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="e2c81-105">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF и приведенные значения-примеры.</span><span class="sxs-lookup"><span data-stu-id="e2c81-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="e2c81-106">Перед началом процедуры необходимо иметь номенклатуру с физическими запасами в наличии.</span><span class="sxs-lookup"><span data-stu-id="e2c81-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="e2c81-107">Создание блокировки запасов</span><span class="sxs-lookup"><span data-stu-id="e2c81-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="e2c81-108">В **области перехода** выберите **Модули > Управление запасами > Периодические задачи > Блокировка запасов**.</span><span class="sxs-lookup"><span data-stu-id="e2c81-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="e2c81-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e2c81-109">Click **New**.</span></span>
3. <span data-ttu-id="e2c81-110">В поле **Код номенклатуры** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e2c81-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e2c81-111">Выберите в списке нужную номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="e2c81-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="e2c81-112">Выберите код номенклатуры с физическими запасами в наличии, которые требуется заблокировать.</span><span class="sxs-lookup"><span data-stu-id="e2c81-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="e2c81-113">При использовании USMF можно выбрать номенклатуру M9201.</span><span class="sxs-lookup"><span data-stu-id="e2c81-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="e2c81-114">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="e2c81-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="e2c81-115">При использовании номенклатуры M9201 необходимо выбрать меньше 200.</span><span class="sxs-lookup"><span data-stu-id="e2c81-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="e2c81-116">Разверните экспресс-вкладку **Складские аналитики**.</span><span class="sxs-lookup"><span data-stu-id="e2c81-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="e2c81-117">В поле **Склад** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e2c81-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e2c81-118">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e2c81-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="e2c81-119">При использовании номенклатуры M9201 можно выбрать склад 51.</span><span class="sxs-lookup"><span data-stu-id="e2c81-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="e2c81-120">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e2c81-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="e2c81-121">Обновление условий блокировки запасов</span><span class="sxs-lookup"><span data-stu-id="e2c81-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="e2c81-122">На экспресс-вкладке **Общие** в поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="e2c81-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="e2c81-123">Обновите поле количества запасов, чтобы отразить блокируемое количество.</span><span class="sxs-lookup"><span data-stu-id="e2c81-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="e2c81-124">В поле **Ожидаемая дата** введите дату.</span><span class="sxs-lookup"><span data-stu-id="e2c81-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="e2c81-125">Есть смысл указать, когда ожидается, что заблокированные запасы будут доступны для резервирования, путем назначения ожидаемой даты.</span><span class="sxs-lookup"><span data-stu-id="e2c81-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="e2c81-126">Если для блокировки запасов выбран вариант "Ожидаемые приходы" (это происходит по умолчанию при создании блокировки вручную), эта дата будет присутствовать в ожидаемой проводке.</span><span class="sxs-lookup"><span data-stu-id="e2c81-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="e2c81-127">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e2c81-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="e2c81-128">Снятие блокировки запасов</span><span class="sxs-lookup"><span data-stu-id="e2c81-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="e2c81-129">В **области действий** щелкните **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e2c81-129">On the **Action Pane**, click **Delete**.</span></span>
2. <span data-ttu-id="e2c81-130">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="e2c81-130">Click **Yes**.</span></span>
3. <span data-ttu-id="e2c81-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e2c81-131">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]