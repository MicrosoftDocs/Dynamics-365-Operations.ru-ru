---
title: Графики поставки
description: Графики поставки позволяют отслеживать количество в строках заказа при использовании нескольких поставок для одного заказа на продажу, предложения по продажам или заказа на покупку.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b50558c5da71351082d36276a3185e1f91543f2b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573473"
---
# <a name="delivery-schedules"></a>Графики поставки

[!include [banner](../includes/banner.md)]

Графики поставки позволяют отслеживать количество в строках заказа при использовании нескольких поставок для одного заказа на продажу, предложения по продажам или заказа на покупку.

Используйте график поставки, когда полное количество в строке заказа или предложения необходимо поставить в нескольких отгрузках. Индивидуальные отгрузки представлены строками поставки. Два или более строки поставки составляют один график поставки. В строках поставки могут быть указаны различные даты, количества и способы поставки или аналитики хранения, такие как сайт и склад.  

**Пример графика поставки**

| Номенклатура                              | значение                                    |
|-----------------------------------|------------------------------------------|
| Итоговый заказ (исходная строка заказа) | 600 стульев                               |
| Запрошенный график поставки       | 100 стульев в месяц                     |
| Запрошенные временные рамки для поставки | 6 месяцев, по первым числам каждого месяца |

В этом случае клиент запрашивает поставку 600 стульев группами по 100 стульев в течение шести месяцев. Чтобы отслеживать требования поставки вы создаете график поставки. На странице графика поставки создается шесть отдельных строк поставки. Каждая строка поставки содержит 100 стульев и отображает даты поставки для этих 100 стульев. В этом случае каждая строка смещается на первый день месяца в течение шести последовательных месяцев.  

Когда вы создаете график поставки, тип строки первоначального заказа автоматически изменяется на **Строка заказа с множественными поставками**. Строка этого типа называется коммерческой строкой и отмечена значком. Строка поставки отмечена другим значком. Если вы изменяете количество в строке поставки, коммерческая строка обновляется до полного количества графика поставки. Если торговое соглашение определило полную скидку для заказа, то график поставки обеспечивает, что для вашего заказа действует полная скидка по заказу, даже если заказ разделен на несколько поставок.  

Заказы, которые имеют график поставки, обрабатываются по строкам поставки. Обработка включает разноску отборочных накладных, поступлений продуктов и выставление накладных.  

Документальные распечатки заказов и предложений, которые имеют график поставки, содержат только строки поставки. В них не отображаются исходные строки (коммерческие строки). **Примечание.** Кроме того, только строки поставки отображаются, когда вы выполняете следующие действия:

-   Разнести
-   Копирование страниц
-   Просмотр страниц списков и отчетов

После подтверждения предложений по продажам в итоговых заказах на покупку отображается весь график поставки, включая даже строки заказа с несколькими поставками. Кроме того, весь график поставки отображается на всех основных страницах, таких как заказы на продажу, предложения по продажам и заказы на покупку.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]