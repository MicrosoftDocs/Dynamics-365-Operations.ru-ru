--- 
title: "Запись сотрудника в переменный план компенсаций"
description: "Менеджер по компенсациям и льготам может регистрировать сотрудников в планах переменных компенсаций для расчета денежных и неденежных вознаграждений для сотрудников."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7e460794b460f2557af6607276b3cd0727e2de85
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="7cbaf-103">Запись сотрудника в переменный план компенсаций</span><span class="sxs-lookup"><span data-stu-id="7cbaf-103">Enroll an employee in a variable compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7cbaf-104">Менеджер по компенсациям и льготам может регистрировать сотрудников в планах переменных компенсаций для расчета денежных и неденежных вознаграждений для сотрудников.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="7cbaf-105">Эта процедура предполагает, что план переменной компенсации создан, в поле "Включить регистрацию" задано значение "Да" и правила приемлемости созданы для данного плана переменной компенсации.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="7cbaf-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7cbaf-107">Чтобы начать эту процедуру, перейдите в раздел "Управление персоналом" > "Работники" > "Сотрудники" > "Компенсация" > "Регистрация переменного плана".</span><span class="sxs-lookup"><span data-stu-id="7cbaf-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="7cbaf-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7cbaf-108">Click New.</span></span>
2. <span data-ttu-id="7cbaf-109">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7cbaf-110">Результаты поиска планов будут отфильтрованы для отображения только тех планов переменной компенсации, на которые имеет право сотрудник согласно правилам приемлемости.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="7cbaf-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7cbaf-112">Переключите развертывание раздела "Общее".</span><span class="sxs-lookup"><span data-stu-id="7cbaf-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="7cbaf-113">В поле "Действует с" введите дату.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="7cbaf-114">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="7cbaf-114">Click Save.</span></span>
7. <span data-ttu-id="7cbaf-115">Переключите развертывание раздела "Переопределения".</span><span class="sxs-lookup"><span data-stu-id="7cbaf-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="7cbaf-116">При необходимости дату правила найма можно настроить для переопределения даты найма для сотрудника, когда правило найма, определенное для выбранного переменного плана, имеет значение "Процент".</span><span class="sxs-lookup"><span data-stu-id="7cbaf-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="7cbaf-117">Если переменный план выражен в процентах от базового плана, процент вознаграждения можно переопределить для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="7cbaf-118">Если план переменной компенсации выражен в количестве единиц, количество единиц можно переопределить для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="7cbaf-119">Если сотрудник должен получать фиксированную сумму в качестве вознаграждения, сумму можно задать здесь.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="7cbaf-120">Переключите развертывание раздела "Переопределение организации".</span><span class="sxs-lookup"><span data-stu-id="7cbaf-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="7cbaf-121">Если в производительности сотрудника следует учитывать производительность различных подразделений или производительность отдела, отличного от отдела, назначенного должности сотрудника, подразделение можно переопределить.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="7cbaf-122">Столбец "Процент" должен в сумме иметь значение 100.</span><span class="sxs-lookup"><span data-stu-id="7cbaf-122">The Percent column should total 100.</span></span>  


