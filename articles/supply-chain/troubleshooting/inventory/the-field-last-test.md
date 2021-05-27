---
title: Поле "Дата последнего испытания" не обновляется при создании нескольких заказов контроля качества
description: Поле "Дата последнего испытания" не обновляется при создании нескольких заказов контроля качества.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026858"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="26f3b-103">Поле "Дата последнего испытания" не обновляется при создании нескольких заказов контроля качества</span><span class="sxs-lookup"><span data-stu-id="26f3b-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="26f3b-104">Номер статьи базы знаний: 4612803</span><span class="sxs-lookup"><span data-stu-id="26f3b-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="26f3b-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="26f3b-105">Symptoms</span></span>

<span data-ttu-id="26f3b-106">Поле **Дата последнего испытания** не обновляется при создании нескольких заказов контроля качества.</span><span class="sxs-lookup"><span data-stu-id="26f3b-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="26f3b-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="26f3b-107">Resolution</span></span>

<span data-ttu-id="26f3b-108">Система работает в соответствии с разработанным поведением.</span><span class="sxs-lookup"><span data-stu-id="26f3b-108">The system is behaving as designed.</span></span> <span data-ttu-id="26f3b-109">Дата последнего испытания не связана с заказами контроля качества.</span><span class="sxs-lookup"><span data-stu-id="26f3b-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="26f3b-110">В ней хранится дата, когда готовые товары были приобретены или произведены впервые.</span><span class="sxs-lookup"><span data-stu-id="26f3b-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="26f3b-111">Эта дата используется для расчета даты уведомления о сроке хранения.</span><span class="sxs-lookup"><span data-stu-id="26f3b-111">This date is used to calculate the shelf life advice date.</span></span>
