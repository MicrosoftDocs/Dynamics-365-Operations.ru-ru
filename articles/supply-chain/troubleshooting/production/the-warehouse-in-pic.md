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
ms.openlocfilehash: 970930bbdd30b57a8374de7810bb3ece8cb19a7010b5ef19d90bfc39d09f172b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740559"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Склад в журнале отгрузочных накладных не обновляется в строке спецификации

Номер статьи базы знаний: 4614848

## <a name="symptoms"></a>Симптомы

Склад в журнале отгрузочных накладных не обновляется в строке спецификации.

## <a name="resolution"></a>Приказ

Система работает в соответствии с разработанным поведением. Если создается строка журнала отгрузочных накладных со ссылкой (через код лота) в строке производственной спецификации, склад в строке производственной спецификации не обновляется, если складская аналитика в строке журнала отгрузочных накладных изменяется позднее.
