--- 
title: "Определение последовательности производственных заданий для непрерывного производства"
description: "В этой процедуре используются краски в качестве примера, чтобы показать, как определить последовательность спланированных заказов в соответствии с приоритетом по цвету и размеру упаковки."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f37b561188cf9c6d90c25e395ba30aa979136590
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Определение последовательности производственных заданий для непрерывного производства

[!include[task guide banner](../../includes/task-guide-banner.md)]

В этой процедуре используются краски в качестве примера, чтобы показать, как определить последовательность спланированных заказов в соответствии с приоритетом по цвету и размеру упаковки. В качестве компании с демонстрационными данными для создания этой процедуры используется USPI. Эта процедура предназначена для планировщика производства.


## <a name="run-master-planning-for-uspi"></a>Выполнение сводного планирования для USPI
1. Перейдите в раздел "Сводное планирование" > "Сводное планирование" > "Выполнить" > "Сводное планирование".
2. В поле "Сводный план" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
3. В списке перейдите по ссылке в выбранной строке.
    * Выберите MasterPlan.  
4. Нажмите кнопку "OК".
    * В результате начнется сводное планирование, включая процесс последовательности. Этот процесс может занять несколько минут.  

## <a name="view-planned-orders-for-the-paint-products"></a>Просмотр спланированных заказов для краски
1. Перейдите в раздел "Сводное планирование" > "Сводное планирование" > "Спланированные заказы".
2. Разверните информационное поле "Сведения о номенклатуре".
3. Разверните информационное поле "Сведения о плане".
4. В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
5. В списке найдите и выберите требуемую запись.
    * Выберите MasterPlan.  
6. В списке перейдите по ссылке в выбранной строке.
7. В экспресс-фильтре по полю "Код номенклатуры" выберите значение "P300".
    * Разблокируйте прокрутку справа, чтобы просмотреть дату заказа и дату поставки. Обратите внимание, что дата заказа этих номенклатур имеет значение "Сегодня", а даты доставки для спланированных заказов не упорядочены по приоритету цвета и размера упаковки, как показано в наименовании продукта. Можно навести указатель мыши на код номенклатуры, чтобы просмотреть наименование и приоритет продукта.  

## <a name="sequence-planned-orders-for-paint"></a>Упорядочение спланированных заказов для краски
1. Закройте страницу.
2. Перейдите в раздел "Сводное планирование" > "Сводное планирование" > "Упорядоченные плановые заказы".
3. Разверните информационное поле "Сведения о номенклатуре".
4. Разверните информационное поле "Сведения о плане".
    * Примечание. Здесь можно увидеть, что дата и время начала спланированных заказов упорядочены по цвету и размеру упаковки в пределах периода в 28 дней. Эти периоды определяются номером в поле "Кампания". Форма упорядоченного планового заказа действует как типовая форма спланированного заказа, и планировщик производства может утвердить спланированные заказы здесь.  
5. Пометьте все строки.
6. Щелкните "Принять".
    * В результате будут обновлены спланированные заказы с выбранным действием последовательности "Отложить" или "Ускорение".  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Проверка последовательности спланированных заказов
1. Закройте страницу.
2. Перейдите в раздел "Сводное планирование" > "Сводное планирование" > "Спланированные заказы".
3. Разверните информационное поле "Сведения о номенклатуре".
4. Разверните информационное поле "Сведения о плане".
5. В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
6. В списке найдите и выберите требуемую запись.
    * Выберите MasterPlan.  
7. В списке перейдите по ссылке в выбранной строке.
8. В экспресс-фильтре по полю "Код номенклатуры" выберите значение "P300".
    * Обратите внимание, что заказы теперь упорядочены в соответствии с приоритетом по цвету и размеру и спланированные заказы запускаются на самую раннюю дату заказа и дату поставки. Проверьте столбец "Дата заказа" или "Дата начала" в информационном поле "Сведения о плане".  

