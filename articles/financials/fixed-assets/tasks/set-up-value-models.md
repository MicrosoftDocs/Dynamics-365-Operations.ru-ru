--- 
title: "Настройка книг"
description: "В этой процедуре показано, как создать новую модель стоимости основных средств и связать ее с группой ОС."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: b18f52254b9073cd95bf50539a4414598a8c19cc
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-books"></a><span data-ttu-id="e2d26-103">Настройка книг</span><span class="sxs-lookup"><span data-stu-id="e2d26-103">Set up books</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e2d26-104">В этой процедуре показано, как создать новую модель стоимости основных средств и связать ее с группой ОС.</span><span class="sxs-lookup"><span data-stu-id="e2d26-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="e2d26-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="e2d26-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="e2d26-106">Создайте книгу</span><span class="sxs-lookup"><span data-stu-id="e2d26-106">Create a book</span></span>
1. <span data-ttu-id="e2d26-107">Перейдите в раздел "Основные средства" > "Настройка" > "Книги".</span><span class="sxs-lookup"><span data-stu-id="e2d26-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="e2d26-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e2d26-108">Click New.</span></span>
3. <span data-ttu-id="e2d26-109">В поле "Книга" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e2d26-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="e2d26-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e2d26-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e2d26-111">Если установлен флажок "Расчет амортизации", связанная модель стоимости основных средств будет включена в предложения по амортизации.</span><span class="sxs-lookup"><span data-stu-id="e2d26-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="e2d26-112">В противном случае модель стоимости основных средств не будет амортизироваться автоматически.</span><span class="sxs-lookup"><span data-stu-id="e2d26-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="e2d26-113">Выберите значение "Да" в поле "Расчет амортизации".</span><span class="sxs-lookup"><span data-stu-id="e2d26-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="e2d26-114">В поле "Профиль амортизации" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e2d26-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="e2d26-115">Альтернативный метод амортизации также называется методом переключения амортизации.</span><span class="sxs-lookup"><span data-stu-id="e2d26-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="e2d26-116">Предложение по амортизации переключается на этот метод, когда альтернативный метод рассчитывает сумму амортизации, которая больше или равна методу амортизации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e2d26-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="e2d26-117">Метод дополнительной амортизации используется для дополнительной амортизации основного средства в необычных условиях.</span><span class="sxs-lookup"><span data-stu-id="e2d26-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="e2d26-118">Например, можно использовать это для записи амортизации в результате стихийного бедствия.</span><span class="sxs-lookup"><span data-stu-id="e2d26-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="e2d26-119">Если установлен флажок "Создание переоценки амортизации с основными поправками", корректировки амортизации создаются автоматически при обновлении стоимости основного средства.</span><span class="sxs-lookup"><span data-stu-id="e2d26-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="e2d26-120">В противном случае обновленная стоимость основного средства повлияет только на расчеты амортизации в будущем.</span><span class="sxs-lookup"><span data-stu-id="e2d26-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="e2d26-121">Выберите "Да" в поле "Создание переоценки амортизации с основными поправками".</span><span class="sxs-lookup"><span data-stu-id="e2d26-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="e2d26-122">По умолчанию проводки модели стоимости ОС разносятся в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="e2d26-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="e2d26-123">Можно отключить разноску в главную книгу для этой книги, установив в поле "Разносить в главную книгу" значение "Нет".</span><span class="sxs-lookup"><span data-stu-id="e2d26-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="e2d26-124">Книги, которые не разносятся в главную книгу, обычно используются для целей налоговой отчетности.</span><span class="sxs-lookup"><span data-stu-id="e2d26-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="e2d26-125">Это дает дополнительную гибкость для удаления исторических проводок из модели стоимости ОС, поскольку они не фиксируются в главной книге.</span><span class="sxs-lookup"><span data-stu-id="e2d26-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="e2d26-126">Поле "Слой разноски" по умолчанию имеет значение "Текущий слой", если книга разносится в главную книгу, или значение "Нет", если она не разносится в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="e2d26-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="e2d26-127">Обновите поле "Слой разноски", если требуется разнести проводки для данной книги на другой слой.</span><span class="sxs-lookup"><span data-stu-id="e2d26-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="e2d26-128">В поле "Календарь" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e2d26-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="e2d26-129">Производные книги будут разносить проводки по различным книгам одновременно.</span><span class="sxs-lookup"><span data-stu-id="e2d26-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="e2d26-130">Вы создаете проводки в основной книге, и во время разноски точные копии проводки разносятся в производной книге.</span><span class="sxs-lookup"><span data-stu-id="e2d26-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="e2d26-131">Пересчет с использованием проводок в производной книге не производится, поэтому она не должна использоваться для проводок амортизации.</span><span class="sxs-lookup"><span data-stu-id="e2d26-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="e2d26-132">Связь книги с группой основных средств</span><span class="sxs-lookup"><span data-stu-id="e2d26-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="e2d26-133">Щелкните "Группы ОС".</span><span class="sxs-lookup"><span data-stu-id="e2d26-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="e2d26-134">В поле "Группа ОС" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e2d26-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="e2d26-135">В поле "Срок службы" введите число.</span><span class="sxs-lookup"><span data-stu-id="e2d26-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="e2d26-136">Обратите внимание, что поле "Периоды амортизации" рассчитывается после задания срока службы.</span><span class="sxs-lookup"><span data-stu-id="e2d26-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="e2d26-137">Можно настроить соглашение по амортизации, требуемое для налогообложения.</span><span class="sxs-lookup"><span data-stu-id="e2d26-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  


