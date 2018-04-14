---
title: "Отображение страниц рядом друг с другом с помощью значка \"Открыть в новом окне\""
description: "Эта статья описывает способ отображения страницы в двухколоночном формате в Microsoft Dynamics 365 for Finance and Operations."
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f19ca5e9642b5a8222ee7bf23fdd228ab75d2ed1
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a><span data-ttu-id="5a84c-103">Отображение страниц рядом друг с другом с помощью значка "Открыть в новом окне"</span><span class="sxs-lookup"><span data-stu-id="5a84c-103">Display pages side-by-side using the Open in New Window icon</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="5a84c-104">Эта статья описывает способ отображения страницы в двухколоночном формате в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5a84c-104">This article explains how to display pages side-by-side in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="5a84c-105">Microsoft Dynamics 365 for Finance and Operations помогает эффективно выполнять задачи.</span><span class="sxs-lookup"><span data-stu-id="5a84c-105">Microsoft Dynamics 365 for Finance and Operations helps you perform tasks efficiently.</span></span> <span data-ttu-id="5a84c-106">В некоторых случаях может потребоваться просмотреть несколько страниц рядом, чтобы быстро завершить задачу.</span><span class="sxs-lookup"><span data-stu-id="5a84c-106">In some cases, you may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="5a84c-107">Например, может потребоваться проверить или ввести строки в несколько журналов.</span><span class="sxs-lookup"><span data-stu-id="5a84c-107">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="5a84c-108">Обычно для этого потребовалось бы переходить между страницей, на которой представлен список журналов, и страницей, на которой представлены строки определенного журнала.</span><span class="sxs-lookup"><span data-stu-id="5a84c-108">Typically, to do this you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="5a84c-109">Однако с помощью функции **Открыть в новом окне** можно отобразить эти страницы рядом, чтобы быстрее выполнить задачи.</span><span class="sxs-lookup"><span data-stu-id="5a84c-109">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span> 

<span data-ttu-id="5a84c-110">В указанном выше примере при просмотре строк можно щелкнуть значок **Открыть в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="5a84c-110">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span> 

<span data-ttu-id="5a84c-111">[![значок открытия в новом окне](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="5a84c-111">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span> 

<span data-ttu-id="5a84c-112">При щелчке значка **Открыть в новом окне** открывается страница строк в новом всплывающем браузере, после чего открывается исходный браузер в истории страницы, на которой отображается список журналов.</span><span class="sxs-lookup"><span data-stu-id="5a84c-112">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="5a84c-113">После этого можно отобразить обе страницы рядом.</span><span class="sxs-lookup"><span data-stu-id="5a84c-113">You can then display both pages side-by-side.</span></span> <span data-ttu-id="5a84c-114">По завершении просмотра журнала можно изменить выбранный журнал на страницу списка журнала, чтобы на странице строк во всплывающем окне автоматически отобразились строки нового выбранного журнала.</span><span class="sxs-lookup"><span data-stu-id="5a84c-114">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span> 

<span data-ttu-id="5a84c-115">[![страницы рядом друг с другом](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="5a84c-115">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span> 

<span data-ttu-id="5a84c-116">Динамическая привязка и обновление выполняются на основании отношений, существующих между данными, поддерживающими эти страницы.</span><span class="sxs-lookup"><span data-stu-id="5a84c-116">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="5a84c-117">Если система не знает об отношении между данными, то всплывающее окно не обновится автоматически в ответ на изменение в окне-источнике.</span><span class="sxs-lookup"><span data-stu-id="5a84c-117">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span> 

<span data-ttu-id="5a84c-118">Некоторые страницы имеют несколько представлений, например "Сетка", "Заголовок" и "Сведения".</span><span class="sxs-lookup"><span data-stu-id="5a84c-118">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="5a84c-119">При щелчке значка **Открыть в новом окне** открывается вся страница в новом окне браузера.</span><span class="sxs-lookup"><span data-stu-id="5a84c-119">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="5a84c-120">Поэтому невозможно открыть два представления одной страницы рядом с помощью функции **Открыть в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="5a84c-120">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="5a84c-121">Однако почти все такие страницы имеют список навигации, который можно использовать для переключения между записями и получения похожей функциональности.</span><span class="sxs-lookup"><span data-stu-id="5a84c-121">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span> 

<span data-ttu-id="5a84c-122">Перед использованием функции **Открыть в новом окне** необходимо настроить блокировщик всплывающих окон браузера так, чтобы он разрешал всплывающие окна по URL-адресам сайта Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5a84c-122">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the Finance and Operations site.</span></span> <span data-ttu-id="5a84c-123">Например, можно разрешить всплывающие окна с URL-адреса "\*.dynamics.com".</span><span class="sxs-lookup"><span data-stu-id="5a84c-123">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span> 

<span data-ttu-id="5a84c-124">Функция **Открыть в новом окне** доступна, только если в окне открыто несколько страниц.</span><span class="sxs-lookup"><span data-stu-id="5a84c-124">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="5a84c-125">Кроме того, всплывающее окно закрывается автоматически, если больше нет открытых страниц (то есть, когда закрывается последняя страница в этом окне).</span><span class="sxs-lookup"><span data-stu-id="5a84c-125">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="5a84c-126">Finance and Operations также закрывает открытые страницы, когда вы переходите в другую область приложения.</span><span class="sxs-lookup"><span data-stu-id="5a84c-126">Finance and Operations also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="5a84c-127">Поэтому, если открыты всплывающие окна и выполняется переход к другой области в приложении, всплывающие окна закрываются автоматически, поскольку страницы в этих окнах были закрыты системой.</span><span class="sxs-lookup"><span data-stu-id="5a84c-127">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span> 

<span data-ttu-id="5a84c-128">На верхней панели во всплывающих окнах отображается доступная только для чтения информация о компании, в которой была открыта страница.</span><span class="sxs-lookup"><span data-stu-id="5a84c-128">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="5a84c-129">Всплывающие окна также зависят от основного окна браузера Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5a84c-129">The pop-up windows also rely on the main Finance and Operations browser window.</span></span> <span data-ttu-id="5a84c-130">Если главное окно зарывается или обновляется, все открытые всплывающие окна становятся доступными только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5a84c-130">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="5a84c-131">Это означает, что можно по-прежнему просматривать информацию в этих окнах, но невозможно взаимодействовать с ней.</span><span class="sxs-lookup"><span data-stu-id="5a84c-131">This means that you can still view the information in these windows, but you will not be able to interact with it.</span></span>




