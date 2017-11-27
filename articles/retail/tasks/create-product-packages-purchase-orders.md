--- 
title: "Создание пакетов продуктов для заказов на покупку"
description: "Эта процедура содержит инструкции по созданию пакета продуктов и его использованию в заказе на покупку."
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 9d3ea8702c79d8aa6bb7cf7caa922277697610fa
ms.contentlocale: ru-ru
ms.lasthandoff: 11/14/2017

---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="61720-103">Создание пакетов продуктов для заказов на покупку</span><span class="sxs-lookup"><span data-stu-id="61720-103">Create product packages for purchase orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="61720-104">Эта процедура содержит инструкции по созданию пакета продуктов и его использованию в заказе на покупку.</span><span class="sxs-lookup"><span data-stu-id="61720-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="61720-105">Заказ на покупку будет использоваться для создания заказа на заранее определенный набор продуктов.</span><span class="sxs-lookup"><span data-stu-id="61720-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="61720-106">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="61720-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="61720-107">Создание пакета продуктов</span><span class="sxs-lookup"><span data-stu-id="61720-107">Create a product package</span></span>
1. <span data-ttu-id="61720-108">Перейдите в раздел "Розничная торговля и коммерция" > "Управление запасами" > "Пополнение" > "Пакеты продуктов".</span><span class="sxs-lookup"><span data-stu-id="61720-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="61720-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="61720-109">Click New.</span></span>
3. <span data-ttu-id="61720-110">В поле "Номер пакета" введите значение.</span><span class="sxs-lookup"><span data-stu-id="61720-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="61720-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="61720-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="61720-112">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="61720-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="61720-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="61720-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="61720-114">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="61720-114">Click Add.</span></span>
8. <span data-ttu-id="61720-115">В поле "Код номенклатуры" введите "0160".</span><span class="sxs-lookup"><span data-stu-id="61720-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="61720-116">В поле "Размер" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="61720-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="61720-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="61720-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="61720-118">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="61720-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="61720-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="61720-119">Click Add.</span></span>
13. <span data-ttu-id="61720-120">В поле "Код номенклатуры" введите "0160".</span><span class="sxs-lookup"><span data-stu-id="61720-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="61720-121">В поле "Номер варианта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="61720-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="61720-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="61720-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="61720-123">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="61720-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="61720-124">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="61720-124">Click Add.</span></span>
18. <span data-ttu-id="61720-125">В поле "Код номенклатуры" введите "0175".</span><span class="sxs-lookup"><span data-stu-id="61720-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="61720-126">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="61720-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="61720-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="61720-127">Click Save.</span></span>
21. <span data-ttu-id="61720-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="61720-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="61720-129">Добавление пакета в заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="61720-129">Add package to purchase order</span></span>
1. <span data-ttu-id="61720-130">Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="61720-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="61720-131">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="61720-131">Click New.</span></span>
3. <span data-ttu-id="61720-132">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="61720-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="61720-133">В списке выберите поставщика, для которого ранее был создан пакет продуктов, если поставщик был выбран.</span><span class="sxs-lookup"><span data-stu-id="61720-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="61720-134">Переключите развертывание раздела "Общее".</span><span class="sxs-lookup"><span data-stu-id="61720-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="61720-135">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="61720-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="61720-136">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="61720-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="61720-137">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="61720-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="61720-138">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="61720-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="61720-139">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="61720-139">Click OK.</span></span>
11. <span data-ttu-id="61720-140">Переключите развертывание раздела "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="61720-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="61720-141">Откройте вкладку "Пакеты продуктов".</span><span class="sxs-lookup"><span data-stu-id="61720-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="61720-142">Щелкните "Строка заказа на покупку".</span><span class="sxs-lookup"><span data-stu-id="61720-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="61720-143">Щелкните "Создать строки из пакета".</span><span class="sxs-lookup"><span data-stu-id="61720-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="61720-144">В списке найдите и выберите пакет продуктов, созданный в предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="61720-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="61720-145">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="61720-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="61720-146">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="61720-146">Click Create.</span></span>
18. <span data-ttu-id="61720-147">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="61720-147">Click Save.</span></span>


