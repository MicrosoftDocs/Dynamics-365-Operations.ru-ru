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
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Сторнирование приемки создает неожиданную открытую проводку

Номер статьи базы знаний: 4612469

## <a name="symptoms"></a>Симптомы

Если сторнировать приемку с маркировкой система создает открытую проводку, в которой сторнированное количество имеет те же складские аналитики, что и сторнированная проводка.

## <a name="resolution"></a>Приказ

При сторнировании операции "приемка" складская аналитика инициализируется из производственного журнала. Поэтому она получает номер партии. Из-за маркировки проводки по заказу на продажу наследуют номер партии.

Аналитика может быть сброшена после разноски приемки.
