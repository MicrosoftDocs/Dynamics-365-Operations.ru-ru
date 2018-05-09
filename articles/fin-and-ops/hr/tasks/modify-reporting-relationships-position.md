--- 
title: "Изменение отношений подотчетности для должности"
description: "Ниже описан порядок изменения связи подотчетных отношений для сотрудника."
author: ShielaSogge
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 32d32cc969548168ce736b18918ce86d9965c4a5
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="c1c82-103">Изменение отношений подотчетности для должности</span><span class="sxs-lookup"><span data-stu-id="c1c82-103">Modify reporting relationships for a position</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1c82-104">Ниже описан порядок изменения связи подотчетных отношений для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="c1c82-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="c1c82-105">Подотчетные отношения позволяют перенаправлять документы через workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="c1c82-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="c1c82-106">Эта процедура также показывает, как назначать сотрудника в дополнительные иерархии.</span><span class="sxs-lookup"><span data-stu-id="c1c82-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="c1c82-107">Например, сотрудник может быть частью проектной группы с неофициальным подотчетным отношением к супервизору проекта.</span><span class="sxs-lookup"><span data-stu-id="c1c82-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="c1c82-108">Можно определить для должности дополнительные отношения подотчетности, чтобы учесть различные сценарии проекта или матрицы.</span><span class="sxs-lookup"><span data-stu-id="c1c82-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="c1c82-109">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="c1c82-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c1c82-110">Перейдите в раздел "Управление персоналом" > "Должности" > "Должности".</span><span class="sxs-lookup"><span data-stu-id="c1c82-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="c1c82-111">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="c1c82-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c1c82-112">Например, отфильтруйте поле "Должность" по значению "000091".</span><span class="sxs-lookup"><span data-stu-id="c1c82-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="c1c82-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c1c82-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c1c82-114">Разверните раздел "Отчитывается перед должностью".</span><span class="sxs-lookup"><span data-stu-id="c1c82-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="c1c82-115">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c1c82-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="c1c82-116">В поле "Отчитывается перед" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c1c82-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="c1c82-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c1c82-117">Click Create.</span></span>
8. <span data-ttu-id="c1c82-118">Разверните раздел "Отношения".</span><span class="sxs-lookup"><span data-stu-id="c1c82-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="c1c82-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="c1c82-119">Click Add.</span></span>
10. <span data-ttu-id="c1c82-120">Установите флажок слева от сетки.</span><span class="sxs-lookup"><span data-stu-id="c1c82-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="c1c82-121">В поле "Имя иерархии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c1c82-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="c1c82-122">Пример: проект</span><span class="sxs-lookup"><span data-stu-id="c1c82-122">Example: Project</span></span>  
12. <span data-ttu-id="c1c82-123">В поле "Отчитывается перед должностью" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c1c82-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="c1c82-124">Пример: 000437</span><span class="sxs-lookup"><span data-stu-id="c1c82-124">Example:  000437</span></span>
13. <span data-ttu-id="c1c82-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c1c82-125">Click Save.</span></span>


