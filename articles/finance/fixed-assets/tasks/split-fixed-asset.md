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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db601be192b57fbec220193d3c9fde1a4f50c085
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213516"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="190ff-103">Разбивка ОС</span><span class="sxs-lookup"><span data-stu-id="190ff-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="190ff-104">В этой теме показано, как разделить процент одной модели стоимости основного средства в новую модель стоимости основного средства.</span><span class="sxs-lookup"><span data-stu-id="190ff-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="190ff-105">В нем используется роль бухгалтера и демонстрационные данные USMF.</span><span class="sxs-lookup"><span data-stu-id="190ff-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="190ff-106">Создание нового основного средства</span><span class="sxs-lookup"><span data-stu-id="190ff-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="190ff-107">В области перехода, перейдите к разделу **Модули \> Основные средства \> Основные средства \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="190ff-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="190ff-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="190ff-108">Select **New**.</span></span>
3. <span data-ttu-id="190ff-109">В поле **Группа ОС** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="190ff-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="190ff-110">Обратите внимание на номер основного средства для использования в процессе разбиения позже.</span><span class="sxs-lookup"><span data-stu-id="190ff-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="190ff-111">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="190ff-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="190ff-112">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="190ff-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="190ff-113">Разбивка ОС</span><span class="sxs-lookup"><span data-stu-id="190ff-113">Split a fixed asset</span></span>

<span data-ttu-id="190ff-114">Перед разбиением полностью амортизированного актива статус журнала ОС должен быть изменен вручную с **Закрыто** на **Открыто**.</span><span class="sxs-lookup"><span data-stu-id="190ff-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="190ff-115">Этот шаг необходим, поскольку статус книги должен быть **Открыто**, если необходимо разнести проводки для актива (например, для продажи выбытия).</span><span class="sxs-lookup"><span data-stu-id="190ff-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="190ff-116">Также необходимо включить параметр **Разрешить несколько проводок в одном ваучере** на вкладке **Общие** на странице **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="190ff-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="190ff-117">После изменения статуса книги активов и разрешения нескольких проводок в одном ваучере выполните следующие шаги, чтобы разделить актив.</span><span class="sxs-lookup"><span data-stu-id="190ff-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="190ff-118">Найдите и выберите в списке ссылку на основное средство для разбиения.</span><span class="sxs-lookup"><span data-stu-id="190ff-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="190ff-119">Выберите **Книги**.</span><span class="sxs-lookup"><span data-stu-id="190ff-119">Select **Books**.</span></span> <span data-ttu-id="190ff-120">Выберите книгу для разбиения в новое основное средство.</span><span class="sxs-lookup"><span data-stu-id="190ff-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="190ff-121">Выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="190ff-121">Select **Functions**.</span></span>
4. <span data-ttu-id="190ff-122">Выберите **Разбивка ОС**.</span><span class="sxs-lookup"><span data-stu-id="190ff-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="190ff-123">В поле **В основные средства** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="190ff-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="190ff-124">В поле **В книгу** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="190ff-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="190ff-125">В поле **Дата проводки** введите дату.</span><span class="sxs-lookup"><span data-stu-id="190ff-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="190ff-126">В поле **Процент** введите число.</span><span class="sxs-lookup"><span data-stu-id="190ff-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="190ff-127">В поле **Наименование журнала** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="190ff-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="190ff-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="190ff-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="190ff-129">Разноска проводки по журналу</span><span class="sxs-lookup"><span data-stu-id="190ff-129">Post the journal transaction</span></span>

1. <span data-ttu-id="190ff-130">В области перехода, перейдите к разделу **Модули \> Основные средства \> Записи журнала \> Журнал основных средств**.</span><span class="sxs-lookup"><span data-stu-id="190ff-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="190ff-131">В списке выберите журнал, созданный в результате процесса разбиения.</span><span class="sxs-lookup"><span data-stu-id="190ff-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="190ff-132">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="190ff-132">Select **Lines**.</span></span>

    - <span data-ttu-id="190ff-133">Проверьте созданные строки журнала.</span><span class="sxs-lookup"><span data-stu-id="190ff-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="190ff-134">Проводка о корректировке приобретения создается для исходного основного средства для уменьшения стоимости на процент, указанный в процессе разбиения.</span><span class="sxs-lookup"><span data-stu-id="190ff-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="190ff-135">Проводка приобретения создается для нового основного средства на ту же сумму.</span><span class="sxs-lookup"><span data-stu-id="190ff-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="190ff-136">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="190ff-136">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]