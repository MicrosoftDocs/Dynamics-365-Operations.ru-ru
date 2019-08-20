---
title: Создание расширенных правил для журналов
description: Эта процедура описывает создание дополнительных правил для журналов.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ec0db1bc5018649acaca05c71a510880b415777
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846687"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="bb594-103">Создание расширенных правил для журналов</span><span class="sxs-lookup"><span data-stu-id="bb594-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb594-104">Эта процедура описывает создание дополнительных правил для журналов.</span><span class="sxs-lookup"><span data-stu-id="bb594-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="bb594-105">Сюда входят настройка управления журналом и ограничения разноски по пользователю.</span><span class="sxs-lookup"><span data-stu-id="bb594-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="bb594-106">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="bb594-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="bb594-107">Настройка управления журналом</span><span class="sxs-lookup"><span data-stu-id="bb594-107">Set up journal control</span></span>
1. <span data-ttu-id="bb594-108">Перейдите в раздел "Главная книга" > "Настройка журнала" > "Наименования журналов".</span><span class="sxs-lookup"><span data-stu-id="bb594-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="bb594-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="bb594-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bb594-110">Щелкните "Управление журналом".</span><span class="sxs-lookup"><span data-stu-id="bb594-110">Click Journal control.</span></span>
4. <span data-ttu-id="bb594-111">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="bb594-111">Click Add.</span></span>
5. <span data-ttu-id="bb594-112">В поле "Компании" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bb594-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="bb594-113">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="bb594-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="bb594-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bb594-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="bb594-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="bb594-115">Click Add.</span></span>
9. <span data-ttu-id="bb594-116">В поле "Структура счета" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bb594-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="bb594-117">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="bb594-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="bb594-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bb594-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="bb594-119">В поле "Сегмент" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bb594-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="bb594-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bb594-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="bb594-121">В поле "Со значения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bb594-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="bb594-122">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="bb594-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="bb594-123">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bb594-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="bb594-124">В поле "До значения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bb594-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="bb594-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="bb594-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="bb594-126">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bb594-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="bb594-127">Настройка ограничений разноски</span><span class="sxs-lookup"><span data-stu-id="bb594-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="bb594-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bb594-128">Close the page.</span></span>
2. <span data-ttu-id="bb594-129">Щелкните "Ограничения разноски"</span><span class="sxs-lookup"><span data-stu-id="bb594-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="bb594-130">В пункте "Каким образом настроить ограничения разноски?" выберите "По группе пользователя".</span><span class="sxs-lookup"><span data-stu-id="bb594-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="bb594-131">В дереве установите флажок "Группа, которой следует разрешить разноску для этого наименования журнала".</span><span class="sxs-lookup"><span data-stu-id="bb594-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="bb594-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bb594-132">Click OK.</span></span>

