---
title: Прогнозирование платежей клиентов (предварительная версия)
description: В этой теме описывается функция прогнозирования платежей, которая может помочь лучше понять типичные порядки платежей для клиентов. Эта функция также позволяет определить обстоятельства, которые могут вынудить вас начать процессы сбора задолженностей раньше, чем вы бы их начали в ином случае.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 84a2342d76dc309fa1fd3de7b2c3de60e62e4d72
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186404"
---
# <a name="customer-payment-predictions-preview"></a>Прогнозирование платежей клиентов (предварительная версия)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

В этой теме описывается функция прогнозирования платежей, которая может помочь лучше понять типичные порядки платежей для клиентов. Эта функция также позволяет определить обстоятельства, которые могут вынудить вас начать процессы сбора задолженностей раньше, чем вы бы их начали в ином случае.

## <a name="overview"></a>Обзор

Организациям часто сложно прогнозировать, когда клиенты будут оплачивать свои накладные. Отсутствие понимания может привести к следующим проблемам:

- Менее точные прогнозы движения денежных средств
- Процессы сбора задолженностей, которые запускаются слишком поздно
- Заказы, которые отпускаются клиентам, которые могут допустить дефолт по своему платежу

Прогнозы платежей клиентов (предварительная версия) помогают организациям предсказать, когда накладная клиента будет оплачена. Таким образом, они могут создавать стратегии сбора задолженностей, которые помогают увеличить вероятность выплаты вовремя.

## <a name="predictions"></a>Прогнозы

Прогнозы по платежам позволяют организациям совершенствовать свои бизнес-процессы, помогая им идентифицировать накладные, которые, вероятно, будут оплачены с задержкой. Организация может использовать эту информацию для выполнения действий, повышающих шансы на то, что они будут оплачены вовремя.

Функция прогнозирования платежей клиентов использует модель машинного обучения для более точного прогнозирования времени, когда клиент оплатит неоплаченную накладную. Эта модель машинного обучения включает исторические накладные, платежи и данные клиентов.

Для каждой открытой накладной функция назначает три вероятности платежа:

- Вероятность того, что платеж будет выполнен вовремя
- Вероятность того, что платеж будет выполнен с задержкой
- Вероятность того, что платеж будет выполнен с большой задержкой

Эта функция также обеспечивает агрегированное представление ожидаемых платежей.

[![Сводное представление о прогнозе платежей](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Каждой накладной назначается вероятность оплаты вовремя. Накладные, для которых вероятность оплаты вовремя составляет менее 50 процентов, помечаются красным кружком, чтобы указать, что они могут потребовать внимания агента по сбору задолженностей.

[![Список вероятностей оплаты](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Функция прогнозирования платежей клиентов также предоставляет контекстные сведения для объяснения прогноза. Эти сведения включают главные факторы, которые влияют на прогноз, текущее состояние бизнеса с клиентом и подробные сведения о поведении платежей клиента в прошлом.

Во многих компаниях процесс сбора задолженностей был реактивным мероприятием. Другими словами, процесс сбора задолженностей не начинается, пока не пройдет срок оплаты накладных. Прогнозирование платежей клиентов позволяет организациям действовать более проактивно в отношении сборов задолженностей. В этом случае больше не требуется ждать, пока наступит крайний срок проводки, чтобы начать процесс сбора задолженностей. Вместо этого они могут использовать функцию прогнозирования платежей, чтобы определить, улучшат ли проактивные сборы вероятность оплаты вовремя.

## <a name="methodology"></a>Методология

В прошлом, как правило, было сложно разработать и развернуть решение искусственного интеллекта (ИИ). Для этого процесса требовалась рабочая группа, включающая специалистов по обработке данных, экспертов по теме и инженеров, которые работали в течение продолжительного периода времени для формулировки, разработки, развертывания и поддержки пригодного к использованию решения ИИ. Прогнозирование платежей клиентов упрощает развертывание и использование ИИ-решений в Microsoft Dynamics 365 Finance. Microsoft упаковывает решения ИИ, которые созданы на основе Microsoft AI Builder. Таким образом, пользователи могут развернуть решение ИИ одним щелчком мыши, чтобы воспользоваться преимуществами интеллектуальных прогнозов. Если вас не устраивает точность прогнозов, опытный пользователь может (опять же, одним щелчком мыши) открыть интерфейс расширения AI Builder, а затем выбрать или очистить поля, используемые для создания прогнозов. Когда вы будете готовы, вы можете "обучить" модель и опубликовать изменения. Новая обученная модель будет автоматически выбрана для создания прогнозов в Dynamics 365 Finance.

## <a name="release-details"></a>Сведения о выпуске

Общедоступная предварительная версия финансового анализа доступна для пробы для развертываний в США, Европе и Соединенном Королевстве. Корпорация Майкрософт последовательно добавляет поддержку дополнительных регионов.

Общедоступные предварительные версии функций должны быть включены только в средах песочницы уровня 2. Настройки и модели ИИ, созданные в среде песочницы, не могут быть перенесены в производственную среду. Дополнительные сведения см. в разделе [Дополнительные условия использования предварительных версий Microsoft Dynamics 365](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
