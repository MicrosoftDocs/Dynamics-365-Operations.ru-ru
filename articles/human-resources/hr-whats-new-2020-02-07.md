---
title: Что нового и что изменилось в Dynamics 365 Human Resources (7 февраля 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 7 февраля 2020 года.
author: andreabichsel
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0a45eed4e094cedb9d6d8ed0cb2bdc81eb31b76e
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128121"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>Что нового и что изменилось в Dynamics 365 Human Resources (7 февраля 2020 г.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources. Изменения применяются для номера сборки 8.1.2835. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>Аналитика обучения не показывает курс, если аудитория пуста (388289)

На странице аналитики обучения теперь отображается курс, если аудитория пуста.

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>Поиск должности не учитывает часовой пояс (405344)

При поиске открытых позиций теперь учитывается часовой пояс при проверке наличия открытой позиции.

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>Вид аналитики по текущему сальдо не обновляется с учетом правильного текущего сальдо отпуска после отправки запросов отсутствия (409756)

Текущее сальдо теперь включает отправленные запросы отсутствия.

## <a name="in-preview"></a>В режиме предварительного просмотра

Следующие функции предварительного просмотра доступны с 3 февраля 2020 г.:

- **Предварительные функции отпуска и отсутствия** — Дополнительные сведения см. в [Предварительные функции отпуска и отсутствия](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Функция предварительного просмотра управления льготами** — дополнительные сведения, включая известные проблемы, см. в разделе [Обзор управления преимуществами](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Скоро

### <a name="platform-update-32"></a>Обновление платформы update 32 

Скоро будет доступно обновление платформы 32. [Дополнительные сведения об обновлении платформы 32 см. здесь](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

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
[Обзор выпуска Dynamics 365 Human Resources 2019, волна 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)