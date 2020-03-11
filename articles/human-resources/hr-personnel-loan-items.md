---
title: Управление номенклатурами, выданным работникам во временное пользование
description: Арендованные номенклатуры для временного пользования — это записи, позволяющие менеджерам отслеживать физические номенклатуры, сдаваемые организацией в аренду работникам.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 02382872b685103810dd7e84cb91eb409df62f66
ms.sourcegitcommit: 880f617d1d6e95eccbed762c7ea04398553c2ec0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036319"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="4a8f1-103">Управление номенклатурами, выданным работникам во временное пользование</span><span class="sxs-lookup"><span data-stu-id="4a8f1-103">Manage items that are lent to workers</span></span>

<span data-ttu-id="4a8f1-104">Арендованные номенклатуры для временного пользования — это записи, позволяющие менеджерам отслеживать физические номенклатуры, сдаваемые организацией в аренду работникам.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="4a8f1-105">Далее приведен список примеров номенклатур, которые компания может сдавать в аренду работникам.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="4a8f1-106">Мобильные телефоны</span><span class="sxs-lookup"><span data-stu-id="4a8f1-106">Mobile telephones</span></span>
-   <span data-ttu-id="4a8f1-107">Автомобили</span><span class="sxs-lookup"><span data-stu-id="4a8f1-107">Automobiles</span></span>
-   <span data-ttu-id="4a8f1-108">Компьютерное оборудование</span><span class="sxs-lookup"><span data-stu-id="4a8f1-108">Computer equipment</span></span>

<span data-ttu-id="4a8f1-109">Каждая физическая номенклатура должна иметь соответствующую номенклатуру временного пользования.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="4a8f1-110">Для каждой записи ссуженной номенклатуры должно быть описано, что было ссужено, кто несет ответственность за ссуду и количество дней, на которые номенклатура была ссужена работнику.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="4a8f1-111">Одновременно можно создать несколько одалживаемых номенклатур, таких как ключи, карточки доступа или комплекты униформы.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="4a8f1-112">При аренде номенклатуры запишите дату предоставления номенклатуры в аренду и планируемую дату возврата.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="4a8f1-113">При возвращении номенклатуры запишите фактическую дату возврата.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="4a8f1-114">Работники могут просматривать записи номенклатур, которые были сданы им в аренду, с помощью рабочей области "Самообслуживание сотрудников".</span><span class="sxs-lookup"><span data-stu-id="4a8f1-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="4a8f1-115">Они могут также редактировать существующие записи или вводить новые сдаваемые в аренду номенклатуры, если они получили дополнительные физические номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="4a8f1-116">Workflow-процесс можно настроить для того, чтобы направить изменения к новым или существующим сдаваемым в аренду номенклатурам через процесс одобрения.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="4a8f1-117">Менеджеры могут просматривать одолженные номенклатуры для своих непосредственных подчиненных.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="4a8f1-118">Им также можно предоставить разрешение добавлять новые сдаваемые в аренду номенклатуры от имени своих работников.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="4a8f1-119">Учет потерянных или замененных ссуженных номенклатур</span><span class="sxs-lookup"><span data-stu-id="4a8f1-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="4a8f1-120">Если номенклатура оказывается поврежденной или замененной, зарегистрируйте воображаемый возврат.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="4a8f1-121">Затем либо удалите номенклатуру, либо сохраните ее в обзоре и измените описание, чтобы показать недоступность номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="4a8f1-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4a8f1-122">Additional resources</span></span>
--------

[<span data-ttu-id="4a8f1-123">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="4a8f1-123">Human resources</span></span>](index.md)



