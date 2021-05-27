---
title: Запись TaxTrans не создана
description: В этой теме содержатся сведения об устранении неполадок, которые могут помочь, когда запись TaxTrans не создается.
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
ms.openlocfilehash: 74987506699834d86703702106e5abf87bfa45da
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018789"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="2d95f-103">Запись TaxTrans не создана</span><span class="sxs-lookup"><span data-stu-id="2d95f-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d95f-104">Если для проводки выбрано **Разнесенный налог**, но на странице **Разнесенный налог** нет строк налогов или отсутствует строка налога, то запись **TaxTrans** могла не быть создана.</span><span class="sxs-lookup"><span data-stu-id="2d95f-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="2d95f-105">[![Страница разнесенного налога, которая не содержит элементов строк](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="2d95f-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="2d95f-106">Для решения проблемы выполните действия, указанные в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="2d95f-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="2d95f-107">Проверка налога до разноски проводки</span><span class="sxs-lookup"><span data-stu-id="2d95f-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="2d95f-108">Перед разноской проводки на странице **Разноска накладной** выберите **Налог** для проверки расчета.</span><span class="sxs-lookup"><span data-stu-id="2d95f-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="2d95f-109">[![Кнопка "Налог" на странице "Разноска накладной"](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="2d95f-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="2d95f-110">На странице **Временные налоговые проводки** проверьте результат расчета.</span><span class="sxs-lookup"><span data-stu-id="2d95f-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="2d95f-111">Если налог не рассчитан, см. [Налог не рассчитан или сумма налога равна нулю](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="2d95f-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="2d95f-112">Поиск записи TaxTrans во всех разнесенных налогах</span><span class="sxs-lookup"><span data-stu-id="2d95f-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="2d95f-113">Перейдите в раздел **Налог** \> **Запросы и отчеты** \> **Налоговые запросы** > **Разнесенный налог**.</span><span class="sxs-lookup"><span data-stu-id="2d95f-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="2d95f-114">В заголовке столбца **Ваучер** выберите символ фильтра для поиска записи **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="2d95f-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="2d95f-115">Если вы нашли нужные налоговые записи, проверьте дату.</span><span class="sxs-lookup"><span data-stu-id="2d95f-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="2d95f-116">Если дата отличается от даты заголовка журнала, создайте запрос в службу поддержки Майкрософт для получения дополнительной поддержки.</span><span class="sxs-lookup"><span data-stu-id="2d95f-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="2d95f-117">[![Страница разнесенного налога](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="2d95f-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="2d95f-118">Отладка для проверки данных</span><span class="sxs-lookup"><span data-stu-id="2d95f-118">Debug to check details</span></span>

1. <span data-ttu-id="2d95f-119">Для получения дополнительных сведений об отладке и определении правильности создания **TmpTaxWorkTrans** и **TaxUncommitted** см. [Значение поля в TaxTrans неправильное](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="2d95f-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="2d95f-120">Если **TaxTmpWorkTrans** или **TaxUncommitted** создается правильно, добавьте точку останова в **TaxPost::SaveAndPost()** и **Tax::SaveAndPost**, чтобы найти причину, почему **TaxTrans** не был вставлен.</span><span class="sxs-lookup"><span data-stu-id="2d95f-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="2d95f-121">[![Точки останова добавлены в код](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="2d95f-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="2d95f-122">[![Результаты добавленных точек останова](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="2d95f-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="2d95f-123">Определение существования настройки</span><span class="sxs-lookup"><span data-stu-id="2d95f-123">Determine whether customization exists</span></span>

<span data-ttu-id="2d95f-124">Если вы выполнили шаги в предыдущих разделах, но не смогли решить проблему, определите, существует ли настройка.</span><span class="sxs-lookup"><span data-stu-id="2d95f-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="2d95f-125">Если настройки не существует, создайте запрос в службу поддержки Майкрософт для получения дополнительной поддержки.</span><span class="sxs-lookup"><span data-stu-id="2d95f-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
