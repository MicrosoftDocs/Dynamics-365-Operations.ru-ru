---
title: Руководство по устранению неполадок при интеграции данных
description: Эта тема предоставляет информацию об устранении неполадок интеграции данных между Microsoft Dynamics 365 for Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797283"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Руководство по устранению неполадок при интеграции данных

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Включение трассировки подключаемых модулей в Common Data Service и проверка сведений об ошибках подключаемого модуля двойной записи

Если вы столкнулись с проблемой или ошибкой с синхронизацией с двойной записью, вы можете проверить ошибки в журнале трассировки:

1. Прежде чем вы сможете проверить ошибки, необходимо включить трассировку подключаемых модулей, используя инструкции в разделе [Регистрация подключаемого модуля](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs), чтобы включить трассировку подключаемых модулей. Теперь вы можете проверить ошибки.
2. Выполните вход в Dynamics 365 for Sales.
3. Щелкните значок настроек (шестеренка) и выберите **Дополнительные параметры**.
4. В меню **Настройки** выберите **Настройка > Журнал трассировки подключаемых модулей**.
5. Нажмите на имя типа **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, чтобы отобразить детали ошибки.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Проверка ошибок синхронизации двойной записи в Finance and Operations

Вы можете проверить ошибки во время тестирования, выполнив следующие действия:

+ Выполните вход в LifeCycle Services (LCS).
+ Откройте проект LCS, который вы выбрали для выполнения тестирования двойной записи.
+ Перейдите в размещенные в облаке среды.
+ Удаленный рабочий стол для ВМ Finance and Operations с использованием локальной учетной записи, которая отображается в LCS.
+ Откройте средство просмотра событий. 
+ Перейдите по пути **Журналы приложений и служб > Microsoft > Dynamics > AX-DualWriteSync > Операционные**. Отображаются ошибки и детали.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Как отвязать среду Common Data Service от Finance and Operations и привязать другую среду

Вы можете обновить ссылки, выполнив следующие действия:

+ Перейдите в среду Finance and Operations.
+ Откройте управление данными.
+ Щелкните **Ссылка на CDS для приложений**.
+ Выберите все запущенные отображения и нажмите **Остановить**. 
+ Выберите все отображения и нажмите **Удалить**.

    > [!NOTE]
    > Вариант **Удалить** не появится, если выбран шаблон **CustomerV3-Account**. Отмените его выбор, если это необходимо. **CustomerV3-Account** — это старый подготовленный шаблон, который работает с решением "Перспективный клиент в наличные деньги". Поскольку он выпущен глобально, он отображается под всеми шаблонами.

+ Щелкните **Удалить связь со средой**.
+ Нажмите **Да** для подтверждения.
+ Чтобы связать новую среду, выполните шаги из [руководства по установке](https://aka.ms/dualwrite-docs).

