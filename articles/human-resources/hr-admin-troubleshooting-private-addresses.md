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
ms.openlocfilehash: 05895d58cfd108c45c3c75921cb6930b904a6482
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068392"
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
