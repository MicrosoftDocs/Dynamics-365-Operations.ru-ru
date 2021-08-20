---
title: После запроса изменения добавление строки в заявку на покупку невозможно
description: Система не позволяет добавлять строку в заявку на покупку после запроса изменения.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchReqTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: jeyao
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f873a487eb573eca562b3f7cd350ed0977a035ecd77b326c5d179777f559d817
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753827"
---
# <a name="you-cant-add-a-line-to-a-purchase-requisition-after-you-request-a-change"></a>После запроса изменения добавление строки в заявку на покупку невозможно

Номер статьи базы знаний: 4611211

## <a name="symptoms"></a>Симптомы

Система не позволяет добавлять строку в заявку на покупку после запроса изменения.

## <a name="resolution"></a>Приказ

Необходимо отозвать рабочий процесс. После того как заявка на покупку получает статус *Черновик*, ее можно продолжить редактировать или добавить к ней строку.
