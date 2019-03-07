---
title: Расчет и корректировка налога по накладной поставщика
description: Если в исходном документе-источнике отображаются суммы налога, отличные от рассчитанных, эти суммы можно изменить перед разноской.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "308928"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="c713a-103">Расчет и корректировка налога по накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="c713a-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c713a-104">Если в исходном документе-источнике отображаются суммы налога, отличные от рассчитанных, эти суммы можно изменить перед разноской.</span><span class="sxs-lookup"><span data-stu-id="c713a-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="c713a-105">В этой задаче используется демонстрационная компания DEMF.</span><span class="sxs-lookup"><span data-stu-id="c713a-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="c713a-106">Перейдите в раздел "Расчеты с поставщиками" > "Накладные" > "Журнал накладных".</span><span class="sxs-lookup"><span data-stu-id="c713a-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="c713a-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c713a-107">Click New.</span></span>
3. <span data-ttu-id="c713a-108">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="c713a-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c713a-109">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c713a-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c713a-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c713a-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c713a-111">Выберите Строки.</span><span class="sxs-lookup"><span data-stu-id="c713a-111">Click Lines.</span></span>
7. <span data-ttu-id="c713a-112">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="c713a-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c713a-113">В поле "Счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="c713a-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="c713a-114">В поле "Накладная" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c713a-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="c713a-115">В поле "Кредит" введите число.</span><span class="sxs-lookup"><span data-stu-id="c713a-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="c713a-116">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="c713a-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="c713a-117">Щелкните "Налог".</span><span class="sxs-lookup"><span data-stu-id="c713a-117">Click Sales tax.</span></span>
13. <span data-ttu-id="c713a-118">В поле "Общая сумма фактического налога" введите число.</span><span class="sxs-lookup"><span data-stu-id="c713a-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="c713a-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c713a-119">Click OK.</span></span>
15. <span data-ttu-id="c713a-120">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="c713a-120">Click Save.</span></span>
16. <span data-ttu-id="c713a-121">Щелкните "Налог".</span><span class="sxs-lookup"><span data-stu-id="c713a-121">Click Sales tax.</span></span>
17. <span data-ttu-id="c713a-122">На вкладке "Корректировка" можно изменить суммы налога по налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="c713a-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="c713a-123">Щелкните "Сбросить рассчитанные суммы до фактических".</span><span class="sxs-lookup"><span data-stu-id="c713a-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="c713a-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c713a-124">Click OK.</span></span>
20. <span data-ttu-id="c713a-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c713a-125">Click Save.</span></span>

