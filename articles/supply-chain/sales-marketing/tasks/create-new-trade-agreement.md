---
title: Создание нового коммерческого соглашения
description: В этой процедуре показано, как создать коммерческом соглашение для регистрации новой цены продажи продукта, согласованной с конкретным клиентом.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9aa46f959c35c209791457aa697ab829264b3275
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211959"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="c5f59-103">Создание нового коммерческого соглашения</span><span class="sxs-lookup"><span data-stu-id="c5f59-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5f59-104">В этой процедуре показано, как создать коммерческом соглашение для регистрации новой цены продажи продукта, согласованной с конкретным клиентом.</span><span class="sxs-lookup"><span data-stu-id="c5f59-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="c5f59-105">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="c5f59-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c5f59-106">При использовании собственных данных перед началом этого руководства убедитесь в наличии имени журнала коммерческих соглашений, у которого параметр "Связь по умолчанию" установлен в значение "Цена (продажа)".</span><span class="sxs-lookup"><span data-stu-id="c5f59-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="c5f59-107">Создание и разноска нового журнала коммерческих соглашений</span><span class="sxs-lookup"><span data-stu-id="c5f59-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="c5f59-108">Перейдите в раздел **Область переходов > Модули > Продажи и маркетинг > Цены и скидки > Журналы коммерческих соглашений**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="c5f59-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-109">Click **New**.</span></span>
3. <span data-ttu-id="c5f59-110">В поле **Имя** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c5f59-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c5f59-111">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c5f59-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c5f59-112">В области **Панель операций** щелкните **Строки**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-112">On **Action pane**, click **Lines**.</span></span>
6. <span data-ttu-id="c5f59-113">В поле **Код счета** выберите "Таблица".</span><span class="sxs-lookup"><span data-stu-id="c5f59-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="c5f59-114">В этом примере вам необходимо обновить цену для конкретного клиенте, т. е. вы должны выбрать "Таблица".</span><span class="sxs-lookup"><span data-stu-id="c5f59-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="c5f59-115">Если бы вы обновляли цену продукта в прайс-листе, вы бы выбрали "Все", чтобы новая цена действовала для всех клиентов.</span><span class="sxs-lookup"><span data-stu-id="c5f59-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="c5f59-116">Если бы вы дифференцировали цен между разными клиентскими сегментами, вы бы выбрали "Группа".</span><span class="sxs-lookup"><span data-stu-id="c5f59-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="c5f59-117">Для выбора варианта "Группа" у вас должны быть настроены ценовые группы клиентов.</span><span class="sxs-lookup"><span data-stu-id="c5f59-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="c5f59-118">В поле **Выбор счета** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c5f59-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c5f59-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c5f59-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="c5f59-120">В поле **Код номенклатуры** выберите "Таблица".</span><span class="sxs-lookup"><span data-stu-id="c5f59-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="c5f59-121">При вводе коммерческого соглашения типа "Цена (продажи)" в поле **Код номенклатуры** необходимо выбирать только "Таблица".</span><span class="sxs-lookup"><span data-stu-id="c5f59-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="c5f59-122">Это связано с тем, что цена — абсолютная величина и не может быть одинаковой для всех продуктов или группы продуктов.</span><span class="sxs-lookup"><span data-stu-id="c5f59-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="c5f59-123">В поле **Связь номенклатуры** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c5f59-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="c5f59-124">Выберите в списке продукт, который требуется включить в соглашение.</span><span class="sxs-lookup"><span data-stu-id="c5f59-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="c5f59-125">Запомните, какой из продуктов вы выбрали.</span><span class="sxs-lookup"><span data-stu-id="c5f59-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="c5f59-126">В поле **От** введите минимальное количество.</span><span class="sxs-lookup"><span data-stu-id="c5f59-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="c5f59-127">Если клиент должен заказать какое-либо минимальное количество, прежде чем он получит право на новую цену, необходимо указать здесь это количество.</span><span class="sxs-lookup"><span data-stu-id="c5f59-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="c5f59-128">Введите значение в поле **До**, чтобы указать максимальное количество, после которого цена в соглашении будет недействительна.</span><span class="sxs-lookup"><span data-stu-id="c5f59-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="c5f59-129">Если вы предлагаете цены и скидки исходя из нескольких количественных диапазонов, укажите каждый диапазон в виде пары минимальное-максимальное значение в полях **От** и **До** соответственно.</span><span class="sxs-lookup"><span data-stu-id="c5f59-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="c5f59-130">В поле **Сумма в валюте** введите цену.</span><span class="sxs-lookup"><span data-stu-id="c5f59-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="c5f59-131">В разделе **Сведения** в поле **Начальная дата** введите дату, с которой начинает действовать соглашение.</span><span class="sxs-lookup"><span data-stu-id="c5f59-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="c5f59-132">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-132">Click **Save**.</span></span>
16. <span data-ttu-id="c5f59-133">Щелкните **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-133">Click **Validate**.</span></span>
17. <span data-ttu-id="c5f59-134">Щелкните **Проверить выбранные строки**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="c5f59-135">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-135">Click **OK**.</span></span>
19. <span data-ttu-id="c5f59-136">Щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-136">Click **Post**.</span></span>
20. <span data-ttu-id="c5f59-137">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="c5f59-138">Просмотр коммерческих соглашений по продукту</span><span class="sxs-lookup"><span data-stu-id="c5f59-138">View trade agreements for a product</span></span>
1. <span data-ttu-id="c5f59-139">Перейдите в раздел **Область переходов > Модули > Управление сведениями о продукте > Продукты > Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="c5f59-140">Найдите в списке и выберите продукт, цену которого вы только что обновили.</span><span class="sxs-lookup"><span data-stu-id="c5f59-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="c5f59-141">В области **Панель операций** щелкните **Продажа**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="c5f59-142">Щелкните **Просмотр коммерческих соглашений**.</span><span class="sxs-lookup"><span data-stu-id="c5f59-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="c5f59-143">Просмотрите сведения о только что созданном коммерческом соглашении по ценам.</span><span class="sxs-lookup"><span data-stu-id="c5f59-143">Review the details of the price trade agreement you have just created.</span></span>    

5. <span data-ttu-id="c5f59-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c5f59-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5f59-145">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c5f59-145">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="c5f59-146">Блоги сообщества</span><span class="sxs-lookup"><span data-stu-id="c5f59-146">Community blogs</span></span>
- [<span data-ttu-id="c5f59-147">Цены продажи в Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c5f59-147">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
