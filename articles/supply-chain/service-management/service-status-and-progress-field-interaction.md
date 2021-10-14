---
title: Взаимодействие статуса обслуживания и поля хода выполнения работ
description: В форме "Заказы на сервисное обслуживание" поле "Ход выполнения" под заголовком заказа на обслуживание отражает статус всего заказа на обслуживание, и указывает статус отдельных строк заказа на обслуживание.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0758c370fd1548770d596115b18f133071f3bbc0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566103"
---
# <a name="service-status-and-progress-field-interaction"></a>Взаимодействие статуса обслуживания и поля хода выполнения работ

[!include [banner](../includes/banner.md)]

В форме **Заказы на сервисное обслуживание** поле **Ход выполнения** под заголовком заказа на сервисное обслуживание отражает статус всего заказа на обслуживание, и указывает **Статус** отдельных строк заказа на обслуживание.

<table>
<colgroup>
<col />
<col />
<col />
<col />
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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
