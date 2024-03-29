---
title: Использование прогнозов платежей клиентов
description: В этой статье рассматриваются необходимые условия и описываются основные шаги, необходимые для использования пробной версии Finance Insights.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 330642624b55a6772ef149b70873021401a6bd83
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901412"
---
# <a name="use-customer-payment-predictions"></a>Использование прогнозов платежей клиентов

[!include [banner](../includes/banner.md)]

В этой статье объясняется, как использовать прогнозы платежей клиентов. Перед тем как использовать эту функцию, убедитесь, что для нее выполнены шаги настройки. Дополнительные сведения см. в разделе [Включение прогнозов платежей клиентов](enable-cust-paymnt-prediction.md).

Прогнозы платежей клиентов можно просматривать в рабочей области **Управление кредитами и сборами задолженностей клиентов** и на двух новых страницах списков: **Прогнозы платежей по проводкам** и **Прогноз платежей клиентов**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Рабочая область управление кредитом и сбором задолженностей клиентов

Рабочая область **Управление кредитами и сборами задолженностей клиентов** включает две новые плитки: **Прогнозы платежей по проводкам** и **Прогнозы платежей клиентов**.

### <a name="transaction-payment-predictions-list-page"></a>Страница списка прогнозов платежей по проводкам

На странице списка **Прогнозы платежей по проводкам** можно просмотреть вероятность платежа по открытым проводкам в периодах **Вовремя**, **С задержкой** и **С большой задержкой**. Для каждой проводки в сетке столбец **Вероятность вовремя** показывает вероятность оплаты накладной в дату срока оплаты или до нее. Если вероятность своевременного платежа меньше 50 процентов, рядом с процентами в столбце **Вероятность вовремя** появляется красный кружок для указания риска платежа с задержкой.

[![Страница прогноза платежей по проводкам.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Панель **Связанные сведения** в правой части страницы содержит более подробные сведения о прогнозах:

- Для проводки, выбранной в сетке, на экспресс-вкладке **Прогноз оплаты** отображаются сведения о прогнозах платежей на периоды **Вовремя**, **С задержкой** и **С большой задержкой**. В разделе **Главные факторы** показаны главные факторы, которые влияют на прогнозы. Главные факторы представляют собой атрибуты выбранной проводки и/или клиента для этой проводки.
- Экспресс-вкладка **Аналитика клиента** отображает текущую статистику по накладным, платежам и сборам задолженностей для клиента для выбранной проводки.
- Экспресс-вкладка **История клиента** показывает историю платежей клиента в категориях времени **Вовремя**, **С задержкой** и **С большой задержкой**.

Данные в разделе **Главные факторы** и на экспресс-вкладках **Аналитика клиента** и **История клиента** помогают объяснить прогнозы платежей. Они могут способствовать повышению уверенности в эффективности прогнозов.

[![Графические индикаторы для прогнозов платежей на панели соответствующей информации.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="customer-payment-predictions-list-page"></a>Страница списка прогнозов платежей клиентов

Страница списка **Прогнозы платежей клиентов** отображает общее открытое сальдо и сумму, прогнозируемую к оплате в категориях времени **Вовремя**, **С задержкой** и **С большой задержкой**.

[![Страница прогнозов платежей по клиентам.](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Сумма платежа в каждом сегменте рассчитывается как сумма взвешенного среднего сальдо по проводкам. Эта сумма рассчитывается на основе вероятностей платежа в каждом сегменте.

Например, клиент имеет три открытые проводки, которые имеют следующие вероятности оплаты в каждом сегменте.

| Проводка | Сумма, руб. | Вероятность платежа вовремя | Вероятность платежа с задержкой | Вероятность платежа с большой задержкой |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10 процентов                  | 50 процентов               | 40 процентов                    |
| T2          | 1000  | 50 процентов                  | 30 процентов               | 20 процентов                    |
| T3          | 10,000 | 1 процентов                   | 4 процентов                | 95 процентов                    |

В этом случае платежи прогнозируются для каждого сегмента следующим образом.

| Сегменты   | Проводка T1      | Проводка T2         | Проводка T3            | Итоговый |
|-----------|---------------------|------------------------|---------------------------|-------|
| Вовремя   | 100 × 10 ÷ 100 = 10 | 1 000 × 50 ÷ 100 = 500 | 10 000 × 1 ÷ 100 = 100    | 610   |
| С опозданием      | 100 × 50 ÷ 100 = 50 | 1 000 × 30 ÷ 100 = 300 | 10 000 × 4 ÷ 100 = 400    | 750   |
| Очень поздно | 100 × 40 ÷ 100 = 40 | 1 000 × 20 ÷ 100 = 200 | 10 000 × 95 ÷ 100 = 9 500 | 9,740 |

Раздел **Связанные сведения** в правой части страницы содержит более подробные сведения о прогнозах:

- Для проводки, выбранной в сетке, на экспресс-вкладке **Прогнозы оплаты** отображаются сведения о прогнозах платежей на периоды **Вовремя**, **С задержкой** и **С большой задержкой**.
- Экспресс-вкладка **Аналитика клиента** отображает текущую статистику по накладным, платежам и сборам задолженностей для клиента для выбранной проводки.
- Экспресс-вкладка **История клиента** показывает историю платежей клиента в категориях времени **Вовремя**, **С задержкой** и **С большой задержкой**.

Данные на экспресс-вкладках **Customer Insights** и **История клиента** помогают объяснить прогнозы платежей. Они могут способствовать повышению уверенности в эффективности прогнозов.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Повышение точности прогнозов платежей

Точность прогнозов платежей можно просмотреть, перейдя к разделу **Кредит и сбор задолженностей \> Настройка \> Финансовый анализ \> Параметры финансового анализа**. На вкладке **Анализ платежей клиентов** в разделе **Модель прогнозирования** отображается точность модели прогнозирования в процентах.

Если точность неудовлетворительна, выберите ссылку **Улучшение точности модели**, чтобы открыть интерфейс расширения AI Builder. В интерфейсе расширения AI Builder можно выбрать или отменить выбор полей до тех пор, пока не будут выбраны поля, которые, по вашему мнению, являются наиболее важными для точного предсказания вероятностей оплаты. После завершения можно легко переучить модель прогнозирования и опубликовать изменения. Новая обученная модель прогнозирования будет автоматически выбрана для прогнозов в Dynamics 365 Finance.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
