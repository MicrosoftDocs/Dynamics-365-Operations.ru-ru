---
title: Создание договора о банковских услугах для гарантийного письма
description: Эта задача создает договор о банковских услугах для обработки гарантийного письма.
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2fe6bfebcc0cc302d623a34fd994a57cbea1c8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179613"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="79f33-103">Создание договора о банковских услугах для гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="79f33-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79f33-104">Эта задача создает договор о банковских услугах для обработки гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="79f33-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="79f33-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="79f33-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="79f33-106">Создание договорах о банковских услугах</span><span class="sxs-lookup"><span data-stu-id="79f33-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="79f33-107">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Договоры о банковских услугах".</span><span class="sxs-lookup"><span data-stu-id="79f33-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="79f33-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="79f33-108">Click New.</span></span>
3. <span data-ttu-id="79f33-109">В поле "Номер договора" введите номер договора с банком для проводки.</span><span class="sxs-lookup"><span data-stu-id="79f33-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="79f33-110">В поле "Банковский счет" выберите номер банковского счета, для которого открыто гарантийное письмо.</span><span class="sxs-lookup"><span data-stu-id="79f33-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="79f33-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="79f33-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="79f33-112">В поле "Дата начала" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="79f33-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="79f33-113">В поле "Дата окончания" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="79f33-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="79f33-114">Переключите развертывание раздела "Общее".</span><span class="sxs-lookup"><span data-stu-id="79f33-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="79f33-115">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="79f33-115">Click Add line.</span></span>
10. <span data-ttu-id="79f33-116">В поле "Тип ссуды" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="79f33-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="79f33-117">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="79f33-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="79f33-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="79f33-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="79f33-119">В поле "Лимит" введите сумму, оговоренную с банком.</span><span class="sxs-lookup"><span data-stu-id="79f33-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="79f33-120">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="79f33-120">Click Save.</span></span>
15. <span data-ttu-id="79f33-121">Переключите развертывание раздела "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="79f33-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="79f33-122">В поле "Метод расчета" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="79f33-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="79f33-123">Введите метод расчета и сведения о процентах для денежной маржи, комиссии выпуска, комиссии расширения, комиссии увеличения стоимости или комиссии уменьшения стоимости, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="79f33-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="79f33-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="79f33-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="79f33-125">Продление договора о банковских услугах</span><span class="sxs-lookup"><span data-stu-id="79f33-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="79f33-126">Щелкните "Развернуть", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="79f33-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="79f33-127">В поле "Новый номер договора" введите значение.</span><span class="sxs-lookup"><span data-stu-id="79f33-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="79f33-128">В поле "Дата окончания" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="79f33-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="79f33-129">Щелкните "Развернуть".</span><span class="sxs-lookup"><span data-stu-id="79f33-129">Click Extend.</span></span>
5. <span data-ttu-id="79f33-130">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="79f33-130">Click Save.</span></span>
6. <span data-ttu-id="79f33-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="79f33-131">Close the page.</span></span>

