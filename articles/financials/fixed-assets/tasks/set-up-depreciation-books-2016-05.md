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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566923"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="aeb7c-103">Настройка журнала амортизации (май 2016)</span><span class="sxs-lookup"><span data-stu-id="aeb7c-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aeb7c-104">В этом руководстве по задаче будет создан новый журнал амортизации и связан с группой основных средств.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="aeb7c-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="aeb7c-106">Создание журнала амортизации</span><span class="sxs-lookup"><span data-stu-id="aeb7c-106">Create a depreciation book</span></span>
1. <span data-ttu-id="aeb7c-107">Перейдите в раздел "Основные средства" > "Настройка" > "Журналы амортизации".</span><span class="sxs-lookup"><span data-stu-id="aeb7c-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="aeb7c-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="aeb7c-108">Click New.</span></span>
3. <span data-ttu-id="aeb7c-109">В поле "Журнал амортизации" введите значение.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="aeb7c-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="aeb7c-111">Установите или снимите флажок "Расчет амортизации".</span><span class="sxs-lookup"><span data-stu-id="aeb7c-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="aeb7c-112">В поле "Метод амортизации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="aeb7c-113">В списке найдите требуемый метод амортизации и выберите его.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="aeb7c-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="aeb7c-115">В поле "Альтернативный метод амортизации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="aeb7c-116">В списке выберите требуемый метод амортизации.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="aeb7c-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aeb7c-118">Метод дополнительной амортизации используется для дополнительной амортизации основного средства в необычных условиях.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="aeb7c-119">Например, можно использовать это для записи амортизации в результате стихийного бедствия.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="aeb7c-120">Установите или снимите флажок "Создание переоценки амортизации с основными поправками".</span><span class="sxs-lookup"><span data-stu-id="aeb7c-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="aeb7c-121">В поле "Календарь" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="aeb7c-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="aeb7c-123">Связь журнала амортизации с группой основных средств</span><span class="sxs-lookup"><span data-stu-id="aeb7c-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="aeb7c-124">Щелкните "Группы ОС".</span><span class="sxs-lookup"><span data-stu-id="aeb7c-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="aeb7c-125">В поле "Группа ОС" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="aeb7c-126">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="aeb7c-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="aeb7c-128">В поле "Соглашение по амортизации" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="aeb7c-129">В поле "Срок службы" введите число.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="aeb7c-130">Обратите внимание, что значение поля "Периоды амортизации" рассчитывается после настройки срока службы.</span><span class="sxs-lookup"><span data-stu-id="aeb7c-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

