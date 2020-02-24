---
title: Human Resources отсутствует в списке приложений Microsoft Dynamics 365
description: В этой статье объясняется, что делать, если клиент не видит приложение Microsoft Dynamics 365 Human Resources среди приложений Microsoft Dynamics 365.
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
ms.openlocfilehash: d39e6ef4168f08f20b92979a296ed088744ad0da
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010408"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources отсутствует в списке приложений Microsoft Dynamics 365

**Выдать**

Клиент не видит Dynamics 365 Human Resources среди приложений Microsoft Dynamics 365.

**Приказ**

Пользователь должен быть добавлен к роли "Создатель среды" для среды в Microsoft Power Apps.

1. Пользователь-администратор, имеющий лицензию Power Apps Plan 2, должен открыть [портал администратора Power Apps](https://preview.admin.powerapps.com/).

2. Выберите **Среды**и выберите правильную среду для Human Resources.

3. На вкладке **Безопасность** на вкладке **Роли среды** выберите **Создатель среды**.

    ![Вкладка ролей среды](media/environment-roles.png)

4. На вкладке **Пользователи** добавьте пользователя или вашу организацию.

    ![Вкладка пользователей](media/environment-maker.png)

5. Нажмите **Сохранить**.

6. Теперь пользователь должен выполнить вход в [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Выберите **Синхронизация**, чтобы обновить приложения пользователя.

    ![Кнопка "Синхронизация"](media/get-more.png)

    По завершении синхронизации Human Resources появится на домашней странице.
