---
title: Контроль качества товаров
description: В этом разделе объясняется, как обработать заказ для контроля качества.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee5f83b2dad60567341f33a73ce63d01e9da8289
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436299"
---
# <a name="inspect-the-quality-of-goods"></a>Контроль качества товаров

[!include [banner](../../includes/banner.md)]

В этом разделе объясняется, как обработать заказ для контроля качества. Это руководство можно выполнить, используя компанию с демонстрационными данными USMF. Перед началом этой процедуры необходимо подтвердить заказ на покупку "000016" и разнести поступление продуктов. При этом автоматически будет создан заказ контроля качества. Контроль качества обычно производится сотрудником отдела контроля качества.


## <a name="select-a-quality-order"></a>Выбор заказа контроля качества
1. В области перехода перейдите к **Модули > Управление запасами > Периодические задачи > Управление качеством > Заказы на контроль качества**.
2. Выберите заказ контроля качества, созданный перед началом этой процедуры.  

## <a name="record-test-results"></a>Запись результатов проверки
1. Выберите **Результаты**.
2. Выберите **Правка**.
3. В поле **Итоговое количество** введите число.
4. В поле **Результат** выберите требуемую запись в раскрывающемся меню.  
- В этом примере результат основан на заранее определенном итоге. Обычно фиксируется более конкретный результат испытаний, например размер или другая аналитика.  
5. Нажмите **Сохранить**.
6. Закройте страницу.

## <a name="validate-the-quality-order"></a>Проверить заказ контроля качества
1. Выберите **Проверить**.
2. В поле **Кем проверено** выберите пользователя, выполняющего проверку, из раскрывающегося меню.  
3. Щелкните **Выбрать**.
4. Нажмите **ОК**.
5. Закройте страницу.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]