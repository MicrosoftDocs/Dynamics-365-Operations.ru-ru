---
title: Настройка разделения обязанностей
description: Можно настроить правила для разделения задач, которые должны выполняться разными пользователями.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40b40b77877680e28671b7a15ea8c8b58ce94417
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180883"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="3af0f-103">Настройка разделения обязанностей</span><span class="sxs-lookup"><span data-stu-id="3af0f-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3af0f-104">Можно настроить правила для разделения задач, которые должны выполняться разными пользователями.</span><span class="sxs-lookup"><span data-stu-id="3af0f-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="3af0f-105">Это называется разделением обязанностей.</span><span class="sxs-lookup"><span data-stu-id="3af0f-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="3af0f-106">Например, вряд ли имеет смысл, чтобы один и тот же человек оформлял получение товаров и обрабатывал платеж поставщику.</span><span class="sxs-lookup"><span data-stu-id="3af0f-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="3af0f-107">Разделение обязанностей помогает снизить риск мошенничества, а также помогает выявлять ошибки или нарушения.</span><span class="sxs-lookup"><span data-stu-id="3af0f-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="3af0f-108">Разделение обязанностей также можно использовать для реализации политик внутреннего контроля.</span><span class="sxs-lookup"><span data-stu-id="3af0f-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="3af0f-109">Выполните следующую процедуру, чтобы создать правило.</span><span class="sxs-lookup"><span data-stu-id="3af0f-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="3af0f-110">Для выполнения процедуры необходимо быть системным администратором.</span><span class="sxs-lookup"><span data-stu-id="3af0f-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="3af0f-111">В качестве компании с демонстрационными данными для создания этой процедуры используется DAT.</span><span class="sxs-lookup"><span data-stu-id="3af0f-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="3af0f-112">Перейдите в раздел **Область перехода > Модули > Администрирование системы > Контроль доступа > Разделение обязанностей > Правила разделения обязанностей**.</span><span class="sxs-lookup"><span data-stu-id="3af0f-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="3af0f-113">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3af0f-113">Click **New**.</span></span>
3. <span data-ttu-id="3af0f-114">В поле **Имя** введите значение для правила.</span><span class="sxs-lookup"><span data-stu-id="3af0f-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="3af0f-115">В поле **Первая обязанность** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3af0f-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3af0f-116">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3af0f-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="3af0f-117">Выберите первое полномочие, управляемое правилом.</span><span class="sxs-lookup"><span data-stu-id="3af0f-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="3af0f-118">В поле **Вторая обязанность** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3af0f-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="3af0f-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3af0f-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="3af0f-120">Выберите второе полномочие, управляемое правилом.</span><span class="sxs-lookup"><span data-stu-id="3af0f-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="3af0f-121">В поле **Серьезность** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="3af0f-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="3af0f-122">Выберите серьезность риска, который возникает, когда один и тот же пользователь или роль имеют оба полномочия.</span><span class="sxs-lookup"><span data-stu-id="3af0f-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="3af0f-123">В поле **Угроза безопасности** введите значение.</span><span class="sxs-lookup"><span data-stu-id="3af0f-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="3af0f-124">Введите описание риска для безопасности.</span><span class="sxs-lookup"><span data-stu-id="3af0f-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="3af0f-125">В поле **Снижение риска безопасности** введите значение.</span><span class="sxs-lookup"><span data-stu-id="3af0f-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="3af0f-126">Введите описание действий, предпринимаемых для снижения риска безопасности.</span><span class="sxs-lookup"><span data-stu-id="3af0f-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="3af0f-127">Например, для снижения риска можно проводить более подробные проверки процесса, проводить ежемесячную административную проверку или использовать ресурсы совместно с другими подразделениями.</span><span class="sxs-lookup"><span data-stu-id="3af0f-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="3af0f-128">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3af0f-128">Click **Save**.</span></span>

