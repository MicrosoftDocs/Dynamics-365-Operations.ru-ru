---
title: Настройка совместного использования финансовых данных компаниями
description: В этой процедуре описывается, как настроить, включить, проверить и разрешить конфликты при обмене данными между компаниями.
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35ec8fc809841c0830224646fb57b0e4e4d40ef4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752300"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="06625-103">Настройка совместного использования финансовых данных компаниями</span><span class="sxs-lookup"><span data-stu-id="06625-103">Configure financial cross-company data sharing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06625-104">В этой процедуре описывается, как настроить, включить, проверить и разрешить конфликты при обмене данными между компаниями.</span><span class="sxs-lookup"><span data-stu-id="06625-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="06625-105">В ней используется компания с демонстрационными данными USMF и шаблон публикации финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="06625-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="06625-106">Для выполнения этого руководства по задаче требуется платформа Dynamics AX 7.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="06625-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="06625-107">Перейдите в раздел **Область переходов > Модули > Администрирование системы > Рабочие области > Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="06625-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="06625-108">Нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="06625-108">Click **Import**.</span></span>
3. <span data-ttu-id="06625-109">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="06625-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="06625-110">В поле **Формат исходных данных** выберите "Тип упаковки".</span><span class="sxs-lookup"><span data-stu-id="06625-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="06625-111">Щелкните **Загрузить**.</span><span class="sxs-lookup"><span data-stu-id="06625-111">Click **Upload**.</span></span> <span data-ttu-id="06625-112">Перейдите к расположению файла пакета шаблона публикации финансовых данных и выберите этот файл.</span><span class="sxs-lookup"><span data-stu-id="06625-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="06625-113">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="06625-113">Click **Save**.</span></span>
6. <span data-ttu-id="06625-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="06625-114">In the list, mark the selected row.</span></span> <span data-ttu-id="06625-115">Выберите только что созданную политику обмена данными.</span><span class="sxs-lookup"><span data-stu-id="06625-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="06625-116">Нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="06625-116">Click **Import**.</span></span>
8. <span data-ttu-id="06625-117">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="06625-117">Click **Close**.</span></span>
9. <span data-ttu-id="06625-118">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="06625-118">Refresh the page.</span></span>
10. <span data-ttu-id="06625-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="06625-119">Close the page.</span></span>
11. <span data-ttu-id="06625-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="06625-120">Close the page.</span></span>
12. <span data-ttu-id="06625-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="06625-121">Close the page.</span></span>
13. <span data-ttu-id="06625-122">Перейдите в раздел **Область переходов > Модули > Администрирование системы > Настройка > Настройка совместного использования данных компаниями**.</span><span class="sxs-lookup"><span data-stu-id="06625-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="06625-123">В списке найдите и выберите **Платежные дни**.</span><span class="sxs-lookup"><span data-stu-id="06625-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="06625-124">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="06625-124">Click **Add**.</span></span>
16. <span data-ttu-id="06625-125">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="06625-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="06625-126">В поле **Компания** введите "USSI".</span><span class="sxs-lookup"><span data-stu-id="06625-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="06625-127">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="06625-127">Click **Add**.</span></span>
19. <span data-ttu-id="06625-128">В поле **Компания** введите "USMF".</span><span class="sxs-lookup"><span data-stu-id="06625-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="06625-129">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="06625-129">Click **Save**.</span></span>
21. <span data-ttu-id="06625-130">Щелкните **Включить**.</span><span class="sxs-lookup"><span data-stu-id="06625-130">Click **Enable**.</span></span>
22. <span data-ttu-id="06625-131">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="06625-131">Click **Yes**.</span></span>
23. <span data-ttu-id="06625-132">Щелкните **Поиск проблем совместного использования**.</span><span class="sxs-lookup"><span data-stu-id="06625-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="06625-133">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="06625-133">Click **Yes**.</span></span>
25. <span data-ttu-id="06625-134">Щелкните **Обновить значение поля**.</span><span class="sxs-lookup"><span data-stu-id="06625-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="06625-135">Щелкните **Использовать значение из компании 1**.</span><span class="sxs-lookup"><span data-stu-id="06625-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="06625-136">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="06625-136">Refresh the page.</span></span>
28. <span data-ttu-id="06625-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="06625-137">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]