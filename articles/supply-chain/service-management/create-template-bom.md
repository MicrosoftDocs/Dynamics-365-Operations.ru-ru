---
title: Создание шаблона спецификации
description: Можно создать шаблон спецификации, используя множество методов.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b34cc2e9921df6e3ef619e2b2adaf8d2069fbac
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974568"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="6e00b-103">Создание шаблона спецификации</span><span class="sxs-lookup"><span data-stu-id="6e00b-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6e00b-104">Можно создать шаблон спецификации, используя любой из перечисленных ниже методов.</span><span class="sxs-lookup"><span data-stu-id="6e00b-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="6e00b-105">Для всех методов поля **Дата начала** и **Дата окончания** необязательны, они предназначены только для сведений.</span><span class="sxs-lookup"><span data-stu-id="6e00b-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="6e00b-106">Создание шаблона спецификации вручную</span><span class="sxs-lookup"><span data-stu-id="6e00b-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="6e00b-107">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6e00b-108">Нажмите клавиши CTRL+N, чтобы открыть форму **Создать шаблон спецификации**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6e00b-109">В разделе **Копировать строки спецификации из ссылки** выберите параметр **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="6e00b-110">В поле **Код номенклатуры** введите номенклатуру типа **Спецификация**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="6e00b-111">В поле **Имя** введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="6e00b-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6e00b-112">В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.</span><span class="sxs-lookup"><span data-stu-id="6e00b-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6e00b-113">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-113">Click **OK**.</span></span>

<span data-ttu-id="6e00b-114">Будет создан новый пустой шаблон спецификации.</span><span class="sxs-lookup"><span data-stu-id="6e00b-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="6e00b-115">Создание шаблона спецификации на основе другого шаблона спецификации</span><span class="sxs-lookup"><span data-stu-id="6e00b-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="6e00b-116">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6e00b-117">Нажмите клавиши CTRL+N, чтобы открыть форму **Создать шаблон спецификации**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6e00b-118">В разделе **Копировать строки спецификации из ссылки** выберите параметр **Шаблон спецификации**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="6e00b-119">В поле **Номер ссылки** выберите имеющийся шаблон спецификации, который необходимо скопировать в новый шаблон.</span><span class="sxs-lookup"><span data-stu-id="6e00b-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="6e00b-120">В поле **Имя** введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="6e00b-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6e00b-121">В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.</span><span class="sxs-lookup"><span data-stu-id="6e00b-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6e00b-122">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-122">Click **OK**.</span></span>

<span data-ttu-id="6e00b-123">Будет создан новый шаблон спецификации с использованием строк, которые соответствуют строкам исходного шаблона спецификации.</span><span class="sxs-lookup"><span data-stu-id="6e00b-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="6e00b-124">Создание шаблона спецификации на основе спецификации номенклатуры</span><span class="sxs-lookup"><span data-stu-id="6e00b-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="6e00b-125">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6e00b-126">Нажмите клавиши CTRL+N, чтобы открыть форму **Создать шаблон спецификации**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6e00b-127">В разделе **Копировать строки спецификации из ссылки** выберите **Спецификация**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="6e00b-128">В поле **Номер ссылки** выберите версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="6e00b-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="6e00b-129">Номенклатура типа "Спецификация" будет скопирована в раздел **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="6e00b-130">В поле **Имя** введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="6e00b-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6e00b-131">В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.</span><span class="sxs-lookup"><span data-stu-id="6e00b-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6e00b-132">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-132">Click **OK**.</span></span>

<span data-ttu-id="6e00b-133">Будет создан новый шаблон спецификации с использованием строк, которые будут соответствовать строкам спецификации, перечисленным в форме **Спецификации**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="6e00b-134">Создание шаблона спецификации на основе спецификации производства</span><span class="sxs-lookup"><span data-stu-id="6e00b-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="6e00b-135">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6e00b-136">Нажмите клавиши CTRL+N, чтобы открыть форму **Создать шаблон спецификации**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6e00b-137">В разделе **Копировать строки спецификации из ссылки** выберите **Производство**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="6e00b-138">В поле **Номер ссылки** выберите производственную спецификацию.</span><span class="sxs-lookup"><span data-stu-id="6e00b-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="6e00b-139">В поле **Имя** введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="6e00b-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6e00b-140">В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.</span><span class="sxs-lookup"><span data-stu-id="6e00b-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6e00b-141">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-141">Click **OK**.</span></span>

<span data-ttu-id="6e00b-142">Будет создан новый шаблон спецификации с использованием строк, которые будут соответствовать строкам спецификации, перечисленным в форме **Спецификация**.</span><span class="sxs-lookup"><span data-stu-id="6e00b-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e00b-143">См. также</span><span class="sxs-lookup"><span data-stu-id="6e00b-143">See also</span></span>

[<span data-ttu-id="6e00b-144">Шаблоны спецификаций</span><span class="sxs-lookup"><span data-stu-id="6e00b-144">Template BOMs</span></span>](template-boms.md)

  


