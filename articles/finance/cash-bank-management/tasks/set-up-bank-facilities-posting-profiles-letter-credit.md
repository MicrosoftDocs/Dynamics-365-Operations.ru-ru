---
title: Настройка банковских услуг и профилей разноски для аккредитива
description: Эта процедура иллюстрирует создание банковской услуги и профиля разноски, необходимых для обработки аккредитивов.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6afa52fa2c784fd7afbdc8db0e079af0689b4bec
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144172"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="55f58-103">Настройка банковских услуг и профилей разноски для аккредитива</span><span class="sxs-lookup"><span data-stu-id="55f58-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55f58-104">Эта процедура иллюстрирует создание банковской услуги и профиля разноски, необходимых для обработки аккредитивов.</span><span class="sxs-lookup"><span data-stu-id="55f58-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="55f58-105">В этих задачах используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="55f58-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="55f58-106">Параметр главной книги</span><span class="sxs-lookup"><span data-stu-id="55f58-106">General ledger parameter</span></span>
1. <span data-ttu-id="55f58-107">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Параметры управления банком и кассовыми операциями".</span><span class="sxs-lookup"><span data-stu-id="55f58-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="55f58-108">Разверните раздел "Банковский документ".</span><span class="sxs-lookup"><span data-stu-id="55f58-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="55f58-109">Выберите параметр "Включить импортный аккредитив".</span><span class="sxs-lookup"><span data-stu-id="55f58-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="55f58-110">Выберите параметр "Включить экспортный аккредитив".</span><span class="sxs-lookup"><span data-stu-id="55f58-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="55f58-111">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="55f58-111">Click Save.</span></span>
6. <span data-ttu-id="55f58-112">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="55f58-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="55f58-113">Создание банковской услуги</span><span class="sxs-lookup"><span data-stu-id="55f58-113">Create Bank facility</span></span>
1. <span data-ttu-id="55f58-114">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Банковские ссуды".</span><span class="sxs-lookup"><span data-stu-id="55f58-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="55f58-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="55f58-115">Click New.</span></span>
3. <span data-ttu-id="55f58-116">В поле "Группа ссуды" введите имя группы банковских услуг.</span><span class="sxs-lookup"><span data-stu-id="55f58-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="55f58-117">В поле "Описание" введите описание группы банковских услуг.</span><span class="sxs-lookup"><span data-stu-id="55f58-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="55f58-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="55f58-118">Click Save.</span></span>
6. <span data-ttu-id="55f58-119">Перейдите на вкладку "Типы ссуд".</span><span class="sxs-lookup"><span data-stu-id="55f58-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="55f58-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="55f58-120">Click New.</span></span>
8. <span data-ttu-id="55f58-121">В поле "Тип ссуды" введите уникальный код.</span><span class="sxs-lookup"><span data-stu-id="55f58-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="55f58-122">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="55f58-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="55f58-123">В поле "Группа ссуды" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="55f58-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="55f58-124">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="55f58-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="55f58-125">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="55f58-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="55f58-126">В поле "Характер ссуды" выберите характер банковской услуги.</span><span class="sxs-lookup"><span data-stu-id="55f58-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="55f58-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="55f58-127">Click Save.</span></span>
15. <span data-ttu-id="55f58-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="55f58-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="55f58-129">Профиль разноски банка</span><span class="sxs-lookup"><span data-stu-id="55f58-129">Bank posting profile</span></span>
1. <span data-ttu-id="55f58-130">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Профиль разноски банковских документов".</span><span class="sxs-lookup"><span data-stu-id="55f58-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="55f58-131">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="55f58-131">Click New.</span></span>
3. <span data-ttu-id="55f58-132">В поле "Номер счета/группы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="55f58-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="55f58-133">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="55f58-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="55f58-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="55f58-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="55f58-135">Выберите главный счет для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="55f58-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="55f58-136">Этот счет используется при расчете прогноза движения денежных средств.</span><span class="sxs-lookup"><span data-stu-id="55f58-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="55f58-137">В поле "Счет расходов" выберите счет для расходных проводок.</span><span class="sxs-lookup"><span data-stu-id="55f58-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="55f58-138">В поле "Счет маржи" выберите счет для проводок маржи.</span><span class="sxs-lookup"><span data-stu-id="55f58-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="55f58-139">Этот счет дебетуется при разноске открывающей маржи и кредитуется при разноске платежа.</span><span class="sxs-lookup"><span data-stu-id="55f58-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="55f58-140">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="55f58-140">Click Save.</span></span>

