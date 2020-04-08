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
ms.openlocfilehash: 002700ae7f6474b48fbe09cb3aaa72e9516b8224
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143568"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="e91ca-103">Управление отпуском</span><span class="sxs-lookup"><span data-stu-id="e91ca-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e91ca-104">В этой процедуре показано, как создать записи отпуска сотрудника.</span><span class="sxs-lookup"><span data-stu-id="e91ca-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="e91ca-105">Отслеживать время отпуска можно по причинам, связанным с медициной, образованием или родительскими мероприятиями.</span><span class="sxs-lookup"><span data-stu-id="e91ca-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="e91ca-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="e91ca-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="e91ca-107">Перейдите в раздел "Управление персоналом" > "Работники" > "Сотрудники".</span><span class="sxs-lookup"><span data-stu-id="e91ca-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="e91ca-108">В списке выберите сотрудника.</span><span class="sxs-lookup"><span data-stu-id="e91ca-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="e91ca-109">Отобразите подробные сведения для выбранного сотрудника, выбрав имя сотрудника.</span><span class="sxs-lookup"><span data-stu-id="e91ca-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="e91ca-110">Перейдите на вкладку "Занятость".</span><span class="sxs-lookup"><span data-stu-id="e91ca-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="e91ca-111">Щелкните "Отпуск".</span><span class="sxs-lookup"><span data-stu-id="e91ca-111">Click Leave.</span></span>
6. <span data-ttu-id="e91ca-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e91ca-112">Click New.</span></span>
7. <span data-ttu-id="e91ca-113">В поле "Тип отпуска" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e91ca-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e91ca-114">Можно связать тип отпуска с кодом дохода в форме "Типы отпусков".</span><span class="sxs-lookup"><span data-stu-id="e91ca-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="e91ca-115">Если тип отпуска связан с кодом дохода, строка дохода будет создаваться со связанным кодом дохода в течение указанного периода отпуска.</span><span class="sxs-lookup"><span data-stu-id="e91ca-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="e91ca-116">В списке выберите тип отпуска.</span><span class="sxs-lookup"><span data-stu-id="e91ca-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="e91ca-117">Пример: "Усыновление"</span><span class="sxs-lookup"><span data-stu-id="e91ca-117">For example: Adoption</span></span>  
9. <span data-ttu-id="e91ca-118">Введите дату начала отпуска.</span><span class="sxs-lookup"><span data-stu-id="e91ca-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="e91ca-119">Пример: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="e91ca-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="e91ca-120">Пример: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="e91ca-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="e91ca-121">Введите дату начала отпуска.</span><span class="sxs-lookup"><span data-stu-id="e91ca-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="e91ca-122">Пример: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="e91ca-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="e91ca-123">В поле примечаний введите описание.</span><span class="sxs-lookup"><span data-stu-id="e91ca-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="e91ca-124">Пример:"Отпуск для усыновления"</span><span class="sxs-lookup"><span data-stu-id="e91ca-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="e91ca-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e91ca-125">Click Save.</span></span>

