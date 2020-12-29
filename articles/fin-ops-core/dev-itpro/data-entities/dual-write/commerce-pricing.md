---
title: Использование механизма ценообразования Dynamics 365 Commerce с Dynamics 365 Sales
description: В этой теме описывается, как использовать механизм ценообразования Microsoft Dynamics 365 Commerce для создания предложений с расценками продаж в Dynamics 365 Sales.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594926"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="d9a78-103">Использование механизма ценообразования Dynamics 365 Commerce с Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="d9a78-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9a78-104">В этой теме описывается, как использовать механизм ценообразования Microsoft Dynamics 365 Commerce для создания предложений с расценками продаж в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d9a78-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="d9a78-105">Механизм ценообразования Dynamics 365 Commerce поддерживает большинство сценариев ценообразования "бизнеса-потребитель" (B2C), таких как ценообразование на уровне магазина, ценообразование на основе предпочтений и лояльности, скидки за комплект, скидки за количество и пороговые скидки.</span><span class="sxs-lookup"><span data-stu-id="d9a78-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="d9a78-106">Механизм ценообразования использует сложные правила для определения наилучшей цены для данного предложения или заказа.</span><span class="sxs-lookup"><span data-stu-id="d9a78-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="d9a78-107">Когда вы используете [двойную запись](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), у вас имеются три вариант для потребностей в ценообразовании.</span><span class="sxs-lookup"><span data-stu-id="d9a78-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="d9a78-108">Можно использовать статические цены, поступающие из прайс-листа в Dynamics 365 Sales, модуль ценообразования в Dynamics 365 Supply Chain Management или модуль ценообразования в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d9a78-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="d9a78-109">Среди этих вариантов механизм ценообразования Commerce лучше всего подходит для сценариев B2C.</span><span class="sxs-lookup"><span data-stu-id="d9a78-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="d9a78-110">Использование механизма ценообразования Commerce в Sales</span><span class="sxs-lookup"><span data-stu-id="d9a78-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="d9a78-111">В настоящее время механизм ценообразования Commerce может использоваться только для создания предложений с расценками в Sales.</span><span class="sxs-lookup"><span data-stu-id="d9a78-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="d9a78-112">Интеграция заказов на продажу с механизмом ценообразования Commerce пока недоступна.</span><span class="sxs-lookup"><span data-stu-id="d9a78-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="d9a78-113">Когда пользователи инициируют предложение с расценками в Sales, платформа двойной записи копирует подробные сведения о предложении с расценками в Commerce.</span><span class="sxs-lookup"><span data-stu-id="d9a78-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="d9a78-114">Любые изменения существующих строк предложения с расценками или любые вновь добавленные строки предложения с расценками в Sales копируются в Commerce.</span><span class="sxs-lookup"><span data-stu-id="d9a78-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="d9a78-115">Когда пользователи хотят использовать модуль ценообразования Commerce для задания цен в предложении, они могут выбрать **Предложение с расценками** для обновления цен предложения на основе механизма ценообразования Commerce.</span><span class="sxs-lookup"><span data-stu-id="d9a78-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="d9a78-116">Цены автоматически обновляются в Sales и Commerce.</span><span class="sxs-lookup"><span data-stu-id="d9a78-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d9a78-117">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="d9a78-117">Prerequisites</span></span>

- <span data-ttu-id="d9a78-118">Прежде чем можно будет использовать механизм ценообразования Commerce в Sales, необходимо выполнить шаги в разделе [Продажа перспективному клиенту в случае двойной записи](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span><span class="sxs-lookup"><span data-stu-id="d9a78-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="d9a78-119">Необходимо отключить оценку коммерческого соглашения для ручного ввода, выполнив следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="d9a78-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="d9a78-120">В своей среде Commerce перейдите в раздел **Расчеты с клиентами \> Настройка \> Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="d9a78-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="d9a78-121">На вкладке **Цены** на экспресс-вкладке **Оценка коммерческого соглашения** снимите флажок **Ручной ввод**.</span><span class="sxs-lookup"><span data-stu-id="d9a78-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9a78-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d9a78-122">Additional resources</span></span>

[<span data-ttu-id="d9a78-123">Продажа перспективному клиенту в случае двойной записи</span><span class="sxs-lookup"><span data-stu-id="d9a78-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)
