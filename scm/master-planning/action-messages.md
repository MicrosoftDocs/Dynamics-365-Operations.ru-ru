---
title: "недокументированные"
description: "Сообщение по действию — это созданное системой предложение изменить существующий Спланированный или подтвержденный заказ."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 21 - 54
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f2ac69ddf485139b057dafa20e5f1a961fc32067
ms.lasthandoff: 03/29/2017


---

# <a name="undocumented"></a>недокументированные

Сообщение по действию — это созданное системой предложение изменить существующий Спланированный или подтвержденный заказ.

### <a name="introduction"></a>Введение

Сообщения по действию создаются расчетом сводного планирования в ответ на изменение потребностей. Например, дата или количество отгрузки могут изменить в заказе на продажу, для которого вы уже создали заказ на покупку, чтобы выполнить требование. В этом случае одно или несколько сообщений по действиям создаются расчетом сводного планирования, чтобы обновить заказ на покупку. Вы решаете, нужно ли выполнять предлагаемые изменения.

Можно настроить, как сообщения по действиям рассчитываются для группы покрытия, присоединенной к номенклатуре.

 <a name="selecting-action-messages"></a>Выбор сообщений по действиям
==========================

На странице **Группы покрытия** можно выбрать сообщения по действиям, которые система должна создать, и группы покрытия или номенклатуры, к которым применяются сообщения. Можно выбрать следующие сообщения по действиям.

| Сообщение             | Описание                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ускорение**         | Если вы выбираете это сообщение, при необходимости система создаст сообщения действия, чтобы переместить заказ на более раннюю дату. В поле **Резерв ускорения** можно также указать максимальное число дней между приходом и выдачей без действия ускорения. |
| **Отсрочка**        | Если вы выбираете это сообщение, при необходимости система создаст сообщения действия, чтобы переместить заказ на более позднюю дату. В поле **Резерв отсрочки** можно указать максимальное число дней между приходом и выдачей без действия отсрочки.       |
| **Сокращение**        | Если вы выбираете это сообщение, производственные заказы, заказы на покупку и другие проводки по приходу должны быть уменьшены для предотвращения избыточного уровня запасов.                                                                                                   |
| **Увеличение**        | Если вы выбираете это сообщение, производственные заказы, заказы на покупку и другие проводки по приходу должны быть увеличены для предотвращения недостаточного уровня запасов.                                                                                                    |
| **Производные действия** | Если вы выбираете это сообщение, создаются сообщения по действиям для производных требований, например действий для заказов компонентов для удовлетворения требований производства.                                                                                                   |



