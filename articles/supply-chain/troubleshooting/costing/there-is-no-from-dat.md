---
title: На вкладке "Активные цены" на странице "Цена номенклатуры" нет значения "Начальная дата"
description: На вкладке "Активные цены" на странице "Цена номенклатуры" нет значения "Начальная дата".
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026862"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="f88d7-103">На вкладке "Активные цены" на странице "Цена номенклатуры" нет значения "Начальная дата"</span><span class="sxs-lookup"><span data-stu-id="f88d7-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="f88d7-104">Номер статьи базы знаний: 4613548</span><span class="sxs-lookup"><span data-stu-id="f88d7-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="f88d7-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="f88d7-105">Symptoms</span></span>

<span data-ttu-id="f88d7-106">На вкладке **Активные цены** на странице **Цена номенклатуры** нет значения **Начальная дата**.</span><span class="sxs-lookup"><span data-stu-id="f88d7-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="f88d7-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="f88d7-107">Resolution</span></span>

<span data-ttu-id="f88d7-108">Значение **Начальная дата** (дата вступления в силу), установленное для ожидающей цены, не переносится в активную цену.</span><span class="sxs-lookup"><span data-stu-id="f88d7-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="f88d7-109">Когда запись стоимости номенклатуры вводится первоначально, она имеет статус *Ожидание* и заданную дату начала действия.</span><span class="sxs-lookup"><span data-stu-id="f88d7-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="f88d7-110">При активации записи стоимости номенклатуры происходит обновление статуса на *Активный* и даты начала действия на дату активации.</span><span class="sxs-lookup"><span data-stu-id="f88d7-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="f88d7-111">Таким образом, дата активации активной цены всегда является фактической датой активации.</span><span class="sxs-lookup"><span data-stu-id="f88d7-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="f88d7-112">Дополнительные сведения см. в разделе [Обзор версий учета затрат](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="f88d7-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
