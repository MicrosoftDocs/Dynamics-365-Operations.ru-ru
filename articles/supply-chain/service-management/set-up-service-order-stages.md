---
title: Настройка этапов заказа на обслуживания
description: Настройка этапов заказа на обслуживания.
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 557e688ddd1155aa475320365a5b6048759904fd
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670730"
---
# <a name="set-up-service-order-stages"></a>Настройка этапов заказа на обслуживания 

[!include [banner](../includes/banner.md)]


1.  Перейдите **Управление сервисным обслуживанием** \> **Настройка** \> **Заказы на обслуживание** \> **Этапы сервисного обслуживания**.

2.  Выберите **Создать** для создания новой записи.

3.  В полях **Этап сервисного обслуживания** и **Описание** укажите код и описание этапа обслуживания.

4.  Выберите соответствующие параметры для этапа.

5.  Выберите для текущего этапа родительский этап или оставьте поле **Родитель** пустым, если данный этап является начальным в настройке этапов.


> [!NOTE]
> <P>После сохранения этапа поле <STRONG>Родитель</STRONG> изменить невозможно. Вместо этого следует удалить запись и снова создать запись с другим значением в поле <STRONG>Родитель</STRONG>.</P>
> <P>Кроме того, можно создать только один этап с пустым полем <STRONG>Родитель</STRONG>. Другими словами, разрешено создание только одного начального этапа.</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]