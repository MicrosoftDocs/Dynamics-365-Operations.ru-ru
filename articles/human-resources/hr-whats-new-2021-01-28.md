---
title: Что нового и что изменилось в Dynamics 365 Human Resources от 28 января 2021 г.
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 28 января 2021 года.
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 47a15cbab388d98359828561acefb7c110e8d1da3ec489df21ee0496aa3a0730
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772600"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Что нового и что изменилось в Dynamics 365 Human Resources от 28 января 2021 г.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описываются новые, измененные и ожидающиеся компоненты в Dynamics 365 Human Resources.

Дополнительные сведения о нашем процессе обновления и графике см. в разделе [Процесс обновления](hr-admin-setup-update-process.md).

Дополнительные сведения о новых функциях и ожидаемых датах общей доступности см. в разделе [Обзор Dynamics 365 Human Resources 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>В данном выпуске

Этот выпуск включает следующие новые функции и исправления ошибок. Изменения применяются для номера сборки 8.1.3906.

### <a name="new-features"></a>Новые возможности

В этой версии следующие функции стали общедоступными.

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Интеграция кодов причин льгот в рабочую область **Управления персоналом** | -- | [Настройка кодов причин](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Исправления ошибок

Этот выпуск содержит следующие исправления ошибок.

> [!NOTE]
> Наша цель — предоставить эту информацию вам как можно скорее. Мы может обновить этот раздел для включения исправлений ошибок, которые были сделаны в сборке после первоначальной публикации этого раздела.


| Номер проблемы | Расход |  описание |
| --- | --- | --- |
| 539456 | В календаре отображается тип отпуска в тексте, который выводится при наведении указателя мыши, если включен параметр **Показывать только отсутствия без подробных сведений**. | Если параметр **Показывать только отсутствия без подробных сведений** включен, дата запроса будет отображаться при наведении указателя мыши. |
| 528907 | Предоставление доступа к юридическому лицу по роли сотрудника приводит к тому, что руководители не смогут увидеть действия баланса отпусков для сотрудников в области **Моя рабочая группа** самообслуживания сотрудников. |Установка этого параметра теперь позволяет менеджерам продолжать видеть действие сальдо отпусков. |
| 526280 | Ошибка разрешений для HcmWorkerEntity, HcmEmployeeEntity и HcmContractorEntity. | Пользователям несистемной роли администратора не удавалось экспортировать перечисленные сущности из-за ошибки разрешений в поле NationalityCountryRegion. Пользователям будет по-прежнему необходимо иметь следующие права для экспорта этой информации: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain и HCMContractorEntityView. |
| 542147 | Поля **Номер банковского счета** и **Код банка** являются обязательными при добавлении банковского счета с помощью самообслуживания сотрудников. | Была исправлена ошибка, из-за которой сотрудникам при добавлении сведений о банковском счете необходимо было ввести **Номер банковского счета** и **Код банка**. Эти поля больше не являются обязательными при сохранении новой информации о банковском счете. |
| 543641 | Почтовый код не заполняется в электронной отчетности. | Исправлена ошибка, в которой почтовый индекс не заполняется в отчете ACA для кодов покрытия от L до Q. |
| 545402 | Добавьте изменение маршрутизации для файла UserBranding.js, чтобы удалить ошибки 404. | Пользователь больше не должен видеть ошибки 404 в консоли. |

## <a name="in-preview"></a>В режиме предварительного просмотра   

В предварительной версии доступны следующие новые функции. Дополнительные сведения о включении и выключении функций см. в разделе [Управление функциями](hr-admin-manage-features.md).

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Приложение Human Resources в Microsoft Teams | [Отпуск и отгулы сотрудников в Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Приложение Human Resources в Teams](./hr-admin-teams-leave-app.md)<br>[Управление запросами на отпуск в Teams](hr-teams-leave-app.md) |
| Представление отпусков в нескольких компаниях для менеджеров | [Представление отпусков сотрудников в нескольких компаниях для менеджеров](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Настройка параметров отпусков и отсутствий](./hr-leave-and-absence-parameters.md) |

## <a name="coming-soon"></a>Скоро

| Функция | Подробности |
| --- | --- |
| Подтверждение электронной почты для регистраций льгот | Эта функция предоставит возможность отправлять подтверждающие сообщения по электронной почте сотрудникам, когда они выходят из интерфейса регистрации льгот в системе самообслуживания сотрудников. Эта функция будет доступна 1 февраля. Дополнительные сведения см. в разделе [Настройка параметров управления льготами для компании](hr-benefits-setup-parameters-per-company.md). |
| Навыки, введенные руководителем для своих сотрудников, могут быть автоматически утверждены рабочим процессом | Скоро появится. |

Полный список запланированных функций и их запланированных выпусков см. в разделе [Обзор выпуска волны 1 Dynamics 365 Human Resources от 2021 года](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Обновления терминологии для Microsoft Dataverse

Начиная с ноября 2020 года Common Data Service был переименован в [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Дополнительные сведения см. в [официальном объявлении](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) в блоге по Power Apps. В сочетании с этим изменением имени была обновлена некоторая терминология в Dataverse. Например, вместо термина *объект* теперь используется термин *таблица*, а вместо термина *поле* — *столбец*. Дополнительные сведения см. в разделе [Обновления терминологии](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

В этом выпуске терминология, связанная в интеграцией Dynamics 365 Human Resources с Dataverse, обновлена в рамках всего приложения, чтобы отразить эти изменения. Например, форма **Интеграция Common Data Service** теперь называется **Интеграция Microsoft Dataverse**.

Дополнительные сведения об интеграции Dynamics 365 Human Resources с Microsoft Dataverse см. в разделах [Настройка интеграции Microsoft Dataverse](./hr-admin-integration-common-data-service.md) и [Настройка виртуальных таблиц Microsoft Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Human Resources](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2021, волна 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]