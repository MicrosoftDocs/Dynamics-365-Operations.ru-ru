---
title: Настройка этапов заказа на обслуживания
description: Настройка этапов заказа на обслуживания.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9aca699283a9de6ea551bd02184498aed88143e9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991648"
---
# <a name="set-up-service-order-stages"></a>Настройка этапов заказа на обслуживания 

[!include [banner](../includes/banner.md)]


1.  Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Заказы на обслуживание** \> **Этапы сервисного обслуживания**.

2.  Нажмите клавиши CTRL+N, чтобы создать новую запись.

3.  В полях **Этап сервисного обслуживания** и **Описание** укажите код и описание этапа обслуживания.

4.  Выберите соответствующие параметры для этапа.

5.  Выберите для текущего этапа родительский этап или оставьте поле **Родитель** пустым, если данный этап является начальным в настройке этапов.


> [!NOTE]
> <P>После сохранения этапа поле <STRONG>Родитель</STRONG> изменить невозможно. Вместо этого следует удалить запись и снова создать запись с другим значением в поле <STRONG>Родитель</STRONG>.</P>
> <P>Кроме того, можно создать только один этап с пустым полем <STRONG>Родитель</STRONG>. Другими словами, разрешено создание только одного начального этапа.</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]