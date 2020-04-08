---
title: Интегрированный налог
description: Эта тема описывает интеграцию данных налога между Finance and Operations и Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173093"
---
# <a name="integrated-tax"></a><span data-ttu-id="2d5a9-103">Интегрированный налог</span><span class="sxs-lookup"><span data-stu-id="2d5a9-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="2d5a9-104">Данные настройки налога определяют настройку для как косвенных налогов (НДС, GST, налог), так и подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="2d5a9-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="2d5a9-105">В нем описывается правило расчета налогов, налоговая ставка, налоговый учет, сопоставление и другие концепции.</span><span class="sxs-lookup"><span data-stu-id="2d5a9-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="2d5a9-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="2d5a9-106">Templates</span></span>

<span data-ttu-id="2d5a9-107">Данные налога включают коллекцию сопоставлений объектов, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2d5a9-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="2d5a9-108">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2d5a9-108">Finance and Operations apps</span></span> | <span data-ttu-id="2d5a9-109">Приложения на основе модели в Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2d5a9-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="2d5a9-110">описание</span><span class="sxs-lookup"><span data-stu-id="2d5a9-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="2d5a9-111">Налоговые коды</span><span class="sxs-lookup"><span data-stu-id="2d5a9-111">Tax codes</span></span>                   | <span data-ttu-id="2d5a9-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="2d5a9-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="2d5a9-113">Налоговые группы</span><span class="sxs-lookup"><span data-stu-id="2d5a9-113">Tax groups</span></span>                 | <span data-ttu-id="2d5a9-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="2d5a9-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="2d5a9-115">Налоговые группы номенклатур</span><span class="sxs-lookup"><span data-stu-id="2d5a9-115">Tax item groups</span></span>             | <span data-ttu-id="2d5a9-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="2d5a9-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="2d5a9-117">Освобождения от налога</span><span class="sxs-lookup"><span data-stu-id="2d5a9-117">Tax Exemptions</span></span>             | <span data-ttu-id="2d5a9-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="2d5a9-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="2d5a9-119">Налоговые органы</span><span class="sxs-lookup"><span data-stu-id="2d5a9-119">Tax Authorities</span></span>             | <span data-ttu-id="2d5a9-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="2d5a9-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="2d5a9-121">Коды подоходного налога</span><span class="sxs-lookup"><span data-stu-id="2d5a9-121">Withholding tax codes</span></span>       | <span data-ttu-id="2d5a9-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="2d5a9-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="2d5a9-123">Группы подоходного налога</span><span class="sxs-lookup"><span data-stu-id="2d5a9-123">Withholding tax groups</span></span>     | <span data-ttu-id="2d5a9-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="2d5a9-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="2d5a9-125">Группа ГК налога</span><span class="sxs-lookup"><span data-stu-id="2d5a9-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="2d5a9-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="2d5a9-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

