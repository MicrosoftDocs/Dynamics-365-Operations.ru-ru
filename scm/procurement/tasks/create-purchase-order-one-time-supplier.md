--- 
title: "Создание заказа на покупку для разового поставщика"
description: "В этой процедуре показано, как создать заказ на покупку для разового поставщика."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 580dfe3680c36a32a24999bc8c266a38a07177fd
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Создание заказа на покупку для разового поставщика

[!include[task guide banner](../../includes/task-guide-banner.md)]

В этой процедуре показано, как создать заказ на покупку для разового поставщика. Поставщик создается автоматически с заказом на покупку вместо того, чтобы создавать счет поставщика вручную. Заказы на покупку обычно создаются специалистом по закупке. Пример, представленный в этом руководстве, можно использовать в компании с демонстрационными данными USMF. В качестве предварительного требования следует настроить счет разового поставщика на странице "Параметры модуля расчетов с поставщиками".


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Создание заказа на покупку для разового поставщика
1. Перейдите в раздел "Закупки и источники" > "Заказы на покупку" > "Все заказы на покупку".
2. Щелкните "Создать".
3. Выберите значение "Да" в поле "Разовый поставщик".
    * Счет поставщика автоматически создается и назначается заказу на покупку. Счет поставщика создается на основе шаблона, указанного на вкладке "Общее" на странице "Параметры модуля расчетов с поставщиками".  
4. В поле "Имя" введите имя поставщика.
5. Нажмите кнопку "OК".
    * Заказ на покупку теперь можно завершить и обработать как любой другой заказ. Не существует особых характеристик, связанных с тем, как это выполняется. В накладной будет учитываться проводка к оплате в счете поставщика, который был создан с заказом, после чего будет обработан платеж. По завершении этого счет поставщика можно удалить. Обычно эту операцию выполняет отдел по расчетам с поставщиками.  

