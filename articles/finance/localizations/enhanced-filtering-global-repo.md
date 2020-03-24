---
title: Улучшенная фильтрация в RCS/глобальном репозитории
description: В этой теме описываются расширенные возможности фильтрации для глобального репозитория RCS, которые были усовершенствованы для включения дополнительных фильтров.
author: JaneA07
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ed5a217b8844bfc76d53370ab4c4c339f5bece36
ms.sourcegitcommit: 0dcdfedec7125562f6b33deb009a3e044a1243eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "3099875"
---
# <a name="enhanced-filtering-options-for-finding-configurations-in-the-global-repository"></a><span data-ttu-id="80a31-103">Расширенные параметры фильтрации для поиска конфигураций в глобальном репозитории</span><span class="sxs-lookup"><span data-stu-id="80a31-103">Enhanced filtering options for finding configurations in the Global repository</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="80a31-104">В этой теме описываются расширенные возможности фильтрации для глобального репозитория службы Regulatory Configuration Service (RCS), которые были усовершенствованы для включения дополнительных фильтров.</span><span class="sxs-lookup"><span data-stu-id="80a31-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the following filters:</span></span> 
- <span data-ttu-id="80a31-105">**Страна/регион** — на основе кодов ISO для стран</span><span class="sxs-lookup"><span data-stu-id="80a31-105">**Country/region** - based on ISO country codes</span></span>  
- <span data-ttu-id="80a31-106">**Теги** — для функциональной области/области функциональных возможностей; отрасль; тип бизнес-документа</span><span class="sxs-lookup"><span data-stu-id="80a31-106">**Tags** - for functional/feature area; Industry; Business document type</span></span> 

<span data-ttu-id="80a31-107">Можно применять фильтры по отдельности или в группах для поиска отдельных или соответствующих конфигураций.</span><span class="sxs-lookup"><span data-stu-id="80a31-107">You can apply filters, either individually or in groups, to find specific or related configurations.</span></span> <span data-ttu-id="80a31-108">Например, для поиска всех настраиваемых деловых документов, относящихся к накладным поставщиков, можно применить фильтр **Типы бизнес-документов**.</span><span class="sxs-lookup"><span data-stu-id="80a31-108">For example, to find all configurable business documents related to vendor invoices, you can apply the **Business document type** filter.</span></span> 

<span data-ttu-id="80a31-109">Можно уточнить поиск, выбрав код страны и нажав **Применить фильтр**.</span><span class="sxs-lookup"><span data-stu-id="80a31-109">You can further refine a search by selecting the country code and clicking **Apply filter**.</span></span>  

<span data-ttu-id="80a31-110">[![Раздел фильтров для глобального репозитория](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="80a31-110">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="80a31-111">В следующем примере показаны результаты фильтрации по параметры **Тип бизнес-документов**.</span><span class="sxs-lookup"><span data-stu-id="80a31-111">The following example shows the results when filtering on **Business document type**.</span></span> 

<span data-ttu-id="80a31-112">[![Примененный фильтр и импорт для типа бизнес-документа](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="80a31-112">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="80a31-113">Отфильтрованные результаты могут импортироваться в RCS или среду Dynamics 365 Finance пользователей, отдельно или в виде набора (путем выбора группы конфигураций), щелчком кнопки **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="80a31-113">Filtered results can be imported into users RCS or Dynamics 365 Finance environment, either individually or as a set (by selecting the group of configurations) and clicking **Import**.</span></span>






