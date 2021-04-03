---
title: Настройка разделения обязанностей
description: Можно настроить правила для разделения задач, которые должны выполняться разными пользователями.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c1521d6bbbe12964fef0942fcc4943f12a4360a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562505"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="dfcca-103">Настройка разделения обязанностей</span><span class="sxs-lookup"><span data-stu-id="dfcca-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dfcca-104">Можно настроить правила для разделения задач, которые должны выполняться разными пользователями.</span><span class="sxs-lookup"><span data-stu-id="dfcca-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="dfcca-105">Это называется разделением обязанностей.</span><span class="sxs-lookup"><span data-stu-id="dfcca-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="dfcca-106">Например, вряд ли имеет смысл, чтобы один и тот же человек оформлял получение товаров и обрабатывал платеж поставщику.</span><span class="sxs-lookup"><span data-stu-id="dfcca-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="dfcca-107">Разделение обязанностей помогает снизить риск мошенничества, а также помогает выявлять ошибки или нарушения.</span><span class="sxs-lookup"><span data-stu-id="dfcca-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="dfcca-108">Разделение обязанностей также можно использовать для реализации политик внутреннего контроля.</span><span class="sxs-lookup"><span data-stu-id="dfcca-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="dfcca-109">Выполните следующую процедуру, чтобы создать правило.</span><span class="sxs-lookup"><span data-stu-id="dfcca-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="dfcca-110">Для выполнения процедуры необходимо быть системным администратором.</span><span class="sxs-lookup"><span data-stu-id="dfcca-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="dfcca-111">Перейдите в раздел **Администрирование системы** > **Контроль доступа** > **Разделение обязанностей** > **Правила разделения обязанностей**.</span><span class="sxs-lookup"><span data-stu-id="dfcca-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="dfcca-112">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="dfcca-112">Click **New**.</span></span>
3. <span data-ttu-id="dfcca-113">В поле **Имя** введите значение для правила.</span><span class="sxs-lookup"><span data-stu-id="dfcca-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="dfcca-114">В поле **Первая обязанность** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="dfcca-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="dfcca-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="dfcca-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="dfcca-116">Выберите первое полномочие, управляемое правилом.</span><span class="sxs-lookup"><span data-stu-id="dfcca-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="dfcca-117">В поле **Вторая обязанность** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="dfcca-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="dfcca-118">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="dfcca-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="dfcca-119">Выберите второе полномочие, управляемое правилом.</span><span class="sxs-lookup"><span data-stu-id="dfcca-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="dfcca-120">В поле **Серьезность** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="dfcca-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="dfcca-121">Выберите серьезность риска, который возникает, когда один и тот же пользователь или роль имеют оба полномочия.</span><span class="sxs-lookup"><span data-stu-id="dfcca-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="dfcca-122">В поле **Угроза безопасности** введите значение.</span><span class="sxs-lookup"><span data-stu-id="dfcca-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="dfcca-123">Введите описание риска для безопасности.</span><span class="sxs-lookup"><span data-stu-id="dfcca-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="dfcca-124">В поле **Снижение риска безопасности** введите значение.</span><span class="sxs-lookup"><span data-stu-id="dfcca-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="dfcca-125">Введите описание действий, предпринимаемых для снижения риска безопасности.</span><span class="sxs-lookup"><span data-stu-id="dfcca-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="dfcca-126">Например, для снижения риска можно проводить более подробные проверки процесса, проводить ежемесячную административную проверку или использовать ресурсы совместно с другими подразделениями.</span><span class="sxs-lookup"><span data-stu-id="dfcca-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="dfcca-127">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dfcca-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="dfcca-128">При создании правила соответствие правилам разделения обязанностей не проверяется.</span><span class="sxs-lookup"><span data-stu-id="dfcca-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="dfcca-129">Можно создать правило, которое создает конфликт для существующих ролей.</span><span class="sxs-lookup"><span data-stu-id="dfcca-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="dfcca-130">Существующие назначения ролей пользователей также могут конфликтовать с новым правилом.</span><span class="sxs-lookup"><span data-stu-id="dfcca-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="dfcca-131">После создания или изменения правила необходимо выполнить проверку соответствия.</span><span class="sxs-lookup"><span data-stu-id="dfcca-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="dfcca-132">Дополнительные сведения см. в разделе [Выявление и разрешение конфликтов в разделении обязанностей](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="dfcca-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]