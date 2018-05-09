---
title: "Поиск действий"
description: "В этой статье описываются функции поиска действий в Microsoft Dynamics 365 for Finance and Operations. Поиск действий служит для поиска и выполнения действий на странице."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6f623c5fc9b277933c4655101fe451c87a1e5224
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="action-search"></a><span data-ttu-id="de5ee-104">Поиск действий</span><span class="sxs-lookup"><span data-stu-id="de5ee-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de5ee-105">В этой статье описываются функции поиска действий в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="de5ee-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="de5ee-106">Поиск действий служит для поиска и выполнения действий на странице.</span><span class="sxs-lookup"><span data-stu-id="de5ee-106">Action search will help you find and run actions on a page.</span></span>

<a name="introduction"></a><span data-ttu-id="de5ee-107">Приветствие</span><span class="sxs-lookup"><span data-stu-id="de5ee-107">Introduction</span></span>
------------

<span data-ttu-id="de5ee-108">Страницы в Microsoft Dynamics 365 for Finance and Operations в первую очередь предоставляют команды на панелях операций, как в стандартной области действий, которая появляется в верхней части страницы, так и на панелях инструментов, которые отображаются в различных разделах страницы.</span><span class="sxs-lookup"><span data-stu-id="de5ee-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="de5ee-109">В предыдущих версиях функция сочетаний клавиш позволяла быстро получить доступ к любой кнопке на панели операций, нажав клавишу Alt, затем последовательность букв.</span><span class="sxs-lookup"><span data-stu-id="de5ee-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span> 

<span data-ttu-id="de5ee-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) Однако в текущей версии Finance and Operations сочетания клавиш становятся недоступны, они были заменены функцией поиска действия.</span><span class="sxs-lookup"><span data-stu-id="de5ee-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="de5ee-111">Эта новая функция позволяет быстро искать и наживать кнопки на любой видимой панели операций.</span><span class="sxs-lookup"><span data-stu-id="de5ee-111">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="de5ee-112">Использование поиска действий</span><span class="sxs-lookup"><span data-stu-id="de5ee-112">Using action search</span></span>
<span data-ttu-id="de5ee-113">Для использования функции поиска действий выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="de5ee-113">To use the action search feature, follow these steps.</span></span>

1.  <span data-ttu-id="de5ee-114">На панели операций щелкните в поле **поиска действий**.</span><span class="sxs-lookup"><span data-stu-id="de5ee-114">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="de5ee-115">(В поле **поиска действий** находится значок в виде лупы.)</span><span class="sxs-lookup"><span data-stu-id="de5ee-115">(The **action search** field contains a magnifying glass icon.)</span></span>
2.  <span data-ttu-id="de5ee-116">Введите все имя или часть имени кнопки, которую требуется выполнить.</span><span class="sxs-lookup"><span data-stu-id="de5ee-116">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="de5ee-117">Можно также выполнять поиск, используя слова из "пути" кнопки.</span><span class="sxs-lookup"><span data-stu-id="de5ee-117">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="de5ee-118">(Дополнительные сведения см. в следующем разделе этой статьи.) Как правило, кнопка появится в верхней части списка результатов после того, как вы введете от двух до четырех символов.</span><span class="sxs-lookup"><span data-stu-id="de5ee-118">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3.  <span data-ttu-id="de5ee-119">Найдите и нажмите кнопку в результатах (с помощью мыши или клавиатуры).</span><span class="sxs-lookup"><span data-stu-id="de5ee-119">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="de5ee-120">После нажатия кнопки фокус возвращается туда, где вы до этого находились на странице, чтобы вы могли продолжить работу.</span><span class="sxs-lookup"><span data-stu-id="de5ee-120">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span> 

