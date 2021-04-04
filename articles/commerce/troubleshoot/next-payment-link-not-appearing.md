---
title: Вариант "сохранить для следующего платежа" не отображается
description: В этом разделе приведены инструкции по устранению неполадок, которые могут помочь, когда флажок "сохранить для следующего платежа" не появился в разделе "Способ оплаты" на странице оформления заказа сайта электронной коммерции.
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
ms.openlocfilehash: 3a4fbcd522651ed1b82b72b751ff6ead44c94a71
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585503"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="55dad-103">Вариант "Сохранить для следующего платежа" не отображается</span><span class="sxs-lookup"><span data-stu-id="55dad-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55dad-104">В этом разделе приведены инструкции по устранению неполадок, которые могут помочь, когда флажок **Сохранить для следующего платежа** не появился в разделе **Способ оплаты** на странице оформления заказа сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="55dad-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="55dad-105">описание</span><span class="sxs-lookup"><span data-stu-id="55dad-105">Description</span></span>

<span data-ttu-id="55dad-106">Флажок **Сохранить для следующего платежа** не отображается в разделе **Способ оплаты** на странице оформления заказа сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="55dad-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="55dad-107">На следующем рисунке показан пример страницы оформления заказа, которая включает флажок **Сохранить для следующего платежа**.</span><span class="sxs-lookup"><span data-stu-id="55dad-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Флажок "Сохранить для следующего платежа" в Модуле платежа](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="55dad-109">Приказ</span><span class="sxs-lookup"><span data-stu-id="55dad-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="55dad-110">Убедитесь, что соединитель платежей Dynamics 365 для Adyen правильно настроен в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="55dad-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="55dad-111">Чтобы убедиться в том, что соединитель платежей Dynamics 365 для Adyen правильно настроен в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="55dad-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="55dad-112">Перейдите в раздел **Retail и Commerce \> Каналы \> Интернет-магазины**.</span><span class="sxs-lookup"><span data-stu-id="55dad-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="55dad-113">Выберите интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="55dad-113">Select the online store.</span></span>
1. <span data-ttu-id="55dad-114">На экспресс-вкладке **счета оплаты** убедитесь, что в поле **Разрешить сохранение информации о платеже в электронной коммерции** задано значение **Истина**.</span><span class="sxs-lookup"><span data-stu-id="55dad-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Разрешить сохранение сведений о платежах в поле электронной коммерции в Commerce headquarters](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="55dad-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="55dad-116">Additional resources</span></span>

[<span data-ttu-id="55dad-117">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="55dad-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="55dad-118">Сохранение интерактивных платежных инструментов с помощью соединителя Adyen</span><span class="sxs-lookup"><span data-stu-id="55dad-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)