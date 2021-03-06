---
title: Управление изменениями в формулах и их ингредиентах
description: В этой теме описывается, как выполнять управление формулами и управлять изменениями в справочнике процесса производства.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 825cc5b9355695a648c857e5197b5b93a21fdb43
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115215"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Управление изменениями в формулах и их ингредиентах

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Если вы используете возможности производственного процесса Microsoft Dynamics 365 Supply Chain Management, вы можете также использовать соответствующие возможности управления формулами для управления следующими изменениями:

- **Формулы и номенклатуры планирования:** управление изменениями ингредиентов в формулах и их сопутствующих и побочных продуктах.
- **Сопутствующие и побочные продукты:** редактирование количества и другой информации о сопутствующих и побочных продуктах в формуле.
- **Номенклатуры с учетом в двух единицах измерения:** управление изменениями номенклатур с учетом в двух единицах измерения.

## <a name="turn-on-this-feature-in-your-system"></a>Включение этой функции в системе

Для использования этой возможности необходимо выполнить следующие задачи:

1. Включите функцию *Управление изменениями разработки* и ее конфигурационный ключ, как описано в разделе [Обзор управления техническими изменениями](product-engineering-overview.md). Как упоминалось в этой теме, убедитесь, что вы также включаете лицензионный ключ **Управление изменениями для непрерывного производства**, который является вложенным под главным лицензионным ключом **Управления техническими изменениями**.
1. Включите функцию *Управление изменениями в формулах и их ингредиентах* в разделе [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="feature-naming-conventions"></a>Соглашения об именовании функций

В пользовательском интерфейсе Supply Chain Management и в документации функция управления изменениями обычно называется *управлением техническими изменениями*, и управляемые продукты обычно называются *инженерными продуктами*. Хотя эта терминология обычно не связана с управлением формулами для непрерывного производства, следует подумать об управлении инженерными изменениями как о простом управлении изменениями, и вы должны думать об инженерных продуктах как о продуктах с версиями.

## <a name="work-with-formula-change-management-features"></a>Работа с функциями управления изменениями формулы

В следующем списке приводятся сведения о том, как функции управления техническими изменениями применяются к управлению формулами. Он также содержит ссылки на дополнительные сведения. Поскольку управление изменениями в формулах использует преимущества функций управления техническими изменениями, следует ознакомиться с тем, как работает управление техническими изменениями в целом, так что его можно использовать для управления формулами и их ингредиентами.

- **Централизованное управление данными о продуктах** — настройте организацию, которая через управляемый процесс выпуска позволяет гарантировать, что точные и соответствующие данные продукта доступны пользователям предприятия в целом. Дополнительные сведения см. в разделе [Инжиниринговые компании и правила владения данными](engineering-org-data-ownership-rules.md).
- **Управление версиями продукта** — отслеживание изменений в продуктах с помощью версий продукта и управление продуктом на всех стадиях цепочки поставок. Таким образом можно отследить изменения в формулах. Дополнительные сведения см. в разделе [Инженерные версии и категории технологических продуктов](engineering-versions-product-category.md).
- **Управление жизненным циклом продукта** — управление видимостью данных продукта в организации и управление доступности версий продукта на каждом этапе цепочки поставок. Имеется детальный контроль над тем, когда версию продукта можно использовать в конкретных бизнес-процессах, а также можно создавать собственные состояния жизненного цикла в соответствии с потребностями бизнеса. Дополнительные сведения см. в разделе [Состояния жизненного цикла продукта и проводки](product-lifecycle-state-transactions.md).
- **Управление изменениями формул** — пользователи в организации могут запрашивать изменения в формулах. Заказы на изменение используются для оценки и документирования воздействия предложенных изменений. Добавьте рабочие процессы для управления процессом изменения и выпуском новых версий продукта и его формулой. Дополнительные сведения см. в разделе [Управления изменениями для технологических продуктов](engineering-change-management.md).
- **Управление готовностью** — используйте системные проверки и руководство пользователя (анкеты и контрольные списки), чтобы убедиться, что все необходимые данные продукта были полностью введены до выпуска продукта. Дополнительные сведения см. в разделе [Готовность продуктов](product-readiness.md).
- **Улучшенная функциональность выпуска продукта** — выпуск полностью определенных версий продукта и его формулы из организации (юридического лица) для других юридических лиц. Можно даже определить, должны ли сведения о продукте проверяться или редактироваться перед выпуском. Дополнительные сведения см. в разделе [Структуры выпуска продуктов](release-product-structure.md).

Обратите внимание, что большинство тем, связанных с предыдущим списком, содержат примеры, основанные на спецификациях (BOM). Однако формулы работают аналогичным образом. Ниже приведены несколько дополнительных концепций, которые полезны для определения того, когда использовать управление изменениями (или только управление изменением формулы) для управления формулами и спецификациями:

- Для каждой [инженерной категории продуктов](engineering-versions-product-category.md) можно указать тип производства (спецификация, формула или номенклатура планирования). Можно также указать, требуется ли поддержка учета в двух единицах измерения для продуктов, использующих эту категорию.
- Сопутствующие и побочные продукты не являются инженерными продуктами. Поэтому они не имеют версий. Если их необходимо изменить, просто создайте новый продукт. Такой подход упрощает обслуживание.
- Можно управлять конечными номенклатурами, которые являются спецификациями и имеют дочерние номенклатуры-формулы. Функциональность будет работать для любой комбинации спецификаций, содержащих формулы и/или формулы, содержащие спецификации.
