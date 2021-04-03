---
title: Интегрированный налог
description: Эта тема описывает интеграцию данных налога между Finance and Operations и Dataverse.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 7501ef21492a96c81b971e1d9077beaba9be897b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560345"
---
# <a name="integrated-tax"></a><span data-ttu-id="ab746-103">Интегрированный налог</span><span class="sxs-lookup"><span data-stu-id="ab746-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="ab746-104">Данные настройки налога определяют настройку для как косвенных налогов (НДС, GST, налог), так и подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="ab746-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="ab746-105">В нем описывается правило расчета налогов, налоговая ставка, налоговый учет, сопоставление и другие концепции.</span><span class="sxs-lookup"><span data-stu-id="ab746-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="ab746-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="ab746-106">Templates</span></span>

<span data-ttu-id="ab746-107">Данные налога включают коллекцию сопоставлений таблиц, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ab746-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="ab746-108">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab746-108">Finance and Operations apps</span></span> | <span data-ttu-id="ab746-109">Приложения на основе модели в Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ab746-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="ab746-110">описание</span><span class="sxs-lookup"><span data-stu-id="ab746-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="ab746-111">Налоговая группа номенклатур</span><span class="sxs-lookup"><span data-stu-id="ab746-111">Item sales tax group</span></span> | <span data-ttu-id="ab746-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="ab746-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="ab746-113">Налоговые органы</span><span class="sxs-lookup"><span data-stu-id="ab746-113">Sales tax authorities</span></span> | <span data-ttu-id="ab746-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="ab746-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="ab746-115">CDS объекта кода налогового освобождения</span><span class="sxs-lookup"><span data-stu-id="ab746-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="ab746-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="ab746-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="ab746-117">Налоговые группы</span><span class="sxs-lookup"><span data-stu-id="ab746-117">Sales tax groups</span></span> | <span data-ttu-id="ab746-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="ab746-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="ab746-119">Группы разноски ГК для налога V2</span><span class="sxs-lookup"><span data-stu-id="ab746-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="ab746-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="ab746-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="ab746-121">Коды подоходного налога</span><span class="sxs-lookup"><span data-stu-id="ab746-121">Withholding tax codes</span></span> | <span data-ttu-id="ab746-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="ab746-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="ab746-123">Группы подоходного налога</span><span class="sxs-lookup"><span data-stu-id="ab746-123">Withholding tax groups</span></span> | <span data-ttu-id="ab746-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="ab746-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]