---
title: Параметры покрытия
description: В этой теме приводятся сведения о параметрах покрытия, которые сводное планирование использует для расчета потребностей в номенклатуре.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ab86db68ddfebe0ffdce26e062defc16c848a1d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240421"
---
# <a name="coverage-settings"></a><span data-ttu-id="198d1-103">Параметры покрытия</span><span class="sxs-lookup"><span data-stu-id="198d1-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="198d1-104">При сводном планировании для вычисления потребностей в номенклатуре используются параметры покрытия.</span><span class="sxs-lookup"><span data-stu-id="198d1-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="198d1-105">Параметры покрытия можно задать несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="198d1-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="198d1-106">Определение параметров покрытия для группы покрытия.</span><span class="sxs-lookup"><span data-stu-id="198d1-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="198d1-107">Можно создать группу покрытия, которая содержит настройки для всех продуктов, связанных с этой группой покрытия.</span><span class="sxs-lookup"><span data-stu-id="198d1-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="198d1-108">Чтобы создать группу покрытия, выберите **Сводное планирование &gt; Настройка &gt; Покрытие &gt; Группы покрытия**.</span><span class="sxs-lookup"><span data-stu-id="198d1-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="198d1-109">Затем можно связать группу покрытия с продуктом.</span><span class="sxs-lookup"><span data-stu-id="198d1-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="198d1-110">Если связь относится к конкретному месту, складу или аналитике продукта, используйте поле **Группа покрытия** на странице **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="198d1-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="198d1-111">Если связь является общей и не зависит от аналитик продукта, используйте поле **Группа покрытия** на экспресс-вкладке **План** на странице **Сведения о продукте**.</span><span class="sxs-lookup"><span data-stu-id="198d1-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="198d1-112">По умолчанию если группа покрытия не связана с продуктом, то в сводном планировании используется общая группа покрытия, которая указана на странице **Параметры сводного планирования**.</span><span class="sxs-lookup"><span data-stu-id="198d1-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="198d1-113">Определение настроек покрытия для продукта.</span><span class="sxs-lookup"><span data-stu-id="198d1-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="198d1-114">Вы можете создавать настройки покрытия для определенного продукта.</span><span class="sxs-lookup"><span data-stu-id="198d1-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="198d1-115">Выберите **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="198d1-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="198d1-116">Выберите продукт, затем, в области действий, на вкладке **План**, в группе **Покрытие**, выберите **Покрытие номенклатуры**, чтобы открыть страницу **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="198d1-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="198d1-117">Если продукт уже связан с группой покрытия, вы можете переопределить настройки группы покрытия, используя поле **Переопределить**.</span><span class="sxs-lookup"><span data-stu-id="198d1-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="198d1-118">Настройки покрытия на странице **Покрытие номенклатуры** имеют приоритет над настройками на странице **Группа покрытия**.</span><span class="sxs-lookup"><span data-stu-id="198d1-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="198d1-119">Определение настроек покрытия для продукта с помощью мастера.</span><span class="sxs-lookup"><span data-stu-id="198d1-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="198d1-120">Мастер помогает по шагам выполнить процесс настройки основных параметров покрытия номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="198d1-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="198d1-121">На странице **Покрытие номенклатуры** в области действий выберите **Мастер**, чтобы открыть **Мастер покрытия номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="198d1-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="198d1-122">Определение параметров покрытия для группы аналитик.</span><span class="sxs-lookup"><span data-stu-id="198d1-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="198d1-123">Выберите **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="198d1-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="198d1-124">На странице **Сведения об используемом продукте**, на экспресс-вкладке **Общее**, в разделе **Администрирование** выберите ссылку в поле **Группа аналитик хранения**.</span><span class="sxs-lookup"><span data-stu-id="198d1-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="198d1-125">На странице **Группы аналитик хранения** выберите флажок **План покрытия по аналитикам**, чтобы создать настройки покрытия для аналитики в группе аналитик хранения.</span><span class="sxs-lookup"><span data-stu-id="198d1-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="198d1-126">Поле **План покрытия по аналитикам** должно быть выбрано для всех аналитик продукта, таких как конфигурация, цвет, размер и стиль.</span><span class="sxs-lookup"><span data-stu-id="198d1-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="198d1-127">Коды покрытия</span><span class="sxs-lookup"><span data-stu-id="198d1-127">Coverage codes</span></span>

<span data-ttu-id="198d1-128">Сводное планирование может быть настроено для использования различных методов пополнения.</span><span class="sxs-lookup"><span data-stu-id="198d1-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="198d1-129">Методы пополнения или методы изменения размера лота являются методами, используемыми системой для определения размера партии для приобретенных или произведенных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="198d1-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="198d1-130">Каждому методу пополнения назначается один из следующих кодов покрытия:</span><span class="sxs-lookup"><span data-stu-id="198d1-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="198d1-131">**Вручную** — метод изменения размера лота, в котором система не предлагает заказов на покупку, перемещение или производство для данной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="198d1-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="198d1-132">Планировщик для номенклатуры будет ответственным за создание необходимых заказов для пополнения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="198d1-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="198d1-133">**По требованию** — метод изменения размера лота, в котором система создает запланированный заказ на покупку, перемещение или производство в соответствии с потребностью для данной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="198d1-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="198d1-134">Обычно он используется для дорогостоящих номенклатур с периодическим спросом.</span><span class="sxs-lookup"><span data-stu-id="198d1-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="198d1-135">**За период** — метод изменения размера лота, объединяющий весь спрос за период в один заказ для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="198d1-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="198d1-136">Заказ будет запланирован для первого дня периода, и его количество будет соответствовать требованиям нетто за установленный период.</span><span class="sxs-lookup"><span data-stu-id="198d1-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="198d1-137">Период начинается с первого спроса номенклатуры и охватывает определенную продолжительность времени.</span><span class="sxs-lookup"><span data-stu-id="198d1-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="198d1-138">Следующий период начнется со следующих потребностей в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="198d1-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="198d1-139">**Мин./Макс.** — метод изменения размера лота, который содержит пополнение запасов вплоть до определенного уровня, когда прогнозируемые запасы в наличии ниже порогового значения.</span><span class="sxs-lookup"><span data-stu-id="198d1-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="198d1-140">Количество пополнения будет разницей между максимальным уровнем и прогнозируемым уровнем запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="198d1-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="198d1-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="198d1-141">Additional resources</span></span>

[<span data-ttu-id="198d1-142">Обзор сводных планов</span><span class="sxs-lookup"><span data-stu-id="198d1-142">Master plans overview</span></span>](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]