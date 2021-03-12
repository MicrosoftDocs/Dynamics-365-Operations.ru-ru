---
title: Создание договора о банковских услугах для гарантийного письма
description: Эта задача создает договор о банковских услугах для обработки гарантийного письма.
author: panolte
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edeadc1b8502171b9ce892efdaeb9347e399b771
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989110"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="380a7-103">Создание договора о банковских услугах для гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="380a7-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="380a7-104">Эта задача создает договор о банковских услугах для обработки гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="380a7-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="380a7-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="380a7-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="380a7-106">Создание договорах о банковских услугах</span><span class="sxs-lookup"><span data-stu-id="380a7-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="380a7-107">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Договоры о банковских услугах".</span><span class="sxs-lookup"><span data-stu-id="380a7-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="380a7-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="380a7-108">Click New.</span></span>
3. <span data-ttu-id="380a7-109">В поле "Номер договора" введите номер договора с банком для проводки.</span><span class="sxs-lookup"><span data-stu-id="380a7-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="380a7-110">В поле "Банковский счет" выберите номер банковского счета, для которого открыто гарантийное письмо.</span><span class="sxs-lookup"><span data-stu-id="380a7-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="380a7-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="380a7-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="380a7-112">В поле "Дата начала" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="380a7-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="380a7-113">В поле "Дата окончания" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="380a7-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="380a7-114">Переключите развертывание раздела "Общее".</span><span class="sxs-lookup"><span data-stu-id="380a7-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="380a7-115">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="380a7-115">Click Add line.</span></span>
10. <span data-ttu-id="380a7-116">В поле "Тип ссуды" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="380a7-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="380a7-117">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="380a7-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="380a7-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="380a7-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="380a7-119">В поле "Лимит" введите сумму, оговоренную с банком.</span><span class="sxs-lookup"><span data-stu-id="380a7-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="380a7-120">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="380a7-120">Click Save.</span></span>
15. <span data-ttu-id="380a7-121">Переключите развертывание раздела "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="380a7-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="380a7-122">В поле "Метод расчета" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="380a7-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="380a7-123">Введите метод расчета и сведения о процентах для денежной маржи, комиссии выпуска, комиссии расширения, комиссии увеличения стоимости или комиссии уменьшения стоимости, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="380a7-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="380a7-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="380a7-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="380a7-125">Продление договора о банковских услугах</span><span class="sxs-lookup"><span data-stu-id="380a7-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="380a7-126">Щелкните "Развернуть", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="380a7-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="380a7-127">В поле "Новый номер договора" введите значение.</span><span class="sxs-lookup"><span data-stu-id="380a7-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="380a7-128">В поле "Дата окончания" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="380a7-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="380a7-129">Щелкните "Развернуть".</span><span class="sxs-lookup"><span data-stu-id="380a7-129">Click Extend.</span></span>
5. <span data-ttu-id="380a7-130">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="380a7-130">Click Save.</span></span>
6. <span data-ttu-id="380a7-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="380a7-131">Close the page.</span></span>

