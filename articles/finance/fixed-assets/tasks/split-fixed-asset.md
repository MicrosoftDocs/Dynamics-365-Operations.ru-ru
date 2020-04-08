---
title: Разбивка ОС
description: В этой теме показано, как разделить процент одной модели стоимости основного средства в новую модель стоимости основного средства.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85ccf187e77faf338ac29452d823c3652b806a21
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138123"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="37268-103">Разбивка ОС</span><span class="sxs-lookup"><span data-stu-id="37268-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37268-104">В этой теме показано, как разделить процент одной модели стоимости основного средства в новую модель стоимости основного средства.</span><span class="sxs-lookup"><span data-stu-id="37268-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="37268-105">В нем используется роль бухгалтера и демонстрационные данные USMF.</span><span class="sxs-lookup"><span data-stu-id="37268-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="37268-106">Создание нового основного средства</span><span class="sxs-lookup"><span data-stu-id="37268-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="37268-107">В области перехода, перейдите к **Модули > Фиксированные активы > Фиксированные активы > Фиксированные активы**.</span><span class="sxs-lookup"><span data-stu-id="37268-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="37268-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="37268-108">Select **New**.</span></span>
3. <span data-ttu-id="37268-109">В поле **Группа ОС** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="37268-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="37268-110">Обратите внимание на номер основного средства для использования в процессе разбиения позже.</span><span class="sxs-lookup"><span data-stu-id="37268-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="37268-111">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="37268-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="37268-112">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="37268-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="37268-113">Разбивка ОС</span><span class="sxs-lookup"><span data-stu-id="37268-113">Split a fixed asset</span></span>
1. <span data-ttu-id="37268-114">Найдите и выберите в списке ссылку на основное средство для разбиения.</span><span class="sxs-lookup"><span data-stu-id="37268-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="37268-115">Выберите **Книги**.</span><span class="sxs-lookup"><span data-stu-id="37268-115">Select **Books**.</span></span> <span data-ttu-id="37268-116">Выберите книгу для разбиения в новое основное средство.</span><span class="sxs-lookup"><span data-stu-id="37268-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="37268-117">Выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="37268-117">Select **Functions**.</span></span>
4. <span data-ttu-id="37268-118">Выберите **Разбивка ОС**.</span><span class="sxs-lookup"><span data-stu-id="37268-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="37268-119">В поле **В основные средства** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="37268-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="37268-120">В поле **В книгу** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="37268-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="37268-121">В поле **Дата проводки** введите дату.</span><span class="sxs-lookup"><span data-stu-id="37268-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="37268-122">В поле **Процент** введите число.</span><span class="sxs-lookup"><span data-stu-id="37268-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="37268-123">В поле **Наименование журнала** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="37268-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="37268-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37268-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="37268-125">Разноска проводки по журналу</span><span class="sxs-lookup"><span data-stu-id="37268-125">Post the journal transaction</span></span>
1. <span data-ttu-id="37268-126">В области перехода, перейдите к **Модули > Основные средства > Записи журнала > Журнал основных средств**.</span><span class="sxs-lookup"><span data-stu-id="37268-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="37268-127">В списке выберите журнал, созданный в результате процесса разбиения.</span><span class="sxs-lookup"><span data-stu-id="37268-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="37268-128">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="37268-128">Select **Lines**.</span></span>

    - <span data-ttu-id="37268-129">Проверьте созданные строки журнала.</span><span class="sxs-lookup"><span data-stu-id="37268-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="37268-130">Проводка о корректировке приобретения создается для исходного основного средства для уменьшения стоимости на процент, указанный в процессе разбиения.</span><span class="sxs-lookup"><span data-stu-id="37268-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="37268-131">Проводка приобретения создается для нового основного средства на ту же сумму.</span><span class="sxs-lookup"><span data-stu-id="37268-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="37268-132">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="37268-132">Select **Post**.</span></span>

