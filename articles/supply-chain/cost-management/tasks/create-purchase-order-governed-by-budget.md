---
title: Создание заказа на покупку в соответствии с бюджетом
description: Эта процедура служит для создания заказа на покупку, который проверяется на наличие доступного бюджета.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 319eb0070a3677035e2a5d89744e80cd38c08d8e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436114"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="27856-103">Создание заказа на покупку в соответствии с бюджетом</span><span class="sxs-lookup"><span data-stu-id="27856-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27856-104">Эта процедура служит для создания заказа на покупку, который проверяется на наличие доступного бюджета.</span><span class="sxs-lookup"><span data-stu-id="27856-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="27856-105">В этой записи используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="27856-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="27856-106">Просмотр конфигурации бюджетного контроля</span><span class="sxs-lookup"><span data-stu-id="27856-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="27856-107">Перейдите в раздел "Бюджетирование" > "Настройка" > "Бюджетный контроль" > "Конфигурация бюджетного контроля".</span><span class="sxs-lookup"><span data-stu-id="27856-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="27856-108">Перейдите на вкладку "Доступные бюджетные средства".</span><span class="sxs-lookup"><span data-stu-id="27856-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="27856-109">Перейдите на вкладку "Документы и журналы".</span><span class="sxs-lookup"><span data-stu-id="27856-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="27856-110">Перейдите на вкладку "Определение правил бюджетного контроля".</span><span class="sxs-lookup"><span data-stu-id="27856-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="27856-111">Перейдите на вкладку "Определить бюджетные группы".</span><span class="sxs-lookup"><span data-stu-id="27856-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="27856-112">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="27856-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="27856-113">Создание заголовка заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="27856-113">Create the purchase order header</span></span>
1. <span data-ttu-id="27856-114">Перейдите в раздел "Закупки и источники" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="27856-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="27856-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="27856-115">Click New.</span></span>
3. <span data-ttu-id="27856-116">В поле "Счет поставщика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="27856-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="27856-117">Разверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="27856-117">Expand the General section.</span></span>
5. <span data-ttu-id="27856-118">В поле "Финансовая дата" установите дату "01.01.2016".</span><span class="sxs-lookup"><span data-stu-id="27856-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="27856-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="27856-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="27856-120">Добавление строки заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="27856-120">Add a purchase order line</span></span>
1. <span data-ttu-id="27856-121">В поле "Категория закупаемой продукции " введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="27856-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="27856-122">Для параметра "Количество" задайте значение "2".</span><span class="sxs-lookup"><span data-stu-id="27856-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="27856-123">В поле "Единица измерения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="27856-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="27856-124">В поле "Цена за ед. изм." введите "10 000".</span><span class="sxs-lookup"><span data-stu-id="27856-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="27856-125">Щелкните "Статистика".</span><span class="sxs-lookup"><span data-stu-id="27856-125">Click Financials.</span></span>
6. <span data-ttu-id="27856-126">Щелкните "Распределить суммы".</span><span class="sxs-lookup"><span data-stu-id="27856-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="27856-127">В поле "Счет ГК" укажите значение "601300-001-023--".</span><span class="sxs-lookup"><span data-stu-id="27856-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="27856-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="27856-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="27856-129">Выполнить проверку бюджета</span><span class="sxs-lookup"><span data-stu-id="27856-129">Perform budget checking</span></span>
1. <span data-ttu-id="27856-130">Щелкните "Статистика".</span><span class="sxs-lookup"><span data-stu-id="27856-130">Click Financials.</span></span>
2. <span data-ttu-id="27856-131">Щелкните "Выполнить проверку бюджета".</span><span class="sxs-lookup"><span data-stu-id="27856-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="27856-132">Щелкните "Статистика".</span><span class="sxs-lookup"><span data-stu-id="27856-132">Click Financials.</span></span>
4. <span data-ttu-id="27856-133">Щелкните "Ошибки или предупреждения бюджетных проверок".</span><span class="sxs-lookup"><span data-stu-id="27856-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="27856-134">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="27856-134">Click Close.</span></span>

