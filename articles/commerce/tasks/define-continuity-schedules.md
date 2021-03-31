---
title: Определение планов непрерывности
description: В этом разделе выполняется пошаговая настройка программы непрерывности (также называемой повторяющимися заказами).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f385d97ce8c458ada944609e165ebd0db500b546
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229944"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="333c7-103">Определение планов непрерывности</span><span class="sxs-lookup"><span data-stu-id="333c7-103">Define continuity schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="333c7-104">В этом разделе выполняется пошаговая настройка программы непрерывности (также называемой повторяющимися заказами).</span><span class="sxs-lookup"><span data-stu-id="333c7-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="333c7-105">В этом разделе в демонстрационных данных используется компания USRT.</span><span class="sxs-lookup"><span data-stu-id="333c7-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="333c7-106">Создание программы непрерывности</span><span class="sxs-lookup"><span data-stu-id="333c7-106">Create continuity program</span></span>
1. <span data-ttu-id="333c7-107">Перейдите в раздел "Retail и Commerce" > "Непрерывность" > "Программы непрерывности".</span><span class="sxs-lookup"><span data-stu-id="333c7-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="333c7-108">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="333c7-108">Click New.</span></span>
3. <span data-ttu-id="333c7-109">В поле "Код плана" введите код плана непрерывности.</span><span class="sxs-lookup"><span data-stu-id="333c7-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="333c7-110">В поле "Начало заказа" выберите "Первое событие".</span><span class="sxs-lookup"><span data-stu-id="333c7-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="333c7-111">Если клиент размещает новый заказ для программы непрерывности, имеются два варианта, для которых продукт будет отгружен: 1.</span><span class="sxs-lookup"><span data-stu-id="333c7-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="333c7-112">Первое событие: будет отгружен первый продукт в программе непрерывности.</span><span class="sxs-lookup"><span data-stu-id="333c7-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="333c7-113">2.</span><span class="sxs-lookup"><span data-stu-id="333c7-113">2.</span></span> <span data-ttu-id="333c7-114">Текущее событие: текущий продукт будет отгружен.</span><span class="sxs-lookup"><span data-stu-id="333c7-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="333c7-115">Например,</span><span class="sxs-lookup"><span data-stu-id="333c7-115">For example.</span></span> <span data-ttu-id="333c7-116">в третий месяц программы клиент получит третий в программе.</span><span class="sxs-lookup"><span data-stu-id="333c7-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="333c7-117">Выберите "Да" для запроса даты начала заказа.</span><span class="sxs-lookup"><span data-stu-id="333c7-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="333c7-118">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="333c7-118">Click Add line.</span></span>
7. <span data-ttu-id="333c7-119">В поле "Код номенклатуры" введите код номенклатуры для первого продукта ("0013").</span><span class="sxs-lookup"><span data-stu-id="333c7-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="333c7-120">Введите "CP".</span><span class="sxs-lookup"><span data-stu-id="333c7-120">Type 'CP'.</span></span>
9. <span data-ttu-id="333c7-121">Введите дату, когда первый продукт будет доступен для заказа.</span><span class="sxs-lookup"><span data-stu-id="333c7-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="333c7-122">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="333c7-122">Click Add line.</span></span>
11. <span data-ttu-id="333c7-123">В поле "Код номенклатуры" введите "0014".</span><span class="sxs-lookup"><span data-stu-id="333c7-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="333c7-124">В поле "Код интервала дат" очистите значение, чтобы это поле осталось пустым.</span><span class="sxs-lookup"><span data-stu-id="333c7-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="333c7-125">Для этой процедуры очистите интервал дат.</span><span class="sxs-lookup"><span data-stu-id="333c7-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="333c7-126">Вы установите дату как последовательно увеличивающуюся с начальной даты для первой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="333c7-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="333c7-127">Здесь введите интервал, с которым отгружаются продукты.</span><span class="sxs-lookup"><span data-stu-id="333c7-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="333c7-128">Введите "30".</span><span class="sxs-lookup"><span data-stu-id="333c7-128">Type '30'.</span></span>
    * <span data-ttu-id="333c7-129">Для ежемесячной программы следует ввести интервал 30 дней.</span><span class="sxs-lookup"><span data-stu-id="333c7-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="333c7-130">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="333c7-130">Click Add line.</span></span>
15. <span data-ttu-id="333c7-131">В поле "Код номенклатуры" введите "0015".</span><span class="sxs-lookup"><span data-stu-id="333c7-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="333c7-132">Введите "Завершить".</span><span class="sxs-lookup"><span data-stu-id="333c7-132">Type 'End'.</span></span>
17. <span data-ttu-id="333c7-133">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="333c7-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="333c7-134">Назначение номенклатуры непрерывности</span><span class="sxs-lookup"><span data-stu-id="333c7-134">Assign to continuity item</span></span>
1. <span data-ttu-id="333c7-135">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="333c7-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="333c7-136">Выберите номенклатуру "0016".</span><span class="sxs-lookup"><span data-stu-id="333c7-136">Select item '0016'.</span></span>
    * <span data-ttu-id="333c7-137">В этой процедуре вы выберите номер номенклатуры 0016.</span><span class="sxs-lookup"><span data-stu-id="333c7-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="333c7-138">Обычно у вас будет созданный выпущенный продукт, к которому будет применена дополнительная бизнес-логика непрерывности, когда он помещается в заказ на продажу в центре обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="333c7-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="333c7-139">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="333c7-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="333c7-140">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="333c7-140">Click Edit.</span></span>
5. <span data-ttu-id="333c7-141">Разверните или сверните раздел "Продажа".</span><span class="sxs-lookup"><span data-stu-id="333c7-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="333c7-142">Здесь введите программу непрерывности, которую эта номенклатура представляет.</span><span class="sxs-lookup"><span data-stu-id="333c7-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="333c7-143">Введите "Код плана", созданной ранее.</span><span class="sxs-lookup"><span data-stu-id="333c7-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="333c7-144">Если эта номенклатура продается в центре обработки вызовов, дополнительная бизнес-логику применяется из выбранной программы непрерывности.</span><span class="sxs-lookup"><span data-stu-id="333c7-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="333c7-145">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="333c7-145">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]