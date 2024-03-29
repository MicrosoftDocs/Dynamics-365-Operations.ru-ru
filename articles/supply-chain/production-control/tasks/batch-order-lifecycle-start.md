---
title: Жизненный цикл заказа партии от создания до запуска
description: Эта процедура включает выполнение первой части жизненного цикла заказа партии.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7ca259ca8f176cd5bc76081836adcb7d272972b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579264"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Жизненный цикл заказа партии от создания до запуска

[!include [banner](../../includes/banner.md)]

Эта процедура включает выполнение первой части жизненного цикла заказа партии.

От создания, оценки затрат и планирования производственного задания до фактического запуска заказа партии.



В качестве компании с демонстрационными данными для создания этой процедуры используется USMF. 



Условиями для запуска процедуры с другим набором данных является выпущенный продукт с активной формулой и версией маршрута.


## <a name="create-a-batch-order"></a>Создание заказа партии
1. Перейдите в раздел "Все производственные заказы".
2. Щелкните "Новый заказ партии".
3. В поле "Код номенклатуры" введите или выберите значение.
4. Щелкните Создать.
5. Используйте экспресс-фильтр для фильтрации поля "Производство" со значением "b".

## <a name="view-production-formula-and-expected-co-products"></a>Просмотр формулы производства и предполагаемых побочные продуктов
1. В области действий щелкните "Производственный заказ".
2. Щелкните Формула.
3. Закройте страницу.
4. Щелкните Побочные продукты.
5. Закройте страницу.

## <a name="estimate-the-batch-order"></a>Оценка заказа партии
1. Щелкните "Оценка".
2. Нажмите кнопку "OК".
3. В области действий щелкните "Управление затратами".
4. Щелкните "Просмотреть сведения расчета".
5. Закройте страницу.

## <a name="release-the-batch-order"></a>Выпуск заказа партии
1. В области действий щелкните "Производственный заказ".
2. Щелкните "Запуск в производство".
3. Нажмите кнопку "OК".

## <a name="schedule-production-jobs"></a>Планирование производственных заданий
1. В области действий щелкните "План".
2. Щелкните "Планирование заданий".
3. Выберите значение "Нет" в поле "Ограничение по мощности".
4. Выберите значение "Нет" в поле "Ограничение по материалам".
5. Нажмите кнопку OK.
6. В области действий щелкните "Производственный заказ".
7. Щелкните "Все задания".
8. Закройте страницу.

## <a name="start-the-batch-order"></a>Запуск заказа партии
1. Щелкните "Начать".
2. Перейдите на вкладку "Общие".
3. В поле "Разнести отборочную накладную" выберите "Нет".
4. Нажмите кнопку "OК".
5. В области действий щелкните "Показать".
6. Щелкните "Лист подбора".
7. В списке перейдите по ссылке в выбранной строке.
8. Закройте страницу.
9. Закройте страницу.
10. Щелкните "Карта маршрута".
11. В списке перейдите по ссылке в выбранной строке.
12. Закройте страницу.
13. Закройте страницу.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]