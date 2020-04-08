---
title: Создание расширенных правил для журналов
description: Эта процедура описывает создание дополнительных правил для журналов.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: ea6ca24d27bb5b00bbe31060ce2f7e40bf2fb335
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145224"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="2bfdb-103">Создание расширенных правил для журналов</span><span class="sxs-lookup"><span data-stu-id="2bfdb-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2bfdb-104">Эта процедура описывает создание дополнительных правил для журналов.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="2bfdb-105">Сюда входят настройка управления журналом и ограничения разноски по пользователю.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="2bfdb-106">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="2bfdb-107">Настройка управления журналом</span><span class="sxs-lookup"><span data-stu-id="2bfdb-107">Set up journal control</span></span>
1. <span data-ttu-id="2bfdb-108">В **области перехода** выберите **Модули > Главная книга > Настройки журнала > Наименования журналов**.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="2bfdb-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2bfdb-110">На **панели операций** щелкните **Проверка журнала**.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="2bfdb-111">На экспресс-вкладке **Какие типы счетов можно разнести** щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="2bfdb-112">В поле **Компании** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2bfdb-113">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2bfdb-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2bfdb-115">На экспресс-вкладке **Какие значения сегмента являются допустимыми для этого журнала** щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="2bfdb-116">В поле **Структура счета** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="2bfdb-117">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="2bfdb-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="2bfdb-119">В поле **Сегмент** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="2bfdb-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="2bfdb-121">В поле **Со значения** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="2bfdb-122">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="2bfdb-123">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="2bfdb-124">В поле **До значения** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="2bfdb-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="2bfdb-126">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="2bfdb-127">Настройка ограничений разноски</span><span class="sxs-lookup"><span data-stu-id="2bfdb-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="2bfdb-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-128">Close the page.</span></span>
2. <span data-ttu-id="2bfdb-129">Щелкните **Ограничения разноски**.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="2bfdb-130">В пункте **Каким образом настроить ограничения разноски?** выберите "По группе пользователя".</span><span class="sxs-lookup"><span data-stu-id="2bfdb-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="2bfdb-131">В дереве установите флажок "Группа, которой следует разрешить разноску для этого наименования журнала".</span><span class="sxs-lookup"><span data-stu-id="2bfdb-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="2bfdb-132">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="2bfdb-132">Click **OK**.</span></span>

