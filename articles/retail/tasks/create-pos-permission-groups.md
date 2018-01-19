--- 
title: "Создание групп разрешений POS"
description: "В этой процедуре показано, как создать группу разрешений POS."
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
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
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 3a1eb7d3137a4cf8105f6c3135eafcb1b8d6d0ce
ms.contentlocale: ru-ru
ms.lasthandoff: 01/19/2018

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="5d2ae-103">Создание групп разрешений POS</span><span class="sxs-lookup"><span data-stu-id="5d2ae-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5d2ae-104">В этой процедуре показано, как создать группу разрешений POS.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="5d2ae-105">В качестве компании с демонстрационными данными для создания этой задачи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="5d2ae-106">Эта задача предназначена для роли директора-распорядителя в розничной торговле.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="5d2ae-107">Перейдите в раздел "Группы разрешений".</span><span class="sxs-lookup"><span data-stu-id="5d2ae-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="5d2ae-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="5d2ae-108">Click New.</span></span>
3. <span data-ttu-id="5d2ae-109">В поле "ИД группы POS-разрешений" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="5d2ae-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5d2ae-111">Выберите "Да" в поле "Просмотр записей часов".</span><span class="sxs-lookup"><span data-stu-id="5d2ae-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="5d2ae-112">Теперь можно активировать или деактивировать различные разрешения для группы разрешений POS.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="5d2ae-113">Для некоторых разрешений можно установить значение, которое будет использоваться для проверки того, может ли пользователь терминала выполнять определенное действие.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="5d2ae-114">В этом руководстве по задачам включено несколько разрешение, которые можно предоставить кассиру.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="5d2ae-115">Выберите "Да" в поле "Разрешить создание заказа".</span><span class="sxs-lookup"><span data-stu-id="5d2ae-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="5d2ae-116">Выберите "Да" в поле "Разрешить изменение заказа".</span><span class="sxs-lookup"><span data-stu-id="5d2ae-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="5d2ae-117">Выберите "Да" в поле "Разрешить получение заказа".</span><span class="sxs-lookup"><span data-stu-id="5d2ae-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="5d2ae-118">Выберите "Да" в поле "Разрешить изменение пароля".</span><span class="sxs-lookup"><span data-stu-id="5d2ae-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="5d2ae-119">Выберите "Да" в поле «Разрешить закрытие "вслепую"».</span><span class="sxs-lookup"><span data-stu-id="5d2ae-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="5d2ae-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5d2ae-120">Click Save.</span></span>
    * <span data-ttu-id="5d2ae-121">После сохранения изменений необходимо запустить график распределения персонала, чтобы передать изменения в розничные каналы.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="5d2ae-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-122">Close the page.</span></span>
13. <span data-ttu-id="5d2ae-123">Перейти в раздел "Задания".</span><span class="sxs-lookup"><span data-stu-id="5d2ae-123">Go to Jobs.</span></span>
    * <span data-ttu-id="5d2ae-124">Теперь мы назначим группы разрешения POS заданию.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="5d2ae-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="5d2ae-126">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="5d2ae-127">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-127">Click Edit.</span></span>
17. <span data-ttu-id="5d2ae-128">Разверните раздел "Классификация задний".</span><span class="sxs-lookup"><span data-stu-id="5d2ae-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="5d2ae-129">В поле "Группа POS-разрешений" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="5d2ae-130">Все работники на должностях для этого задания будут использовать настройки этой группы разрешений POS, если разрешения POS работника не были переопределены на уровне должности.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="5d2ae-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5d2ae-131">Click Save.</span></span>
    * <span data-ttu-id="5d2ae-132">После сохранения изменений необходимо запустить график распределения персонала, чтобы передать изменения в розничные каналы.</span><span class="sxs-lookup"><span data-stu-id="5d2ae-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


