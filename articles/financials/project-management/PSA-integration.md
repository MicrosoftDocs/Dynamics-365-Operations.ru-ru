---
title: Обзор Project Service Automation
description: В этом разделе содержатся сведения о решении интеграции Project Service Automation с Finance and Operations. Это решение интеграции использует функцию интеграции данных для синхронизации данных между экземплярами Microsoft Dynamics 365 for Finance and Operations и Microsoft Dynamics 365 for Project Service Automation с помощью Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85dde35033122ad234ec8efd1bddf64b950578ef
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865636"
---
# <a name="project-service-automation-overview"></a>Обзор Project Service Automation

[!include[banner](../includes/banner.md)]

Решение интеграции Project Service Automation с Finance and Operations использует интеграцию данных для синхронизации данных между экземплярами Microsoft Dynamics 365 for Finance and Operations и Microsoft Dynamics 365 for Project Service Automation с помощью Common Data Service. Шаблоны интеграции, доступные с функцией интеграции данных, позволяют передавать данные по проектам, контрактам проекта, строкам контракта проекта, этапам строк контракта проекта, задачам проекта, категориям транзакции расходов, оценкам часов и оценкам расходов из Project Service Automation в Finance and Operations.

> [!NOTE]
> - При использовании Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, после установки обновлений КБ 4132657 и 4132660 КБ, можно использовать шаблоны для интеграции задачи проекта, категорий транзакций расходов, оценок часов, оценок расходов и фактических данных и для настройки функции блокировки. Если необходимо сбросить распределения по бухгалтерским счетам, рекомендуется также установить КБ 4131710.
> - При использовании Finance and Operations 7.3.0 необходимо установить KB 4074835. После этого можно будет интегрировать проекты с фиксированной ценой.
> - Если при использовании Finance and Operations 7.3.0 вы переносите проводки по сборам из Project Service Automation, чтобы включить эти расходы в накладную проекта необходимо установить KB 4345320.
> - Если вы используете Microsoft Dynamics 365 for Finance and Operations версии 8.0, вы можете использовать интеграция задач проекта, категории транзакции расходов, оценки часов, оценки затрат и блокировку функциональности.
> - При использовании Microsoft Dynamics 365 for Finance and Operations версии 8.0.1 или новее можно выполнить синхронизацию фактических данных.

Перед интеграцией Project Service Automation with Finance and Operations необходимо конфигурировать параметры интеграции Project Service Automation. Для получения дополнительных сведений см. раздел [Параметры интеграции Project Service Automation](PSA-parameters.md).

Эта интеграция обеспечивает прямую синхронизацию в следующих сценариях:

- Поддержка контрактов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations
- Создание проектов в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations.
- Поддержка строк контракта по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations
- Поддержка этапов строк контракта по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations
- Поддержка задач по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations
- Поддержка категорий транзакции расходов в Finance and Operations и их синхронизация непосредственно из Finance and Operations в Project Service Automation.
- Создание оценок часов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations.
- Создание оценок расходов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance and Operations.
- Создание фактических данных проекта по времени, расходам и сборам в Project Service Automation и создание проводок по проекту в журнале интеграции Project Service Automation, чтобы из можно было разнести в Finance and Operations.

## <a name="data-synchronization"></a>Синхронизация данных

На следующем рисунке показано, как данные синхронизируются в рамках интеграции между Project Service Automation и Finance and Operations.

> [!NOTE]
> Не все шаблоны в данный момент доступны. Шаблоны освобождаются сразу после их завершения.

[![Интеграция Project Service Automation с Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Системные требования для Finance and Operations

Чтобы использовать решение интеграции Project Service Automation в Finance and Operations, необходимо установить Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 с обновлениями платформы 12 или более поздней версии.

## <a name="system-requirements-for-project-service-automation"></a>Требования к системе для Project Service Automation

Чтобы использовать решение интеграции Project Service Automation в Finance and Operations необходимо установить следующие компоненты:

- Microsoft Dynamics 365 for Project Service Automation версии 9.0.0.0 или более новая версия
- Решение "Перспективный клиент в наличные деньги" для Microsoft Dynamics 365 for Sales, версия 1.14.0.0 (v14) или более новая версия
- Решение для интеграции Project Service Automation в Finance and Operations для Microsoft Dynamics 365 for Project Service Automation версии 1.0.0.0 или новее

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Установите решение интеграции Project Service Automation в Finance and Operations в вашем экземпляре Project Service Automation

Загрузите решение интеграции Project Service Automation с Finance and Operations из [центра загрузки Майкрософт](https://www.microsoft.com/download/details.aspx?id=57016) и следуйте указаниям, включенным в решение.
