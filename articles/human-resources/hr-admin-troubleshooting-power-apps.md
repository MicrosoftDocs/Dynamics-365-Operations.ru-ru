---
title: Невозможно создать среду в центре администрирования Power Apps
description: В этой статье объясняется, что делать, если администратор не может создать среду в центре администрирования Microsoft Power Apps.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f4c75706183a3d6c961852395e464d46ba3ec1f2
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010302"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Невозможно создать среду в центре администрирования Power Apps

**Выдать**

- Администратор владельца/среды не может создать среду в центре администрирования Microsoft Power Apps.
- Лицензия, дающая пользователям право на выполнение этапа создания среды, еще не была назначена непосредственно пользователю, который выполняет этот этап.

**Решение**

Убедитесь в том, что администратор владельца назначил действительную лицензию Power Apps P2 непосредственно пользователю, который будет выполнять этап создания среды. Вот планы обслуживания Microsoft Dynamics, которые предоставляют это право.

| Общая единица складского хранения (SKU) продукта       | План услуг Power Apps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps для Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps для Dynamics 365 |

Обратите внимание, что различные единицы складского хранения Microsoft Office также предоставляют это право, вместе с автономными единицами складского хранения Power Apps Plan 2. Важно, что необходимо наличие одной из этих единиц складского хранения.

1. Перейдите на страницу [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Создайте среды, следуйте инструкциям в разделе [Подготовка Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).