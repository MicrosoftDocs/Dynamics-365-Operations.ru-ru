---
title: Коды шагов волны
description: В этой теме представлен обзор кодов шагов волны и способов их использования.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992365"
---
# <a name="wave-step-codes"></a><span data-ttu-id="3bcbc-103">Коды шагов волны</span><span class="sxs-lookup"><span data-stu-id="3bcbc-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="3bcbc-104">О кодах шагов волны</span><span class="sxs-lookup"><span data-stu-id="3bcbc-104">About wave step codes</span></span>

<span data-ttu-id="3bcbc-105">Коды шагов волны — это коды, которые пользователи могут настроить и использовать для связывания определенных экземпляров методов волны с соответствующим шаблоном.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="3bcbc-106">Шаблоны включают шаблоны для пополнения, контейнеризации, печати меток, создания загрузки и сортировки.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="3bcbc-107">Когда коды шагов волны не используются, пользователи должны ввести произвольный текст, чтобы создать ссылку на конкретный шаблон из экземпляра метода волны.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="3bcbc-108">Свободный текст подвержен ошибкам, так как пользователь должен обеспечить, что текст шага волн, добавляемый к конкретному методу шага волны, будет точно соответствовать тексту шага волны в конечном шаблоне.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="3bcbc-109">Коды шагов волны для определенного типа шага волны настраиваются на отдельной странице.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="3bcbc-110">Для каждого экземпляра метода шага волны в шаблоне волны, для которого требуется код шага волны, код шага волны необходимо выбрать в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="3bcbc-111">Выбор в раскрывающемся списке заменяет ввод свободного текста и помогает снизить риск воздействия ошибки человека.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="3bcbc-112">Коды настройки используются для связи метода шага волны в шаблоне волны с целевым шаблоном для метода.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="3bcbc-113">Использование функции кодов шагов волны не является обязательным, обновление выполняется отдельно для каждого юридического лица.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="3bcbc-114">Таким образом, если конкретное юридическое лицо использует эту функцию, все существующие коды шагов волны в этом юридическом лице будут обновлены до новой структуры.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="3bcbc-115">Демонстрация настройки</span><span class="sxs-lookup"><span data-stu-id="3bcbc-115">Setup demo</span></span> 

<span data-ttu-id="3bcbc-116">Для этой демонстрации необходимо установить демонстрационные данные, а также необходимо использовать компанию **USMF** с демонстрационными данными.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="3bcbc-117">Включить коды шагов волны</span><span class="sxs-lookup"><span data-stu-id="3bcbc-117">Enable wave step codes</span></span>

<span data-ttu-id="3bcbc-118">Чтобы включить функцию кодов шагов волны, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="3bcbc-119">Перейдите в раздел **Управление складом \> Настройка \> Параметры управления складом**.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="3bcbc-120">На вкладке **Общее** на экспресс-вкладке **Обработка волны** установите параметр **Включить коды шагов волны** в значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="3bcbc-121">Все существующие произвольные тексты шагов волны обновляются до новой структуры.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="3bcbc-122">После завершения этого обновления для юридического лица параметр **Включить коды шагов волны** больше не доступен на странице **Параметры управления складом**.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="3bcbc-123">Проверки выполняются во время обновления, и если обновление завершилось с ошибкой, выводится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="3bcbc-124">Обновление может закончиться ошибкой из-за следующих конфликтов:</span><span class="sxs-lookup"><span data-stu-id="3bcbc-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="3bcbc-125">Существуют повторяющиеся произвольные тексты для шагов волны.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="3bcbc-126">Имеются персональные настройки.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-126">Customizations exist.</span></span>
- <span data-ttu-id="3bcbc-127">Произвольный текст шага волны, связанный с экземпляром метод шага волны, не совпадает с ожидаемым типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="3bcbc-128">После разрешения всех конфликтов, выявленных во время проверок, можно повторно выполнить процесс обновления.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="3bcbc-129">После успешного выполнения страница **Коды шагов волны** (**Управление складом \> Настройка \> Волны \> Коды шагов волны**) становится доступной.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="3bcbc-130">На этой странице перечислены коды шагов волны, которые были обновлены, когда была включена функция кодов шагов волны.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="3bcbc-131">Создание новых кодов шагов волны</span><span class="sxs-lookup"><span data-stu-id="3bcbc-131">Create new wave step codes</span></span>

<span data-ttu-id="3bcbc-132">Можно использовать страницу **Коды шагов волны**, чтобы создавать и удалять коды шагов волны.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="3bcbc-133">Каждый новый код шага волны и связанный с ним идентификатор должны быть уникальными для всех типов шагов волны, и они должны быть определены для конкретного типа шага волны.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="3bcbc-134">Применение кодов шагов волны</span><span class="sxs-lookup"><span data-stu-id="3bcbc-134">Apply wave step codes</span></span>

<span data-ttu-id="3bcbc-135">После определения соответствующих кодов шагов волны они могут применяться к методам обработки волны.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="3bcbc-136">Чтобы применить коды шагов волны, перейдите к соответствующему целевому шаблону.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="3bcbc-137">Ниже приведены целевые шаблоны, на которые направляются коды шагов волны:</span><span class="sxs-lookup"><span data-stu-id="3bcbc-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="3bcbc-138">**Шаблоны пополнения:** Управление складом \> Настройка \> Пополнение \> Шаблоны пополнения</span><span class="sxs-lookup"><span data-stu-id="3bcbc-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="3bcbc-139">**Шаблоны формирования загрузок:** Управление складом \> Настройка \> Загрузка \> Шаблоны формирования загрузок</span><span class="sxs-lookup"><span data-stu-id="3bcbc-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="3bcbc-140">**Сортировка шаблонов:** Управление складом \> Настройка \> Упаковка \> Шаблоны исходящей сортировки</span><span class="sxs-lookup"><span data-stu-id="3bcbc-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="3bcbc-141">**Шаблоны создания контейнера:** Управление складом \> Настройка \> Контейнеры \> Шаблоны создания контейнера</span><span class="sxs-lookup"><span data-stu-id="3bcbc-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="3bcbc-142">**Шаблоны печати этикеток:** Управление складом \> Настройка \> Маршрутизация документов \> Шаблоны печати этикеток</span><span class="sxs-lookup"><span data-stu-id="3bcbc-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="3bcbc-143">Шаблоны из этого списка применяются, когда на них имеются ссылка из метода обработки волны, выбранного в шаблоне волны.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="3bcbc-144">Когда код шага волны в методе обработки полны в шаблоне волны совпадает с кодом шага волны в одном из типов шаблонов, применяется этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="3bcbc-145">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="3bcbc-145">Sample scenario</span></span>

<span data-ttu-id="3bcbc-146">Следующая процедура помогает гарантировать, что созданный шаблон пополнения будет применяться для шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="3bcbc-147">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Коды шагов волны** и создайте код шагов волны для типа **Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="3bcbc-148">Перейдите в раздел **Управление складом \> Настройка \> Пополнение \> Шаблоны пополнения** и создайте шаблон пополнения.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="3bcbc-149">В шаблоне пополнения выберите код шага волны, созданный для типа **Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="3bcbc-150">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны** и выберите шаблон волны, который предполагается использовать.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="3bcbc-151">В этом шаблоне на экспресс-вкладке **Методы** выберите метод **Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="3bcbc-152">В поле **Код шага волны** выберите код шага волны, выбранный в шаблоне пополнения.</span><span class="sxs-lookup"><span data-stu-id="3bcbc-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
