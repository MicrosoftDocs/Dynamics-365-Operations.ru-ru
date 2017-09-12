--- 
title: "Обработка корректировок баллов поощрения по программе лояльности"
description: "Эта процедура показывает, как искать данные карточки постоянного клиента и корректировать баллы поощрения лояльности."
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 44e406c8869ec376858f1a9312d533029a534c09
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="96b91-103">Обработка корректировок баллов поощрения по программе лояльности</span><span class="sxs-lookup"><span data-stu-id="96b91-103">Process loyalty reward point adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="96b91-104">Эта процедура показывает, как искать данные карточки постоянного клиента и корректировать баллы поощрения лояльности.</span><span class="sxs-lookup"><span data-stu-id="96b91-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="96b91-105">В качестве компании с демонстрационными данными для создания этой задачи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="96b91-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="96b91-106">Эта задача назначена для роли директора-распорядителя в розничной торговле или менеджера по обслуживанию клиентов.</span><span class="sxs-lookup"><span data-stu-id="96b91-106">This task is intended for the Retail operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="96b91-107">Перейдите в раздел "Карты лояльности".</span><span class="sxs-lookup"><span data-stu-id="96b91-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="96b91-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="96b91-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="96b91-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="96b91-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="96b91-110">Щелкните "Проводки по карте".</span><span class="sxs-lookup"><span data-stu-id="96b91-110">Click Card transactions.</span></span>
    * <span data-ttu-id="96b91-111">На этой странице можно просмотреть все проводки программы лояльности для выбранной карточки постоянного клиента.</span><span class="sxs-lookup"><span data-stu-id="96b91-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="96b91-112">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="96b91-112">Close the page.</span></span>
6. <span data-ttu-id="96b91-113">Щелкните "Корректировки по карте".</span><span class="sxs-lookup"><span data-stu-id="96b91-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="96b91-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="96b91-114">Click New.</span></span>
8. <span data-ttu-id="96b91-115">В поле "Точки вознаграждения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="96b91-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="96b91-116">В поле "Сумма или количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="96b91-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="96b91-117">Можно добавлять или удалять баллы из карточки постоянного клиента с помощью него положительных и отрицательных значений.</span><span class="sxs-lookup"><span data-stu-id="96b91-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="96b91-118">В поле "Программа лояльности" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="96b91-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="96b91-119">В поле "Комментарий" введите значение.</span><span class="sxs-lookup"><span data-stu-id="96b91-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="96b91-120">Щелкните "Разноска корректировки".</span><span class="sxs-lookup"><span data-stu-id="96b91-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="96b91-121">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="96b91-121">Click Yes.</span></span>
14. <span data-ttu-id="96b91-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="96b91-122">Close the page.</span></span>
    * <span data-ttu-id="96b91-123">Обычно на этом этапе можно обновить страницу, чтобы увидеть результаты корректировки баллов поощрения на вкладке "Сводка баллов поощрений".</span><span class="sxs-lookup"><span data-stu-id="96b91-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab.</span></span> <span data-ttu-id="96b91-124">Но если вы выполняете это руководство по задаче, не обновляйте страницу сейчас, поскольку в этом случае выполнение руководства по задаче остановится.</span><span class="sxs-lookup"><span data-stu-id="96b91-124">But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="96b91-125">Щелкните "Проводки по карте".</span><span class="sxs-lookup"><span data-stu-id="96b91-125">Click Card transactions.</span></span>
16. <span data-ttu-id="96b91-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="96b91-126">Close the page.</span></span>


