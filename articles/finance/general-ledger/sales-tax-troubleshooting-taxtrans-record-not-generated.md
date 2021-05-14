---
title: Запись TaxTrans не создана
description: В этой теме содержатся сведения об устранении неполадок, которые могут помочь, когда запись TaxTrans не создается.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947697"
---
# <a name="taxtrans-record-isnt-generated"></a>Запись TaxTrans не создана

[!include [banner](../includes/banner.md)]

Если для проводки выбрано **Разнесенный налог**, но на странице **Разнесенный налог** нет строк налогов или отсутствует строка налога, то запись **TaxTrans** могла не быть создана.

[![Страница разнесенного налога, которая не содержит элементов строк](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Для решения проблемы выполните действия, указанные в следующих разделах.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Проверка налога до разноски проводки

1. Перед разноской проводки на странице **Разноска накладной** выберите **Налог** для проверки расчета.

    [![Кнопка "Налог" на странице "Разноска накладной"](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. На странице **Временные налоговые проводки** проверьте результат расчета. Если налог не рассчитан, см. [Налог не рассчитан или сумма налога равна нулю](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>Поиск записи TaxTrans во всех разнесенных налогах

1. Перейдите в раздел **Налог** \> **Запросы и отчеты** \> **Налоговые запросы** > **Разнесенный налог**.
2. В заголовке столбца **Ваучер** выберите символ фильтра для поиска записи **TaxTrans**.
3. Если вы нашли нужные налоговые записи, проверьте дату. Если дата отличается от даты заголовка журнала, создайте запрос в службу поддержки Майкрософт для получения дополнительной поддержки.

    [![Страница разнесенного налога](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Отладка для проверки данных

1. Для получения дополнительных сведений об отладке и определении правильности создания **TmpTaxWorkTrans** и **TaxUncommitted** см. [Значение поля в TaxTrans неправильное](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. Если **TaxTmpWorkTrans** или **TaxUncommitted** создается правильно, добавьте точку останова в **TaxPost::SaveAndPost()** и **Tax::SaveAndPost**, чтобы найти причину, почему **TaxTrans** не был вставлен.

    [![Точки останова добавлены в код](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Результаты добавленных точек останова](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Определение существования настройки

Если вы выполнили шаги в предыдущих разделах, но не смогли решить проблему, определите, существует ли настройка. Если настройки не существует, создайте запрос в службу поддержки Майкрософт для получения дополнительной поддержки.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
