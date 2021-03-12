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
ms.openlocfilehash: 2536e87953267eae13cf3b42c2bd5476fc647c22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994723"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="ce2b4-103">Расчет и корректировка налога по накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="ce2b4-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce2b4-104">Эта тема объясняет, как скорректировать налог в счете-фактуре поставщика.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="ce2b4-105">Если в исходном документе-источнике отображаются суммы налога, отличные от рассчитанных, эти суммы можно изменить перед разноской.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="ce2b4-106">В этой задаче используется демонстрационная компания DEMF.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="ce2b4-107">В области переходов выберите **Модули > Расчеты с поставщиками > Накладные > Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="ce2b4-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-108">Select **New**.</span></span>
3. <span data-ttu-id="ce2b4-109">В поле **Имя** новой строки выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="ce2b4-110">На панели действий выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="ce2b4-111">В поле **Счет** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="ce2b4-112">В поле **Накладная** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="ce2b4-113">В поле **Кредит** введите число.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="ce2b4-114">В поле **Корр.счет** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="ce2b4-115">Выберите **Налог**.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="ce2b4-116">В поле **Общая сумма фактического налога** введите число.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="ce2b4-117">На вкладке **Корректировка** можно изменить суммы налога по налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="ce2b4-118">Выберите **Сбросить рассчитанные суммы до фактических**.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="ce2b4-119">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-119">Select **OK**.</span></span>
14. <span data-ttu-id="ce2b4-120">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ce2b4-120">Select **Save**.</span></span>

