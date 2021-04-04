---
title: Предварительная версия Dynamics 365 Supply Chain Management 10.0.17 (апрель 2021)
description: В этой теме описываются новые и измененные компоненты Dynamics 365 Supply Chain Management 10.0.17.
author: kamaybac
manager: annbe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 985879ef765bf3074387a909d508f0f93a4771ed
ms.sourcegitcommit: d7c18228256daeefbf6518c3ef82fed4f7dbc161
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571820"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10017-april-2021"></a>Предварительная версия Dynamics 365 Supply Chain Management 10.0.17 (апрель 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

В этой теме перечислены новые и измененные компоненты предварительной версии Microsoft Dynamics 365 Supply Chain Management выпуска 10.0.17. Эта версия имеет номер сборки 10.0.761 и доступна следующим образом:

- **Предварительная версия**: февраль 2021 года
- **Общая доступность выпуска (самостоятельное обновление):** март 2021 года
- **Общая доступность выпуска (автоматическое обновление):** апрель 2021 года

## <a name="features-included-in-this-release"></a>Возможности, включенные в данный выпуск

Этот выпуск содержит следующие функции. Некоторые из вышеперечисленных функций все еще являются предварительными версиями, в то время как другие могут уже быть общедоступными. Перейдите по ссылке на [план выпуска](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), чтобы просмотреть официальные даты выпуска для каждой функции.

Большая часть этих функций должна быть включена с помощью [Управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), прежде чем их можно будет использовать.

### <a name="asset-management"></a>Управление активами

- [Применение правил группировки заказов на работу во время выполнения плана обслуживания](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/apply-rules-grouping-work-orders-while-running-maintenance-plan)<br> - Дополнительные сведения см. в разделе [Создание заказов на работу](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md).

- [Выставление счетов клиентам за работы по обслуживанию](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/bill-customers-maintenance-work)<br> - Дополнительные сведения см. в разделе [Выставление счетов за обслуживание активов, принадлежащих клиенту](../asset-management/integration-to-project-management-and-accounting/customer-billing.md).

- [Планирование обслуживания на основе накопленных значений счетчика актива](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/plan-maintenance-based-accumulated-asset-counter-values)<br> - Дополнительные сведения см. в разделе [Планы обслуживания](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md).

### <a name="inventory-and-logistics"></a>Запасы и логистика

- [Интеграционная структура для оборудования обработки материалов для автоматизированных складских процессов (ранее MHAX)](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/integration-framework-material-handling-equipment-automated-warehouse-processes-previously-mhax)<br> - Дополнительные сведения см. в разделе [Интерфейс транспортно-складского оборудования (MHAX)](../warehousing/mhax.md).

- [Стоимость на складе](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/landed-cost)<br> - Дополнительные сведения см в разделе [Модуль "Стоимость на складе"](../landed-cost/landed-cost-overview.md).

- [Аналитики упаковки и хранения](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/packing-vs.-storage-dimensions)<br> - Дополнительные сведения см. в разделе [Настройка различных аналитик для упаковки и хранения](../warehousing/packing-vs-storage-dimensions.md).

- [Сохраненные представления для запасов и логистики](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-inventory-logistics)<br> - Дополнительные сведения см. в разделе [Стандартные сохраненные представления для Supply Chain Management](saved-views-scm.md).

- [Планирование создания складских работ](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-warehouse-work-creation)<br> - Дополнительные сведения см. в разделе [Планирование создания работы во время волны](../warehousing/configure-wave-schedule-work-creation.md).

- [Задание финансовых аналитик по умолчанию для операций переоценки стандартной себестоимости запасов](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/set-default-financial-dimensions-inventory-standard-cost-revaluation-vouchers)<br> - Дополнительные сведения см. в разделе [Управление обновлениями стандартных затрат](../cost-management/manage-standard-cost-updates.md).

- [Отгрузка небольших посылок (SPS)](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/small-parcel-shipping-sps)<br> - Дополнительные сведения см. в разделе [Отгрузка небольших посылок](../warehousing/small-parcel-shipping.md).

- [Выполнение склада с единицами масштабирования в облаке](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-scale-units-cloud)<br> - Дополнительные сведения см. в разделах [Рабочие нагрузки управления складом для облачных и пограничных единиц масштабирования](../cloud-edge/cloud-edge-workload-warehousing.md) и [Заказы склада для облачных и пограничных единиц масштабирования](../cloud-edge/cloud-edge-warehouse-order.md).

- [Мобильное приложение управления складом](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application)<br> - Дополнительные сведения см. в разделах [Установка и подключение приложения управления складом](../warehousing/install-configure-warehouse-management-app.md) и [Пользовательские параметры мобильного устройства](../warehousing/mobile-device-user-settings.md).

### <a name="manufacturing"></a>Производство

- [Функции управления активами в интерфейсе выполнения производственного цеха](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/asset-management-capabilities-production-floor-execution-interface)<br> - Дополнительные сведения см. в разделе [Как работники используют интерфейс выполнения производственного цеха](../production-control/production-floor-execution-use.md).

- [Переопределение принципа резервирования по умолчанию для материалов в производстве](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/override-default-reservation-principle-materials-production)<br> - Дополнительные сведения см. в разделе [Переопределение принципа резервирования по умолчанию для материалов в производстве](../production-control/override-default-reservation-principle.md).

- [Сохраненные представления для управления производством](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-production-control)<br> - Дополнительные сведения см. в разделе [Стандартные сохраненные представления для Supply Chain Management](saved-views-scm.md).

- [Выполнение производства с единицами масштабирования в облаке](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-scale-units-cloud)<br> - Дополнительные сведения см. в разделе [Производственные рабочие нагрузки для облачных и пограничных единиц масштабирования](../cloud-edge/cloud-edge-workload-manufacturing.md).

### <a name="planning"></a>Планирование

- [Поддержка временных границ покрытия для оптимизации планирования](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/coverage-time-fence-support-planning-optimization)<br> - Дополнительные сведения см. в разделе [Временные границы покрытия](../master-planning/planning-optimization/coverage-time-fence.md).

- [Поддержка подмоделей прогноза для оптимизации планирования](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/forecast-submodel-support-planning-optimization)<br> - Для получения дополнительных сведений см. [Сводное планирование с прогнозами спроса](../master-planning/planning-optimization/demand-forecast.md).

- [Поддержка заявок на закупку для оптимизации планирования](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/purchase-requisition-support-planning-optimization)<br> - Дополнительные сведения см. в разделе [Заявки на закупку](../master-planning/planning-optimization/purchase-requisitions.md).

- [Сохраненные представления для спланированных заказов](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-planned-orders)<br> - Дополнительные сведения см. в разделе [Стандартные сохраненные представления для Supply Chain Management](saved-views-scm.md).

### <a name="product-information-management"></a>Управление сведениями о продукте

- [Включить управление изменениями для существующих продуктов](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enable-change-management-existing-products)<br> - Дополнительные сведения см. в разделе [Включить управление изменениями для существующих продуктов](../engineering-change-management/change-management-existing-products.md).

## <a name="new-and-updated-documentation-resources"></a>Новые и обновленные ресурсы документации

Недавно были добавлены или существенно обновлены следующие разделы справки. Они не обязательно связаны с новыми функциями, добавленными для данного выпуска, как это перечислено в предыдущем разделе, но они могут помочь эффективнее использовать существующие функции.

### <a name="cost-management"></a>Управление затратами

- [Устранение неполадок при управлении затратами](../cost-management/troubleshoot-costmanagement.md)

### <a name="asset-management"></a>Управление активами

- [Настройка мобильной рабочей области управления активами](../asset-management/set-up-asset-management-mobile.md)

### <a name="inventory-and-logistics"></a>Запасы и логистика

- [Настройка фильтров продуктов для складских проводок](../warehousing/filters-and-filter-codes.md)

- [Частичный цикличный подсчет по ячейкам](../warehousing/partial-location-cycle-counting.md)

- [Группировка строк комплектации](../warehousing/pick-line-grouping.md)

- [Устранение неполадок операций с запасами](../inventory/troubleshoot-inventory-operations.md)

- [Слоттинг на складе](../warehousing/warehouse-slotting.md)

### <a name="manufacturing"></a>Производство

- [Разработка интерфейса выполнения производственного цеха](../production-control/production-floor-execution-tabs.md)

### <a name="planning"></a>Планирование

- [Внутрихолдинговое планирование](../master-planning/planning-optimization/Intercompany-planning.md)

- [Маркировка запасов с оптимизацией планирования](../master-planning/planning-optimization/marking.md)

- [Планирование производства](../master-planning/planning-optimization/production-planning.md)

- [Заявки на закупку в сводном планировании](../master-planning/planning-optimization/purchase-requisitions.md)

## <a name="additional-resources"></a>Дополнительные ресурсы

### <a name="platform-updates-for-finance-and-operations-apps"></a>Обновления платформы для приложений Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.17 включает обновления платформы. Дополнительные сведения см. в разделе [Обновления платформы для версии 10.0.17 приложений Finance and Operations (апрель 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md).

### <a name="bug-fixes"></a>Исправления ошибок

Для получения сведений об исправлениях ошибок, включенных в каждое из обновлений, которые являются частью 10.0.17, войдите в службы Lifecycle Services (LCS) и просмотрите [статью базы знаний](https://fix.lcs.dynamics.com/Issue/Details?bugId=551039&dbType=3&qc=91219e7c3fc585acb17b810c915c3cbea499403538520c40e54de43a53aea6a8).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: план выпуска волны 1 за 2021 год

Интересуетесь предстоящими и недавно выпущенными возможностями наших бизнес-приложений и платформ?

Ознакомьтесь с разделом [Dynamics 365: план выпуска волны 1 за 2021 год](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/). Мы собрали в одном документе все сведения, чтобы вы могли использовать их для планирования.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Удаленные и устаревшие функции Supply Chain Management

В теме [Удаленные или устаревшие функции в Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) описываются функции, которые запланированы к удалению или которые планируется удалить или объявить устаревшими для Supply Chain Management.

- *Удаленная* функция больше недоступна в продукте.
- *Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.

Перед удалением каких-либо функций из продукта уведомление об устаревании будет объявлено в теме [Удаленные или устаревшие функции в Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) за 12 месяцев до удаления.

Для критических изменений, которые влияют только на время компиляции, но являются двоично совместимыми с песочницей и производственными средами, время устаревания будет меньше 12 месяцев. Обычно это функциональные обновления, которые должны быть выполнены для компилятора.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]