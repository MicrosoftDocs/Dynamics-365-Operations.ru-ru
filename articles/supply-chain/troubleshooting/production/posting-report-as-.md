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
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Ошибка при выполнении разноски журнала "Приемка"

Номер статьи базы знаний: 4612891

## <a name="symptoms"></a>Симптомы

При разноске журнала **Приемка** происходит ошибка, и появляется следующее сообщение об ошибке:

> Заказанное количество не может быть сокращено, так как недостаточно открытых складских проводок со статусом "Заказано". Номенклатуры куплены, получены или зарегистрированы.

Эта ошибка возникает только в том случае, если поле **Количество ошибочных** установлено в первой строке журнала **Приемка**, а поле **Количество правильных** задано в последней строке. Если поле **Количество ошибочных** указано в последней строке, ошибка не возникает.

## <a name="resolution"></a>Приказ

Чтобы не допустить возникновения этой ошибки, откройте страницу **Параметры управления производством**, а затем на вкладке **Общие** установите параметр **Увеличить оставшееся кол-во на ошибочное кол-во** как *Да*.
