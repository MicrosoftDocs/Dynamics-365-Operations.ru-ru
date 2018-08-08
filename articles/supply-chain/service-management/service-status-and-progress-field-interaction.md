---
title: "Взаимодействие статуса обслуживания и поля хода выполнения работ"
description: "В форме \"Заказы на сервисное обслуживание\" поле \"Ход выполнения\" под заголовком заказа на обслуживание отражает статус всего заказа на обслуживание, и указывает статус отдельных строк заказа на обслуживание."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 51ef39266e8de00488954918568d00a297a9b50a
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---


# <a name="service-status-and-progress-field-interaction"></a>Взаимодействие статуса обслуживания и поля хода выполнения работ 

[!include [banner](../includes/banner.md)]


В форме **Заказы на сервисное обслуживание** поле **Ход выполнения** под заголовком заказа на сервисное обслуживание отражает статус всего заказа на обслуживание, и указывает **Статус** отдельных строк заказа на обслуживание.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Прогресс</p></th>
<th><p>Статус по строке 1</p></th>
<th><p>Статус по строке 2</p></th>
<th><p>Статус по строке 3</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>В работе</strong></p></td>
<td><p><strong>Создано</strong></p></td>
<td><p><strong>Создано</strong></p></td>
<td><p><strong>Создано</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>В работе</strong></p></td>
<td><p><strong>Отменено</strong></p></td>
<td><p><strong>Создано</strong></p></td>
<td><p><strong>Создано</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>В работе</strong></p></td>
<td><p><strong>Создано</strong></p></td>
<td><p><strong>Отменено</strong></p></td>
<td><p><strong>Разнесено</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Отменено</strong></p></td>
<td><p><strong>Отменено</strong></p></td>
<td><p><strong>Отменено</strong></p></td>
<td><p><strong>Отменено</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Разнесено</strong></p></td>
<td><p><strong>Разнесено</strong></p></td>
<td><p><strong>Разнесено</strong></p></td>
<td><p><strong>Разнесено</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Разнесено</strong></p></td>
<td><p><strong>Разнесено</strong></p></td>
<td><p><strong>Отменено</strong></p></td>
<td><p><strong>Отменено</strong></p></td>
</tr>
</tbody>
</table>


Ход выполнения заказа на сервисное обслуживание обрабатывается, если все строки имеют статус **Создано**, он также обрабатывается, если некоторые строки имеют статус **Отменено** или **Разнесено**.

Если все строки заказа на сервисное обслуживание помечены как **Разнесено**, ход выполнения заказа на обслуживание имеет статус **Разнесено**. Если некоторые строки имеют статус **Разнесено**, а некоторые **Отменено**, ход выполнения по-прежнему будет иметь статус **Разнесено**.

  



