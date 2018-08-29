--- 
title: "Создание коммерческих соглашений с помощью правил ценообразования категорий"
description: "Эта процедура демонстрирует способ создания коммерческих соглашения по ценам продажи с использованием правила ценообразования категории."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 20393f80c8f4aa12e3103cb7df214367aa35ab16
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---
# <a name="create-trade-agreements-by-using-category-pricing-rules"></a><span data-ttu-id="b087c-103">Создание коммерческих соглашений с помощью правил ценообразования категорий</span><span class="sxs-lookup"><span data-stu-id="b087c-103">Create trade agreements by using category pricing rules</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b087c-104">Эта процедура демонстрирует способ создания коммерческих соглашения по ценам продажи с использованием правила ценообразования категории.</span><span class="sxs-lookup"><span data-stu-id="b087c-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="b087c-105">В качестве компании с демонстрационными данными для создания этой задачи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="b087c-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="b087c-106">Эта задача предназначена для роли Директора по сбыту в розничной торговле.</span><span class="sxs-lookup"><span data-stu-id="b087c-106">This task is intended for the Retail merchandising manager role.</span></span>

1. <span data-ttu-id="b087c-107">Щелкните "Управление ценообразованием и скидками".</span><span class="sxs-lookup"><span data-stu-id="b087c-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="b087c-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b087c-108">Click New.</span></span>
3. <span data-ttu-id="b087c-109">Щелкните "Правило цены категории".</span><span class="sxs-lookup"><span data-stu-id="b087c-109">Click Category price rule.</span></span>
4. <span data-ttu-id="b087c-110">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b087c-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="b087c-111">В поле "Код счета" выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b087c-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="b087c-112">Для настройки коммерческих соглашений по ценам продажи, специфичных для каналов, программ лояльности, каталогов и назначений, используется код счета типа "Группа".</span><span class="sxs-lookup"><span data-stu-id="b087c-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="b087c-113">В поле "Выбор счета" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b087c-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="b087c-114">В поле "Категория" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b087c-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="b087c-115">В поле "Сумма/процент" введите число.</span><span class="sxs-lookup"><span data-stu-id="b087c-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="b087c-116">В поле "Версия округления" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b087c-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="b087c-117">Щелкните "Создать коммерческие соглашения".</span><span class="sxs-lookup"><span data-stu-id="b087c-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="b087c-118">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="b087c-118">Click Next.</span></span>
12. <span data-ttu-id="b087c-119">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="b087c-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="b087c-120">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="b087c-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="b087c-121">Выберите значение "Да" в поле "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="b087c-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="b087c-122">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="b087c-122">Click Next.</span></span>
16. <span data-ttu-id="b087c-123">Нажмите кнопку Готово.</span><span class="sxs-lookup"><span data-stu-id="b087c-123">Click Finish.</span></span>
    * <span data-ttu-id="b087c-124">При этом создается журнал коммерческих соглашений и открывается для вашего просмотра.</span><span class="sxs-lookup"><span data-stu-id="b087c-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="b087c-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b087c-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b087c-126">Журналы коммерческих соглашений, созданные из правил ценообразования категории, не разносятся.</span><span class="sxs-lookup"><span data-stu-id="b087c-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="b087c-127">Вы можете просматривать и изменять созданные цены перед их разноской.</span><span class="sxs-lookup"><span data-stu-id="b087c-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="b087c-128">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="b087c-128">Click Edit.</span></span>
19. <span data-ttu-id="b087c-129">В поле "Сумма в валюте" введите число.</span><span class="sxs-lookup"><span data-stu-id="b087c-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="b087c-130">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="b087c-130">Click Post.</span></span>
21. <span data-ttu-id="b087c-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b087c-131">Click OK.</span></span>
22. <span data-ttu-id="b087c-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b087c-132">Close the page.</span></span>
23. <span data-ttu-id="b087c-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b087c-133">Close the page.</span></span>
24. <span data-ttu-id="b087c-134">Щелкните вкладку "Правила цены категории".</span><span class="sxs-lookup"><span data-stu-id="b087c-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="b087c-135">В этом списке будут отображаться правила ценообразования категории, относящиеся к каналу.</span><span class="sxs-lookup"><span data-stu-id="b087c-135">Channel specific Category pricing rules will show in this list.</span></span>  


