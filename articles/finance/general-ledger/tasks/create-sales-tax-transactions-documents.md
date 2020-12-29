---
title: Создание налоговых проводок по документам
description: Налог в документах рассчитывается путем указания налоговой группы и налоговой группы номенклатур в строках документа.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11e006e41f467a594521dfc601f46b4d1b492ce5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447286"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="c5296-103">Создание налоговых проводок по документам</span><span class="sxs-lookup"><span data-stu-id="c5296-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5296-104">Налог в документах рассчитывается путем указания налоговой группы и налоговой группы номенклатур в строках документа.</span><span class="sxs-lookup"><span data-stu-id="c5296-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="c5296-105">Эти значения берутся по умолчанию из справочника, но их можно изменить вручную при необходимости.</span><span class="sxs-lookup"><span data-stu-id="c5296-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="c5296-106">Рассчитанный налог можно проверить на уровне строки и документа.</span><span class="sxs-lookup"><span data-stu-id="c5296-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="c5296-107">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="c5296-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c5296-108">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="c5296-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c5296-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c5296-109">Click New.</span></span>
3. <span data-ttu-id="c5296-110">В поле "Счет клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c5296-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c5296-111">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c5296-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c5296-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c5296-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c5296-113">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="c5296-113">Click OK.</span></span>
7. <span data-ttu-id="c5296-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="c5296-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c5296-115">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c5296-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c5296-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c5296-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c5296-117">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="c5296-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="c5296-118">Разверните или сверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="c5296-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="c5296-119">Перейдите на вкладку Настройка.</span><span class="sxs-lookup"><span data-stu-id="c5296-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="c5296-120">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c5296-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="c5296-121">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="c5296-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="c5296-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c5296-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="c5296-123">Щелкните "Статистика".</span><span class="sxs-lookup"><span data-stu-id="c5296-123">Click Financials.</span></span>
17. <span data-ttu-id="c5296-124">Щелкните "Налог".</span><span class="sxs-lookup"><span data-stu-id="c5296-124">Click Sales tax.</span></span>
18. <span data-ttu-id="c5296-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c5296-125">Click OK.</span></span>
19. <span data-ttu-id="c5296-126">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="c5296-126">Click Add line.</span></span>
20. <span data-ttu-id="c5296-127">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="c5296-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="c5296-128">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c5296-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="c5296-129">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="c5296-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="c5296-130">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c5296-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="c5296-131">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="c5296-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="c5296-132">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c5296-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="c5296-133">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="c5296-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="c5296-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c5296-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="c5296-135">В области действий щелкните "Продажа".</span><span class="sxs-lookup"><span data-stu-id="c5296-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="c5296-136">Щелкните "Налог".</span><span class="sxs-lookup"><span data-stu-id="c5296-136">Click Sales tax.</span></span>
30. <span data-ttu-id="c5296-137">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c5296-137">Click OK.</span></span>

