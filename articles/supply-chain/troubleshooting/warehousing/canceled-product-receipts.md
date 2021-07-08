---
title: Отмененные поступления продуктов не обновляют статус проводки на "Зарегистрировано"
description: После отмены поступления продуктов при входящей загрузке система автоматически обновляет статус складской проводки с "Получено" на "Заказано".
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294162"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="048d5-103">Отмененные поступления продуктов не обновляют статус проводки на "Зарегистрировано"</span><span class="sxs-lookup"><span data-stu-id="048d5-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="048d5-104">Симптомы</span><span class="sxs-lookup"><span data-stu-id="048d5-104">Symptoms</span></span>

<span data-ttu-id="048d5-105">После выполнения действия **Отмена поступления продуктов** при входящей загрузке система автоматически обновляет статус проводок по запасам с *Получено* на *Заказано*.</span><span class="sxs-lookup"><span data-stu-id="048d5-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="048d5-106">Решение</span><span class="sxs-lookup"><span data-stu-id="048d5-106">Resolution</span></span>

<span data-ttu-id="048d5-107">При отмене отборочных накладных для исходящих загрузок статус проводок по запасам остается *Скомплектовано*.</span><span class="sxs-lookup"><span data-stu-id="048d5-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="048d5-108">Однако когда отменяются поступления продуктов из входящей загрузки, статус проводок по запасам не восстанавливается на *Зарегистрировано*.</span><span class="sxs-lookup"><span data-stu-id="048d5-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="048d5-109">Поэтому после того, как поступление продуктов из входящей загрузки отменяется, работник склада должен повторно зарегистрировать количества номенклатур для загрузок.</span><span class="sxs-lookup"><span data-stu-id="048d5-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="048d5-110">Дополнительные сведения см. в разделе [Регистрация количества номенклатур, поступивших во входящей загрузке](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="048d5-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
