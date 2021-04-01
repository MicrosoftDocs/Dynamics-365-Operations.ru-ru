---
title: Настройка ставок, привязанных к индексу
description: В этом разделе описывается, как настроить ставки, привязанные к индексу. Ставки, привязанные к индексам, требуются, если ваша организация связывает суммы платежей арендной платы с набором ставок, привязанных к индексу.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b6d201329996f23d94c0fc76a9635d3bb99c931e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249685"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="bfa1c-104">Настройка ставок, привязанных к индексу</span><span class="sxs-lookup"><span data-stu-id="bfa1c-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfa1c-105">Если платежи по аренде зависят от индекса, в системе можно добавлять и поддерживать типы ставок, привязанных к индексу.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="bfa1c-106">Чтобы переоценить платежи аренды со страницы **Тип ставки, привязанной к индексу**, процесс переоценки ставок, привязанных к индексу, использует самую последнюю ставку, привязанную к индексу, из даты переоценки.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="bfa1c-107">Чтобы добавить типы ставок, привязанных к индексу, и ставки, привязанные к индексу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="bfa1c-108">Перейдите в раздел **Аренда активов \> Настройка \> Типы ставок, привязанных к индексу**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="bfa1c-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-109">Select **New**.</span></span>
3. <span data-ttu-id="bfa1c-110">В соответствующих полях введите тип ставки и имя ставки, привязанной к индексу.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="bfa1c-111">Чтобы добавить новое значение ставки, привязанной к индексу, выберите тип ставки, привязанной к индексу, и затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="bfa1c-112">Выберите дату начала действия ставки и выберите значение ставки.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="bfa1c-113">В качестве метода оценки индекса необходимо выбрать **Разница значений ставки, привязанной к индексу** или **Значение ставки, привязанной к индексу**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="bfa1c-114">Выберите метод **Разница значений ставки, привязанной к индексу** для расчета нового платежа по аренде, основанный на разнице между ставкой, привязанной к индексу, на начальную дату и последней ставкой, привязанной к индексу.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="bfa1c-115">Ставка, привязанная к индексу, определяется в поле **Ставка, привязанная к индексу (%)**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="bfa1c-116">Выберите метод **Значение ставки, привязанной к индексу** для расчета платежа по аренде с использованием процентного значения, указанного в поле **Ставка индекса (%)**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]