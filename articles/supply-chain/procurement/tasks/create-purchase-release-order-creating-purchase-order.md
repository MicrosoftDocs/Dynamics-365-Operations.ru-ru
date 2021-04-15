---
title: Создание заказа на выпуск покупки при создании заказа на покупку
description: В этой процедуре показано, как использовать договор покупки при создании заказа на покупку.
author: kamaybac
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2f02961f5f7da9bff389737b447e3b143dd72e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812280"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a><span data-ttu-id="a20f5-103">Создание заказа на выпуск покупки при создании заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="a20f5-103">Create a purchase release order when creating the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a20f5-104">В этой процедуре показано, как использовать договор покупки при создании заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="a20f5-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="a20f5-105">При создании заказа на покупку необходимо применить к нему договор покупки, поскольку в нем содержатся общие условия, которые следует скопировать в заголовок заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="a20f5-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="a20f5-106">Обычно эту задачу выполняет специалист по закупке.</span><span class="sxs-lookup"><span data-stu-id="a20f5-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="a20f5-107">Предварительным условием для данного руководства является наличие действующего договора покупки с обязательством по количеству продукта для поставщика и номенклатур.</span><span class="sxs-lookup"><span data-stu-id="a20f5-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="a20f5-108">Эта же процедура может использоваться при наличии договора покупки с другими типами обязательств.</span><span class="sxs-lookup"><span data-stu-id="a20f5-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="a20f5-109">Это руководство можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="a20f5-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="a20f5-110">При использовании компании USMF можно сначала выполнить руководств "Создание договора покупки" для выполнения необходимых предварительных условий для данного руководства.</span><span class="sxs-lookup"><span data-stu-id="a20f5-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="a20f5-111">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="a20f5-111">Create a purchase order</span></span>
1. <span data-ttu-id="a20f5-112">Откройте рабочую область подготовки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="a20f5-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="a20f5-113">Щелкните "Новый заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="a20f5-113">Click New purchase order.</span></span>
3. <span data-ttu-id="a20f5-114">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a20f5-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a20f5-115">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="a20f5-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a20f5-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a20f5-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a20f5-117">Переключите развертывание раздела "Общее".</span><span class="sxs-lookup"><span data-stu-id="a20f5-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="a20f5-118">В поле "Договор покупки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a20f5-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a20f5-119">Здесь перечислены все доступные соглашения по поставщику.</span><span class="sxs-lookup"><span data-stu-id="a20f5-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="a20f5-120">Найдите действующее соглашение, которое необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="a20f5-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="a20f5-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a20f5-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a20f5-122">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="a20f5-122">Click Yes.</span></span>
10. <span data-ttu-id="a20f5-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a20f5-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="a20f5-124">Добавление строки</span><span class="sxs-lookup"><span data-stu-id="a20f5-124">Add a line</span></span>
1. <span data-ttu-id="a20f5-125">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a20f5-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a20f5-126">При наличии в обязательстве конкретных аналитик запасов или местонахождения необходимо ввести те же значения в строке заказа на покупку, чтобы использовать соглашение.</span><span class="sxs-lookup"><span data-stu-id="a20f5-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="a20f5-127">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a20f5-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a20f5-128">Сайт может уже быть заполнен значением по умолчанию из заказа или из поставщика.</span><span class="sxs-lookup"><span data-stu-id="a20f5-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="a20f5-129">В таком случае пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="a20f5-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="a20f5-130">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a20f5-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a20f5-131">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a20f5-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a20f5-132">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="a20f5-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a20f5-133">Убедитесь, что цена скопирована из обязательства.</span><span class="sxs-lookup"><span data-stu-id="a20f5-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="a20f5-134">Поиск обязательства</span><span class="sxs-lookup"><span data-stu-id="a20f5-134">Look up the commitment</span></span>
1. <span data-ttu-id="a20f5-135">Щелкните "Обновить строку".</span><span class="sxs-lookup"><span data-stu-id="a20f5-135">Click Update line.</span></span>
2. <span data-ttu-id="a20f5-136">Щелкните "Присоединено".</span><span class="sxs-lookup"><span data-stu-id="a20f5-136">Click Attached.</span></span>
    * <span data-ttu-id="a20f5-137">Здесь можно получить сведения о договоре покупки.</span><span class="sxs-lookup"><span data-stu-id="a20f5-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="a20f5-138">Например, можно узнать цену, а также являются ли цена и скидка фиксированными; это означает, что изменении цены или скидки в заказе на покупку на значение, отличное от значения в обязательстве, система удалит ссылку, чтобы строка заказа на покупку не засчитывалась в обязательство.</span><span class="sxs-lookup"><span data-stu-id="a20f5-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="a20f5-139">Также можно увидеть, выбран ли параметр "Используется максимум", что означает, что при суммировании всех покупок, засчитываемых в обязательство, количество в обязательстве превысить нельзя.</span><span class="sxs-lookup"><span data-stu-id="a20f5-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="a20f5-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a20f5-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="a20f5-141">Поиск договора покупки</span><span class="sxs-lookup"><span data-stu-id="a20f5-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="a20f5-142">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="a20f5-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="a20f5-143">Щелкните "Договор покупки".</span><span class="sxs-lookup"><span data-stu-id="a20f5-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="a20f5-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a20f5-144">Close the page.</span></span>
4. <span data-ttu-id="a20f5-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a20f5-145">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]