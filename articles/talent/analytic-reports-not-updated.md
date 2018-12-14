---
title: "Аналитические отчеты не обновляются"
description: "В этом разделе объясняется, что делать, если изменения данных клиента не отображаются ни в одной из рабочих областей клиента."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: ru-ru
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a>Аналитические отчеты не обновляются

[!include [banner](includes/banner.md)]

**Расход**

Изменения данных клиента не отображаются на вкладках **Аналитики** ни одной из рабочих областей клиента.

**Причина**

По умолчанию отчеты Microsoft Power BI обновляются каждые четыре часа согласно графику пакетного задания развертывания измерения.

**Разрешение**

Эта проблема может быть просто вопросом времени. Выполните следующие шаги для запуска пакетного задания и обновления рабочих областей аналитик.

1. Откройте страницу **Пакетные задания** в меню **Администрирование системы \> Ссылки \> Пакетные задания \> Пакетные задания**. Можно также использовать поиск и ввести **Пакетные задания**.
1. Найдите в списке задание **Развертывание измерения**.
1. Выберите **Изменить** в верхней части страницы, и задайте для запланированной даты и времени запуска значение, которое обновит аналитики ближе к текущему времени.

![Пакетные задания](media/batch-jobs.png)

