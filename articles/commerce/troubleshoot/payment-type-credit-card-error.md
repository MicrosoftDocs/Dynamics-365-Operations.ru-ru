---
title: Ошибка "Тип оплаты должен быть кредитной картой" на странице заказа на продажу
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь при появлении сообщения об ошибке на странице заказа на продажу после синхронизации заказа.
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
ms.openlocfilehash: eabc64acc74645c7e6c7c4ab5794ed9fdb9dc997
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801683"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="cc2fe-103">Ошибка "Тип оплаты должен быть кредитной картой" на странице заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="cc2fe-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc2fe-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь при появлении сообщения об ошибке на странице заказа на продажу после синхронизации заказа.</span><span class="sxs-lookup"><span data-stu-id="cc2fe-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="cc2fe-105">описание</span><span class="sxs-lookup"><span data-stu-id="cc2fe-105">Description</span></span>

<span data-ttu-id="cc2fe-106">При открытии страницы заказа на продажу после синхронизации заказа появляется следующее сообщение об ошибке: "Тип оплаты должен быть кредитной картой, так как указан номер кредитной карты".</span><span class="sxs-lookup"><span data-stu-id="cc2fe-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Ошибка "Тип оплаты должен быть кредитной картой"](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="cc2fe-108">Приказ</span><span class="sxs-lookup"><span data-stu-id="cc2fe-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="cc2fe-109">Настройка типа платежа в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="cc2fe-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="cc2fe-110">Перейдите в раздел **Расчеты с клиентами \> Настройка платежей \> Условия оплаты**.</span><span class="sxs-lookup"><span data-stu-id="cc2fe-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="cc2fe-111">В левой области переходов выберите условия оплаты.</span><span class="sxs-lookup"><span data-stu-id="cc2fe-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="cc2fe-112">Убедитесь, что в поле **Тип платежа** выбрана **кредитная карта**.</span><span class="sxs-lookup"><span data-stu-id="cc2fe-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc2fe-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cc2fe-113">Additional resources</span></span>

[<span data-ttu-id="cc2fe-114">Разноска интернет-продаж и платежей</span><span class="sxs-lookup"><span data-stu-id="cc2fe-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
