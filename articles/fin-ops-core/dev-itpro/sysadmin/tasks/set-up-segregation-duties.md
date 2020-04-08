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
ms.openlocfilehash: 712cc90bef4f3ad56291e99edd9f963ae88add48
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143520"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="a36d6-103">Настройка разделения обязанностей</span><span class="sxs-lookup"><span data-stu-id="a36d6-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a36d6-104">Можно настроить правила для разделения задач, которые должны выполняться разными пользователями.</span><span class="sxs-lookup"><span data-stu-id="a36d6-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="a36d6-105">Это называется разделением обязанностей.</span><span class="sxs-lookup"><span data-stu-id="a36d6-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="a36d6-106">Например, вряд ли имеет смысл, чтобы один и тот же человек оформлял получение товаров и обрабатывал платеж поставщику.</span><span class="sxs-lookup"><span data-stu-id="a36d6-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="a36d6-107">Разделение обязанностей помогает снизить риск мошенничества, а также помогает выявлять ошибки или нарушения.</span><span class="sxs-lookup"><span data-stu-id="a36d6-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="a36d6-108">Разделение обязанностей также можно использовать для реализации политик внутреннего контроля.</span><span class="sxs-lookup"><span data-stu-id="a36d6-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="a36d6-109">Выполните следующую процедуру, чтобы создать правило.</span><span class="sxs-lookup"><span data-stu-id="a36d6-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="a36d6-110">Для выполнения процедуры необходимо быть системным администратором.</span><span class="sxs-lookup"><span data-stu-id="a36d6-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="a36d6-111">В качестве компании с демонстрационными данными для создания этой процедуры используется DAT.</span><span class="sxs-lookup"><span data-stu-id="a36d6-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="a36d6-112">Перейдите в раздел **Область перехода > Модули > Администрирование системы > Контроль доступа > Разделение обязанностей > Правила разделения обязанностей**.</span><span class="sxs-lookup"><span data-stu-id="a36d6-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="a36d6-113">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a36d6-113">Click **New**.</span></span>
3. <span data-ttu-id="a36d6-114">В поле **Имя** введите значение для правила.</span><span class="sxs-lookup"><span data-stu-id="a36d6-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="a36d6-115">В поле **Первая обязанность** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a36d6-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a36d6-116">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a36d6-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="a36d6-117">Выберите первое полномочие, управляемое правилом.</span><span class="sxs-lookup"><span data-stu-id="a36d6-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="a36d6-118">В поле **Вторая обязанность** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a36d6-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="a36d6-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a36d6-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="a36d6-120">Выберите второе полномочие, управляемое правилом.</span><span class="sxs-lookup"><span data-stu-id="a36d6-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="a36d6-121">В поле **Серьезность** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="a36d6-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="a36d6-122">Выберите серьезность риска, который возникает, когда один и тот же пользователь или роль имеют оба полномочия.</span><span class="sxs-lookup"><span data-stu-id="a36d6-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="a36d6-123">В поле **Угроза безопасности** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a36d6-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="a36d6-124">Введите описание риска для безопасности.</span><span class="sxs-lookup"><span data-stu-id="a36d6-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="a36d6-125">В поле **Снижение риска безопасности** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a36d6-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="a36d6-126">Введите описание действий, предпринимаемых для снижения риска безопасности.</span><span class="sxs-lookup"><span data-stu-id="a36d6-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="a36d6-127">Например, для снижения риска можно проводить более подробные проверки процесса, проводить ежемесячную административную проверку или использовать ресурсы совместно с другими подразделениями.</span><span class="sxs-lookup"><span data-stu-id="a36d6-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="a36d6-128">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a36d6-128">Click **Save**.</span></span>

