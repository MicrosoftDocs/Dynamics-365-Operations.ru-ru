---
title: Расчет и корректировка налога по накладной поставщика
description: Эта тема объясняет, как скорректировать налог в счете-фактуре поставщика в Dynamics 365 for Finance and Operations.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 684529087d5348c9e02310f812f8aa6f64c6655f
ms.sourcegitcommit: 016832198c306e8329ad21b5254e7d1cdff74c2f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862622"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="d1293-103">Расчет и корректировка налога по накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="d1293-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1293-104">Эта тема объясняет, как скорректировать налог в счете-фактуре поставщика в Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d1293-104">This topic explains how to adjust sales tax on a vendor invoice in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d1293-105">Если в исходном документе-источнике отображаются суммы налога, отличные от рассчитанных, эти суммы можно изменить перед разноской.</span><span class="sxs-lookup"><span data-stu-id="d1293-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="d1293-106">В этой задаче используется демонстрационная компания DEMF.</span><span class="sxs-lookup"><span data-stu-id="d1293-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="d1293-107">В области переходов выберите **Модули > Расчеты с поставщиками > Накладные > Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="d1293-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="d1293-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d1293-108">Select **New**.</span></span>
3. <span data-ttu-id="d1293-109">В поле **Имя** новой строки выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="d1293-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="d1293-110">На панели действий выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="d1293-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="d1293-111">В поле **Счет** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="d1293-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="d1293-112">В поле **Накладная** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d1293-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="d1293-113">В поле **Кредит** введите число.</span><span class="sxs-lookup"><span data-stu-id="d1293-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="d1293-114">В поле **Корр.счет** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="d1293-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="d1293-115">Выберите **Налог**.</span><span class="sxs-lookup"><span data-stu-id="d1293-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="d1293-116">В поле **Общая сумма фактического налога** введите число.</span><span class="sxs-lookup"><span data-stu-id="d1293-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="d1293-117">На вкладке **Корректировка** можно изменить суммы налога по налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="d1293-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="d1293-118">Выберите **Сбросить рассчитанные суммы до фактических**.</span><span class="sxs-lookup"><span data-stu-id="d1293-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="d1293-119">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d1293-119">Select **OK**.</span></span>
14. <span data-ttu-id="d1293-120">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d1293-120">Select **Save**.</span></span>

