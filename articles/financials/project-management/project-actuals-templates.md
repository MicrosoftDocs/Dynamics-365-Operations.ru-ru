---
title: "Синхронизировать фактические данные проекта из Project Service Automation непосредственно в журнал интеграции проекта для разноски в Finance and Operations"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации фактических данных проекта непосредственно из Microsoft Dynamics 365 for Project Service Automation с Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: ru-ru
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Синхронизировать фактические данные проекта из Project Service Automation непосредственно в журнал интеграции проекта для разноски в Finance and Operations

В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации фактических данных проекта непосредственно из Microsoft Dynamics 365 for Project Service Automation с Microsoft Dynamics 365 for Finance and Operations.

Шаблон синхронизирует транзакции из Project Service Automation в промежуточную таблицу в Finance and Operations. После завершения синхронизации необходимо импортировать из промежуточной таблицы в журнал интеграции.

> [!NOTE]
> Интеграция фактические данные проекта доступен в Dynamics 365 for Finance and Operations версии 8.01.

> [!NOTE]
> При своевременном вводе суммы налога или проводок расходов в Project Service Automation необходимо установить Обновление 7 проекта Project Service Automation. Если это обновление не установлено, фактические данные налога не будут связаны со ассоциированным временем или фактические данные о расходах и не будут синхронизированы с Finance and Operations. Для получения дополнительных сведений обратитесь в поддержку .


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Поток данных для Project Service Automation для Finance and Operations

Решение по интеграции Project Service Automation в Finance and Operations использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance and Operations. Шаблоны интеграции, доступные при использовании функции интеграции данных, включают поток данных по фактическим данным проекта из Project Service Automation в Finance and Operations.

На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance and Operations.

