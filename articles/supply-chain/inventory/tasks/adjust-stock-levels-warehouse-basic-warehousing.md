---
title: Корректировка уровней запасов на складе (базовая работа со складом)
description: Эта процедура позволяет создать и разнести журнал коррекции запасов для корректировки уровней запасов продуктов на складе.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bba1df70cd23a29ddffad96a4a581154619dc74
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834153"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Корректировка уровней запасов на складе (базовая работа со складом)

[!include [banner](../../includes/banner.md)]

Эта процедура позволяет создать и разнести журнал коррекции запасов для корректировки уровней запасов продуктов на складе. Необходимо настроить наименование журнала запасов для корректировки запасов перед началом этой процедуры. Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные. Эти задачи обычно выполняются работником склада.


## <a name="create-an-inventory-adjustment-journal"></a>Создание журнала коррекции запасов
1. Перейдите "Управление запасами" > "Записи журнала" > "Номенклатуры" > "Корректировка запасов".
2. Щелкните "Создать".
3. В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
4. В списке щелкните наименование журнала коррекции запасов, который необходимо использовать.
    * Некоторые другие поля будут заполнены на основе настройки выбранного наименования журнала коррекции запасов.  
5. Нажмите кнопку "OК".

## <a name="create-journal-lines"></a>Создать строки журнала
1. Щелкните "Создать".
2. Отметьте поле кода номенклатуры в списке.
3. В поле "Код номенклатуры" выберите номенклатуру. При использовании компании с демонстрационными данными USMF введите "D0001".
4. В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
5. Выберите сайт в списке.
6. В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
7. Выберите склад в списке.
    * Если выбрана номенклатура с местонахождением как обязательная аналитика, здесь необходимо указать местонахождение.  
8. В поле "Количество" введите число.
    * В поле себестоимости указывается стоимость на единицу для поступлений на склад. Если для кода номенклатуры не указана себестоимость или ее нужно изменить вручную, это делается здесь.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Проверка и разноска журнала коррекции запасов
1. Щелкните "Проверить".
2. Нажмите кнопку "OК".
3. Щелкните "Разнести".
    * При разноске этого типа журнала разносится приход на склад или расход со склада, изменяются уровень и величина запаса и создаются проводки ГК.  
4. Нажмите кнопку "OК".
5. Закройте форму.
6. Закройте страницу.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]