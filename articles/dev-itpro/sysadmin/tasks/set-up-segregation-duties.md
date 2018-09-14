--- 
title: "Настройка разделения обязанностей"
description: "Можно настроить правила для разделения задач, которые должны выполняться разными пользователями."
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 68e1a4419eaa11a59e1b634deb8e76a2bb9b6fdf
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="afa27-103">Настройка разделения обязанностей</span><span class="sxs-lookup"><span data-stu-id="afa27-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="afa27-104">Можно настроить правила для разделения задач, которые должны выполняться разными пользователями.</span><span class="sxs-lookup"><span data-stu-id="afa27-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="afa27-105">Это называется разделением обязанностей.</span><span class="sxs-lookup"><span data-stu-id="afa27-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="afa27-106">Например, вряд ли имеет смысл, чтобы один и тот же человек оформлял получение товаров и обрабатывал платеж поставщику.</span><span class="sxs-lookup"><span data-stu-id="afa27-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="afa27-107">Разделение обязанностей помогает снизить риск мошенничества, а также помогает выявлять ошибки или нарушения.</span><span class="sxs-lookup"><span data-stu-id="afa27-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="afa27-108">Разделение обязанностей также можно использовать для реализации политик внутреннего контроля.</span><span class="sxs-lookup"><span data-stu-id="afa27-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="afa27-109">Выполните следующую процедуру, чтобы создать правило.</span><span class="sxs-lookup"><span data-stu-id="afa27-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="afa27-110">Для выполнения процедуры необходимо быть системным администратором.</span><span class="sxs-lookup"><span data-stu-id="afa27-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="afa27-111">В качестве компании с демонстрационными данными для создания этой процедуры используется DAT.</span><span class="sxs-lookup"><span data-stu-id="afa27-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="afa27-112">Перейдите в раздел "Администрирование системы" > "Контроль доступа" > "Разделение обязанностей" > "Правила разделения обязанностей".</span><span class="sxs-lookup"><span data-stu-id="afa27-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="afa27-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="afa27-113">Click New.</span></span>
3. <span data-ttu-id="afa27-114">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="afa27-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="afa27-115">Введите имя для правила.</span><span class="sxs-lookup"><span data-stu-id="afa27-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="afa27-116">В поле "Первая обязанность" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="afa27-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="afa27-117">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="afa27-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="afa27-118">Выберите первое полномочие, управляемое правилом.</span><span class="sxs-lookup"><span data-stu-id="afa27-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="afa27-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="afa27-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="afa27-120">В поле "Вторая обязанность" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="afa27-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="afa27-121">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="afa27-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="afa27-122">Выберите второе полномочие, управляемое правилом.</span><span class="sxs-lookup"><span data-stu-id="afa27-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="afa27-123">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="afa27-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="afa27-124">В поле "Строгость" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="afa27-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="afa27-125">Выберите серьезность риска, который возникает, когда один и тот же пользователь или роль имеют оба полномочия.</span><span class="sxs-lookup"><span data-stu-id="afa27-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="afa27-126">В поле "Угроза безопасности" введите значение.</span><span class="sxs-lookup"><span data-stu-id="afa27-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="afa27-127">Введите описание риска для безопасности.</span><span class="sxs-lookup"><span data-stu-id="afa27-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="afa27-128">В поле "Снижение риска безопасности" введите значение.</span><span class="sxs-lookup"><span data-stu-id="afa27-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="afa27-129">Введите описание действий, предпринимаемых для снижения риска безопасности.</span><span class="sxs-lookup"><span data-stu-id="afa27-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="afa27-130">Например, для снижения риска можно проводить более подробные проверки процесса, проводить ежемесячную административную проверку или использовать ресурсы совместно с другими подразделениями.</span><span class="sxs-lookup"><span data-stu-id="afa27-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="afa27-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="afa27-131">Click Save.</span></span>


