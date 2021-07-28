---
title: Обзор интеграции Dynamics 365 Commerce и Microsoft Teams
description: В этой теме представлен обзор интеграции Microsoft Dynamics 365 Commerce и Microsoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6d82c1cafe35db5523c58870f4dcb2a7f63134a1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352646"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Обзор интеграции Dynamics 365 Commerce и Microsoft Teams

[!include [banner](includes/banner.md)]

В этой теме представлен обзор интеграции Microsoft Dynamics 365 Commerce и Microsoft Teams.

Dynamics 365 Commerce интегрируется с Teams, чтобы помочь клиентам и их сотрудникам повысить производительность за счет синхронизации управления задачами между двумя приложениями. Бесшовное управление задачами, которое предоставляет интеграция Commerce и Teams, позволяет менеджерам магазинов и сотрудникам создавать списки задач, назначать задачи нескольким магазинам и отслеживать статус задач по магазинам из любого из этих приложений.

Интеграция Commerce и Teams доступна в выпуске Commerce версии 10.0.18.

## <a name="key-features"></a>Ключевые возможности

Вот некоторые из основных функций, обеспечиваемых интеграцией Commerce и Microsoft Teams:

- Подготовьте Teams, используя хорошо определенную информацию из Commerce, такую как организационная структура и сведения о магазинах, работниках, разрешениях и контексте бизнеса.
- Без труда синхронизируйте текущие изменения (например, добавление новых магазинов или приемов новых сотрудников) между Commerce и Teams, но сохраняйте Commerce в качестве основного источника данных организационной структуры.
- Интеграция управления задачами между Commerce и Teams помогает работникам магазинов, менеджерам магазинов, региональным менеджерам и менеджерам по взаимодействию управлять задачами из любого из этих приложений.

## <a name="prerequisites-for-using-integration-features"></a>Необходимые условия для использования функций интеграции

Прежде чем можно будет приступить к использованию функций интеграции Microsoft Teams, должны быть выполнены следующие условия:

- Стандартная лицензия Microsoft 365 бизнес (Эта лицензия содержит Teams.)
- Учетные записи Azure Active Directory (Azure AD) для всех менеджеров и работников магазинов
- Системы POS-терминалов, настроенные с проверкой подлинности Azure AD

## <a name="conceptual-architecture"></a>Концептуальная архитектура

На следующем рисунке показана концептуальная архитектура интеграции Dynamics 365 Commerce и Microsoft Teams, в качестве примера используется магазин в Сан-Франциско. Teams и приложение POS-терминала Commerce используют Microsoft Planner в качестве репозитория, чтобы задачи, опубликованные из Teams, отображались в приложении POS-терминала, а задачи, созданные менеджером магазина в приложении POS-терминала, были представлены в Teams, что приводит к бесшовному управлению задачами между приложениями.    

![Архитектура интеграции Commerce и Teams.](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Включение интеграции Dynamics 365 Commerce и Microsoft Teams](enable-teams-integration.md)

[Подготовка Microsoft Teams из Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Синхронизация управления задачами между Microsoft Teams и Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Управление ролями пользователей в Microsoft Teams](manage-user-roles-teams.md)

[Сопоставление магазинов и рабочих групп, если имеются готовые рабочие группы в Microsoft Teams](map-stores-existing-teams.md)

[Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams](teams-integration-faq.md)
