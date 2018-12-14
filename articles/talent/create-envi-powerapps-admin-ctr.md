---
title: "Не удается создать среду в центре администрирования PowerApps"
description: "В этом разделе объясняется, что делать, если администратор не может создать среду в центре администрирования Microsoft PowerApps."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: ru-ru
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>Не удается создать среду в центре администрирования PowerApps

[!include [banner](includes/banner.md)]

**Расход**

- Администратор владельца/среды не может создать среду в центре администрирования Microsoft PowerApps.
- Лицензия, дающая пользователям право на выполнение этапа создания среды, еще не была назначена непосредственно пользователю, который выполняет этот этап.

**Решение**

Убедитесь в том, что администратор владельца назначил действительную лицензию PowerApps P2 непосредственно пользователю, который будет выполнять этап создания среды. Вот планы обслуживания Microsoft Dynamics, которые предоставляют это право.

| Общая единица складского хранения (SKU) продукта       | План обслуживания PowerApps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps для Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | PowerApps для Dynamics 365 |

Обратите внимание, что различные единицы складского хранения Microsoft Office также предоставляют это право, вместе с автономными единицами складского хранения PowerApps Plan 2. Важно, что необходимо наличие одной из этих единиц складского хранения.

1. Перейдите на страницу [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Создайте среды, следуйте инструкциям в разделе [Подготовка Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).
