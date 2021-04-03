---
title: Добавление данных в журнал производительности и отправка похвалы другому пользователю
description: Журнал производительности содержит информацию, относящуюся к тому, насколько вы соответствуете целям или как хорошо вы работали во время периода.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EssWorkspace, HcmPerfJournal, HcmPerfJournalAddLink, HcmPerfPraise, HcmWorkerLookUpByPerson, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a865ee37ed650c564961f6b3dd8773eea4f7b9ea
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465638"
---
# <a name="add-to-your-performance-journal-and-send-praise-to-someone"></a><span data-ttu-id="96eca-103">Добавление данных в журнал производительности и отправка похвалы другому пользователю</span><span class="sxs-lookup"><span data-stu-id="96eca-103">Add to your performance journal and send praise to someone</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="96eca-104">Журнал производительности содержит информацию, относящуюся к тому, насколько вы соответствуете целям или как хорошо вы работали во время периода.</span><span class="sxs-lookup"><span data-stu-id="96eca-104">The performance journal holds information that relates to how you met your goals or how you performed during a period.</span></span> <span data-ttu-id="96eca-105">Можно также похвалить действий сотрудника из журнала.</span><span class="sxs-lookup"><span data-stu-id="96eca-105">You can also praise the actions of a co-worker from the journal.</span></span> <span data-ttu-id="96eca-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="96eca-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="96eca-107">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="96eca-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="96eca-108">Перейдите в раздел "Все рабочие области" > "Самообслуживание сотрудников".</span><span class="sxs-lookup"><span data-stu-id="96eca-108">Go to All workspaces > Employee self service.</span></span>
2. <span data-ttu-id="96eca-109">Щелкните "Журнал показателей производительности".</span><span class="sxs-lookup"><span data-stu-id="96eca-109">Click Performance journal.</span></span>
3. <span data-ttu-id="96eca-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="96eca-110">Click New.</span></span>
4. <span data-ttu-id="96eca-111">В поле "Заголовок" введите значение.</span><span class="sxs-lookup"><span data-stu-id="96eca-111">In the Title field, type a value.</span></span>
5. <span data-ttu-id="96eca-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="96eca-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="96eca-113">Дата журнала производительности — это дата создания журнала.</span><span class="sxs-lookup"><span data-stu-id="96eca-113">The performance journal date is the date that the journal was created.</span></span>  
    * <span data-ttu-id="96eca-114">Источник представляет, откуда появился журнал производительности.</span><span class="sxs-lookup"><span data-stu-id="96eca-114">The source represents where the performance journal came from.</span></span> <span data-ttu-id="96eca-115">Когда вы создаете журнал, он создается из пункта "Мой журнал".</span><span class="sxs-lookup"><span data-stu-id="96eca-115">When you create one, it comes from My journal.</span></span> <span data-ttu-id="96eca-116">Если менеджер создает журнал, он берется из пункта "Журналы менеджера".</span><span class="sxs-lookup"><span data-stu-id="96eca-116">If your manager creates one, it comes from the Manager journal.</span></span>  
    * <span data-ttu-id="96eca-117">Можно предоставить доступ к журналу своему менеджеру или сделать его видимым только вам.</span><span class="sxs-lookup"><span data-stu-id="96eca-117">You can share this journal with your manager or make it only visible to you.</span></span>  
6. <span data-ttu-id="96eca-118">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="96eca-118">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="96eca-119">В поле "Дата завершения" введите дату.</span><span class="sxs-lookup"><span data-stu-id="96eca-119">In the Date completed field, enter a date.</span></span>
8. <span data-ttu-id="96eca-120">Выберите "Да" в поле "План развития".</span><span class="sxs-lookup"><span data-stu-id="96eca-120">Select Yes in the Development plan field.</span></span>
9. <span data-ttu-id="96eca-121">В поле "Ключевые слова" введите значение.</span><span class="sxs-lookup"><span data-stu-id="96eca-121">In the Keywords field, type a value.</span></span>
10. <span data-ttu-id="96eca-122">Щелкните "Добавить внешнюю ссылку".</span><span class="sxs-lookup"><span data-stu-id="96eca-122">Click Add external link.</span></span>
11. <span data-ttu-id="96eca-123">В поле "Описание" введите "Envision".</span><span class="sxs-lookup"><span data-stu-id="96eca-123">In the Description field, type 'Envision'.</span></span>
12. <span data-ttu-id="96eca-124">В поле "Веб-адрес" введите "https://www.microsoft.com/en/envision/default".</span><span class="sxs-lookup"><span data-stu-id="96eca-124">In the Internet address field, type 'https://www.microsoft.com/en/envision/default'.</span></span>
13. <span data-ttu-id="96eca-125">Нажмите на заголовок под кнопкой "Сохранить" с называнием "Журнал производительности" для возврата в сетку.</span><span class="sxs-lookup"><span data-stu-id="96eca-125">Click on the caption below the Save button called "Performance journal" to return to the grid.</span></span>
    * <span data-ttu-id="96eca-126">Можно добавить выбранный журнал или журналы к цели, чтобы они отображались при открытии цели.</span><span class="sxs-lookup"><span data-stu-id="96eca-126">You can add the selected journal or journals to a goal so that it appears when you open the goal.</span></span> <span data-ttu-id="96eca-127">На экспресс-вкладку "Ссылки" добавляется ссылка. Если добавить журнал к цели а затем добавить цель к оценке, журнал будет отображаться в оценке автоматически.</span><span class="sxs-lookup"><span data-stu-id="96eca-127">A link will be added in the Links fast tab.    If you add a journal to a goal and then add the goal to a review, the journal will appear on the review automatically.</span></span>  
    * <span data-ttu-id="96eca-128">Можно добавить выбранный журнал или журналы к оценке, чтобы они отображались при открытии оценки.</span><span class="sxs-lookup"><span data-stu-id="96eca-128">You can add the selected journal or journals to a review so that it appears when you open the review.</span></span>    <span data-ttu-id="96eca-129">Ссылка добавляется на экспресс-вкладку "Ссылки".</span><span class="sxs-lookup"><span data-stu-id="96eca-129">A link will be added in the Links fast tab.</span></span>  
14. <span data-ttu-id="96eca-130">Щелкните "Быстрое добавление".</span><span class="sxs-lookup"><span data-stu-id="96eca-130">Click Quick add.</span></span>
15. <span data-ttu-id="96eca-131">В поле "Заголовок" введите значение.</span><span class="sxs-lookup"><span data-stu-id="96eca-131">In the Title field, type a value.</span></span>
16. <span data-ttu-id="96eca-132">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="96eca-132">In the Description field, type a value.</span></span>
17. <span data-ttu-id="96eca-133">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="96eca-133">Click Save.</span></span>
18. <span data-ttu-id="96eca-134">Щелкните "Отправить благодарность".</span><span class="sxs-lookup"><span data-stu-id="96eca-134">Click Send praise.</span></span>
19. <span data-ttu-id="96eca-135">Выберите человека в списке сотрудников компании.</span><span class="sxs-lookup"><span data-stu-id="96eca-135">Select a person from the list of employees in the company.</span></span>
20. <span data-ttu-id="96eca-136">В поле "Описание" введите "Спасибо для большую помощь на конференции!".</span><span class="sxs-lookup"><span data-stu-id="96eca-136">In the Description field, enter 'Thanks for all the help at the conference!'.</span></span>
21. <span data-ttu-id="96eca-137">Нажмите кнопку Отправить.</span><span class="sxs-lookup"><span data-stu-id="96eca-137">Click Send.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]