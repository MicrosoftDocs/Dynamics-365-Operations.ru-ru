--- 
title: "Назначение и переопределения налога"
description: "В этой процедуре показано, как назначить налоговые группы каналам розничной торговли."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8b3dc0beec17d80f7bbbcf234656a537a445789f
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="97c55-103">Назначение и переопределения налога</span><span class="sxs-lookup"><span data-stu-id="97c55-103">Sales tax assignment and overrides</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97c55-104">В этой процедуре показано, как назначить налоговые группы каналам розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="97c55-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="97c55-105">В ней также представлен процесс создания нового переопределения налога и его назначения существующей группе переопределений налога.</span><span class="sxs-lookup"><span data-stu-id="97c55-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="97c55-106">В этой процедуре</span><span class="sxs-lookup"><span data-stu-id="97c55-106">This procedure</span></span>

<span data-ttu-id="97c55-107">используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="97c55-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="97c55-108">Перейдите в раздел Розничная торговля и коммерция > Каналы > Магазины розничной торговли > Все розничные магазины.</span><span class="sxs-lookup"><span data-stu-id="97c55-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="97c55-109">В списке перейдите по ссылке "Код канала розничной торговли" для канала "Хьюстон".</span><span class="sxs-lookup"><span data-stu-id="97c55-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="97c55-110">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="97c55-110">Click Edit.</span></span>
    * <span data-ttu-id="97c55-111">В поле "Налоговая группа" содержится список налоговых групп для текущей компании.</span><span class="sxs-lookup"><span data-stu-id="97c55-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="97c55-112">Группа, назначенная в настоящее время, является универсальной налоговой группой "Техас".</span><span class="sxs-lookup"><span data-stu-id="97c55-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="97c55-113">Также имеются налоговые группы для "Вашингтон" и "Вашингтон, округ Кинг".</span><span class="sxs-lookup"><span data-stu-id="97c55-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="97c55-114">Налоговые группы могут включать применимые налоги для нескольких муниципалитетов.</span><span class="sxs-lookup"><span data-stu-id="97c55-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="97c55-115">В поле "Переопределение налога" можно сопоставить группы переопределений налога с каналом.</span><span class="sxs-lookup"><span data-stu-id="97c55-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="97c55-116">Группы переопределений налога можно использовать для группировки переопределений налога, которые работают для нескольких магазинов.</span><span class="sxs-lookup"><span data-stu-id="97c55-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="97c55-117">Вместо того, чтобы вручную назначать переопределения налога по одному, можно создать группу и назначить ее непосредственно каналам для экономии времени.</span><span class="sxs-lookup"><span data-stu-id="97c55-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="97c55-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="97c55-118">Click Save.</span></span>
5. <span data-ttu-id="97c55-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="97c55-119">Close the page.</span></span>
6. <span data-ttu-id="97c55-120">Перейдите в раздел "Розничная торговля и коммерция" > "Настройка канала" > "Налоги" > "Переопределение налогов".</span><span class="sxs-lookup"><span data-stu-id="97c55-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="97c55-121">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="97c55-121">Click New.</span></span>
8. <span data-ttu-id="97c55-122">В поле "Переопределение налога" введите имя нового переопределения.</span><span class="sxs-lookup"><span data-stu-id="97c55-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="97c55-123">В поле "Описание" введите описание переопределения.</span><span class="sxs-lookup"><span data-stu-id="97c55-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="97c55-124">Установите статус "Включено".</span><span class="sxs-lookup"><span data-stu-id="97c55-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="97c55-125">Разверните или сверните раздел "Переопределение".</span><span class="sxs-lookup"><span data-stu-id="97c55-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="97c55-126">В поле "Тип" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="97c55-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="97c55-127">Налоговые группы номенклатур можно использовать для переопределения налогов для конкретных номенклатур, которые принадлежат группе.</span><span class="sxs-lookup"><span data-stu-id="97c55-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="97c55-128">Например, продукты питания обычно облагаются налогом не так, как товары длительного пользования, и, вероятно, будут иметь собственную налоговую группу.</span><span class="sxs-lookup"><span data-stu-id="97c55-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="97c55-129">Налоговые группы — это группы налогов, которые применяются к определенному каналу.</span><span class="sxs-lookup"><span data-stu-id="97c55-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="97c55-130">Например, если канал продает в розницу и розничный канал и по схеме "предприятие-предприятие", могут использоваться различные налоговые группы номенклатур.</span><span class="sxs-lookup"><span data-stu-id="97c55-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="97c55-131">Все применимые налоги будут сопоставлены с налоговой группой.</span><span class="sxs-lookup"><span data-stu-id="97c55-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="97c55-132">Теперь можно выбрать налоги "Из" и "В" или "Начальная налоговая группа" и "Конечная налоговая группа" для создания переопределения налога.</span><span class="sxs-lookup"><span data-stu-id="97c55-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="97c55-133">В поле "Из" указывается налог или налоговая группа, которая должна быть переопределена.</span><span class="sxs-lookup"><span data-stu-id="97c55-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="97c55-134">При переопределении по налоговой группе номенклатур доступны другие параметры, чем при переопределении по налоговой группе.</span><span class="sxs-lookup"><span data-stu-id="97c55-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="97c55-135">Переопределения налога можно настроить для переопределения налогов во всех проводках или в определенных строках проводки.</span><span class="sxs-lookup"><span data-stu-id="97c55-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="97c55-136">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="97c55-136">Click Save.</span></span>
14. <span data-ttu-id="97c55-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="97c55-137">Close the page.</span></span>
15. <span data-ttu-id="97c55-138">Перейдите в раздел "Розничная торговля и коммерция" > "Настройка канала" > "Налоги" > "Группы переопределений налога".</span><span class="sxs-lookup"><span data-stu-id="97c55-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="97c55-139">На этом шаге вы назначите созданное переопределение налога группе переопределений налога, назначенной каналу "Хьюстон".</span><span class="sxs-lookup"><span data-stu-id="97c55-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="97c55-140">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="97c55-140">Click Edit.</span></span>
17. <span data-ttu-id="97c55-141">Разверните или сверните раздел "Настройка".</span><span class="sxs-lookup"><span data-stu-id="97c55-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="97c55-142">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="97c55-142">Click Add.</span></span>
19. <span data-ttu-id="97c55-143">В поле "Переопределение налога" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="97c55-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="97c55-144">Выберите ранее созданное переопределение налога из списка.</span><span class="sxs-lookup"><span data-stu-id="97c55-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="97c55-145">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="97c55-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="97c55-146">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="97c55-146">Click Save.</span></span>


