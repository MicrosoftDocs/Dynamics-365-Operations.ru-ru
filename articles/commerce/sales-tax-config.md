---
title: Настройка налога для интернет-заказов
description: В этом разделе представлен обзор выбора налоговой группы для различных типов интернет-заказов в Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 36dd3e8a3d47f02eed5b9c8bb79d773d98069376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254849"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="cd4c5-103">Настройка налога для интернет-заказов</span><span class="sxs-lookup"><span data-stu-id="cd4c5-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cd4c5-104">В этом разделе представлен обзор выбора налоговой группы для различных типов интернет-заказов.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="cd4c5-105">Вам может требоваться, чтобы канал электронной коммерции поддерживал такие возможности, как доставка или самовывоз для интернет-заказов.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="cd4c5-106">Применимость налога базируется на параметре, выбранном интернет-пользователями.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="cd4c5-107">Когда клиент сайта выбирает купить номенклатуру по Интернету с доставкой по некоторому адресу, налог определяется на основе настройки налоговой группы адреса доставки клиента.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="cd4c5-108">Когда клиент решает сам забрать купленную номенклатуру в магазине, налог определяется на основе настройки налоговой группы магазина самовывоза.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="cd4c5-109">Заказы, отгруженные по адресу клиента</span><span class="sxs-lookup"><span data-stu-id="cd4c5-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="cd4c5-110">В общем случае налоги для интернет-заказов, доставляемых по адресу клиентов, определяются пунктом назначения.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="cd4c5-111">Каждая налоговая группа имеет конфигурацию налога на основе места назначения розничной доставки, в которой предприятие может определить сведения о месте назначения, такие как страна/регион, область, район и город в иерархической форме.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="cd4c5-112">При размещении интернет-заказа налоговый механизм Commerce использует адрес доставки каждой номенклатуры строки в заказе и находит налоговые группы с соответствующими критериями налогов на основе пункта назначения.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="cd4c5-113">Например, для интернет-заказа с адресом поставки номенклатуры строки в Сан-Франциско, Калифорния, налоговая система найдет налоговую группу и налоговый код для Калифорнии, а затем рассчитает налог для каждой номенклатуры строки соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="cd4c5-114">Налоговые группы на основе клиентов</span><span class="sxs-lookup"><span data-stu-id="cd4c5-114">Customer-based tax groups</span></span>

<span data-ttu-id="cd4c5-115">В Commerce Headquarters имеются два места, где настраиваются налоговые группы клиентов:</span><span class="sxs-lookup"><span data-stu-id="cd4c5-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="cd4c5-116">**Профиль клиента**</span><span class="sxs-lookup"><span data-stu-id="cd4c5-116">**Customer's profile**</span></span>
- <span data-ttu-id="cd4c5-117">**Адрес доставки для клиента**</span><span class="sxs-lookup"><span data-stu-id="cd4c5-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="cd4c5-118">Если для профиля клиента настроена налоговая группа</span><span class="sxs-lookup"><span data-stu-id="cd4c5-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="cd4c5-119">Для записи профиля клиента в Headquarters можно настроить налоговую группу, однако для интернет-заказов налоговая группа, настроенная в профиле клиента, не будет использоваться налоговой системой.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="cd4c5-120">Если для адреса доставки для клиента настроена налоговая группа</span><span class="sxs-lookup"><span data-stu-id="cd4c5-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="cd4c5-121">Если для записи адреса доставки для клиента настроена налоговая группа и интернет-заказ (или номенклатура строки) отгружается в адрес доставки клиента, то налоговая группа, настроенная в записи адреса клиента, будет использоваться налоговым модулем для расчета налогов.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="cd4c5-122">Настройка налоговой группы для записи адреса доставки для клиента</span><span class="sxs-lookup"><span data-stu-id="cd4c5-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="cd4c5-123">Чтобы настроить налоговую группу для записи адреса доставки для клиента в Commerce Headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="cd4c5-124">Перейдите в раздел **Все клиенты**, затем выберите нужного клиента.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="cd4c5-125">На экспресс-вкладке **Адреса** выберите нужный адрес, затем выберите **Дополнительные параметры \> Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="cd4c5-126">На вкладке **Общие** на странице **Управление адресами** задайте требуемое значение налога.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="cd4c5-127">Налоговая группа определяется с использованием адреса доставки строки заказа, а налоги по месту назначения настраиваются в самой налоговой группе.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="cd4c5-128">Дополнительные сведения см. в разделе [Настройка налогов для интернет-магазинов на основе места назначения](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="cd4c5-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="cd4c5-129">Получение заказа в магазине</span><span class="sxs-lookup"><span data-stu-id="cd4c5-129">Order pickup in store</span></span>

<span data-ttu-id="cd4c5-130">Для строк заказа с указанным получением в магазине или в окне выдачи будет применяться налоговая группа из выбранного магазина самовывоза.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="cd4c5-131">Дополнительные сведения о настройке налоговой группы для данного магазина см. в разделе [Задание других параметров налогов для магазинов](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="cd4c5-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="cd4c5-132">Когда строка заказа получается самовывозом в магазине, параметры налога по адресу клиента (если настроены) игнорируются налоговым модулем, и будет применена конфигурация налога для магазина получения заказа.</span><span class="sxs-lookup"><span data-stu-id="cd4c5-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="cd4c5-133">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cd4c5-133">Additional resources</span></span>

[<span data-ttu-id="cd4c5-134">Обзор налога</span><span class="sxs-lookup"><span data-stu-id="cd4c5-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="cd4c5-135">Методы расчета налога в поле "Основание"</span><span class="sxs-lookup"><span data-stu-id="cd4c5-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="cd4c5-136">Назначение и переопределения налога</span><span class="sxs-lookup"><span data-stu-id="cd4c5-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="cd4c5-137">Параметры расчета "Полная сумма" и "Интервал" для налоговых кодов</span><span class="sxs-lookup"><span data-stu-id="cd4c5-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="cd4c5-138">Расчет налогового освобождения</span><span class="sxs-lookup"><span data-stu-id="cd4c5-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]