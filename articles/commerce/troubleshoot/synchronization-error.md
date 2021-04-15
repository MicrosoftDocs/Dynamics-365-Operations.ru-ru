---
title: Ошибка синхронизации заказа, которая связана со службой платежей по умолчанию
description: В этом разделе содержатся инструкции по устранению неполадок, которые могут помочь исправить ошибку, которая может возникнуть при синхронизации интернет-заказов.
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
ms.openlocfilehash: 45eeae751051b58e1c9e725eb4ed4b5240026e7f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801443"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="2d74d-103">Ошибка синхронизации заказа, которая связана со службой платежей по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2d74d-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2d74d-104">В этом разделе содержатся инструкции по устранению неполадок, которые могут помочь исправить ошибку, которая может возникнуть при синхронизации интернет-заказов.</span><span class="sxs-lookup"><span data-stu-id="2d74d-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="2d74d-105">описание</span><span class="sxs-lookup"><span data-stu-id="2d74d-105">Description</span></span>

<span data-ttu-id="2d74d-106">При синхронизации интернет-заказов появляется следующее сообщение об ошибке: "для обработки проводок кредитной карты должна использоваться служба платежей по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="2d74d-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Отсутствует ошибка службы платежа по умолчанию](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="2d74d-108">Приказ</span><span class="sxs-lookup"><span data-stu-id="2d74d-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="2d74d-109">Подтверждение или настройка службы платежа по умолчанию в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="2d74d-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="2d74d-110">Для подтверждения или настройки службы платежа по умолчанию в Commerce headquarters, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="2d74d-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2d74d-111">Перейдите в раздел **Расчеты с клиентами \> Настройка платежей \> Службы платежей**.</span><span class="sxs-lookup"><span data-stu-id="2d74d-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="2d74d-112">Убедитесь, что для параметра **Процессор по умолчанию для новых кредитных карт** установлен значение **Да** для одной службы платежей.</span><span class="sxs-lookup"><span data-stu-id="2d74d-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d74d-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2d74d-113">Additional resources</span></span>

[<span data-ttu-id="2d74d-114">Настройка, авторизация и проверка данных кредитной карты</span><span class="sxs-lookup"><span data-stu-id="2d74d-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
