---
title: Введение API интеграции заработной платы
description: В этом разделе описывается API интеграции заработной платы Dynamics 365 Human Resources.
author: twheeloc
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3743561e3ea3c798c37d71d851eb6b197c8d1c41
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533836"
---
# <a name="payroll-integration-api-introduction"></a>Введение API интеграции заработной платы


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом документе описывается API интеграции заработной платы Dynamics 365 Human Resources. API позволяет упростить сквозную интеграцию между модулями Human Resources и партнерскими системами расчета заработной платы. Интегрированный опыт начинает работать в модуле Human Resources с профилем сотрудника, зарплатой и вычетом, а также информацией о вкладе. При приеме на работу сотрудника и вводе требуемого профиля и информации о зарплате в Human Resources система заработной платы извлекает эту информацию для использования при обработке заработной платы. Все обновления, сделанные для сотрудника или информации о зарплате, также извлекаются для использования в последующих запусках платежей.

[![Поток интеграции зарплаты.](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

Для включения интеграции модуль Human Resources включает следующие компоненты:

- [Функции для маркировки сотрудника как готового к оплате.](hr-compensation-payroll.md)
- API интеграции, открывающий новые функции для интеграции приложений.

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Этот API построен на основе Microsoft Dataverse (ранее Common Data Service). Все взаимодействие RESTful с этим API осуществляется с помощью веб-API Microsoft Dataverse, использующего OData. Этот API является подмножеством веб-API Dataverse. Веб-API Dataverse определяет такие характеристики, как проверка подлинности, соглашения SLA, пакет, управление одновременным доступом и обработка ошибок.

Дополнительные общие сведения о веб-API Microsoft Dataverse см. в разделах:

- [Что такое Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Использование веб-API Microsoft Dataverse](/powerapps/developer/data-platform/webapi/overview)
- [Руководство разработчика Microsoft Dataverse](/powerapps/developer/data-platform)

В этой документации содержатся сведения и руководство разработчика по использованию веб-API Dataverse, включая следующие разделы:

- [Проверка подлинности в Microsoft Dataverse с веб-API](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Выполнение операций с помощью веб-API](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Использование Postman в веб-интерфейсе API](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Отслеживание изменений используется для синхронизации данных с внешними системами](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Виртуальные таблицы для Human Resources в Dataverse

Конечные точки для API интеграции заработной платы используют возможности платформы виртуальных таблиц Microsoft Dataverse. По умолчанию виртуальные таблицы и связанные с ними конечные точки API не развертываются для сред Human Resources, позволяя организациям определять, какие конечные точки OData будут доступны для данной среды. Для использования API-интерфейса необходимо создать виртуальные таблицы для сущностей Human Resources для данной среды.

Сведения о создании виртуальных таблиц для API см. в разделе [Настройка виртуальных таблиц Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Модель данных

На следующей схеме показаны отношения внутри API. У нескольких типов есть внешние ключи для других, ранее существующих сущностей в модуле Human Resources, которые здесь не иллюстрируются. В этом документе приводятся сведения о сущностях, предназначенных специально для сценариев интеграции заработной платы. Однако в веб-API Dataverse для Human Resources имеется множество других сущностей, которые также могут быть связаны с интеграцией. Некоторые из этих сущностей упоминаются в отношениях внешнего ключа или свойствах навигации.

[![Модель данных API интеграции заработной платы.](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>Сотрудник заработной платы и связанные сущности

Объекты:

- [Сотрудник зарплаты](hr-admin-integration-payroll-api-payroll-employee.md)
- [Адрес работника зарплаты](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [План фиксированной компенсации зарплаты](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [План переменной компенсации зарплаты.](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [Задание позиции зарплаты](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Позиция зарплаты](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>См. также

[Создание и проверка объектов зарплаты](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Настройка параметров Human Resources](hr-setup-parameters.md)<br>
[Настройка общих параметров Human Resources](hr-setup-shared-parameters.md)<br>
[Что такое Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Использование веб-API Microsoft Dataverse](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
