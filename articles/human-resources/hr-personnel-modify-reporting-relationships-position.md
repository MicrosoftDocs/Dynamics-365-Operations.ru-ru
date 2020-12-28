---
title: Изменение отношений подотчетности для должности
description: Ниже описан порядок изменения связи подотчетных отношений для сотрудника.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ae8ca5b20f331709e9fc1d9ae3b5f350e5c19ab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420257"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="35bfb-103">Изменение отношений подотчетности для должности</span><span class="sxs-lookup"><span data-stu-id="35bfb-103">Modify reporting relationships for a position</span></span>



<span data-ttu-id="35bfb-104">Ниже описан порядок изменения связи подотчетных отношений для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="35bfb-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="35bfb-105">Подотчетные отношения позволяют перенаправлять документы через workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="35bfb-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="35bfb-106">Эта процедура также показывает, как назначать сотрудника в дополнительные иерархии.</span><span class="sxs-lookup"><span data-stu-id="35bfb-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="35bfb-107">Например, сотрудник может быть частью проектной группы с неофициальным подотчетным отношением к супервизору проекта.</span><span class="sxs-lookup"><span data-stu-id="35bfb-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="35bfb-108">Можно определить для должности дополнительные отношения подотчетности, чтобы учесть различные сценарии проекта или матрицы.</span><span class="sxs-lookup"><span data-stu-id="35bfb-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="35bfb-109">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="35bfb-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="35bfb-110">Перейдите в раздел "Управление персоналом" > "Должности" > "Должности".</span><span class="sxs-lookup"><span data-stu-id="35bfb-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="35bfb-111">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="35bfb-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="35bfb-112">Например, отфильтруйте поле "Должность" по значению "000091".</span><span class="sxs-lookup"><span data-stu-id="35bfb-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="35bfb-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="35bfb-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="35bfb-114">Разверните раздел "Отчитывается перед должностью".</span><span class="sxs-lookup"><span data-stu-id="35bfb-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="35bfb-115">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35bfb-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="35bfb-116">В поле "Отчитывается перед" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="35bfb-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="35bfb-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="35bfb-117">Click Create.</span></span>
8. <span data-ttu-id="35bfb-118">Разверните раздел "Отношения".</span><span class="sxs-lookup"><span data-stu-id="35bfb-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="35bfb-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35bfb-119">Click Add.</span></span>
10. <span data-ttu-id="35bfb-120">Установите флажок слева от сетки.</span><span class="sxs-lookup"><span data-stu-id="35bfb-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="35bfb-121">В поле "Имя иерархии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="35bfb-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="35bfb-122">Пример: проект</span><span class="sxs-lookup"><span data-stu-id="35bfb-122">Example: Project</span></span>  
12. <span data-ttu-id="35bfb-123">В поле "Отчитывается перед должностью" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="35bfb-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="35bfb-124">Пример: 000437</span><span class="sxs-lookup"><span data-stu-id="35bfb-124">Example:  000437</span></span>
13. <span data-ttu-id="35bfb-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="35bfb-125">Click Save.</span></span>

