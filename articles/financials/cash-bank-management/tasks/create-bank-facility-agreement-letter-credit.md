---
title: Создание договора о банковских услугах для аккредитива
description: В этой задаче представлен процесс создания договора о банковских услугах для обработки аккредитива.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18395f300965df7e024f0eec2b53fa4e8ad2cc3e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566210"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="8439b-103">Создание договора о банковских услугах для аккредитива</span><span class="sxs-lookup"><span data-stu-id="8439b-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8439b-104">В этой задаче представлен процесс создания договора о банковских услугах для обработки аккредитива.</span><span class="sxs-lookup"><span data-stu-id="8439b-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="8439b-105">До выполнения этой задачи необходимо настроить банковские услуги и профили разноски.</span><span class="sxs-lookup"><span data-stu-id="8439b-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="8439b-106">В данной задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="8439b-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="8439b-107">Создание договорах о банковских услугах</span><span class="sxs-lookup"><span data-stu-id="8439b-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="8439b-108">Перейдите в раздел "Управление банком и кассовыми операциями" > "Аккредитивы" > "Договоры о банковских услугах".</span><span class="sxs-lookup"><span data-stu-id="8439b-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="8439b-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8439b-109">Click New.</span></span>
3. <span data-ttu-id="8439b-110">В поле "Номер договора" введите номер договора согласно договору с банком.</span><span class="sxs-lookup"><span data-stu-id="8439b-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="8439b-111">В поле "Банковский счет" введите номер счета в выставляющем банке.</span><span class="sxs-lookup"><span data-stu-id="8439b-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="8439b-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8439b-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8439b-113">В поле "Дата начала" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="8439b-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="8439b-114">В поле "Дата окончания" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="8439b-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="8439b-115">Разверните или сверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="8439b-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="8439b-116">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="8439b-116">Click Add line.</span></span>
10. <span data-ttu-id="8439b-117">В поле "Тип ссуды" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8439b-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8439b-118">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="8439b-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="8439b-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8439b-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="8439b-120">В поле "Лимит" введите сумму ссуды, согласованную с банком.</span><span class="sxs-lookup"><span data-stu-id="8439b-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="8439b-121">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="8439b-121">Click Save.</span></span>
15. <span data-ttu-id="8439b-122">Щелкните "Развернуть", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8439b-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="8439b-123">В поле "Новый номер договора" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8439b-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="8439b-124">В поле "Дата окончания" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="8439b-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="8439b-125">Щелкните "Развернуть".</span><span class="sxs-lookup"><span data-stu-id="8439b-125">Click Extend.</span></span>
19. <span data-ttu-id="8439b-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8439b-126">Close the page.</span></span>

