---
title: Что нового и что изменилось в Dynamics 365 Human Resources (19 марта 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 19 марта 2020 года.
author: andreabichsel
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f88a3a83794cc46f670143bdb97c9624cff8dd0
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694769"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a>Что нового и что изменилось в Dynamics 365 Human Resources (19 марта 2020 г.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources. Изменения применяются для номера сборки 8.1.3014. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Lifecycle Services (LCS) для справки.

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Ограничения среды Human Resources теперь основаны на обновленной лицензии (394595)

Изменилось предельное число сред для каждого проекта в службах Lifecycle Services (LCS). Предыдущим пределом было две среды. Ограничение на число производственных сред и "песочниц", которые можно создать для Human Resources в LCS, теперь основано на обновленном лицензировании. Теперь можно создать столько сред, сколько требуется для проекта LCS, в зависимости от числа купленных лицензий. Новая лицензия, обновленная 1 февраля 2020 г., позволяет клиентам покупать дополнительные среды. Дополнительные сведения о требованиях лицензирования для дополнительных сред см. в [Руководстве по лицензированию Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a>Предоставление межфирменного просмотра данных компенсаций для сотрудников и руководителей (403904)

Включите эту функцию в рабочей области **Управление функциями**. Дополнительные сведения см. в разделе [Включение или отключение предварительных версий функций](hr-admin-manage-features.md#enable-or-disable-preview-features).

Когда эта функция включена, менеджеры могут просматривать компенсации прямых и расширенных подчиненных без необходимости входить в компанию, в которой они работают. Полная история компенсаций доступна из любой компании, в которую выполнен вход, к которой имеет доступ менеджер. Дополнительные сведения см. в разделе [Обзор самообслуживания сотрудников и менеджеров](hr-employee-manager-self-service-overview.md).

## <a name="enable-global-address-book-merge-functionality-427189"></a>Включение функции объединения глобальных адресных книг (427189)

Теперь можно выполнить слияние дубликатов записей адресной книги, выбрав дубликаты записей и выбрав **Объединить** на странице **Глобальная адресная книга**.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a>Невозможно скорректировать сальдо отпусков для плана без начислений, созданных с функцией нескольких типов отпусков (419635)

Теперь можно скорректировать сальдо для планов отпусков, которые были созданы с использованием предварительной версии функции **Несколько типов отпусков**, включенной в управлении функциями.

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a>Поле основной должности в WorkerPositionAssignmentEntity при увольнении сотрудника (420774)

Для уволенных сотрудников основная должность, которая была активна на момент увольнения, отображается в объекте. Для интеграций повторная запись больше не будет создаваться для назначения рабочей должности сотрудника. 

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Решение Dataverse теперь доступно со следующими изменениями:

| описание | Изменение |
| --- | --- |
| Изменение объекта **Работа/должность** | <ul><li>Добавлено **Регион компенсации**</li>|
| Добавлен объект **Аналитика должностных обязанностей** | <ul><li>Добавлено **Финансовые аналитики**</li>
| Изменения объекта **Работник** | <ul><li>Добавлено **Последовательность имени**</li><li>Добавлено **Работа из дома**</li><li>Добавлено **Язык**</li><li>Добавлено **Дата начала стажа**</li><li>Добавлено **Дата юбилея**</li><li>Добавлено **Дата первоначального приема на работу**</li></ul> |
| Изменения объекта **Занятость** | <ul><li>Добавлено **Финансовые аналитики**</li><li>Добавлено **Причина увольнения**</li><li>**Дата увольнения** переименовано на **Дата передачи**</li><li>Добавлено **Дата испытательного срока**</li></ul> |
| Изменения объекта **Адрес работника** | <ul><li>Добавлен **Адрес улицы**</li><li>**Строка адреса 1**, **Строка адреса 2** и **Строка адреса 3** отмечены для устаревания</li></ul> |
| Новые объекты настройки переменной компенсации | <ul><li>**Тип плана переменной компенсации**</li><li>**План переменной компенсации**</li><li>**Положения о передаче прав на льготы**</li><li>**Уровень плана переменной компенсации**</li></ul> |
| Новый объект **Занятость по календарю работников** | <ul><li>Добавлено **Объект рабочего календаря**</li></ul> |
| Новый объект **Сведения о позиции зарплаты** | <ul><li>Добавлено **Сведения о позиции зарплаты**</li></ul> |
| Новый объект **Заголовок** | <ul><li>Добавлен **Заголовок**</li></ul>Новый объект **Заголовок** включен в Dataverse, но не упоминается в сущностях **Должностное положение** или **Должность** в данный момент. |

> [!NOTE]
> Финансовые аналитики для должностей и трудоустройства обеспечивают однонаправленную интеграцию для обновлений из модуля Human Resources в Dataverse. Обновления финансовых аналитик в данный момент не синхронизируются из Dataverse в модуль Human Resources.

В течение следующих нескольких недель эти изменения объекта будут доступны во всех средах. Чтобы вручную установить последнюю версию решения Dataverse для модуля Human Resources:

1.  Перейдите к [Центру администрирования Power Platform](https://admin.powerplatform.microsoft.com).

2.  Выберите **Среды**.

3.  Найдите среду, которую требуется обновить. Среда должна соответствовать значению **Имя среды** в разделе **Сведения Common Data Service** в форме **Сведения** в модуле Human Resources.

4.  Выберите среду, чтобы просмотреть сведения о среде.

5.  В верхней части на панели действий выберите **Управление решениями**. Откроется новое окно браузера; перейдите в **центр администрирования Dynamics 365** в контексте вашей среды.

6.  В списке **Решение** выберите **Привязка Dynamics 365 Human Resources**.

7.  Выберите **Обновить** для применения последнего решения.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>Предварительный просмотр SharePoint не работает в некоторых средах

Если предварительный просмотр документов, хранящихся в SharePoint, не работает, попробуйте выполнить следующую процедуру:

1. Убедитесь, что учетная запись администратора имеет адрес электронной почты, связанный с записью пользователя. Можно просмотреть эту информацию на странице **Пользователи**. Если адрес электронной почты не настроен, необходимо добавить адрес электронной почты и поставщика с помощью надстройки Excel OData. По умолчанию адрес электронной почты отсутствует в макете Excel. Необходимо отредактировать макет Excel, добавить все поля, применить и обновить. После выполнения этих шагов можно обновить учетную запись администратора.

2. После того как учетная запись администратора имеет связанную учетную запись электронной почты, войдите в Human Resources с учетными данными администратора.

3. Перейдите к вложению в SharePoint для запуска предварительного просмотра документа.

4. Выполните вход с другой учетной записью пользователя, который имеет доступ к вложениям, и убедитесь, что предварительный просмотр выполняется правильно.

## <a name="coming-soon"></a>Скоро

### <a name="platform-update-33"></a>Обновление платформы update 33

- Приложения полной страницы (предварительная версия) — это предварительная версия функции, которая требует включения функции сохраненных представлений, позволяет добавлять приложения Power Apps и приложения сторонних производителей в полноэкранном режиме с помощью панели мониторинга.

- Сохраненные представления (предварительная версия) — это предварительная версия функции, которая предоставляет значительные улучшения подсистемы персонализации. Эта функция позволяет пользователям иметь несколько именованных наборов личных настроек на каждой странице. Можно также публиковать представления для ролей безопасности.

- Оптимизированное взаимодействие фильтрации "один из" — эта функция обеспечивает возможность оптимизированной фильтрации "является одним из", что облегчает ввод нескольких значений фильтров, имеет более простой механизм для удаления отдельных или всех значений фильтров и более компактное и интуитивное визуальное представление значений фильтров.

- Рекомендуемые поля — пользователям часто приходится добавлять поля к сетке или странице. Это может быть сложно при наличии такого большого количества доступных полей. Вместо того, чтобы выполнять поиск в большом списке, эта функция позволяет системе показывать набор рекомендуемых полей в зависимости от того, что другие пользователи часто добавляются в подобных сценариях.

- Клейкие действия по умолчанию в сетках — эта функция гарантирует, что выполняемое по умолчанию действие в сетке связано с определенным столбцом в сетке, независимо от того, был ли этот столбец перемещен или скрыт.

## <a name="new-production-release-cadence"></a>Новая ритмичность выпуска производственных выпусков

Начиная с апреля, ритмичности выпуска Human Resources будет изменена с еженедельного обновления на обновление раз в две недели. Это обеспечит соответствие рекомендациям по безопасному развертыванию и поддержке высоких стандартов стабильности и надежности службы. Мы вводим дополнительное тестирование и мониторинг для проверки успешности развертывания на каждом этапе процесса. Дополнительные сведения о ритмичности выпуска см. в разделе [Процесс обновления](hr-admin-setup-update-process.md).

## <a name="in-preview"></a>В режиме предварительного просмотра

Следующие функции предварительного просмотра доступны с 3 февраля 2020 г.:

- **Предварительные функции отпуска и отсутствия** — Дополнительные сведения см. в [Предварительные функции отпуска и отсутствия](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Функция предварительного просмотра управления льготами** — дополнительные сведения, включая известные проблемы, см. в разделе [Обзор управления преимуществами](hr-benefits-management-overview.md).

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Human Resources](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2019, волна 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]