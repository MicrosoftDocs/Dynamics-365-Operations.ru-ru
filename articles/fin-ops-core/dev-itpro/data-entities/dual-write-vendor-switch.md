---
title: Переключение между дизайнами поставщиков
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772372"
---
# <a name="switch-between-vendor-designs"></a>Переключение между дизайнами поставщиков

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Поток данных поставщика 

Если используете другие приложения Dynamics 365 для обработки поставщиков и хотите изолировать информацию о поставщиках от информации о клиентах, используйте основной дизайн поставщика.  

![Основной поток поставщика](media/dual-write-switch-1.png)
 
Если используете другие приложения Dynamics 365 для обработки поставщиков и хотите продолжать использовать сущность **Организация** для хранения информации о поставщиках, используйте этот расширенный дизайн поставщика. В этом дизайне расширенные сведения о поставщике, такие как статус заблокированного поставщика и профиль поставщика, хранятся в объекте **поставщики** в Common Data Service. 

![Поток расширенных поставщиков](media/dual-write-switch-2.png)
 
Выполните следующие действия, чтобы использовать расширенный дизайн поставщиков: 
 
1. Пакет решения **SupplyChainCommon** содержит шаблоны workflow-процессов, как показано на следующем рисунке.
    > [!div class="mx-imgBorder"]
    > ![Шаблоны workflow-процессов](media/dual-write-switch-3.png)
2. Создание новых workflow-процессов с помощью шаблонов workflow-процессов: 
    1. Создайте новый workflow-процесс для объекта **Поставщик** с помощью шаблона workflow-процессов **Создание поставщиков в объекте "Организация"** и щелкните **ОК**. Этот workflow-процесс обрабатывает сценарий создания поставщиков для объекта **Организация**.
        > [!div class="mx-imgBorder"]
        > ![Создание поставщиков в объекте "Организация"](media/dual-write-switch-4.png)
    2. Создайте новый workflow-процесс для объекта **Поставщик** с помощью шаблона workflow-процессов **Обновление объекта "Организации"** и щелкните **ОК**. Этот workflow-процесс обрабатывает сценарий обновления поставщиков для объекта **Организация**. 
        > [!div class="mx-imgBorder"]
        > ![Обновление объекта "Организации"](media/dual-write-switch-5.png)
    3. Создание workflow-процессов из шаблонов, созданных в объекте **Организации**. 
        > [!div class="mx-imgBorder"]
        > ![Создание поставщиков в объекте "Поставщики"](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Обновление объекта "Поставщики"](media/dual-write-switch-7.png)
    4. Workflow-процессы можно настроить как workflow-процессы в реальном времени или в фоновом режиме в соответствии с требованиями пользователя. 
        > [!div class="mx-imgBorder"]
        > ![Преобразование в фоновый workflow-процесс](media/dual-write-switch-8.png)
    5. Активируйте workflow-процессы, созданные в объектах **Организация** и **Поставщик**, чтобы начать использовать объект **Организация** Customer Engagement для хранения информации о поставщике. 
 
