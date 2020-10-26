---
title: Настройка работника с использованием мобильного устройства задания
description: В этом разделе показано, как назначить правильные роли учетной записи пользователя работника, а затем позволить работнику регистрироваться в цеху.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ada42a98a8a87e377f939d063b17f9904f6b3408
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978242"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="051f5-103">Настройка работника с использованием мобильного устройства задания</span><span class="sxs-lookup"><span data-stu-id="051f5-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="051f5-104">В этом разделе показано, как назначить правильные роли учетной записи пользователя работника, а затем позволить работнику регистрироваться в цеху.</span><span class="sxs-lookup"><span data-stu-id="051f5-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="051f5-105">Проверить, что работнику назначена определенная роль</span><span class="sxs-lookup"><span data-stu-id="051f5-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="051f5-106">В этом примере удостоверьтесь, что пользователю "SHANNON" присваивается роль оператора перед настройкой учетной записи работника.</span><span class="sxs-lookup"><span data-stu-id="051f5-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="051f5-107">Перейдите в раздел **Область перехода > Модули > Администрирование системы > Пользователи > Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="051f5-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="051f5-108">Поиск пользователя в быстром фильтре.</span><span class="sxs-lookup"><span data-stu-id="051f5-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="051f5-109">В этом примере введите `shannon`.</span><span class="sxs-lookup"><span data-stu-id="051f5-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="051f5-110">Выберите ссылку в столбце **Идентификатор пользователя** учетной записи пользователя, который появляется.</span><span class="sxs-lookup"><span data-stu-id="051f5-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="051f5-111">В дереве **Роли пользователя** выберите **Роли > Оператор станка**.</span><span class="sxs-lookup"><span data-stu-id="051f5-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="051f5-112">Закройте страницы **Сведения о пользователе** и **пользователи**, чтобы вернуться на домашнюю страницу.</span><span class="sxs-lookup"><span data-stu-id="051f5-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="051f5-113">Настройте учетную запись работника</span><span class="sxs-lookup"><span data-stu-id="051f5-113">Configure worker account</span></span>
1. <span data-ttu-id="051f5-114">Перейдите к **Область перехода > Модули > Управление персоналом > Работники > Работники**.</span><span class="sxs-lookup"><span data-stu-id="051f5-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="051f5-115">Поиск пользователя в быстром фильтре.</span><span class="sxs-lookup"><span data-stu-id="051f5-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="051f5-116">В этом примере введите `shannon`.</span><span class="sxs-lookup"><span data-stu-id="051f5-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="051f5-117">Выберите ссылку в столбце **Имя** учетной записи пользователя, который появляется.</span><span class="sxs-lookup"><span data-stu-id="051f5-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="051f5-118">Выберите вкладку **Регистрация времени**.</span><span class="sxs-lookup"><span data-stu-id="051f5-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="051f5-119">Выберите **Активировать в терминалах регистрации**.</span><span class="sxs-lookup"><span data-stu-id="051f5-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="051f5-120">Введите или выберите значения в следующих полях:</span><span class="sxs-lookup"><span data-stu-id="051f5-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="051f5-121">**Группа расчета**</span><span class="sxs-lookup"><span data-stu-id="051f5-121">**Calculation group**</span></span>  
    - <span data-ttu-id="051f5-122">**Группа расчета по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="051f5-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="051f5-123">**Группа утверждения**</span><span class="sxs-lookup"><span data-stu-id="051f5-123">**Approval group**</span></span>  
    - <span data-ttu-id="051f5-124">**Стандартный профиль**</span><span class="sxs-lookup"><span data-stu-id="051f5-124">**Standard profile**</span></span>  
    - <span data-ttu-id="051f5-125">**Группа графиков**</span><span class="sxs-lookup"><span data-stu-id="051f5-125">**Profile group**</span></span>  

7. <span data-ttu-id="051f5-126">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="051f5-126">Select **OK**.</span></span>
8. <span data-ttu-id="051f5-127">Выберите **Изменить**, чтобы ввести номер пропуска для нового работника с регистрацией времени.</span><span class="sxs-lookup"><span data-stu-id="051f5-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="051f5-128">Введите значение в поле **Код пропуска**.</span><span class="sxs-lookup"><span data-stu-id="051f5-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="051f5-129">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="051f5-129">Select **Save**.</span></span>
10. <span data-ttu-id="051f5-130">Закройте страницы **Сведения о работнике** и **Работники**.</span><span class="sxs-lookup"><span data-stu-id="051f5-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="051f5-131">Назначьте работника группе устройств</span><span class="sxs-lookup"><span data-stu-id="051f5-131">Assign worker to device group</span></span>
1. <span data-ttu-id="051f5-132">Перейдите к **Управление производством > Настройка > Управление производством > Настроить карту заданий для устройств**.</span><span class="sxs-lookup"><span data-stu-id="051f5-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="051f5-133">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="051f5-133">Select **Add**.</span></span>
3. <span data-ttu-id="051f5-134">В списке выберите требуемого работника.</span><span class="sxs-lookup"><span data-stu-id="051f5-134">In the list, select the desired worker.</span></span> <span data-ttu-id="051f5-135">В этом примере выберите **SHANNON**.</span><span class="sxs-lookup"><span data-stu-id="051f5-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="051f5-136">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="051f5-136">Select **OK**.</span></span>
5. <span data-ttu-id="051f5-137">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="051f5-137">Select **Edit**.</span></span>
6. <span data-ttu-id="051f5-138">В поле **Производственное подразделение** можно установить фильтр по умолчанию для работника.</span><span class="sxs-lookup"><span data-stu-id="051f5-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="051f5-139">В результате, когда работник входит в систему для устройства, будут отображаться только производственные задания для выбранного производственного подразделения.</span><span class="sxs-lookup"><span data-stu-id="051f5-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="051f5-140">Введите требуемое значение.</span><span class="sxs-lookup"><span data-stu-id="051f5-140">Enter the desired value.</span></span>
7. <span data-ttu-id="051f5-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="051f5-141">Close the page.</span></span>

