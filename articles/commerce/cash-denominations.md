---
title: Настройка номиналов денежных знаков для терминала POS
description: Можно определить в бэк-офисе номиналы банкнот и монет, которые будут использоваться кассирами, продавцами и менеджерами в магазине из POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b2fb6676f45bc7efa4652de60e829b507292ac37
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213194"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a><span data-ttu-id="df75d-103">Настройка номиналов денежных знаков для терминала POS</span><span class="sxs-lookup"><span data-stu-id="df75d-103">Configure cash denominations for the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="df75d-104">Можно определить в бэк-офисе номиналы банкнот и монет, которые будут использоваться кассирами, продавцами и менеджерами в магазине из POS.</span><span class="sxs-lookup"><span data-stu-id="df75d-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="df75d-105">Эти номиналы могут использоваться для облегчения инвентаризации кассы для декларирования платежных средств в конце дня или для ускорения расчетов при продажах.</span><span class="sxs-lookup"><span data-stu-id="df75d-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="df75d-106">Определение номиналов</span><span class="sxs-lookup"><span data-stu-id="df75d-106">Define denominations</span></span>

<span data-ttu-id="df75d-107">Номиналы настраиваются для каждого магазина на странице **Настроить** \> **Декларирование наличности** в свойствах магазина.</span><span class="sxs-lookup"><span data-stu-id="df75d-107">The denominations are set up per store on the **Set up** \> **Cash declaration** option from the store property page.</span></span>

![Параметр декларирования наличности](./media/image1-denomination.png)

<span data-ttu-id="df75d-109">Чтобы определить номинал:</span><span class="sxs-lookup"><span data-stu-id="df75d-109">To define a denomination:</span></span>

1. <span data-ttu-id="df75d-110">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="df75d-110">Click **New**.</span></span>
1. <span data-ttu-id="df75d-111">Укажите тип (монета или банкнота).</span><span class="sxs-lookup"><span data-stu-id="df75d-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="df75d-112">Укажите сумму (значение).</span><span class="sxs-lookup"><span data-stu-id="df75d-112">Specify the amount (value).</span></span>

![Страница декларирования наличности по номиналам](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="df75d-114">Настройка профиля функциональности</span><span class="sxs-lookup"><span data-stu-id="df75d-114">Configure the functionality profile</span></span>

<span data-ttu-id="df75d-115">При оплате наличными в POS пользователь может использовать номиналы банкнот для быстрого ввода суммы, уплаченной клиентом.</span><span class="sxs-lookup"><span data-stu-id="df75d-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="df75d-116">В профиле функциональности можно настроить два параметра для отображения номиналов в POS.</span><span class="sxs-lookup"><span data-stu-id="df75d-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

- <span data-ttu-id="df75d-117">**Больше или равно сумме к выплате** — по умолчанию POS будет только отображать номиналы банкнот, которые больше суммы к выплате, что позволяет принять оплату одним нажатием.</span><span class="sxs-lookup"><span data-stu-id="df75d-117">**Greater or equal to amount due** – By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="df75d-118">Например, если сумма к уплате составляет 75 рублей, в POS отобразятся следующие номиналы: 100, 500, 1000 и 5000 рублей.</span><span class="sxs-lookup"><span data-stu-id="df75d-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="df75d-119">При нажатии любой их этих сумм она автоматически будет принята в уплату за покупку.</span><span class="sxs-lookup"><span data-stu-id="df75d-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="df75d-120">5-, 10- и 50-рублевые банкноты не отображаются, поскольку эти суммы меньше суммы к уплате.</span><span class="sxs-lookup"><span data-stu-id="df75d-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>
- <span data-ttu-id="df75d-121">**Все номиналы** — выберите этот вариант, чтобы в POS всегда отображались все номиналы, независимо от суммы к выплате.</span><span class="sxs-lookup"><span data-stu-id="df75d-121">**All denominations** – Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="df75d-122">Это означает, что пользователь может использовать сочетание банкнот для достижения суммы к выплате.</span><span class="sxs-lookup"><span data-stu-id="df75d-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="df75d-123">Например если сумма к уплате составляет 60 рублей, пользователь может выбрать 50 рублей и 10 рублей для совершения продажи.</span><span class="sxs-lookup"><span data-stu-id="df75d-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]