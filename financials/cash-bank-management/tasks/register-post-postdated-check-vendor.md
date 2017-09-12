--- 
title: "Регистрация и разноска датированного будущим числом чека для поставщика"
description: "Для регистрации сведений по чеку, датированному задним числом, до отправки чека поставщику можно использовать ваучер журнала."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8689421d3281f93af9298f777f92c5c3b2c1c86c
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="35774-103">Регистрация и разноска датированного будущим числом чека для поставщика</span><span class="sxs-lookup"><span data-stu-id="35774-103">Register and post a postdated check for a vendor</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35774-104">Для регистрации сведений по чеку, датированному задним числом, до отправки чека поставщику можно использовать ваучер журнала.</span><span class="sxs-lookup"><span data-stu-id="35774-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="35774-105">Также можно разнести чек, датированный будущим числом, и сформировать финансовые проводки.</span><span class="sxs-lookup"><span data-stu-id="35774-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="35774-106">Прежде чем регистрировать и разносить датированный будущим числом чек от поставщика, выполните следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="35774-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="35774-107">Настройка датированных будущим числом чеков на странице "Управление банком и кассовыми операциями".</span><span class="sxs-lookup"><span data-stu-id="35774-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="35774-108">Роль для выполнения этого руководства по задачам — казначей.</span><span class="sxs-lookup"><span data-stu-id="35774-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="35774-109">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="35774-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="35774-110">Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="35774-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="35774-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="35774-111">Click New.</span></span>
3. <span data-ttu-id="35774-112">В поле "Имя" введите "VendPay".</span><span class="sxs-lookup"><span data-stu-id="35774-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="35774-113">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="35774-113">Click Lines.</span></span>
5. <span data-ttu-id="35774-114">В поле "Счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="35774-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="35774-115">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="35774-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="35774-116">В поле "Дебет" введите число.</span><span class="sxs-lookup"><span data-stu-id="35774-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="35774-117">В поле "Способ оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="35774-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35774-118">Выберите способ оплаты для чека, датированного будущим числом.</span><span class="sxs-lookup"><span data-stu-id="35774-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="35774-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="35774-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="35774-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="35774-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="35774-121">Перейдите на вкладку "Чеки, датированные будущим числом".</span><span class="sxs-lookup"><span data-stu-id="35774-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="35774-122">В поле "Номер чека" введите значение.</span><span class="sxs-lookup"><span data-stu-id="35774-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="35774-123">Введите или измените номер чека, датированного задним числом.</span><span class="sxs-lookup"><span data-stu-id="35774-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="35774-124">В поле "Наименование выставляющего банка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="35774-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="35774-125">Введите реквизиты выставляющего банка.</span><span class="sxs-lookup"><span data-stu-id="35774-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="35774-126">Щелкните вкладку "Список".</span><span class="sxs-lookup"><span data-stu-id="35774-126">Click the List tab.</span></span>
15. <span data-ttu-id="35774-127">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="35774-127">Click Post.</span></span>
16. <span data-ttu-id="35774-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="35774-128">Close the page.</span></span>
17. <span data-ttu-id="35774-129">Перейдите на вкладку "Чеки, датированные будущим числом".</span><span class="sxs-lookup"><span data-stu-id="35774-129">Click the Postdated checks tab.</span></span>


