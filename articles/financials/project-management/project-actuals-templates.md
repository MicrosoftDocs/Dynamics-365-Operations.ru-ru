---
title: Синхронизировать фактические данные проекта непосредственно из Project Service Automation в журнал интеграции проекта для разноски в Finance and Operations
description: В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации фактических данных проекта непосредственно из Microsoft Dynamics 365 for Project Service Automation в Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0a965e8de596decf39a15977e6df8a6aa9dd35b0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "343359"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Синхронизировать фактические данные проекта непосредственно из Project Service Automation в журнал интеграции проекта для разноски в Finance and Operations

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации фактических данных проекта непосредственно из Microsoft Dynamics 365 for Project Service Automation в Microsoft Dynamics 365 for Finance and Operations.

Шаблон синхронизирует транзакции из Project Service Automation в промежуточную таблицу в Finance and Operations. После завершения синхронизации **необходимо** импортировать данные из промежуточной таблицы в журнал интеграции.

> [!NOTE]
> - Интеграция фактических данных проекта доступна в Microsoft Dynamics 365 for Finance and Operations версии 8.0.1 или новее.
> - При использовании Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, после установки обновлений КБ 4132657 и 4132660 КБ, можно использовать шаблоны для интеграции задачи проекта, категорий транзакций расходов, оценок часов, оценок расходов и фактических данных и для настройки функции блокировки. Если необходимо сбросить распределения по бухгалтерским счетам, рекомендуется также установить КБ 4131710.
> - Если при использовании Finance and Operations 7.3.0 вы переносите проводки по сборам из Project Service Automation, чтобы включить эти расходы в накладную проекта необходимо установить KB 4345320.
> - При своевременном вводе суммы налога или проводок расходов в Project Service Automation необходимо установить Project Service Automation Update 7. В противном случае фактические данные налога не будут связаны с ассоциированным временем или фактическими данными о расходах, и они не будут синхронизированы с Finance and Operations. Для получения дополнительных сведений обратитесь в службу поддержки.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Поток данных для Project Service Automation для Finance and Operations

Решение по интеграции Project Service Automation в Finance and Operations использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance and Operations. Шаблоны интеграции, доступные при использовании функции интеграции данных, включают поток данных по фактическим данным проекта из Project Service Automation в Finance and Operations.

На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance and Operations.

