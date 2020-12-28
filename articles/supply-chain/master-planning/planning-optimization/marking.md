---
title: Маркировка запасов с оптимизацией планирования
description: В этой теме приводятся сведения о параметрах, которые доступны для маркировки запасов в утвержденных заказах при использовании оптимизации планирования.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99a52c03e519384955d68d7101a7b73b7e9a7af6
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672205"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="59671-103">Маркировка запасов с оптимизацией планирования</span><span class="sxs-lookup"><span data-stu-id="59671-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59671-104">В этой теме приводятся сведения о параметрах, которые доступны для маркировки запасов в утвержденных заказах при использовании оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="59671-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="59671-105">*Маркировка* используется для связывания поставок и спроса.</span><span class="sxs-lookup"><span data-stu-id="59671-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="59671-106">Она напоминает *определение источника потребности*, которая определяет, как сводное планирование предполагает покрывать спрос.</span><span class="sxs-lookup"><span data-stu-id="59671-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="59671-107">С точки зрения планирования основное различие заключается в том, что маркировка является более постоянной, чем определение источника потребности.</span><span class="sxs-lookup"><span data-stu-id="59671-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="59671-108">Маркировка была введена для поддержки специальных сценариев калькуляции себестоимости: "первым пришел, первым ушел" (ФИФО) и "последним пришел, первым ушел" (ЛИФО).</span><span class="sxs-lookup"><span data-stu-id="59671-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="59671-109">Однако сейчас она также используется для некоторых сценариев без расчета себестоимости.</span><span class="sxs-lookup"><span data-stu-id="59671-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="59671-110">Маркировка между поставками и спросом является необязательной и почти постоянной.</span><span class="sxs-lookup"><span data-stu-id="59671-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="59671-111">Маркировка может быть удалена вручную пользователем, или можно удалить ее, запустив развертывание строки заказа на продажу, в которой выбран параметр **Удалить маркировку**.</span><span class="sxs-lookup"><span data-stu-id="59671-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="59671-112">Определение источника потребности управляется сводным планированием в процессе покрытия для связывания спроса с требуемыми поставками.</span><span class="sxs-lookup"><span data-stu-id="59671-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="59671-113">Определение источника потребности может быть обновлено для каждого выполнения планирования с целью оптимизации поставок, необходимой для покрытия спроса.</span><span class="sxs-lookup"><span data-stu-id="59671-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="59671-114">Когда сводное планирование обновляет сведения определения источника потребности, оно учитывает всю существующую маркировку.</span><span class="sxs-lookup"><span data-stu-id="59671-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="59671-115">Определение источника потребности начинает с включения соответствующей маркировки, резервирования запасов в наличии и резервирования по заказу в следующей последовательности:</span><span class="sxs-lookup"><span data-stu-id="59671-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="59671-116">Маркировка между спросом и поставками</span><span class="sxs-lookup"><span data-stu-id="59671-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="59671-117">Резервирования запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="59671-117">On-hand reservations</span></span>
1. <span data-ttu-id="59671-118">Резервирования по заказам</span><span class="sxs-lookup"><span data-stu-id="59671-118">On-order reservations</span></span>

<span data-ttu-id="59671-119">При утверждении спланированного заказа в диалоговом окне **Утверждение** предоставляется поле **Обновить маркировку**, которое можно использовать для настройки параметров маркировки для заказов, созданных во время утверждения.</span><span class="sxs-lookup"><span data-stu-id="59671-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="59671-120">Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="59671-120">Select one of the following values:</span></span>

- <span data-ttu-id="59671-121">**Нет** — складская маркировка не применяется.</span><span class="sxs-lookup"><span data-stu-id="59671-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="59671-122">**Стандарт** — складская маркировка обновляется согласно определению источника потребности.</span><span class="sxs-lookup"><span data-stu-id="59671-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="59671-123">Заказ типа "Потребность в номенклатуре" (спрос) помечается по заказу на выполнение (поставка).</span><span class="sxs-lookup"><span data-stu-id="59671-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="59671-124">Если некоторое количество остается в заказе на выполнение, оно не отмечается, а справочная информация остается пустой.</span><span class="sxs-lookup"><span data-stu-id="59671-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="59671-125">Например, если заказ на продажу на 100 шт. привязан к заказу на покупку на 150 шт., справочная информация будет назначена только этому заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="59671-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="59671-126">**Расширено** — заказ типа "Потребность в номенклатуре" (спрос) и заказ на выполнение (поставка) маркируются, вне зависимости от оставшегося для заказа на выполнение количества.</span><span class="sxs-lookup"><span data-stu-id="59671-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="59671-127">Например, если заказ на продажу на 100 шт. привязан к заказу на покупку на 150 шт., справочная информация будет назначена как заказу на продажу, так и заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="59671-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>
