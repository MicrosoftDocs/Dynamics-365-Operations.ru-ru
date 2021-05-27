---
title: Платежи автоматически сопоставляются до выставления накладных или отгрузки заказов
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь при сопоставлении платежа в портале Adyen сразу после размещения заказа, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018268"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="18619-103">Платежи автоматически сопоставляются до выставления накладных или отгрузки заказов</span><span class="sxs-lookup"><span data-stu-id="18619-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18619-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь при сопоставлении платежа в портале Adyen сразу после размещения заказа, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.</span><span class="sxs-lookup"><span data-stu-id="18619-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="18619-105">описание</span><span class="sxs-lookup"><span data-stu-id="18619-105">Description</span></span>

<span data-ttu-id="18619-106">После размещения заказа платеж сразу сопоставляется в портале Adyen, даже если по заказу на продажу не выставлены накладные или не выполнена отгрузка.</span><span class="sxs-lookup"><span data-stu-id="18619-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="18619-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="18619-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="18619-108">Настройка регистрации вручную для платежей электронной коммерции на портале Adyen</span><span class="sxs-lookup"><span data-stu-id="18619-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="18619-109">Чтобы настроить регистрацию вручную для платежей электронной коммерции на портале Adyen, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="18619-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="18619-110">Выполните вход на портал Adyen.</span><span class="sxs-lookup"><span data-stu-id="18619-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="18619-111">В верхнем правом углу выберите счет продавца для канала электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="18619-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="18619-112">На верхней панели навигации выберите **Учетная запись**, а затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="18619-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="18619-113">В поле **Задержка регистрации** выберите **вручную**.</span><span class="sxs-lookup"><span data-stu-id="18619-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Параметр "Задержка регистрации" на портале Adyen](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="18619-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="18619-115">Additional resources</span></span>

[<span data-ttu-id="18619-116">Регистрация платежа Adyen</span><span class="sxs-lookup"><span data-stu-id="18619-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="18619-117">Соединитель платежей Dynamics 365 для Adyen</span><span class="sxs-lookup"><span data-stu-id="18619-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="18619-118">Настройка соединителя платежей Adyen для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="18619-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
