---
title: Что нового и что изменилось в Dynamics 365 Human Resources (3 мая 2021 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 3 мая 2021 года.
author: marcelbf
ms.date: 05/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 944d5794bb535faa18b4f2de8b5382ebfb9bc2ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022071"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>Что нового и что изменилось в Dynamics 365 Human Resources (3 мая 2021 г.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описываются новые, измененные и ожидающиеся компоненты в Dynamics 365 Human Resources.

Дополнительные сведения о нашем процессе обновления и графике см. в разделе [Процесс обновления](hr-admin-setup-update-process.md).

Дополнительные сведения о новых функциях и ожидаемых датах общей доступности см. в разделе [Обзор Dynamics 365 Human Resources 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>В данном выпуске

Этот выпуск включает следующие новые функции и исправления ошибок. Изменения применяются для номера сборки 8.1.4140.

### <a name="new-features"></a>Новые возможности

В этой версии следующие функции стали общедоступными.

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Панель информации добавляется при создании событий жизненного цикла. | - | При создании события жизненного цикла информационная панель отображает сообщение, указывающее тип созданного события жизненного цикла.

### <a name="bug-fixes"></a>Исправления ошибок

Этот выпуск содержит следующие исправления ошибок.

> [!NOTE]
> Наша цель — предоставить эту информацию вам как можно скорее. Мы может обновить этот раздел для включения исправлений ошибок, которые были сделаны в сборке после первоначальной публикации этого раздела.

| Номер проблемы | Расход |  описание |
| --- | --- | --- |
| 559312 |  Уровень не отображается при создании плана фиксированной компенсации для сотрудника. |  При несоответствии часового пояса и часового пояса пользователя и компании, уровень компенсации в задании не может быть прочитан. Запрос был обновлен до выборки в соответствии с временем в формате UTC. |
| 573676  | Не удается добавить новый период в форму **План льгот**. | Обновлена форма таким образом, что кнопка **Создать** доступна на экспресс-вкладке **Период** в **Планы льгот**. |

## <a name="in-preview"></a>В режиме предварительного просмотра

В предварительной версии доступны следующие новые функции. Дополнительные сведения о включении и выключении функций см. в разделе [Управление функциями](hr-admin-manage-features.md).

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Рабочая область управления льготами | [Рабочая область управления льготами (предварительная версия)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Рабочая область управления льготами](hr-benefits-management-workspace.md) |
| Улучшения системы workflow-процесса отпуска и отсутствия | [Улучшения системы workflow-процесса отпуска и отсутствия](https://go.microsoft.com/fwlink/?linkid=2147528) | [Запрос на отгул](hr-employee-self-service-request-time-off.md)|
| Включить упрощенную интеграцию зарплаты (API интеграции зарплаты) | [Включение упрощенной интеграции с поставщиками зарплаты](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API интеграции зарплаты](hr-admin-integration-payroll-api-introduction.md)|
| Аудит проводок начислений отпуска | - | [Аудит проводок начислений отпуска](hr-leave-and-absence-accrue.md#preview-leave-accrual-transaction-auditing)|

## <a name="coming-soon"></a>Скоро

| Функция | Подробности |
| --- | --- |
| Навыки, введенные руководителем для своих сотрудников, могут быть автоматически утверждены рабочим процессом | Скоро появится. |
| Обновление платформы 10.0.18 (42) | Планируется начать развертывание обновления платформы 10.0.18 с сервисным выпуском 17 мая 2021 года. Дополнительные сведения см. в разделе [Обновления платформы для версии 10.0.18 приложений Finance and Operations (май 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Поддержка настраиваемых полей в правилах приемлемости управления льготами  | [Поддержка настраиваемых полей для обработки допустимости](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Полный список запланированных функций и их запланированных выпусков см. в разделе [Обзор выпуска волны 1 Dynamics 365 Human Resources от 2021 года](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Human Resources](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2021, волна 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
