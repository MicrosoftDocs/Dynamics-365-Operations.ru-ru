--- 
title: "Обработка ретробонусов для оплаты"
description: "В этой процедуре демонстрируется, как преобразовывать утвержденные и обработанные ретробонусы клиентов в кредит-ноты."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 791ec304b9ea7c49fbea506d73c4daffd4478739
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="8e44b-103">Обработка ретробонусов для оплаты</span><span class="sxs-lookup"><span data-stu-id="8e44b-103">Process rebates for payment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e44b-104">В этой процедуре демонстрируется, как преобразовывать утвержденные и обработанные ретробонусы клиентов в кредит-ноты.</span><span class="sxs-lookup"><span data-stu-id="8e44b-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="8e44b-105">Это руководство можно выполнить в компании демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="8e44b-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="8e44b-106">Необходимым условием для этого руководства является наличие одного или нескольких требований по ретробонусам со статусом "Пометка".</span><span class="sxs-lookup"><span data-stu-id="8e44b-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="8e44b-107">При использовании компании USMF необходимо выполнить руководство "Создание и обработка ретробонусов клиента", прежде чем приступать к этому руководству.</span><span class="sxs-lookup"><span data-stu-id="8e44b-107">If you’re using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="8e44b-108">Преобразование требований по ретробонусам в кредит-ноту</span><span class="sxs-lookup"><span data-stu-id="8e44b-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="8e44b-109">Перейдите в раздел "Все клиенты".</span><span class="sxs-lookup"><span data-stu-id="8e44b-109">Go to All customers.</span></span>
2. <span data-ttu-id="8e44b-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8e44b-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8e44b-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8e44b-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8e44b-112">В области действий щелкните "Сбор".</span><span class="sxs-lookup"><span data-stu-id="8e44b-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="8e44b-113">Щелкните "Сопоставление проводок".</span><span class="sxs-lookup"><span data-stu-id="8e44b-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="8e44b-114">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="8e44b-114">Click Functions.</span></span>
7. <span data-ttu-id="8e44b-115">Щелкните "Программа бонусов".</span><span class="sxs-lookup"><span data-stu-id="8e44b-115">Click Rebate program.</span></span>
    * <span data-ttu-id="8e44b-116">На странице "Ретробонус" перечислены требования по ретробонусам, которые вы обработали на рабочем месте по начислению ретробонусов и которые находятся в состоянии "Пометка".</span><span class="sxs-lookup"><span data-stu-id="8e44b-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="8e44b-117">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="8e44b-117">Click Edit.</span></span>
    * <span data-ttu-id="8e44b-118">Установите флажки в поле "Пометка" для требований, которые вы хотите включить в кредит-ноту.</span><span class="sxs-lookup"><span data-stu-id="8e44b-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="8e44b-119">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="8e44b-119">Click Functions.</span></span>
10. <span data-ttu-id="8e44b-120">Щелкните "Создать кредит-ноту".</span><span class="sxs-lookup"><span data-stu-id="8e44b-120">Click Create credit note.</span></span>
    * <span data-ttu-id="8e44b-121">Появляется сообщение о том, что журнал разнесен (это журнал потребления модуля "Расчеты с клиентами", как указано на странице "Параметры модуля расчетов с клиентами").</span><span class="sxs-lookup"><span data-stu-id="8e44b-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="8e44b-122">В результате этого сумма реального обязательства (кредита) переносится на сальдо клиента.</span><span class="sxs-lookup"><span data-stu-id="8e44b-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="8e44b-123">Это означает, что счет клиента кредитуется, а счет начисления "Ретробонус" дебетуется.</span><span class="sxs-lookup"><span data-stu-id="8e44b-123">This means that the customer’s account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="8e44b-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8e44b-124">Close the page.</span></span>
12. <span data-ttu-id="8e44b-125">Щелкните "Отмена".</span><span class="sxs-lookup"><span data-stu-id="8e44b-125">Click Cancel.</span></span>
    * <span data-ttu-id="8e44b-126">В результате страница будет обновлена, и вы увидите новые данные.</span><span class="sxs-lookup"><span data-stu-id="8e44b-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="8e44b-127">В области действий щелкните "Сбор".</span><span class="sxs-lookup"><span data-stu-id="8e44b-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="8e44b-128">Щелкните "Сопоставление проводок".</span><span class="sxs-lookup"><span data-stu-id="8e44b-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="8e44b-129">Обратите внимание, что к сальдо клиента была добавлена проводка на отрицательную сумму, соответствующую суммарной величине ретробонусов, без ссылки на накладную.</span><span class="sxs-lookup"><span data-stu-id="8e44b-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="8e44b-130">Щелкните "Отмена".</span><span class="sxs-lookup"><span data-stu-id="8e44b-130">Click Cancel.</span></span>


