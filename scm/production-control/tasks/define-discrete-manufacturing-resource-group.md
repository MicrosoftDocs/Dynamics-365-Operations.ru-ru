--- 
title: "Определение групп ресурсов для дискретного производства"
description: "Группа ресурсов — это набор операционных ресурсов, которые обычно соответствуют физической организации производственных ячеек, определенных желтыми строками в цехе производства."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2423fe91d1531a326080e3a584195ea864f2e3e
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="05621-103">Определение групп ресурсов для дискретного производства</span><span class="sxs-lookup"><span data-stu-id="05621-103">Define discrete manufacturing resource group</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05621-104">Группа ресурсов — это набор операционных ресурсов, которые обычно соответствуют физической организации производственных ячеек, определенных желтыми строками в цехе производства.</span><span class="sxs-lookup"><span data-stu-id="05621-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="05621-105">Следующая процедура используется для определения группы ресурсов для использования в дискретном производстве.</span><span class="sxs-lookup"><span data-stu-id="05621-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="05621-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="05621-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="05621-107">Перейдите в раздел "Группы ресурсов".</span><span class="sxs-lookup"><span data-stu-id="05621-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="05621-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="05621-108">Click New.</span></span>
3. <span data-ttu-id="05621-109">В поле "Группа ресурсов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="05621-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="05621-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="05621-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="05621-111">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="05621-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="05621-112">В поле "Производственное подразделение" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="05621-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="05621-113">Определение рабочих параметров по умолчанию</span><span class="sxs-lookup"><span data-stu-id="05621-113">Define default operational parameters</span></span>
1. <span data-ttu-id="05621-114">Разверните раздел "Операция".</span><span class="sxs-lookup"><span data-stu-id="05621-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="05621-115">В поле "Процент отходов" введите число.</span><span class="sxs-lookup"><span data-stu-id="05621-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="05621-116">В поле "Категория настройки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="05621-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="05621-117">В поле "Категория времени выполнения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="05621-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="05621-118">В поле "Процент планирования операций" введите число.</span><span class="sxs-lookup"><span data-stu-id="05621-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="05621-119">Определение часов работы</span><span class="sxs-lookup"><span data-stu-id="05621-119">Define operating hours</span></span>
1. <span data-ttu-id="05621-120">Разверните раздел "Календари".</span><span class="sxs-lookup"><span data-stu-id="05621-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="05621-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="05621-121">Click Add.</span></span>
3. <span data-ttu-id="05621-122">В поле "Календарь" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="05621-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="05621-123">Добавление операционных ресурсов</span><span class="sxs-lookup"><span data-stu-id="05621-123">Add operations resources</span></span>
1. <span data-ttu-id="05621-124">Разверните раздел "Ресурсы".</span><span class="sxs-lookup"><span data-stu-id="05621-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="05621-125">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="05621-125">Click Add.</span></span>
3. <span data-ttu-id="05621-126">В поле "Ресурс" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="05621-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="05621-127">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="05621-127">Click Add.</span></span>
5. <span data-ttu-id="05621-128">В поле "Ресурс" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="05621-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="05621-129">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="05621-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="05621-130">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="05621-130">In the list, click the link in the selected row.</span></span>


