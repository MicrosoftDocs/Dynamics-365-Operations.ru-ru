---
title: Доступ к личным адресам по роли безопасности
description: В этой статье объясняется, как решить проблему, когда клиент не может получить доступ к частным адресам.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2018
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
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 49f9f50b774df8e215c084bbb493a6be9de6b234
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463944"
---
# <a name="access-to-private-addresses-by-security-role"></a>Доступ к частным адресам по роли безопасности

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Расход**

После того как клиент продублировал роль безопасности и выполнил вход с новой ролью, клиент не может увидеть адреса, которые были помечены как частные.

**Разрешение**

Для решения проблемы клиент должен выполнить следующие действия для дублированной роли безопасности.

1. Перейдите в раздел **Управление организацией \> Глобальная адресная книга \> Параметры глобальной адресной книги**.
2. На вкладке **Безопасность частного местоположения** переместить новую роль безопасности из списка **Доступные роли** в список **Выбранные роли**.
3. Выберите **Сохранить**.

![Страница параметров глобальной адресной книги](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]