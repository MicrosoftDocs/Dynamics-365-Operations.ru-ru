---
title: При выборе нового кода лота очищается номер партии
description: При просмотре строки журнала отгрузочных накладных значение в поле "Номер партии" очищается, если выбрано новое значение в поле "Код лота".
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026832"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="a49bc-103">При выборе нового кода лота очищается номер партии</span><span class="sxs-lookup"><span data-stu-id="a49bc-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="a49bc-104">Номер статьи базы знаний: 4613107</span><span class="sxs-lookup"><span data-stu-id="a49bc-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="a49bc-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="a49bc-105">Symptoms</span></span>

<span data-ttu-id="a49bc-106">При просмотре строки журнала отгрузочных накладных значение в поле **Номер партии** очищается, если выбрано новое значение в поле **Код лота**.</span><span class="sxs-lookup"><span data-stu-id="a49bc-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="a49bc-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="a49bc-107">Resolution</span></span>

<span data-ttu-id="a49bc-108">Система работает в соответствии с разработанным поведением.</span><span class="sxs-lookup"><span data-stu-id="a49bc-108">The system is behaving as designed.</span></span> <span data-ttu-id="a49bc-109">При изменении кода лота изменяется контекст номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a49bc-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="a49bc-110">Поэтому номер партии сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="a49bc-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="a49bc-111">Чтобы связать номер партии с кодом лота, необходимо сначала установить код лота.</span><span class="sxs-lookup"><span data-stu-id="a49bc-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
