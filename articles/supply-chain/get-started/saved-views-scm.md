---
title: Стандартные сохраненные представления для Supply Chain Management
description: В этой теме описываются доступные стандартные сохраненные представления и объясняется, как их включить.
author: kamaybac
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1b1077fdb4707bf2c019e86cb073b30465817577
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270667"
---
# <a name="standard-saved-views-for-supply-chain-management"></a>Стандартные сохраненные представления для Supply Chain Management

[!include [banner](../../includes/banner.md)]

В Microsoft Dynamics 365 Supply Chain Management имеется несколько сохраненных представлений, которые можно включить и использовать при необходимости. Некоторые из этих стандартных сохраненных представлений оптимизированы и именуются для определенной роли или задачи (например, "контроль качества" или "получение"). Другие оптимизируются таким образом, что они содержат только поля и параметры, которые, как указывает статистика использования Microsoft, чаще всего используются клиентами. Эти сохраненные представления обычно называют *упрощенными* представлениями. В этой теме описываются доступные стандартные сохраненные представления и объясняется, как их включить и настроить.

Полные сведения о работе с сохраненными представлениями, включая стандартные сохраненные представления, после их включения см. в разделе [Сохраненные представления](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="customizing-the-standard-saved-views"></a>Настройка стандартных сохраненных представлений

Можно настроить стандартные сохраненные представления, точно так же как можно настроить собственные сохраненные представления. Однако при настройке стандартного сохраненного представления настоятельно рекомендуется сохранить пользовательскую версию под новым именем. В противном случае настройки могут быть перезаписаны после обновления Supply Chain Management.

Дополнительные сведения о настройке и переименовании сохраненных представлений см. в разделе [Сохраненные представления](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="available-saved-views-and-how-to-enable-them"></a>Доступные сохраненные представления и способ их включения

Чтобы использовать сохраненные представления, независимо от того, будут ли использоваться стандартные сохраненные представления, необходимо включить функцию *Сохраненные представления* в модуле [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

В остальных разделах этой темы приводятся таблицы, описывающие стандартные сохраненные представления, доступные в настоящее время для каждого соответствующего модуля. В каждой таблице отображаются названия всех сохраненных представлений, страниц, где их можно найти, и их описание. В каждой таблице также показано название функции, которая включает сохраненное представление. Для просмотра стандартного сохраненного представления в системе необходимо включить указанную функцию в разделе [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="saved-views-for-the-inventory-management-module"></a>Сохраненные представления для модуля управления запасами

В следующей таблице описаны сохраненные представления, доступные для модуля "Управление запасами".

| Страница | Имя представления | Описание представления | Имя функции |
|---|---|---|---|
| Список количества в наличии | Финансы | Этот упрощенное представление позволяет сосредоточиться на финансовой информации при управлении запасами в наличии. | Сохраненные представления для управления запасами |
| Список количества в наличии | Контроль качества | Этот упрощенное представление позволяет сосредоточиться на контроле качества при управлении запасами в наличии. | Сохраненные представления для управления запасами |
| Список количества в наличии | Получение | Этот упрощенное представление позволяет сосредоточиться на операциях получения при управлении запасами в наличии. | Сохраненные представления для управления запасами |
| Список количества в наличии | Отгрузка | Этот упрощенное представление позволяет сосредоточиться на операциях отгрузки при управлении запасами в наличии. | Сохраненные представления для управления запасами |
| Проводки | Упрощенное | Это упрощенное представление позволяет просматривать статус запасов, не отвлекаясь на финансовую информацию и другие поля, которые используются реже остальных. | Сохраненные представления для управления запасами |
| Заказы на перемещение | Отгрузка | Этот упрощенное представление позволяет сосредоточиться на операциях отгрузки при управлении заказами на перемещение. | Сохраненные представления для управления запасами |
| Заказы на перемещение | Получение | Этот упрощенное представление позволяет сосредоточиться на операциях получения при управлении заказами на перемещение. | Сохраненные представления для управления запасами |
| Заказы на перемещение | Контроль качества | Этот упрощенное представление позволяет сосредоточиться на контроле качества при управлении заказами на перемещение. | Сохраненные представления для управления запасами |
| Заказы на перемещение | Финансы | Этот упрощенное представление позволяет сосредоточиться на финансовой информации при управлении заказами на перемещение. | Сохраненные представления для управления запасами |

## <a name="saved-views-for-the-master-planning-module"></a>Сохраненные представления для модуля сводного планирования

В следующей таблице описаны сохраненные представления, доступные для модуля "Сводное планирование".

| Страница | Имя представления | Описание представления | Имя функции |
|---|---|---|---|
| Спланированные заказы: страница сведений о спланированных заказах | Упрощенное | Это упрощенное представление включает только поля, которые чаще всего используются для работы с подробными сведениями об одном спланированном заказе. Таким образом обеспечивается более быстрый обзор и упрощенный процесс работы. | Сохраненные представления для спланированных заказов |
| Спланированные заказы: страница списка спланированных заказов | Упрощенное | Это упрощенное представление включает только поля, которые чаще всего используются для работы со списком спланированных заказов. Таким образом обеспечивается более быстрый обзор и упрощенный процесс работы. | Сохраненные представления для спланированных заказов |

## <a name="saved-views-for-the-procurement-and-sourcing-module"></a>Сохраненные представления модуля закупок и источников

В следующей таблице описаны сохраненные представления, доступные для модуля "Закупки и источники".

| Страница | Имя представления | Описание представления | Имя функции |
|---|---|---|---|
| Сведения о заказе на покупку | Создание заказа | Это упрощенное представление оптимизировано для создания новых заказов на покупку. | Сохраненные представления для заказов на покупку |
| Сведения о заказе на покупку | Управление запасами | Это упрощенное представление оптимизировано для выполнения действий, связанных с запасами, таких как дальнейшие действия с полученными запасами, получение запасов, проверка чистых потребностей и корректировка количеств по заказам. | Сохраненные представления для заказов на покупку |
| Сведения о заказе на покупку | Управление финансами | Это упрощенное представление оптимизировано для выполнения финансовых операций, таких как выставление накладных и проверка цен, итоговых сумм и накладных расходов. | Сохраненные представления для заказов на покупку |
| Сведения о заказе на покупку | Утверждение заказа | Это упрощенное представление оптимизировано для утверждения заказов на покупку. | Сохраненные представления для заказов на покупку |

## <a name="saved-views-for-the-production-control-module"></a>Сохраненные представления для модуля управления производством

В следующей таблице описаны сохраненные представления, доступные для модуля "Управление производством".

| Страница | Имя представления | Описание представления | Имя функции |
|---|---|---|---|
| Страница спецификации производственного заказа | Упрощенное | Это упрощенное представление включает только наиболее часто используемые поля. Таким образом обеспечивается более быстрый обзор и упрощенный процесс работы. | Сохраненные представления для управления производством |
| Страница сведений о производственном заказе | Упрощенное | Это упрощенное представление включает только наиболее часто используемые поля. Таким образом обеспечивается более быстрый обзор и упрощенный процесс работы. | Сохраненные представления для управления производством |
| Страница листа подбора по производственному заказу | Упрощенное | Это упрощенное представление включает только наиболее часто используемые поля. Таким образом обеспечивается более быстрый обзор и упрощенный процесс работы. | Сохраненные представления для управления производством |
| Страница списка производственных заказов | Упрощенное | Это упрощенное представление включает только наиболее часто используемые поля. Таким образом обеспечивается более быстрый обзор и упрощенный процесс работы. | Сохраненные представления для управления производством |

## <a name="saved-views-for-the-sales-and-marketing-module"></a>Сохраненные представления для модуля продажи и маркетинга

В следующей таблице описаны сохраненные представления, доступные для модуля "Продажи и маркетинг".

| Страница | Имя представления | Описание представления | Имя функции |
|---|---|---|---|
| Журнал отборочных накладных | Обзор журнала | Это упрощенное представление включает только поля, которые чаще всего используются для просмотра журналов отборочных накладных. | Сохраненные представления для продажи и маркетинга |
| Заказ на продажу | Создание заказа | Это упрощенное представление включает только поля, которые чаще всего используются для создания заказов на продажу. | Сохраненные представления для продажи и маркетинга |
| Заказ на продажу | Просмотр заказа | Это упрощенное представление включает только поля, которые чаще всего используются для просмотра заказов на продажу. | Сохраненные представления для продажи и маркетинга |
| Предложение по продажам | Создание предложений с расценками | Это упрощенное представление включает только поля, которые чаще всего используются для создания предложений по продажам. | Сохраненные представления для продажи и маркетинга |

## <a name="saved-views-for-the-warehouse-management-module"></a>Сохраненные представления для модуля управления складом

В следующей таблице описаны сохраненные представления, доступные для модуля "Управление складом".

| Страница | Имя представления | Описание представления | Имя функции |
|---|---|---|---|
| Все загрузки | Входящая обработка | Это упрощенное представление включает только поля, которые чаще всего используются для обработки входящих загрузок. | Сохраненные представления для обработки загрузки |
| Все загрузки | Исходящая обработка | Это упрощенное представление включает только поля, которые чаще всего используются для обработки исходящих загрузок. | Сохраненные представления для обработки загрузки |
| Все отгрузки | Входящая обработка | Это упрощенное представление включает только поля, которые чаще всего используются для обработки входящих отгрузок. | Сохраненные представления для обработки отгрузки |
| Все отгрузки | Исходящая обработка | Это упрощенное представление включает только поля, которые чаще всего используются для обработки исходящих отгрузок. | Сохраненные представления для обработки отгрузки |
| Все волны | Упрощенное | Это упрощенное представление включает только наиболее часто используемые поля. Таким образом обеспечивается более быстрый обзор и упрощенный процесс работы. | Сохраненное представление для обработки волны |
| Рабочее место планирования загрузки | Упрощенное | Это упрощенное представление включает только наиболее часто используемые поля. Таким образом обеспечивается более быстрый обзор и упрощенный процесс работы. | Сохраненное представление для рабочего места планирования работ |
| Сведения о работе | Упрощенное | Это упрощенное представление включает только наиболее часто используемые поля. Таким образом обеспечивается более быстрый обзор и упрощенный процесс работы. | Сохраненное представление для страницы сведений о работе |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]