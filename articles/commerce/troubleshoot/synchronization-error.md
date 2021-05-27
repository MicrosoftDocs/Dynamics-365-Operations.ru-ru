---
title: Ошибка синхронизации заказа, которая связана со службой платежей по умолчанию
description: В этом разделе содержатся инструкции по устранению неполадок, которые могут помочь исправить ошибку, которая может возникнуть при синхронизации интернет-заказов.
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021135"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="9edf6-103">Ошибка синхронизации заказа, которая связана со службой платежей по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9edf6-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9edf6-104">В этом разделе содержатся инструкции по устранению неполадок, которые могут помочь исправить ошибку, которая может возникнуть при синхронизации интернет-заказов.</span><span class="sxs-lookup"><span data-stu-id="9edf6-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="9edf6-105">описание</span><span class="sxs-lookup"><span data-stu-id="9edf6-105">Description</span></span>

<span data-ttu-id="9edf6-106">При синхронизации интернет-заказов появляется следующее сообщение об ошибке: "для обработки проводок кредитной карты должна использоваться служба платежей по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="9edf6-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Отсутствует ошибка службы платежа по умолчанию](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="9edf6-108">Приказ</span><span class="sxs-lookup"><span data-stu-id="9edf6-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="9edf6-109">Подтверждение или настройка службы платежа по умолчанию в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="9edf6-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="9edf6-110">Для подтверждения или настройки службы платежа по умолчанию в Commerce headquarters, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="9edf6-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9edf6-111">Перейдите в раздел **Расчеты с клиентами \> Настройка платежей \> Службы платежей**.</span><span class="sxs-lookup"><span data-stu-id="9edf6-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="9edf6-112">Убедитесь, что для параметра **Процессор по умолчанию для новых кредитных карт** установлен значение **Да** для одной службы платежей.</span><span class="sxs-lookup"><span data-stu-id="9edf6-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9edf6-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9edf6-113">Additional resources</span></span>

[<span data-ttu-id="9edf6-114">Настройка, авторизация и проверка данных кредитной карты</span><span class="sxs-lookup"><span data-stu-id="9edf6-114">Credit card setup, authorization, and capture</span></span>](../../finance/accounts-receivable/credit-card-authorizations.md)