---
title: Настройка журналов амортизации
description: Данная процедура проходит через процесс создания нового журнала амортизации и связывает его с группой основных средств.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0ab7f9332e3224c3dadd62aae532ccffb05c82a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815604"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="7c9ba-103">Настройка журналов амортизации</span><span class="sxs-lookup"><span data-stu-id="7c9ba-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c9ba-104">Данная процедура проходит через процесс создания нового журнала амортизации и связывает его с группой основных средств.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="7c9ba-105">Создание журнала амортизации</span><span class="sxs-lookup"><span data-stu-id="7c9ba-105">Create a depreciation book</span></span>
1. <span data-ttu-id="7c9ba-106">Перейдите в раздел "Основные средства" > "Настройка" > "Журналы амортизации".</span><span class="sxs-lookup"><span data-stu-id="7c9ba-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="7c9ba-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7c9ba-107">Click New.</span></span>
3. <span data-ttu-id="7c9ba-108">В поле "Журнал амортизации" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="7c9ba-109">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7c9ba-110">Установите или снимите флажок "Расчет амортизации".</span><span class="sxs-lookup"><span data-stu-id="7c9ba-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="7c9ba-111">В поле "Метод амортизации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7c9ba-112">В списке найдите требуемый метод амортизации и выберите его.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="7c9ba-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7c9ba-114">В поле "Альтернативный метод амортизации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="7c9ba-115">В списке выберите требуемый метод амортизации.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="7c9ba-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7c9ba-117">Метод дополнительной амортизации используется для дополнительной амортизации основного средства в необычных условиях.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="7c9ba-118">Например, можно использовать это для записи амортизации в результате стихийного бедствия.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="7c9ba-119">Установите или снимите флажок "Создание переоценки амортизации с основными поправками".</span><span class="sxs-lookup"><span data-stu-id="7c9ba-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="7c9ba-120">В поле "Календарь" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="7c9ba-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="7c9ba-122">Связь журнала амортизации с группой основных средств</span><span class="sxs-lookup"><span data-stu-id="7c9ba-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="7c9ba-123">Щелкните "Группы ОС".</span><span class="sxs-lookup"><span data-stu-id="7c9ba-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="7c9ba-124">В поле "Группа ОС" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7c9ba-125">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7c9ba-126">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7c9ba-127">В поле "Соглашение по амортизации" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="7c9ba-128">В поле "Срок службы" введите число.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="7c9ba-129">Обратите внимание, что значение поля "Периоды амортизации" рассчитывается после настройки срока службы.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]