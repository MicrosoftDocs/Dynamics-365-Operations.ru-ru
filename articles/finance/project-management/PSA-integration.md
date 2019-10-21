---
title: Обзор Project Service Automation
description: В этом разделе содержится информация о решении интеграции Dynamics 365 Project Service Automation с Dynamics 365 Finance.
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250561"
---
# <a name="project-service-automation-overview"></a>Обзор Project Service Automation

[!include[banner](../includes/banner.md)]

Решение интеграции Project Service Automation с Finance использует интеграцию данных для синхронизации данных между экземплярами Dynamics 365 Finance и Dynamics 365 Project Service Automation с помощью Common Data Service. Шаблоны интеграции, доступные с функцией интеграции данных, позволяют передавать данные по проектам, контрактам проекта, строкам контракта проекта, этапам строк контракта проекта, задачам проекта, категориям транзакции расходов, оценкам часов и оценкам расходов из Project Service Automation в Finance.

> [!NOTE]
> - При использовании версии 7.3.0 необходимо установить KB 4074835. После этого можно будет интегрировать проекты с фиксированной ценой.
> - Если при использовании версии 7.3.0 вы переносите проводки по сборам из Project Service Automation, чтобы включить эти расходы в накладную проекта необходимо установить KB 4345320.
> - Если вы используете версию 8.0, вы можете использовать интеграция задач проекта, категории транзакции расходов, оценки часов, оценки затрат и блокировку функциональности.
> - При использовании версии 8.0.1 или новее можно выполнить синхронизацию фактических данных.

Перед интеграцией Project Service Automation с Finance необходимо настроить параметры интеграции Project Service Automation. Для получения дополнительных сведений см. раздел [Параметры интеграции Project Service Automation](PSA-parameters.md).

Эта интеграция обеспечивает прямую синхронизацию в следующих сценариях:

- Поддержка контрактов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.
- Создание проектов в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.
- Поддержка строк контрактов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.
- Поддержка промежуточных этапов строк контрактов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.
- Поддержка задач по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.
- Поддержка категорий транзакции расходов в Finance и их синхронизация непосредственно из Finance в Project Service Automation.
- Создание оценок часов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.
- Создание оценок расходов по проекту в Project Service Automation и их синхронизация непосредственно из Project Service Automation в Finance.
- Создание фактических данных проекта по времени, расходам и сборам в Project Service Automation и создание проводок по проекту в журнале интеграции Project Service Automation, чтобы из можно было разнести в Finance.

## <a name="data-synchronization"></a>Синхронизация данных

На следующем рисунке показано, как данные синхронизируются в рамках интеграции между Project Service Automation и Finance.

> [!NOTE]
> Не все шаблоны в данный момент доступны. Шаблоны освобождаются сразу после их завершения.

[![Параметры интеграции Project Service Automation с Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Системные требования для Finance

Чтобы использовать решение интеграции Project Service Automation в Finance, необходимо установить , Enterprise edition 7.3 с обновлением платформы Platform update 12 или более поздней версии.

## <a name="system-requirements-for-project-service-automation"></a>Требования к системе для Project Service Automation

Чтобы использовать решение интеграции Project Service Automation с Finance, необходимо установить следующие компоненты:

- Dynamics 365 Project Service Automation версии 9.0.0.0 или более новая версия
- Решение "Перспективный клиент в наличные деньги" Dynamics 365 Sales, версия 1.14.0.0 (v14) или выше
- Решение для интеграции Project Service Automation с Finance для Dynamics 365 Project Service Automation версии 1.0.0.0 или новее

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Установите решение интеграции Project Service Automation с Finance в вашем экземпляре Project Service Automation

Загрузите решение интеграции Project Service Automation с Finance из [центра загрузки Майкрософт](https://www.microsoft.com/download/details.aspx?id=57016) и следуйте указаниям, включенным в решение.
