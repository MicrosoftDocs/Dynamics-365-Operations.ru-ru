---
title: Налоги по интернет-заказам рассчитываются неправильно
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь при неправильном расчете налогов в интернет-заказах, или когда налоговая группа в строке продаж настроена неправильно.
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
ms.openlocfilehash: 421df7545e285950ef8a3c4b753c8c6dc5f26422
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585497"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="68500-103">Налоги по интернет-заказам рассчитываются неправильно</span><span class="sxs-lookup"><span data-stu-id="68500-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="68500-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь при неправильном расчете налогов в интернет-заказах, или когда налоговая группа в строке продаж настроена неправильно.</span><span class="sxs-lookup"><span data-stu-id="68500-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="68500-105">описание</span><span class="sxs-lookup"><span data-stu-id="68500-105">Description</span></span>

<span data-ttu-id="68500-106">При размещении заказа электронной коммерции налоги рассчитываются неправильно или налоговая группа в строке продаж настроена неправильно.</span><span class="sxs-lookup"><span data-stu-id="68500-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="68500-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="68500-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="68500-108">Настройте налог для розничного магазина в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="68500-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="68500-109">Чтобы настроить налог для розничного магазина в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="68500-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="68500-110">Перейдите в раздел **Retail и Commerce \> Каналы \> Все магазины**.</span><span class="sxs-lookup"><span data-stu-id="68500-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="68500-111">Выберите магазин, для которого необходимо настроить налог.</span><span class="sxs-lookup"><span data-stu-id="68500-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="68500-112">На экспресс-вкладке **Общие** в разделе **налог** настройте сведения о налогах для магазина.</span><span class="sxs-lookup"><span data-stu-id="68500-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="68500-113">Для самовывоза продуктов из магазина налоговая группа берется из магазина, выбранного для самовывоза.</span><span class="sxs-lookup"><span data-stu-id="68500-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="68500-114">Дополнительные сведения см. в [Задание других параметров налогов для магазинов](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="68500-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="68500-115">Настройте налог для адреса клиента в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="68500-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="68500-116">Чтобы настроить налог для адреса клиента в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="68500-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="68500-117">Перейдите в раздел **Расчеты с клиентами \> Клиенты \> Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="68500-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="68500-118">Выберите клиента, для которого нужно настроить налоги.</span><span class="sxs-lookup"><span data-stu-id="68500-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="68500-119">На экспресс-вкладке **адреса** выберите адрес для настройки налогов, выберите пункт **Дополнительные параметры**, а затем выберите **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="68500-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="68500-120">На экспресс-вкладке **Общие** выберите **Налоговая группа**.</span><span class="sxs-lookup"><span data-stu-id="68500-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="68500-121">Выберите в поле **Налог** выберите подходящее значение.</span><span class="sxs-lookup"><span data-stu-id="68500-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="68500-122">Для отгрузки, которая включает налог на адрес клиента, адрес поставки строки определяет налоговую группу для строки.</span><span class="sxs-lookup"><span data-stu-id="68500-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="68500-123">Если клиент отправляет товар на существующий адрес, для которого уже настроена налоговая группа, будет использована существующая налоговая группа.</span><span class="sxs-lookup"><span data-stu-id="68500-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="68500-124">По умолчанию в создаваемых адресах не указана налоговая группа.</span><span class="sxs-lookup"><span data-stu-id="68500-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="68500-125">Настройка общих налоговых групп в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="68500-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="68500-126">Чтобы настроить общие налоговые группы в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="68500-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="68500-127">Перейдите в раздел **Налог \> Косвенные налоги \> Налог \> Налоговые группы**.</span><span class="sxs-lookup"><span data-stu-id="68500-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="68500-128">В левой области переходов выберите налоговую группу для настройки.</span><span class="sxs-lookup"><span data-stu-id="68500-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="68500-129">На экспресс-вкладке **Налог на основе розничной торговли** настройте налоги для налоговой группы.</span><span class="sxs-lookup"><span data-stu-id="68500-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="68500-130">Для отгрузки, которая не затрагивает налог по адресу клиента, адрес поставки для строки и налоги по месту назначения, настроенные для налоговой группы, определяют налоговую группу.</span><span class="sxs-lookup"><span data-stu-id="68500-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="68500-131">Дополнительные сведения см. в разделе [Настройка налогов для интернет-магазинов на основе места назначения](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="68500-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68500-132">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="68500-132">Additional resources</span></span>

[<span data-ttu-id="68500-133">Настройка налога для интернет-заказов</span><span class="sxs-lookup"><span data-stu-id="68500-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
