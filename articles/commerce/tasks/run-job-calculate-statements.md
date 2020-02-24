---
title: Настройка и выполнение задания для расчета отчетов
description: Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для создания и расчета журналов операций для выбранного магазина или группы магазинов.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52798303ef5d96a44270f971703928d0c6c4c2c1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023786"
---
# <a name="configure-and-run-job-to-calculate-statements"></a>Настройка и выполнение задания для расчета отчетов

[!include[task guide banner](../includes/task-guide-banner.md)]

Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для создания и расчета журналов операций для выбранного магазина или группы магазинов. В этой процедуре используется компания с демонстрационными данными USRT.

1. Перейдите "Все рабочие области > Финансовая информация магазина".
2. Щелкните "Создать строки журнала операций".
    * Выберите конкретный магазин или узел, если вы хотите создать пакетное задание для группы магазинов.  
    * Нажмите на стрелку для добавления выбора.  
3. Щелкните вкладку "Выполнять в фоновом режиме".
4. В поле "Пакетная обработка" выберите "Да".
5. Щелкните "Повторение".
6. В поле "Дата начала" введите дату.
7. В поле "Время начала" введите время.
8. Выберите параметр "Дата завершения не указана".
9. В поле PatternUnit введите "Дни".
10. В поле "На" введите число.
11. Нажмите кнопку "OК".
12. Нажмите кнопку "OК".

