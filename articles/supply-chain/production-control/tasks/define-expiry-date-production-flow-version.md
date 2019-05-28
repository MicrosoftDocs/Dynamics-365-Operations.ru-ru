---
title: Определение даты окончания срока действия для версии производственного потока
description: Чтобы завершить срок действия и обработку версии производственного потока на определенную дату или запланировать замену активной версии новой версией, необходимо задать дату окончания для версии.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa0bde90273f9392a36732ed79afdad2eea8bf86
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573219"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Определение даты окончания срока действия для версии производственного потока

[!include [task guide banner](../../includes/task-guide-banner.md)]

Чтобы завершить срок действия и обработку версии производственного потока на определенную дату или запланировать замену активной версии новой версией, необходимо задать дату окончания для версии. Нет необходимости деактивировать версию.


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a>Установка даты окончания для завершения версии производственного потока
1. Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".
2. В списке найдите и выберите требуемую запись.
    * Выберите любой производственный поток, который имеет уже определенную версию.  
3. В списке перейдите по ссылке в выбранной строке.
4. Щелкните "Изменить".
5. В списке пометьте выбранную строку.
6. В поле "Дата окончания срока действия" введите дату и время.
    * Для даты окончания срока действия новая версия не начнется и не станет активной. Также будет невозможно создавать или запускать задания для данного производственного потока. Тем не менее можно завершать запущенные задания после окончании срока действия.  

