--- 
title: "Ввод договоров продажи"
description: "В этой процедуре показано, как создать договор продажи, который обязывает одного из ваших клиентов закупить продукцию на согласованную суммы в течение определенно времени в обмен на специальные скидки."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8c11164f7edb8e05b93f3c58b9707c0bf2482228
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="098d3-103">Ввод договоров продажи</span><span class="sxs-lookup"><span data-stu-id="098d3-103">Enter sales agreements</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="098d3-104">В этой процедуре показано, как создать договор продажи, который обязывает одного из ваших клиентов закупить продукцию на</span><span class="sxs-lookup"><span data-stu-id="098d3-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an</span></span>

<span data-ttu-id="098d3-105">согласованную сумму в течение определенного времени в обмен на специальные скидки.</span><span class="sxs-lookup"><span data-stu-id="098d3-105">agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="098d3-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="098d3-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="098d3-107">Настройка заголовка договора продажи</span><span class="sxs-lookup"><span data-stu-id="098d3-107">Set up sales agreement header</span></span>
1. <span data-ttu-id="098d3-108">Перейдите в раздел "Продажи и маркетинг" > "Договоры продажи" > "Договоры продажи".</span><span class="sxs-lookup"><span data-stu-id="098d3-108">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="098d3-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="098d3-109">Click New.</span></span>
3. <span data-ttu-id="098d3-110">В поле "Счет клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="098d3-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="098d3-111">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="098d3-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="098d3-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="098d3-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="098d3-113">В поле "Классификация договоров продажи" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="098d3-113">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="098d3-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="098d3-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="098d3-115">Разверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="098d3-115">Expand the General section.</span></span>
9. <span data-ttu-id="098d3-116">В поле "Обязательство по умолчанию" выберите "Обязательство по стоимости продукта".</span><span class="sxs-lookup"><span data-stu-id="098d3-116">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="098d3-117">Тип обязательства является обязательным критерием, который необходимо назначить договору, чтобы определить, как будет выполняться договор.</span><span class="sxs-lookup"><span data-stu-id="098d3-117">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="098d3-118">Четыре предварительно определенных типа позволяют настраивать цель обязательства клиента, выраженную через количество или стоимость.</span><span class="sxs-lookup"><span data-stu-id="098d3-118">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="098d3-119">Тип обязательства количества может применяться только к конкретному продукту, а типы основе стоимости могут применяться к продажам как специфичных, так и неспецифичных продуктов.</span><span class="sxs-lookup"><span data-stu-id="098d3-119">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="098d3-120">В поле "Дата окончания" установите дату в будущем, когда должен истечь срок действия договора.</span><span class="sxs-lookup"><span data-stu-id="098d3-120">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="098d3-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="098d3-121">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="098d3-122">Настройка строк обязательства по стоимости продукта</span><span class="sxs-lookup"><span data-stu-id="098d3-122">Set up product value commitment lines</span></span>
1. <span data-ttu-id="098d3-123">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="098d3-123">Click Add line.</span></span>
2. <span data-ttu-id="098d3-124">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="098d3-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="098d3-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="098d3-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="098d3-126">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="098d3-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="098d3-127">Тип обязательства, выбранного для договора, влияет на тип информации, которую можно вносить в строки договора.</span><span class="sxs-lookup"><span data-stu-id="098d3-127">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="098d3-128">Например, для основанного на стоимости договора необходимо определить общую чистой суммы (в согласованной валюте), на которую клиент обязан приобрести у вас товары.</span><span class="sxs-lookup"><span data-stu-id="098d3-128">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="098d3-129">В этом примере поля количества и единицы в строке недоступны, поскольку вы создаете договор на покупку клиентом продукции на определенную сумму.</span><span class="sxs-lookup"><span data-stu-id="098d3-129">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="098d3-130">В поле "Чистая сумма" введите денежную сумму, на которую должен совершить покупки клиент.</span><span class="sxs-lookup"><span data-stu-id="098d3-130">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="098d3-131">В поле "Процент скидки" введите значение в процентах, которое будет применяться к строкам заказа на продажу, которые связаны с данным договором.</span><span class="sxs-lookup"><span data-stu-id="098d3-131">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="098d3-132">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="098d3-132">Expand the Line details section.</span></span>
8. <span data-ttu-id="098d3-133">В поле "Используется максимум" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="098d3-133">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="098d3-134">Параметр "Используется максимум" означает, что общая сумма всех строк заказа на продажу, которые используют специальные цены, скидки или особые условия по обязательству, не должна превышать сумму, указанную в обязательстве.</span><span class="sxs-lookup"><span data-stu-id="098d3-134">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="098d3-135">Минимальные и максимальные суммы выпуска определяют диапазон сумм, на которые нужно продать в рамках каждого заказа на продажу для договора.</span><span class="sxs-lookup"><span data-stu-id="098d3-135">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="098d3-136">Разверните раздел "Заголовок договора продажи".</span><span class="sxs-lookup"><span data-stu-id="098d3-136">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="098d3-137">Если договор не имеет состояния "Действует", заказы на продажу невозможно сопоставить с договором и поэтому таки заказы не могут вносить вклад в выполнение этого соглашения.</span><span class="sxs-lookup"><span data-stu-id="098d3-137">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="098d3-138">На этом этапе вы можете вручную изменить состояние.</span><span class="sxs-lookup"><span data-stu-id="098d3-138">You can change the status manually at this stage.</span></span> <span data-ttu-id="098d3-139">Однако состояние обычно изменяется при подтверждении договора для клиента.</span><span class="sxs-lookup"><span data-stu-id="098d3-139">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="098d3-140">В области действий щелкните "Договор продажи".</span><span class="sxs-lookup"><span data-stu-id="098d3-140">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="098d3-141">Щелкните "Подтверждение".</span><span class="sxs-lookup"><span data-stu-id="098d3-141">Click Confirmation.</span></span>
    * <span data-ttu-id="098d3-142">Убедитесь, что параметр "Пометить договор как действующий" имеет значение "Да".</span><span class="sxs-lookup"><span data-stu-id="098d3-142">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="098d3-143">В поле "Печать отчета" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="098d3-143">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="098d3-144">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="098d3-144">Click OK.</span></span>
14. <span data-ttu-id="098d3-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="098d3-145">Close the page.</span></span>
    * <span data-ttu-id="098d3-146">Теперь договор действует и вы можете связывать заказы клиента с этим договором для достижения установленной цели.</span><span class="sxs-lookup"><span data-stu-id="098d3-146">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


