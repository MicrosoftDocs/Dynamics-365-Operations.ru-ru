---
title: Физически полученные заказы на покупку не отображаются в отчете закрытия склада
description: Физически полученные заказы на покупку не отображаются в отчете закрытия склада "Проверка открытых количеств".
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026847"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="27d4c-103">Физически полученные заказы на покупку не отображаются в отчете закрытия склада</span><span class="sxs-lookup"><span data-stu-id="27d4c-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="27d4c-104">Номер статьи базы знаний: 4612595</span><span class="sxs-lookup"><span data-stu-id="27d4c-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="27d4c-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="27d4c-105">Symptoms</span></span>

<span data-ttu-id="27d4c-106">Физически полученные заказы на покупку не отображаются в отчете закрытия склада **Проверка открытых количеств**.</span><span class="sxs-lookup"><span data-stu-id="27d4c-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="27d4c-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="27d4c-107">Resolution</span></span>

<span data-ttu-id="27d4c-108">В отчете **Проверка открытых количеств** отображаются проводки расхода, которые невозможно сопоставить с финансово обновленными приходами запасов по состоянию на выбранную дату закрытия.</span><span class="sxs-lookup"><span data-stu-id="27d4c-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="27d4c-109">Можно включить в отчет физические приходы.</span><span class="sxs-lookup"><span data-stu-id="27d4c-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="27d4c-110">В этом случае физические приходы будут отображаться, если они могут охватывать проводки расхода, которые невозможно сопоставить.</span><span class="sxs-lookup"><span data-stu-id="27d4c-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="27d4c-111">Дополнительные сведения см. в разделе [Подготовка к закрытию складов](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span><span class="sxs-lookup"><span data-stu-id="27d4c-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>
