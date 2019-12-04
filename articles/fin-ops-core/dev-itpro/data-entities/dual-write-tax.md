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
ms.openlocfilehash: b6be53e9a2065373ca37c2791568a8161823803f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772418"
---
## <a name="integrated-tax"></a><span data-ttu-id="55b57-103">Интегрированный налог</span><span class="sxs-lookup"><span data-stu-id="55b57-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55b57-104">Данные настройки налога определяют настройку для как косвенных налогов (НДС, GST, налог), так и подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="55b57-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="55b57-105">В нем описывается правило расчета налогов, налоговая ставка, налоговый учет, сопоставление и другие концепции.</span><span class="sxs-lookup"><span data-stu-id="55b57-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="55b57-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="55b57-106">Templates</span></span>

<span data-ttu-id="55b57-107">Данные налога включают коллекцию сопоставлений объектов, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="55b57-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="55b57-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="55b57-108">Finance and Operations</span></span>   | <span data-ttu-id="55b57-109">Приложение Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="55b57-109">Customer Engagement application</span></span>
-------------------------|---------------------------------
<span data-ttu-id="55b57-110">Налоговые коды</span><span class="sxs-lookup"><span data-stu-id="55b57-110">Tax codes</span></span>                  | <span data-ttu-id="55b57-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="55b57-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="55b57-112">Налоговые группы</span><span class="sxs-lookup"><span data-stu-id="55b57-112">Tax groups</span></span>               | <span data-ttu-id="55b57-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="55b57-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="55b57-114">Налоговые группы номенклатур</span><span class="sxs-lookup"><span data-stu-id="55b57-114">Tax item groups</span></span>          | <span data-ttu-id="55b57-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="55b57-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="55b57-116">Освобождения от налога</span><span class="sxs-lookup"><span data-stu-id="55b57-116">Tax Exemptions</span></span>           | <span data-ttu-id="55b57-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="55b57-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="55b57-118">Налоговые органы</span><span class="sxs-lookup"><span data-stu-id="55b57-118">Tax Authorities</span></span>          | <span data-ttu-id="55b57-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="55b57-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="55b57-120">Коды подоходного налога</span><span class="sxs-lookup"><span data-stu-id="55b57-120">Withholding tax codes</span></span>      | <span data-ttu-id="55b57-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="55b57-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="55b57-122">Группы подоходного налога</span><span class="sxs-lookup"><span data-stu-id="55b57-122">Withholding tax groups</span></span>   | <span data-ttu-id="55b57-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="55b57-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="55b57-124">Группа ГК налога</span><span class="sxs-lookup"><span data-stu-id="55b57-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="55b57-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="55b57-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

