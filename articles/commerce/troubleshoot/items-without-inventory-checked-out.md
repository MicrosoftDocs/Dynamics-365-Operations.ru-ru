---
title: Номенклатуры без запасов могут быть оформлены
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том, что клиенты могут добавлять номенклатуры, отсутствующие на складе, в корзину и перейти к оформлению заказа.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: af44def901d3aa7d4b24ab6abfac60d066a8d1a3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801755"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Номенклатуры без запасов могут быть оформлены

[!include [banner](../../includes/banner.md)]

В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том, что клиенты могут добавлять номенклатуры, отсутствующие на складе, в корзину и перейти к оформлению заказа.

## <a name="description"></a>описание

Пользователи могут добавить номенклатуру в корзину, даже если в магазине нет запасов в наличии, а затем перейти на страницу извлечения.

## <a name="resolution"></a>Приказ

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>Включение свойства Показывать ошибки "Нет в наличии" в конструкторе сайтов Commerce

Чтобы включить свойства **Показывать ошибки "Нет в наличии"** в конструкторе сайтов Commerce, сделайте следующее.

1. Выберите сайт, с которым вы работаете в данный момент.
1. В левой области переходов выберите **Страницы**.
1. Выберите **Страница корзины**, чтобы открыть его.
1. Выберите **Корзина 1**, выберите **Изменить**, а затем в области свойств установите флажок **Показывать ошибки "Нет в наличии"**.
1. Сохраните и опубликуйте страницу.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Применение настроек запасов](../inventory-settings.md)

[Расчет наличия запасов для розничных каналов](../calculated-inventory-retail-channels.md)

[Настройка буферов запасов и уровней запасов](../inventory-buffers-levels.md)
