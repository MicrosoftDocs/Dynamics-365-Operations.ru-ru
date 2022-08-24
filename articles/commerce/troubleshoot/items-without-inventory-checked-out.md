---
title: Номенклатуры без запасов могут быть оформлены
description: В этой статье содержатся указания по устранению неполадок, которые могут помочь в том, что клиенты могут добавлять номенклатуры, отсутствующие на складе, в корзину и перейти к оформлению заказа.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 3bc924e44077886b942e19b25a84f0f1d4298c13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282743"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Номенклатуры без запасов могут быть оформлены

[!include [banner](../../includes/banner.md)]

В этой статье содержатся указания по устранению неполадок, которые могут помочь в том, что клиенты могут добавлять номенклатуры, отсутствующие на складе, в корзину и перейти к оформлению заказа.

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
