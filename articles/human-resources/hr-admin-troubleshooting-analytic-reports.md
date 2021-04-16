---
title: Устранение неполадок аналитических отчетов
description: В этой статье объясняется, что делать, если изменения данных клиента не отображаются ни в одной из рабочих областей клиента.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b500d519d61edfd20456355376e3fc81f16517a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794981"
---
# <a name="troubleshoot-analytic-reports"></a>Устранение неполадок аналитических отчетов

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Выдать**

Изменения данных клиента не отображаются на вкладках **Аналитики** ни одной из рабочих областей клиента.

**Причина**

По умолчанию отчеты Microsoft Power BI обновляются каждые четыре часа согласно графику пакетного задания развертывания измерения.

**Разрешение**

Эта проблема может быть просто вопросом времени. Выполните следующие шаги для запуска пакетного задания и обновления рабочих областей аналитик.

1. Откройте страницу **Пакетные задания** в меню **Администрирование системы \> Ссылки \> Пакетные задания \> Пакетные задания**. Можно также использовать поиск и ввести **Пакетные задания**.
1. Найдите в списке задание **Развертывание измерения**.
1. Выберите **Изменить** в верхней части страницы, и задайте для запланированной даты и времени запуска значение, которое обновит аналитики ближе к текущему времени.

![Пакетные задания](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]