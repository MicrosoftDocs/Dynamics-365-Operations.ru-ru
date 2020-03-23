---
title: Массовое обновление основных средств
description: При использовании книг можно изменить соглашения по амортизации для группы активов, являющейся частью одной и той же книги.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30b9aaaabcac09c9147c350422924a23f785c0ce
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179573"
---
# <a name="fixed-asset-mass-update"></a>Массовое обновление основных средств

[!include [banner](../includes/banner.md)]

При использовании книг можно изменить соглашения по амортизации для группы активов, являющейся частью одной и той же книги.

Например, если вы находитесь в Соединенных Штатах и в течение четвертого квартала ввели в эксплуатацию более 40 процентов своих основных средств, то необходимо использовать соглашение по амортизации для середины квартала. Можно использовать процесс массового обновления, чтобы внести изменения для всех активов, которым требуется новое соглашение по амортизации 

При обновлении соглашения по амортизации активов происходит удаление все проводок по амортизации, существующих для этих активов. Также удаляются все проводки корректировок амортизации, проводки амортизационных премий и проводки дополнительной амортизации для этих активов. 

Чтобы обновить соглашение по амортизации для активов, которые уже были списаны, необходимо сначала удалить существующие проводки выбытия, включая проводки, созданные по причине выполнения процесса списания. Также необходимо удалить все проводки, которые были созданы по причине выполнения процесса списания. 

После обновления соглашения по амортизации для активов можно выполнить обработку амортизации и дополнительной амортизации для каждого актива. Если это необходимо, можно выполнить корректировки амортизации вручную.




