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
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>При выборе нового кода лота очищается номер партии

Номер статьи базы знаний: 4613107

## <a name="symptoms"></a>Симптомы

При просмотре строки журнала отгрузочных накладных значение в поле **Номер партии** очищается, если выбрано новое значение в поле **Код лота**.

## <a name="resolution"></a>Приказ

Система работает в соответствии с разработанным поведением. При изменении кода лота изменяется контекст номенклатуры. Поэтому номер партии сбрасывается.

Чтобы связать номер партии с кодом лота, необходимо сначала установить код лота.
