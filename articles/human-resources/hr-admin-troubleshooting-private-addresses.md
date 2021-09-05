---
title: Доступ к личным адресам по роли безопасности
description: В этой теме объясняется, как решить проблему, когда клиент не может получить доступ к частным адресам.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0b96733946e4ef79de244730d0c442b9900426c1
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413347"
---
# <a name="access-to-private-addresses-by-security-role"></a>Доступ к личным адресам по роли безопасности

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Расход**

После того как клиент продублировал роль безопасности и выполнил вход с новой ролью, клиент не может увидеть адреса, которые были помечены как частные.

**Разрешение**

Для решения проблемы клиент должен выполнить следующие действия для дублированной роли безопасности.

1. Перейдите в раздел **Управление организацией \> Глобальная адресная книга \> Параметры глобальной адресной книги**.
2. На вкладке **Безопасность частного местоположения** переместить новую роль безопасности из списка **Доступные роли** в список **Выбранные роли**.
3. Нажмите **Сохранить**.

![Страница параметров глобальной адресной книги.](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
