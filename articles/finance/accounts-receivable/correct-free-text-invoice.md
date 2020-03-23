---
title: Корректировка накладной с произвольным текстом
description: Эта статья описывает порядок коррекции накладной с произвольным текстом, которая была разнесена, и повторно выпуск ее как исправленной накладной.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf6e7a070d7c151c6ff5d868f4f916359b82683
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031000"
---
# <a name="correct-a-free-text-invoice"></a>Корректировка накладной с произвольным текстом

[!include [banner](../includes/banner.md)]

Эта статья описывает порядок коррекции накладной с произвольным текстом, которая была разнесена, и повторно выпуск ее как исправленной накладной.

Чтобы исправить накладную с произвольным текстом, которая уже была разнесена, откройте разнесенную накладную с произвольным текстом. На странице **Накладная** выберите **Отмена**, затем выберите **Исправить накладную**. Выберите код причины, добавьте комментарии и выберите дату для новой исправленной накладной. Исправленную накладную можно изменить и разнести. 

При разноске исправленной накладной отменяющая накладная создается для суммы кредита, равной сумме исходной накладной. Таким образом, объединенное сальдо исходной и отменяющей накладной равно 0. Отменяющая накладная сопоставляется с исходной накладной. 

После разноски исправленной накладной будет доступно три накладных:

-   **Исходная накладная** — накладная, включающая сведения, которые исправляются.
-   **Отменяющая накладная** — создаваемая системой накладная, служащая для отмены исправляемой накладной.
-   **Исправленная накладная** — накладная, которая содержит исправленные данные.

Вы можете определить отменяющую и корректирующую накладные двумя способами:

-   На странице **Все накладные с произвольным текстом** есть столбец **Корректировка**, где можно просмотреть, какие накладные являются отменяющими, а какие корректирующими.
-   В заголовке накладной с произвольным текстом отображается статус **Отменяющая накладная "\[номер накладной\]"** или **Исправленная накладная "\[номер накладной\]"**.

> [!NOTE]
> Эта функция доступна, только если выбран конфигурационный ключ **Исправление накладной с произвольным текстом**. Дополнительные сведения о том, как включить конфигурационные ключи, см. раздел "Включение (или отключение) ключей конфигурации" в теме [Режим обслуживания](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md). 


