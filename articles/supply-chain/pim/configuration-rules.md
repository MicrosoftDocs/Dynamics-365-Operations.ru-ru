---
title: Правила конфигурации
description: В этой статье представлена общая информация о правилах конфигурации. Правила конфигурации определяют связи между номенклатурами в спецификации для продуктов, для которых используется технология конфигурации на основе аналитик.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac3515837df45b65121ebec72a32ac98d740796a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221879"
---
# <a name="configuration-rules"></a><span data-ttu-id="ae04b-104">Правила конфигурации</span><span class="sxs-lookup"><span data-stu-id="ae04b-104">Configuration rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae04b-105">В этой статье представлена общая информация о правилах конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ae04b-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="ae04b-106">Правила конфигурации определяют связи между номенклатурами в спецификации для продуктов, для которых используется технология конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="ae04b-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="ae04b-107">Правила конфигурации доступны, когда вы определяете модели конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="ae04b-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="ae04b-108">Правила конфигурации используются, чтобы принудительно задать или запретить определенные сочетания номенклатур в спецификациях.</span><span class="sxs-lookup"><span data-stu-id="ae04b-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="ae04b-109">После того как спецификация создана, и соответствующие номенклатуры назначены своим группам конфигурации, можно определить одно или несколько правил конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ae04b-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="ae04b-110">Если две номенклатуры используются совместно, используется оператор **Выбрать** для того, чтобы обеспечить включение.</span><span class="sxs-lookup"><span data-stu-id="ae04b-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="ae04b-111">Если две номенклатуры являются взаимоисключающими, используется оператор **Отменить выбор**, чтобы обеспечить исключение.</span><span class="sxs-lookup"><span data-stu-id="ae04b-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="ae04b-112">**Примечание.** Эта информация применяется только к шаблонам продукта, которые используют технологии конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="ae04b-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="ae04b-113">На существующие конфигурации не влияют последующие изменения правил конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ae04b-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="ae04b-114">Однако важно выполнить установку правил перед определением новой конфигурации и произвести проверку правил, если имеется подозрение, что они были изменены.</span><span class="sxs-lookup"><span data-stu-id="ae04b-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="ae04b-115">**Примечание.** При применении метода **Выбрать** производится автоматический выбор производной конфигурационной группы, кода номенклатуры и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ae04b-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="ae04b-116">Метод **Отменить выбор** запрещает выбор производной конфигурационной группы, кода номенклатуры и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ae04b-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ae04b-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ae04b-117">Additional resources</span></span>
--------

[<span data-ttu-id="ae04b-118">Обзор конфигураций продуктов на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="ae04b-118">Dimension-based product configuration overview</span></span>](dimension-based-product-configuration.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]