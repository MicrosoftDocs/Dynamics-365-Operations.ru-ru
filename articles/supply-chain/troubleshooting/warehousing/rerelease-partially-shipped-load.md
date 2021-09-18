---
title: Невозможно выпустить частично отгруженную загрузку на склад
description: В более ранних версиях нельзя было повторно выпустить частично отгруженную загрузку при использовании определенных функций с неполным резервированием. Это решено.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477433"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>Невозможно выпустить частично отгруженную загрузку на склад

## <a name="symptoms"></a>Симптомы

Невозможно выпустить частично отгруженную загрузку на склад. При выполнении выпуска на склад появляется сообщение "Операция завершена", но ничего не происходит, и работа для оставшегося количества не создается. Эта проблема возникает при использовании функциональности транспортной загрузки и неполного резервирования.

## <a name="resolution"></a>Решение

[Проблема статьи базы знаний 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Частично отгруженные загрузки могут быть повторно обработаны волной и повторно обработаны") исправлена в [выпуске 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15).
