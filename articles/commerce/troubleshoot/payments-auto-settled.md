---
title: Платежи автоматически сопоставляются до выставления накладных или отгрузки заказов
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь при сопоставлении платежа в портале Adyen сразу после размещения заказа, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.
author: Reza-Assadi
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
ms.openlocfilehash: 43fe90cf99ddbe42dc89685e7fc747ded5a285c0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801659"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="3d247-103">Платежи автоматически сопоставляются до выставления накладных или отгрузки заказов</span><span class="sxs-lookup"><span data-stu-id="3d247-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3d247-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь при сопоставлении платежа в портале Adyen сразу после размещения заказа, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.</span><span class="sxs-lookup"><span data-stu-id="3d247-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="3d247-105">описание</span><span class="sxs-lookup"><span data-stu-id="3d247-105">Description</span></span>

<span data-ttu-id="3d247-106">После размещения заказа платеж сразу сопоставляется в портале Adyen, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.</span><span class="sxs-lookup"><span data-stu-id="3d247-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="3d247-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="3d247-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="3d247-108">Настройка регистрации вручную для платежей электронной коммерции на портале Adyen</span><span class="sxs-lookup"><span data-stu-id="3d247-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="3d247-109">Чтобы настроить регистрацию вручную для платежей электронной коммерции на портале Adyen, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3d247-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="3d247-110">Выполните вход на портал Adyen.</span><span class="sxs-lookup"><span data-stu-id="3d247-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="3d247-111">В верхнем правом углу выберите счет продавца для канала электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="3d247-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="3d247-112">На верхней панели навигации выберите **Учетная запись**, а затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="3d247-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="3d247-113">В поле **Задержка регистрации** выберите **вручную**.</span><span class="sxs-lookup"><span data-stu-id="3d247-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Параметр "Задержка регистрации" на портале Adyen](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="3d247-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3d247-115">Additional resources</span></span>

[<span data-ttu-id="3d247-116">Регистрация платежа Adyen</span><span class="sxs-lookup"><span data-stu-id="3d247-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="3d247-117">Соединитель платежей Dynamics 365 для Adyen</span><span class="sxs-lookup"><span data-stu-id="3d247-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="3d247-118">Настройка соединителя платежей Adyen для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3d247-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
