---
title: Что нового и что изменилось в Dynamics 365 Human Resources от 21 января 2021 г.
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 21 января 2021 года.
author: marcelbf
manager: tfehr
ms.date: 01/21/2021
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
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: af847ed36187c0d0629ce4063d9c17cb0fa8cfcf
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060850"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Что нового и что изменилось в Dynamics 365 Human Resources от 21 января 2021 г.

В этой теме описываются новые, измененные и ожидающиеся компоненты в Dynamics 365 Human Resources.

Дополнительные сведения о нашем процессе обновления и графике см. в разделе [Процесс обновления](hr-admin-setup-update-process.md).

Дополнительные сведения о новых функциях и ожидаемых датах общей доступности см. в разделе [Обзор Dynamics 365 Human Resources 2020](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>В данном выпуске

Этот выпуск включает следующие новые функции и исправления ошибок. Изменения применяются для номера сборки 8.1.3866.

### <a name="new-features"></a>Новые возможности

В этой версии следующие функции стали общедоступными.

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Platform update 10.0.16 (40) | -- | [Обновления платформы для версии 10.0.16 приложений Finance and Operations (февраль 2021 г.)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16) |
| Расширенные запросы и утверждения рабочих процессов | [Улучшения рабочих процессов управления организациями и персоналом](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Параметр конфигурации для размещения списка рабочих элементов, назначенных мне](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Обновления соответствия закону США о доступном медицинском обслуживании (ACA) для формы 1095-C, формы 1095-B и электронной отчетности с устаревшими льготами | -- | -- | 
| Управление льготами теперь поддерживает соответствие ACA для юридических лиц, расположенных в США | -- | [Создание отчетов ACA в управлении льготами](hr-benefits-management-aca-reports.md) |
| Управление льготами теперь предоставляет сущности уровней ставок льгот и уровней двойных ставок льгот  | -- | -- |

### <a name="bug-fixes"></a>Исправления ошибок

Этот выпуск содержит следующие исправления ошибок.

> [!NOTE]
> Наша цель — предоставить эту информацию вам как можно скорее. Мы может обновить этот раздел для включения исправлений ошибок, которые были сделаны в сборке после первоначальной публикации этого раздела.

| Номер проблемы | Расход |  описание |
| --- | --- | --- |
| 533079 | Ошибка навигации "Форма была вызвана неправильно" при попытке просмотра вычетов. | Исправлена ошибка при поиске вычетов льгот с представлением **На дату**. |
| 543641 | Почтовый код не заполняется в электронной отчетности.  | Устранена внутренняя ошибка, из-за которой почтовый индекс не появляется в электронных отчетах ACA для управления льготами, если код покрытия имеет значение от M до Q. |
| 542815 | Экран личного контакта в модуле самообслуживания сотрудников позволяет сотрудникам видеть личные контакты других пользователей. | Исправлена ошибка, из-за которой формат **Изменить** для личных контактов самообслуживания сотрудников не ограничивает свой запрос достаточно, чтобы гарантировать получение только одного личного контакта, позволяя пользователю использовать сочетания клавиш для просмотра контактов других пользователей. |
| 536157 | Не удается открыть страницу **Интеграция Microsoft Dataverse** в системном администрировании из-за вызова IsVirtualEntityPackageInstalled(). | Проблема предотвращает загрузку страницы **Интеграция Microsoft Dataverse** в модуле Human Resources. |
| 533079 | Ошибка навигации "Форма была вызвана неправильно" при попытке просмотра вычетов. | Исправлена ошибка, возникавшая в форме **Вычеты** для управления льготами при просмотре **На дату**. |
| 537264 | Экспресс-вкладка **Личные данные** отсутствует из записи кандидата. | Личные данные кандидата теперь доступны в записи кандидата. |
| 537267 | **Опыт работы** не отображается в записях внутренних кандидатов. | Экспресс-вкладка **Опыт работы** теперь отображается в записях внутренних кандидатов. Ранее, если кандидат был внутренним, **Опыт работы** заменялся **Журналом занятости**, который является историей занятости кандидата в рамках организации. Оба варианта применимы и должны выводиться для внутренних кандидатов. |
| 537067 | **Разрешено связываться с работодателем** не отображается. | Элемент управления **Разрешено связываться с работодателем** добавлен в область **Изменить профессиональный опыт** для записи кандидата. |
| 525957 | **Статус кандидата** не обновляется для внутренних кандидатов после завершения перехода. | После завершения перехода (кнопка **Изменить должность** или **Продолжить** выбрана на странице **Перевести работника на другую должность**) поле **Статус** в записи кандидата должно измениться на **Принят на работу**. |
| 537051 | Символы денежных единиц для индийской рупии и турецкой лиры не синхронизованы правильно с Dataverse | Символы индийской рупии и турецкой лиры теперь правильно синхронизируются с Dataverse. |
| 534846 | Для управления данными необходимо включить таблицы набора персонала. | Новые таблицы, созданные для запросов набора персонала и кандидатов, теперь включены для управления данными. Это позволяет включить отслеживание изменений для этих таблиц, обеспечивая отслеживание изменений в OData для виртуальных таблиц Dataverse. |
| 533474 | Исправлена отсутствующая ссылка на Microsoft.SqlServer.XEvent.dll. | Исключения загрузки сборки для Microsoft.SqlServer.XEvent.dll препятствовали настройке виртуальных таблиц Dataverse в некоторых средах. |
| 481122 | Рабочая область **Люди** показывала отмененные должности. | Отмененные должности отображались как открытые должности в рабочей области **Люди**. Отмененные позиции больше не отображаются. | 
| 541978 | Добавьте основной адрес электронной почты в сущность BaseWorker. | Это изменение добавило основной адрес электронной почты работника в HcmWorkerBaseEntity. |

## <a name="in-preview"></a>В режиме предварительного просмотра

В предварительной версии доступны следующие новые функции. Дополнительные сведения о включении и выключении функций см. в разделе [Управление функциями](hr-admin-manage-features.md).

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Приложение Human Resources в Microsoft Teams | [Отпуск и отгулы сотрудников в Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Приложение Human Resources в Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Управление запросами на отпуск в Teams](hr-teams-leave-app.md) |
| Интеграция с LinkedIn Talent Hub | [Интеграция с LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Интеграция с LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| Представление отпусков в нескольких компаниях для менеджеров | [Представление отпусков сотрудников в нескольких компаниях для менеджеров](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Настройка параметров отпусков и отсутствий](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Предоставление дополнительных сведений о балансе отпусков| [Предоставление дополнительных сведений о балансе отпусков](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Управление отпусками сотрудников](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Менеджеры могут отправлять запросы на подбор персонала по должностям | [Менеджеры могут отправить запрос на подбор персонала по открытым вакансиям](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Добавление запроса по набору сотрудников](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Улучшенный профиль кандидатов в управлении персоналом | [Улучшенный профиль кандидатов в управлении персоналом](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Добавление или изменение профиля кандидата](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Включение упрощенных интеграций с поставщиками по набору персонала | [Включение упрощенных интеграций с поставщиками по набору персонала](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Найм кандидатов на должность](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Скоро
| Функция | Подробности |
| --- | --- |
| Подтверждение электронной почты для регистраций льгот | Эта функция предоставит возможность отправлять подтверждающие сообщения по электронной почте сотрудникам, когда они выходят из интерфейса регистрации льгот в системе самообслуживания сотрудников. Дополнительные сведения см. в разделе [Настройка параметров управления льготами для компании](hr-benefits-setup-parameters-per-company.md). |
| Навыки, введенные руководителем для своих сотрудников, могут быть автоматически утверждены рабочим процессом | Скоро появится. |

Полный список запланированных функций и их запланированных выпусков см. в разделе [Обзор выпуска волны 2 Dynamics 365 Human Resources от 2020 года](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Обновления терминологии для Microsoft Dataverse

Начиная с ноября 2020 года Common Data Service был переименован в [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro). Дополнительные сведения см. в [официальном объявлении](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) в блоге по Power Apps. В сочетании с этим изменением имени была обновлена некоторая терминология в Dataverse. Например, вместо термина *объект* теперь используется термин *таблица*, а вместо термина *поле* — *столбец*. Дополнительные сведения см. в разделе [Обновления терминологии](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

В этом выпуске терминология, связанная в интеграцией Dynamics 365 Human Resources с Dataverse, обновлена в рамках всего приложения, чтобы отразить эти изменения. Например, форма **Интеграция Common Data Service** теперь называется **Интеграция Microsoft Dataverse**.

Дополнительные сведения об интеграции Dynamics 365 Human Resources с Microsoft Dataverse см. в разделах [Настройка интеграции Microsoft Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service) и [Настройка виртуальных таблиц Microsoft Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Human Resources](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2020, волна 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]