---
title: Предварительная версия Dynamics 365 Supply Chain Management 10.0.19 (июль 2021 г.)
description: В этой теме описываются новые и измененные компоненты Dynamics 365 Supply Chain Management 10.0.19.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8bb4a7c8085b40ab3eca72675dbe7a3be412d8c1
ms.sourcegitcommit: 2eb7a9ae544f504155657c5c584cbac66c21dba4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2021
ms.locfileid: "5961689"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10019-july-2021"></a>Предварительная версия Dynamics 365 Supply Chain Management 10.0.19 (июль 2021 г.)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

В этой теме перечислены новые и измененные компоненты предварительной версии Microsoft Dynamics 365 Supply Chain Management выпуска 10.0.19. Эта версия имеет номер сборки 10.0.837 и доступна следующим образом:

- **Выпуск предварительной версии:** апрель 2021 г.
- **Общая доступность выпуска (самостоятельное обновление):** июнь 2021 г.
- **Общая доступность выпуска (автоматическое обновление):** июль 2021 года

## <a name="features-included-in-this-release"></a>Возможности, включенные в данный выпуск

В этой таблице перечислены функции в выпуске. Столбец *Функция* содержит ссылки на [план выпуска](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), где можно просмотреть официальные даты выпуска каждой функции. В столбце *Дополнительные сведения* представлены ссылки на сопутствующую документацию.

Большая часть этих функций должна быть включена с помощью [Управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), прежде чем их можно будет использовать. Некоторые из вышеперечисленных функций все еще являются предварительными версиями, в то время как другие могут уже быть общедоступными.

| Область компонентов | Функция | Дополнительные сведения |
|---|---|---|
| Запасы и логистика | [Оптимизация экспорта информационного объекта контактного лица](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | *Недоступно* |
| Запасы и логистика | [Постепенные усовершенствования для возможностей выполнения задач склада с единицами масштабирования](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Сообщения обработчика сообщений](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Корректировка запасов склада](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Рабочие нагрузки управления складом для облачных и пограничных единиц масштабирования](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Запасы и логистика | [Функции поиска для полей введения к документу и подписи к документу на странице предложения по продажам](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | *Недоступно* |
| Запасы и логистика | [Выполнение склада с пограничными единицами масштабирования на настраиваемом оборудовании](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Развертывание пограничных единиц измерения на настраиваемом оборудовании с помощью LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Производство | [Выполнение производства с пограничными единицами масштабирования на настраиваемом оборудовании](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Развертывание пограничных единиц измерения на настраиваемом оборудовании с помощью LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Планирование | Подтверждение спланированного заказа на основе запроса | [Утверждение спланированных заказов](../master-planning/planning-optimization/planned-order-firming.md) |
| Управление сведениями о продукте | [Улучшения страницы предложений вариантов](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Создание заранее определенных вариантов продукта](../pim/tasks/create-predefined-product-variants.md) |

## <a name="new-and-updated-documentation-resources"></a>Новые и обновленные ресурсы документации

Недавно были добавлены или существенно обновлены следующие разделы справки. Они не обязательно связаны с новыми функциями, добавленными для данного выпуска, как это перечислено в предыдущем разделе, но они могут помочь эффективнее использовать существующие функции.

| Область компонентов | Новые или обновленные темы |
|---|---|
| Управление изменениями разработки | [Вопросы и ответы по управлению изменениями разработки](../engineering-change-management/change-management-faq.md) |
| Закупки и источники | [Управление запросами на категорию от поставщиков](../procurement/category-requests-from-vendors.md) |
| Управление сведениями о продукте | [Управление единицей измерения](../pim/tasks/manage-unit-measure.md)<br><br>[Расчеты модели конфигурации продукта](../pim/config-model-calculations.md) |
| Управление производством | [Единая номерная серия для кодов заданий](../production-control/unified-job-ids.md) |
| Управление транспортировкой | [Классы LTL](../transportation/ltl-class.md)<br><br>[Коды NMFC](../transportation/nmfc-codes.md) |
| Управление складом | [Устранение неполадок в иерархиях складских партий и последовательного резервирования](../warehousing/troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) |
| Управление складом, создание и обработка волн | [Создание и обработка волны](../warehousing/wave-processing.md)<br><br>[Параметры склада для обработки волны](../warehousing/wave-warehouse-parameters.md)<br><br>[Шаблоны волны](../warehousing/wave-templates.md)<br><br>[Распределение волны](../warehousing/wave-allocation-method.md)<br><br>[Планирование создания работы во время волны](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Контейнеризация](../warehousing/wave-containerization.md)<br><br>[Уведомления о выполнении волны](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Дополнительные ресурсы

### <a name="platform-updates-for-finance-and-operations-apps"></a>Обновления платформы для приложений Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.19 включает обновления платформы. Дополнительные сведения см. в разделе [Обновления платформы для версии 10.0.19 приложений Finance and Operations (июль 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Исправления ошибок

Для получения сведений об исправлениях ошибок, включенных в каждое из обновлений, которые являются частью 10.0.19, войдите в службы Lifecycle Services (LCS) и просмотрите [статью базы знаний](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: план выпуска волны 1 за 2021 год

Интересуетесь предстоящими и недавно выпущенными возможностями наших бизнес-приложений и платформ?

Ознакомьтесь с разделом [Dynamics 365: план выпуска волны 1 за 2021 год](/dynamics365-release-plan/2021wave1/). Мы собрали в одном документе все сведения, чтобы вы могли использовать их для планирования.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Удаленные и устаревшие функции Supply Chain Management

В теме [Удаленные или устаревшие функции в Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) описываются функции, которые запланированы к удалению или которые планируется удалить или объявить устаревшими для Supply Chain Management.

- *Удаленная* функция больше недоступна в продукте.
- *Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.

Перед удалением каких-либо функций из продукта уведомление об устаревании будет объявлено в теме [Удаленные или устаревшие функции в Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) за 12 месяцев до удаления.

Для критических изменений, которые влияют только на время компиляции, но являются двоично совместимыми с песочницей и производственными средами, время устаревания будет меньше 12 месяцев. Обычно это функциональные обновления, которые должны быть выполнены для компилятора.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
