---
title: Что нового и что изменилось в Dynamics 365 Talent (21 января 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528130"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Что нового и что изменилось в Dynamics 365 Talent (21 января 2020 г.)

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой статье описываются новые и измененные компоненты в Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract. Мы добавили функции в Attract для поддержки нашего последнего объявления, [Повышение эффективности сотрудников с Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/).

### <a name="download-environment-data"></a>Загрузка данных среды

Администраторы могут загружать данные своей среды. Данные экспортируются в стандартном формате JSON со всеми заданиями, кандидатами и конфигурацией, экспортированными в ZIP-файл. Дополнительные сведения см. в разделе [Экспорт данных из Attract и Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Ограничение доступа к средам для пользователей, не являющихся администраторами

Администраторы могут ограничить доступ к среде для пользователей, не являющихся администраторами. Это действие невозможно отменить. Дополнительные сведения см. в разделе [Ограничение доступа к Attract](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Изменения в Onboard

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

### <a name="exporting-onboarding-guides"></a>Экспорт руководств по адаптации

Пользователи теперь могут экспортировать все руководства по адаптации и шаблоны по адаптации в формате документов Word. Дополнительные сведения см. в разделе [Экспорт данных из Attract и Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2726. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>Поле последней ежегодной компенсации в форме проверки найма не соответствует (392092)

Этот выпуск включает изменения, которые будут постоянно отображать последнюю валюту на основе выбора компании в форме **Проверка занятости**.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Называется полем, добавленным в поиск получателя обратной связи (407789)

При обеспечении обратной связи по производительности поиск сотрудников не предоставлял достаточно сведений, чтобы определить, будет ли обратная связь передана правильному человеку. Мы добавили столбец **Известно как**, который поможет идентифицировать уникальное имя сотрудника.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>Запись HcmWorkerPayrollInfo создается без связи с работником (394526)

Этот выпуск включает изменение, чтобы не записывать HcmWorkerPayrollInfo без ссылки на сотрудника.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Возможность редактирования подразделения при переходах из иерархии должностей (341001)

Когда безопасность настроена на запрет доступа к редактируемым подразделениям, редактирование отключено при переходе к форме **Подразделения** во всех сценариях.

## <a name="coming-soon"></a>Скоро

Новое решение Common Data Service будет доступно в ближайшее время со следующими изменениями:

| Описание | Изменение |
| --- | --- |
| Изменение объекта **Работа/должность** | <ul><li>Добавлено **Регион компенсации**</li><li>Добавлено **Финансовые аналитики**</li></ul> |
| Изменения объекта **Работник** | <ul><li>Добавлено **Последовательность имени**</li><li>Добавлено **Работа из дома**</li><li>Добавлено **Язык**</li><li>Добавлено **Дата начала стажа**</li><li>Добавлено **Дата юбилея**</li><li>Добавлено **Дата первоначального приема на работу**</li></ul> |
| Изменения объекта **Занятость** | <ul><li>Добавлено **Финансовые аналитики**</li><li>Добавлено **Причина увольнения**</li><li>**Дата увольнения** переименовано на **Дата передачи**</li><li>Добавлено **Дата испытательного срока**</li></ul> |
| Изменения объекта **Адрес работника** | <ul><li>Добавлен **Адрес улицы**</li><li>**Строка адреса 1**, **Строка адреса 2** и **Строка адреса 3** отмечены для устаревания</li></ul> |
| Новые объекты настройки переменной компенсации | <ul><li>**Тип плана переменной компенсации**</li><li>**План переменной компенсации**</li><li>**Положения о передаче прав на льготы**</li><li>**Уровень плана переменной компенсации**</li></ul> |
| Новый объект **Занятость по календарю работников** | <ul><li>Добавлено **Объект рабочего календаря**</li></ul> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]