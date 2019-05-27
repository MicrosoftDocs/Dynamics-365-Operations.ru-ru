---
title: Параметры покрытия
description: В этой теме приводятся сведения о параметрах покрытия, которые сводное планирование использует для расчета потребностей в номенклатуре.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538902"
---
# <a name="coverage-settings"></a><span data-ttu-id="3b91c-103">Параметры покрытия</span><span class="sxs-lookup"><span data-stu-id="3b91c-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b91c-104">При сводном планировании для вычисления потребностей в номенклатуре используются параметры покрытия.</span><span class="sxs-lookup"><span data-stu-id="3b91c-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="3b91c-105">Параметры покрытия можно задать несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="3b91c-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="3b91c-106">Определение параметров покрытия для группы покрытия.</span><span class="sxs-lookup"><span data-stu-id="3b91c-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="3b91c-107">Можно создать группу покрытия, которая содержит настройки для всех продуктов, связанных с этой группой покрытия.</span><span class="sxs-lookup"><span data-stu-id="3b91c-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="3b91c-108">Чтобы создать группу покрытия, выберите **Сводное планирование &gt; Настройка &gt; Покрытие &gt; Группы покрытия**.</span><span class="sxs-lookup"><span data-stu-id="3b91c-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="3b91c-109">Затем можно связать группу покрытия с продуктом.</span><span class="sxs-lookup"><span data-stu-id="3b91c-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="3b91c-110">Если связь относится к конкретному месту, складу или аналитике продукта, используйте поле **Группа покрытия** на странице **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="3b91c-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="3b91c-111">Если связь является общей и не зависит от аналитик продукта, используйте поле **Группа покрытия** на экспресс-вкладке **План** на странице **Сведения о продукте**.</span><span class="sxs-lookup"><span data-stu-id="3b91c-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="3b91c-112">По умолчанию если группа покрытия не связана с продуктом, то в сводном планировании используется общая группа покрытия, которая указана на странице **Параметры сводного планирования**.</span><span class="sxs-lookup"><span data-stu-id="3b91c-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="3b91c-113">Определение настроек покрытия для продукта.</span><span class="sxs-lookup"><span data-stu-id="3b91c-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="3b91c-114">Вы можете создавать настройки покрытия для определенного продукта.</span><span class="sxs-lookup"><span data-stu-id="3b91c-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="3b91c-115">Выберите **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="3b91c-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="3b91c-116">Выберите продукт, затем, в области действий, на вкладке **План**, в группе **Покрытие**, выберите **Покрытие номенклатуры**, чтобы открыть страницу **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="3b91c-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="3b91c-117">Если продукт уже связан с группой покрытия, вы можете переопределить настройки группы покрытия, используя поле **Переопределить**.</span><span class="sxs-lookup"><span data-stu-id="3b91c-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="3b91c-118">Настройки покрытия на странице **Покрытие номенклатуры** имеют приоритет над настройками на странице **Группа покрытия**.</span><span class="sxs-lookup"><span data-stu-id="3b91c-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="3b91c-119">Определение настроек покрытия для продукта с помощью мастера.</span><span class="sxs-lookup"><span data-stu-id="3b91c-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="3b91c-120">Мастер помогает по шагам выполнить процесс настройки основных параметров покрытия номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3b91c-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="3b91c-121">На странице **Покрытие номенклатуры** в области действий выберите **Мастер**, чтобы открыть **Мастер покрытия номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="3b91c-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="3b91c-122">Определение параметров покрытия для группы аналитик.</span><span class="sxs-lookup"><span data-stu-id="3b91c-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="3b91c-123">Выберите **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="3b91c-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="3b91c-124">На странице **Сведения об используемом продукте**, на экспресс-вкладке **Общее**, в разделе **Администрирование** выберите ссылку в поле **Группа аналитик хранения**.</span><span class="sxs-lookup"><span data-stu-id="3b91c-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="3b91c-125">На странице **Группы аналитик хранения** выберите флажок **План покрытия по аналитикам**, чтобы создать настройки покрытия для аналитики в группе аналитик хранения.</span><span class="sxs-lookup"><span data-stu-id="3b91c-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="3b91c-126">Поле **План покрытия по аналитикам** должно быть выбрано для всех аналитик продукта, таких как конфигурация, цвет, размер и стиль.</span><span class="sxs-lookup"><span data-stu-id="3b91c-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b91c-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3b91c-127">Additional resources</span></span>

[<span data-ttu-id="3b91c-128">Сводные планы</span><span class="sxs-lookup"><span data-stu-id="3b91c-128">Master plans</span></span>](master-plans.md)
