---
title: Невозможно выставить накладную на заказ на продажу, направленный клиенту
description: После включения параметра автоматической разноски накладной больше нельзя выставлять накладную по исходному заказу на продажу и исходной прямой поставке.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026843"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="56d50-103">Невозможно выставить накладную на заказ на продажу, направленный клиенту</span><span class="sxs-lookup"><span data-stu-id="56d50-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="56d50-104">Номер статьи базы знаний: 4611793</span><span class="sxs-lookup"><span data-stu-id="56d50-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="56d50-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="56d50-105">Symptoms</span></span>

<span data-ttu-id="56d50-106">После включения параметра **Автоматическая разноска накладной** на странице **Внутрихолдинговый** для поставщика больше нельзя выставлять накладную по исходному заказу на продажу и исходной прямой поставке.</span><span class="sxs-lookup"><span data-stu-id="56d50-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="56d50-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="56d50-107">Resolution</span></span>

<span data-ttu-id="56d50-108">Поведение синхронизации для внутрихолдинговых накладных по заказу и прямых поставок управляется и переопределяется параметрами, описанными в разделе [Настройка параметров для разноски внутрихолдингового заказа](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span><span class="sxs-lookup"><span data-stu-id="56d50-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="56d50-109">После настройки этих параметров сначала необходимо выставить накладную по внутрихолдинговому заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="56d50-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="56d50-110">Затем будут синхронизованы исходные заказы на продажу и заказы на покупку.</span><span class="sxs-lookup"><span data-stu-id="56d50-110">The original sales orders and purchase orders will then be synchronized.</span></span>
