---
title: Настройка разделения обязанностей
description: Можно настроить правила для разделения задач, которые должны выполняться разными пользователями.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcbd32131f9980a4f55e91b9d7ad48171069f72e
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826402"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="5b5ef-103">Настройка разделения обязанностей</span><span class="sxs-lookup"><span data-stu-id="5b5ef-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b5ef-104">Можно настроить правила для разделения задач, которые должны выполняться разными пользователями.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="5b5ef-105">Это называется разделением обязанностей.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="5b5ef-106">Например, вряд ли имеет смысл, чтобы один и тот же человек оформлял получение товаров и обрабатывал платеж поставщику.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="5b5ef-107">Разделение обязанностей помогает снизить риск мошенничества, а также помогает выявлять ошибки или нарушения.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="5b5ef-108">Разделение обязанностей также можно использовать для реализации политик внутреннего контроля.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="5b5ef-109">Выполните следующую процедуру, чтобы создать правило.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="5b5ef-110">Для выполнения процедуры необходимо быть системным администратором.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="5b5ef-111">Перейдите в раздел **Администрирование системы** > **Контроль доступа** > **Разделение обязанностей** > **Правила разделения обязанностей**.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="5b5ef-112">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-112">Click **New**.</span></span>
3. <span data-ttu-id="5b5ef-113">В поле **Имя** введите значение для правила.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="5b5ef-114">В поле **Первая обязанность** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5b5ef-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="5b5ef-116">Выберите первое полномочие, управляемое правилом.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="5b5ef-117">В поле **Вторая обязанность** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="5b5ef-118">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="5b5ef-119">Выберите второе полномочие, управляемое правилом.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="5b5ef-120">В поле **Серьезность** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="5b5ef-121">Выберите серьезность риска, который возникает, когда один и тот же пользователь или роль имеют оба полномочия.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="5b5ef-122">В поле **Угроза безопасности** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="5b5ef-123">Введите описание риска для безопасности.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="5b5ef-124">В поле **Снижение риска безопасности** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="5b5ef-125">Введите описание действий, предпринимаемых для снижения риска безопасности.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="5b5ef-126">Например, для снижения риска можно проводить более подробные проверки процесса, проводить ежемесячную административную проверку или использовать ресурсы совместно с другими подразделениями.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="5b5ef-127">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="5b5ef-128">При создании правила соответствие правилам разделения обязанностей не проверяется.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="5b5ef-129">Можно создать правило, которое создает конфликт для существующих ролей.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="5b5ef-130">Существующие назначения ролей пользователей также могут конфликтовать с новым правилом.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="5b5ef-131">После создания или изменения правила необходимо выполнить проверку соответствия.</span><span class="sxs-lookup"><span data-stu-id="5b5ef-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="5b5ef-132">Дополнительные сведения см. в разделе [Выявление и разрешение конфликтов в разделении обязанностей](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="5b5ef-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>
