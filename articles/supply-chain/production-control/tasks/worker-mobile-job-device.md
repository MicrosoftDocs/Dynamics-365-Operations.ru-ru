---
title: Настройка работника с использованием мобильного устройства задания
description: В этой процедуры показано, как назначить правильные роли учетной записи пользователя работника, а затем позволить работнику регистрироваться в цеху.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "327397"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="83ed9-103">Настройка работника с использованием мобильного устройства задания</span><span class="sxs-lookup"><span data-stu-id="83ed9-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83ed9-104">В этой процедуры показано, как назначить правильные роли учетной записи пользователя работника, а затем позволить работнику регистрироваться в цеху.</span><span class="sxs-lookup"><span data-stu-id="83ed9-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="83ed9-105">Назначение ролей учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="83ed9-105">Assign roles to user account</span></span>
1. <span data-ttu-id="83ed9-106">Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="83ed9-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="83ed9-107">С помощью экспресс-фильтра отфильтруйте по имени работника, для которого учетная запись пользователя связана с ролью оператора станка.</span><span class="sxs-lookup"><span data-stu-id="83ed9-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="83ed9-108">В примерах данных это будет имя Shannon.</span><span class="sxs-lookup"><span data-stu-id="83ed9-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="83ed9-109">Выделите запись учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="83ed9-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="83ed9-110">В списке нажмите ссылку "Имя" в выбранной строке для просмотра сведений об учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="83ed9-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="83ed9-111">В дереве выберите "Роли\Оператор станка".</span><span class="sxs-lookup"><span data-stu-id="83ed9-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="83ed9-112">Закройте страницу сведений об у четной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="83ed9-112">Close the user account details page.</span></span>
7. <span data-ttu-id="83ed9-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83ed9-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="83ed9-114">Настройте учетную запись работника.</span><span class="sxs-lookup"><span data-stu-id="83ed9-114">Configure worker account.</span></span>
1. <span data-ttu-id="83ed9-115">Перейдите в раздел "Управление персоналом" > "Работники" > "Работники".</span><span class="sxs-lookup"><span data-stu-id="83ed9-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="83ed9-116">С помощью экспресс-фильтра отфильтруйте по имени работника, для которого учетная запись пользователя связана с ролью оператора станка.</span><span class="sxs-lookup"><span data-stu-id="83ed9-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="83ed9-117">В примерах данных это будет имя Shannon.</span><span class="sxs-lookup"><span data-stu-id="83ed9-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="83ed9-118">Выделите запись учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="83ed9-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="83ed9-119">В списке нажмите ссылку "Имя" в выбранной строке для просмотра сведений об учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="83ed9-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="83ed9-120">Перейдите на вкладку "Занятость".</span><span class="sxs-lookup"><span data-stu-id="83ed9-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="83ed9-121">Разверните экспресс-вкладку "Регистрация времени", а затем щелкните "Активировать в терминалах регистрации".</span><span class="sxs-lookup"><span data-stu-id="83ed9-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="83ed9-122">Щелкните "Активировать в терминалах регистрации".</span><span class="sxs-lookup"><span data-stu-id="83ed9-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="83ed9-123">В поле "Группа расчета" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="83ed9-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="83ed9-124">В поле "Группа расчета по умолчанию" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="83ed9-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="83ed9-125">В поле "Группа утверждения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="83ed9-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="83ed9-126">В поле "Стандартный профиль" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="83ed9-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="83ed9-127">В поле "Группа графиков" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="83ed9-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="83ed9-128">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="83ed9-128">Click OK.</span></span>
14. <span data-ttu-id="83ed9-129">Нажмите "Изменить", чтобы ввести номер значка для нового работника с регистрацией времени.</span><span class="sxs-lookup"><span data-stu-id="83ed9-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="83ed9-130">В поле "Код эмблемы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83ed9-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="83ed9-131">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="83ed9-131">Click Save.</span></span>
17. <span data-ttu-id="83ed9-132">Используйте ярлык SaveRecord.</span><span class="sxs-lookup"><span data-stu-id="83ed9-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="83ed9-133">Закройте страницу сведений о работнике.</span><span class="sxs-lookup"><span data-stu-id="83ed9-133">Close the worker details page.</span></span>
19. <span data-ttu-id="83ed9-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83ed9-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="83ed9-135">Назначьте работника группе устройств.</span><span class="sxs-lookup"><span data-stu-id="83ed9-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="83ed9-136">Перейдите в раздел "Управление производством" > "Настройка" > "Управление производством" > "Настроить карту заданий для устройств".</span><span class="sxs-lookup"><span data-stu-id="83ed9-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="83ed9-137">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="83ed9-137">Click Add.</span></span>
3. <span data-ttu-id="83ed9-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="83ed9-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="83ed9-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="83ed9-139">Click OK.</span></span>
5. <span data-ttu-id="83ed9-140">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="83ed9-140">Click Edit.</span></span>
6. <span data-ttu-id="83ed9-141">В поле "Производственное подразделение" можно установить фильтр по умолчанию для работника.</span><span class="sxs-lookup"><span data-stu-id="83ed9-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="83ed9-142">В результате, когда работник входит в систему для устройства, будут отображаться только производственные задания для выбранного производственного подразделения.</span><span class="sxs-lookup"><span data-stu-id="83ed9-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="83ed9-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83ed9-143">Close the page.</span></span>

