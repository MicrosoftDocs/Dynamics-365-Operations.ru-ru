---
title: Настройка журнала амортизации (май 2016)
description: В этом руководстве по задаче будет создан новый журнал амортизации и связан с группой основных средств.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fd53ea1dff9b116d19c525c5d6967ece0993b6f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "355572"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="664ab-103">Настройка журнала амортизации (май 2016)</span><span class="sxs-lookup"><span data-stu-id="664ab-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="664ab-104">В этом руководстве по задаче будет создан новый журнал амортизации и связан с группой основных средств.</span><span class="sxs-lookup"><span data-stu-id="664ab-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="664ab-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="664ab-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="664ab-106">Создание журнала амортизации</span><span class="sxs-lookup"><span data-stu-id="664ab-106">Create a depreciation book</span></span>
1. <span data-ttu-id="664ab-107">Перейдите в раздел "Основные средства" > "Настройка" > "Журналы амортизации".</span><span class="sxs-lookup"><span data-stu-id="664ab-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="664ab-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="664ab-108">Click New.</span></span>
3. <span data-ttu-id="664ab-109">В поле "Журнал амортизации" введите значение.</span><span class="sxs-lookup"><span data-stu-id="664ab-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="664ab-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="664ab-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="664ab-111">Установите или снимите флажок "Расчет амортизации".</span><span class="sxs-lookup"><span data-stu-id="664ab-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="664ab-112">В поле "Метод амортизации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="664ab-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="664ab-113">В списке найдите требуемый метод амортизации и выберите его.</span><span class="sxs-lookup"><span data-stu-id="664ab-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="664ab-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="664ab-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="664ab-115">В поле "Альтернативный метод амортизации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="664ab-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="664ab-116">В списке выберите требуемый метод амортизации.</span><span class="sxs-lookup"><span data-stu-id="664ab-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="664ab-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="664ab-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="664ab-118">Метод дополнительной амортизации используется для дополнительной амортизации основного средства в необычных условиях.</span><span class="sxs-lookup"><span data-stu-id="664ab-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="664ab-119">Например, можно использовать это для записи амортизации в результате стихийного бедствия.</span><span class="sxs-lookup"><span data-stu-id="664ab-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="664ab-120">Установите или снимите флажок "Создание переоценки амортизации с основными поправками".</span><span class="sxs-lookup"><span data-stu-id="664ab-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="664ab-121">В поле "Календарь" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="664ab-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="664ab-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="664ab-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="664ab-123">Связь журнала амортизации с группой основных средств</span><span class="sxs-lookup"><span data-stu-id="664ab-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="664ab-124">Щелкните "Группы ОС".</span><span class="sxs-lookup"><span data-stu-id="664ab-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="664ab-125">В поле "Группа ОС" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="664ab-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="664ab-126">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="664ab-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="664ab-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="664ab-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="664ab-128">В поле "Соглашение по амортизации" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="664ab-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="664ab-129">В поле "Срок службы" введите число.</span><span class="sxs-lookup"><span data-stu-id="664ab-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="664ab-130">Обратите внимание, что значение поля "Периоды амортизации" рассчитывается после настройки срока службы.</span><span class="sxs-lookup"><span data-stu-id="664ab-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

