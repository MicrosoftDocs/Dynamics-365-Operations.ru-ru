---
title: Возврат по заказу на возврат отклонен
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь, когда возврат по заказу на возврат отклонен, так как кредитная карта, используемая для выставления накладной, отличается от карты, которая использовалась при исходной авторизации платежа.
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
ms.openlocfilehash: 99fd4b816b1a3a1fe3c2d1579be45b43fdc3d385
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020764"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="3a695-103">Возврат по заказу на возврат отклонен</span><span class="sxs-lookup"><span data-stu-id="3a695-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a695-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь, когда возврат по заказу на возврат отклонен, так как кредитная карта, используемая для выставления накладной, отличается от карты, которая использовалась при исходной авторизации платежа.</span><span class="sxs-lookup"><span data-stu-id="3a695-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="3a695-105">описание</span><span class="sxs-lookup"><span data-stu-id="3a695-105">Description</span></span>

<span data-ttu-id="3a695-106">Возврат отклоняется, если кредитная карта, используемая для выставления накладной для заказа на возврат, отличается от карты, которая использовалась во время исходной авторизации платежа.</span><span class="sxs-lookup"><span data-stu-id="3a695-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="3a695-107">Будет выведено следующее сообщение об ошибке: "Некоторые платежи для разноски имеют неправильный статус.</span><span class="sxs-lookup"><span data-stu-id="3a695-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="3a695-108">Перед выставлением накладных выполните повторную проверку статуса всех платежей".</span><span class="sxs-lookup"><span data-stu-id="3a695-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="3a695-109">Данные авторизации платежа будут включать следующее сообщение об ошибке: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span><span class="sxs-lookup"><span data-stu-id="3a695-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Ошибка отклонения возврата по заказу на возврат](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="3a695-111">Приказ</span><span class="sxs-lookup"><span data-stu-id="3a695-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="3a695-112">Включить возвраты вслепую в Adyen</span><span class="sxs-lookup"><span data-stu-id="3a695-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="3a695-113">Чтобы включить возвраты вслепую, выполните шаги, описанные в разделе [Устранение неполадок с соединитель платежей Dynamics 365 для Adyen](adyen-support.md), чтобы связаться с группой поддержки Adyen, и запросите, что функция возвратов вслепую должна быть включена на вашем счете Adyen.</span><span class="sxs-lookup"><span data-stu-id="3a695-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a695-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3a695-114">Additional resources</span></span>

[<span data-ttu-id="3a695-115">Соединитель платежей Dynamics 365 для Adyen</span><span class="sxs-lookup"><span data-stu-id="3a695-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="3a695-116">Настройка соединителя платежей Adyen для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3a695-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
