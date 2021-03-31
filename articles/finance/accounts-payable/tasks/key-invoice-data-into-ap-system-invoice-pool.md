---
title: Ввод данных счета в модуль расчетов с поставщиками с использованием кластера накладных
description: В этой теме описывается, как использовать регистр накладных для создания накладных.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 670dd2ec15aa26791758ec4bea2b431482499436
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227168"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="d1c6d-103">Ввод данных счета в модуль расчетов с поставщиками с использованием кластера накладных</span><span class="sxs-lookup"><span data-stu-id="d1c6d-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1c6d-104">В этой теме описывается, как использовать регистр накладных для создания накладных.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="d1c6d-105">Затем используйте кластер накладных для сопоставления накладной с заказом на покупку и завершения оформления расходов на странице накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="d1c6d-106">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="d1c6d-106">Create a purchase order</span></span>
1. <span data-ttu-id="d1c6d-107">В области перехода перейдите к **Модули > Расчеты с поставщиками > Заказы на покупку > Заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="d1c6d-108">Выберите **Создать**, чтобы создать заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="d1c6d-109">В поле **Счет поставщика** выберите поставщика для раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="d1c6d-110">Например, выберите поставщика **1001**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="d1c6d-111">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-111">Select **OK**.</span></span>
5. <span data-ttu-id="d1c6d-112">В поле **Код номенклатуры** выберите код номенклатуры обслуживания из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="d1c6d-113">Например, выберите **S0001**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-113">For example, select **S0001**.</span></span> <span data-ttu-id="d1c6d-114">Чистая сумма равна 75,00.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-114">The net amount is 75.00.</span></span>  <span data-ttu-id="d1c6d-115">Это сумма, которая ожидается в накладной.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="d1c6d-116">На панели операций выберите **Покупка**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="d1c6d-117">Выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="d1c6d-118">Создание и разноска накладной</span><span class="sxs-lookup"><span data-stu-id="d1c6d-118">Create and post and invoice</span></span>
1. <span data-ttu-id="d1c6d-119">В области переходов выберите **Модули > Расчеты с поставщиками > Накладные > Регистрация накладных**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="d1c6d-120">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-120">Select **New**.</span></span>
3. <span data-ttu-id="d1c6d-121">Откройте поиск, чтобы выбрать имя регистра накладных для использования.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="d1c6d-122">Выберите имя регистра накладных для использования.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="d1c6d-123">Выберите **Строки**, чтобы открыть регистр и ввести строки расходов.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="d1c6d-124">В окне поиска выберите поставщика.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="d1c6d-125">Например, выберите поставщика **1001**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="d1c6d-126">В поле **Накладная** введите номер накладной.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="d1c6d-127">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="d1c6d-128">В поле **Кредит** введите число.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="d1c6d-129">В поле **Заказ на покупку** откройте раскрывающийся список, чтобы выбрать созданный ранее заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="d1c6d-130">В поле **Кем утверждено** выделите утверждающего в раскрывающемся списке и щелкните **Выбрать**, чтобы выбрать утверждающего.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="d1c6d-131">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="d1c6d-132">Открытие накладной из кластера и сопоставление накладной с заказом на покупку для завершения процесса накладной</span><span class="sxs-lookup"><span data-stu-id="d1c6d-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="d1c6d-133">В области переходов выберите **Модули > Расчеты с поставщиками > Накладные > Пул накладных**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="d1c6d-134">Выберите **Заказ на покупку**, чтобы создать накладную поставщика из накладной в кластере.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="d1c6d-135">Выберите накладную, которую требуется просмотреть.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="d1c6d-136">Выберите **Обновить статус сопоставления**, чтобы завершить сопоставление.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="d1c6d-137">На панели операций выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="d1c6d-138">Выберите **Изменить режим просмотра**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-138">Select **Change view**.</span></span>
7. <span data-ttu-id="d1c6d-139">Выберите **Представление сетки**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="d1c6d-140">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-140">Select **Post**.</span></span>
9. <span data-ttu-id="d1c6d-141">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-141">Close the form.</span></span>
10. <span data-ttu-id="d1c6d-142">В области переходов выберите **Модули > Расчеты с поставщиками > Поставщики > Поставщики**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="d1c6d-143">Выберите поставщика, указанного в заказе на покупку.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="d1c6d-144">Например, выберите поставщика **1001**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="d1c6d-145">На панели операций выберите **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="d1c6d-146">Выберите **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="d1c6d-147">Выберите созданную накладную.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-147">Select the invoice that you created.</span></span> <span data-ttu-id="d1c6d-148">Начисление регистра накладных было реверсировано и разнесено на соответствующий счет расходов.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]