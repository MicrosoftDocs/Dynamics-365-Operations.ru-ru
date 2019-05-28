---
title: Настройка разделителя плана счетов как уникального
description: В Dynamics 365 for Finance and Operations не допускается одинаковый разделитель для плана счетов и значений аналитик. После обновления необходимо изменить значения разделителя.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559536"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Настройка разделителя плана счетов как уникального

[!include [banner](../includes/banner.md)]

В Microsoft Dynamics AX 2012 можно использовать одинаковые разделителя для вашего плана счетов и значений аналитик. В Dynamics 365 for Finance and Operations не допускается одинаковый разделитель для плана счетов и значений аналитик. Если имеется дублирующий разделитель, его можно изменить после обновления. 

Эта функция недоступна в:
- Dynamics 365 for Finance and Operations версии 8.0
- Dynamics 365 for Finance and Operations версии 7.1, KB 4094701, Невозможно ввести финансовые аналитики, когда значения аналитики содержат разделитель плана счетов
- Dynamics 365 for Finance and Operations версии 7.2, KB 4092967 Невозможно выбрать подпроект как аналитику, когда формат подпроекта содержит разделитель аналитики

## <a name="update-delimiter"></a>Обновление разделителя
Если имеется конфликт с планом счетов, можно изменить разделитель плана счетов и формат кода проекта/подпроекта. Никакие другие разделители аналитики изменить невозможно. 
- Разделитель плана счетов можно изменить после обновления на Finance and Operations в **Параметры главной книги** > **Планы счетов и аналитики** > **Изменить разделитель**. 
- Если имеется только конфликт с форматом кода проекта/подпроекта, можно изменить это значение в параметре **Параметры модуля "Управление и учет по проектам"** > **Общее** > **Изменить формат подпроекта**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Как определить, требуется ли в вашей среде обновление разделителей 
В случае конфликта разделители в обновленной среде возможна неустойчивая работа при вводе значений в элементе управление сегментированным вводом или элементе управления вводом аналитики. Это означает, что необходимо будет всегда использовать поиск с подстановкой или всплывающее меню при вводе комбинаций счета и аналитики.
