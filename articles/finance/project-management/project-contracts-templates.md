---
title: Синхронизация контрактов по проекту и проектов непосредственно из Project Service Automation с Finance and Operations
description: В этой теме обсуждается шаблон и базовые задачи, которые используются для синхронизации контрактов по проекту и проектов непосредственно из Microsoft Dynamics 365 Project Service Automation в Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 76c62f3a503ff2a8c93143390fc91ef81fbf7d0f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250469"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Синхронизация контрактов по проекту и проектов непосредственно из Project Service Automation с Finance and Operations

[!include[banner](../includes/banner.md)]

В этой теме обсуждается шаблон и базовые задачи, которые используются для синхронизации контрактов по проекту и проектов непосредственно из Dynamics 365 Project Service Automation в Dynamics 365 Finance.

> [!NOTE] 
> При использовании Enterprise edition 7.3.0, необходимо установить KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Поток данных для Project Service Automation в Finance

> [!NOTE]
> Прежде чем вы сможете использовать решение интеграции Project Service Automation в Finance, вы должны быть знакомы с функцией интеграции данных Dynamics 365.

Решение по интеграции Project Service Automation с Finance использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance. Шаблон интеграции, доступный с функцией интеграции данных, позволяет передавать данные о контрактах по проекту, проектах, линиях контрактов по проекту и промежуточных этапов строк контракта проекта из Project Service Automation в Finance.

На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance.

