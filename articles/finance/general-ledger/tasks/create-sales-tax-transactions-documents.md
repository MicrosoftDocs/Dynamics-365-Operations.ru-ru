---
title: Создание налоговых проводок по документам
description: Налог в документах рассчитывается путем указания налоговой группы и налоговой группы номенклатур в строках документа.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 061949dedde763c188e13c07cec750895cbef175
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836993"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="dd25d-103">Создание налоговых проводок по документам</span><span class="sxs-lookup"><span data-stu-id="dd25d-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd25d-104">Налог в документах рассчитывается путем указания налоговой группы и налоговой группы номенклатур в строках документа.</span><span class="sxs-lookup"><span data-stu-id="dd25d-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="dd25d-105">Эти значения берутся по умолчанию из справочника, но их можно изменить вручную при необходимости.</span><span class="sxs-lookup"><span data-stu-id="dd25d-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="dd25d-106">Рассчитанный налог можно проверить на уровне строки и документа.</span><span class="sxs-lookup"><span data-stu-id="dd25d-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="dd25d-107">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="dd25d-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="dd25d-108">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="dd25d-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="dd25d-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="dd25d-109">Click New.</span></span>
3. <span data-ttu-id="dd25d-110">В поле "Счет клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="dd25d-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="dd25d-111">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="dd25d-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="dd25d-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="dd25d-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="dd25d-113">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="dd25d-113">Click OK.</span></span>
7. <span data-ttu-id="dd25d-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="dd25d-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="dd25d-115">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="dd25d-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="dd25d-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="dd25d-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="dd25d-117">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="dd25d-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="dd25d-118">Разверните или сверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="dd25d-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="dd25d-119">Перейдите на вкладку Настройка.</span><span class="sxs-lookup"><span data-stu-id="dd25d-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="dd25d-120">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="dd25d-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="dd25d-121">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="dd25d-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="dd25d-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="dd25d-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="dd25d-123">Щелкните "Статистика".</span><span class="sxs-lookup"><span data-stu-id="dd25d-123">Click Financials.</span></span>
17. <span data-ttu-id="dd25d-124">Щелкните "Налог".</span><span class="sxs-lookup"><span data-stu-id="dd25d-124">Click Sales tax.</span></span>
18. <span data-ttu-id="dd25d-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="dd25d-125">Click OK.</span></span>
19. <span data-ttu-id="dd25d-126">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="dd25d-126">Click Add line.</span></span>
20. <span data-ttu-id="dd25d-127">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="dd25d-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="dd25d-128">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="dd25d-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="dd25d-129">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="dd25d-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="dd25d-130">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="dd25d-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="dd25d-131">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="dd25d-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="dd25d-132">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="dd25d-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="dd25d-133">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="dd25d-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="dd25d-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="dd25d-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="dd25d-135">В области действий щелкните "Продажа".</span><span class="sxs-lookup"><span data-stu-id="dd25d-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="dd25d-136">Щелкните "Налог".</span><span class="sxs-lookup"><span data-stu-id="dd25d-136">Click Sales tax.</span></span>
30. <span data-ttu-id="dd25d-137">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="dd25d-137">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]