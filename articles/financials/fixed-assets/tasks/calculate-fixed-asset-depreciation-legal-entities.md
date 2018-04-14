--- 
title: "Расчет амортизации ОС в разных юридических лицах"
description: "Эта процедура показывает, как настроить и запустить процесс амортизации для нескольких юридических лиц."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 662554b1b6bed63e5017aad3a292dad7a2f0bcea
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="65933-103">Расчет амортизации ОС в разных юридических лицах</span><span class="sxs-lookup"><span data-stu-id="65933-103">Calculate fixed asset depreciation across legal entities</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="65933-104">Можно запустить амортизации основных средств для нескольких юридических лиц за один шаг.</span><span class="sxs-lookup"><span data-stu-id="65933-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="65933-105">Эта процедура показывает, как настроить и запустить процесс для нескольких юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="65933-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="65933-106">Она использует роль бухгалтера.</span><span class="sxs-lookup"><span data-stu-id="65933-106">It uses the accountant role.</span></span>  

<span data-ttu-id="65933-107">В данной записи используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="65933-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="65933-108">Подзадача действий (16): настроить журналы запуска амортизации по нескольким компаниям.</span><span class="sxs-lookup"><span data-stu-id="65933-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="65933-109">Сначала в каждом юридическом лице необходимо настроить журналы для использования при выполнении амортизации в нескольких компаниях.</span><span class="sxs-lookup"><span data-stu-id="65933-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="65933-110">Перейдите в раздел "Основные средства" > "Настройка" > "Параметры основных средств".</span><span class="sxs-lookup"><span data-stu-id="65933-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="65933-111">Разверните раздел "Предложения по ОС".</span><span class="sxs-lookup"><span data-stu-id="65933-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="65933-112">Создайте запись с именем журнала, который должен использоваться для каждого слоя разноски в юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="65933-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="65933-113">Если книги не разносятся в главную книгу, следует выбрать слой разноски "Нет" со связанным журналом.</span><span class="sxs-lookup"><span data-stu-id="65933-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="65933-114">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="65933-114">Click Add.</span></span> 
4. <span data-ttu-id="65933-115">В поле "Слой разноски" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="65933-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="65933-116">В поле "Наименование журнала" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="65933-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="65933-117">Повторите настройку журнала на странице "Параметры основных средств" в каждом юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="65933-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="65933-118">Подзадача: расчет амортизации</span><span class="sxs-lookup"><span data-stu-id="65933-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="65933-119">Используйте страницу "Создать предложение по амортизации" для запуска выполнения амортизации для нескольких юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="65933-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="65933-120">Перейдите в раздел "Основные средства" > "Записи в журнале" > "Создать предложение по амортизации".</span><span class="sxs-lookup"><span data-stu-id="65933-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="65933-121">В поле "Слой разноски" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="65933-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="65933-122">Имя журнала по умолчанию берется из параметров основных средств.</span><span class="sxs-lookup"><span data-stu-id="65933-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="65933-123">Его можно изменить здесь для текущего юридического лица.</span><span class="sxs-lookup"><span data-stu-id="65933-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="65933-124">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="65933-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="65933-125">Выберите юридические лица для включения в прогон амортизации.</span><span class="sxs-lookup"><span data-stu-id="65933-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="65933-126">В списке будут отображаться только юридические лица с журналами, настроенными для предложений ОС на странице "Параметры основных средств".</span><span class="sxs-lookup"><span data-stu-id="65933-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="65933-127">Если параметр "Разнести журналы" включен, при создании журналов амортизации они будут автоматически разноситься.</span><span class="sxs-lookup"><span data-stu-id="65933-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="65933-128">Если этот параметр не выбран, журналы будут созданы, но не будут разнесены, чтобы можно было просматривать информацию перед разноской.</span><span class="sxs-lookup"><span data-stu-id="65933-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="65933-129">В поле "Разнести журналы" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="65933-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="65933-130">Поля фильтрации включают все основные средства, группы и книги для юридических лиц, выбранных для этого прогона амортизации.</span><span class="sxs-lookup"><span data-stu-id="65933-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="65933-131">Параметр пакетной обработки по умолчанию включен.</span><span class="sxs-lookup"><span data-stu-id="65933-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="65933-132">Если этот параметр включен, создание и разноска журнала амортизации будут выполняться в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="65933-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="65933-133">Щелкните "Создать журнал".</span><span class="sxs-lookup"><span data-stu-id="65933-133">Click Create journal.</span></span> 
10. <span data-ttu-id="65933-134">Необходимо просмотреть журналы амортизации, созданные в соответствующих юридических лицах.</span><span class="sxs-lookup"><span data-stu-id="65933-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="65933-135">Перейдите в раздел "Основные средства" > "Записи в журнале" > "Журнал основных средств".</span><span class="sxs-lookup"><span data-stu-id="65933-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

