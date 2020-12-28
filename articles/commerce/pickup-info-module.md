---
title: Модуль сведений о самовывозе
description: В этом разделе описывается модуль сведений о самовывозе, а также описывается, как добавить его на страницы оформления заказа в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 61b97d72b6a397737c10476cd6c02764e60f10b1
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665356"
---
# <a name="pickup-information-module"></a><span data-ttu-id="0604c-103">Модуль сведений о самовывозе</span><span class="sxs-lookup"><span data-stu-id="0604c-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0604c-104">В этом разделе описывается модуль сведений о самовывозе, а также описывается, как добавить его на страницы оформления заказа в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0604c-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0604c-105">Модуль сведений о самовывозе может использоваться в модуле оформления заказа для отображения сведений о самовывозе заказа.</span><span class="sxs-lookup"><span data-stu-id="0604c-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="0604c-106">Клиенты могут просматривать доступные даты и временные интервалы самовывоза, а затем выбирать подходящее время для получения их заказа.</span><span class="sxs-lookup"><span data-stu-id="0604c-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="0604c-107">Например, клиент может выбрать забрать заказ в 15:00 21 марта из магазина в Сан-Франциско.</span><span class="sxs-lookup"><span data-stu-id="0604c-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="0604c-108">Временные интервалы получения для соответствующих магазинов необходимо настроить в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0604c-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="0604c-109">Дополнительные сведения см. в разделе [Создание и обновление временных интервалов для самовывоза клиентом](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="0604c-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="0604c-110">Если модуль сведений о самовывозе создается на странице оформления заказа, но для магазина, выбранного для получения, не определен ни один из временных интервалов, то в модуле будут показаны сведения, но пользователь не сможет выбрать какие-либо временные интервалы.</span><span class="sxs-lookup"><span data-stu-id="0604c-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="0604c-111">Временные интервалы являются необязательными и не требуются для размещения заказа.</span><span class="sxs-lookup"><span data-stu-id="0604c-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="0604c-112">Если для получения в нескольких магазинах выбрано несколько номенклатур, в модуле сведений о самовывозе будет разрешено пользователю выбрать временной интервал для каждого магазина, при условии, что для него доступны временные интервалы.</span><span class="sxs-lookup"><span data-stu-id="0604c-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="0604c-113">Поддержка временных интервалов и модуля информации о самовывозе при оформлении заказа доступна в Dynamics 365 Commerce версии 10.0.15 и выше.</span><span class="sxs-lookup"><span data-stu-id="0604c-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="0604c-114">На следующем рисунке показан пример выбора временного интервала с помощью модуля сведений о самовывозе на странице оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="0604c-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Пример модуля сведений о самовывозе на странице оформления заказа](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="0604c-116">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="0604c-116">Module properties</span></span>

- <span data-ttu-id="0604c-117">**Заголовок** — введите заголовок для модуля.</span><span class="sxs-lookup"><span data-stu-id="0604c-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="0604c-118">Отображение сведений о временном интервале после размещения заказа</span><span class="sxs-lookup"><span data-stu-id="0604c-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="0604c-119">После размещения заказа сведения о выбранном временном интервале можно просмотреть в [модуле подтверждения заказа](order-confirmation-module.md) и в [модуле сведений о заказе](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="0604c-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="0604c-120">Оба этих модуля имеют свойство **Показать сведения о временном интервале**.</span><span class="sxs-lookup"><span data-stu-id="0604c-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="0604c-121">Чтобы можно было показать выбранный временной интервал во время процесса заказа, этому свойству должно быть присвоено значение **True**.</span><span class="sxs-lookup"><span data-stu-id="0604c-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="0604c-122">Добавление модуля сведений о самовывозе при оформления заказа на страницу</span><span class="sxs-lookup"><span data-stu-id="0604c-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="0604c-123">Инструкции о порядке добавления модуля сведений о самовывозе на страницу оформления заказа и задания требуемых свойств см. в разделе [Модуль оформления заказа](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="0604c-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="0604c-124">На следующем рисунке показан пример страницы оформления заказа электронной коммерции, которая включает временные интервалы для номенклатур строк с самовывозом.</span><span class="sxs-lookup"><span data-stu-id="0604c-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![Пример страницы оформления заказа электронной коммерции, которая включает временные интервалы для номенклатур строк с самовывозом](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="0604c-126">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0604c-126">Additional resources</span></span>

[<span data-ttu-id="0604c-127">Создание и обновление временных интервалов для самовывоза клиентами</span><span class="sxs-lookup"><span data-stu-id="0604c-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="0604c-128">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="0604c-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0604c-129">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="0604c-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0604c-130">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="0604c-130">Order details module</span></span>](account-management.md)
