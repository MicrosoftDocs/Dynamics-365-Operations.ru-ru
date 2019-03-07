---
title: Создание финансовых аналитик для каналов розничной торговли и настройка значений аналитик для магазинов
description: Эта процедура содержит инструкции по созданию финансовой аналитики канала розничной торговли со значениями аналитик и по настройке значений финансовых аналитик для розничных магазинов.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf32d17a36fd699141ce697d23e20b2eb5cbfa54
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "354537"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="24e73-103">Создание финансовых аналитик для каналов розничной торговли и настройка значений аналитик для магазинов</span><span class="sxs-lookup"><span data-stu-id="24e73-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="24e73-104">Эта процедура содержит инструкции по созданию финансовой аналитики канала розничной торговли со значениями аналитик и по настройке значений финансовых аналитик для розничных магазинов.</span><span class="sxs-lookup"><span data-stu-id="24e73-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="24e73-105">Раздел не включает другие связанные действия, например создание наборов аналитик и структур счетов.</span><span class="sxs-lookup"><span data-stu-id="24e73-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="24e73-106">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="24e73-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="24e73-107">Перейдите в раздел "Главная книга" > "План счетов" > "Аналитики" > "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="24e73-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="24e73-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="24e73-108">Click New.</span></span>
3. <span data-ttu-id="24e73-109">В поле "Использовать значения из" выберите "Каналы розничной торговли".</span><span class="sxs-lookup"><span data-stu-id="24e73-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="24e73-110">В поле "Наименование аналитики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="24e73-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="24e73-111">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="24e73-111">Click Activate.</span></span>
6. <span data-ttu-id="24e73-112">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="24e73-112">Click Close.</span></span>
7. <span data-ttu-id="24e73-113">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="24e73-113">Click Activate.</span></span>
8. <span data-ttu-id="24e73-114">Щелкните "Значения аналитик".</span><span class="sxs-lookup"><span data-stu-id="24e73-114">Click Dimension values.</span></span>
9. <span data-ttu-id="24e73-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="24e73-115">Close the page.</span></span>
10. <span data-ttu-id="24e73-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="24e73-116">Click Save.</span></span>
11. <span data-ttu-id="24e73-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="24e73-117">Close the page.</span></span>
12. <span data-ttu-id="24e73-118">Перейдите в раздел Розничная торговля и коммерция > Каналы > Магазины розничной торговли > Все розничные магазины.</span><span class="sxs-lookup"><span data-stu-id="24e73-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="24e73-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="24e73-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="24e73-120">Переключите развертывание раздела "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="24e73-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="24e73-121">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="24e73-121">Click Edit.</span></span>
16. <span data-ttu-id="24e73-122">В поле "Retailchannel" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="24e73-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="24e73-123">В списке найдите и выберите значение аналитики для обновляемого магазина.</span><span class="sxs-lookup"><span data-stu-id="24e73-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="24e73-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="24e73-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="24e73-125">В поле "CostCenter" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="24e73-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="24e73-126">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="24e73-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="24e73-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="24e73-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="24e73-128">В поле "Подразделение" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="24e73-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="24e73-129">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="24e73-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="24e73-130">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="24e73-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="24e73-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="24e73-131">Click Save.</span></span>

