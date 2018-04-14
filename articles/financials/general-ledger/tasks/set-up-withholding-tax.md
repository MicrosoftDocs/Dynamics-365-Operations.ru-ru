--- 
title: "Настройка подоходного налога"
description: "Подоходный налог — это налог на поставщиков, который не приводит к созданию налоговых проводок."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ccaccd7b5b32431ac463925c887324a7607ae7dc
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="fe679-103">Настройка подоходного налога</span><span class="sxs-lookup"><span data-stu-id="fe679-103">Set up withholding tax</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fe679-104">Подоходный налог — это налог на поставщиков, который не приводит к созданию налоговых проводок.</span><span class="sxs-lookup"><span data-stu-id="fe679-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="fe679-105">Подоходный налог, рассчитываемый по платежам поставщиков, является задолженностью.</span><span class="sxs-lookup"><span data-stu-id="fe679-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="fe679-106">Поэтому действительными счетами для разноски подоходного налога являются только балансовые счета или счета задолженности.</span><span class="sxs-lookup"><span data-stu-id="fe679-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="fe679-107">В этом руководстве по задаче показано, как настроить подоходный налог.</span><span class="sxs-lookup"><span data-stu-id="fe679-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="fe679-108">Перейдите в раздел "Налог" > "Косвенные налоги" > "Подоходный налог" > "Коды подоходного налога".</span><span class="sxs-lookup"><span data-stu-id="fe679-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="fe679-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fe679-109">Click New.</span></span>
3. <span data-ttu-id="fe679-110">В поле "Подоходный налог" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fe679-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="fe679-111">В поле "Имя подоходного налога" введите имя кода подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="fe679-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="fe679-112">В поле "Счет ГК" выберите счет ГК для разноски налоговых обязательств по подоходному налогу.</span><span class="sxs-lookup"><span data-stu-id="fe679-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="fe679-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fe679-113">Click Save.</span></span>
7. <span data-ttu-id="fe679-114">Щелкните "Значение".</span><span class="sxs-lookup"><span data-stu-id="fe679-114">Click Values.</span></span>
8. <span data-ttu-id="fe679-115">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fe679-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="fe679-116">В поле "Значение" введите процент, используемый для расчета подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="fe679-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="fe679-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fe679-117">Click Save.</span></span>
11. <span data-ttu-id="fe679-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fe679-118">Close the page.</span></span>
12. <span data-ttu-id="fe679-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fe679-119">Click Save.</span></span>
13. <span data-ttu-id="fe679-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fe679-120">Close the page.</span></span>
14. <span data-ttu-id="fe679-121">Перейдите в раздел "Налог" > "Косвенные налоги" > "Подоходный налог" > "Группы подоходного налога".</span><span class="sxs-lookup"><span data-stu-id="fe679-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="fe679-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fe679-122">Click New.</span></span>
16. <span data-ttu-id="fe679-123">В поле "Группа подоходного налога" введите код группы подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="fe679-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="fe679-124">В поле "Описание" введите имя группы подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="fe679-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="fe679-125">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fe679-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="fe679-126">В поле "Код подоходного налога" выберите код подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="fe679-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="fe679-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="fe679-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="fe679-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fe679-128">Click Save.</span></span>


