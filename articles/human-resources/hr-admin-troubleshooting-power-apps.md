---
title: Невозможно создать среду в центре администрирования Power Apps
description: В этой статье объясняется, что делать, если администратор не может создать среду в центре администрирования Microsoft Power Apps.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc62d3c8fe560d4f7d2e754a79de6fec3ef6041b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882934"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Невозможно создать среду в центре администрирования Power Apps


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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
2. Создайте среды, следуйте инструкциям в разделе [Подготовка Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
