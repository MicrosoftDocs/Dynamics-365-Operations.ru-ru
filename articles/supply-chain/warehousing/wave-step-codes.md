---
title: Коды шагов волны
description: В этой теме представлен обзор кодов шагов волны и способов их использования.
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c28134b9be92802196b4861cbd20801419ef8d23
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212683"
---
# <a name="wave-step-codes"></a><span data-ttu-id="b4a2b-103">Коды шагов волны</span><span class="sxs-lookup"><span data-stu-id="b4a2b-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4a2b-104">Коды шагов волны — это коды, которые пользователи могут настроить и использовать для связывания определенных экземпляров методов волны с соответствующим шаблоном.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="b4a2b-105">Шаблоны включают шаблоны для пополнения, контейнеризации, печати меток, создания загрузки и сортировки.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="b4a2b-106">Когда коды шагов волны не используются, пользователи должны ввести произвольный текст, чтобы создать ссылку на конкретный шаблон из экземпляра метода волны.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="b4a2b-107">Свободный текст подвержен ошибкам, так как пользователь должен обеспечить, что текст шага волн, добавляемый к конкретному методу шага волны, будет точно соответствовать тексту шага волны в конечном шаблоне.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="b4a2b-108">Коды шагов волны для определенного типа шага волны настраиваются на отдельной странице.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="b4a2b-109">Для каждого экземпляра метода шага волны в шаблоне волны, для которого требуется код шага волны, код шага волны необходимо выбрать в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="b4a2b-110">Выбор в раскрывающемся списке заменяет ввод свободного текста и помогает снизить риск воздействия ошибки человека.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="b4a2b-111">Коды настройки используются для связи метода шага волны в шаблоне волны с целевым шаблоном для метода.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="b4a2b-112">Использование функции кодов шагов волны является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="b4a2b-113">Это включено для организации для всех юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="b4a2b-114">Демонстрация настройки</span><span class="sxs-lookup"><span data-stu-id="b4a2b-114">Setup demo</span></span> 

<span data-ttu-id="b4a2b-115">Для этой демонстрации необходимо установить демонстрационные данные, а также необходимо использовать компанию **USMF** с демонстрационными данными.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="b4a2b-116">Включить коды шагов волны</span><span class="sxs-lookup"><span data-stu-id="b4a2b-116">Enable wave step codes</span></span>

<span data-ttu-id="b4a2b-117">Чтобы включить функцию кодов шагов волны, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="b4a2b-118">Перейдите **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="b4a2b-119">Выберите для включения функции **Код шага волны для организации**.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="b4a2b-120">Все существующие произвольные тексты шагов волны для всех юридических лиц обновляются до новой структуры.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="b4a2b-121">После завершения этого обновления для всех юридических лиц, функция включена.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="b4a2b-122">Если функция не может быть включена для одного или нескольких юридических лиц, то функция не включена для всех юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="b4a2b-123">Во время включения проверки проводятся во время обновления данных.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="b4a2b-124">Если обновление не удается, вы получаете сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="b4a2b-125">Обновление может закончиться ошибкой из-за следующих конфликтов:</span><span class="sxs-lookup"><span data-stu-id="b4a2b-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="b4a2b-126">Существуют повторяющиеся произвольные тексты для шагов волны.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="b4a2b-127">Имеются персональные настройки.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-127">Customizations exist.</span></span>
- <span data-ttu-id="b4a2b-128">Произвольный текст шага волны, связанный с экземпляром метод шага волны, не совпадает с ожидаемым типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="b4a2b-129">После разрешения всех конфликтов, выявленных во время проверок, можно повторно включить функцию.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="b4a2b-130">После включения функции страница **Коды шагов волны** (**Управление складом \> Настройка \> Волны \> Коды шагов волны**) становится доступной.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="b4a2b-131">На этой странице перечислены коды шагов волны, которые были обновлены, когда была включена функция кодов шагов волны организации.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="b4a2b-132">Создание новых кодов шагов волны</span><span class="sxs-lookup"><span data-stu-id="b4a2b-132">Create new wave step codes</span></span>

<span data-ttu-id="b4a2b-133">Можно использовать страницу **Коды шагов волны**, чтобы создавать и удалять коды шагов волны.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="b4a2b-134">Каждый новый код шага волны и связанный с ним идентификатор должны быть уникальными для всех типов шагов волны, и они должны быть определены для конкретного типа шага волны.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="b4a2b-135">Применение кодов шагов волны</span><span class="sxs-lookup"><span data-stu-id="b4a2b-135">Apply wave step codes</span></span>

<span data-ttu-id="b4a2b-136">После определения соответствующих кодов шагов волны они могут применяться к методам обработки волны.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="b4a2b-137">Чтобы применить коды шагов волны, перейдите к соответствующему целевому шаблону.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="b4a2b-138">Ниже приведены целевые шаблоны, на которые направляются коды шагов волны:</span><span class="sxs-lookup"><span data-stu-id="b4a2b-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="b4a2b-139">**Шаблоны пополнения:** Управление складом \> Настройка \> Пополнение \> Шаблоны пополнения</span><span class="sxs-lookup"><span data-stu-id="b4a2b-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="b4a2b-140">**Шаблоны формирования загрузок:** Управление складом \> Настройка \> Загрузка \> Шаблоны формирования загрузок</span><span class="sxs-lookup"><span data-stu-id="b4a2b-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="b4a2b-141">**Сортировка шаблонов:** Управление складом \> Настройка \> Упаковка \> Шаблоны исходящей сортировки</span><span class="sxs-lookup"><span data-stu-id="b4a2b-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="b4a2b-142">**Шаблоны создания контейнера:** Управление складом \> Настройка \> Контейнеры \> Шаблоны создания контейнера</span><span class="sxs-lookup"><span data-stu-id="b4a2b-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="b4a2b-143">**Шаблоны печати этикеток:** Управление складом \> Настройка \> Маршрутизация документов \> Шаблоны печати этикеток</span><span class="sxs-lookup"><span data-stu-id="b4a2b-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="b4a2b-144">Шаблоны из этого списка применяются, когда на них имеются ссылка из метода обработки волны, выбранного в шаблоне волны.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="b4a2b-145">Когда код шага волны в методе обработки полны в шаблоне волны совпадает с кодом шага волны в одном из типов шаблонов, применяется этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="b4a2b-146">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="b4a2b-146">Sample scenario</span></span>

<span data-ttu-id="b4a2b-147">Следующая процедура помогает гарантировать, что созданный шаблон пополнения будет применяться для шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="b4a2b-148">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Коды шагов волны** и создайте код шагов волны для типа **Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="b4a2b-149">Перейдите в раздел **Управление складом \> Настройка \> Пополнение \> Шаблоны пополнения** и создайте шаблон пополнения.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="b4a2b-150">В шаблоне пополнения выберите код шага волны, созданный для типа **Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="b4a2b-151">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны** и выберите шаблон волны, который предполагается использовать.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="b4a2b-152">В этом шаблоне на экспресс-вкладке **Методы** выберите метод **Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="b4a2b-153">В поле **Код шага волны** выберите код шага волны, выбранный в шаблоне пополнения.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="b4a2b-154">Вы выполняете эти действия для каждого юридического лица.</span><span class="sxs-lookup"><span data-stu-id="b4a2b-154">You perform these steps for each legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]