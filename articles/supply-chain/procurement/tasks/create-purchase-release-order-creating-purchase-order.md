---
title: Создание заказа на выпуск покупки при создании заказа на покупку
description: В этой процедуре показано, как использовать договор покупки при создании заказа на покупку.
author: mkirknel
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
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad74f52682627d6164270de54e2dbcaeb57111fe
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547522"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a><span data-ttu-id="f27be-103">Создание заказа на выпуск покупки при создании заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="f27be-103">Create a purchase release order when creating the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f27be-104">В этой процедуре показано, как использовать договор покупки при создании заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f27be-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="f27be-105">При создании заказа на покупку необходимо применить к нему договор покупки, поскольку в нем содержатся общие условия, которые следует скопировать в заголовок заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f27be-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="f27be-106">Обычно эту задачу выполняет специалист по закупке.</span><span class="sxs-lookup"><span data-stu-id="f27be-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="f27be-107">Предварительным условием для данного руководства является наличие действующего договора покупки с обязательством по количеству продукта для поставщика и номенклатур.</span><span class="sxs-lookup"><span data-stu-id="f27be-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="f27be-108">Эта же процедура может использоваться при наличии договора покупки с другими типами обязательств.</span><span class="sxs-lookup"><span data-stu-id="f27be-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="f27be-109">Это руководство можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="f27be-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="f27be-110">При использовании компании USMF можно сначала выполнить руководств "Создание договора покупки" для выполнения необходимых предварительных условий для данного руководства.</span><span class="sxs-lookup"><span data-stu-id="f27be-110">If you’re using USMF, you can run the “Create a purchase agreement” guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="f27be-111">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="f27be-111">Create a purchase order</span></span>
1. <span data-ttu-id="f27be-112">Откройте рабочую область подготовки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f27be-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="f27be-113">Щелкните "Новый заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="f27be-113">Click New purchase order.</span></span>
3. <span data-ttu-id="f27be-114">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f27be-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f27be-115">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="f27be-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f27be-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f27be-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f27be-117">Переключите развертывание раздела "Общее".</span><span class="sxs-lookup"><span data-stu-id="f27be-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="f27be-118">В поле "Договор покупки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f27be-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f27be-119">Здесь перечислены все доступные соглашения по поставщику.</span><span class="sxs-lookup"><span data-stu-id="f27be-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="f27be-120">Найдите действующее соглашение, которое необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="f27be-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="f27be-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f27be-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f27be-122">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="f27be-122">Click Yes.</span></span>
10. <span data-ttu-id="f27be-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f27be-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="f27be-124">Добавление строки</span><span class="sxs-lookup"><span data-stu-id="f27be-124">Add a line</span></span>
1. <span data-ttu-id="f27be-125">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f27be-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f27be-126">При наличии в обязательстве конкретных аналитик запасов или местонахождения необходимо ввести те же значения в строке заказа на покупку, чтобы использовать соглашение.</span><span class="sxs-lookup"><span data-stu-id="f27be-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="f27be-127">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f27be-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f27be-128">Сайт может уже быть заполнен значением по умолчанию из заказа или из поставщика.</span><span class="sxs-lookup"><span data-stu-id="f27be-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="f27be-129">В таком случае пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="f27be-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="f27be-130">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f27be-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f27be-131">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f27be-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f27be-132">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="f27be-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="f27be-133">Убедитесь, что цена скопирована из обязательства.</span><span class="sxs-lookup"><span data-stu-id="f27be-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="f27be-134">Поиск обязательства</span><span class="sxs-lookup"><span data-stu-id="f27be-134">Look up the commitment</span></span>
1. <span data-ttu-id="f27be-135">Щелкните "Обновить строку".</span><span class="sxs-lookup"><span data-stu-id="f27be-135">Click Update line.</span></span>
2. <span data-ttu-id="f27be-136">Щелкните "Присоединено".</span><span class="sxs-lookup"><span data-stu-id="f27be-136">Click Attached.</span></span>
    * <span data-ttu-id="f27be-137">Здесь можно получить сведения о договоре покупки.</span><span class="sxs-lookup"><span data-stu-id="f27be-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="f27be-138">Например, можно узнать цену, а также являются ли цена и скидка фиксированными; это означает, что изменении цены или скидки в заказе на покупку на значение, отличное от значения в обязательстве, система удалит ссылку, чтобы строка заказа на покупку не засчитывалась в обязательство.</span><span class="sxs-lookup"><span data-stu-id="f27be-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="f27be-139">Также можно увидеть, выбран ли параметр "Используется максимум", что означает, что при суммировании всех покупок, засчитываемых в обязательство, количество в обязательстве превысить нельзя.</span><span class="sxs-lookup"><span data-stu-id="f27be-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="f27be-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f27be-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="f27be-141">Поиск договора покупки</span><span class="sxs-lookup"><span data-stu-id="f27be-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="f27be-142">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="f27be-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="f27be-143">Щелкните "Договор покупки".</span><span class="sxs-lookup"><span data-stu-id="f27be-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="f27be-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f27be-144">Close the page.</span></span>
4. <span data-ttu-id="f27be-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f27be-145">Close the page.</span></span>

