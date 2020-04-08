---
title: Создание групп разрешений POS
description: В этом разделе объясняется, как создать группу разрешений POS.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ffc64fd39a390af3ca7110178ef0999527106dc
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141392"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="96fe0-103">Создание групп разрешений POS</span><span class="sxs-lookup"><span data-stu-id="96fe0-103">Create POS permission groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96fe0-104">В этом разделе объясняется, как создать группу разрешений POS.</span><span class="sxs-lookup"><span data-stu-id="96fe0-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="96fe0-105">В качестве компании с демонстрационными данными для создания этой задачи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="96fe0-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="96fe0-106">Эта задача предназначена для роли директора-распорядителя в Commerce.</span><span class="sxs-lookup"><span data-stu-id="96fe0-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="96fe0-107">В области переходов выберите **Модули > Retail и Commerce > Сотрудники > Группы разрешений**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="96fe0-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-108">Select **New**.</span></span>
3. <span data-ttu-id="96fe0-109">В поле **ИД группы POS-разрешений** введите значение.</span><span class="sxs-lookup"><span data-stu-id="96fe0-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="96fe0-110">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="96fe0-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="96fe0-111">Выберите **Да** в поле **Просмотр записей часов**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="96fe0-112">Теперь можно активировать или деактивировать различные разрешения для группы разрешений POS.</span><span class="sxs-lookup"><span data-stu-id="96fe0-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="96fe0-113">Для некоторых разрешений можно установить значение, которое будет использоваться для проверки того, может ли пользователь терминала выполнять определенное действие.</span><span class="sxs-lookup"><span data-stu-id="96fe0-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="96fe0-114">В этом руководстве по задачам включено несколько разрешение, которые можно предоставить кассиру.</span><span class="sxs-lookup"><span data-stu-id="96fe0-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="96fe0-115">Выберите **Да** в поле **Разрешить создание заказа**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="96fe0-116">Выберите **Да** в поле **Разрешить изменение заказа**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="96fe0-117">Выберите **Да** в поле **Разрешить получение заказа**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="96fe0-118">Выберите **Да** в поле **Разрешить изменение пароля**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="96fe0-119">Выберите **Да** в поле **Разрешить закрытие "вслепую"**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="96fe0-120">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-120">Select **Save**.</span></span> <span data-ttu-id="96fe0-121">После сохранения изменений необходимо запустить график распределения персонала, чтобы передать изменения в Commerce.</span><span class="sxs-lookup"><span data-stu-id="96fe0-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="96fe0-122">В области перехода выберите **Модули > Управление персоналом > Должности > Должности**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="96fe0-123">Теперь мы назначим группы разрешения POS заданию.</span><span class="sxs-lookup"><span data-stu-id="96fe0-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="96fe0-124">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="96fe0-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="96fe0-125">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-125">Select **Edit**.</span></span>
15. <span data-ttu-id="96fe0-126">Разверните раздел **Классификация задний**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="96fe0-127">В поле "Группа POS-разрешений" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="96fe0-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="96fe0-128">Все работники на должностях для этого задания будут использовать настройки этой группы разрешений POS, если разрешения POS работника не были переопределены на уровне должности.</span><span class="sxs-lookup"><span data-stu-id="96fe0-128">All Workers in Positions for this Job will use this POS permission group's settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="96fe0-129">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-129">Select **Save**.</span></span> <span data-ttu-id="96fe0-130">После сохранения изменений необходимо запустить график распределения персонала, чтобы передать изменения в каналы.</span><span class="sxs-lookup"><span data-stu-id="96fe0-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  