[![Поток данных для интеграции Project Service Automation с Finance](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Шаблоны и задачи

Для доступа к доступным шаблонам в центре администрирования Microsoft PowerApps выберите **Проекты** и выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.

Следующие шаблоны и базовые задачи используются для синхронизации контрактов и проектов из Project Service Automation в Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Интеграция с Dynamics 365 Project Service Automation v2.x
- **Имя шаблона в интеграции данных:** Проекты и контракты (PSA в Fin and Ops)
- **Имя задач в проекте:**

    - Контракты по проекту из PSA в Fin and Ops
    - Проекты из PSA в Fin and Ops
    - Строки контракта проекта из PSA в Fin and Ops
    - Промежуточные этапы строки контракта проекта из PSA в Fin and Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Интеграция с Dynamics 365 Project Service Automation v3.x
В Project Service Automation имеется изменение схемы, которое оказывает влияние на шаблон промежуточных этапов строки контракта проекта и использование версии v2 шаблона является необходимым для интеграции Project Service Automation v3.x с Dynamics 365.

- **Имя шаблона в интеграции данных:** Проекты и контракты (PSA 3.x в Fin and Ops) - v2
- **Имя задач в проекте:**

    - Контракты по проекту из PSA в Fin and Ops
    - Проекты из PSA в Fin and Ops
    - Строки контракта проекта из PSA в Fin and Ops
    - Промежуточные этапы строки контракта проекта из PSA в Fin and Ops

Перед синхронизацией контрактов проекта и проектов вы должны синхронизировать учетные записи.

## <a name="entity-set"></a>Набор объектов

| Project Service Automation       | Финансы                                                |
|----------------------------------|--------------------------------------------------------|
| Заказы                           | Объект интеграции для контракта проекта                |
| Проекты                         | Объект интеграции для проекта                         |
| Строки заказа                      | Объект интеграции для строки контракта проекта           |
| Промежуточные этапы строки контракта проекта | Объект интеграции для промежуточного этапа строки контракта проекта |

## <a name="entity-flow"></a>Поток объектов

Контракты проекта управляются в Project Service Automation и синхронизируются с Finance как контракты проекта. В рамках шаблона интеграции вы можете установить источник интеграции в Finance для контракта проекта.

Проект "время и расходы" и проекты с фиксированной ценой управляются в Project Service Automation и синхронизируются с Finance как проекты. В рамках шаблона интеграции вы можете установить источник интеграции в Finance для проекта.

Строки контракта проекта управляются в Project Service Automation и синхронизируются с Finance как правила выставления счетов для контракта проекта. Если метод выставления счетов отличается от типа проекта по умолчанию, синхронизация обновляет тип проекта для проекта строки контракта и группы проектов.

Промежуточные этапы строки контракта проекта управляются в Project Service Automation и синхронизируются с Finance как этапы правил выставления счетов для контракта проекта.

## <a name="project-service-automation-to-finance-integration-solution"></a>Решение для интеграции Project Service Automation в Finance

Поле **Код контракта по проекту** доступно на странице **Контракты по проектам**. Это поле является естественным и уникальным ключом для поддержки интеграции.

При создании контракта по проекту, если значение **Код контракта по проекту** еще не существует, оно создается автоматически с использованием номерной серии. Значение состоит из **ORD**, после чего следует увеличивающая номерная серия и суффикс из шести символов. Рассмотрим пример: **ORD-01022-Z4M9Q0**.

Поле **Номер проекта** доступно на странице **Проекты**. Это поле является естественным и уникальным ключом для поддержки интеграции.

При создании нового проекта, если значение **Номер проекта** еще не существует, оно создается автоматически с использованием номерной серии. Значение состоит из **PRJ**, после чего следует увеличивающая номерная серия и суффикс из шести символов. Рассмотрим пример: **PRJ-01049-CCNID0**.

После применения решения интеграции Project Service Automation в Finance, сценария обновления задает поле **Код контракта по проекту** для существующих контрактов по проекту и поле **Номер проекта для проектов**, существующих в Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления

- Перед синхронизацией контрактов проекта и проектов вы должны синхронизировать учетные записи.
- При подключении добавить соответствие ключевого поля интеграции для **msdyn\_organizationalunits** в **msdyn\_имя \[Имя\]**. Сначала может потребоваться добавить проекты в набор подключения. Дополнительные сведения см. в разделе [Интеграция данных в Common Data Service для приложений](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- При подключении добавить соответствие ключевого поля интеграции для **msdyn\_projects** в **msdynce\_projectnumber \[Project Number\]**. Сначала может потребоваться добавить проекты в набор подключения. Дополнительные сведения см. в разделе [Интеграция данных в Common Data Service для приложений](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** для контрактов по проекту и проектов могут быть обновлены на другое значение или удалены из соответствия. Шаблон по умолчанию — **Project Service Automation**.
- Соответствие **PaymentTerms** должно быть обновлено, чтобы соответствовать допустимым условиям оплаты в Finance. Можно также удалить соответствии из задачи проекта. Значение по умолчанию имеет значения по умолчанию для демонстрационных данных. Следующая таблица показывает значения в Project Service Automation.

    | Стоимость | описание   |
    |-------|---------------|
    | 1     | Сальдо 30        |
    | 2     | 2% 10, Чистые 30 |
    | 3     | Сальдо 45        |
    | 4     | Сальдо 60        |

## <a name="power-query"></a>Power Query

Необходимо использовать Microsoft Power Query для Excel для фильтрации данных при соблюдении следующих условий:

- У вас есть заказы на продажу в Dynamics 365 Sales.
- У вас есть несколько подразделений в Project Service Automation, и эти подразделения соответствуют несколько юридических лиц в Finance.

При использовании Power Query необходимо выполните следующее:

- В шаблоне проектов и контрактов (PSA в Fin and Ops) имеется фильтр по умолчанию, который включает только заказы на продажу типа **Рабочий элемент (msdyn\_ordertype = 192350001)**. Этот фильтр помогает гарантировать, чтобы контракты по проектам не создавались для заказов на продажу в Finance. При создании собственного шаблона, необходимо добавить этот фильтр.
- Необходимо создать фильтр Power Query, который содержит только контрактные организации, которые должны быть синхронизированы с набором подключения интеграции к юридическому лицу. Например должны быть синхронизированы контракты с контрактными подразделениями Contoso US, которые должны быть синхронизированы с юридическим лицом USSI, однако контракты по проекту, заключенные с подразделениями Contoso Global, должны быть синхронизированы с юридическом лицом USMF. Если не добавить этот фильтр для ваших задач сопоставления, все контракты по проекту будут синхронизированы с юридическим лицом, определенным для набора подключения вне зависимости от контрактного подразделения.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

> [!NOTE] 
> Поля **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, и **AddressZipCode** не включаются в соответствие по умолчанию для контрактов по проекту. Если требуется синхронизация этих данных для контрактов по проекту можно добавить соответствия.
>
> Поля **Описание**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** и **ProjectType** не включаются в соответствие по умолчанию для проектов. Если требуется синхронизация этих данных для проектов можно добавить соответствия.

На следующих рисунках показаны примеры соответствия задания шаблона при интеграции данных. Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance.

[![Соответствие шаблона](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Соответствие шаблона](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Соответствие шаблона](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Соответствие шаблона](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Шаблон сопоставления промежуточных этапов строки контракта проекта в проектах и контрактах (PSA 3.x в Dynamics) - v2:

[![Соответствие шаблона](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
