---
title: Синхронизация даты и времени в заданиях импорта
description: Чтобы избежать проблем с преобразованием часового пояса, используйте часовые пояса в формате UTC в заданиях импорта.
author: peakerbl
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c76eadc5839785ba1624ee3894ef1d0872369aa9
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403849"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Синхронизация даты и времени в заданиях импорта

[!include [banner](../includes/banner.md)]

Важно задать для задания импорта часовой пояс с временем в формате UTC. При использовании других настроек в импортируемых данных могут отображаться неправильные даты и время. Без правильной настройки процесс импорта преобразует дату в формате UTC в локальный формат, а затем настройки системы снова преобразуют его.

Это двойное преобразование приводит к изменению дат между приложениями. Например, двойное преобразование может привести к тому, что дата начала работы сотрудника будет разной в приложениях Dynamics 365 Human Resources и Dynamics 365 Finance в результате разницы в местных часовых поясах. Настройка задания импорта в формате UTC разрешает эту проблему.

1. В Dynamics 365 Finance and Operations выберите **Управление данными**.

2. Выберите **Проекты импорта**, затем выберите проект.

3. В пункте **Исходный формат даты** выберите **CSV-Unicode**.

   [![Изменение исходного формата даты на UTC.](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Измените **Часовой пояс** на **Часовой пояс UTC** и измените **Язык** на **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
