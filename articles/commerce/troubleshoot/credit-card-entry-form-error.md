---
title: Страница запись кредитной карты отображает ошибку при оформлении заказа
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том случае, когда раздел "Способ платежа" не загружен и отображается сообщение об ошибке.
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
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018514"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="4f826-103">Страница запись кредитной карты отображает ошибку при оформлении заказа</span><span class="sxs-lookup"><span data-stu-id="4f826-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f826-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том случае, когда раздел **Способ платежа** не загружен и отображается сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4f826-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="4f826-105">описание</span><span class="sxs-lookup"><span data-stu-id="4f826-105">Description</span></span>

<span data-ttu-id="4f826-106">При открытии страницы оформления заказа Интернет-магазина раздел **Способ платежа** не загружается, и отображается следующее сообщение об ошибке: "Возникла ошибка.</span><span class="sxs-lookup"><span data-stu-id="4f826-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="4f826-107">Повторите попытку позже".</span><span class="sxs-lookup"><span data-stu-id="4f826-107">Please try again later."</span></span>

![Ошибка модуля платежа](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="4f826-109">Приказ</span><span class="sxs-lookup"><span data-stu-id="4f826-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="4f826-110">Подождите, пока истечет срок действия кэша Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="4f826-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="4f826-111">Параметры службы платежа на странице оформления заказа в Интернет-магазине кэшируются в Commerce Scale Unit, и их отображение на сайте электронной коммерции может занять до 15 минут.</span><span class="sxs-lookup"><span data-stu-id="4f826-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="4f826-112">Эти параметры службы платежа включают изменения кода счета продавца, ключа облачного API и различных параметров конфигурации, которые относятся к методу оплаты.</span><span class="sxs-lookup"><span data-stu-id="4f826-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f826-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4f826-113">Additional resources</span></span>

[<span data-ttu-id="4f826-114">Настройка канала онлайн-торговли</span><span class="sxs-lookup"><span data-stu-id="4f826-114">Set up an online channel</span></span>](../channel-setup-online.md)
