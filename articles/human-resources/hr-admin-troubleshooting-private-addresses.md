---
title: Доступ к личным адресам по роли безопасности
description: В этой теме объясняется, как решить проблему, когда клиент не может получить доступ к частным адресам.
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
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 213aada51a477257df0b079c95e74610854b5a4f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689588"
---
# <a name="access-to-private-addresses-by-security-role"></a>Доступ к личным адресам по роли безопасности


[!INCLUDE [PEAP](../includes/peap-2.md)]

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
