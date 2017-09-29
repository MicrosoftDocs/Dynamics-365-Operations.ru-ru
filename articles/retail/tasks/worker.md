--- 
title: "Настройка работника"
description: "Эта процедура демонстрирует порядок настройки работника розничной торговли в качестве торгового представителя, который имеет право на комиссионные по продажам в POS."
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 09c5d263f3ad0bade6b7dd8f099dd3f62a1ddf5d
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="configure-a-worker"></a><span data-ttu-id="31e31-103">Настройка работника</span><span class="sxs-lookup"><span data-stu-id="31e31-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="31e31-104">Эта процедура демонстрирует порядок настройки работника розничной торговли в качестве торгового представителя, который имеет право на комиссионные по продажам в POS.</span><span class="sxs-lookup"><span data-stu-id="31e31-104">This procedure demonstrates how to configure a retail worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="31e31-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="31e31-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="31e31-106">Создание группы комиссий по продажам для работника</span><span class="sxs-lookup"><span data-stu-id="31e31-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="31e31-107">Перейдите в раздел "Продажи и маркетинг" > "Комиссии" > "Группы продаж".</span><span class="sxs-lookup"><span data-stu-id="31e31-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="31e31-108">Работники и могут быть назначены в одну или несколько групп продаж.</span><span class="sxs-lookup"><span data-stu-id="31e31-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="31e31-109">В POS можно выбрать любую группу продаж, содержащую работников из адресной книги магазина.</span><span class="sxs-lookup"><span data-stu-id="31e31-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="31e31-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="31e31-110">Click New.</span></span>
3. <span data-ttu-id="31e31-111">В поле "Группа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="31e31-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="31e31-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="31e31-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="31e31-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="31e31-113">Click Save.</span></span>
6. <span data-ttu-id="31e31-114">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="31e31-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="31e31-115">Щелкните "Торг. представитель".</span><span class="sxs-lookup"><span data-stu-id="31e31-115">Click Sales rep.</span></span>
    * <span data-ttu-id="31e31-116">Группа продаж может содержать несколько работников.</span><span class="sxs-lookup"><span data-stu-id="31e31-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="31e31-117">Комиссии можно разделить между работниками на основе того, как определена доля в комиссии.</span><span class="sxs-lookup"><span data-stu-id="31e31-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="31e31-118">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="31e31-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="31e31-119">В поле "Распределение комиссии" введите число.</span><span class="sxs-lookup"><span data-stu-id="31e31-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="31e31-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="31e31-120">Click Save.</span></span>
11. <span data-ttu-id="31e31-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="31e31-121">Close the page.</span></span>
12. <span data-ttu-id="31e31-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="31e31-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="31e31-123">Назначение группы продаж по умолчанию для работников</span><span class="sxs-lookup"><span data-stu-id="31e31-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="31e31-124">Перейдите в раздел "Розничная торговля и коммерция" > "Сотрудники" > "Работники".</span><span class="sxs-lookup"><span data-stu-id="31e31-124">Go to Retail and commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="31e31-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="31e31-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="31e31-126">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="31e31-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="31e31-127">Перейдите на вкладку Розница.</span><span class="sxs-lookup"><span data-stu-id="31e31-127">Click the Retail tab.</span></span>
    * <span data-ttu-id="31e31-128">Работник может быть назначен группе продаж по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="31e31-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="31e31-129">Группа продаж по умолчанию будет автоматически добавлена в строки продаж в POS, если этот параметр включен в профиле функции для магазина.</span><span class="sxs-lookup"><span data-stu-id="31e31-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="31e31-130">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="31e31-130">Click Edit.</span></span>
6. <span data-ttu-id="31e31-131">В поле "Группа по умолчанию" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="31e31-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="31e31-132">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="31e31-132">Click Save.</span></span>


