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
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000301"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="3a5f5-103">Разбивка ОС</span><span class="sxs-lookup"><span data-stu-id="3a5f5-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a5f5-104">В этой теме показано, как разделить процент одной модели стоимости основного средства в новую модель стоимости основного средства.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="3a5f5-105">В нем используется роль бухгалтера и демонстрационные данные USMF.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="3a5f5-106">Создание нового основного средства</span><span class="sxs-lookup"><span data-stu-id="3a5f5-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="3a5f5-107">В области перехода, перейдите к разделу **Модули \> Основные средства \> Основные средства \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="3a5f5-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-108">Select **New**.</span></span>
3. <span data-ttu-id="3a5f5-109">В поле **Группа ОС** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="3a5f5-110">Обратите внимание на номер основного средства для использования в процессе разбиения позже.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="3a5f5-111">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="3a5f5-112">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="3a5f5-113">Разбивка ОС</span><span class="sxs-lookup"><span data-stu-id="3a5f5-113">Split a fixed asset</span></span>

<span data-ttu-id="3a5f5-114">Перед разбиением полностью амортизированного актива статус журнала ОС должен быть изменен вручную с **Закрыто** на **Открыто**.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="3a5f5-115">Этот шаг необходим, поскольку статус книги должен быть **Открыто** , если необходимо разнести проводки для актива (например, для продажи выбытия).</span><span class="sxs-lookup"><span data-stu-id="3a5f5-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="3a5f5-116">После изменения статуса журнала ОС выполните следующие шаги, чтобы разделить актив.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="3a5f5-117">Найдите и выберите в списке ссылку на основное средство для разбиения.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="3a5f5-118">Выберите **Книги**.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-118">Select **Books**.</span></span> <span data-ttu-id="3a5f5-119">Выберите книгу для разбиения в новое основное средство.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="3a5f5-120">Выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-120">Select **Functions**.</span></span>
4. <span data-ttu-id="3a5f5-121">Выберите **Разбивка ОС**.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="3a5f5-122">В поле **В основные средства** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="3a5f5-123">В поле **В книгу** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3a5f5-124">В поле **Дата проводки** введите дату.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="3a5f5-125">В поле **Процент** введите число.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="3a5f5-126">В поле **Наименование журнала** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="3a5f5-127">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="3a5f5-128">Разноска проводки по журналу</span><span class="sxs-lookup"><span data-stu-id="3a5f5-128">Post the journal transaction</span></span>

1. <span data-ttu-id="3a5f5-129">В области перехода, перейдите к разделу **Модули \> Основные средства \> Записи журнала \> Журнал основных средств**.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="3a5f5-130">В списке выберите журнал, созданный в результате процесса разбиения.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="3a5f5-131">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-131">Select **Lines**.</span></span>

    - <span data-ttu-id="3a5f5-132">Проверьте созданные строки журнала.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="3a5f5-133">Проводка о корректировке приобретения создается для исходного основного средства для уменьшения стоимости на процент, указанный в процессе разбиения.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="3a5f5-134">Проводка приобретения создается для нового основного средства на ту же сумму.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="3a5f5-135">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="3a5f5-135">Select **Post**.</span></span>
