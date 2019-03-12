---
title: Что нового и что изменилось в Dynamics 365 for Talent Core HR (11 января 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6e7edf52db663c7ad28f316c324d68e57bf6699a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "305973"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a>Что нового и что изменилось в Dynamics 365 for Talent Core HR (11 января 2019 г.)

[!include [banner](includes/banner.md)]

**Сборка 8.1.2100**

В этой теме описываются новые и измененные компоненты Core HR.

## <a name="changes"></a>Изменения

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Проверка запросов на отпуск путем прогнозирования доступного сальдо
Изменения, внесенные в данном выпуске, позволяют сотрудникам запрашивать отпуск в будущем времени без вычитания из их текущего сальдо. Стандартные workflow-процессы будут использоваться для любых будущих запросов. Дополнительные сведения см. в разделе [Начисление времени отпуска на основе отработанных часов](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>Просмотр прогнозируемого сальдо отпуска в системе дистанционной регистрации рабочего времени и области "Люди"
Эта функция позволяет просматривать сальдо для отпуска будущих периодов сотрудниками отдела кадров, руководителями и сотрудниками. Сотрудники могли посмотреть будущие сальдо в рабочей области **Дистанционная регистрация рабочего времени**, а отделу кадров эта же информация доступна в рабочей области **Люди**.

### <a name="notifications-for-changing-leave-balances"></a>Уведомления об изменении сальдо отпуска
Сальдо отпуска будут отображать текущее сальдо сотрудников. Будущие сальдо можно найти в рабочих областях **Дистанционная регистрация рабочего времени** и **Люди**, введя "на дату" для расчета прогнозируемого сальдо.

Навигация была добавлена для просмотра прогнозируемых сальдо в следующих областях:
  - Карточка **Отгул** в рабочей области **Дистанционная регистрация рабочего времени**.
  - Карточка **Отпуск и отсутствие** в рабочей области **Портал самообслуживания менеджеров**.
  - Страница **Отпуск и отсутствие** в рабочей области **Люди**.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Разрешить десятичные знаки для планов переменной компенсации (планы денежных средств)
Переменное денежное вознаграждение и планы теперь содержат дополнительную гибкость для сумм и переопределения значений с десятичными суммами.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>Не удается изменить даты регистраций переменной компенсации после сохранения плана
Это изменение позволяет обновить дату окончания плана (продленный или с истекшим сроком действия) после сохранения плана. Вы может по-прежнему активировать или отключить планы независимо от даты начала и окончания.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Информации о заработной плате доступна при назначении роли безопасности администратора заработной платы
Роль администратора заработной платы была обновлена для доступа к информации о заработной плате во время процесса запроса.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Детализация иерархии портала самообслуживания сотрудников | штатных единиц из плитки не получает родительский узел
Чтобы устранить ошибки, возникшие при добавлении иерархии должностей в новые рабочие области и навигации в организационной структуре организации, были внесены изменения.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Новое сообщение проверки, когда номерная серия персонала уже используется
Изменение было сделано для уточнения того, что проблема возникает, когда при приеме сотрудника на работу и следующий номер персонала используется.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Рабочая область дистанционного обслуживания сотрудников выбрана в качестве исходной начальной страницы
Когда рабочая область **Самообслуживание сотрудников** выбрана как страница начальной загрузки для пользователя, и пользователю не назначена роль сотрудника, система будет перенаправлять на панель мониторинга по умолчанию.

### <a name="termination-reason-code-updates-position-assignment-record"></a>Код причины увольнения обновляет запись назначения для должность
Код причины увольнения теперь обновляет назначение на должность при увольнении сотрудника и прекращении должности. 