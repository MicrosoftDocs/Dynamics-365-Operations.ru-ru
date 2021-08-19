---
title: Синхронизация списка проектов из Supply Chain Management в Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации проектов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 920c3741ab45f4ae88ea5febba583d34b5a1230cd25316226db850730927798d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717851"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Синхронизация списка проектов из Supply Chain Management в Field Service

[!include[banner](../includes/banner.md)]

В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации проектов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.

[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service.](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи
Следующий шаблон и базовые задачи используются для выполнения синхронизации проектов из Supply Chain Management в Field Service.

**Шаблон в интеграции данных**
- Проекты (из Supply Chain Management в Field Service)

**Задача в проекте интеграции данных**
- Проекты

Чтобы была возможна синхронизация списка проектов, требуются следующие задачи синхронизации:
- Счета (из Sales в Supply Chain Management) 

## <a name="entity-set"></a>Набор объектов
| Field Service           | Управление цепочкой поставок  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Проекты                |

## <a name="entity-flow"></a>Поток объектов
Проекты создаются в Supply Chain Management. Проекты, для которых в поле **Тип проекта** задано значение **Время и расходы**, а в поле **Этап проекта** задано значение **В работе**, будут синхронизироваться с объектом **Внешний проект** в Field Service, включая номер проекта, название проекта, этап проекта и сведения об организации клиента. Список **Внешний проект** используется для сопоставления заказов на обслуживание в Field Service с проектами Supply Chain Management.

## <a name="field-service-crm-solution"></a>Решение Field Service CRM
Объект **Внешний проект** получает все проекты из Supply Chain Management. Поле **Внешний проект** было добавлено в объект **Заказ на выполнение работ**. Это поле подстановки, поэтому за счет отметки проекта в вашем заказе на выполнение работ заказ на покупку будет связан с проектом в Supply Chain Management. После изменения значения **Состояние системы** из **Открыто — В работе(690,970,000)** на более высокий статус, поле **Внешний проект** будет заблокировано и вы больше не сможете добавить, удалить или изменить значение.

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления
### <a name="supply-chain-management"></a>Управление цепочкой поставок
Включение отслеживания изменений для информационного объекта проектов

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Проекты (из Supply Chain Management в Field Service): Проекты

[![Сопоставление шаблона в интеграции данных.](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]