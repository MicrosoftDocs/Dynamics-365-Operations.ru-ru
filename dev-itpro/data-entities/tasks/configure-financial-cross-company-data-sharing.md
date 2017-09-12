--- 
title: "Настройка совместного использования финансовых данных компаниями"
description: "В этой процедуре описывается, как настроить, включить, проверить и разрешить конфликты при обмене данными между компаниями."
author: aprilolson
manager: AnnBe
ms.date: 06/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d36f19b5fa617169d33e7720e6a7602581cb525a
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="54dd4-103">Настройка совместного использования финансовых данных компаниями</span><span class="sxs-lookup"><span data-stu-id="54dd4-103">Configure financial cross-company data sharing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54dd4-104">В этой процедуре описывается, как настроить, включить, проверить и разрешить конфликты при обмене данными между компаниями.</span><span class="sxs-lookup"><span data-stu-id="54dd4-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="54dd4-105">В ней используется компания с демонстрационными данными USMF и шаблон публикации финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="54dd4-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="54dd4-106">Для выполнения этого руководства по задаче требуется платформа Dynamics AX 7.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="54dd4-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="54dd4-107">Перейдите в раздел "Администрирование системы" > "Рабочие области" > "Управление данными".</span><span class="sxs-lookup"><span data-stu-id="54dd4-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="54dd4-108">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="54dd4-108">Click Import.</span></span>
3. <span data-ttu-id="54dd4-109">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="54dd4-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="54dd4-110">В поле "Формат исходных данных" выберите "Тип упаковки".</span><span class="sxs-lookup"><span data-stu-id="54dd4-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="54dd4-111">Щелкните Загрузить.</span><span class="sxs-lookup"><span data-stu-id="54dd4-111">Click Upload.</span></span> <span data-ttu-id="54dd4-112">Перейдите к расположению файла пакета шаблона публикации финансовых данных и выберите этот файл.</span><span class="sxs-lookup"><span data-stu-id="54dd4-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="54dd4-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="54dd4-113">Click Save.</span></span>
6. <span data-ttu-id="54dd4-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="54dd4-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="54dd4-115">Выберите только что созданную политику обмена данными.</span><span class="sxs-lookup"><span data-stu-id="54dd4-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="54dd4-116">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="54dd4-116">Click Import.</span></span>
8. <span data-ttu-id="54dd4-117">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="54dd4-117">Click Close.</span></span>
9. <span data-ttu-id="54dd4-118">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="54dd4-118">Refresh the page.</span></span>
10. <span data-ttu-id="54dd4-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="54dd4-119">Close the page.</span></span>
11. <span data-ttu-id="54dd4-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="54dd4-120">Close the page.</span></span>
12. <span data-ttu-id="54dd4-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="54dd4-121">Close the page.</span></span>
13. <span data-ttu-id="54dd4-122">Перейдите в раздел "Администрирование системы" > "Настройка" > "Настройка совместного использования данных компаниями".</span><span class="sxs-lookup"><span data-stu-id="54dd4-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="54dd4-123">В списке найдите и выберите "Платежные дни".</span><span class="sxs-lookup"><span data-stu-id="54dd4-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="54dd4-124">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="54dd4-124">Click Add.</span></span>
16. <span data-ttu-id="54dd4-125">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="54dd4-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="54dd4-126">В поле "Компания" введите "USSI".</span><span class="sxs-lookup"><span data-stu-id="54dd4-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="54dd4-127">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="54dd4-127">Click Add.</span></span>
19. <span data-ttu-id="54dd4-128">В поле "Компания" введите "USMF".</span><span class="sxs-lookup"><span data-stu-id="54dd4-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="54dd4-129">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="54dd4-129">Click Save.</span></span>
21. <span data-ttu-id="54dd4-130">Нажмите кнопку Включить.</span><span class="sxs-lookup"><span data-stu-id="54dd4-130">Click Enable.</span></span>
22. <span data-ttu-id="54dd4-131">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="54dd4-131">Click Yes.</span></span>
23. <span data-ttu-id="54dd4-132">Щелкните "Поиск проблем совместного использования".</span><span class="sxs-lookup"><span data-stu-id="54dd4-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="54dd4-133">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="54dd4-133">Click Yes.</span></span>
25. <span data-ttu-id="54dd4-134">Щелкните "Обновить значение поля".</span><span class="sxs-lookup"><span data-stu-id="54dd4-134">Click Update field value.</span></span>
26. <span data-ttu-id="54dd4-135">Щелкните "Использовать значение из компании 1".</span><span class="sxs-lookup"><span data-stu-id="54dd4-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="54dd4-136">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="54dd4-136">Refresh the page.</span></span>
28. <span data-ttu-id="54dd4-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="54dd4-137">Close the page.</span></span>


