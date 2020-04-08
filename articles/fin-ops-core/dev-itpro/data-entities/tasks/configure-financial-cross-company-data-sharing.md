---
title: Настройка совместного использования финансовых данных компаниями
description: В этой процедуре описывается, как настроить, включить, проверить и разрешить конфликты при обмене данными между компаниями.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98eeae9f50238aae172e4a217d40be39ee46a0b8
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142969"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="1647c-103">Настройка совместного использования финансовых данных компаниями</span><span class="sxs-lookup"><span data-stu-id="1647c-103">Configure financial cross-company data sharing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1647c-104">В этой процедуре описывается, как настроить, включить, проверить и разрешить конфликты при обмене данными между компаниями.</span><span class="sxs-lookup"><span data-stu-id="1647c-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="1647c-105">В ней используется компания с демонстрационными данными USMF и шаблон публикации финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="1647c-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="1647c-106">Для выполнения этого руководства по задаче требуется платформа Dynamics AX 7.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="1647c-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="1647c-107">Перейдите в раздел **Область переходов > Модули > Администрирование системы > Рабочие области > Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="1647c-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="1647c-108">Нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="1647c-108">Click **Import**.</span></span>
3. <span data-ttu-id="1647c-109">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1647c-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="1647c-110">В поле **Формат исходных данных** выберите "Тип упаковки".</span><span class="sxs-lookup"><span data-stu-id="1647c-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="1647c-111">Щелкните **Загрузить**.</span><span class="sxs-lookup"><span data-stu-id="1647c-111">Click **Upload**.</span></span> <span data-ttu-id="1647c-112">Перейдите к расположению файла пакета шаблона публикации финансовых данных и выберите этот файл.</span><span class="sxs-lookup"><span data-stu-id="1647c-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="1647c-113">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1647c-113">Click **Save**.</span></span>
6. <span data-ttu-id="1647c-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1647c-114">In the list, mark the selected row.</span></span> <span data-ttu-id="1647c-115">Выберите только что созданную политику обмена данными.</span><span class="sxs-lookup"><span data-stu-id="1647c-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="1647c-116">Нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="1647c-116">Click **Import**.</span></span>
8. <span data-ttu-id="1647c-117">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="1647c-117">Click **Close**.</span></span>
9. <span data-ttu-id="1647c-118">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="1647c-118">Refresh the page.</span></span>
10. <span data-ttu-id="1647c-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1647c-119">Close the page.</span></span>
11. <span data-ttu-id="1647c-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1647c-120">Close the page.</span></span>
12. <span data-ttu-id="1647c-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1647c-121">Close the page.</span></span>
13. <span data-ttu-id="1647c-122">Перейдите в раздел **Область переходов > Модули > Администрирование системы > Настройка > Настройка совместного использования данных компаниями**.</span><span class="sxs-lookup"><span data-stu-id="1647c-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="1647c-123">В списке найдите и выберите **Платежные дни**.</span><span class="sxs-lookup"><span data-stu-id="1647c-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="1647c-124">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="1647c-124">Click **Add**.</span></span>
16. <span data-ttu-id="1647c-125">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1647c-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="1647c-126">В поле **Компания** введите "USSI".</span><span class="sxs-lookup"><span data-stu-id="1647c-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="1647c-127">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="1647c-127">Click **Add**.</span></span>
19. <span data-ttu-id="1647c-128">В поле **Компания** введите "USMF".</span><span class="sxs-lookup"><span data-stu-id="1647c-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="1647c-129">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1647c-129">Click **Save**.</span></span>
21. <span data-ttu-id="1647c-130">Щелкните **Включить**.</span><span class="sxs-lookup"><span data-stu-id="1647c-130">Click **Enable**.</span></span>
22. <span data-ttu-id="1647c-131">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="1647c-131">Click **Yes**.</span></span>
23. <span data-ttu-id="1647c-132">Щелкните **Поиск проблем совместного использования**.</span><span class="sxs-lookup"><span data-stu-id="1647c-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="1647c-133">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="1647c-133">Click **Yes**.</span></span>
25. <span data-ttu-id="1647c-134">Щелкните **Обновить значение поля**.</span><span class="sxs-lookup"><span data-stu-id="1647c-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="1647c-135">Щелкните **Использовать значение из компании 1**.</span><span class="sxs-lookup"><span data-stu-id="1647c-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="1647c-136">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="1647c-136">Refresh the page.</span></span>
28. <span data-ttu-id="1647c-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1647c-137">Close the page.</span></span>

