---
title: Улучшенная фильтрация RCS в RCS/глобальном репозитории
description: В этой теме описываются расширенные возможности фильтрации для глобального репозитория RCS, которые были усовершенствованы для включения дополнительных фильтров.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 7df49a85de484d013518217ba8ada6c61da4b6e4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2020
ms.locfileid: "3287947"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="b26eb-103">Параметры расширенной фильтрации RCS для поиска конфигураций в RCS/глобальном репозитории</span><span class="sxs-lookup"><span data-stu-id="b26eb-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b26eb-104">В этой теме описываются расширенные возможности фильтрации для глобального репозитория службы Regulatory Configuration Service (RCS), которые были усовершенствованы для включения возможности фильтрации по следующим критериям:</span><span class="sxs-lookup"><span data-stu-id="b26eb-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="b26eb-105">**Страна/регион** — на основе кодов ISO для стран</span><span class="sxs-lookup"><span data-stu-id="b26eb-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="b26eb-106">Типы **Теги** для:</span><span class="sxs-lookup"><span data-stu-id="b26eb-106">**Tags** types for:</span></span>
  - <span data-ttu-id="b26eb-107">Функциональная область</span><span class="sxs-lookup"><span data-stu-id="b26eb-107">Functional area</span></span>
  - <span data-ttu-id="b26eb-108">Область компонентов</span><span class="sxs-lookup"><span data-stu-id="b26eb-108">Feature area</span></span>
  - <span data-ttu-id="b26eb-109">Отрасль</span><span class="sxs-lookup"><span data-stu-id="b26eb-109">Industry</span></span> 
  - <span data-ttu-id="b26eb-110">Бизнес-документ</span><span class="sxs-lookup"><span data-stu-id="b26eb-110">Business document</span></span> 

<span data-ttu-id="b26eb-111">Для упрощения поиска отдельных или связанных конфигураций можно применять фильтры по отдельности или в группе.</span><span class="sxs-lookup"><span data-stu-id="b26eb-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="b26eb-112">Например, чтобы найти один тип настраиваемых деловых документов, связанных с накладными поставщика, можно применить фильтр **Тип бизнес-документа** для поиска документа этого типа.</span><span class="sxs-lookup"><span data-stu-id="b26eb-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="b26eb-113">[![Раздел фильтров для глобального репозитория](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="b26eb-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="b26eb-114">Для дальнейшего уточнения поиска можно выбрать тип документа, например "накладная поставщика", и щелкнуть **Применить фильтр**.</span><span class="sxs-lookup"><span data-stu-id="b26eb-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="b26eb-115">В следующем примере показаны результаты фильтрации по параметры **Тип бизнес-документов** с добавленным типом документа.</span><span class="sxs-lookup"><span data-stu-id="b26eb-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="b26eb-116">[![Примененный фильтр и импорт для типа бизнес-документа](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="b26eb-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="b26eb-117">Отфильтрованные результаты могут импортироваться в репозиторий RCS пользователей или в среду Dynamics 365 Finance отдельно или в виде набора.</span><span class="sxs-lookup"><span data-stu-id="b26eb-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="b26eb-118">Для этого выберите группу конфигураций и нажмите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="b26eb-118">To do this, select the group of configurations, and click **Import**.</span></span>
