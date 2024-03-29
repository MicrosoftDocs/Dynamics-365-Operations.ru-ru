---
title: Отчеты по розничным ценам
description: В этой статье представлен обзор функции отчета по ценам, который можно использовать для просмотра предстоящих изменений цены на продукты, включенные в ассортимент.
author: ShalabhjainMSFT
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 09350d15660978126d36199a3b4e93f6be5fe157
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269036"
---
# <a name="retail-price-reports"></a>Отчеты по розничным ценам

[!include [banner](includes/banner.md)]


Для предоставления конкурентных цен своим клиентам предприятия розничной торговли часто изменяют цены продуктов. Менеджерам магазина требуется возможность легкого доступа к последним или предстоящим изменениям цен, чтобы они могли планировать необходимые ресурсы для обновления ценников, отображаемых на полках магазина. В версии 10.0 Retail менеджер магазина может открыть отчет **Цена**, перейдя в **Все магазины \> Магазин \> Отчет о цене** и просмотрев обновленные цены на продукты, связанные с магазином. 

Чтобы включить отчет о ценах, должен быть включен параметр **Включить отчет о ценах для магазина**. Этот параметр находится на вкладке **Параметры Commerce \> Скидки \> Разное**. При открытии страницы **Отчет о ценах** отображается диалоговое окно с различными конфигурациями. Ниже перечислены доступные конфигурации.

| Конфигурация | описание |
|---|---|
| Начальная дата / Конечная дата| Диапазон дат, для которого требуется создать отчет о ценах. Продолжительность в настоящее время ограничивается 7 днями. |
| Канал| Магазин, для которого требуется создать отчет о ценах. |
| Показать продукты с доступными запасами| Если установить **Да**, будут показаны цены только для тех продуктов, для которых в настоящее время в магазине имеются доступные физические складские запасы. |
| Показать цены для вариантов | Если установить **Да**, будут отображаться цены вариантов вместе с шаблонами продукта. Это должно быть включено **Вкл.** только при наличии разных цены за разные варианты, поскольку количество строк становится очень большим. В будущих выпусках мы обеспечим цены на основе аналитик, чтобы менеджер магазина мог выбрать измерения, по которым должны отображаться цены. |
| Показать продукты с изменениями цен | Если установить значение **Да**, будут отображаться цены только для тех дат, в которые цены были изменены. Цена за *один день до* выбранной даты **Начальная дата** всегда отображается, чтобы менеджер магазина мог легко выявить продукты, цены на которые не изменялись в течение всего выбранного периода, и также может просмотреть текущую цену. |

После создания отчета можно загрузить файл Excel для любой дополнительной требуемой фильтрации. Отчет о ценах может также использоваться для проверки журнала цен продуктов за прошедшие даты.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