[![Поток данных для интеграции Project Service Automation с Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Фактические данные по проекту из Project Service Automation

### <a name="template-and-tasks"></a>Шаблон и задачи

Для доступа к доступным шаблонам в центре администрирования Microsoft PowerApps выберите **Проекты** и выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.

Следующий шаблон и базовые задачи используются для синхронизации фактических данных по проект из Project Service Automation в Finance and Operations:

- **Имя шаблона в интеграции данных:** Фактические данные по проекту (PSA в Fin and Ops)
- **Имя задач в проекте:**

    - Фактические данные
    - TransactionConnections

### <a name="entity-set"></a>Набор объектов

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Фактические данные                    | Объект интеграции для фактических данных проекта                   |
| Связи проводок    | Объект интеграции для связей проводок по проекту |

### <a name="entity-flow"></a>Поток объектов

Фактические данные проекта управляются в Project Service Automation и синхронизируются с журналом интеграции проекта в Finance and Operations. Учет применяется на основе финансовых аналитик по умолчанию и настройки разноски.

### <a name="prerequisites"></a>Необходимые условия

Прежде чем произойдет синхронизация фактических данных, необходимо настроить параметры интеграции Project Service Automation и синхронизировать проекты, задачи по проекту и категории транзакции расходов для проекта.

### <a name="power-query"></a>Power Query

В шаблоне фактических данных по проекту необходимо использовать Microsoft Power Query для Excel для выполнения следующих задач:

- Преобразование типа транзакции в Project Service Automation в правильный тип транзакции в Finance and Operations. Это преобразование уже определено в шаблоне фактических данных проекта (PSA и Fin and Ops).
- Преобразуйте тип выставления счетов в Project Service Automation в правильный тип выставления счетов в Finance and Operations. Это преобразование уже определено в шаблоне фактических данных проекта (PSA и Fin and Ops). Тип выставления счетов сопоставляется со свойством строки на основе конфигурации на странице **Параметры интеграции Project Service Automation**.
- Отфильтруйте определенные подразделения ресурсов, которые должны быть синхронизированы с помощью этого шаблона.
- Если фактические данные по внутрихолдинговым значениям времени или внутрихолдинговые расходам будут синхронизированы с Finance and Operations, следует преобразовать контрактное подразделение в правильное юридическое лицо в Finance and Operations. В шаблоне фактических данных по проекту (PSA в Fin and Ops) определен столбец условий на основе демонстрационных данных. Необходимо обновить последний вставленный столбец с условиями с указанием правильных юридических лиц. В противном случае может произойти ошибка интеграции или неправильные фактические транзакции могут быть импортированы в Finance and Operations.
- Если фактические данные по внутрихолдинговым значениям времени или внутрихолдинговые расходам не будет синхронизированы с Finance and operations, необходимо удалить последний вставленный столбец с условиями из шаблона. В противном случае может произойти ошибка интеграции или неправильные фактические транзакции могут быть импортированы в Finance and Operations.

#### <a name="contract-organizational-unit"></a>Контрактное подразделение
Чтобы обновить вставленный в шаблон столбец с условиями, щелкните стрелку **Сопоставить**, чтобы открыть соответствие. Выберите ссылку **Расширенный запрос и фильтрация**, чтобы открыть Power Query.

- При использовании шаблона по умолчанию для фактических данных проекта (PSA и Fin and Ops) в Power Query выберите последнее **Вставленное условие** из раздела **Примененные действия**. В записи **Функция** замените **USSI** на имя юридического лица, которое должно использоваться при интеграции. Введите требуемые дополнительные условия в запись **Функция** и обновите условие **else** из **USMF** на правильное юридическое лицо.
- При создании нового шаблона необходимо добавить этот столбец для поддержки внутрихолдингового времени и расходов. Выберите **Добавить столбец с условиями** и введите имя для столбца, например **LegalEntity**. Введите условие для столбца, где если **msdyn\_contractorganizationalunitid.msdyn\_name** является \<организационным подразделением\>, то \<введите юридическое лицо\>; в противном случае значение null.

### <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующих рисунках показан пример соответствия задания шаблона при интеграции данных. Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance and Operations.

[![Соответствие шаблона](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Соответствие шаблона](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Импорт из промежуточной таблицы после интеграции из Project Service Automation

Периодический процесс импорта из промежуточной таблицы должен запускаться после синхронизации фактических данных из Project Service Automation в Finance and Operations. Этот процесс импортирует транзакции по проекту из промежуточной таблицы в журнал интеграции Project Service Automation, где применяется учет, и импортированные транзакции могут быть разнесены. Рекомендуется запускать этот процесс в пакетном режиме и при необходимости можно настроить его в виде повторяющегося пакетного задания.

## <a name="update-actuals-from-finance-and-operations"></a>Обновление фактических данных из Finance and Operations

### <a name="template-and-tasks"></a>Шаблон и задачи

Следующий шаблон и базовые задачи используются для синхронизации номера ваучера и налогов для разнесенных проводок из Project Service Automation в Finance and Operations:

- **Имя шаблона в интеграции данных:** Обновление фактических данных (Fin Ops и PSA)
- **Имя задач в проекте:**

    - Фактические данные 
    - TransactionConnections

### <a name="entity-set"></a>Набор объектов

| Finance and Operations                                   | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Объект интеграции для фактических данных проекта                   | Фактические данные                    |
| Объект интеграции для связей проводок по проекту | Связи проводок    |

### <a name="entity-flow"></a>Поток объектов

Фактические данные проекта управляются в Project Service Automation и синхронизируются с журналом интеграции проекта в Finance and Operations. После разноски фактических данных в Finance and Operations они обновляются в Project Service Automation с кодом ваучера из Finance and Operations. Если налоги были добавлены в Finance and Operations, в Project Service Automation создаются новые фактические данные по налогу.

### <a name="power-query"></a>Power Query

В шаблоне обновления фактических данных по проекту необходимо использовать Power Query для выполнения следующих задач:

- Преобразование типа транзакции в Finance and Operations в правильный тип транзакции в Project Service Automation. Это преобразование уже определено в шаблоне обновления фактических данных проекта (PSA и Fin and Ops).
- Преобразуйте тип выставления счетов в Finance and Operations в правильный тип выставления счетов в Project Service Automation. Это преобразование уже определено в шаблоне обновления фактических данных проекта (PSA и Fin and Ops).

### <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующих рисунках показаны примеры соответствия задания шаблона при интеграции данных. Соответствие показывает, какие данные полей будут синхронизированы из Finance and Operations в Project Service Automation.

[![Соответствие шаблона](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Соответствие шаблона](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
