---
title: Что нового и что изменилось в Dynamics 365 Human Resources (03 сентября 2020 г.)
description: В этой статье описываются новые или измененные функции в Microsoft Dynamics 365 Human Resources от 3 сентября 2020 года.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d558f4b0ddb3e8fe3479567483e2c2349a40774
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891360"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Что нового и что изменилось в Dynamics 365 Human Resources (3 сентября 2020 г.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources. Изменения применяются для номера сборки 8.1.3504. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Lifecycle Services (LCS) для справки.

Дополнительные сведения о предстоящих функциях в модуле Human Resources см. в разделе [Обзор Dynamics 365 Human Resources волны 2 выпуска 2019 года](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Дополнительные сведения о процессе обновления для модуля Human Resources см. в разделе [Процесс обновления](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>В данном выпуске

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Новая сетка финансовых аналитик по умолчанию и шаблон диалогов Human Resources (469495)

Новый шаблон для финансовых аналитик будет доступен в следующих областях:

- Действия должностей (форма: **HcmPositionActionDetail**)
- Код дохода в зарплате (форма: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>Записи не отображаются в календаре отпусков компании, если не включены усовершенствования календаря отпусков и отсутствия (484406)

В этой версии исправлена проблема, в которой не отображаются записи в календаре отпусков компании. Эта проблема возникает только в том случае, если параметр управления функциями **Улучшения календаря отпусков и отсутствия** не включен.

### <a name="benefitplanemployeeentity-issue-467597"></a>Проблема BenefitPlanEmployeeEntity (467597)

В этом выпуске исправлена проблема с сущностью **BenefitsPlanEmployee**. При импорте регистраций работников **Код покрытия** и **Код типа плана** теперь устанавливаются правильно. Эта проблема приводит к неправильному отображению планов льгот сотрудников в формах **План льгот работников** и **Открытие регистрации** в службе самообслуживания сотрудников.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>Выходные данные электронного файла 1094-C отсутствует буква в XML (435190)

Это изменение исправляет проблему, связанную с отсутствием в выходном файле 1094-C символа, необходимого при отправке в IRS.

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Таблица переменных компенсаций сотрудников, сопоставленных с формой фиксированной компенсации (476117)

Это изменение выравнивает поля фиксированной компенсации с формой фиксированной компенсации. Поля переменной компенсации теперь становятся доступными только с помощью формы переменной компенсации.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>Запросы на отпуск разрешены до регистрации, если этот тип отпуска имеет отрицательный минимальный баланс (469917)

Это изменение запрещает ввод запросов на отпуск до регистрации в плане, даже если для регистрации указано отрицательное минимальное сальдо. Вводить или отправлять запросы можно только тогда, когда план активен.

### <a name="document-templates-dont-download-457279"></a>Шаблоны документов не загружаются (457279)

Теперь это изменение позволяет загрузить все шаблоны документов. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Данные отображаются в виде заголовков столбцов вместо строк в поле ставки оплаты в отчете плана компенсаций (476077)

В отчете аналитики отображаются правильные сведения для поля **Ставка оплаты**.

## <a name="in-preview"></a>В режиме предварительного просмотра

### <a name="human-resources-application-in-teams"></a>Приложение Human Resources в Teams

Сотрудники могут просматривать и запрашивать время отсутствия на работе в Microsoft Teams. Они могут взаимодействовать с ботом для создания запросов на отпуск. Дополнительные сведения см.

- [Отпуск сотрудника и опыт отсутствия в Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) в плане выпуска Dynamics 365 волны 1 за 2020 год
- [Приложение Human Resources в Teams](./hr-admin-teams-leave-app.md) в документации Human Resources

### <a name="human-resources-app-in-teams-preview-features"></a>Предварительные версии функций приложения Human Resources в Teams
 
-  **Уведомления**: отправители и утверждающие запросы отпусков получают уведомления в приложении Human Resources в Teams. Утверждающие смогут утверждать или отклонять запросы на отсутствие. Отправители получат уведомление, если запрос был утвержден или отклонен. Дополнительные сведения см.
   - [Отпуск сотрудника и опыт отсутствия в Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) в плане выпуска Dynamics 365 волны 2 за 2020 год
   - [Включение уведомлений для приложения Human Resources в Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) в документации Human Resources
   - [Включение или выключение уведомлений Teams для отдельных пользователей](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) в документации Human Resources
   - [Уведомления Teams](./hr-teams-leave-app.md#respond-to-teams-notifications) в документации Human Resources
   - [Просмотр календаря отпусков вашей рабочей группы](./hr-teams-leave-app.md#view-your-teams-leave-calendar) в документации Human Resources
 
- **Календарь отпусков руководителя**: руководители смогут просматривать утвержденные и ожидающие отпуска для их непосредственных подчиненных в представлении календаря. Это представление упрощает понимание того, когда члены рабочей группы не находятся на рабочем месте. Дополнительные сведения см.
   - [Отпуск сотрудника и опыт отсутствия в Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) в плане выпуска Dynamics 365 волны 2 за 2020 год
   - [Просмотр календаря отпусков вашей рабочей группы](./hr-teams-leave-app.md#view-your-teams-leave-calendar) в документации Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Параметр конфигурации для размещения списка рабочих элементов, назначенных мне (477004)

Новый параметр теперь становится доступным для позиционирования списка **Рабочие элементы, назначенные мне** в правом столбце панели мониторинга. При таком изменении все рабочие элементы и списки дел отображаются в одной области. Активируйте эту функцию, включив **Предварительная версия — улучшения рабочего процесса** в управлении функциями. Дополнительные сведения о включении предварительных версий функций см. в разделе [Управление функциями](hr-admin-manage-features.md).

Эта функция также поддерживает параметры рабочего процесса, которые отображаются в формах действий персонала. Параметры рабочего процесса также появляются над экспресс-вкладкой действий для быстрого доступа. Дополнительные сведения см. 

- [Улучшения рабочего процесса управления предприятием и персоналом](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) в плане волны 2 выпуска 2020 года Dynamics 365

![Рабочие элементы, назначенные мне.](./media/hr-workflow-work-items-assigned-to-me.png)

![Быстрый доступ к элементам рабочего процесса.](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Скоро

### <a name="checklist-entities-included-in-dataverse"></a>Сущности контрольного списка, включенные в Dataverse

Сущности контрольного списка для адаптации, увольнения, переходов и бизнес-процессов в скором времени будут доступны в Dataverse.

### <a name="benefits-management-reason-codes"></a>Коды причин управления льготами

Коды причин управления льготами скоро будут объединены с существующими кодами причин в Human Resources. Если созданные коды причин в модуле управления льготами имеют более 15 символов, необходимо изменить имя кода причины в форме **Коды причин** управления льготами, чтобы оно состояло не более чем из 15 символов. После обновления имени код причины появится под существующим кодом причины в управлении персоналом. Это изменение будет доступно в будущем и не повлияет на существующие функции.

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Human Resources](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2019, волна 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