[![Поток данных для интеграции Project Service Automation с Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Шаблоны и задачи

Для доступа к доступным шаблонам в центре администрирования Microsoft PowerApps выберите **Проекты**и выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.

Следующий шаблон и базовые задачи используются для синхронизации фактических данных по проект из Project Service Automation в Finance and Operations:

-  **Имя шаблона в интеграции данных:** Фактические данные по проекту (PSA в Fin and Ops)

-  **Имя задач в проекте:** 
    - Фактические данные 
    - TransactionConnections

## <a name="entity-set"></a>Набор объектов

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| Фактические данные                         | Объект интеграции для фактических данных проекта                      |
| Связи проводок         | Объект интеграции для связей проводок по проекту    |

## <a name="entity-flow"></a>Поток объектов

Фактические данные проекта управляются в Project Service Automation и синхронизируются с Finance and Operations в журнале интеграции проекта. Учет применяется на основе финансовых аналитик по умолчанию и настройки разноски.

## <a name="preconditions"></a>Предварительные условия

Прежде чем произойдет синхронизация фактических данных, необходимо настроить параметры интеграции Project Service Automation и синхронизировать проекты, задачи по проекту и категории транзакции расходов для проекта.

## <a name="power-query"></a>Power Query

Необходимо использовать Microsoft Power Query в шаблоне проекта фактические данные для:
- Преобразование **Тип транзакции** Project Service Automation в правильный **Тип транзакции** в Finance and Operations. Шаблон фактических данных проекта (PSA и Fin and Ops) уже имеет определенное преобразование.
- Преобразование **Тип выставления счетов** Project Service Automation в правильный **Тип выставления счетов** в Finance and Operations. Шаблон фактических данных проекта (PSA и Fin and Ops) уже имеет определенное преобразование. Тип выставления счетов сопоставляется с **Свойства строки** на основе конфигурации в форме параметров интеграции Dynamics 365 for Project Service Automation.
- Отфильтруйте определенные **Подразделения ресурсов**, которые должны быть синхронизированы с помощью этого шаблона.
- Если **фактические данные по внутрихолдинговым значениям времени или внутрихолдинговые расходам** будут синхронизированы с Finance and Operations, следует преобразовать контракт **Контрактное подразделение** в правильное **юридическое лицо** в Finance and Operations. В шаблоне фактических данных по проекту (PSA в Fin and Ops) есть столбец условий, определенных на основе демонстрационных данных. Необходимо обновить последний вставленный столбец с условиями с указанием правильных юридических лиц. Несоблюдение этого может привести к ошибке интеграции или неправильным фактическим транзакциям, импортированным в Finance and Operations.
- Если **фактические данные по внутрихолдинговым значениям времени или внутрихолдинговые расходам** не будет синхронизированы с Finance and operations, необходимо удалить последний вставленный столбец с условиями из шаблона. Несоблюдение этого может привести к ошибке интеграции или неправильным фактическим транзакциям, импортированным в Finance and Operations.

### <a name="contract-organizational-unit"></a>Контрактное подразделение
Чтобы обновить вставленный в шаблон столбец с условиями, щелкните стрелку **Сопоставить**, чтобы открыть соответствие. Выберите, чтобы открыть расширенный запрос и фильтрацию
- При использовании шаблона по умолчанию для фактических данных проекта Microsoft (PSA и Fin and Ops) выберите **Вставленное условие** в разделе **Примененные действия**. Выбрав **Функции**, замените **USSI** на имя **Юридическое лицо**, которое должно использоваться при интеграции. Введите дополнительные условия, необходимые для ввода **Функции**, и обновите условие **еще** с условия **USMF** на правильное **Юридическое лицо**.
- При создании нового шаблона необходимо добавить этот столбец для поддержки внутрихолдингового времени и расходов. Выберите **Добавить столбец с условиями** и присвойте столбцу имя, например LegalEntity. Введите условие для столбца где msdyn_contractorganizationalunitid.msdyn_name — это <organizational unit>, а затем <enter the Legal entity>; "еще" равен null.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показан пример соответствия задания шаблона при интеграции данных. Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance and Operations.

[![Соответствие шаблона](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Соответствие шаблона](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Импорт из промежуточной таблицы

Периодический процесс импорта из промежуточной таблицы должен запускаться после синхронизации фактических данных из Project Service Automation в Finance and Operations. Этот процесс импортирует транзакции по проекту из промежуточной таблицы в журнал интеграции Project Service Automation, где применяется учет, и импортированные транзакции могут быть разнесены. Рекомендуется запускать этот процесс в пакетном режиме и при необходимости можно настроить его в виде повторяющегося пакетного задания.

## <a name="update-actuals"></a>Обновление фактических данных

Следующий шаблон и базовые задачи используются для синхронизации номера ваучера и налогов для разнесенных проводок из Project Service Automation в Finance and Operations:

-  **Имя шаблона в интеграции данных:** Обновление фактических данных (Fin Ops и PSA)
-  **Имя задач в проекте:** 
     - Фактические данные 
     - TransactionConnections

## <a name="entity-set"></a>Набор объектов

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| Объект интеграции для фактических данных проекта                         | Фактические данные                           |
| Объект интеграции для связей проводок по проекту       | Связи проводок           |

## <a name="entity-flow"></a>Поток объектов

Фактические данные проекта управляются в Project Service Automation и синхронизируются с Finance and Operations в журнале интеграции проекта. После разноски в Finance and Operations фактические данные обновляются в Project Service Automation с кодом ваучера из Finance and Operations. Если налоги были добавлены в Finance and Operations, в Project Service Automation будут создаваться новые фактические данные по налогу.

## <a name="power-query"></a>Power Query

Необходимо использовать Microsoft Power Query в шаблоне обновления фактических данных проекта:
- Преобразуйте **Тип транзакции** Finance and Operations в правильный **Тип транзакции** в Project Service Automation. Шаблон обновления фактических данных проекта (Fin Ops м PSA) уже имеет определенное преобразование.
- Преобразуйте **Тип выставления счетов** Finance and Operations в правильный **Тип выставления счетов** в Project Service Automation. Шаблон обновления фактических данных проекта (Fin Ops м PSA) уже имеет определенное преобразование.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующих рисунках показаны примеры соответствия задания шаблона при интеграции данных. Соответствие показывает, какие данные полей будут синхронизированы из Finance and Operations в Project Service Automation.

[![Соответствие шаблона](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Соответствие шаблона](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




