---
title: Консолидация отгрузок, когда политика консолидации отгрузок переопределена
description: В этой статье представлен сценарий, в котором одна или несколько строк продаж должны быть запущены на склад вручную со страницы Запуск на склад, а политика консолидации отгрузок, определяемая системой, должна быть переопределена до запуска.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e2c4fed880c423790b979f27511d8d5697bd244c
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427964"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden"></a>Консолидация отгрузок, когда политика консолидации отгрузок переопределена

[!include [banner](../includes/banner.md)]

В этой статье представлен сценарий, в котором одна или несколько строк продаж должны быть запущены на склад вручную со страницы **Запуск на склад**, а политика консолидации отгрузок, определяемая системой, должна быть переопределена до запуска. Переопределение политики консолидации отгрузок может потребоваться, например, если заказ, который обычно не был консолидирован с открытыми отгрузками, должен быть консолидирован с открытыми отгрузками.

В ходе сценария создается набор заказов на продажу, а затем политика консолидации отгрузок по умолчанию переопределяется до запуска заказов на склад.

## <a name="make-demo-data-available"></a>Сделать демонстрационные данные доступными

Сценарий в этой статье ссылается на значения и записи, включенные в стандартные демонстрационные данные, предоставляемые в Microsoft Dynamics 365 Supply Chain Management. Если вы хотите использовать значения, указанные здесь, в ходе выполнения упражнений, убедитесь, что вы работаете в среде, в которой установлены демонстрационные данные, и настройте юридическое лицо на **USMF** перед началом работы.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Настройка политик консолидации отгрузок и фильтров продуктов

Описанный здесь сценарий предполагает, что функция уже включена, выполнены упражнения в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md), а также создаются политики и другие записи, которые описаны здесь. Обязательно выполните эти упражнения перед выполнением этого сценария.

## <a name="create-the-sales-orders-for-this-scenario"></a>Создание заказов на продажу для этого сценария

1. Перейти к **Расчеты с клиентами \> Заказы \> Все заказы на продажу** и создать три одинаковых заказа на продажу со следующими параметрами:

    - **Счет клиента:** *US-002*

1. Добавьте строку заказа со следующими параметрами:

    - **Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)
    - **Количество:** *1.00*

1. Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>Запуск заказов на продажу со страницы запуск на склад

Выполните следующие действия, чтобы переопределить политику консолидации отгрузок в ходе запуска на склад.

1. Перейдите на страницу **Управление складом \> Запуск на склад \> Запуск на склад**.
1. В верхней области выберите первый заказ на продажу, созданный для этого сценария.
1. Выберите **Добавить**, чтобы добавить строку в запуск на склад. Обратите внимание, что политика консолидации отгрузок *по умолчанию* применяется в нижней области.
1. В нижней области выберите **выбрать новую политику консолидации отгрузок**.
1. Выбор политики, позволяющей выполнить консолидацию с другими открытыми отгрузками той же политики. Например, выберите политику *CustomerOrderNo*.
1. Выберите **Запуск на склад**.
1. Выберите второй и третий заказы на продажу, созданный для этого сценария.
1. Выберите **Добавить**, чтобы добавить строки в запуск на склад. Обратите внимание, что политика *по умолчанию* применяется в нижней области.
1. Выберите вторую строку, а затем в поле **выберите новую политику консолидации отгрузок** выберите политику *CustomerOrderNo*.
1. Выберите вариант **Запуск на склад** для обеих строк.

## <a name="verify-the-shipments"></a>Проверка отгрузок

Должны быть созданы две отгрузки:

- Первая отгрузка содержит две строки и была создана с помощью политики консолидации отгрузок *CustomerOrderNo*.
- Вторая отгрузка содержит одну строку и была создана с помощью политики консолидации отгрузок *По умолчанию*.

Чтобы просмотреть созданные отгрузки, выполните следующие действия.

1. Выберите **Управление складом \> Отгрузки \> Все отгрузки**.
1. Найдите и выберите нужную отгрузку.
1. В поле **Политика консолидации отгрузок** просмотрите политику консолидации, которая использовалась при создании отгрузки.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор политик консолидации отгрузок](about-shipment-consolidation-policies.md)
- [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]