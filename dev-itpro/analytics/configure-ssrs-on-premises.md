---
title: "Настройка служб SQL Server Reporting Services для локального развертывания"
description: "В этой теме представлены сведения о настройке служб SQL Server Reporting Services (SSRS) для локального развертывания."
author: kfend
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, UnifiedOperations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: b0bfaadabe960f31d7609512b7ad6eaf848afddc
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a>Настройка служб SQL Server Reporting Services для локального развертывания

Используйте шаги, приведенные ранее в этой теме, для настройки служб SQL Server Reporting Services (SSRS) для развертывания Microsoft Dynamics 365 for Finance and Operations, выпуск Enterprise (локальная версия).

1. Откройте приложение "Диспетчер конфигурации Reporting Services".
2. Оставьте значение по умолчанию **Имя сервера**, которое должно представлять собой имя текущего компьютера, и **Экземпляра сервера отчетов**, **MSSQLSERVER**. 
3. Щелкните **Подключить**.
   
   [![Подключение конфигурации Reporting Services](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)
   
4. Щелкните вкладку **Учетная запись службы** и убедитесь, что параметры соответствуют приведенному ниже рисунку.

    [![Вкладка "Учетная запись службы"](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)
    
5. Щелкните вкладку **URL-адрес веб-службы** и убедитесь, что параметры соответствуют приведенному ниже рисунку. 

    [![Вкладка "URL-адрес веб-службы"](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png) 
    
6. Щелкните вкладку **База данных** и убедитесь, что значения **Имя базы данных** и **Параметры учетных данных** соответствуют приведенному ниже рисунку. **Примечание.** Будет необходимо создать новую базу данных. Для этого щелкните **Изменить базу данных**, а затем убедитесь, что имя новой базы данных: **DynamicsAxReportServer**.

    [![вкладка "База данных"](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)
    
7. Щелкните вкладку **URL-адрес веб-портала** и убедитесь, что параметры соответствуют приведенному ниже рисунку. **Примечание.** Необходимо щелкнуть **Применить** для создания и правильной настройки портала.

    [![вкладка "URL-адрес веб-портала"](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)
    
  После настройки портала вкладка **Веб-портал** будет соответствовать приведенному ниже рисунку.
    [![вкладка "Веб-портал"](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)
    
8. Перейдите по URL-адресу отчетов для просмотра веб-портал SQL Server Reporting Services. 
9.  Находясь на портале, создайте новую папку с именем **Dynamics**.

    [![папка Dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)
    
10. В разделе **Диспетчер конфигурации служб Reporting Services** щелкните вкладку **Параметры электронной почты** и убедитесь, что параметры соответствуют приведенному ниже рисунку.

    [![вкладка "Параметры электронной почты"](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)
    
11. Щелкните вкладку **Учетная запись для выполнения** и убедитесь, что параметры соответствуют приведенному ниже рисунку.

    [![вкладка "Учетная запись для выполнения"](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)
    
  Не следует изменять параметры по умолчанию на вкладке **Ключи шифрования**.
    [![вкладка "Ключи шифрования"](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)
    
12. Щелкните вкладку **Параметры подписки** и убедитесь, что параметры соответствуют приведенному ниже рисунку.

    [![вкладка "Параметры подписки"](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)
    
  Не следует изменять параметры по умолчанию на вкладке **Масштабное развертывание**.
    [![вкладка "Масштабное развертывание"](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)
    
  Не следует изменять параметры по умолчанию на вкладке **Интеграция с Power BI**.
    [![вкладка "Интеграция с Power BI"](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png) 
    
13. Щелкните **Выход**, чтобы закрыть **Диспетчер конфигурации Reporting Services**.

    [![закрытие диспетчера конфигурации служб Reporting Services](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
    

