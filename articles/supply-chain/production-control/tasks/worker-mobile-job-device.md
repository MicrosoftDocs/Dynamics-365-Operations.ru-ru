--- 
title: "Настройка работника с использованием мобильного устройства задания"
description: "В этой процедуры показано, как назначить правильные роли учетной записи пользователя работника, а затем позволить работнику регистрироваться в цеху."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5322d77af470c25f0849cbbfbbfbc4a50a7e859b
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="a8049-103">Настройка работника с использованием мобильного устройства задания</span><span class="sxs-lookup"><span data-stu-id="a8049-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8049-104">В этой процедуры показано, как назначить правильные роли учетной записи пользователя работника, а затем позволить работнику регистрироваться в цеху.</span><span class="sxs-lookup"><span data-stu-id="a8049-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="a8049-105">Назначение ролей учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="a8049-105">Assign roles to user account</span></span>
1. <span data-ttu-id="a8049-106">Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="a8049-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="a8049-107">С помощью экспресс-фильтра отфильтруйте по имени работника, для которого учетная запись пользователя связана с ролью оператора станка.</span><span class="sxs-lookup"><span data-stu-id="a8049-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="a8049-108">В примерах данных это будет имя Shannon.</span><span class="sxs-lookup"><span data-stu-id="a8049-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="a8049-109">Выделите запись учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8049-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="a8049-110">В списке нажмите ссылку "Имя" в выбранной строке для просмотра сведений об учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8049-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="a8049-111">В дереве выберите "Роли\Оператор станка".</span><span class="sxs-lookup"><span data-stu-id="a8049-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="a8049-112">Закройте страницу сведений об у четной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8049-112">Close the user account details page.</span></span>
7. <span data-ttu-id="a8049-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a8049-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="a8049-114">Настройте учетную запись работника.</span><span class="sxs-lookup"><span data-stu-id="a8049-114">Configure worker account.</span></span>
1. <span data-ttu-id="a8049-115">Перейдите в раздел "Управление персоналом" > "Работники" > "Работники".</span><span class="sxs-lookup"><span data-stu-id="a8049-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="a8049-116">С помощью экспресс-фильтра отфильтруйте по имени работника, для которого учетная запись пользователя связана с ролью оператора станка.</span><span class="sxs-lookup"><span data-stu-id="a8049-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="a8049-117">В примерах данных это будет имя Shannon.</span><span class="sxs-lookup"><span data-stu-id="a8049-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="a8049-118">Выделите запись учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8049-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="a8049-119">В списке нажмите ссылку "Имя" в выбранной строке для просмотра сведений об учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8049-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="a8049-120">Перейдите на вкладку "Занятость".</span><span class="sxs-lookup"><span data-stu-id="a8049-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="a8049-121">Разверните экспресс-вкладку "Регистрация времени", а затем щелкните "Активировать в терминалах регистрации".</span><span class="sxs-lookup"><span data-stu-id="a8049-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="a8049-122">Щелкните "Активировать в терминалах регистрации".</span><span class="sxs-lookup"><span data-stu-id="a8049-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="a8049-123">В поле "Группа расчета" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a8049-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="a8049-124">В поле "Группа расчета по умолчанию" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a8049-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="a8049-125">В поле "Группа утверждения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a8049-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="a8049-126">В поле "Стандартный профиль" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a8049-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="a8049-127">В поле "Группа графиков" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a8049-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="a8049-128">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a8049-128">Click OK.</span></span>
14. <span data-ttu-id="a8049-129">Нажмите "Изменить", чтобы ввести номер значка для нового работника с регистрацией времени.</span><span class="sxs-lookup"><span data-stu-id="a8049-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="a8049-130">В поле "Код эмблемы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a8049-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="a8049-131">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="a8049-131">Click Save.</span></span>
17. <span data-ttu-id="a8049-132">Используйте ярлык SaveRecord.</span><span class="sxs-lookup"><span data-stu-id="a8049-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="a8049-133">Закройте страницу сведений о работнике.</span><span class="sxs-lookup"><span data-stu-id="a8049-133">Close the worker details page.</span></span>
19. <span data-ttu-id="a8049-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a8049-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="a8049-135">Назначьте работника группе устройств.</span><span class="sxs-lookup"><span data-stu-id="a8049-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="a8049-136">Перейдите в раздел "Управление производством" > "Настройка" > "Управление производством" > "Настроить карту заданий для устройств".</span><span class="sxs-lookup"><span data-stu-id="a8049-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="a8049-137">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="a8049-137">Click Add.</span></span>
3. <span data-ttu-id="a8049-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a8049-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a8049-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a8049-139">Click OK.</span></span>
5. <span data-ttu-id="a8049-140">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="a8049-140">Click Edit.</span></span>
6. <span data-ttu-id="a8049-141">В поле "Производственное подразделение" можно установить фильтр по умолчанию для работника.</span><span class="sxs-lookup"><span data-stu-id="a8049-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="a8049-142">В результате, когда работник входит в систему для устройства, будут отображаться только производственные задания для выбранного производственного подразделения.</span><span class="sxs-lookup"><span data-stu-id="a8049-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="a8049-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a8049-143">Close the page.</span></span>

