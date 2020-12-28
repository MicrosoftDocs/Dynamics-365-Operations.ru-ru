---
title: Настройка обработки кредитных карт
description: Эта процедура содержит инструкции по просмотру списка поставщиков платежей и настройке счета платежа для расчетов с клиентами.
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
ms.openlocfilehash: 2cfec44bc1c767dff1109c4ecd4e2862443fb1d0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415295"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="581a2-103">Настройка обработки кредитных карт</span><span class="sxs-lookup"><span data-stu-id="581a2-103">Configure credit card processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="581a2-104">Эта процедура содержит инструкции по просмотру списка поставщиков платежей и настройке счета платежа для расчетов с клиентами.</span><span class="sxs-lookup"><span data-stu-id="581a2-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="581a2-105">Эта процедура использует компанию USRT с демонстрационными данными и предназначена для администраторов и ИТ-специалистов.</span><span class="sxs-lookup"><span data-stu-id="581a2-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="581a2-106">Просмотр списка поставщиков платежей</span><span class="sxs-lookup"><span data-stu-id="581a2-106">View a list of payment providers</span></span>
1. <span data-ttu-id="581a2-107">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Службы платежей".</span><span class="sxs-lookup"><span data-stu-id="581a2-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="581a2-108">Щелкните "Просмотр доступных поставщиков".</span><span class="sxs-lookup"><span data-stu-id="581a2-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="581a2-109">Настройка счета платежа</span><span class="sxs-lookup"><span data-stu-id="581a2-109">Configure payment account</span></span>
1. <span data-ttu-id="581a2-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="581a2-110">Click New.</span></span>
2. <span data-ttu-id="581a2-111">В поле "Служба платежей" введите значение.</span><span class="sxs-lookup"><span data-stu-id="581a2-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="581a2-112">В поле "Соединитель платежей" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="581a2-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="581a2-113">Переключите развертывание раздела "Учетная запись службы платежей".</span><span class="sxs-lookup"><span data-stu-id="581a2-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="581a2-114">В поле "Среда:" введите "PROD".</span><span class="sxs-lookup"><span data-stu-id="581a2-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="581a2-115">Щелкните "Типы кредитных карт".</span><span class="sxs-lookup"><span data-stu-id="581a2-115">Click Credit card types.</span></span>
7. <span data-ttu-id="581a2-116">В поле "Журнал платежей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="581a2-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="581a2-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="581a2-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="581a2-118">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="581a2-118">Click Add.</span></span>
10. <span data-ttu-id="581a2-119">В поле "Валюта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="581a2-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="581a2-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="581a2-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="581a2-121">В поле "Журнал платежей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="581a2-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="581a2-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="581a2-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="581a2-123">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="581a2-123">Click Add.</span></span>
15. <span data-ttu-id="581a2-124">В поле "Валюта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="581a2-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="581a2-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="581a2-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="581a2-126">Можно повторить эти шаги для произвольного количества типов карт.</span><span class="sxs-lookup"><span data-stu-id="581a2-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="581a2-127">В поле "Журнал платежей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="581a2-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="581a2-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="581a2-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="581a2-129">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="581a2-129">Click Add.</span></span>
20. <span data-ttu-id="581a2-130">В поле "Валюта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="581a2-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="581a2-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="581a2-131">Click Save.</span></span>
22. <span data-ttu-id="581a2-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="581a2-132">Close the page.</span></span>
23. <span data-ttu-id="581a2-133">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="581a2-133">Click Validate.</span></span>
24. <span data-ttu-id="581a2-134">Установите флажок "Процессор по умолчанию для новых кредитных карт".</span><span class="sxs-lookup"><span data-stu-id="581a2-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="581a2-135">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="581a2-135">Click Save.</span></span>

