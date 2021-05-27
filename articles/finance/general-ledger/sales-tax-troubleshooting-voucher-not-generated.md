---
title: Ваучер не создан
description: В этой теме содержатся сведения об устранении неполадок, которые могут помочь, когда ваучер должен быть создан, но не создан.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ba23b597b1d7d283b99638fb7d5d91da00afb09c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018765"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="0b1f9-103">Ваучер не создан</span><span class="sxs-lookup"><span data-stu-id="0b1f9-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b1f9-104">Если ваучер должна быть сформирован, но на странице **Проводки ваучера** не отображаются ваучеры, выполните действия, указанные в следующих разделах, в соответствии с требованиями для устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="0b1f9-105">[![Страница проводок ваучера без ваучеров](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="0b1f9-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="0b1f9-106">Проверка применимости налога</span><span class="sxs-lookup"><span data-stu-id="0b1f9-106">Check the tax applicability</span></span>

1. <span data-ttu-id="0b1f9-107">Перейдите **Налог** \> **Периодические задачи** \> **Записи журнала субкниги еще не переданы**.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="0b1f9-108">Если есть запись в журнале, выберите ее, а затем выберите **Перенести сейчас**.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="0b1f9-109">[![Кнопка "Перенести сейчас" на странице "Записи журнала субкниги еще не переданы"](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="0b1f9-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="0b1f9-110">Снова откройте страницу **Проводки ваучера**, чтобы просмотреть, был ли создан данный ваучер.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="0b1f9-111">Определение существования настройки</span><span class="sxs-lookup"><span data-stu-id="0b1f9-111">Determine whether customization exists</span></span>

<span data-ttu-id="0b1f9-112">Если вы выполнили шаги в предыдущем разделе, но не смогли решить проблему, определите, существует ли настройка.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="0b1f9-113">Если настройки не существует, создайте запрос в службу поддержки Майкрософт для получения дополнительной поддержки.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
