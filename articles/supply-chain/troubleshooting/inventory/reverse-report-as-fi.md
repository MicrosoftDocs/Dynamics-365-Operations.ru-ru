---
title: Сторнирование приемки создает неожиданную открытую проводку
description: Сторнирование приемки с маркировкой создает открытую проводку, в которой сторнированное количество имеет те же складские аналитики, что и сторнированная проводка.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026859"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="15520-103">Сторнирование приемки создает неожиданную открытую проводку</span><span class="sxs-lookup"><span data-stu-id="15520-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="15520-104">Номер статьи базы знаний: 4612469</span><span class="sxs-lookup"><span data-stu-id="15520-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="15520-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="15520-105">Symptoms</span></span>

<span data-ttu-id="15520-106">Если сторнировать приемку с маркировкой система создает открытую проводку, в которой сторнированное количество имеет те же складские аналитики, что и сторнированная проводка.</span><span class="sxs-lookup"><span data-stu-id="15520-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="15520-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="15520-107">Resolution</span></span>

<span data-ttu-id="15520-108">При сторнировании операции "приемка" складская аналитика инициализируется из производственного журнала.</span><span class="sxs-lookup"><span data-stu-id="15520-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="15520-109">Поэтому она получает номер партии.</span><span class="sxs-lookup"><span data-stu-id="15520-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="15520-110">Из-за маркировки проводки по заказу на продажу наследуют номер партии.</span><span class="sxs-lookup"><span data-stu-id="15520-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="15520-111">Аналитика может быть сброшена после разноски приемки.</span><span class="sxs-lookup"><span data-stu-id="15520-111">The dimension can be reset when the reporting as finished is posted.</span></span>
