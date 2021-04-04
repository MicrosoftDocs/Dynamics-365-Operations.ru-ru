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
ms.openlocfilehash: 5afcb8171b674281faf8100d5c01fdff8d6ff764
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470793"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="0bc03-103">Создание шаблона спецификации</span><span class="sxs-lookup"><span data-stu-id="0bc03-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0bc03-104">Можно создать шаблон спецификации, используя любой из перечисленных ниже методов.</span><span class="sxs-lookup"><span data-stu-id="0bc03-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="0bc03-105">Для всех методов поля **Дата начала** и **Дата окончания** необязательны, они предназначены только для сведений.</span><span class="sxs-lookup"><span data-stu-id="0bc03-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="0bc03-106">Создание шаблона спецификации вручную</span><span class="sxs-lookup"><span data-stu-id="0bc03-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="0bc03-107">Перейдите **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0bc03-108">Выберите **Создать**, чтобы открыть форму **Создать шаблон спецификации**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0bc03-109">В разделе **Копировать строки спецификации из ссылки** выберите параметр **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="0bc03-110">В поле **Код номенклатуры** введите номенклатуру типа **Спецификация**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="0bc03-111">В поле **Имя** введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="0bc03-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0bc03-112">В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.</span><span class="sxs-lookup"><span data-stu-id="0bc03-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0bc03-113">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-113">Select **OK**.</span></span>

<span data-ttu-id="0bc03-114">Будет создан новый пустой шаблон спецификации.</span><span class="sxs-lookup"><span data-stu-id="0bc03-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="0bc03-115">Создание шаблона спецификации на основе другого шаблона спецификации</span><span class="sxs-lookup"><span data-stu-id="0bc03-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="0bc03-116">Выберите **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0bc03-117">Выберите **Создать**, чтобы открыть форму **Создать шаблон спецификации**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0bc03-118">В разделе **Копировать строки спецификации из ссылки** выберите параметр **Шаблон спецификации**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="0bc03-119">В поле **Номер ссылки** выберите имеющийся шаблон спецификации, который необходимо скопировать в новый шаблон.</span><span class="sxs-lookup"><span data-stu-id="0bc03-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="0bc03-120">В поле **Имя** введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="0bc03-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0bc03-121">В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.</span><span class="sxs-lookup"><span data-stu-id="0bc03-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0bc03-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-122">Select **OK**.</span></span>

<span data-ttu-id="0bc03-123">Будет создан новый шаблон спецификации с использованием строк, которые соответствуют строкам исходного шаблона спецификации.</span><span class="sxs-lookup"><span data-stu-id="0bc03-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="0bc03-124">Создание шаблона спецификации на основе спецификации номенклатуры</span><span class="sxs-lookup"><span data-stu-id="0bc03-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="0bc03-125">Выберите **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0bc03-126">Выберите **Создать**, чтобы открыть форму **Создать шаблон спецификации**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0bc03-127">В разделе **Копировать строки спецификации из ссылки** выберите **Спецификация**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="0bc03-128">В поле **Номер ссылки** выберите версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="0bc03-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="0bc03-129">Номенклатура типа "Спецификация" будет скопирована в раздел **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="0bc03-130">В поле **Имя** введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="0bc03-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0bc03-131">В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.</span><span class="sxs-lookup"><span data-stu-id="0bc03-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0bc03-132">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-132">Select **OK**.</span></span>

<span data-ttu-id="0bc03-133">Будет создан новый шаблон спецификации с использованием строк, которые будут соответствовать строкам спецификации, перечисленным в форме **Спецификации**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="0bc03-134">Создание шаблона спецификации на основе спецификации производства</span><span class="sxs-lookup"><span data-stu-id="0bc03-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="0bc03-135">Выберите **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0bc03-136">Выберите **Создать**, чтобы открыть форму **Создать шаблон спецификации**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0bc03-137">В разделе **Копировать строки спецификации из ссылки** выберите **Производство**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="0bc03-138">В поле **Номер ссылки** выберите производственную спецификацию.</span><span class="sxs-lookup"><span data-stu-id="0bc03-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="0bc03-139">В поле **Имя** введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="0bc03-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0bc03-140">В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.</span><span class="sxs-lookup"><span data-stu-id="0bc03-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0bc03-141">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-141">Select **OK**.</span></span>

<span data-ttu-id="0bc03-142">Будет создан новый шаблон спецификации с использованием строк, которые будут соответствовать строкам спецификации, перечисленным в форме **Спецификация**.</span><span class="sxs-lookup"><span data-stu-id="0bc03-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="0bc03-143">См. также</span><span class="sxs-lookup"><span data-stu-id="0bc03-143">See also</span></span>

[<span data-ttu-id="0bc03-144">Шаблоны спецификаций</span><span class="sxs-lookup"><span data-stu-id="0bc03-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]