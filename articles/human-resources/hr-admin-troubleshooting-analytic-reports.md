---
title: Устранение неполадок аналитических отчетов
description: В этой теме объясняется, как устранять неполадки и выявлять проблемы, если изменения данных клиента не отображаются ни в одной из рабочих областей клиента.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ea04c06858cc98b0e233b9133d9dfbebfe59fd6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067737"
---
# <a name="troubleshoot-analytic-reports"></a>Устранение неполадок аналитических отчетов


[!INCLUDE [PEAP](../includes/peap-2.md)]

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

![Пакетные задания.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
