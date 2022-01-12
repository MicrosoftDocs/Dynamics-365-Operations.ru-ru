---
title: Предварительная версия Dynamics 365 Supply Chain Management 10.0.24 (февраль 2022 года)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Supply Chain Management 10.0.24.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f6402d7f9f433ca621c475bd62553529943dbe62
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920556"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10024-february-2022"></a>Предварительная версия Dynamics 365 Supply Chain Management 10.0.24 (февраль 2022 года)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

В этой теме перечислены новые и измененные компоненты предварительной версии Microsoft Dynamics 365 Supply Chain Management выпуска 10.0.24. Эта версия имеет номер сборки 10.0.1084 и доступна следующим образом:

- **Предварительная версия**: декабрь 2021 г.
- **Общая доступность выпуска (самостоятельное обновление):** январь 2022 г.
- **Общая доступность выпуска (автоматическое обновление):** февраль 2022 г.

## <a name="features-included-in-this-release"></a>Возможности, включенные в данный выпуск

В этой таблице перечислены функции в выпуске. Можно обновить этот раздел для включения функций, которые были сделаны в сборке после первоначальной публикации этого раздела.

| Область компонентов | Функция | Дополнительные сведения | Включено пользователем   |
|---|---|---|---|
| Распределенная гибридная топология | [Улучшенные рабочие нагрузки выполнения склада на единицах масштабирования](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Рабочие нагрузки управления складом для облачных и пограничных единиц масштабирования](../cloud-edge/cloud-edge-workload-warehousing.md) | Включено по умолчанию. |
| Планирование | [Поддержка оптимизации планирования резерва заказа и резервного времени для отпуска](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Резервное время](../master-planning/planning-optimization/safety-margins.md) | Включено по умолчанию. |

## <a name="feature-enhancements-included-in-this-release"></a>Улучшения функций, включенные в данный выпуск

