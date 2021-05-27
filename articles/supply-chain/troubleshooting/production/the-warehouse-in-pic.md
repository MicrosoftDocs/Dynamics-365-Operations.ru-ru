---
title: Склад в журнале отгрузочных накладных не обновляется в строке спецификации.
description: Склад в журнале отгрузочных накладных не обновляется в строке спецификации.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026838"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a><span data-ttu-id="39964-103">Склад в журнале отгрузочных накладных не обновляется в строке спецификации</span><span class="sxs-lookup"><span data-stu-id="39964-103">The warehouse in the picking list journal isn't updated on a BOM line</span></span>

<span data-ttu-id="39964-104">Номер статьи базы знаний: 4614848</span><span class="sxs-lookup"><span data-stu-id="39964-104">KB number: 4614848</span></span>

## <a name="symptoms"></a><span data-ttu-id="39964-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="39964-105">Symptoms</span></span>

<span data-ttu-id="39964-106">Склад в журнале отгрузочных накладных не обновляется в строке спецификации.</span><span class="sxs-lookup"><span data-stu-id="39964-106">The warehouse in the picking list journal isn't updated on a bill of materials (BOM) line.</span></span>

## <a name="resolution"></a><span data-ttu-id="39964-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="39964-107">Resolution</span></span>

<span data-ttu-id="39964-108">Система работает в соответствии с разработанным поведением.</span><span class="sxs-lookup"><span data-stu-id="39964-108">The system is behaving as designed.</span></span> <span data-ttu-id="39964-109">Если создается строка журнала отгрузочных накладных со ссылкой (через код лота) в строке производственной спецификации, склад в строке производственной спецификации не обновляется, если складская аналитика в строке журнала отгрузочных накладных изменяется позднее.</span><span class="sxs-lookup"><span data-stu-id="39964-109">If a picking list journal line is created that has a reference (via the lot ID) to a production BOM line, the warehouse on the production BOM line won't be updated if the warehouse dimension on the production picking list journal line is changed later.</span></span>
