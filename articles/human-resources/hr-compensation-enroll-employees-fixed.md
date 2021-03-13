---
title: Включение сотрудника в план фиксированных компенсаций
description: Менеджер по компенсациям и льготам может назначить сотрудников планам фиксированной компенсации для управления их базовой заработной платой.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc8373a4a39a1a212ab445b2b300fbddfe0e4a39
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114011"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="06224-103">Включение сотрудника в план фиксированных компенсаций</span><span class="sxs-lookup"><span data-stu-id="06224-103">Enroll an employee in a fixed compensation plan</span></span>

<span data-ttu-id="06224-104">Менеджер по компенсациям и льготам может назначить сотрудников планам фиксированной компенсации для управления их базовой заработной платой.</span><span class="sxs-lookup"><span data-stu-id="06224-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="06224-105">Эта процедура предполагает, что фиксированный план создан и активен и что правила приемлемости для плана заданы.</span><span class="sxs-lookup"><span data-stu-id="06224-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="06224-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="06224-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="06224-107">Чтобы начать процедуру, перейдите в раздел "Управление персоналом" > "Работники" > "Сотрудники" > "Компенсация" > "Фиксированный план".</span><span class="sxs-lookup"><span data-stu-id="06224-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="06224-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="06224-108">Click New.</span></span>
2. <span data-ttu-id="06224-109">В поле действий выберите действие "Фиксированная компенсация" типа "Прием на работу / Повторный прием на работу" для описания изменения в компенсации сотрудника.</span><span class="sxs-lookup"><span data-stu-id="06224-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="06224-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="06224-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="06224-111">В поле "Должность" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="06224-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="06224-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="06224-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="06224-113">Уровень, который отображается на основании уровня компенсации задания в должности.</span><span class="sxs-lookup"><span data-stu-id="06224-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="06224-114">Уровень необходимо настроить для задания до назначения компенсации сотруднику.</span><span class="sxs-lookup"><span data-stu-id="06224-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="06224-115">В поле "План" выберите план фиксированной компенсации для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="06224-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="06224-116">Результаты поиска планов будут отфильтрованы для отображения только тех планов, на которые имеет право сотрудник согласно правилам приемлемости.</span><span class="sxs-lookup"><span data-stu-id="06224-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="06224-117">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="06224-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="06224-118">В качестве даты вступления в силу и даты окончания срока действия компенсации по умолчанию используются дата начала и дата окончания назначения работника на должность.</span><span class="sxs-lookup"><span data-stu-id="06224-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="06224-119">Эти даты можно изменить при необходимости.</span><span class="sxs-lookup"><span data-stu-id="06224-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="06224-120">Если план фиксированной компенсации является пошаговым планом, выберите шаг, содержащий правильную ставку оплаты для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="06224-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="06224-121">Если план фиксированной компенсации является ступенчатым или ленточным планом, введите ставку оплаты для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="06224-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="06224-122">Ставка оплаты будет утверждена согласно настроек допуска для плана, а также минимальной и максимальной опорных точек для уровня компенсации задания.</span><span class="sxs-lookup"><span data-stu-id="06224-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="06224-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="06224-123">Click OK.</span></span>

