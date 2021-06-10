---
title: Что нового и что изменилось в Dynamics 365 Human Resources (23 июля 2020 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 23 июля 2020 года.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e48b0694418710322957de811952e12da22b0509
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055397"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Что нового и что изменилось в Dynamics 365 Human Resources (23 июля 2020 г.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме описываются новые и измененные компоненты Dynamics 365 Human Resources. Изменения применяются для номера сборки 8.1.3416. Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Удаление финансовых аналитик для позиции не работает должным образом (445476)

После удаления аналитик из позиции эти же позиции удаляются из Dataverse.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Позиции не в иерархии показывают неактивные позиции (397257)

Неактивные позиции (с истекшим сроком действия) не отображаются в иерархии позиций в качестве **Позиции не в иерархии**. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Проверка между LeaveEnrollmentEntity и HcmWorkerEntity в импорте в структуре управления данными (DMF) вызывает медленную загрузку данных (442324)

Изменения в этом выпуске увеличивают производительность **LeaveEnrollmentEntity**.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Невозможно выполнить индивидуальную настройку в администрировании организации (447490)

С этим изменением теперь можно персонализировать ссылки в **Администрирование организации**.

## <a name="in-preview"></a>В режиме предварительного просмотра

## <a name="mandatory-fields"></a>Обязательные поля 

Теперь можно сделать поля обязательными, используя возможности персонализации в Human Resources. Для этой функции требуются **сохраненные представления**.

## <a name="human-resources-application-in-teams"></a>Приложение Human Resources в Teams

Сотрудники могут просматривать и запрашивать время отсутствия на работе в Microsoft Teams. Они могут взаимодействовать с ботом для создания запросов на отпуск. Дополнительные сведения см. в разделе [Приложение Human Resources в Teams](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Объекты платформы управления данными (ДМФ) для управления льготами
 
Объекты управления льготами выпускаются. Объекты DMF позволяют импортировать и экспортировать данные для упрощения настройки управления льготами. Будет доступен шаблон управления льготами для перемещения данных. Шаблон экспортирует и импортирует данные последовательно для учета зависимостей данных.

## <a name="buy-and-sell-leave"></a>Покупка и продажа отпуска 

Некоторые организации предоставляют льготу, позволяющую сотрудникам покупать или продавать отпуск. Этот процесс часто управляется вручную. Эта функция автоматизирует управление политиками и запросами для отдела кадров. Она упрощает процесс управления отпусками и помогает исключить ошибки. Дополнительные сведения см.

- [Управление политиками покупки и продажи отпусков](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Покупка и продажа отпуска](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Начисление отпуска для одной компании или одного плана

Клиенты могут обрабатывать начисления для одной компании или для одного плана отпусков и отсутствия. Эта возможность обеспечивает ясность для процесса начисления для клиентов с различными политиками лет отпусков или начисления отпусков. Дополнительные сведения см. в разделе [Начисление отпуска по компаниям или по плану отпуска](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Добавление вложений в запросы на отгулы

Возможность добавлять вложения к утвержденным запросам отпусков является критической в текущей среде COVID-19. Сотрудники теперь смогут добавлять эти вложения. Они также имеют более глубокое представление о том, как выполняются запросы на отпуск. Дополнительные сведения см. в разделе [Добавление вложений к существующему запросу](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Добавление кода основания к приостановке начисления 

Коды основания были добавлены в приостановку начисления.

## <a name="carry-forward-rules"></a>Правила переноса 

Можно указать тип переноса отпуска для переноса сальдо, где переносятся корректировки переноса. Например, если сотрудник переносит на 10 дней вперед, можно выбрать другой тип отпуска для этих 10 дней. Дополнительные сведения см. в разделе [Настройка типов отпусков и отгулов](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Приостановка начисления отпуска для указанных типов отпусков

Вы можете создать правило приостановки начисления для сотрудников с запросами на отпуск, которые выбрали неоплачиваемый отпуск. Тип "Неоплачиваемый отпуск" возможен, но это не обязательно. Можно приостановить любой отпуск на основе другого типа отпуска.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>Объект DMF доступен для приостановки начисления 

Объект DMF теперь доступен для приостановки начисления.

## <a name="coming-soon"></a>Скоро

## <a name="checklist-entities-included-in-dataverse"></a>Сущности контрольного списка, включенные в Dataverse

Сущности контрольного списка для адаптации, увольнения, переходов и бизнес-процессов в скором времени будут доступны в Dataverse.

## <a name="platform-changes"></a>Изменения платформы

Обновление платформы 10.0.12 (36)

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Human Resources](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2019, волна 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]