--- 
title: "Создание проводок начисления ГК"
description: "Это руководство описывает создание проводок начисления ГК, которые основаны на схемах начисления."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4a65bec066bdcb01ce8acf8cfbf2d31611104921
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="e631d-103">Создание проводок начисления ГК</span><span class="sxs-lookup"><span data-stu-id="e631d-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e631d-104">Это руководство описывает создание проводок начисления ГК, которые основаны на схемах начисления</span><span class="sxs-lookup"><span data-stu-id="e631d-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="e631d-105">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="e631d-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="e631d-106">В списке найдите и выберите требуемый журнал или создайте новый.</span><span class="sxs-lookup"><span data-stu-id="e631d-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="e631d-107">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="e631d-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="e631d-108">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="e631d-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="e631d-109">В поле "Счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="e631d-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="e631d-110">В этом примере определяются расходы для страховки.</span><span class="sxs-lookup"><span data-stu-id="e631d-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="e631d-111">Они станут периодической суммой расходов.</span><span class="sxs-lookup"><span data-stu-id="e631d-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="e631d-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e631d-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="e631d-113">В поле "Дебет" введите число.</span><span class="sxs-lookup"><span data-stu-id="e631d-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="e631d-114">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="e631d-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="e631d-115">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="e631d-115">Click Functions.</span></span>
10. <span data-ttu-id="e631d-116">Щелкните "Начисления ГК".</span><span class="sxs-lookup"><span data-stu-id="e631d-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="e631d-117">В поле "Код начисления" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e631d-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="e631d-118">В списке найдите и выберите схему начисления, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="e631d-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="e631d-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="e631d-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="e631d-120">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="e631d-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="e631d-121">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="e631d-121">Click Transactions.</span></span>
16. <span data-ttu-id="e631d-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e631d-122">Close the page.</span></span>
17. <span data-ttu-id="e631d-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e631d-123">Click OK.</span></span>
18. <span data-ttu-id="e631d-124">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="e631d-124">Click Post.</span></span>


