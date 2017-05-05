---
title: "Инфокоды"
description: "В этой статье приводится обзор инфокодов, групп инфокодов и способов их использования."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d463d4ac9b4258c2282dc70547145ce38e4e8e98
ms.lasthandoff: 03/31/2017


---

# <a name="info-codes"></a>Инфокоды

[!include[banner](includes/banner.md)]


В этой статье приводится обзор инфокодов, групп инфокодов и способов их использования.

С помощью инфокодов можно выполнить сбор данных в ККМ POS. Инфокоды можно использовать для отправки запроса кассиру на ввод сведений во время различных действий в POS, например при продаже номенклатуры, возврате номенклатуры или выбор клиентов. Кассиры могут выбрать сведения из списка или ввести их в виде кода, числа, даты или текста. Инфокоды можно назначить предварительно заданным действиям в магазине, розничной номенклатуре, способам оплаты, клиентам и конкретным операциям POS. Инфокоды позволяют выполнять следующие действия.
-   Получение дополнительных сведений во временя проводки, например номер рейса или причина возврата.
-   Выдача запроса кассиру ККМ на выбор из прейскуранта цены для конкретных продуктов.
-   Связь дополнительного кода с инфокодом, чтобы выдавать запрос кассиру на ввод тех или иных данных во время определенного действия. Например, если клиент возвращает продукт, можно отправить кассиру запрос на указание причин возврата продукта. Также дополнительные коды можно использовать для отображения списка причин, в котором кассир может сделать выбор.
-   Продажа продукта как продукта с обычной ценой, ценой со скидкой или бесплатного продукта.
-   Выдача запроса кассиру на ввод значения или выбор значения из списка дополнительных кодов при открытии ящика ККМ без выполнения операции продажи.

## <a name="info-codes-group-in-retail-and-commerce"></a>Группа инфокодов в модуле "Розничная торговля и коммерция"
В модуле Dynamics 365 for Operations – Retail можно создавать группы информационных кодов. Группы инфокодов добавляют гибкость работе, позволяя определять меньше инфокодов, а затем использовать их более разнообразными способами. Группы инфокодов можно использовать следующими способами.
-   Для определения меньшего числа инфокодов для более простого повторного использования. Инфокоды, включенные в группу инфокодов, не имеют предварительно определенных зависимостей от других инфокодов. Один и тот же инфокод можно включить в несколько групп инфокодов, а затем использовать приоритет для представления одинаковых инфокодов в заказе с учетом любой конкретной ситуации.
-   Для связи инфокодов с другими инфокодами или группами инфокодов для сбора сведений о продукте или проводке без необходимости определения отдельного инфокода или связанного инфокода для каждого сценария.

## <a name="info-code-examples"></a>Примеры инфокодов
**Пример 1. Повторное использование инфокодов.** Можно связать инфокоды таким образом, чтобы при запуске одного инфокода сразу же запускался другой инфокод. Например, при продаже некоторых продуктов можно отправить кассиру запрос на то, чтобы он узнал у клиента, хочет ли тот приобрести батарейки и гарантию на продукт. При продаже других продуктов можно отправить кассиру запрос на то, чтобы он узнал у клиента, хочет ли тот приобрести батарейки, и узнал у него почтовый код. При создании связанных инфокодов для этих сценариев необходимо настроить каждое изменение инфокода таким образом, чтобы кассир спрашивал правильные сведения. При использовании групп инфокодов общие инфокоды, такие как вопрос про батарейки, можно настроить один раз и повторно использовать в нескольких группах инфокодов. Можно также установить приоритет в группах инфокодов для определения порядка отображения запросов. **Пример 2. Связывание инфокодов с группами инфокодов.** При продаже некоторых продуктов, например мобильных устройств, всегда необходимо выполнять сбор определенного набора данных, таких как номер телефона, идентификатор мобильного телефона (MEID) и серийный номер. Однако также требуется выполнять сбор определенной информации по планшетам и мобильным телефонам. Можно определить группу инфокодов, которая включает запросы на номер телефона, идентификатор MEID и серийный номер, а затем связать группу инфокодов с отдельным инфокодом. При активации определенного для продукта инфокода можно активировать группу инфокодов, чтобы иметь возможность выполнять сбор общих сведений, не определяя несколько наборов связанных инфокодов для каждого устройства.

 
-





