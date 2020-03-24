---
title: Поддерживаемые сценарии для настройки двойной записи
description: В этом разделе описываются сценарии, поддерживаемые для настройки с двойной записью.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112507"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Поддерживаемые сценарии для настройки двойной записи

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Можно настроить подключение с двойной записью между средой Finance and Operations и средой Common Data Service.

+ **Среда Finance and Operations** предоставляет основную платформу для **приложений Finance and Operations** (например, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail и Dynamics 365 Human Resources).
+ **Среда Common Data Service** предоставляет основную платформу для **приложений на основе моделей в Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing и Dynamics 365 Project Service Automation).

Механизм настройки различается в зависимости от подписки и среды.

+ Для новых экземпляров приложений Finance and Operations настройка подключения с двойной записью начинается с Microsoft Dynamics Lifecycle Services (LCS). Если у вас есть лицензия на Microsoft Power Platform, вы получите новую среду Common Data Service, если у клиента ее нет.
+ Для существующих экземпляров приложений Finance and Operations настройка подключения двойной записи начинается со среды Finance and Operations.

Поддерживаются следующие сценарии настройки:

+ [Новый экземпляр приложения Finance and Operations и новый экземпляр приложения на основе модели](#new-new)
+ [Новый экземпляр приложения Finance and Operations и существующий экземпляр приложения на основе модели](#new-existing)
+ [Новый экземпляр приложения Finance and Operations с демонстрационными данными и новый экземпляр приложения на основе модели](#new-demo-new)
+ [Новый экземпляр приложения Finance and Operations с демонстрационными данными и существующий экземпляр приложения на основе модели](#new-demo-existing)
+ [Существующий экземпляр приложения Finance and Operations и новый или существующий экземпляр приложения на основе модели](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>Новый экземпляр приложения Finance and Operations и новый экземпляр приложения на основе модели

Для настройки подключения с двойной записью между новым экземпляром приложения Finance and Operations, в котором отсутствуют данные, и новым экземпляром приложения на основе модели в Dynamics 365, выполните действия, указанные в разделе [Настройка двойной записи из Lifecycle Services](lcs-setup.md). После завершения настройки подключения выполняются следующие действия автоматически:

- Подготавливается новая пустая среда Finance and Operations.
- Будет подготовлен новый пустой экземпляр приложения на основе модели, в котором устанавливается простое решение CRM.
- Для данных компании DAT устанавливается подключение с двойной записью.
- Сопоставления объектов включаются для синхронизации в реальном времени.

Обе среды затем готовы для синхронизации данных в режиме реального времени.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>Новый экземпляр приложения Finance and Operations и существующий экземпляр приложения на основе модели

Для настройки подключения с двойной записью между новым экземпляром приложения Finance and Operations, в котором отсутствуют данные, и существующим экземпляром приложения на основе модели в Dynamics 365, выполните действия, указанные в разделе [Настройка двойной записи из Lifecycle Services](lcs-setup.md). После завершения настройки подключения выполняются следующие действия автоматически:

- Подготавливается новая пустая среда Finance and Operations.
- Для данных компании DAT устанавливается подключение с двойной записью.
- Сопоставления объектов включаются для синхронизации в реальном времени.

Обе среды затем готовы для синхронизации данных в режиме реального времени.

Чтобы синхронизировать существующие данные Common Data Service с приложением Finance and Operations, выполните следующие действия.

1. Создайте новую компанию в приложении Finance and Operations.
2. Добавьте эту компанию в настройку подключения двойной записи.
3. [Выполните начальную загрузку](bootstrap-company-data.md) данных Common Data Service с помощью трехбуквенного кода ISO компании.

Поскольку двойная запись является режимом синхронизации в реальном времени, данные из Common Data Service автоматически начинают перетекать в приложение Finance and Operations.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>Новый экземпляр приложения Finance and Operations с демонстрационными данными и новый экземпляр приложения на основе модели

Чтобы настроить подключение с двойной записью между новым экземпляром приложения Finance and Operations, в котором имеются демонстрационные данные, и новым экземпляром приложения на основе модели в Dynamics 365, следуйте указаниям из раздела [Новый экземпляр приложения Finance and Operations и новый экземпляр приложения на основе модели](#new-new) ранее в этом разделе. Если после завершения настройки подключения требуется синхронизировать демонстрационные данные с приложением на основе модели, выполните следующие действия.

1. Откройте приложение Finance and Operations на странице LCS, войдите в систему, затем откройте **Управление данными \> Двойная запись**.
2. Выполните функцию **Начальная синхронизация** для тех объектов, для которых требуется синхронизировать данные.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>Новый экземпляр приложения Finance and Operations с демонстрационными данными и существующий экземпляр приложения на основе модели

Чтобы настроить подключение с двойной записью между новым экземпляром приложения Finance and Operations, в котором имеются демонстрационные данные, и существующим экземпляром приложения на основе модели в Dynamics 365, следуйте указаниям из раздела [Новый экземпляр приложения Finance and Operations и существующий экземпляр приложения на основе модели](#new-existing) ранее в этом разделе. Если после завершения настройки подключения требуется синхронизировать демонстрационные данные с приложением на основе модели, выполните следующие действия.

1. Откройте приложение Finance and Operations на странице LCS, войдите в систему, затем откройте **Управление данными \> Двойная запись**.
2. Выполните функцию **Начальная синхронизация** для тех объектов, для которых требуется синхронизировать данные.

Чтобы синхронизировать существующие данные Common Data Service с приложением Finance and Operations, выполните следующие действия.

1. Создайте новую компанию в приложении Finance and Operations.
2. Добавьте эту компанию в настройку подключения двойной записи.
3. [Выполните начальную загрузку](bootstrap-company-data.md) данных Common Data Service с помощью трехбуквенного кода ISO компании.

Поскольку двойная запись является режимом синхронизации в реальном времени, данные из Common Data Service автоматически начинают перетекать в приложение Finance and Operations.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>Существующий экземпляр приложения Finance and Operations и новый или существующий экземпляр приложения на основе модели

Настройка подключения двойной записи между существующим экземпляром приложения Finance and Operations и новым или существующим экземпляром приложения на основе модели в Dynamics 365 производится в среде Finance and Operations.

1. Настройте подключение из приложения Finance and Operations.
2. Чтобы синхронизировать существующие данные Common Data Service с приложением Finance and Operations, необходимо [выполнить загрузку](bootstrap-company-data.md) данных Common Data Service, используя трехбуквенный код компании ISO.

Поскольку двойная запись является режимом синхронизации в реальном времени, данные из Common Data Service автоматически начинают перетекать в приложение Finance and Operations.
