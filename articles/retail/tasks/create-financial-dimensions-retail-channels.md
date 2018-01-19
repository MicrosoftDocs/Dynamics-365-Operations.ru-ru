--- 
title: "Создание финансовых аналитик для каналов розничной торговли и настройка значений аналитик для магазинов"
description: "Эта процедура содержит инструкции по созданию финансовой аналитики канала розничной торговли со значениями аналитик и по настройке значений финансовых аналитик для розничных магазинов."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 9c46be996b2c002b05b9ee10329ff266e1a077c1
ms.contentlocale: ru-ru
ms.lasthandoff: 01/19/2018

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="6b608-103">Создание финансовых аналитик для каналов розничной торговли и настройка значений аналитик для магазинов</span><span class="sxs-lookup"><span data-stu-id="6b608-103">Create financial dimensions for Retail channels and configure dimension values on stores</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6b608-104">Эта процедура содержит инструкции по созданию финансовой аналитики канала розничной торговли со значениями аналитик и по настройке значений финансовых аналитик для розничных магазинов.</span><span class="sxs-lookup"><span data-stu-id="6b608-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="6b608-105">Раздел не включает другие связанные действия, например создание наборов аналитик и структур счетов.</span><span class="sxs-lookup"><span data-stu-id="6b608-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="6b608-106">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="6b608-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="6b608-107">Перейдите в раздел "Главная книга" > "План счетов" > "Аналитики" > "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="6b608-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="6b608-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6b608-108">Click New.</span></span>
3. <span data-ttu-id="6b608-109">В поле "Использовать значения из" выберите "Каналы розничной торговли".</span><span class="sxs-lookup"><span data-stu-id="6b608-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="6b608-110">В поле "Наименование аналитики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6b608-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="6b608-111">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="6b608-111">Click Activate.</span></span>
6. <span data-ttu-id="6b608-112">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="6b608-112">Click Close.</span></span>
7. <span data-ttu-id="6b608-113">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="6b608-113">Click Activate.</span></span>
8. <span data-ttu-id="6b608-114">Щелкните "Значения аналитик".</span><span class="sxs-lookup"><span data-stu-id="6b608-114">Click Dimension values.</span></span>
9. <span data-ttu-id="6b608-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6b608-115">Close the page.</span></span>
10. <span data-ttu-id="6b608-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6b608-116">Click Save.</span></span>
11. <span data-ttu-id="6b608-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6b608-117">Close the page.</span></span>
12. <span data-ttu-id="6b608-118">Перейдите в раздел Розничная торговля и коммерция > Каналы > Магазины розничной торговли > Все розничные магазины.</span><span class="sxs-lookup"><span data-stu-id="6b608-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="6b608-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="6b608-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6b608-120">Переключите развертывание раздела "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="6b608-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="6b608-121">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="6b608-121">Click Edit.</span></span>
16. <span data-ttu-id="6b608-122">В поле "Retailchannel" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="6b608-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="6b608-123">В списке найдите и выберите значение аналитики для обновляемого магазина.</span><span class="sxs-lookup"><span data-stu-id="6b608-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="6b608-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="6b608-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="6b608-125">В поле "CostCenter" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="6b608-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="6b608-126">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="6b608-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="6b608-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="6b608-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="6b608-128">В поле "Подразделение" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="6b608-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="6b608-129">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="6b608-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="6b608-130">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="6b608-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="6b608-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6b608-131">Click Save.</span></span>


