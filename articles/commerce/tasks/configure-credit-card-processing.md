---
title: Настройка обработки кредитных карт
description: Эта процедура содержит инструкции по просмотру списка поставщиков платежей и настройке счета платежа для расчетов с клиентами.
author: jashanno
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13aa59ab1c6b0170ae9ab8972fb00bcf47e2b754
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789764"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="52265-103">Настройка обработки кредитных карт</span><span class="sxs-lookup"><span data-stu-id="52265-103">Configure credit card processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52265-104">Эта процедура содержит инструкции по просмотру списка поставщиков платежей и настройке счета платежа для расчетов с клиентами.</span><span class="sxs-lookup"><span data-stu-id="52265-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="52265-105">Эта процедура использует компанию USRT с демонстрационными данными и предназначена для администраторов и ИТ-специалистов.</span><span class="sxs-lookup"><span data-stu-id="52265-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="52265-106">Просмотр списка поставщиков платежей</span><span class="sxs-lookup"><span data-stu-id="52265-106">View a list of payment providers</span></span>
1. <span data-ttu-id="52265-107">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Службы платежей".</span><span class="sxs-lookup"><span data-stu-id="52265-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="52265-108">Щелкните "Просмотр доступных поставщиков".</span><span class="sxs-lookup"><span data-stu-id="52265-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="52265-109">Настройка счета платежа</span><span class="sxs-lookup"><span data-stu-id="52265-109">Configure payment account</span></span>
1. <span data-ttu-id="52265-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="52265-110">Click New.</span></span>
2. <span data-ttu-id="52265-111">В поле "Служба платежей" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52265-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="52265-112">В поле "Соединитель платежей" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="52265-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="52265-113">Переключите развертывание раздела "Учетная запись службы платежей".</span><span class="sxs-lookup"><span data-stu-id="52265-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="52265-114">В поле "Среда:" введите "PROD".</span><span class="sxs-lookup"><span data-stu-id="52265-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="52265-115">Щелкните "Типы кредитных карт".</span><span class="sxs-lookup"><span data-stu-id="52265-115">Click Credit card types.</span></span>
7. <span data-ttu-id="52265-116">В поле "Журнал платежей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="52265-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="52265-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="52265-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="52265-118">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="52265-118">Click Add.</span></span>
10. <span data-ttu-id="52265-119">В поле "Валюта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52265-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="52265-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="52265-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="52265-121">В поле "Журнал платежей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="52265-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="52265-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="52265-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="52265-123">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="52265-123">Click Add.</span></span>
15. <span data-ttu-id="52265-124">В поле "Валюта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52265-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="52265-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="52265-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="52265-126">Можно повторить эти шаги для произвольного количества типов карт.</span><span class="sxs-lookup"><span data-stu-id="52265-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="52265-127">В поле "Журнал платежей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="52265-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="52265-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="52265-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="52265-129">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="52265-129">Click Add.</span></span>
20. <span data-ttu-id="52265-130">В поле "Валюта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52265-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="52265-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="52265-131">Click Save.</span></span>
22. <span data-ttu-id="52265-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="52265-132">Close the page.</span></span>
23. <span data-ttu-id="52265-133">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="52265-133">Click Validate.</span></span>
24. <span data-ttu-id="52265-134">Установите флажок "Процессор по умолчанию для новых кредитных карт".</span><span class="sxs-lookup"><span data-stu-id="52265-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="52265-135">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="52265-135">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]