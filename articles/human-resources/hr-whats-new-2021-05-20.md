---
title: Что нового и что изменилось в Dynamics 365 Human Resources (20 мая 2021 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 20 мая 2021 года.
author: marcelbf
ms.date: 05/20/2021
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
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4519e90e19d0652f855999d1a73ca64777b53b53465d6065987afc1cf2494187
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731945"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Что нового и что изменилось в Dynamics 365 Human Resources (20 мая 2021 г.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описываются новые, измененные и ожидающиеся компоненты в Dynamics 365 Human Resources.

Дополнительные сведения о нашем процессе обновления и графике см. в разделе [Процесс обновления](hr-admin-setup-update-process.md).

Дополнительные сведения о новых функциях и ожидаемых датах общей доступности см. в разделе [Обзор Dynamics 365 Human Resources 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>В данном выпуске

Этот выпуск включает следующие новые функции и исправления ошибок. Изменения применяются для номера сборки 8.1.4189.

### <a name="new-features"></a>Новые возможности

В этой версии следующие функции стали общедоступными.

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Обновление платформы 10.0.18 (42) | -- | [Обновления платформы для версии 10.0.18 приложений Finance and Operations (май 2021 г.)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Приложение Human Resources для Microsoft Teams поддерживает определения половины дня и возможности разделения дней | -- | [Управление запросами на отпуск в Teams](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Исправления ошибок

Этот выпуск содержит следующие исправления ошибок.

> [!NOTE]
> Наша цель — предоставить эту информацию вам как можно скорее. Мы может обновить этот раздел для включения исправлений ошибок, которые были сделаны в сборке после первоначальной публикации этого раздела.

| Номер проблемы | Проблема |  описание |
| --- | --- | --- |
| 583776 | Массовая регистрация сотрудников в планах отпусков вызывает ошибку дублирования записей | Эта ошибка была исправлена в последнем выпуске и массовая регистрации планов отпусков должна быть успешно обработана. |
| 582263 | Невозможно выполнить обработку событий в жизни для всех работников одновременно | Если поле **Работник** оставлено пустым для обработки событий в жизни, все работники будут обработаны. |
| 558383 | Основной бенефициар не помечается как 100%, если не выбран кандидат по умолчанию | Ошибка исправлена, так что пользователю нужно только выбрать переключатель основного бенефициара.|
| 509404 | Анализ численности подразделений не учитывает перемещение сотрудников между подразделениями |Аналитика была обновлена, чтобы включить в нее перемещения сотрудников между подразделениями|
| 579420 | Закрепление столбцов в сетках еще не должно быть доступно | Функция **Фиксация столбцов в сетках**, которая недоступна в Human Resources, была указана как доступна в модуле "Управление персоналом". Эта функция была удалена из списка функций для включения. |

## <a name="in-preview"></a>В режиме предварительного просмотра

В предварительной версии доступны следующие новые функции. Дополнительные сведения о включении и выключении функций см. в разделе [Управление функциями](hr-admin-manage-features.md).

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Поддержка настраиваемых полей в правилах приемлемости управления льготами | [Поддержка настраиваемых полей для обработки допустимости](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Настройка правил приемлемости](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Рабочая область управления льготами | [Рабочая область управления льготами (предварительная версия)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Рабочая область управления льготами](hr-benefits-management-workspace.md) |
| Улучшения системы workflow-процесса отпуска и отсутствия | [Улучшения системы workflow-процесса отпуска и отсутствия](https://go.microsoft.com/fwlink/?linkid=2147528) | [Запрос на отгул](hr-employee-self-service-request-time-off.md)|
| Включить упрощенную интеграцию зарплаты (API интеграции зарплаты) | [Включение упрощенной интеграции с поставщиками зарплаты](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API интеграции зарплаты](hr-admin-integration-payroll-api-introduction.md)|
| Аудит проводок начислений отпуска | - | [Аудит проводок начислений отпуска](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Скоро

| Функция | Подробности |
| --- | --- |
|  Использование менеджера отсутствия для управления отпуском | [Использование менеджера отсутствия для управления отпуском](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Полный список запланированных функций и их запланированных выпусков см. в разделе [Обзор выпуска волны 1 Dynamics 365 Human Resources от 2021 года](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Human Resources](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2021, волна 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
