---
title: "Отчет о движении основных средств"
description: "В этом разделе описывается использование отчета о движении основных средств."
author: saraschi2
manager: 
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 8075abccdcdde21df967dcc9948a738895f35cef
ms.openlocfilehash: 0a78df4ede8fd57afbc3e9a7e5a38b840f479cdf
ms.contentlocale: ru-ru
ms.lasthandoff: 01/25/2018

---
# <a name="fixed-assets-roll-forward-report"></a>Отчет о движении основных средств

[!include[banner](../includes/banner.md)]

Отчет **Движение основных средств** предоставляет в удобном для восприятии формате Microsoft Excel подробные данные об основных средствах, которые могут потребоваться для закрытия периода, финансовых отчетов и налоговой отчетности. Отчет включает в себя начальное и конечное сальдо для основных средств, вместе с изменениями оценки для периода, а также все новые приобретения и выбытия активов, произошедшие во время периода. Данные собираются для отдельных основных средств, а также приводятся сводные значения для групп основных средств и юридического лица.

Отчет **Движение основных средств** использует инфраструктуру электронной отчетности (ER). Перед запуском отчета модель основных средств и конфигурации движения основных средств должны быть импортированы из Microsoft Dynamics Lifecycle Services (LCS). Инструкции см. в разделе [Загрузка конфигураций электронной отчетности из Lifecycle Services](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Этот отчет доступен в Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3, или в качестве исправления для Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.). Три исправления должно применяться для сред, в которых установлена версия от июля 2017 г.:

- **KB 4041754:** конфигурацию электронной отчетности (ER) не удается загрузить из LCS как неприменимую для текущей версии приложения после применения пакета обновления платформы
- **KB 4056107:** накопительное обновление электронной отчетности (GER) номер 5
- **KB 4056353:** отчеты о выписке по основным средствам и примечаниям не соответствуют требованиям, приведенным в GAAP и IFRS

В следующей таблице описываются поля, которые доступны в отчете.

| Поле                                       | описание |
|---------------------------------------------|-------------|
| Сальдо: входящее                           | Остаточная стоимость основных средств на дату "от", указанную в отчете. |
| Сальдо: исходящее                           | Остаточная стоимость основных средств на дату "до", указанную в отчете. |
| Приобретение: значение на начало периода                 | Сумма по всем проводкам типов **Приобретение** и **Корректировка стоимости приобретения** вплоть до даты "от", указанной в отчете. |
| Приобретение: приобретения за период           | Сумма по всем проводкам типов **Приобретение** и **Корректировка стоимости приобретения**, которые были разнесены за период отчета. |
| Приобретение: выбытие за период              | Сумма по всем разнесенным проводкам сторнирования приобретения, которые имеют проводки выбытия за период отчета. |
| Приобретение: значение на конец периода                 | Сумма по всем проводкам типов **Приобретение** и **Корректировка стоимости приобретения** вплоть до даты "по", указанной в отчете. |
| Амортизация: значение на начало периода                | Сумма по всем проводкам типов **Амортизация**, **Корректировка амортизации**, **Амортизационная премия** и **Дополнительная амортизация** до даты "от", указанной в отчете. |
| Амортизация: амортизация за период         | Сумма по всем проводкам типов **Амортизация**, **Корректировка амортизации** и **Дополнительная амортизация**, которые были разнесены за период отчета. |
| Амортизация: специальная амортизация за период | Сумма по всем проводкам типа **Амортизационная премия**, которые были разнесены за период отчета. |
| Амортизация: выбытие за период             | Сумма по всем разнесенным проводкам сторнирования амортизации, которые имеют проводки выбытия за период отчета. |
| Амортизации: на конец периода                | Сумма по всем проводкам типов **Амортизация**, **Корректировка амортизации**, **Амортизационная премия** и **Дополнительная амортизация** до даты "по", указанной в отчете. |
| Увеличение/уменьшение балансовой стоимости: значение на начало периода        | Сумма по всем проводкам типов **Увеличение балансовой стоимости**, **Уменьшение балансовой стоимости** и **Переоценка** вплоть до даты "от", указанной в отчете. |
| Увеличение/уменьшение балансовой стоимости: увеличение балансовой стоимости за период     | Сумма по всем проводкам типа **Увеличение балансовой стоимости**, которые были разнесены за период отчета. |
| Увеличение/уменьшение балансовой стоимости: уменьшение балансовой стоимости за период   | Сумма по всем проводкам типа **Уменьшение балансовой стоимости**, которые были разнесены за период отчета. |
| Увеличение/уменьшение балансовой стоимости: переоценка за период  | Сумма по всем проводкам типа **Переоценка**, которые были разнесены за период отчета. |
| Увеличение/уменьшение балансовой стоимости: выбытие за период     | Сумма по всем разнесенным проводкам сторнирования увеличения балансовой стоимости, уменьшения балансовой стоимости и переоценки, которые имеют проводки выбытия за период отчета. |
| Увеличение/уменьшение балансовой стоимости: значение на конец периода        | Сумма по всем проводкам типов **Увеличение балансовой стоимости**, **Уменьшение балансовой стоимости** и **Переоценка** вплоть до даты "по", указанной в отчете. |
| Выбытие: дата выбытия                    | Дата выбытия для журнала основных средств. |
| Выбытие: остаточная стоимость на момент выбытия       | Остаточная стоимость по журналу ОС на момент выбытия. |
| Выбытие: стоимость продажи                       | Сумма продажи для журнала основных средств с выбытием — проводка продажи. |
| Выбытие: ликвидационная стоимость                      | Ликвидационная стоимость для журнала основных средств с выбытием — проводка ликвидации. |
| Выбытие: прибыль/убыток                      | Сумма прибыли или убытка, которая вычисляется как часть проводки выбытия для журнала основных средств. |
