---
title: Связывание индекса топлива с перевозчиком как дополнительного расхода
description: В этом руководстве демонстрируется создание назначения дополнения, дополнительных расходов перевозчика, справочника дополнений для доплаты за топливо, а также связывание индекс топлива перевозчика с перевозчиком.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae0aa90cfd673704bcd8e19f795499283ff01d44
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "349799"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="b1e43-103">Связывание индекса топлива с перевозчиком как дополнительного расхода</span><span class="sxs-lookup"><span data-stu-id="b1e43-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1e43-104">В этом руководстве демонстрируется создание назначения дополнения, дополнительных расходов перевозчика, справочника дополнений для доплаты за топливо, а также связывание индекс топлива перевозчика с перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="b1e43-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="b1e43-105">Перед выполнением этого руководства необходимо настроить индекс топлива перевозчика.</span><span class="sxs-lookup"><span data-stu-id="b1e43-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="b1e43-106">Для этого можно использовать руководство "Настройка индекса топлива перевозчика".</span><span class="sxs-lookup"><span data-stu-id="b1e43-106">You can use the “Set up a carrier fuel index” guide to do this.</span></span> <span data-ttu-id="b1e43-107">Обычно эти задачи по настройки выполняет менеджер по логистике.</span><span class="sxs-lookup"><span data-stu-id="b1e43-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="b1e43-108">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="b1e43-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="b1e43-109">Создание справочника дополнений</span><span class="sxs-lookup"><span data-stu-id="b1e43-109">Create an accessorial master</span></span>
1. <span data-ttu-id="b1e43-110">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Расчет ставок" > "Шаблоны дополнения".</span><span class="sxs-lookup"><span data-stu-id="b1e43-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="b1e43-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b1e43-111">Click New.</span></span>
3. <span data-ttu-id="b1e43-112">В поле "Шаблон дополнения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b1e43-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="b1e43-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b1e43-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b1e43-114">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b1e43-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="b1e43-115">Создание дополнительных накладных расходов перевозчика</span><span class="sxs-lookup"><span data-stu-id="b1e43-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="b1e43-116">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Расчет ставок" > "Дополнительные расходы перевозчика".</span><span class="sxs-lookup"><span data-stu-id="b1e43-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="b1e43-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b1e43-117">Click New.</span></span>
3. <span data-ttu-id="b1e43-118">В поле "Код дополнительного перевозчика" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b1e43-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="b1e43-119">В поле "Перевозчик, осуществляющий доставку " нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b1e43-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b1e43-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b1e43-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b1e43-121">В этом примере выберите автомобильного перевозчика.</span><span class="sxs-lookup"><span data-stu-id="b1e43-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="b1e43-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b1e43-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b1e43-123">В поле "Услуга перевозчика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b1e43-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b1e43-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b1e43-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b1e43-125">В поле "Шаблон дополнения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b1e43-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="b1e43-126">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b1e43-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b1e43-127">В этом примере выберите только что созданный справочник дополнений.</span><span class="sxs-lookup"><span data-stu-id="b1e43-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="b1e43-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b1e43-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="b1e43-129">Создание назначения дополнения</span><span class="sxs-lookup"><span data-stu-id="b1e43-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="b1e43-130">Щелкните "Дополнительные встречи".</span><span class="sxs-lookup"><span data-stu-id="b1e43-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="b1e43-131">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b1e43-131">Click New.</span></span>
3. <span data-ttu-id="b1e43-132">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b1e43-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b1e43-133">Переключите развертывание раздела "Критерии".</span><span class="sxs-lookup"><span data-stu-id="b1e43-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="b1e43-134">В критериях можно указать, всегда ли следует применять доплату за топливо — или, как в этом примере, указать, что она должна применяться только в пределах конкретного региона.</span><span class="sxs-lookup"><span data-stu-id="b1e43-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="b1e43-135">В поле "Почтовый индекс от" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b1e43-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="b1e43-136">В поле "Почтовый индекс до" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b1e43-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="b1e43-137">Переключите развертывание раздела "Расчет".</span><span class="sxs-lookup"><span data-stu-id="b1e43-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="b1e43-138">В разделе расчета можно указать способ расчета доплаты за топливо.</span><span class="sxs-lookup"><span data-stu-id="b1e43-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="b1e43-139">Этот расчет зависит от единицы дополнений, выбранной в качестве базы для расчета.</span><span class="sxs-lookup"><span data-stu-id="b1e43-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="b1e43-140">В поле "Тип дополнительного сбора" выберите "Доплата за топливо".</span><span class="sxs-lookup"><span data-stu-id="b1e43-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="b1e43-141">В поле "Единица дополнения" выберите "Пробег".</span><span class="sxs-lookup"><span data-stu-id="b1e43-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="b1e43-142">В поле "Регион" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b1e43-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b1e43-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b1e43-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b1e43-144">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b1e43-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="b1e43-145">Обновление профиля оценки перевозчика</span><span class="sxs-lookup"><span data-stu-id="b1e43-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="b1e43-146">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Перевозчики" > "Перевозчики".</span><span class="sxs-lookup"><span data-stu-id="b1e43-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="b1e43-147">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b1e43-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b1e43-148">Переключите развертывание раздела "Профили оценки".</span><span class="sxs-lookup"><span data-stu-id="b1e43-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="b1e43-149">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="b1e43-149">Click Edit.</span></span>
5. <span data-ttu-id="b1e43-150">В поле "Индекс топлива перевозчика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b1e43-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b1e43-151">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b1e43-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b1e43-152">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b1e43-152">Click Save.</span></span>

