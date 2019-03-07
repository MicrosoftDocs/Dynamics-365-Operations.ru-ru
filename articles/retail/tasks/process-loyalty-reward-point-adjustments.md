---
title: Обработка корректировок баллов поощрения по программе лояльности
description: Эта процедура показывает, как искать данные карточки постоянного клиента и корректировать баллы поощрения лояльности.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85aaa82bf56d55c69f39bab49682c79f51247251
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "346165"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="ce620-103">Обработка корректировок баллов поощрения по программе лояльности</span><span class="sxs-lookup"><span data-stu-id="ce620-103">Process loyalty reward point adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ce620-104">Эта процедура показывает, как искать данные карточки постоянного клиента и корректировать баллы поощрения лояльности.</span><span class="sxs-lookup"><span data-stu-id="ce620-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="ce620-105">В качестве компании с демонстрационными данными для создания этой задачи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="ce620-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="ce620-106">Эта задача назначена для роли директора-распорядителя в розничной торговле или менеджера по обслуживанию клиентов.</span><span class="sxs-lookup"><span data-stu-id="ce620-106">This task is intended for the Retail operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="ce620-107">Перейдите в раздел "Карты лояльности".</span><span class="sxs-lookup"><span data-stu-id="ce620-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="ce620-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ce620-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ce620-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ce620-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ce620-110">Щелкните "Проводки по карте".</span><span class="sxs-lookup"><span data-stu-id="ce620-110">Click Card transactions.</span></span>
    * <span data-ttu-id="ce620-111">На этой странице можно просмотреть все проводки программы лояльности для выбранной карточки постоянного клиента.</span><span class="sxs-lookup"><span data-stu-id="ce620-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="ce620-112">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ce620-112">Close the page.</span></span>
6. <span data-ttu-id="ce620-113">Щелкните "Корректировки по карте".</span><span class="sxs-lookup"><span data-stu-id="ce620-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="ce620-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ce620-114">Click New.</span></span>
8. <span data-ttu-id="ce620-115">В поле "Точки вознаграждения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ce620-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="ce620-116">В поле "Сумма или количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="ce620-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="ce620-117">Можно добавлять или удалять баллы из карточки постоянного клиента с помощью него положительных и отрицательных значений.</span><span class="sxs-lookup"><span data-stu-id="ce620-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="ce620-118">В поле "Программа лояльности" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ce620-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="ce620-119">В поле "Комментарий" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ce620-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="ce620-120">Щелкните "Разноска корректировки".</span><span class="sxs-lookup"><span data-stu-id="ce620-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="ce620-121">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="ce620-121">Click Yes.</span></span>
14. <span data-ttu-id="ce620-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ce620-122">Close the page.</span></span>
    * <span data-ttu-id="ce620-123">Обычно на этом этапе можно обновить страницу, чтобы увидеть результаты корректировки баллов поощрения на вкладке "Сводка баллов поощрений". Но если вы выполняете это руководство по задаче, не обновляйте страницу сейчас, поскольку в этом случае выполнение руководства по задаче остановится.</span><span class="sxs-lookup"><span data-stu-id="ce620-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="ce620-124">Щелкните "Проводки по карте".</span><span class="sxs-lookup"><span data-stu-id="ce620-124">Click Card transactions.</span></span>
16. <span data-ttu-id="ce620-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ce620-125">Close the page.</span></span>

