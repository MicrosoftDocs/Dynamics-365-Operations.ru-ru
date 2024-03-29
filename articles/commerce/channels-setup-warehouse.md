---
title: Настройка склада
description: В этой статье описывается, как настроить склад для использования с новым каналом в Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 476f78d7fe1bc61c2c9b783ed1f82bc660248b02
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273648"
---
# <a name="warehouse-set-up"></a>Настройка складов

[!include [banner](includes/banner.md)]

В этой статье описывается, как настроить склад для использования с новым каналом в Microsoft Dynamics 365 Commerce.

Для каждого канала Commerce необходим настроенный склад, который должен быть связан с ним. Следующие процедуры обеспечивают минимальную конфигурацию, необходимую для настройки склада для канала Commerce. Дополнительные сведения о настройке склада см. в [Обзор управления складом](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).

## <a name="configure-a-warehouse-site"></a>Настройка сайта склада

Перед настройкой склада необходимо настроить сайт склада.

Чтобы настроить сайт склада, выполните следующие действия.

1. В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Сайты**.
1. В области действий выберите **Создать**.
1. В поле **Сайт** введите значение.
1. В поле **Имя** введите значение.
1. В разделе **Общее** задайте соответствующий **Часовой пояс**.
1. В разделе **Адреса** введите адрес.
1. На панели операций выберите **Сохранить**.

На следующем рисунке показан пример сайта склада.

![Пример: сайт склада.](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>Настройка склада

Чтобы настроить склад, выполните следующие шаги.

1. В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Склады**.
1. В области действий выберите **Создать**.
1. В поле **Склад** введите значение.  Если это сопоставление 1:1 с магазином, можно воспользоваться именем магазина или названием регионального центра распределения.
1. В поле **Имя** введите значение.
1. В раскрывающемся списке **Сайт** выберите сайт склада, который был создан ранее.
1. В поле **Тип** выберите **По умолчанию**.
    - Если требуется настроить **Карантинный склад**, сначала необходимо выполнить следующие действия для создания дополнительного склада, где для этого **Тип** устанавливается значение **Карантин**.
    - Если требуется настроить **Транзитный склад**, сначала необходимо выполнить следующие действия для создания дополнительного склада, где для этого **Тип** устанавливается значение **Транзит**.
1. На панели операций выберите **Сохранить**.

## <a name="set-up-inventory-aisles"></a>Настройка складских проходов

Чтобы настроить складские проходы, выполните следующие действия.

1. В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Настройка местонахождения \> Складские проходы**.
1. В области действий выберите **Создать**.
1. В раскрывающемся списке **Склад** выберите склад, который был создан ранее.
1. В поле **Проход** введите имя (например, "Def").
1. В поле **Имя** введите имя (например, "Default aisle").
1. На панели операций выберите **Сохранить**.

## <a name="set-up-warehouse-inventory-locations"></a>Настройка местонахождений запасов склада

Чтобы настроить местонахождения запасов склада для стандартных, поврежденных и возвращенных запасов, выполните следующие действия.

1. В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Склады**.
1. Выберите созданный ранее склад.
1. На панели операций выберите **Правка**.
1. На панели операций выберите **Склад**, а затем выберите **Место хранения**.
1. В области действий выберите **Создать**. В раскрывающемся списке **Склад** должно быть значение по умолчанию для нового склада.
    1. В поле **Проход** введите название прохода, который был указан ранее. 
    1. Задайте для **Ручное изменение** **Да**
    1. В поле **Местонахождение** введите имя склада.
    1. На панели операций выберите **Сохранить**.
 1. В области действий выберите **Создать**.  В раскрывающемся списке **Склад** должно быть значение по умолчанию для нового склада.
    1. В поле **Проход** введите название прохода, который был указан ранее.  
    1. Задайте для **Ручное изменение** **Да**
    1. В поле **Местоположение** введите "повреждено".
    1. На панели операций выберите **Сохранить**.
 1. В области действий выберите **Создать**.  В раскрывающемся списке **Склад** должно быть значение по умолчанию для нового склада.
    1. В поле **Проход** введите название прохода, который был указан ранее. 
    1. Задайте для **Ручное изменение** **Да**
    1. В поле **Местоположение** введите "возврат".
    1. На панели операций выберите **Сохранить**.
    
На следующем рисунке показана настройка местонахождения запасов склада "Сан-Франциско".

![Пример настройки местонахождения запасов.](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Завершение настройки склада

Чтобы завершить настройку склада, выполните следующие действия.

1. В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Склады**.
1. Выберите созданный ранее склад.
1. На панели операций выберите **Правка**.
1. В **Управление запасами и складами**:
    1. Задайте для **Ячейка прихода по умолчанию** ячейку по умолчанию, созданную выше.
    1. Выберите для **Ячейка расхода по умолчанию** ячейку по умолчанию, созданную выше.
1. В разделе **Адреса** введите адрес склада.
1. В разделе **Розница**: 
    1. В поле **Расположение возврата по умолчанию** введите ранее созданное местонахождение возврата.
    1. Задайте для **Магазин** значение **Да**.
    1. Задайте **Вес** как **1,00**. 
    1. В поле **Аналитики хранения** введите ранее созданное местонахождение по умолчанию.
1. В разделе **Склад** установите для параметра **Физический отрицательный запас** значение **Да**.
1. На панели операций выберите **Сохранить**.

На следующем рисунке показаны данные для настроенного склада.

![Пример настроенного склада.](media/warehouse-sample.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор управления складом](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[Обзор каналов](channels-overview.md)

[Необходимые условия для настройки каналов](channels-prerequisites.md)

[Настройка канала розничной торговли](channel-setup-retail.md)
    
[Настройка интернет-канала](channel-setup-online.md)

[Настройка канала центра обработки вызовов](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
