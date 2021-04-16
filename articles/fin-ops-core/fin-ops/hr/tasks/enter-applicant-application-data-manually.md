---
title: Ввод кандидата и данных заявления вручную
description: В этой процедуре показано ведение информации о кандидатах и их заявлениях вручную.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08104729f5be15ef7e727102e7be731bdda1a38c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751990"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="a7b83-103">Ввод кандидата и данных заявления вручную</span><span class="sxs-lookup"><span data-stu-id="a7b83-103">Enter applicant and application data manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7b83-104">В этой процедуре показано ведение информации о кандидатах и их заявлениях вручную.</span><span class="sxs-lookup"><span data-stu-id="a7b83-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="a7b83-105">Можно вводить и обновлять личные данные, даты и время собеседований, рекомендации, компетенции и запросы на удобства кандидатов.</span><span class="sxs-lookup"><span data-stu-id="a7b83-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="a7b83-106">Также можно обновлять статус заявлений кандидатов о приеме на работу и создавать письма или сообщений электронной почты для отправки кандидатам.</span><span class="sxs-lookup"><span data-stu-id="a7b83-106">You can also update the status of applicants' applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="a7b83-107">При создании записи кандидата в глобальной адресной создается запись о лице для этого кандидата.</span><span class="sxs-lookup"><span data-stu-id="a7b83-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="a7b83-108">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="a7b83-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="a7b83-109">Создание новой записи кандидата</span><span class="sxs-lookup"><span data-stu-id="a7b83-109">Create a new applicant record</span></span>
1. <span data-ttu-id="a7b83-110">Перейдите в раздел "Управление персоналом" > "Набор сотрудников" > "Кандидаты" > "Кандидаты".</span><span class="sxs-lookup"><span data-stu-id="a7b83-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="a7b83-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a7b83-111">Click New.</span></span>
3. <span data-ttu-id="a7b83-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a7b83-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="a7b83-113">В поле "Фамилия" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a7b83-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="a7b83-114">Можно ввести дополнительную информацию о кандидате, если таковая имеется.</span><span class="sxs-lookup"><span data-stu-id="a7b83-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="a7b83-115">Например, эта информация может включать в себя ученую степень кандидата, название его текущей должности или предыдущего работодателя.</span><span class="sxs-lookup"><span data-stu-id="a7b83-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="a7b83-116">Переключите развертывание раздела "Контактная информация".</span><span class="sxs-lookup"><span data-stu-id="a7b83-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="a7b83-117">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="a7b83-117">Click Add.</span></span>
7. <span data-ttu-id="a7b83-118">В поле "Описание" введите "Электронная почта для связи".</span><span class="sxs-lookup"><span data-stu-id="a7b83-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="a7b83-119">В поле "Тип" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="a7b83-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="a7b83-120">В поле "Номер/адрес контактного лица" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a7b83-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="a7b83-121">Этот адрес электронной почты будет использоваться для автоматически формируемой электронной переписки с кандидатом.</span><span class="sxs-lookup"><span data-stu-id="a7b83-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="a7b83-122">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="a7b83-122">Click Add.</span></span>
11. <span data-ttu-id="a7b83-123">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a7b83-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="a7b83-124">В поле "Номер/адрес контактного лица" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a7b83-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="a7b83-125">Личные данные кандидата.</span><span class="sxs-lookup"><span data-stu-id="a7b83-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="a7b83-126">При необходимости можно ввести дополнительные личные данные кандидата.</span><span class="sxs-lookup"><span data-stu-id="a7b83-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="a7b83-127">Например, это может быть дата рождения, этническое происхождение, пол или семейное положение.</span><span class="sxs-lookup"><span data-stu-id="a7b83-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="a7b83-128">В области действий щелкните "Компетенции".</span><span class="sxs-lookup"><span data-stu-id="a7b83-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="a7b83-129">Можно ввести профиль компетенции кандидата, включая его навыки, профессиональный опыт, образование, сданные тесты или полученные сертификаты.</span><span class="sxs-lookup"><span data-stu-id="a7b83-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="a7b83-130">Эту информацию можно использовать для сопоставления навыков кандидата с навыками, связанными с должностями, определенными в данных вашей компании.</span><span class="sxs-lookup"><span data-stu-id="a7b83-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="a7b83-131">Создание заявления для кандидата</span><span class="sxs-lookup"><span data-stu-id="a7b83-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="a7b83-132">Щелкните "Заявления".</span><span class="sxs-lookup"><span data-stu-id="a7b83-132">Click Applications.</span></span>
2. <span data-ttu-id="a7b83-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a7b83-133">Click New.</span></span>
3. <span data-ttu-id="a7b83-134">В поле "Проект по набору сотрудников" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a7b83-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a7b83-135">При выборе проекта по набору сотрудников кандидат связывается с конкретной вакансией, входящей в этот проект по набору сотрудников.</span><span class="sxs-lookup"><span data-stu-id="a7b83-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="a7b83-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a7b83-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a7b83-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a7b83-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a7b83-138">По умолчанию должность и подразделение основываются на выбранном проекте по набору сотрудников.</span><span class="sxs-lookup"><span data-stu-id="a7b83-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="a7b83-139">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a7b83-139">Click Save.</span></span>
    * <span data-ttu-id="a7b83-140">После сохранения заявления в него можно вложить документы, в том числе опыт кандидата, поощрения и сопроводительное письмо.</span><span class="sxs-lookup"><span data-stu-id="a7b83-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]