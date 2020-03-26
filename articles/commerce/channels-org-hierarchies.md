---
title: Настройка организационных иерархий
description: В этом разделе описывается, как настроить организационные иерархии в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 29d4b686cbb66715196fca06e4642fbb8a337ace
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113859"
---
# <a name="set-up-organization-hierarchies"></a>Настройка организационных иерархий


[!include [banner](includes/banner.md)]

В этом разделе описывается, как настроить организационные иерархии в Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Перед созданием каналов необходимо подтвердить настройку организационных иерархий.

Организационные иерархии служат для просмотра сведений и составления отчетов о бизнесе с разных точек зрения. Например, можно настроить одну иерархию для налоговой, юридической или правовой отчетности. И можно настроить другую иерархию, чтобы составлять отчеты с использованием финансовой информации, которая не является юридически обязательной, но используется для целей внутренней отчетности.

Перед созданием организационной иерархии необходимо создать организации. Дополнительные сведения см. в задачах [Создание юридических лиц](channels-legal-entities.md) или [Создание операционных единиц](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Дополнительные сведения см. в следующих разделах.
- [Обзор организаций и организационных иерархий](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [Планирование организационной иерархии](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [Создание организационной иерархии](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Создание организационной иерархии

Для создания организационной иерархии выполните следующие действия.

1. В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Организационные иерархии**.
1. В области действий выберите **Создать**.
1. В поле **Имя** введите значение.
1. В разделе **Назначение** выберите **Назначение цели**.
1. В списке найдите и выберите требуемую запись. Выберите цель для назначения организационной иерархии.
1. В разделе **Назначенные иерархии** выберите **Добавить**.
1. В списке пометьте выбранную строку. Найдите только что созданную иерархию.
1. Нажмите **ОК**.

На следующем рисунке показан пример организационной иерархии, созданной для вымышленного набора магазинов "Adventure Works".

![Пример организационное иерархии](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Добавление организаций в иерархию

Чтобы добавить организации в иерархию, выполните следующие действия.

1. В списке найдите и выберите требуемую запись. Выберите иерархию.
1. На панели операций выберите **Вид**.
1. Добавьте организации при необходимости.
1. Чтобы добавить организацию, выберите **Правка**, затем выберите **Вставить**. После внесения изменений можно сохранить черновик и опубликовать изменения.

На следующем рисунке показано юридическое лицо, добавленное в корень иерархии, и четыре места возникновения затрат, добавленные для каналов "Торговый центр", "Торговая точка", "Интернет" и "Центр обработки вызовов". Затем можно добавить каналы розничной торговли, центра обработки вызовов и интернет-каналы.

![Пример конструктора иерархий](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор организаций и организационных иерархий](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Планирование организационной иерархии](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Создание юридических лиц](channels-legal-entities.md)

[Создание операционных единиц](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Обзор каналов](channels-overview.md)

[Необходимые условия для настройки каналов](channels-prerequisites.md)
