---
title: Создание проводок начисления ГК
description: Это руководство описывает создание проводок начисления ГК, которые основаны на схемах начисления.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06743ca3ed13906e3f65d3783db7a7f74fb53e3f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186195"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="256ba-103">Создание проводок начисления ГК</span><span class="sxs-lookup"><span data-stu-id="256ba-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="256ba-104">Это руководство описывает создание проводок начисления ГК, которые основаны на схемах начисления</span><span class="sxs-lookup"><span data-stu-id="256ba-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="256ba-105">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="256ba-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="256ba-106">В списке найдите и выберите требуемый журнал или создайте новый.</span><span class="sxs-lookup"><span data-stu-id="256ba-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="256ba-107">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="256ba-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="256ba-108">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="256ba-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="256ba-109">В поле "Счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="256ba-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="256ba-110">В этом примере определяются расходы для страховки.</span><span class="sxs-lookup"><span data-stu-id="256ba-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="256ba-111">Они станут периодической суммой расходов.</span><span class="sxs-lookup"><span data-stu-id="256ba-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="256ba-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="256ba-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="256ba-113">В поле "Дебет" введите число.</span><span class="sxs-lookup"><span data-stu-id="256ba-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="256ba-114">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="256ba-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="256ba-115">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="256ba-115">Click Functions.</span></span>
10. <span data-ttu-id="256ba-116">Щелкните "Начисления ГК".</span><span class="sxs-lookup"><span data-stu-id="256ba-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="256ba-117">В поле "Код начисления" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="256ba-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="256ba-118">В списке найдите и выберите схему начисления, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="256ba-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="256ba-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="256ba-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="256ba-120">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="256ba-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="256ba-121">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="256ba-121">Click Transactions.</span></span>
16. <span data-ttu-id="256ba-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="256ba-122">Close the page.</span></span>
17. <span data-ttu-id="256ba-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="256ba-123">Click OK.</span></span>
18. <span data-ttu-id="256ba-124">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="256ba-124">Click Post.</span></span>

