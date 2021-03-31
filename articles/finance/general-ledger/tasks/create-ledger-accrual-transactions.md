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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1722c72ebc5ea7c0f8704ba3761f971f5075744
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216457"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="d36e5-103">Создание проводок начисления ГК</span><span class="sxs-lookup"><span data-stu-id="d36e5-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d36e5-104">Это руководство описывает создание проводок начисления ГК, которые основаны на схемах начисления</span><span class="sxs-lookup"><span data-stu-id="d36e5-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="d36e5-105">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="d36e5-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="d36e5-106">В списке найдите и выберите требуемый журнал или создайте новый.</span><span class="sxs-lookup"><span data-stu-id="d36e5-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="d36e5-107">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="d36e5-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="d36e5-108">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d36e5-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="d36e5-109">В поле "Счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="d36e5-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="d36e5-110">В этом примере определяются расходы для страховки.</span><span class="sxs-lookup"><span data-stu-id="d36e5-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="d36e5-111">Они станут периодической суммой расходов.</span><span class="sxs-lookup"><span data-stu-id="d36e5-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="d36e5-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d36e5-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="d36e5-113">В поле "Дебет" введите число.</span><span class="sxs-lookup"><span data-stu-id="d36e5-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="d36e5-114">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="d36e5-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="d36e5-115">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="d36e5-115">Click Functions.</span></span>
10. <span data-ttu-id="d36e5-116">Щелкните "Начисления ГК".</span><span class="sxs-lookup"><span data-stu-id="d36e5-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="d36e5-117">В поле "Код начисления" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d36e5-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="d36e5-118">В списке найдите и выберите схему начисления, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="d36e5-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="d36e5-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d36e5-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d36e5-120">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="d36e5-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="d36e5-121">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="d36e5-121">Click Transactions.</span></span>
16. <span data-ttu-id="d36e5-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d36e5-122">Close the page.</span></span>
17. <span data-ttu-id="d36e5-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d36e5-123">Click OK.</span></span>
18. <span data-ttu-id="d36e5-124">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="d36e5-124">Click Post.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]