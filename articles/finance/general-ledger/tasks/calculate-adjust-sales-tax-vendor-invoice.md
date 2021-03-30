---
title: Расчет и корректировка налога по накладной поставщика
description: Эта тема объясняет, как скорректировать налог в счете-фактуре поставщика в Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4d01fe7587e01c04af28be934a235d955455216
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204745"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="f91e1-103">Расчет и корректировка налога по накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="f91e1-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f91e1-104">Эта тема объясняет, как скорректировать налог в счете-фактуре поставщика.</span><span class="sxs-lookup"><span data-stu-id="f91e1-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="f91e1-105">Если в исходном документе-источнике отображаются суммы налога, отличные от рассчитанных, эти суммы можно изменить перед разноской.</span><span class="sxs-lookup"><span data-stu-id="f91e1-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="f91e1-106">В этой задаче используется демонстрационная компания DEMF.</span><span class="sxs-lookup"><span data-stu-id="f91e1-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="f91e1-107">В области переходов выберите **Модули > Расчеты с поставщиками > Накладные > Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="f91e1-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="f91e1-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f91e1-108">Select **New**.</span></span>
3. <span data-ttu-id="f91e1-109">В поле **Имя** новой строки выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="f91e1-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="f91e1-110">На панели действий выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="f91e1-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="f91e1-111">В поле **Счет** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="f91e1-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="f91e1-112">В поле **Накладная** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f91e1-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="f91e1-113">В поле **Кредит** введите число.</span><span class="sxs-lookup"><span data-stu-id="f91e1-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="f91e1-114">В поле **Корр.счет** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="f91e1-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="f91e1-115">Выберите **Налог**.</span><span class="sxs-lookup"><span data-stu-id="f91e1-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="f91e1-116">В поле **Общая сумма фактического налога** введите число.</span><span class="sxs-lookup"><span data-stu-id="f91e1-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="f91e1-117">На вкладке **Корректировка** можно изменить суммы налога по налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="f91e1-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="f91e1-118">Выберите **Сбросить рассчитанные суммы до фактических**.</span><span class="sxs-lookup"><span data-stu-id="f91e1-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="f91e1-119">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f91e1-119">Select **OK**.</span></span>
14. <span data-ttu-id="f91e1-120">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f91e1-120">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]