---
title: Что нового и что изменилось в Dynamics 365 Human Resources 22 октября 2020 г.
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 22 октября 2020 года.
author: jcart1106
manager: tfehr
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 41b4e92720c6a9f830d940900c3c6e5b0a173de0
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130839"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Что нового и что изменилось в Dynamics 365 Human Resources 22 октября 2020 г.

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме описываются новые, измененные и ожидающиеся компоненты в Dynamics 365 Human Resources. Дополнительные сведения о нашем процессе обновления и графике см. в разделе [Процесс обновления](hr-admin-setup-update-process.md).

Дополнительные сведения о новых функциях и ожидаемых датах общей доступности см. в разделе [Обзор Dynamics 365 Human Resources 2020](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>В данном выпуске

Этот выпуск включает следующие новые функции и исправления ошибок. Изменения применяются для номера сборки 8.1.3680.

### <a name="new-features"></a>Новые возможности

В этой версии следующие функции стали общедоступными.

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Platform update 10.0.14 (38) | -- | [Обновления платформы для версии 10.0.14 приложений Finance and Operations (ноябрь 2020 г.)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14) |
| Улучшения рабочих процессов управления организациями и персоналом | [Улучшения рабочих процессов управления организациями и персоналом](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Параметр конфигурации для размещения списка рабочих элементов, назначенных мне](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Исправления ошибок

Этот выпуск содержит следующие исправления ошибок.

> [!NOTE]
> Наша цель — предоставить эту информацию вам как можно скорее. Мы может обновить этот раздел для включения исправлений ошибок, которые были сделаны в сборке после первоначальной публикации этого раздела.

| Номер проблемы| Расход  | описание|
| --- | --- | --- |
| 437922 | Импорт часов FMLA с использованием сущности DMF приводит к ошибке "только для чтения". | Сбой использования сущности часов FMLA для импорта часов, связанных с обращением FMLA. Мы добавили логику, чтобы убедиться, что импортируемые часы не превысят количество оставшихся часов для обращения. |
| 512019 | Неверная сумма **Последний перенос**. | На странице **Отгул** при изменении поля **Состояние на дату** на первый день следующего финансового периода отображалась неправильная сумма **Перенос** для типа **Ежегодный отпуск**. Теперь отображается правильная сумма. |
| 458639 | Сущность **Контакты сотрудника** не поддерживает режим отслеживания изменений. | Мы обновили сущность **Контакты работника**, чтобы можно было использовать его в сценариях собственных баз данных (BYOD).|
| 505347 | Руководители обучения могут представить запрос на отпуск для сотрудника, когда активирована функция оптимизации работы сотрудника. | Роли, отличные от сотрудника отдела кадров и менеджера отдела кадров, не имеют разрешения отправлять запросы отгулов для сотрудников. |
| 513490 | Ведение журнала управления льготами: добавление ведения журнала для планов без параметров покрытия. | Мы включили результаты ведения журналов для **плана без параметров покрытия**. Они теперь будут отображены в таблице **Результаты процесса** и будут правильно отсортированы в верхней части. |
| 517021 | Невозможно выбрать несколько планов с одним и тем же кодом **Тип плана**, если **Тип плана** имеет одну регистрацию на тип. | Мы изменили ограничения для выбора планов, в которых разрешена только одна регистрация. Ограничения в настоящее время находятся на уровне **Код типа плана**, а не на уровне **Тип плана**. Это изменение позволяет планам, таким как HSA и FSA, имеющим один и тот же тип, но им можно присвоить отдельный **Код типа плана**. Таким образом, можно выбрать оба параметра для одного и того же периода регистрации. |
| 444791 | Невозможно просмотреть компенсацию в самообслуживании сотрудников, когда **Ограничение доступа** включено в плане компенсации. | На карточке **Компенсация** самообслуживания сотрудников текущая сумма компенсаций и процент увеличения отображаются как "0", если сотрудник был зарегистрирован в плане с включенным **Ограничением доступа** и назначен определенным ролям. Мы решили эту проблему, чтобы сотрудник и менеджер всегда могли видеть сведения о компенсациях самих себя и своих непосредственных подчиненных. |
| 457542 | Обновление сведений курса после закрытия курса также не обновляет эту же информацию для сотрудника, который прошел курс. | Теперь сведения о сотруднике обновляются правильно при изменении сведений о курсе после закрытия и повторного открытия курса. |
| 515342 | Невозможно вставить данные через **CDSLeaveRequestDetailEntity**. Компания не найдена или не существует. | Теперь можно использовать **CDSLeaveRequestDetailEntity** для вставки данных. |
| 514743 | Ошибка в форме **Параметры электронной почты** при использовании Microsoft Exchange. | Сообщение "Не удается загрузить файлы или сборку..." отображается на странице **Параметры электронной почты**, когда поставщик электронной почты был настроен на **Exchange**. Кроме того, это исправление позволяет странице **Параметры электронной почты** загружаться и сохраняться должным образом. |


## <a name="in-preview"></a>В режиме предварительного просмотра

В предварительной версии доступны следующие новые функции. Дополнительные сведения о включении и выключении функций см. в разделе [Управление функциями](hr-admin-manage-features.md).

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Приложение Human Resources в Microsoft Teams | [Отпуск и отгулы сотрудников в Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Приложение Human Resources в Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Управление запросами на отпуск в Teams](hr-teams-leave-app.md) |
| Расширенные запросы и утверждения рабочих процессов | [Улучшения рабочих процессов управления организациями и персоналом](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Параметр конфигурации для размещения списка рабочих элементов, назначенных мне](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Виртуальные сущности в Dataverse для Human Resources | [Развертывание основных данных Dynamics 365 Human Resources в Dataverse](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Настройка виртуальных сущностей Dataverse](hr-admin-integration-common-data-service-virtual-entities.md) |
| Интеграция с LinkedIn Talent Hub | [Интеграция с LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Интеграция с LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| Пользовательские ссылки на портале самообслуживания менеджеров | [Пользовательские ссылки на портале самообслуживания менеджеров](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Пользовательские ссылки на портале самообслуживания менеджеров](https://aka.ms/MSSCustomLinks) |

## <a name="coming-soon"></a>Скоро

Полный список запланированных функций и их запланированных выпусков см. в разделе [Обзор выпуска волны 2 Dynamics 365 Human Resources от 2020 года](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>См. также

[Что нового и что изменилось в Human Resources](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2020, волна 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]