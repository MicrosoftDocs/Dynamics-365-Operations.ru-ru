---
title: Пользователи Attract не могут подавать заявления на вакансии на портале вакансий
description: В этой теме объясняется, как устранить проблему, когда пользователи Attract не могут подавать заявления на вакансии на портале вакансий.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462318"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Пользователи Attract не могут подавать заявления на вакансии на портале вакансий

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Расход

Пользователи Attract не могут подавать заявления на вакансии на портале вакансий. При попытке подать заявление на вакансию, которая была создана в Dynamics 365 Talent: Attract, браузер загружает страницу непрерывно и не выполняет действие.

## <a name="cause"></a>Причина

Эта проблема возникает, когда рабочая группа отношений Talent не имеет роли пользователя Talent.

## <a name="resolution"></a>Приказ

Назначьте роль пользователя Talent рабочей группе отношений Talent.

1. Выполните вход в [центр администрирования Power Platform](https://admin.powerplatform.microsoft.com) с любыми из следующих учетных данных администратора:

   - Администратор Dynamics 365
   - Глобальный администратор
   - Администратор Power Platform

2. В области переходов выберите **Среды**, затем выберите среду, в которой требуется назначить роль пользователя Talent рабочей группе отношений Talent.

   ![Выбор среды](./media/attract-troubleshoot-career-portal-select-environment.png)

3. На панели **Среда** выберите **URL-адрес среды** и выполните вход на портал администрирования среды (например, https:<orgname>.crm.dynamics.com).

4. Выберите **Параметры**, выберите **Система**, а затем выберите **Безопасность**.

   ![Переход к разделу безопасности](./media/attract-troubleshoot-career-portal-security.png)

5. Выберите **Группы**.

   ![Выберите "Группы"](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Выполните поиск **Рабочая группа отношений Talent** в поле поиска, затем выберите рабочую группу из результатов поиска.

7. Выберите **УПРАВЛЕНИЕ РОЛЯМИ** на ленте.

8. В диалоговом окне **Управление ролями рабочей группы** выберите **Пользователь Talent** из списка доступных ролей, затем выберите **ОК**, чтобы применить роль.

   ![Применение роли](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Проверьте свои изменения:

   1. Войдите на портал вакансий из нового окна браузера.
   2. Подайте заявление на вакансию на портале вакансий. 