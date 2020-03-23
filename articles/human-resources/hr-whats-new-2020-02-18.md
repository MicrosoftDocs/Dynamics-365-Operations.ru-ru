---
title: Что нового и что изменилось в Dynamics 365 Human Resources (18 февраля 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 96e66c86e98cc1cfee82221da06f9c57a17d170b
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077469"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Что нового и что изменилось в Dynamics 365 Human Resources (18 февраля 2020 г.)

В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources. Изменения применяются для номера сборки 8.1.2903. Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.

## <a name="platform-update-32"></a>Обновление платформы update 32 

Доступно обновление платформы 32. Для получения дополнительных сведений см. раздел [Что нового и что изменилось в обновлении платформы 32 для Finance and Operations (февраль 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Значения поиска запоминаются при изменении параметров просмотра в упрощенной форме сотрудника (383833)

Новая форма **Работник** теперь запоминает значения поиска при изменении параметров просмотра и применении изменений.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Сводные плитки управления компенсациями в функции предварительного просмотра перенаправляют в неправильную форму (401861)

Плитки управления фиксированной и переменной компенсацией теперь отображают правильные записи в новой форме **Работник**. Применяется только к функции предварительного просмотра упрощенной формы сотрудника. Эту функцию предварительного просмотра можно включить в **управлении функциями**. Дополнительные сведения см. в разделе [Управление функциями](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a>Пустое поле статуса для некоторых записей запроса отпуска в Common Data Service (414915)

Это изменение исправляет проблему с Common Data Service, когда поле **Статус** в запросе отпуска установлено на **Просмотреть**. Common Data Service теперь отображает статус.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Анализ несоответствия навыков возможен для назначенного задания (411390)

Теперь можно выполнить анализ несоответствия навыков для любого задания, определенного в Управление персоналом.

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a>Системная валюта не синхронизируется из Common Data Service с Управление персоналом в новых средах (418011)

Системная валюта в Common Data Service теперь может синхронизироваться с Управление персоналом.

## <a name="in-preview"></a>В режиме предварительного просмотра

- [Предварительные функции отпуска и отсутствия](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Предварительная версия управления льготами](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Скоро

### <a name="updated-common-data-service-solution"></a>Обновленное решение Common Data Service

Новое решение Common Data Service будет доступно в ближайшее время со следующими изменениями:

| Описание | Изменение |
| ----------------------------------------- | --- |
| Изменение объекта **Работа/должность** | Добавлено **Регион компенсации**</br>Добавлено **Финансовые аналитики** |
| Изменения объекта **Работник** | Добавлено **Последовательность имени**</br>Добавлено **Работа из дома**</br>Добавлено **Язык**</br>Добавлено **Дата начала стажа**</br>Добавлено **Дата юбилея**</br>Добавлено **Дата первоначального приема на работу** |
| Изменения объекта **Занятость** | Добавлено **Финансовые аналитики**</br>Добавлено **Причина увольнения**</br>**Дата увольнения** переименовано на **Дата передачи**</br>Добавлено **Дата испытательного срока** |
| Изменения объекта **Адрес работника** | Добавлен **Адрес улицы**</br>**Строка адреса 1**, **Строка адреса 2** и **Строка адреса 3** отмечены для устаревания |
| Новые объекты настройки переменной компенсации | **Тип плана переменной компенсации**</br>**План переменной компенсации**</br>**Положения о передаче прав на льготы**</br>**Уровень плана переменной компенсации** |
| Новый объект **Занятость по календарю работников** | Добавлено **Объект рабочего календаря** |
| Новый объект **Сведения о позиции зарплаты** | Добавлено **Сведения о позиции зарплаты** |
| Новый объект **Заголовок** | Добавлено **Заголовок**. Новый объект **Заголовок** будет включен в процесс синхронизации между Управление персоналом и Common Data Service. Она не должна быть изначально указана в объектах **Позиция** или **Должность**. |

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Управление персоналом](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2019, волна 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)