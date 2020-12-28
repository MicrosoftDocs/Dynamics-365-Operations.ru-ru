---
title: Создание заказа на выпуск покупки из договора покупки
description: В этой процедуре показано, как использовать договор покупки при создании заказа на покупку.
author: mkirknel
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee0c40dfc3c820343c7054238cc2da47e8203d59
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435979"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="9639a-103">Создание заказа на выпуск покупки из договора покупки</span><span class="sxs-lookup"><span data-stu-id="9639a-103">Create a purchase release order from a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9639a-104">В этой процедуре показано, как использовать договор покупки при создании заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="9639a-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="9639a-105">При создании заказа на покупку необходимо применить к нему договор покупки, поскольку в нем содержатся общие условия, которые следует скопировать в заголовок заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="9639a-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="9639a-106">Обычно эту задачу выполняет специалист по закупке.</span><span class="sxs-lookup"><span data-stu-id="9639a-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="9639a-107">Предварительным условием для данного руководства является наличие действующего договора покупки с обязательством по количеству продукта для поставщика и номенклатур.</span><span class="sxs-lookup"><span data-stu-id="9639a-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="9639a-108">Эта же процедура может использоваться при наличии договора покупки с другими типами обязательств.</span><span class="sxs-lookup"><span data-stu-id="9639a-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="9639a-109">Это руководство можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="9639a-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="9639a-110">При использовании компании USMF можно сначала выполнить руководств "Создание договора покупки" для выполнения необходимых предварительных условий для данного руководства.</span><span class="sxs-lookup"><span data-stu-id="9639a-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="9639a-111">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="9639a-111">Create a purchase order</span></span>
1. <span data-ttu-id="9639a-112">В **области перехода** выберите **Рабочие области > Подготовка заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="9639a-112">In the **Navigation pane**, go to **Workspaces > Purchase order preparation**.</span></span> 
2. <span data-ttu-id="9639a-113">Щелкните **Новый заказ на покупку**.</span><span class="sxs-lookup"><span data-stu-id="9639a-113">Click **New purchase order**.</span></span>
3. <span data-ttu-id="9639a-114">В поле **Счет поставщика** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9639a-114">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9639a-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="9639a-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9639a-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9639a-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9639a-117">Разверните экспресс-вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="9639a-117">Expand the **General** fastTab.</span></span>
7. <span data-ttu-id="9639a-118">В поле **Договор покупки** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9639a-118">In the **Purchase agreement** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="9639a-119">Здесь перечислены все доступные соглашения по поставщику.</span><span class="sxs-lookup"><span data-stu-id="9639a-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="9639a-120">Найдите действующее соглашение, которое необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="9639a-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="9639a-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9639a-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9639a-122">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="9639a-122">Click **Yes**.</span></span>
10. <span data-ttu-id="9639a-123">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="9639a-123">Click **OK**.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="9639a-124">Добавление строки</span><span class="sxs-lookup"><span data-stu-id="9639a-124">Add a line</span></span>
1. <span data-ttu-id="9639a-125">В поле **Код номенклатуры** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9639a-125">In the **Item number** field, type a value.</span></span> <span data-ttu-id="9639a-126">При наличии в обязательстве конкретных аналитик запасов или местонахождения необходимо ввести те же значения в строке заказа на покупку, чтобы использовать соглашение.</span><span class="sxs-lookup"><span data-stu-id="9639a-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="9639a-127">В поле **Место** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9639a-127">In the **Site** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="9639a-128">Сайт может уже быть заполнен значением по умолчанию из заказа или из поставщика.</span><span class="sxs-lookup"><span data-stu-id="9639a-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="9639a-129">В таком случае пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="9639a-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="9639a-130">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="9639a-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="9639a-131">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9639a-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9639a-132">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="9639a-132">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="9639a-133">Убедитесь, что цена скопирована из обязательства.</span><span class="sxs-lookup"><span data-stu-id="9639a-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="9639a-134">Поиск обязательства</span><span class="sxs-lookup"><span data-stu-id="9639a-134">Look up the commitment</span></span>
1. <span data-ttu-id="9639a-135">Щелкните **Обновить строку**.</span><span class="sxs-lookup"><span data-stu-id="9639a-135">Click **Update line**.</span></span>
2. <span data-ttu-id="9639a-136">Щелкните **Присоединено**.</span><span class="sxs-lookup"><span data-stu-id="9639a-136">Click **Attached**.</span></span> <span data-ttu-id="9639a-137">Здесь можно получить сведения о договоре покупки.</span><span class="sxs-lookup"><span data-stu-id="9639a-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="9639a-138">Например, можно узнать цену, а также являются ли цена и скидка фиксированными; это означает, что изменении цены или скидки в заказе на покупку на значение, отличное от значения в обязательстве, система удалит ссылку, чтобы строка заказа на покупку не засчитывалась в обязательство.</span><span class="sxs-lookup"><span data-stu-id="9639a-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="9639a-139">Также можно увидеть, выбран ли параметр "Используется максимум", что означает, что при суммировании всех покупок, засчитываемых в обязательство, количество в обязательстве превысить нельзя.</span><span class="sxs-lookup"><span data-stu-id="9639a-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="9639a-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9639a-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="9639a-141">Поиск договора покупки</span><span class="sxs-lookup"><span data-stu-id="9639a-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="9639a-142">На **панели операций** щелкните **Общее**.</span><span class="sxs-lookup"><span data-stu-id="9639a-142">On the **Action Pane**, click **General**.</span></span>
2. <span data-ttu-id="9639a-143">Щелкните **Договор покупки**.</span><span class="sxs-lookup"><span data-stu-id="9639a-143">Click **Purchase agreement**.</span></span>
3. <span data-ttu-id="9639a-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9639a-144">Close the page.</span></span>
4. <span data-ttu-id="9639a-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9639a-145">Close the page.</span></span>

