---
title: Изменение способа поставки в POS-терминале
description: В этом разделе описывается, как настроить и использовать операцию изменения режима поставки в POS-терминале.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 26e798c664844b575de6f019ad8f5349ed92be98
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2020
ms.locfileid: "3114412"
---
# <a name="change-mode-of-delivery-in-pos"></a>Изменение способа поставки в POS-терминале

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

В этом разделе описывается, как настроить и использовать функцию "изменение режима поставки" в среде POS-терминала. 

В Dynamics 365 Commerce версии 10.0.10 и более поздних операция **Изменить способ поставки** (647) доступна для добавления на макеты экрана POS-терминала.

Функция изменения режима поставки предоставляет возможность изменить способ поставки для одной или нескольких строк продаж, настроенных для поставки, в POS-проводке. В предыдущих версиях Commerce необходимо было выполнить полные потоки конфигурации **Отгрузить все** и **Отгрузить выбранное**, если необходимо изменить способ поставки в существующей строке, которая была настроена для отгрузки. Этот процесс требует много времени и может привести к случайным изменениям происхождения поставки или дат поставки для строки. Новая функциональность предоставляет альтернативный метод эффективного обновления способа поставки по этим строкам продаж.

Дополнительные сведения о порядке добавления операции в кнопку в сетке кнопок POS-терминала см. в разделе [Макеты экрана для POS-терминала](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).

После того, как эта функция будет настроена в POS-терминале, при выборе команды **Изменить способ поставки** будет открыта страница со списком, в которой можно выбрать строки проводки, для которой требуется изменить режим поставки. Можно выбрать некоторые или все строки или выйти без внесения каких-либо изменений. Строки продажи, которые ранее были настроены для отгрузки, являются единственными строками в списке, которые можно изменить. Если необходимо изменить строку, назначенную для получения в магазине или на вынос для отправки, следует использовать операции **Отгрузить все** или **Отгрузить выбранное**. И наоборот, если необходимо изменить строку, обозначенную как отгрузка для получения в магазине или на вынос, следует использовать операции **Забрать все**, **Забрать выбранное**, **На вынос все** или **На вынос выбранное**.

После выбора строк, которые необходимо изменить, щелкните **Изменить способ поставки**, и будет предложено выбрать вариант способа поставки. Если для изменения выбрано несколько строк, в POS-терминале будут отображены только режимы доставки, которые были настроены как допустимые для всех выбранных продуктов. Способы поставки могут быть настроены для поддержки различных продуктов и адресов поставки. Если имеется способ доставки, допустимый для одной комбинации продукта и адреса, но неприемлемый для другого выбранного сочетания продукта и адреса, этот режим доставки будет недоступен. Возможно, потребуется выбрать строки по одной и изменить режим доставки для каждой строки отдельно, если требуется выбрать режим поставки для одного продукта, который не поддерживается другим продуктом.  

После выбора нового способа поставки отображается страница проводки. Для просмотра нового выбора режима поставки выберите вкладку **Поставка** в списке проводок.   