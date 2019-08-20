---
title: Определение условий оплаты для поставщиков
description: В этом разделе описывается, как настроить условия оплаты для счетов поставщиков.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6432d04aa821e76d67e2c430e514f4b9056d8228
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843203"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="0f633-103">Определение условий оплаты для поставщиков</span><span class="sxs-lookup"><span data-stu-id="0f633-103">Define vendor payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0f633-104">В этом разделе описывается, как настроить условия оплаты для счетов поставщиков.</span><span class="sxs-lookup"><span data-stu-id="0f633-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="0f633-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="0f633-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="0f633-106">Выберите **Область переходов > Модули > Расчеты с поставщиками > Настройка платежей > Условия оплаты**.</span><span class="sxs-lookup"><span data-stu-id="0f633-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="0f633-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0f633-107">Select **New**.</span></span> <span data-ttu-id="0f633-108">Страница "Условия оплаты" используется для определения способа расчета срока выполнения.</span><span class="sxs-lookup"><span data-stu-id="0f633-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="0f633-109">Она не используется для определения способа расчета дата скидки по оплате.</span><span class="sxs-lookup"><span data-stu-id="0f633-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="0f633-110">В поле **Условия оплаты** введите значение.</span><span class="sxs-lookup"><span data-stu-id="0f633-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="0f633-111">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="0f633-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="0f633-112">В поле **Дни** введите число.</span><span class="sxs-lookup"><span data-stu-id="0f633-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="0f633-113">Число, введенное здесь, будет использоваться для добавления к сроку выполнения или в конец периода, указанного в способе оплаты.</span><span class="sxs-lookup"><span data-stu-id="0f633-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="0f633-114">Например, если выбрать значение **Нетто**, это число будет добавлено к сроку выполнения.</span><span class="sxs-lookup"><span data-stu-id="0f633-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="0f633-115">Если выбрать значение **Текущий месяц**, это число будет добавлено к последнему дню текущего месяца для расчета срока выполнения.</span><span class="sxs-lookup"><span data-stu-id="0f633-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="0f633-116">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0f633-116">Select **Save**.</span></span>
7. <span data-ttu-id="0f633-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0f633-117">Close the page.</span></span>
8. <span data-ttu-id="0f633-118">Перейдите в раздел **Расчеты с поставщиками > Настройка платежей > Скидки по оплате**.</span><span class="sxs-lookup"><span data-stu-id="0f633-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="0f633-119">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0f633-119">Select **New**.</span></span>
10. <span data-ttu-id="0f633-120">В поле **Скидка по оплате** введите код.</span><span class="sxs-lookup"><span data-stu-id="0f633-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="0f633-121">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="0f633-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="0f633-122">Если поставщик предлагает многоуровневую скидку, выберите следующую скидку по оплате по истечении срока действия текущей скидки.</span><span class="sxs-lookup"><span data-stu-id="0f633-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="0f633-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0f633-123">Close the page.</span></span>
14. <span data-ttu-id="0f633-124">В поле **Дни** введите число.</span><span class="sxs-lookup"><span data-stu-id="0f633-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="0f633-125">Количество, указанное в поле **Дни**, будет использоваться для расчета даты скидки при оплате на основании параметра, выбранного в поле **Нетто/Период**.</span><span class="sxs-lookup"><span data-stu-id="0f633-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="0f633-126">Если выбрано значение **Нетто**, количество будет добавляться к дате накладной для определения даты скидки по оплате.</span><span class="sxs-lookup"><span data-stu-id="0f633-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="0f633-127">Если выбрано значение **Текущий месяц**, количество будет добавляться в конец текущего месяца для определения даты скидки по оплате.</span><span class="sxs-lookup"><span data-stu-id="0f633-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="0f633-128">Введите процент скидки по оплате в поле **Скидка**.</span><span class="sxs-lookup"><span data-stu-id="0f633-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="0f633-129">Введите счет ГК, на который будет разнесена скидка по оплате для счетов-фактур клиента, затем введите счет ГК, на который будет разнесана скидка по оплате для счетов-фактур поставщиков.</span><span class="sxs-lookup"><span data-stu-id="0f633-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="0f633-130">Если для параметра **Корр. счет скидки** задано значение **Использовать счет ГК для скидок поставщика**, будет использоваться счет ГК.</span><span class="sxs-lookup"><span data-stu-id="0f633-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="0f633-131">Если для параметра задано значение **Счета в строках накладной**, скидка по оплате будет разнесена на счета основного средства/расходов в строках накладной.</span><span class="sxs-lookup"><span data-stu-id="0f633-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="0f633-132">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0f633-132">Select **Save**.</span></span>

