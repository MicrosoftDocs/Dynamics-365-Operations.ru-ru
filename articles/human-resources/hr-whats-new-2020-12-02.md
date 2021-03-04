---
title: Что нового и что изменилось в Dynamics 365 Human Resources от 2 декабря 2020 г.
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 2 декабря 2020 года.
author: marcelbf
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aba35563266d1149131124f489f89da61432bfb2
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669186"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Что нового и что изменилось в Dynamics 365 Human Resources от 2 декабря 2020 г.

В этой теме описываются новые, измененные и ожидающиеся компоненты в Dynamics 365 Human Resources.

Дополнительные сведения о нашем процессе обновления и графике см. в разделе [Процесс обновления](hr-admin-setup-update-process.md).

Дополнительные сведения о новых функциях и ожидаемых датах общей доступности см. в разделе [Обзор Dynamics 365 Human Resources 2020](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>В данном выпуске

Этот выпуск включает следующие новые функции и исправления ошибок. Изменения применяются для номера сборки 8.1.3788.

### <a name="new-features"></a>Новые возможности

В этой версии следующие функции стали общедоступными.

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Менеджеры могут отправлять запросы на подбор персонала по должностям | [Менеджеры могут отправить запрос на подбор персонала по открытым вакансиям](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Добавление запроса по набору сотрудников](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Улучшенный профиль кандидатов в управлении персоналом | [Улучшенный профиль кандидатов в управлении персоналом](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Добавление или изменение профиля кандидата](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Включение упрощенных интеграций с поставщиками по набору персонала | [Включение упрощенных интеграций с поставщиками по набору персонала](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Найм кандидатов на работу](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |
| Пользовательские ссылки на портале самообслуживания менеджеров | [Пользовательские ссылки на портале самообслуживания менеджеров](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Пользовательские ссылки на портале самообслуживания менеджеров](https://aka.ms/MSSCustomLinks) |


### <a name="bug-fixes"></a>Исправления ошибок

Этот выпуск содержит следующие исправления ошибок.

> [!NOTE]
> Наша цель — предоставить эту информацию вам как можно скорее. Мы может обновить этот раздел для включения исправлений ошибок, которые были сделаны в сборке после первоначальной публикации этого раздела.

| Номер проблемы | Расход | описание |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult должны включать дату и время, которые использовались при обработке. | Результат обработки BenefitEligibity теперь включает отметку даты и времени для последней обработки, которая отсутствовала ранее. |
| 526903 | Регистрация льготы не выполняется для планов с иждивенцами, если параметр **Автоматически выбирать кандидатов** включен в **общих параметрах Human Resources**. | Исправлена проблема, в которой не производилась регистрация льгот для иждивенцев, когда параметр **Автоматически выбирать кандидатов** был включен для кандидатов по умолчанию. |
| 521922 | Параметр **Показывать отсутствия без подробных сведений** показывает запросы отсутствия в календаре отсутствия для рабочей группы. | Тип отпуска, цвет типа отпуска и сведения о дне недели отображаются в календаре отсутствия рабочей группы, когда для параметра **Показывать отсутствие без подробных сведений** задано значение **Да** в пункте **Параметры отпусков и отсутствия**. Эта проблема была исправлена, и теперь не отображается тип отпуска, и цвет отпуска по умолчанию (темно-синий) используется для всех типов отпусков в календаре отсутствия рабочей группы. |
| 527316 | Изменения заголовков для уведомлений работы, должности и работника не синхронизируются. | Связь заголовка была добавлена ранее в сущности работы, должности и работника. Синхронизация для этой связи выполняется для синхронизации из Human Resources в Common Data Service, но не работает для уведомлений из Common Data Service. Это было решено. |
| 512275 | Удалите параметры цвета из пункта **Параметры отпусков и отсутствия**. | Теперь, когда для типа отпуска определены цвета, параметры цветов больше не нужны в пункте **Параметры отпусков и отсутствия**, поэтому они были удалены. |
| 437112 | Вводящий в заблуждение текст сообщения об ошибке при назначении должности сотрудника. | Обновлено сообщение об ошибке, когда при найме сотрудника производится попытка назначить сотрудника для неактивной должности. Обновленное сообщение: **Указанная должность не активна по состоянию на дату начала занятости. Проверьте продолжительность данной должности.** |
| 527816 | Проблемы производительности на странице **Отгул**. | Улучшена производительность на странице **Отгул**. |
| 523158 | BenefitPeriodMigrationUpgrade и BenefitPlanMigrationUpgrade не выполняются. | Исправлены проблемы, связанные с неправильным выполнением заданий миграции льгот, связанных с параметрами **Период** и **План**. |

## <a name="in-preview"></a>В режиме предварительного просмотра

В предварительной версии доступны следующие новые функции. Дополнительные сведения о включении и выключении функций см. в разделе [Управление функциями](hr-admin-manage-features.md).

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Приложение Human Resources в Microsoft Teams | [Отпуск и отгулы сотрудников в Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Приложение Human Resources в Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Управление запросами на отпуск в Teams](hr-teams-leave-app.md) |
| Расширенные запросы и утверждения рабочих процессов | [Улучшения рабочих процессов управления организациями и персоналом](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Параметр конфигурации для размещения списка рабочих элементов, назначенных мне](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Интеграция с LinkedIn Talent Hub | [Интеграция с LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Интеграция с LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
|Представление отпусков в нескольких компаниях для менеджеров | [Представление отпусков сотрудников в нескольких компаниях для менеджеров](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Настройка параметров отпусков и отсутствий](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Предоставление дополнительных сведений о балансе отпусков| [Предоставление дополнительных сведений о балансе отпусков](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Управление отпусками сотрудников](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Менеджеры могут отправлять запросы на подбор персонала по должностям | [Менеджеры могут отправить запрос на подбор персонала по открытым вакансиям](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Добавление запроса по набору сотрудников](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Улучшенный профиль кандидатов в управлении персоналом | [Улучшенный профиль кандидатов в управлении персоналом](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Добавление или изменение профиля кандидата](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Включение упрощенных интеграций с поставщиками по набору персонала | [Включение упрощенных интеграций с поставщиками по набору персонала](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Найм кандидатов на работу](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Скоро

Полный список запланированных функций и их запланированных выпусков см. в разделе [Обзор выпуска волны 2 Dynamics 365 Human Resources от 2020 года](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Human Resources](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2020, волна 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]