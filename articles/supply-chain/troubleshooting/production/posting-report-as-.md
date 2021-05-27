---
title: Ошибка при выполнении разноски журнала "Приемка"
description: При разноске журнала "Приемка" выводится сообщение об ошибке, в котором говорится, что заказанное количество не может быть уменьшено.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026836"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="72eab-103">Ошибка при выполнении разноски журнала "Приемка"</span><span class="sxs-lookup"><span data-stu-id="72eab-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="72eab-104">Номер статьи базы знаний: 4612891</span><span class="sxs-lookup"><span data-stu-id="72eab-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="72eab-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="72eab-105">Symptoms</span></span>

<span data-ttu-id="72eab-106">При разноске журнала **Приемка** происходит ошибка, и появляется следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="72eab-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="72eab-107">Заказанное количество не может быть сокращено, так как недостаточно открытых складских проводок со статусом "Заказано".</span><span class="sxs-lookup"><span data-stu-id="72eab-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="72eab-108">Номенклатуры куплены, получены или зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="72eab-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="72eab-109">Эта ошибка возникает только в том случае, если поле **Количество ошибочных** установлено в первой строке журнала **Приемка**, а поле **Количество правильных** задано в последней строке.</span><span class="sxs-lookup"><span data-stu-id="72eab-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="72eab-110">Если поле **Количество ошибочных** указано в последней строке, ошибка не возникает.</span><span class="sxs-lookup"><span data-stu-id="72eab-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="72eab-111">Приказ</span><span class="sxs-lookup"><span data-stu-id="72eab-111">Resolution</span></span>

<span data-ttu-id="72eab-112">Чтобы не допустить возникновения этой ошибки, откройте страницу **Параметры управления производством**, а затем на вкладке **Общие** установите параметр **Увеличить оставшееся кол-во на ошибочное кол-во** как *Да*.</span><span class="sxs-lookup"><span data-stu-id="72eab-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
