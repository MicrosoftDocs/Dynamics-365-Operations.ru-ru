---
title: Интегрированный налог
description: Эта тема описывает интеграцию данных налога между Finance and Operations и Dataverse.
author: robinarh
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
ms.openlocfilehash: a7992520b57b4c19b6dc8e13bd8e9ffc87b40f5a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750650"
---
# <a name="integrated-tax"></a><span data-ttu-id="2cd41-103">Интегрированный налог</span><span class="sxs-lookup"><span data-stu-id="2cd41-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="2cd41-104">Данные настройки налога определяют настройку для как косвенных налогов (НДС, GST, налог), так и подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="2cd41-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="2cd41-105">В нем описывается правило расчета налогов, налоговая ставка, налоговый учет, сопоставление и другие концепции.</span><span class="sxs-lookup"><span data-stu-id="2cd41-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="2cd41-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="2cd41-106">Templates</span></span>

<span data-ttu-id="2cd41-107">Данные налога включают коллекцию сопоставлений таблиц, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2cd41-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="2cd41-108">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2cd41-108">Finance and Operations apps</span></span> | <span data-ttu-id="2cd41-109">Приложения на основе модели в Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2cd41-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="2cd41-110">описание</span><span class="sxs-lookup"><span data-stu-id="2cd41-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="2cd41-111">Налоговая группа номенклатур</span><span class="sxs-lookup"><span data-stu-id="2cd41-111">Item sales tax group</span></span> | <span data-ttu-id="2cd41-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="2cd41-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="2cd41-113">Налоговые органы</span><span class="sxs-lookup"><span data-stu-id="2cd41-113">Sales tax authorities</span></span> | <span data-ttu-id="2cd41-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="2cd41-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="2cd41-115">CDS объекта кода налогового освобождения</span><span class="sxs-lookup"><span data-stu-id="2cd41-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="2cd41-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="2cd41-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="2cd41-117">Налоговые группы</span><span class="sxs-lookup"><span data-stu-id="2cd41-117">Sales tax groups</span></span> | <span data-ttu-id="2cd41-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="2cd41-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="2cd41-119">Группы разноски ГК для налога V2</span><span class="sxs-lookup"><span data-stu-id="2cd41-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="2cd41-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="2cd41-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="2cd41-121">Коды подоходного налога</span><span class="sxs-lookup"><span data-stu-id="2cd41-121">Withholding tax codes</span></span> | <span data-ttu-id="2cd41-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="2cd41-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="2cd41-123">Группы подоходного налога</span><span class="sxs-lookup"><span data-stu-id="2cd41-123">Withholding tax groups</span></span> | <span data-ttu-id="2cd41-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="2cd41-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]