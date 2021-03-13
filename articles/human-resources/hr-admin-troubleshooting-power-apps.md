---
title: Невозможно создать среду в центре администрирования Power Apps
description: В этой статье объясняется, что делать, если администратор не может создать среду в центре администрирования Microsoft Power Apps.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114001"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Невозможно создать среду в центре администрирования Power Apps

**Выдать**

- Администратор владельца/среды не может создать среду в центре администрирования Microsoft Power Apps.
- У пользователя нет лицензии, которая содержит право на создание сред.

**Решение**

Убедитесь, что администратор клиента назначил действительную лицензию Power Apps P2 для пользователя, создающего среду. В следующих планах обслуживания Microsoft Dynamics имеются разрешения на создание сред:

| Общая единица складского хранения (SKU) продукта       | План услуг Power Apps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps для Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps для Dynamics 365 |

Обратите внимание, что различные единицы складского хранения Microsoft Office также предоставляют это право, вместе с автономными единицами складского хранения Power Apps Plan 2. Важно, что необходимо наличие одной из этих единиц складского хранения.

1. Перейдите на страницу [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Создайте среды, следуйте инструкциям в разделе [Подготовка Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
