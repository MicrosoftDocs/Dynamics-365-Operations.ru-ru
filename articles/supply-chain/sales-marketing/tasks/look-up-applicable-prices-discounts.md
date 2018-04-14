--- 
title: "Поиск применимых цен и скидок"
description: "В этой процедуре показано, как найти цену и/или скидку по продукту, которая в настоящее время действует для определенного клиента, без создания заказа на продажу."
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
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c90de64ccc61a6515298c55dacaec44b79b19a3b
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="e4658-103">Поиск применимых цен и скидок</span><span class="sxs-lookup"><span data-stu-id="e4658-103">Look up applicable prices and discounts</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4658-104">В этой процедуре показано, как найти цену и/или скидку по продукту, которая в настоящее время действует для определенного клиента, без создания заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="e4658-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="e4658-105">Процедура представляет собой конкретный например, и выполнять его необходимо с использованием демонстрационной компании USMF, чтобы выбирать необходимые значения.</span><span class="sxs-lookup"><span data-stu-id="e4658-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="e4658-106">Поиск применимой цены</span><span class="sxs-lookup"><span data-stu-id="e4658-106">Find the applicable price</span></span>
1. <span data-ttu-id="e4658-107">Перейдите в раздел "Продажи и маркетинг" > "Цены и скидки" > "Поиск цен".</span><span class="sxs-lookup"><span data-stu-id="e4658-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="e4658-108">В поле "Счет клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e4658-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e4658-109">В списке найдите и выберите клиента US-001.</span><span class="sxs-lookup"><span data-stu-id="e4658-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="e4658-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="e4658-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e4658-111">В поле "Код номенклатуры" введите "T0004".</span><span class="sxs-lookup"><span data-stu-id="e4658-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="e4658-112">По умолчанию в поле "Количество" установлено значение 1.</span><span class="sxs-lookup"><span data-stu-id="e4658-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="e4658-113">Однако если вы знаете объем заказа, который клиент намеревается разместить на данный продукт, введите вместо него это количество.</span><span class="sxs-lookup"><span data-stu-id="e4658-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="e4658-114">Эта информация используется, если в коммерческих соглашениях с клиентом предусмотрены количественные диапазоны, т. е. если цена продукта зависит от минимального приобретаемого количества.</span><span class="sxs-lookup"><span data-stu-id="e4658-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="e4658-115">В поле "Дата" введите дату, когда клиент рассчитывает разместить заказ.</span><span class="sxs-lookup"><span data-stu-id="e4658-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="e4658-116">Дата может быть сегодняшней датой или любой датой в будущем.</span><span class="sxs-lookup"><span data-stu-id="e4658-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="e4658-117">Система возвращает цену, действительную для выбранного продукта при покупке выбранным клиентом на выбранную дату в указанном количестве.</span><span class="sxs-lookup"><span data-stu-id="e4658-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="e4658-118">В этом примере, если бы клиент US-001 купил 1 единицу продукта T0004 сегодня, ему пришлось бы заплатить 350 канадских долларов за единицу.</span><span class="sxs-lookup"><span data-stu-id="e4658-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="e4658-119">Эта цена берется из существующего и активного коммерческого соглашения с клиентом.</span><span class="sxs-lookup"><span data-stu-id="e4658-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="e4658-120">Другие поля на странице содержат более подробные сведения о цене и себестоимости продукта (если она настроена в шаблоне продукта), а также рассчитанную рентабельность.</span><span class="sxs-lookup"><span data-stu-id="e4658-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="e4658-121">Если установлен флажок "Показать связанные варианты продукта", это означает, что для вариантов продукта существуют дополнительные коммерческие соглашения.</span><span class="sxs-lookup"><span data-stu-id="e4658-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="e4658-122">Установите флажок "Показать связанные варианты продукта".</span><span class="sxs-lookup"><span data-stu-id="e4658-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="e4658-123">Отображается список вариантов продукта с информацией об их аналитиках.</span><span class="sxs-lookup"><span data-stu-id="e4658-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="e4658-124">В списке пометьте строку, представляющий цвет "Белый".</span><span class="sxs-lookup"><span data-stu-id="e4658-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="e4658-125">Обратите внимание, что цена продукта теперь отличается от той, которая отображалась раньше, когда цена не была указана по аналитикам.</span><span class="sxs-lookup"><span data-stu-id="e4658-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="e4658-126">Щелкните "Просмотр цен продажи".</span><span class="sxs-lookup"><span data-stu-id="e4658-126">Click View sales prices.</span></span>
    * <span data-ttu-id="e4658-127">На странице "Цена (продажи)" отображаются все коммерческие соглашения, применимые к продукту, включая его варианты.</span><span class="sxs-lookup"><span data-stu-id="e4658-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="e4658-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e4658-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="e4658-129">Поиск применимой скидки</span><span class="sxs-lookup"><span data-stu-id="e4658-129">Find the applicable discount</span></span>
    * <span data-ttu-id="e4658-130">Убедитесь, что поле "Счет клиента" содержит код клиента US-001 </span><span class="sxs-lookup"><span data-stu-id="e4658-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="e4658-131">В поле "Код номенклатуры" введите "T0012".</span><span class="sxs-lookup"><span data-stu-id="e4658-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="e4658-132">Убедитесь, что в поле "Количество" задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="e4658-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="e4658-133">Следующие сведения ценообразования, показанные для продукта T0012, берутся из одного или нескольких коммерческих соглашений: цена за единицу составляет 1000 канадскихдолларов, а процент скидки составляет 5.</span><span class="sxs-lookup"><span data-stu-id="e4658-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="e4658-134">В поле "Количество" укажите "20".</span><span class="sxs-lookup"><span data-stu-id="e4658-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="e4658-135">При увеличении количества в заказе скидка по строке, которая будет предложена клиенту, меняется с 5 на 7 процентов.</span><span class="sxs-lookup"><span data-stu-id="e4658-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="e4658-136">Чистая сумма рассчитывается на основе цены за единицу, скидки и общего количества.</span><span class="sxs-lookup"><span data-stu-id="e4658-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="e4658-137">Щелкните "Просмотр скидки по строке".</span><span class="sxs-lookup"><span data-stu-id="e4658-137">Click View line discount.</span></span>
    * <span data-ttu-id="e4658-138">Для продукта T0012 существует для соглашения по скидке по сроке, согласно которым при количестве по строке заказа от 1 до 10 скидка составляет 5 процентов, а при количестве свыше 10 — 7 процентов.</span><span class="sxs-lookup"><span data-stu-id="e4658-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="e4658-139">Обратите внимание, что скидки применяются к группе продуктов, в данном примере с кодом группы 01, в которую входит продукт T0012.</span><span class="sxs-lookup"><span data-stu-id="e4658-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="e4658-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e4658-140">Close the page.</span></span>


