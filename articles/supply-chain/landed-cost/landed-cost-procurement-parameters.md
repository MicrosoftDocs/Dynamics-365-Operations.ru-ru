---
title: Параметры модуля "Закупки и источники" для стоимости на складе
description: В этом разделе описывается, как настроить соответствующие параметры закупок и источников при использовании модуля стоимости на складе.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 49e046a1437917cfa866f690511789496fac2c53
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500750"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="85776-103">Параметры модуля "Закупки и источники" для стоимости на складе</span><span class="sxs-lookup"><span data-stu-id="85776-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="85776-104">На странице **Параметры модуля "Закупки и источники"** есть несколько настроек, которые особенно подходят при использовании модуля **Стоимость на складе**.</span><span class="sxs-lookup"><span data-stu-id="85776-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="85776-105">Используйте диалоговое окно **Обновление строк заказа**, которое открывается со страницы **Параметры модуля "Закупки и источники"**, чтобы указать, должны ли строки заказа на покупку автоматически обновляться при внесении изменений в заголовок заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="85776-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="85776-106">Чтобы завершить эту настройку, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="85776-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="85776-107">Выберите **Закупки и источники \> Настройка \> Параметры модуля "Закупки и источники"**.</span><span class="sxs-lookup"><span data-stu-id="85776-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="85776-108">На вкладке **Общее** выберите ссылку **Обновление строк заказа**.</span><span class="sxs-lookup"><span data-stu-id="85776-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="85776-109">В диалоговом окне **Обновление строк заказа** перечислены поля в заголовке заказа, которые также могут применяться при автоматическом обновлении к соответствующим полям в строках заказа.</span><span class="sxs-lookup"><span data-stu-id="85776-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="85776-110">Задайте в каждом поле в списке одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="85776-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="85776-111">**Всегда** — строки заказа должны обновляться автоматически при обновлении заголовка заказа.</span><span class="sxs-lookup"><span data-stu-id="85776-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="85776-112">**Никогда** — строки заказа не должны никогда обновляться при обновлении заголовка заказа.</span><span class="sxs-lookup"><span data-stu-id="85776-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="85776-113">**Запрос** — пользователю будет предложено указать, следует ли обновлять строки заказа.</span><span class="sxs-lookup"><span data-stu-id="85776-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
