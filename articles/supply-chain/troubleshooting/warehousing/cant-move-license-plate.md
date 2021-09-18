---
title: Невозможно переместить грузоместа, если разрешены пустой выпуск и пустое поступление
description: Невозможно переместить грузоместа, если в серийном номере разрешены пустой выпуск и пустое поступление. Это будет устранено путем того, что поле "серийный номер" является необязательным.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477408"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Невозможно переместить грузоместа, если в серийном номере разрешены пустой выпуск и пустое поступление

## <a name="symptoms"></a>Симптомы

Нельзя переместить грузоместо, используя пункт меню **Перемещение**, если серийный номер имеет настройки *Пропуск для расходов* и *Пропуск для приходов* в группе аналитик отслеживания, и если в одном местоположении имеется несколько грузомест, некоторые из которых имеют серийные номера, а другие — не имеют.

## <a name="resolution"></a>Решение

Эта проблема будет устранена изменениями, которые разворачиваются в [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Эти изменения сделают поле **Серийный номер** необязательным, если разрешены пустой прием и пустой расход.
