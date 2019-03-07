---
title: Создание штрих-кода для продукта
description: В этой процедуре описан порядок создания вручную штрих-кода с использованием кода номенклатуры M0001 в качестве примера.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, InventItemBarcode, InventItemBarcodeLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ae2765a125045d60566267d01e380069d5d527c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "329398"
---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="bacc2-103">Создание штрих-кода для продукта</span><span class="sxs-lookup"><span data-stu-id="bacc2-103">Create a bar code for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bacc2-104">В этой процедуре описан порядок создания вручную штрих-кода с использованием кода номенклатуры M0001 в качестве примера.</span><span class="sxs-lookup"><span data-stu-id="bacc2-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="bacc2-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="bacc2-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="bacc2-106">Щелкните "Обслуживание выпущенного продукта".</span><span class="sxs-lookup"><span data-stu-id="bacc2-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="bacc2-107">Щелкните "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="bacc2-107">Click Released products.</span></span>
3. <span data-ttu-id="bacc2-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="bacc2-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="bacc2-109">В области действий щелкните "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="bacc2-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="bacc2-110">Щелкните "Штрих-коды".</span><span class="sxs-lookup"><span data-stu-id="bacc2-110">Click Bar codes.</span></span>
6. <span data-ttu-id="bacc2-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bacc2-111">Click New.</span></span>
7. <span data-ttu-id="bacc2-112">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bacc2-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="bacc2-113">В поле "Настройка штрих-кода" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bacc2-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="bacc2-114">В поле "Штрих-код" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bacc2-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="bacc2-115">В поле "Штрих-код" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bacc2-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="bacc2-116">Нажмите клавишу TAB.</span><span class="sxs-lookup"><span data-stu-id="bacc2-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="bacc2-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bacc2-117">Close the page.</span></span>
12. <span data-ttu-id="bacc2-118">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="bacc2-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="bacc2-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bacc2-119">Click Save.</span></span>
    * <span data-ttu-id="bacc2-120">Когда вы нажмете "Сохранить", выполняется штрих-код, и в этом случае отображается ошибка, что ожидалась контрольная цифра 8, а найдена цифра 3.</span><span class="sxs-lookup"><span data-stu-id="bacc2-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="bacc2-121">Вручную обновите номер штрих-кода, чтобы он заканчивался цифрой 8.</span><span class="sxs-lookup"><span data-stu-id="bacc2-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="bacc2-122">В поле "Штрих-код" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bacc2-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="bacc2-123">В поле "Штрих-код" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bacc2-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="bacc2-124">Нажмите клавишу TAB.</span><span class="sxs-lookup"><span data-stu-id="bacc2-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="bacc2-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bacc2-125">Close the page.</span></span>
17. <span data-ttu-id="bacc2-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bacc2-126">Click Save.</span></span>
18. <span data-ttu-id="bacc2-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bacc2-127">Close the page.</span></span>