В этой таблице перечислены улучшения функций, включенные в этот выпуск. Каждая из них обеспечивает дополнительное усовершенствование существующей функции. Поскольку они только улучшения, они не перечисляются в [плане выпуска](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Однако чтобы гарантировать, что эти улучшения не будут конфликтовать с существующими настройками или предпочтениями, каждое из них отключена по умолчанию (если не указано иное).

Если вы хотите включить или отключить какие-либо из этих функций, необходимо сделать это в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Модуль | Имя функции в управлении функциями | Дополнительные сведения |
|---|---|---|
| Управление производством | Проверка доступности материалов по запросу для производственных заказов | Эта функция ускоряет открытие страницы **Производственные заказы для выпуска**, которая доступна в рабочей области **Управление производственным участком**. Без этой функции система автоматически проверяет доступность материалов для всех перечисленных производственных заказов при открытии страницы, что может занять значительное время, если имеется большое количество заказов. Если эта функция включена, в системе вместо этого будет предусмотрена кнопка на панели инструментов, которая позволяет начать проверку материалов только для выбранных заказов и при необходимости. |
| Управление производством | (Предварительная версия) Регистрация потребления материалов в интерфейсе выполнения производственного цеха (без службы управления рабочими процессами) | Эта функция позволяет сотрудникам использовать интерфейс выполнения производственного цеха для регистрации потребления материалов, номеров партий и серийных номеров. Эта функция поддерживает только номенклатуры, для которых не включено использование расширенных складских процессов (WMS). Поддержка номенклатур с поддержкой WMS планируется для будущего выпуска.<p>Некоторые производители, особенно в перерабатывающих отраслях, должны явным образом регистрировать количество материала, потребляемое для каждого партии или производственного заказа. Например, работники могут использовать весы для того, чтобы взвесить количество потребленного материала по мере их работы. Чтобы обеспечить полную трассировку материалов, в этих организациях также необходимо регистрировать номера партий, потребляемых при производстве каждого продукта. |
| Управление производством | Приемка рабочей нагрузки управления складом для облачных и пограничных единиц масштабирования | Эта функция позволяет работникам использовать мобильное приложение Warehouse Management, чтобы сообщить о завершении производственного заказа или заказа партии, когда приложение запущено для рабочей нагрузки управления складом в облачной или пограничной единице масштабирования. Дополнительные сведения см. в разделе [Приемка и размещение в единице масштабирования](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF). |
| Управление производством | Запуск производственного заказа для рабочей нагрузки управления складом для облачных и пограничных единиц масштабирования | Эта функция позволяет работникам использовать мобильное приложение Warehouse Management, чтобы запустить производственный заказ или заказ партии, когда приложение запущено для рабочей нагрузки управления складом в облачной или пограничной единице масштабирования. |
| Управление складом | Новые страницы рабочего места планирования загрузки | Включает две новые страницы рабочего места планирования загрузки: **Рабочее место планирования входящей загрузки** и **Рабочее место планирования исходящей загрузки**. |

## <a name="new-and-updated-documentation-resources"></a>Новые и обновленные ресурсы документации

Недавно были добавлены или существенно обновлены следующие разделы справки. Эти разделы необязательно связаны с новыми функциями, которые были добавлены в данный выпуск, как это показано в предыдущем разделе. Однако они могут повысить эффективность существующих функций.

| Область компонентов | Новые или обновленные темы |
|---|---|
| Управление затратами | [Отчеты о стоимости запасов](../cost-management/inventory-value-report-storage.md) |
| Управление затратами | [Примеры и логика отчетов о стоимости запасов](../cost-management/inventory-value-report-examples.md) |
| Сводное планирование | [Параметры даты и времени, используемые при оптимизации планирования](../master-planning/planning-optimization/date-time-used.md) |
| Сводное планирование | [Настройка прогнозирования спроса](../master-planning/demand-forecasting-setup.md) |
| Сводное планирование | [Использование журнала резервного запаса для обновления минимального покрытия для номенклатур](../master-planning/safety-stock-journal.md) |
| Управление производством | [Настройка интерфейса выполнения производственного цеха](../production-control/production-floor-execution-customize.md) |
| Управление производством | [Стиль интерфейса выполнения производственного цеха](../production-control/production-floor-execution-styles.md) |
| Продажи и маркетинг | [Повышение производительности очистки истории продаж](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Управление складом | [Учетные записи пользователей мобильного устройства](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Дополнительные ресурсы

### <a name="platform-updates-for-finance-and-operations-apps"></a>Обновления платформы для приложений Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.24 включает обновления платформы. Дополнительные сведения см. в разделе [Обновления платформы для версии 10.0.24 приложений Finance and Operations (ноябрь 2021 г.)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Исправления ошибок

Для получения сведений об исправлениях ошибок, включенных в каждое из обновлений, которые являются частью 10.0.24, войдите в службы Lifecycle Services (LCS) и просмотрите [статью базы знаний](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 и промышленные облака: план выпуска волны 2 за 2021 год

Интересуетесь предстоящими и недавно выпущенными возможностями наших бизнес-приложений и платформ?

См. [Dynamics 365 и промышленные облака: план выпуска волны 2 за 2021 год](/dynamics365-release-plan/2021wave2/). Мы собрали в одном документе все сведения, чтобы вы могли использовать их для планирования.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Удаленные и устаревшие функции Supply Chain Management

В теме [Удаленные или устаревшие функции в Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) описываются функции, которые запланированы к удалению или которые планируется удалить или объявить устаревшими для Supply Chain Management.

- *Удаленная* функция больше недоступна в продукте.
- *Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.

Перед удалением каких-либо функций из продукта уведомление об устаревании будет объявлено в теме [Удаленные или устаревшие функции в Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) за 12 месяцев до удаления.

Для критических изменений, которые влияют только на время компиляции, но являются двоично совместимыми с песочницей и производственными средами, время устаревания будет меньше 12 месяцев. Обычно это функциональные обновления, которые должны быть выполнены для компилятора.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]