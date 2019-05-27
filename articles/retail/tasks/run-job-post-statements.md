---
title: Настройка и выполнение задания для разноски отчетов
description: Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для разноски журналов операций для выбранного магазина или группы магазинов.
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
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550124"
---
# <a name="configure-and-run-job-to-post-statements"></a>Настройка и выполнение задания для разноски отчетов

[!include[task guide banner](../includes/task-guide-banner.md)]

Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для разноски журналов операций для выбранного магазина или группы магазинов. В этой процедуре используется компания с демонстрационными данными USRT.

1. Перейдите в раздел "Все рабочие области" > .. > "Финансовая информация розничного магазина".
2. Щелкните "Разнести журналы операций".
    * Выберите организационную иерархию, а затем в дереве узлов организации выберите отдельный магазин или узел. Выберите узел, если вы хотите создать пакетное задание для группы магазинов.  
    * Нажмите на стрелку для добавления выбора.  
3. Щелкните вкладку "Выполнять в фоновом режиме".
4. Установите или снимите флажок "Пакетная обработка".
5. Щелкните "Повторение".
6. В поле "Дата начала" введите дату.
7. В поле "Время начала" введите время.
    * Выберите, нужно ли завершать повторы после определенного количества запусков, в конкретный день или никогда. Затем выберите разные параметры, определяющие периодичность запуска задания.  
8. Нажмите кнопку "OК".
9. Нажмите кнопку "OК".

