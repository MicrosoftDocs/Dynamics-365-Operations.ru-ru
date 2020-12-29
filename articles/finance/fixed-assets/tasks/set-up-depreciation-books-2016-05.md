---
title: Настройка журналов амортизации
description: Данная процедура проходит через процесс создания нового журнала амортизации и связывает его с группой основных средств.
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
ms.openlocfilehash: 03f915fa91e0eeff2f26ab9a60bbd5118317e853
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447274"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="0cafb-103">Настройка журналов амортизации</span><span class="sxs-lookup"><span data-stu-id="0cafb-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0cafb-104">Данная процедура проходит через процесс создания нового журнала амортизации и связывает его с группой основных средств.</span><span class="sxs-lookup"><span data-stu-id="0cafb-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="0cafb-105">Создание журнала амортизации</span><span class="sxs-lookup"><span data-stu-id="0cafb-105">Create a depreciation book</span></span>
1. <span data-ttu-id="0cafb-106">Перейдите в раздел "Основные средства" > "Настройка" > "Журналы амортизации".</span><span class="sxs-lookup"><span data-stu-id="0cafb-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="0cafb-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="0cafb-107">Click New.</span></span>
3. <span data-ttu-id="0cafb-108">В поле "Журнал амортизации" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0cafb-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="0cafb-109">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0cafb-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0cafb-110">Установите или снимите флажок "Расчет амортизации".</span><span class="sxs-lookup"><span data-stu-id="0cafb-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="0cafb-111">В поле "Метод амортизации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="0cafb-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0cafb-112">В списке найдите требуемый метод амортизации и выберите его.</span><span class="sxs-lookup"><span data-stu-id="0cafb-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="0cafb-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="0cafb-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0cafb-114">В поле "Альтернативный метод амортизации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="0cafb-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="0cafb-115">В списке выберите требуемый метод амортизации.</span><span class="sxs-lookup"><span data-stu-id="0cafb-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="0cafb-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="0cafb-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0cafb-117">Метод дополнительной амортизации используется для дополнительной амортизации основного средства в необычных условиях.</span><span class="sxs-lookup"><span data-stu-id="0cafb-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="0cafb-118">Например, можно использовать это для записи амортизации в результате стихийного бедствия.</span><span class="sxs-lookup"><span data-stu-id="0cafb-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="0cafb-119">Установите или снимите флажок "Создание переоценки амортизации с основными поправками".</span><span class="sxs-lookup"><span data-stu-id="0cafb-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="0cafb-120">В поле "Календарь" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="0cafb-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="0cafb-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="0cafb-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="0cafb-122">Связь журнала амортизации с группой основных средств</span><span class="sxs-lookup"><span data-stu-id="0cafb-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="0cafb-123">Щелкните "Группы ОС".</span><span class="sxs-lookup"><span data-stu-id="0cafb-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="0cafb-124">В поле "Группа ОС" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="0cafb-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0cafb-125">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="0cafb-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0cafb-126">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="0cafb-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0cafb-127">В поле "Соглашение по амортизации" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="0cafb-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="0cafb-128">В поле "Срок службы" введите число.</span><span class="sxs-lookup"><span data-stu-id="0cafb-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="0cafb-129">Обратите внимание, что значение поля "Периоды амортизации" рассчитывается после настройки срока службы.</span><span class="sxs-lookup"><span data-stu-id="0cafb-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

