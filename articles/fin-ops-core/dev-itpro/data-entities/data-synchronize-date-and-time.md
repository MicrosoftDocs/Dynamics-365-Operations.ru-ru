---
title: Синхронизация даты и времени в заданиях импорта
description: Чтобы избежать проблем с преобразованием часового пояса, используйте часовые пояса в формате UTC в заданиях импорта.
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748677"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Синхронизация даты и времени в заданиях импорта

[!include [banner](../includes/banner.md)]

Важно задать для задания импорта часовой пояс с временем в формате UTC. При использовании других настроек в импортируемых данных могут отображаться неправильные даты и время. Без правильной настройки процесс импорта преобразует дату в формате UTC в локальный формат, а затем настройки системы снова преобразуют его.

Это двойное преобразование приводит к изменению дат между приложениями. Например, двойное преобразование может привести к тому, что дата начала работы сотрудника будет разной в приложениях Dynamics 365 Human Resources и Dynamics 365 Finance в результате разницы в местных часовых поясах. Настройка задания импорта в формате UTC разрешает эту проблему.

1. В Dynamics 365 Finance and Operations выберите **Управление данными**.

2. Выберите **Проекты импорта**, затем выберите проект.

3. В пункте **Исходный формат даты** выберите **CSV-Unicode**.

   [![Изменение исходного формата даты на UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Измените **Часовой пояс** на **Часовой пояс UTC** и измените **Язык** на **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]