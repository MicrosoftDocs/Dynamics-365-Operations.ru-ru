--- 
title: "Регистрация поступления товаров по заказу на покупку"
description: "В этой процедуре показано, как зарегистрировать поступление товаров непосредственно в заказе на покупку."
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
ms.openlocfilehash: 01fbf4964dfcecab272204db9c3f5068ca1879cb
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Регистрация поступления товаров по заказу на покупку

[!include[task guide banner](../../includes/task-guide-banner.md)]

В этой процедуре показано, как зарегистрировать поступление товаров непосредственно в заказе на покупку. Также можно зарегистрировать поступление продуктов на складе, а затем зарегистрировать его в заказе на покупку. Эта задача обычно выполняется специалистом по закупке или координатором расчетов с поставщиками. Пример, представленный в этом руководстве, можно использовать в компании с демонстрационными данными USMF. Этот пример описывает шаги создания простого заказа на покупку, чтобы можно процедуру можно было воспроизвести как руководство по задаче. Если вы используете собственные данные в процедуре, вы начнете с подзадачи "Регистрация получения товаров".


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Подготовка нового заказа на покупку для поступления товаров
1. Перейдите в раздел "Закупки и источники" > "Заказы на покупку" > "Все заказы на покупку".
2. Щелкните "Создать".
3. В поле "Счет поставщика" введите "US-101".
4. Нажмите кнопку "OК".
5. В поле "Код номенклатуры" введите "M0001".
6. В поле "Количество" введите 5.
7. В области действий щелкните "Покупка".
8. Нажмите кнопку "Подтвердить".

## <a name="record-receipt-of-goods"></a>Регистрация получения товаров
1. В области действий щелкните "Получение".
2. Щелкните "Поступление продуктов".
    * Поле "Количество" позволяет выбрать различные параметры для количества, которое требуется получить. Например, если количество ранее было зарегистрировано на складе, можно выбрать параметр "Зарегистрированное количество".  В этом примере используется значение "Зарегистрированное количество".   
3. В поле "Поступление продуктов" введите любое значение.
    * Это поле используется для ввода ссылки, которая будет использоваться как ваучер для журнала поступления продуктов.  
4. Разверните раздел "Строки".
5. В поле "Количество" укажите "4".
    * Здесь можно вручную указать количество, которое получается по каждой строке в заказе.  
6. Сверните раздел "Строки".
7. Нажмите кнопку "OК".
    * Товары зарегистрированы как полученные по заказу на покупку, и журнал поступления продуктов был создан как документ, в котором это указано. Можно использовать действие "Поступление продуктов" для просмотра журналов, созданных с заказом на покупку, чтобы узнать, что было получено и когда.  

