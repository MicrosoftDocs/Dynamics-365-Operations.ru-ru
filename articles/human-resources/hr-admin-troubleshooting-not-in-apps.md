---
title: Human Resources отсутствует в списке приложений Microsoft Dynamics 365
description: В этой статье объясняется, что делать, если клиент не видит приложение Microsoft Dynamics 365 Human Resources среди приложений Microsoft Dynamics 365.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 658c6a4f17c022c3d0e3e49d16eb89624c4be27c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803977"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources отсутствует в списке приложений Microsoft Dynamics 365

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Выдать**

Клиент не видит Dynamics 365 Human Resources среди приложений Microsoft Dynamics 365.

**Приказ**

Пользователь должен быть добавлен к роли "Создатель среды" для среды в Microsoft Power Apps.

1. Пользователь-администратор, имеющий лицензию Power Apps Plan 2, должен открыть [портал администратора Power Apps](https://preview.admin.powerapps.com/).

2. Выберите **Среды** и выберите правильную среду для Human Resources.

3. На вкладке **Безопасность** на вкладке **Роли среды** выберите **Создатель среды**.

    ![Вкладка ролей среды](media/environment-roles.png)

4. На вкладке **Пользователи** добавьте пользователя или вашу организацию.

    ![Вкладка пользователей](media/environment-maker.png)

5. Нажмите **Сохранить**.

6. Теперь пользователь должен выполнить вход в [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Выберите **Синхронизация**, чтобы обновить приложения пользователя.

    ![Кнопка "Синхронизация"](media/get-more.png)

    По завершении синхронизации Human Resources появится на домашней странице.


[!INCLUDE[footer-include](../includes/footer-banner.md)]