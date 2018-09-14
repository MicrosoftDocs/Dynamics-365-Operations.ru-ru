--- 
title: "Разбивка ОС"
description: "В данном руководстве по задаче показано, как разделить процент одной модели стоимости основного средства в новую модель стоимости основного средства."
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6be9de64265a4d7b5c91af3ee8acfce80c78e0f1
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="cc619-103">Разбивка ОС</span><span class="sxs-lookup"><span data-stu-id="cc619-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc619-104">В данном руководстве по задаче показано, как разделить процент одной модели стоимости основного средства в новую модель стоимости основного средства.</span><span class="sxs-lookup"><span data-stu-id="cc619-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="cc619-105">В нем используется роль бухгалтера и демонстрационные данные USMF.</span><span class="sxs-lookup"><span data-stu-id="cc619-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="cc619-106">Создание нового основного средства</span><span class="sxs-lookup"><span data-stu-id="cc619-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="cc619-107">Перейдите в раздел "Основные средства" > "Основные средства" > "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="cc619-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="cc619-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="cc619-108">Click New.</span></span>
3. <span data-ttu-id="cc619-109">В поле "Группа ОС" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="cc619-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="cc619-110">Обратите внимание на номер основного средства для использования в процессе разбиения позже.</span><span class="sxs-lookup"><span data-stu-id="cc619-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="cc619-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cc619-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="cc619-112">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="cc619-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="cc619-113">Разбивка ОС</span><span class="sxs-lookup"><span data-stu-id="cc619-113">Split a fixed asset</span></span>
1. <span data-ttu-id="cc619-114">Найдите в списке основное средство для разбиения и выберите его.</span><span class="sxs-lookup"><span data-stu-id="cc619-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="cc619-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="cc619-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="cc619-116">Нажмите "Книги".</span><span class="sxs-lookup"><span data-stu-id="cc619-116">Click Books.</span></span>
    * <span data-ttu-id="cc619-117">Выберите книгу для разбиения в новое основное средство.</span><span class="sxs-lookup"><span data-stu-id="cc619-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="cc619-118">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="cc619-118">Click Functions.</span></span>
5. <span data-ttu-id="cc619-119">Щелкните "Разбивка ОС".</span><span class="sxs-lookup"><span data-stu-id="cc619-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="cc619-120">В поле "В основные средства" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="cc619-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="cc619-121">В поле "В книгу" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="cc619-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="cc619-122">В поле "Дата проводки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="cc619-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="cc619-123">В поле "Процент" введите число.</span><span class="sxs-lookup"><span data-stu-id="cc619-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="cc619-124">В поле "Наименование журнала" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="cc619-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="cc619-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="cc619-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="cc619-126">Разноска проводки по журналу</span><span class="sxs-lookup"><span data-stu-id="cc619-126">Post the journal transaction</span></span>
1. <span data-ttu-id="cc619-127">Перейдите в раздел "Основные средства" > "Записи в журнале" > "Журнал основных средств".</span><span class="sxs-lookup"><span data-stu-id="cc619-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="cc619-128">В списке выберите журнал, созданный в результате процесса разбиения.</span><span class="sxs-lookup"><span data-stu-id="cc619-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="cc619-129">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="cc619-129">Click Lines.</span></span>
    * <span data-ttu-id="cc619-130">Проверьте созданные строки журнала.</span><span class="sxs-lookup"><span data-stu-id="cc619-130">Verify the journal lines created.</span></span>  <span data-ttu-id="cc619-131">Проводка о корректировке приобретения создается для исходного основного средства для уменьшения стоимости на процент, указанный в процессе разбиения.</span><span class="sxs-lookup"><span data-stu-id="cc619-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="cc619-132">Проводка приобретения создается для нового основного средства на ту же сумму.</span><span class="sxs-lookup"><span data-stu-id="cc619-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="cc619-133">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="cc619-133">Click Post.</span></span>


