---
title: Настройка и выполнение задания для разноски отчетов
description: Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для разноски журналов операций для выбранного магазина или группы магазинов.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b1401d51491205731843abe6e2278f798c5c979
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232745"
---
# <a name="configure-and-run-job-to-post-statements"></a>Настройка и выполнение задания для разноски отчетов

[!include [banner](../includes/banner.md)]

Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для разноски журналов операций для выбранного магазина или группы магазинов. В этой процедуре используется компания с демонстрационными данными USRT.

1. Перейдите в раздел "Все рабочие области" > .. > Финансовая информация магазина.
2. Нажмите «Пакетная разноска журналов операций»
    * Выберите организационную иерархию, а затем в дереве узлов организации выберите отдельный магазин или узел. Выберите узел, если вы хотите создать пакетное задание для группы магазинов.  
    * Нажмите на стрелку для добавления выбора.  
3. Щелкните вкладку "Выполнять в фоновом режиме". ![Выполнять в фоновом режиме](../dev-itpro/media/runbackground.png "Выполнять в фоновом режиме") 
4. Установите или снимите флажок "Пакетная обработка".
![Пакетная обработка](../dev-itpro/media/batchprocessing.png "Пакетная обработка и периодичность") 
5. Щелкните "Повторение".
6. В поле "Дата начала" введите дату.
7. В поле "Время начала" введите время.
    * Выберите, нужно ли завершать повторы после определенного количества запусков, в конкретный день или никогда. Затем выберите разные параметры, определяющие периодичность запуска задания.  
8. Нажмите кнопку "OК".
9. Нажмите кнопку "OК".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]