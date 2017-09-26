---
title: "Амортизация ОС"
description: "В этой статье приводится обзор амортизации для основных средств."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a7f27847832e7c4814f1dc5982b6352c2ba98741
ms.contentlocale: ru-ru
ms.lasthandoff: 05/25/2017

---

# <a name="fixed-asset-depreciation"></a>Амортизация ОС

[!include[banner](../includes/banner.md)]


В этой статье приводится обзор амортизации для основных средств.

Амортизация — это периодическая проводка, которая обычно уменьшает значение основных средств в балансовом отчете и учитывается в качестве расхода в счете прибыли и убытков. Поэтому, главный счет обычно используется для кредитования периодической амортизации в балансовом отчете. Корр. счет — это счет в части прибылей и убытков плана счетов.

## <a name="depreciation-adjustment"></a>Корректировка амортизации
Обычно только корректировка в уже разнесенной проводки амортизации разносится в качестве переоценки амортизации. Поэтому настраиваются главный и корр. счет аналогично как и счета для амортизации. Корректировка амортизации может быть положительной или отрицательной суммой, но функциональность главного счета (в качестве счета балансового отчета) и функциональность корр. счета (обычно в качестве счета прибыли и убытков) остается той же самой.

## <a name="extraordinary-depreciation"></a>Дополнительная амортизация
Дополнительная амортизация работает аналогично базовой амортизации. Поэтому счет ГК используется для кредитования суммы амортизации в балансовом отчете и уменьшает значение основного средства. Корр. счет — это счет учета прибыли и расходов, где амортизация рассчитывается для финансового периода вычитается как расход. 

Дополнительная амортизация функционирует независимо от базовой амортизации. Применение дополнительной амортизации в качестве отдельного типа проводки позволяет разнести и представить в отчете дополнительную амортизацию отдельно от обычной базовой амортизации.

## <a name="special-depreciation-allowance"></a>Особая амортизационная премия
Можно использовать специальные амортизационные премии, чтобы взимать суммы дополнительной амортизации в течении первого года, в который актив введен в эксплуатацию и амортизируется. Амортизационные премии необходимо применять до любых других расчетов амортизации. Поскольку амортизационные премии часто становятся известны только на более поздних этапах срока службы основного средства, рекомендуется использовать этот тип амортизации с книгой, которая на разносится в главную книгу. Можно использовать периодическую функцию "Удалить проводки, не разнесенные в главную книгу" для удаления истории проводок для этих книг. Затем можно удалить историю амортизации для журнала основных средств, разнести амортизационную премия, когда она станет известна, а затем разнести остальные проводки амортизации за год. 

Можно создать неограниченное количество записей специальных амортизационных премий. После назначения этих записей журналу группы активов они используются для журнала активов. 

Специальная амортизационная премия вводится как процент или фиксированная сумма. При разноске предложений по амортизации проводки амортизационной премии разносятся в книгу как проводки, отделенные от проводок амортизации.

## <a name="depreciation-calendars"></a>Календари амортизации
Каждая книга имеет календарь, который используется при амортизации основных средств. Если не указать календарь в книге, по умолчанию книга использует финансовый календарь книги учета. Необходимо выбрать финансовый календарь для книги, когда связанный с книгой профиль амортизации использует фискальный год амортизации. 

Вы можете создать общие календари, используя страницу **Финансовые календари** в главной книге.

Дополнительные сведения см. в разделе [Методы амортизации и соглашения по амортизации](depreciation-methods-conventions.md).