<span data-ttu-id="de5ee-121">[![поле-поиска-действия](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="de5ee-121">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="de5ee-122">Запустить поиск действий можно также путем нажатия сочетаний клавиш Ctrl+/ или Alt+Q.</span><span class="sxs-lookup"><span data-stu-id="de5ee-122">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="de5ee-123">Нажмите сочетание клавиш еще раз, чтобы фокус вернулся на то место на странице, где вы раньше находились.</span><span class="sxs-lookup"><span data-stu-id="de5ee-123">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="de5ee-124">Что представляет собой список результатов</span><span class="sxs-lookup"><span data-stu-id="de5ee-124">Understanding the results list</span></span>
<span data-ttu-id="de5ee-125">Как правило в Finance and Operations необходимо знать местонахождение и контекст кнопки, чтобы полностью понимать назначение этой кнопки.</span><span class="sxs-lookup"><span data-stu-id="de5ee-125">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="de5ee-126">Поэтому для каждого элемента в списке результатов отображаются дополнительные сведения, чтобы точно понимать, какие кнопки отображаются в списке.</span><span class="sxs-lookup"><span data-stu-id="de5ee-126">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="de5ee-127">В частности, отображается "путь" к кнопке.</span><span class="sxs-lookup"><span data-stu-id="de5ee-127">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="de5ee-128">В этот путь могут входить метки следующих элементов пользовательского интерфейса:</span><span class="sxs-lookup"><span data-stu-id="de5ee-128">This path might include the labels of the following UI elements, as relevant:</span></span>

-   <span data-ttu-id="de5ee-129">Вкладка панели операций</span><span class="sxs-lookup"><span data-stu-id="de5ee-129">Action Pane tab</span></span>
-   <span data-ttu-id="de5ee-130">Группа кнопок</span><span class="sxs-lookup"><span data-stu-id="de5ee-130">Button group</span></span>
-   <span data-ttu-id="de5ee-131">Кнопка меню (если кнопка находится внутри кнопки меню)</span><span class="sxs-lookup"><span data-stu-id="de5ee-131">Menu button (if the button is inside a menu button)</span></span>
-   <span data-ttu-id="de5ee-132">Разделитель меню (если кнопка находится внутри именованной группы внутри кнопки меню)</span><span class="sxs-lookup"><span data-stu-id="de5ee-132">Menu separator (if the button is inside a named group inside a menu button)</span></span>
-   <span data-ttu-id="de5ee-133">Группа или вкладка на странице (например, имя экспресс-вкладки)</span><span class="sxs-lookup"><span data-stu-id="de5ee-133">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="de5ee-134">Предположим, что вы ввели в поле **поиска действий** буквы **ито** и теперь изучаете список результатов.</span><span class="sxs-lookup"><span data-stu-id="de5ee-134">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="de5ee-135">Первая запись для кнопки с именем **Итоги** выделяется.</span><span class="sxs-lookup"><span data-stu-id="de5ee-135">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="de5ee-136">Также отображается путь к кнопке: **Заказ на продажу** &gt; **Просмотр**.</span><span class="sxs-lookup"><span data-stu-id="de5ee-136">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="de5ee-137">Часть пути **Заказ на продажу** соответствует вкладке **Заказ на продажу** в области действий, а часть пути **Просмотр** соответствует группе **Просмотр** на этой вкладке. Аналогичным образом путь кнопки **Общая скидка** (**Продажа** &gt; **Рассчитать**) сообщает, что эта кнопка находится в группе **Рассчитать** на вкладке **Продажа** панели операций.</span><span class="sxs-lookup"><span data-stu-id="de5ee-137">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="de5ee-138">Таким образом, эта информация помогает точно определить, какая кнопка будет запущена поиском действия (если выбрать эту кнопку в списке результатов).</span><span class="sxs-lookup"><span data-stu-id="de5ee-138">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span> 

<span data-ttu-id="de5ee-139">[![поле-поиска-действия-с-данными](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="de5ee-139">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span> 

<span data-ttu-id="de5ee-140">В предыдущем примере поиск действия показал результаты из стандартной панели действий в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="de5ee-140">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="de5ee-141">Однако поиск действий показывает также результаты с видимых панелей инструментов, которые находятся в других местах на странице.</span><span class="sxs-lookup"><span data-stu-id="de5ee-141">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="de5ee-142">Например, нужно найти кнопку **Запасы в наличии**, расположенную на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="de5ee-142">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="de5ee-143">В данном случае путь кнопки, указанный в списке результатов (**Строки заказа на продажу** &gt; **Запасы** &gt; **Просмотр**), проинформирует вас о том, что эта кнопка находится под заголовком **Просмотр** на кнопке меню **Запасы** на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="de5ee-143">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span> 

<span data-ttu-id="de5ee-144">[![запасы-в-наличии](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="de5ee-144">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="de5ee-145">Поиск действий и навигационный поиск</span><span class="sxs-lookup"><span data-stu-id="de5ee-145">Action search vs. Navigation search</span></span>
<span data-ttu-id="de5ee-146">Тогда как поиск действий предназначен для поиска и запуска операций на странице, для поиска страниц в Finance and Operations и перехода к ним предусмотрен другой поисковый механизм.</span><span class="sxs-lookup"><span data-stu-id="de5ee-146">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="de5ee-147">Дополнительные сведения об этой функции см. в статье [Навигационный поиск](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="de5ee-147">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>




