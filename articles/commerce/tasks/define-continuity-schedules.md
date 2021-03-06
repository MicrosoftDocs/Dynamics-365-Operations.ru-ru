---
title: Определение планов непрерывности
description: В этом разделе выполняется пошаговая настройка программы непрерывности (также называемой повторяющимися заказами).
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8414377ddec0e001f003f842866725eb58bd75a3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791615"
---
# <a name="define-continuity-schedules"></a>Определение планов непрерывности

[!include [banner](../includes/banner.md)]

В этом разделе выполняется пошаговая настройка программы непрерывности (также называемой повторяющимися заказами). В этом разделе в демонстрационных данных используется компания USRT.


## <a name="create-continuity-program"></a>Создание программы непрерывности
1. Перейдите в раздел "Retail и Commerce" > "Непрерывность" > "Программы непрерывности".
2. Нажмите Создать.
3. В поле "Код плана" введите код плана непрерывности.
4. В поле "Начало заказа" выберите "Первое событие".
    * Если клиент размещает новый заказ для программы непрерывности, имеются два варианта, для которых продукт будет отгружен: 1. Первое событие: будет отгружен первый продукт в программе непрерывности.  2. Текущее событие: текущий продукт будет отгружен. Например, в третий месяц программы клиент получит третий в программе.  
5. Выберите "Да" для запроса даты начала заказа.
6. Щелкните "Добавить строку".
7. В поле "Код номенклатуры" введите код номенклатуры для первого продукта ("0013").
8. Введите "CP".
9. Введите дату, когда первый продукт будет доступен для заказа.
10. Щелкните "Добавить строку".
11. В поле "Код номенклатуры" введите "0014".
12. В поле "Код интервала дат" очистите значение, чтобы это поле осталось пустым.
    * Для этой процедуры очистите интервал дат. Вы установите дату как последовательно увеличивающуюся с начальной даты для первой номенклатуры.  
13. Здесь введите интервал, с которым отгружаются продукты. Введите "30".
    * Для ежемесячной программы следует ввести интервал 30 дней.  
14. Щелкните "Добавить строку".
15. В поле "Код номенклатуры" введите "0015".
16. Введите "Завершить".
17. Нажмите кнопку "Сохранить".

## <a name="assign-to-continuity-item"></a>Назначение номенклатуры непрерывности
1. Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".
2. Выберите номенклатуру "0016".
    * В этой процедуре вы выберите номер номенклатуры 0016. Обычно у вас будет созданный выпущенный продукт, к которому будет применена дополнительная бизнес-логика непрерывности, когда он помещается в заказ на продажу в центре обработки вызовов.  
3. В списке перейдите по ссылке в выбранной строке.
4. Щелкните "Изменить".
5. Разверните или сверните раздел "Продажа".
6. Здесь введите программу непрерывности, которую эта номенклатура представляет. Введите "Код плана", созданной ранее.
    * Если эта номенклатура продается в центре обработки вызовов, дополнительная бизнес-логику применяется из выбранной программы непрерывности.  
7. Нажмите кнопку "Сохранить".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]