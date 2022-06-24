---
title: Human Resources отсутствует в списке приложений Microsoft Dynamics 365
description: В этой статье объясняется, что делать, если приложение Microsoft Dynamics 365 Human Resources не указано среди приложений Microsoft Dynamics 365.
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
ms.openlocfilehash: 2d520ac06bcc0990714929c0fdd622516eda5f30
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872249"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Приложение Human Resources отсутствует в списке приложений Microsoft Dynamics 365


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Проблема**

Клиент не видит Dynamics 365 Human Resources среди приложений Microsoft Dynamics 365.

**Приказ**

Пользователь должен быть добавлен к роли "Создатель среды" для среды в Microsoft Power Apps.

1. Пользователь-администратор, имеющий лицензию Power Apps Plan 2, должен открыть [портал администратора Power Apps](https://preview.admin.powerapps.com/).

2. Выберите **Среды** и выберите правильную среду для Human Resources.

3. На вкладке **Безопасность** на вкладке **Роли среды** выберите **Создатель среды**.

    ![Вкладка ролей среды.](media/environment-roles.png)

4. На вкладке **Пользователи** добавьте пользователя или вашу организацию.

    ![Вкладка пользователей.](media/environment-maker.png)

5. Нажмите **Сохранить**.

6. Теперь пользователь должен выполнить вход в [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Выберите **Синхронизация**, чтобы обновить приложения пользователя.

    ![Кнопка "Синхронизация".](media/get-more.png)

    По завершении синхронизации Human Resources появится на домашней странице.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
