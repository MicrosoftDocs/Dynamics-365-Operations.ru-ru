---
title: Что нового и что изменилось в Dynamics 365 Human Resources (12 февраля 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 12 февраля 2020 года.
author: andreabichsel
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ce265627bf5cef023770be3f8953e12d49866be
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686921"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Что нового и что изменилось в Dynamics 365 Human Resources (12 февраля 2020 г.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources. Изменения применяются для номера сборки 8.1.2867. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>Существующие объекты CompFixedEmpls и HcmPersonImage должны быть доступны из OData (414178)

В выпуске этой недели субъекты **CompFixedEmpls** и **HcmPersonImage** стали общедоступными и доступны через ODAta.

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a>Удаление занятости из Dataverse не работает, когда сведения о занятости не активны (403193)

Это изменение теперь позволяет удалять занятость через Dataverse, когда не существует активных сведений о занятости.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>Статус workflow-процесса регистрации курса изменится на завершено, и после второго утверждения появляются ошибки (409749)

Workflow-процесс регистрации курса был обновлен, чтобы учесть нескольких утверждающих.

## <a name="in-preview"></a>В режиме предварительного просмотра

Следующие функции предварительного просмотра доступны с 3 февраля 2020 г.:

- **Предварительные функции отпуска и отсутствия** — Дополнительные сведения см. в [Предварительные функции отпуска и отсутствия](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Функция предварительного просмотра управления льготами** — дополнительные сведения, включая известные проблемы, см. в разделе [Обзор управления преимуществами](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Скоро

### <a name="platform-update-32"></a>Обновление платформы update 32 

Скоро будет доступно обновление платформы 32. [Дополнительные сведения об обновлении платформы 32 см. здесь](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

### <a name="updated-dataverse-solution"></a>Обновленное решение Dataverse

Новое решение Dataverse будет доступно в ближайшее время со следующими изменениями:

| Описание | Изменение |
| ----------------------------------------- | --- |
| Изменение объекта **Работа/должность** | Добавлено **Регион компенсации**</br>Добавлено **Финансовые аналитики** |
| Изменения объекта **Работник** | Добавлено **Последовательность имени**</br>Добавлено **Работа из дома**</br>Добавлено **Язык**</br>Добавлено **Дата начала стажа**</br>Добавлено **Дата юбилея**</br>Добавлено **Дата первоначального приема на работу** |
| Изменения объекта **Занятость** | Добавлено **Финансовые аналитики**</br>Добавлено **Причина увольнения**</br>**Дата увольнения** переименовано на **Дата передачи**</br>Добавлено **Дата испытательного срока** |
| Изменения объекта **Адрес работника** | Добавлен **Адрес улицы**</br>**Строка адреса 1**, **Строка адреса 2** и **Строка адреса 3** отмечены для устаревания |
| Новые объекты настройки переменной компенсации | **Тип плана переменной компенсации**</br>**План переменной компенсации**</br>**Положения о передаче прав на льготы**</br>**Уровень плана переменной компенсации** |
| Новый объект **Занятость по календарю работников** | Добавлено **Объект рабочего календаря** |
| Новый объект **Сведения о позиции зарплаты** | Добавлено **Сведения о позиции зарплаты** |
| Новый объект **Заголовок** | Добавлено **Заголовок**. Новый объект **Заголовок** будет включен в процесс синхронизации между Управление персоналом и Dataverse. Она не должна быть изначально указана в объектах **Позиция** или **Должность**. |

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Управление персоналом](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2019, волна 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]