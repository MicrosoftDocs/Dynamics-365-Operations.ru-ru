---
title: Номенклатуры без запасов могут быть оформлены
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том, что клиенты могут добавлять номенклатуры, отсутствующие на складе, в корзину и перейти к оформлению заказа.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6df9c77248c7f4e16765b98327fe5838f0fce7e4
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585499"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="f7bd2-103">Номенклатуры без запасов могут быть оформлены</span><span class="sxs-lookup"><span data-stu-id="f7bd2-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7bd2-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том, что клиенты могут добавлять номенклатуры, отсутствующие на складе, в корзину и перейти к оформлению заказа.</span><span class="sxs-lookup"><span data-stu-id="f7bd2-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="f7bd2-105">описание</span><span class="sxs-lookup"><span data-stu-id="f7bd2-105">Description</span></span>

<span data-ttu-id="f7bd2-106">Пользователи могут добавить номенклатуру в корзину, даже если в магазине нет запасов в наличии, а затем перейти на страницу извлечения.</span><span class="sxs-lookup"><span data-stu-id="f7bd2-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="f7bd2-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="f7bd2-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="f7bd2-108">Включение свойства Показывать ошибки "Нет в наличии" в конструкторе сайтов Commerce</span><span class="sxs-lookup"><span data-stu-id="f7bd2-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="f7bd2-109">Чтобы включить свойства **Показывать ошибки "Нет в наличии"** в конструкторе сайтов Commerce, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="f7bd2-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f7bd2-110">Выберите сайт, с которым вы работаете в данный момент.</span><span class="sxs-lookup"><span data-stu-id="f7bd2-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="f7bd2-111">В левой области переходов выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="f7bd2-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="f7bd2-112">Выберите **Страница корзины**, чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="f7bd2-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="f7bd2-113">Выберите **Корзина 1**, выберите **Изменить**, а затем в области свойств установите флажок **Показывать ошибки "Нет в наличии"**.</span><span class="sxs-lookup"><span data-stu-id="f7bd2-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="f7bd2-114">Сохраните и опубликуйте страницу.</span><span class="sxs-lookup"><span data-stu-id="f7bd2-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7bd2-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f7bd2-115">Additional resources</span></span>

[<span data-ttu-id="f7bd2-116">Применение настроек запасов</span><span class="sxs-lookup"><span data-stu-id="f7bd2-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="f7bd2-117">Расчет наличия запасов для розничных каналов</span><span class="sxs-lookup"><span data-stu-id="f7bd2-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="f7bd2-118">Настройка буферов запасов и уровней запасов</span><span class="sxs-lookup"><span data-stu-id="f7bd2-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
