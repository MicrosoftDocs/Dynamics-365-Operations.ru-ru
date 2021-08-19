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
ms.openlocfilehash: 73ebc45ee83516f573c3f73ef8106da9ae44c590c05d8dbd08520bc5ef19e49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714218"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Сторнирование приемки создает неожиданную открытую проводку

Номер статьи базы знаний: 4612469

## <a name="symptoms"></a>Симптомы

Если сторнировать приемку с маркировкой система создает открытую проводку, в которой сторнированное количество имеет те же складские аналитики, что и сторнированная проводка.

## <a name="resolution"></a>Приказ

При сторнировании операции "приемка" складская аналитика инициализируется из производственного журнала. Поэтому она получает номер партии. Из-за маркировки проводки по заказу на продажу наследуют номер партии.

Аналитика может быть сброшена после разноски приемки.
