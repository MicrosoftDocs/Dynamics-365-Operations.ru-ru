---
title: Устранение неполадок аналитических отчетов
description: В этой статье объясняется, что делать, если изменения данных клиента не отображаются ни в одной из рабочих областей клиента.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010283"
---
# <a name="troubleshoot-analytic-reports"></a>Устранение неполадок аналитических отчетов

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
