--- 
title: "Создание заказа на продажу для настраиваемого продукта"
description: "Эта процедура показывает, как применять шаблон конфигурации к продукту в заказе на продажу."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6546d504a2fda255cb5183408dfe84a3074543ab
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Создание заказа на продажу для настраиваемого продукта

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта процедура показывает, как применять шаблон конфигурации к продукту в заказе на продажу. В этом примере использует модель динамика D0006 в демонстрационных данных компании USMF. Обычно эту процедуру используется сотрудник, обрабатывающий заказы на продажу.


## <a name="create-a-sales-order"></a>Создать заказ на продажу
1. Щелкните "Обработка и запрос заказов на продажу".
2. Щелкните "Создать".
3. Щелкните "Заказ на продажу".
4. В поле "Счет клиента" выберите US-001. 
5. Нажмите кнопку "OК".
6. В поле "Код номенклатуры" выберите "D0006".
    * Для этой задачи необходимо выбрать конфигурируемый продукт.  
7. Щелкните "Продукт и поставки".
8. Щелкните "Настроить строку".
    * Обратите внимание, что цена была изменена, на основании конфигурации, которая была выбрана, и что в поле "Включая кабель" теперь установлено значение "Истина".  
    * Заметьте цену по умолчанию и параметры, выбранные для кабеля.  
9. Щелкните "Загрузить шаблон".
    * В этом примере показано, как можно применить шаблон для выбора предопределенной конфигурации. Если эта процедура используется как проводник по задаче, и вы хотите видеть другие значения атрибутов, которые доступны, необходимо нажать на кнопку "Разблокировать".  
10. Нажмите кнопку "OК".
11. Нажмите кнопку "OК".
12. Разверните раздел "Сведения о строке".
13. Перейдите на вкладку "Продукт".
    * Конфигурация номенклатуры теперь указана в аналитиках продукта.  
14. Закройте страницу.

## <a name="select-the-product-configuration"></a>Выберите конфигурацию продукта.

