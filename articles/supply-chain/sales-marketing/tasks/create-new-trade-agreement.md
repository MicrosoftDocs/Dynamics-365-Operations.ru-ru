--- 
title: "Создание нового коммерческого соглашения"
description: "В этой процедуре показано, как создать коммерческом соглашение для регистрации новой цены продажи продукта, согласованной с конкретным клиентом."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1eb7a945243387f85ec5f38cc3b969d8d030ff25
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="9eb63-103">Создание нового коммерческого соглашения</span><span class="sxs-lookup"><span data-stu-id="9eb63-103">Create a new trade agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9eb63-104">В этой процедуре показано, как создать коммерческом соглашение для регистрации новой цены продажи продукта, согласованной с конкретным клиентом.</span><span class="sxs-lookup"><span data-stu-id="9eb63-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="9eb63-105">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="9eb63-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="9eb63-106">При использовании собственных данных перед началом этого руководства убедитесь в наличии имени журнала коммерческих соглашений, у которого параметр "Связь по умолчанию" установлен в значение "Цена (продажа)".</span><span class="sxs-lookup"><span data-stu-id="9eb63-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="9eb63-107">Создание и разноска нового журнала коммерческих соглашений</span><span class="sxs-lookup"><span data-stu-id="9eb63-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="9eb63-108">Перейдите в раздел "Продажи и маркетинг" > "Цены и скидки" > "Журналы коммерческих соглашений".</span><span class="sxs-lookup"><span data-stu-id="9eb63-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="9eb63-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9eb63-109">Click New.</span></span>
3. <span data-ttu-id="9eb63-110">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9eb63-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9eb63-111">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="9eb63-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9eb63-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9eb63-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9eb63-113">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="9eb63-113">Click Lines.</span></span>
7. <span data-ttu-id="9eb63-114">В поле "Код счета" выберите "Таблица".</span><span class="sxs-lookup"><span data-stu-id="9eb63-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="9eb63-115">В этом примере вам необходимо обновить цену для конкретного клиенте, т. е. вы должны выбрать "Таблица".</span><span class="sxs-lookup"><span data-stu-id="9eb63-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="9eb63-116">Если бы вы обновляли цену продукта в прайс-листе, вы бы выбрали "Все", чтобы новая цена действовала для всех клиентов.</span><span class="sxs-lookup"><span data-stu-id="9eb63-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="9eb63-117">Если бы вы дифференцировали цен между разными клиентскими сегментами, вы бы выбрали "Группа".</span><span class="sxs-lookup"><span data-stu-id="9eb63-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="9eb63-118">Для выбора варианта "Группа" у вас должны быть настроены ценовые группы клиентов.</span><span class="sxs-lookup"><span data-stu-id="9eb63-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="9eb63-119">В поле "Выбор счета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9eb63-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="9eb63-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="9eb63-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9eb63-121">В поле "Код номенклатуры" выберите "Таблица".</span><span class="sxs-lookup"><span data-stu-id="9eb63-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="9eb63-122">При вводе коммерческого соглашения типа "Цена (продажи)" в поле "Код номенклатуры" необходимо выбирать только "Таблица".</span><span class="sxs-lookup"><span data-stu-id="9eb63-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="9eb63-123">Это связано с тем, что цена — абсолютная величина и не может быть одинаковой для всех продуктов или группы продуктов.</span><span class="sxs-lookup"><span data-stu-id="9eb63-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="9eb63-124">В поле "Связь номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9eb63-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="9eb63-125">Выберите в списке продукт, который требуется включить в соглашение.</span><span class="sxs-lookup"><span data-stu-id="9eb63-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="9eb63-126">Запомните, какой из продуктов вы выбрали.</span><span class="sxs-lookup"><span data-stu-id="9eb63-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="9eb63-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9eb63-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9eb63-128">В поле "От" введите минимальное количество.</span><span class="sxs-lookup"><span data-stu-id="9eb63-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="9eb63-129">Если клиент должен заказать какое-либо минимальное количество, прежде чем он получит право на новую цену, необходимо указать здесь это количество.</span><span class="sxs-lookup"><span data-stu-id="9eb63-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="9eb63-130">Введите значение в поле "До", чтобы указать максимальное количество, после которого цена в соглашении будет недействительна.</span><span class="sxs-lookup"><span data-stu-id="9eb63-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="9eb63-131">Если вы предлагаете цены и скидки исходя из нескольких количественных диапазонов, укажите каждый диапазон в виде пары минимальное-максимальное значение в полях "От" и "До" соответственно.</span><span class="sxs-lookup"><span data-stu-id="9eb63-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="9eb63-132">В поле "Сумма в валюте" введите цену.</span><span class="sxs-lookup"><span data-stu-id="9eb63-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="9eb63-133">В поле "Начальная дата" введите дату, с которой начинает действовать соглашение.</span><span class="sxs-lookup"><span data-stu-id="9eb63-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="9eb63-134">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9eb63-134">Click Save.</span></span>
18. <span data-ttu-id="9eb63-135">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="9eb63-135">Click Validate.</span></span>
19. <span data-ttu-id="9eb63-136">Щелкните "Проверить выбранные строки".</span><span class="sxs-lookup"><span data-stu-id="9eb63-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="9eb63-137">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9eb63-137">Click OK.</span></span>
21. <span data-ttu-id="9eb63-138">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="9eb63-138">Click Post.</span></span>
22. <span data-ttu-id="9eb63-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9eb63-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="9eb63-140">Просмотр коммерческих соглашений по продукту</span><span class="sxs-lookup"><span data-stu-id="9eb63-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="9eb63-141">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="9eb63-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="9eb63-142">Найдите в списке и выберите продукт, цену которого вы только что обновили.</span><span class="sxs-lookup"><span data-stu-id="9eb63-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="9eb63-143">В области действий щелкните "Продажа".</span><span class="sxs-lookup"><span data-stu-id="9eb63-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="9eb63-144">Щелкните "Просмотр коммерческих соглашений".</span><span class="sxs-lookup"><span data-stu-id="9eb63-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="9eb63-145">Просмотрите сведения о только что созданном коммерческом соглашении по ценам.</span><span class="sxs-lookup"><span data-stu-id="9eb63-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="9eb63-146">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9eb63-146">Close the page.</span></span>


