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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839865"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="f4c96-103">Настройка журнала амортизации (май 2016)</span><span class="sxs-lookup"><span data-stu-id="f4c96-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4c96-104">В этом руководстве по задаче будет создан новый журнал амортизации и связан с группой основных средств.</span><span class="sxs-lookup"><span data-stu-id="f4c96-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="f4c96-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="f4c96-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="f4c96-106">Создание журнала амортизации</span><span class="sxs-lookup"><span data-stu-id="f4c96-106">Create a depreciation book</span></span>
1. <span data-ttu-id="f4c96-107">Перейдите в раздел "Основные средства" > "Настройка" > "Журналы амортизации".</span><span class="sxs-lookup"><span data-stu-id="f4c96-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="f4c96-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f4c96-108">Click New.</span></span>
3. <span data-ttu-id="f4c96-109">В поле "Журнал амортизации" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f4c96-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="f4c96-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f4c96-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f4c96-111">Установите или снимите флажок "Расчет амортизации".</span><span class="sxs-lookup"><span data-stu-id="f4c96-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="f4c96-112">В поле "Метод амортизации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f4c96-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f4c96-113">В списке найдите требуемый метод амортизации и выберите его.</span><span class="sxs-lookup"><span data-stu-id="f4c96-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="f4c96-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f4c96-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f4c96-115">В поле "Альтернативный метод амортизации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f4c96-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f4c96-116">В списке выберите требуемый метод амортизации.</span><span class="sxs-lookup"><span data-stu-id="f4c96-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="f4c96-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f4c96-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f4c96-118">Метод дополнительной амортизации используется для дополнительной амортизации основного средства в необычных условиях.</span><span class="sxs-lookup"><span data-stu-id="f4c96-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="f4c96-119">Например, можно использовать это для записи амортизации в результате стихийного бедствия.</span><span class="sxs-lookup"><span data-stu-id="f4c96-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="f4c96-120">Установите или снимите флажок "Создание переоценки амортизации с основными поправками".</span><span class="sxs-lookup"><span data-stu-id="f4c96-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="f4c96-121">В поле "Календарь" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f4c96-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="f4c96-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f4c96-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="f4c96-123">Связь журнала амортизации с группой основных средств</span><span class="sxs-lookup"><span data-stu-id="f4c96-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="f4c96-124">Щелкните "Группы ОС".</span><span class="sxs-lookup"><span data-stu-id="f4c96-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="f4c96-125">В поле "Группа ОС" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f4c96-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f4c96-126">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="f4c96-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f4c96-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f4c96-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f4c96-128">В поле "Соглашение по амортизации" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="f4c96-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="f4c96-129">В поле "Срок службы" введите число.</span><span class="sxs-lookup"><span data-stu-id="f4c96-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="f4c96-130">Обратите внимание, что значение поля "Периоды амортизации" рассчитывается после настройки срока службы.</span><span class="sxs-lookup"><span data-stu-id="f4c96-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

