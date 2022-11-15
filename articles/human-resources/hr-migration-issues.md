---
title: Известные проблемы объединение инфраструктуры Dynamics 365 Human Resources
description: В этой статье перечислены проблемы, которые могут возникать во время объединения инфраструктуры Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f5981801317ad9647f57a0f68f9b67b592256ab
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752699"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Известные проблемы объединение инфраструктуры Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Общие среды Dataverse

Платформа двойной записи не поддерживает связывание двух сред приложений для управления финансами и операциями с одной и той же средой Dataverse. Если у вас имеется среда Dataverse, которая совместно используется обеими следующими элементами, необходимо либо скопировать среду Dataverse, либо разделить ее:

- Приложение для управления финансами и операциями
- Текущая среда Human Resources

## <a name="environment-type-requirements"></a>Требования к типу среды

Прежде чем выполнять миграцию, необходимы следующие типы сред:

- Если автономные среды песочницы отсутствуют, необходимо создать одну такую среду для проверки миграции.
- Если имеется несколько автономных производственных сред, можно выполнить миграцию одной из них. Обратитесь в службу поддержки Microsoft, чтобы пометить другие среды в качестве "песочницы".

## <a name="teams-integration"></a>Интеграция с Teams

Существующее приложение Human Resources в Teams в данный момент переводится в решение Microsoft Power Platform. Дополнительные сведения см. в разделе [Приложение Human Resources в Teams](hr-admin-teams-leave-app.md).

