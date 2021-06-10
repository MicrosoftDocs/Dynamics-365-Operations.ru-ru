---
title: Работники без трудоустройства
description: Работники, не имеющие будущего, активного или исторического трудоустройства в вашей организацией, будут отображаться в форме сотрудники без занятости.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6fbada6feb55b8627b1aa1ddfe367177edb7a0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051721"
---
# <a name="workers-without-employment"></a>Работники без трудоустройства

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Работники, не имеющие будущего, активного или исторического трудоустройства в вашей организацией, будут отображаться в форме **Сотрудники без занятости**. Работники с этим статусом могут отображаться при импорте работников, не имеющих записи о приеме на работу, или при удалении занятости сотрудника через **Работники > История занятости**.

По умолчанию форма **Сотрудники без занятости** доступна для следующих ролей:

- Помощник Human Resources
- Менеджер Human Resources
- Агентство по найму
- Менеджер компенсаций и льгот
- Администратор зарплаты
- Менеджер зарплаты
- Менеджер по обучению

В списке **Сотрудники без занятости** можно удалить перечисленные лица. По умолчанию эта привилегия предоставляется роли помощника Human Resources. Вы можете предоставить эту привилегию другим ролям, выполнив следующие действия:

1. Выберите **Администрирование системы**, затем перейдите на вкладку **Конфигурация безопасности**.

2. На вкладке **Привилегии** отфильтруйте список **Привилегии** до **Ведение работников**.

   [![Отфильтруйте список привилегий](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. В столбце **Ссылки** выберите **Пункты меню отображения**.

4. В **Пункты меню отображения** выберите **HcmWorkersWithoutEmployment**.

   [![Выбрать форму](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. Установите разрешение **Удалить** как **Разрешить**.

6. Перейдите на вкладку **Неопубликованные объекты**.

7. Выберите **Опубликовать все**.

   [![Публикация изменений](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]