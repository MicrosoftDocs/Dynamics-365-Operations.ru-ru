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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 26818ceace7d2b7e7c3ed4d0bb0bd9ab2e884aba
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997608"
---
# <a name="integrated-tax"></a><span data-ttu-id="9a950-103">Интегрированный налог</span><span class="sxs-lookup"><span data-stu-id="9a950-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="9a950-104">Данные настройки налога определяют настройку для как косвенных налогов (НДС, GST, налог), так и подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="9a950-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="9a950-105">В нем описывается правило расчета налогов, налоговая ставка, налоговый учет, сопоставление и другие концепции.</span><span class="sxs-lookup"><span data-stu-id="9a950-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="9a950-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="9a950-106">Templates</span></span>

<span data-ttu-id="9a950-107">Данные налога включают коллекцию сопоставлений объектов, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9a950-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="9a950-108">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9a950-108">Finance and Operations apps</span></span> | <span data-ttu-id="9a950-109">Приложения на основе модели в Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9a950-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="9a950-110">описание</span><span class="sxs-lookup"><span data-stu-id="9a950-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="9a950-111">Налоговая группа номенклатур</span><span class="sxs-lookup"><span data-stu-id="9a950-111">Item sales tax group</span></span> | <span data-ttu-id="9a950-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="9a950-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="9a950-113">Налоговые органы</span><span class="sxs-lookup"><span data-stu-id="9a950-113">Sales tax authorities</span></span> | <span data-ttu-id="9a950-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="9a950-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="9a950-115">CDS объекта кода налогового освобождения</span><span class="sxs-lookup"><span data-stu-id="9a950-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="9a950-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="9a950-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="9a950-117">Налоговые группы</span><span class="sxs-lookup"><span data-stu-id="9a950-117">Sales tax groups</span></span> | <span data-ttu-id="9a950-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="9a950-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="9a950-119">Группы разноски ГК для налога V2</span><span class="sxs-lookup"><span data-stu-id="9a950-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="9a950-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="9a950-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="9a950-121">Коды подоходного налога</span><span class="sxs-lookup"><span data-stu-id="9a950-121">Withholding tax codes</span></span> | <span data-ttu-id="9a950-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="9a950-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="9a950-123">Группы подоходного налога</span><span class="sxs-lookup"><span data-stu-id="9a950-123">Withholding tax groups</span></span> | <span data-ttu-id="9a950-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="9a950-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

