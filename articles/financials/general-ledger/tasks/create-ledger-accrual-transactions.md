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
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846615"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="439cf-103">Создание проводок начисления ГК</span><span class="sxs-lookup"><span data-stu-id="439cf-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="439cf-104">Это руководство описывает создание проводок начисления ГК, которые основаны на схемах начисления</span><span class="sxs-lookup"><span data-stu-id="439cf-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="439cf-105">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="439cf-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="439cf-106">В списке найдите и выберите требуемый журнал или создайте новый.</span><span class="sxs-lookup"><span data-stu-id="439cf-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="439cf-107">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="439cf-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="439cf-108">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="439cf-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="439cf-109">В поле "Счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="439cf-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="439cf-110">В этом примере определяются расходы для страховки.</span><span class="sxs-lookup"><span data-stu-id="439cf-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="439cf-111">Они станут периодической суммой расходов.</span><span class="sxs-lookup"><span data-stu-id="439cf-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="439cf-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="439cf-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="439cf-113">В поле "Дебет" введите число.</span><span class="sxs-lookup"><span data-stu-id="439cf-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="439cf-114">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="439cf-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="439cf-115">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="439cf-115">Click Functions.</span></span>
10. <span data-ttu-id="439cf-116">Щелкните "Начисления ГК".</span><span class="sxs-lookup"><span data-stu-id="439cf-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="439cf-117">В поле "Код начисления" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="439cf-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="439cf-118">В списке найдите и выберите схему начисления, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="439cf-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="439cf-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="439cf-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="439cf-120">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="439cf-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="439cf-121">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="439cf-121">Click Transactions.</span></span>
16. <span data-ttu-id="439cf-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="439cf-122">Close the page.</span></span>
17. <span data-ttu-id="439cf-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="439cf-123">Click OK.</span></span>
18. <span data-ttu-id="439cf-124">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="439cf-124">Click Post.</span></span>

