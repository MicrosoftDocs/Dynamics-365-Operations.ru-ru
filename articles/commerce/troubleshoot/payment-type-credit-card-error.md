---
title: Ошибка "Тип оплаты должен быть кредитной картой" на странице заказа на продажу
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь при появлении сообщения об ошибке на странице заказа на продажу после синхронизации заказа.
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
ms.openlocfilehash: 5be19949e9d1dbc43fdd3e6def119effa50a34d0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018418"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="6f65a-103">Ошибка "Тип оплаты должен быть кредитной картой" на странице заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="6f65a-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f65a-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь при появлении сообщения об ошибке на странице заказа на продажу после синхронизации заказа.</span><span class="sxs-lookup"><span data-stu-id="6f65a-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="6f65a-105">описание</span><span class="sxs-lookup"><span data-stu-id="6f65a-105">Description</span></span>

<span data-ttu-id="6f65a-106">При открытии страницы заказа на продажу после синхронизации заказа появляется следующее сообщение об ошибке: "Тип оплаты должен быть кредитной картой, так как указан номер кредитной карты".</span><span class="sxs-lookup"><span data-stu-id="6f65a-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Ошибка "Тип оплаты должен быть кредитной картой"](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="6f65a-108">Приказ</span><span class="sxs-lookup"><span data-stu-id="6f65a-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="6f65a-109">Настройка типа платежа в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="6f65a-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="6f65a-110">Перейдите в раздел **Расчеты с клиентами \> Настройка платежей \> Условия оплаты**.</span><span class="sxs-lookup"><span data-stu-id="6f65a-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="6f65a-111">В левой области переходов выберите условия оплаты.</span><span class="sxs-lookup"><span data-stu-id="6f65a-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="6f65a-112">Убедитесь, что в поле **Тип платежа** выбрана **кредитная карта**.</span><span class="sxs-lookup"><span data-stu-id="6f65a-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f65a-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6f65a-113">Additional resources</span></span>

[<span data-ttu-id="6f65a-114">Разноска интернет-продаж и платежей</span><span class="sxs-lookup"><span data-stu-id="6f65a-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
