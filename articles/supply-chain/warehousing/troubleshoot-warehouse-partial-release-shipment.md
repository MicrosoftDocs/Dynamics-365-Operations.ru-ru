---
title: Устранение неполадок частичных отпусков и частичных отгрузок
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с частичными отпусками и частичными отгрузками в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c9246376505e163a4a41bf141a98deed0fd511f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263273"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="e7ae1-103">Устранение неполадок частичных отпусков и частичных отгрузок</span><span class="sxs-lookup"><span data-stu-id="e7ae1-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7ae1-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с частичными отпусками и частичными отгрузками в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="e7ae1-105">Статус выпуска заказа на продажу остается частично отпущенным даже после того, как выставляется накладная по заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e7ae1-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e7ae1-106">Issue description</span></span>

<span data-ttu-id="e7ae1-107">Заказ на продажу является заказом на поставку, но одна или несколько номенклатур в нем имеют другой способ поставки.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="e7ae1-108">После выставления накладной по заказу он по-прежнему имеет статус отпуска *Частично отпущен*.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="e7ae1-109">Например, заказ на продажу содержит две номенклатуры: одну для доставки, а другую для получения самовывозом.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="e7ae1-110">Были выполнены как доставка, так и получение самовывозом.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="e7ae1-111">Поэтому по обеим строкам были выставлены накладные.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="e7ae1-112">Однако статус отпуска по-прежнему отображается как *Частично отпущенный*, что является ошибочным.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e7ae1-113">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e7ae1-113">Issue resolution</span></span>

<span data-ttu-id="e7ae1-114">Статус отпуска применяется только к строкам заказа, для которых номенклатуры включены для управления складом.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="e7ae1-115">Таким образом, статус отпуска остается *Частично отпущен* в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="e7ae1-116">Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функции.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="e7ae1-117">Расширение может быть добавлено как часть отборочной накладной и процесса выставления накладных, чтобы обновить статус отпуска.</span><span class="sxs-lookup"><span data-stu-id="e7ae1-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]