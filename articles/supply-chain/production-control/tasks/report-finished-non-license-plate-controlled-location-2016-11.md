---
title: Приемка в местонахождении, не находящемся под управлением грузоместа (приложение, май 2016 г.)
description: В этом руководстве по задаче показан пример приемки отчетности в местонахождении, которое не управляется грузоместом.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdb24238bf8c0cfea0006aa0aa0217de9d3f1bc2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831946"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="04cb3-103">Приемка в местонахождении, не находящемся под управлением грузоместа (приложение, май 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="04cb3-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04cb3-104">В этом руководстве по задаче показан пример приемки отчетности в местонахождении, которое не управляется грузоместом.</span><span class="sxs-lookup"><span data-stu-id="04cb3-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="04cb3-105">Применимая политика работы является обязательным условием для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="04cb3-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="04cb3-106">В предыдущем руководстве по задаче показана настройка политики работы.</span><span class="sxs-lookup"><span data-stu-id="04cb3-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="04cb3-107">Для выполнения этого руководства по задаче требуется приложение Dynamics AX 7.0.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="04cb3-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="04cb3-108">Настройка местонахождения выхода</span><span class="sxs-lookup"><span data-stu-id="04cb3-108">Set up an output location</span></span>
1. <span data-ttu-id="04cb3-109">Перейдите в раздел "Управление организацией" > "Ресурсы" > "Группы ресурсов".</span><span class="sxs-lookup"><span data-stu-id="04cb3-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="04cb3-110">В списке выберите группу ресурсов "5102".</span><span class="sxs-lookup"><span data-stu-id="04cb3-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="04cb3-111">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="04cb3-111">Click Edit.</span></span>
4. <span data-ttu-id="04cb3-112">В поле "Склад выпуска" введите "51".</span><span class="sxs-lookup"><span data-stu-id="04cb3-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="04cb3-113">В поле "Местонахождение выхода" введите "001".</span><span class="sxs-lookup"><span data-stu-id="04cb3-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="04cb3-114">Местонахождение 001 не является местонахождением под управлением грузоместа.</span><span class="sxs-lookup"><span data-stu-id="04cb3-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="04cb3-115">Местонахождение выхода, которое не находится под управлением грузоместа, можно настроить, только если для местоположения существует соответствующая политика работы.</span><span class="sxs-lookup"><span data-stu-id="04cb3-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="04cb3-116">Создание производственного заказа и его приемка</span><span class="sxs-lookup"><span data-stu-id="04cb3-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="04cb3-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="04cb3-117">Close the page.</span></span>
2. <span data-ttu-id="04cb3-118">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="04cb3-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="04cb3-119">Щелкните "Новый производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="04cb3-119">Click New production order.</span></span>
4. <span data-ttu-id="04cb3-120">В поле "Код номенклатуры" введите "L0101".</span><span class="sxs-lookup"><span data-stu-id="04cb3-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="04cb3-121">Щелкните Создать.</span><span class="sxs-lookup"><span data-stu-id="04cb3-121">Click Create.</span></span>
6. <span data-ttu-id="04cb3-122">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="04cb3-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="04cb3-123">Щелкните "Оценка".</span><span class="sxs-lookup"><span data-stu-id="04cb3-123">Click Estimate.</span></span>
8. <span data-ttu-id="04cb3-124">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="04cb3-124">Click OK.</span></span>
9. <span data-ttu-id="04cb3-125">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="04cb3-125">Click Start.</span></span>
10. <span data-ttu-id="04cb3-126">Перейдите на вкладку Общие.</span><span class="sxs-lookup"><span data-stu-id="04cb3-126">Click the General tab.</span></span>
11. <span data-ttu-id="04cb3-127">В поле "Автопотребление по спецификации" выберите "Никогда".</span><span class="sxs-lookup"><span data-stu-id="04cb3-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="04cb3-128">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="04cb3-128">Click OK.</span></span>
13. <span data-ttu-id="04cb3-129">Щелкните Приемка.</span><span class="sxs-lookup"><span data-stu-id="04cb3-129">Click Report as finished.</span></span>
14. <span data-ttu-id="04cb3-130">Перейдите на вкладку Общие.</span><span class="sxs-lookup"><span data-stu-id="04cb3-130">Click the General tab.</span></span>
15. <span data-ttu-id="04cb3-131">Выберите значение "Да" в поле "Допускать ошибки".</span><span class="sxs-lookup"><span data-stu-id="04cb3-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="04cb3-132">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="04cb3-132">Click OK.</span></span>
17. <span data-ttu-id="04cb3-133">В области действий щелкните "Склад".</span><span class="sxs-lookup"><span data-stu-id="04cb3-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="04cb3-134">Щелкните "Сведения о работе".</span><span class="sxs-lookup"><span data-stu-id="04cb3-134">Click Work details.</span></span>
    * <span data-ttu-id="04cb3-135">При учете производственного заказа не была создана работа размещения.</span><span class="sxs-lookup"><span data-stu-id="04cb3-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="04cb3-136">Это происходит, потому что определена политика работы, которая предотвращает создание работы при приемке продукта L0101 в местоположении 001.</span><span class="sxs-lookup"><span data-stu-id="04cb3-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]