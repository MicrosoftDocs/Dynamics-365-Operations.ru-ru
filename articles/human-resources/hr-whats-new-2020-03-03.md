---
title: Что нового и что изменилось в Dynamics 365 Human Resources (3 марта 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fdd409b33989e371d0bd2a6e21b27721336cea0
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2020
ms.locfileid: "3114435"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Что нового и что изменилось в Dynamics 365 Human Resources (3 марта 2020 г.)

В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources. Изменения применяются для номера сборки 8.1.2955. Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Решение Common Data Service теперь доступно со следующими изменениями:

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

В течение следующих нескольких недель эти изменения объекта будут доступны во всех средах. Чтобы вручную установить последнюю версию решения Common Data Service для модуля Human Resources:

1.  Перейдите к [Центру администрирования Power Platform](https://admin.powerplatform.microsoft.com).

2.  Выберите **Среды**.

3.  Найдите среду, которую требуется обновить. Среда должна соответствовать значению **Имя среды** в разделе **Сведения Common Data Service** в форме **Сведения** в модуле Human Resources.

4.  Выберите среду, чтобы просмотреть сведения о среде.

5.  В верхней части на панели действий выберите **Управление решениями**. Откроется новое окно браузера; перейдите в **центр администрирования Dynamics 365** в контексте вашей среды.

6.  В списке **Решение** выберите **Привязка Dynamics 365 Human Resources**.

7.  Выберите **Обновить** для применения последнего решения.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>Проблемы импорта с информационным объектом регистрации отпусков (406082)

Теперь можно зарегистрировать сотрудника в новом плане отпусков того же типа, если новая дата регистрации позже даты окончания срока регистрации предыдущего плана.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>Проблема с экспортом ставок взносов в объекте 401k payrollWorkerEnrolledBenefitDetail в DMF (420700)

Это изменение исправляет функцию экспорта для объекта **payrollWorkerEnrolledBenefitDetail**, чтобы отобразить текущие значения для вклада работодателя.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Поиск в упрощенной форме работника приводит к появлению сообщения "Поле человека должно быть заполнено" (402525)

При поиске сотрудника больше не будет выводиться сообщение о том, что необходимо заполнить поле **Человек**.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>Значение поля примечания не отображается в форме добавления дополнительных навыков (380134)

Это изменение исправляет проблему при настройке формы **Добавить дополнительные навыки** в службе дистанционного обслуживания сотрудников.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Срок действия нескольких планов фиксированной компенсации не истекает при перемещении сотрудников (389466)

С этим изменением срок действия всех активных записей фиксированной компенсации для старой должности истечет в дату перехода.

## <a name="in-preview"></a>В режиме предварительного просмотра

Следующие функции предварительного просмотра станут доступны 3 февраля 2020 г.:

- **Предварительные функции отпуска и отсутствия** — Дополнительные сведения см. в [Предварительные функции отпуска и отсутствия](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Функция предварительного просмотра управления льготами** — дополнительные сведения, включая известные проблемы, см. в разделе [Обзор управления преимуществами](hr-benefits-management-overview.md).