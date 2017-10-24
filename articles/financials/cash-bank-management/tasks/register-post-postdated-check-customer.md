--- 
title: "Регистрация и разноска датированного будущим числом чека для клиента"
description: "Вы можете вводить информацию о полученных от клиентов чеках, датированных будущим числом."
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1610036815349f625a67d5dd67260114d42fff97
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="2de29-103">Регистрация и разноска датированного будущим числом чека для клиента</span><span class="sxs-lookup"><span data-stu-id="2de29-103">Register and post a postdated check for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2de29-104">Вы можете вводить информацию о полученных от клиентов чеках, датированных будущим числом.</span><span class="sxs-lookup"><span data-stu-id="2de29-104">You can register details of a postdated cheque received from a customer.</span></span> <span data-ttu-id="2de29-105">Также можно разнести чек, датированный будущим числом, и сформировать финансовые проводки.</span><span class="sxs-lookup"><span data-stu-id="2de29-105">You can also post the postdated cheque and generate financial transactions.</span></span>   <span data-ttu-id="2de29-106">Выполните следующие задачи, прежде чем регистрировать и разносить полученный от клиента чек, датированный будущим числом: • Настройка датированных будущим числом чеков на странице "Управление банком и кассовыми операциями" • Настройка способ оплаты для чеков, датированных будущим числом  Роль для выполнения этой процедуры — казначей.</span><span class="sxs-lookup"><span data-stu-id="2de29-106">Complete the following tasks before you register and post a postdated cheque received from a customer:   • Set up postdated Cheques in the Cash and bank management page • Set up a method of payment for postdated Cheques   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="2de29-107">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="2de29-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="2de29-108">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="2de29-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="2de29-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2de29-109">Click New.</span></span>
3. <span data-ttu-id="2de29-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2de29-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2de29-111">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="2de29-111">Click Lines.</span></span>
5. <span data-ttu-id="2de29-112">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="2de29-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="2de29-113">В поле "Счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="2de29-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="2de29-114">В поле "Кредит" введите число.</span><span class="sxs-lookup"><span data-stu-id="2de29-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="2de29-115">Введите сумму, указанную в чеке, датированном будущим числом.</span><span class="sxs-lookup"><span data-stu-id="2de29-115">Enter the amount specified in the postdated cheque.</span></span>  
8. <span data-ttu-id="2de29-116">Перейдите на вкладку Платеж.</span><span class="sxs-lookup"><span data-stu-id="2de29-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="2de29-117">В поле "Способ оплаты" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2de29-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="2de29-118">Выберите способ оплаты для чека, датированного будущим числом.</span><span class="sxs-lookup"><span data-stu-id="2de29-118">Select the method of payment for the postdated cheque</span></span>  
10. <span data-ttu-id="2de29-119">Перейдите на вкладку "Чеки, датированные будущим числом".</span><span class="sxs-lookup"><span data-stu-id="2de29-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="2de29-120">В поле "Дата погашения" введите дату.</span><span class="sxs-lookup"><span data-stu-id="2de29-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="2de29-121">Введите дату срока оплаты для чека, датированного будущим числом.</span><span class="sxs-lookup"><span data-stu-id="2de29-121">Enter the date when the postdated cheque is due for payment.</span></span>  
12. <span data-ttu-id="2de29-122">В поле "Отделение выставляющего банка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2de29-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="2de29-123">Введите сведения о банке для чека, датированного будущим числом.</span><span class="sxs-lookup"><span data-stu-id="2de29-123">Enter the bank details of the postdated cheque.</span></span>  
13. <span data-ttu-id="2de29-124">В поле "Номер чека" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2de29-124">In the cheque number field, type a value.</span></span>
14. <span data-ttu-id="2de29-125">В поле "Наименование выставляющего банка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2de29-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="2de29-126">Введите сведения о банке для чека, датированного будущим числом.</span><span class="sxs-lookup"><span data-stu-id="2de29-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="2de29-127">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="2de29-127">Click Post.</span></span>
16. <span data-ttu-id="2de29-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2de29-128">Close the page.</span></span>


