---
title: Переключение между вариантами дизайна поставщиков
description: Эта тема описывает способ переключения интеграции данных поставщиков между приложениями Finance and Operations и Common Data Service.
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
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902733"
---
# <a name="switch-between-vendor-designs"></a>Переключение между вариантами дизайна поставщиков

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Поток данных поставщика 

Если используете другие приложения Dynamics 365 для обработки поставщиков и хотите изолировать информацию о поставщиках от информации о клиентах, используйте основной дизайн поставщика.  

![Основной поток поставщика](media/dual-write-vendor-data-flow.png)
 
Если используете другие приложения Dynamics 365 для обработки поставщиков и хотите продолжать использовать сущность **Организация** для хранения информации о поставщиках, используйте этот расширенный дизайн поставщика. В этом дизайне расширенные сведения о поставщике, такие как статус заблокированного поставщика и профиль поставщика, хранятся в объекте **поставщики** в Common Data Service. 

![Поток расширенных поставщиков](media/dual-write-vendor-detail.jpg)
 
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
    5. Активируйте workflow-процессы, созданные в объектах **Организация** и **Поставщик**, чтобы начать использовать объект **Организация** для хранения информации о поставщике. 
 
