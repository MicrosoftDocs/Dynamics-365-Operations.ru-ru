---
title: Talent отсутствует среди приложений Microsoft Dynamics 365 (Common Data Service 1.0)
description: В этом разделе объясняется, что делать, если клиент не видит приложение Microsoft Dynamics 365 for Talent среди приложений Microsoft Dynamics 365.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ad5add2b572ccb6bff175806b965f63b53986152
ms.sourcegitcommit: 45b79d1e587e03f5cde2766cdec4eaa7a2a897a3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2019
ms.locfileid: "949790"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent отсутствует среди приложений Microsoft Dynamics 365 (Common Data Service 1.0)

[!include [banner](includes/banner.md)]

**Выдать**

Клиент не видит приложения Microsoft Dynamics 365 for Talent среди приложений Microsoft Dynamics 365.

**Разрешение**

Пользователь должен быть добавлен к роли "Создатель среды" для среды в Microsoft PowerApps.

1. Пользователь-администратор, имеющий лицензию PowerApps Plan 2, должен открыть [портал администратора PowerApps](https://preview.admin.powerapps.com/).
2. Выберите **Среды**и выберите правильную среду для Talent.
3. На вкладке **Безопасность** на вкладке **Роли среды** выберите **Создатель среды**.

    ![Вкладка ролей среды](media/environment-roles.png)

4. На вкладке **Пользователи** добавьте пользователя или вашу организацию.

    ![Вкладка пользователей](media/environment-maker.png)

5. Нажмите **Сохранить**.
6. Теперь пользователь должен выполнить вход в [Microsoft Dynamics 365](https://home.dynamics.com/).
7. Выберите **Синхронизация**, чтобы обновить приложения пользователя.

    ![Кнопка "Синхронизация"](media/get-more.png)

    По завершении синхронизации Talent появится на домашней странице.
