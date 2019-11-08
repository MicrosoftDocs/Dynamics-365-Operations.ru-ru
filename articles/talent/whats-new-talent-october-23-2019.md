---
title: Что нового и что изменилось в Dynamics 365 Talent (23 октября 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
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
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 94243f83121a1306d8f9ae9be23d24e5c9b63a2d
ms.sourcegitcommit: 07e109dec176a93eff0df8a37ba5d875f212e9f1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "2662673"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (23 октября 2019 г.)

[!include [banner](includes/banner.md)]

В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract
Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Изменения в Onboard
Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2569. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Обновление платформы 30 для приложений Finance and Operations

Для получения дополнительных сведений см. раздел [Что нового и что изменилось в обновлении платформы 30 для приложений Finance and Operations (Ноябрь 2019)](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30).

### <a name="remove-benefits-open-enrollment-preview-feature"></a>Удалить функцию предварительного просмотра открытой регистрации льгот

В сочетании с нашим объявлением в записи блога Стратегические инвестиции в Core HR способствуют повышению производительности Корпорация Майкрософт удаляет функцию открытой регистрации льгот из общедоступной предварительной версии 18 октября 2019 года. Вместо этого в будущем будут выпущены новые функции. Производственное использование функции открытой регистрации льгот, которая в настоящее время находится в общедоступной предварительной версии, не будет поддерживаться.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>Ошибка при выборе страны/региона в форме работника во второй раз (350294)

В выпуске этой недели проблема при выборе страны/региона в форме **Работник** была исправлена.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>Значения финансовой аналитики по умолчанию устанавливаются в поле Показывать комбинации, если для параметра не разрешать ввод вручную задано значение true (340097)

При этом изменении, при настройке финансовых аналитик и использовании параметра не разрешать ввод вручную, значение аналитики по умолчанию корректно используется системой в поле **Показывать комбинации**.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>Новые типы связей следует добавить в поиск связей в форме личные контакты (347691)

В состав этого выпуска входят новые возможности добавления новых типов связей в таблицу **Типы связей** и отражения изменений в поиске связей для личных контактов.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>Дополнительные значения списка в настраиваемых полях не отражаются в Common Data Service (379599)

В выпуске этой недели при добавлении нового значения списка в существующее настраиваемое поле, которое уже было синхронизировано с Common Data Service, новые значения списка выбора отобразятся после применения изменений к объекту.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>На странице Условия найма все условия найма сотрудника отображаются после выбора пункта Открыть в Excel (348073)

В этом выпуске в Microsoft Excel будут открываться только условия найма выбранных сотрудников. Также учитывается вся безопасность компании.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service---324178"></a>Связь между сущностью выходного рабочего календаря и сущностью рабочего календаря отсутствует в Common Data Service — (324178)

Эта связь была добавлена в этом выпуске. Это изменение позволит отображать в PowerApps рабочие дни сотрудника. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>Ошибка при использовании Workflow-процессов самообслуживания сотрудников с настраиваемыми иерархиями (370132)

В этом выпуске улучшена система обмена сообщениями, в которой можно настроить workflow-процессы, используя настраиваемые иерархии. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>Система позволяет создавать новые должности, для которых дата доступности для назначения предшествует дате активации (340103)

Это изменение выведет предупреждение, если дата **доступности для назначения** предшествует дате **активации** должности.

## <a name="coming-soon"></a>Скоро

### <a name="print-performance-reviews"></a>Печать оценок производительности

См. раздел [Печать оценок производительности](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) в Dynamics 365 волны 2 выпуска 2019 года.

### <a name="feature-management-workspace"></a>Рабочая область управления функциями

Функции добавляются и обновляются в каждом выпуске. Опыт управления функциями предоставляет рабочую область, в которой можно просматривать список функций, которые были поставлены в каждом выпуске. По умолчанию новые функции отключены. Можно использовать рабочую область для их включения и просмотра документации по ним.

Для получения дополнительных сведений об изменениях, связанных с управлением функциями, см. раздел [Обзор управления функциями,](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
