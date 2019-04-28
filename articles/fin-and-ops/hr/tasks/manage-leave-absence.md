---
title: Управление отпуском
description: В этой процедуре показано, как создать записи отпуска сотрудника.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ce57495be4ae601d6ac06bb4780a2e1192dfcc5
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "859352"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="17904-103">Управление отпуском</span><span class="sxs-lookup"><span data-stu-id="17904-103">Manage leave of absence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="17904-104">В этой процедуре показано, как создать записи отпуска сотрудника.</span><span class="sxs-lookup"><span data-stu-id="17904-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="17904-105">Отслеживать время отпуска можно по причинам, связанным с медициной, образованием или родительскими мероприятиями.</span><span class="sxs-lookup"><span data-stu-id="17904-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="17904-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="17904-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="17904-107">Перейдите в раздел "Управление персоналом" > "Работники" > "Сотрудники".</span><span class="sxs-lookup"><span data-stu-id="17904-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="17904-108">В списке выберите сотрудника.</span><span class="sxs-lookup"><span data-stu-id="17904-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="17904-109">Отобразите подробные сведения для выбранного сотрудника, выбрав имя сотрудника.</span><span class="sxs-lookup"><span data-stu-id="17904-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="17904-110">Перейдите на вкладку "Занятость".</span><span class="sxs-lookup"><span data-stu-id="17904-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="17904-111">Щелкните "Отпуск".</span><span class="sxs-lookup"><span data-stu-id="17904-111">Click Leave.</span></span>
6. <span data-ttu-id="17904-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="17904-112">Click New.</span></span>
7. <span data-ttu-id="17904-113">В поле "Тип отпуска" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="17904-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="17904-114">Можно связать тип отпуска с кодом дохода в форме "Типы отпусков".</span><span class="sxs-lookup"><span data-stu-id="17904-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="17904-115">Если тип отпуска связан с кодом дохода, строка дохода будет создаваться со связанным кодом дохода в течение указанного периода отпуска.</span><span class="sxs-lookup"><span data-stu-id="17904-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="17904-116">В списке выберите тип отпуска.</span><span class="sxs-lookup"><span data-stu-id="17904-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="17904-117">Пример: "Усыновление"</span><span class="sxs-lookup"><span data-stu-id="17904-117">For example: Adoption</span></span>  
9. <span data-ttu-id="17904-118">Введите дату начала отпуска.</span><span class="sxs-lookup"><span data-stu-id="17904-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="17904-119">Пример: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="17904-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="17904-120">Пример: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="17904-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="17904-121">Введите дату начала отпуска.</span><span class="sxs-lookup"><span data-stu-id="17904-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="17904-122">Пример: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="17904-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="17904-123">В поле примечаний введите описание.</span><span class="sxs-lookup"><span data-stu-id="17904-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="17904-124">Пример:"Отпуск для усыновления"</span><span class="sxs-lookup"><span data-stu-id="17904-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="17904-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="17904-125">Click Save.</span></span>

