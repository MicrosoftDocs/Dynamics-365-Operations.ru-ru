---
title: "Параметры покрытия"
description: "При сводном планировании для вычисления потребностей в номенклатуре используются параметры покрытия."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 50f47394a4d4e95b4e158ea42a630d9e6e91f05b
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="coverage-settings"></a><span data-ttu-id="7bbbb-103">Параметры покрытия</span><span class="sxs-lookup"><span data-stu-id="7bbbb-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bbbb-104">При сводном планировании для вычисления потребностей в номенклатуре используются параметры покрытия.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="7bbbb-105">Параметры покрытия можно задать несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="7bbbb-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="7bbbb-106">Определение параметров покрытия для группы покрытия.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="7bbbb-107">Можно создать группу покрытия, которая содержит настройки для всех продуктов, связанных с этой группой покрытия.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="7bbbb-108">Нажмите **Сводное планирование &gt; Настройка &gt; Покрытие &gt; Группы покрытия**, чтобы создать группу покрытия.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="7bbbb-109">Затем можно связать группу покрытия с продуктом.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="7bbbb-110">Если связь относится к конкретному месту, складу или аналитике продукта, используйте поле **Группа покрытия** на странице **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="7bbbb-111">Если связь является общей и не зависит от аналитик продукта, используйте **Группу покрытия** на экспресс-вкладке **План** на странице **Сведения о продукте**.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="7bbbb-112">Если группа покрытия не связана с продуктом, то в сводном планировании используется **Общая группа покрытия**, которая указана на странице **Параметры сводного планирования** в качестве параметра по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="7bbbb-113">Определение настроек покрытия для продукта.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="7bbbb-114">Вы можете создавать настройки покрытия для определенного продукта.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="7bbbb-115">Щелкните **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="7bbbb-116">Выберите продукт в **области действий**, на вкладке **План**, в пункте **Группа покрытия**, щелкните **Покрытие номенклатуры**, чтобы открыть страницу **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="7bbbb-117">Если продукт уже связан с группой покрытия, вы можете переопределить настройки группы покрытия, используя поле **Переопределить**.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="7bbbb-118">Настройки покрытия на странице **Покрытие номенклатуры** имеют приоритет над настройками на странице **Группа покрытия**.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="7bbbb-119">Определение настроек покрытия для продукта с помощью мастера.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="7bbbb-120">Мастер представляет собой пошаговое руководство по настройке основных параметров покрытия номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="7bbbb-121">На странице **Покрытие номенклатуры** щелкните **Мастер**, чтобы открыть **Мастер покрытия номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

- <span data-ttu-id="7bbbb-122">Определение параметров покрытия для группы аналитик.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="7bbbb-123">Щелкните **Управление сведениями о продукте &gt; Общее &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="7bbbb-124">На странице **Сведения об используемом продукте**, на вкладке **Общее**, в группе **Администрирование** перейдите по ссылке **Группа аналитик хранения**.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-124">On the **Released product detail** page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="7bbbb-125">На странице **Группа аналитик хранения** выберите поле **План покрытия по аналитикам**, чтобы создать настройки покрытия для аналитики в группе аналитик хранения.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="7bbbb-126">Для всех аналитик продукта, таких как конфигурация, цвет, размер и стиль, должно быть выбрано поле **План покрытия по аналитикам**.</span><span class="sxs-lookup"><span data-stu-id="7bbbb-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="additional-resources"></a><span data-ttu-id="7bbbb-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7bbbb-127">Additional resources</span></span>
--------

[<span data-ttu-id="7bbbb-128">Сводные планы</span><span class="sxs-lookup"><span data-stu-id="7bbbb-128">Master plans</span></span>](master-plans.md)




