--- 
title: "Создание банковского счета поставщика"
description: "В этой процедуре показано, как создать банковский счет для поставщика."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 636bbafc87835f1cfe5de0301e3f020a8ac01a56
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="5ac49-103">Создание банковского счета поставщика</span><span class="sxs-lookup"><span data-stu-id="5ac49-103">Create a vendor bank account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ac49-104">В этой процедуре показано, как создать банковский счет для поставщика.</span><span class="sxs-lookup"><span data-stu-id="5ac49-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="5ac49-105">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="5ac49-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="5ac49-106">Перейдите в раздел "Закупки и источники" > "Поставщики" > "Все поставщики".</span><span class="sxs-lookup"><span data-stu-id="5ac49-106">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="5ac49-107">Выберите поставщика, для которого необходимо создавать банковский счет, и перейдите по ссылке в коде счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="5ac49-107">Select the vendor that you want to create a bank account for, and then click the link on the Vendor account ID.</span></span>
3. <span data-ttu-id="5ac49-108">В области действий щелкните "Поставщик".</span><span class="sxs-lookup"><span data-stu-id="5ac49-108">On the Action Pane, click Vendor.</span></span>
4. <span data-ttu-id="5ac49-109">Щелкните "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="5ac49-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="5ac49-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="5ac49-110">Click New.</span></span>
6. <span data-ttu-id="5ac49-111">В поле "Банковский счет" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5ac49-111">In the Bank account field, type a value.</span></span>
    * <span data-ttu-id="5ac49-112">Этот код будет использоваться для идентификации банковского счета в запись поставщика.</span><span class="sxs-lookup"><span data-stu-id="5ac49-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="5ac49-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5ac49-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="5ac49-114">В поле "Банковские группы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5ac49-114">In the Bank groups field, enter or select a value.</span></span>
9. <span data-ttu-id="5ac49-115">В поле "Тип кода банка" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="5ac49-115">In the Routing number type field, select an option.</span></span>
    * <span data-ttu-id="5ac49-116">Это тип внутреннего номера, используемого для международных платежей.</span><span class="sxs-lookup"><span data-stu-id="5ac49-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="5ac49-117">В поле "Номер банковского счета" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5ac49-117">In the Bank account number field, type a value.</span></span>
11. <span data-ttu-id="5ac49-118">В поле "SWIFT-код" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5ac49-118">In the SWIFT code field, type a value.</span></span>
12. <span data-ttu-id="5ac49-119">В поле "IBAN" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5ac49-119">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="5ac49-120">Номер IBAN должен указываться в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="5ac49-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="5ac49-121">Например, можно использовать DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="5ac49-121">For example, you could use DE89370400440532013000.</span></span>  
    * <span data-ttu-id="5ac49-122">Банковский счет будет иметь статус "Активно", если достигнуто значение в поле "Действует с" и не превышено значение в поле "Дата окончания срока действия".</span><span class="sxs-lookup"><span data-stu-id="5ac49-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="5ac49-123">Он также будет активным, если поля "Действует с" и "Дата окончания срока действия" пусты.</span><span class="sxs-lookup"><span data-stu-id="5ac49-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="5ac49-124">Ели обе даты, указанные в полях "Действует с" и "Дата окончания срока действия", относятся к будущему периоду, электронные платежи недоступны.</span><span class="sxs-lookup"><span data-stu-id="5ac49-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="5ac49-125">Доступны другие типы платежей, и банковский счет является активным.</span><span class="sxs-lookup"><span data-stu-id="5ac49-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="5ac49-126">Разверните раздел "Настройка".</span><span class="sxs-lookup"><span data-stu-id="5ac49-126">Expand the Setup section.</span></span>
14. <span data-ttu-id="5ac49-127">В поле "Код текста" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5ac49-127">In the Text code field, type a value.</span></span>
    * <span data-ttu-id="5ac49-128">В этом поле указывается код, который отображается в банковской выписке получателя.</span><span class="sxs-lookup"><span data-stu-id="5ac49-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="5ac49-129">В поле "Сообщение в банк" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5ac49-129">In the Message to bank field, type a value.</span></span>
16. <span data-ttu-id="5ac49-130">В поле "Ссылка на курс" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5ac49-130">In the Exchange reference field, type a value.</span></span>
    * <span data-ttu-id="5ac49-131">Это номер ссылки любого валютного курса с изменяемыми или фиксированными условиями.</span><span class="sxs-lookup"><span data-stu-id="5ac49-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>  
17. <span data-ttu-id="5ac49-132">В поле "Валюта" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5ac49-132">In the Currency field, enter or select a value.</span></span>
    * <span data-ttu-id="5ac49-133">Если выпускаются контрольные операции, в этом разделе содержится обзор их статуса ("Ожидание" или "Утверждено").</span><span class="sxs-lookup"><span data-stu-id="5ac49-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="5ac49-134">Разверните раздел "Адрес".</span><span class="sxs-lookup"><span data-stu-id="5ac49-134">Expand the Address section.</span></span>
19. <span data-ttu-id="5ac49-135">Разверните раздел "Контрольные операции".</span><span class="sxs-lookup"><span data-stu-id="5ac49-135">Expand the Prenotes section.</span></span>
20. <span data-ttu-id="5ac49-136">Разверните раздел "Контактная информация".</span><span class="sxs-lookup"><span data-stu-id="5ac49-136">Expand the Contact information section.</span></span>
21. <span data-ttu-id="5ac49-137">В поле "Телефон" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5ac49-137">In the Telephone field, type a value.</span></span>
22. <span data-ttu-id="5ac49-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5ac49-138">Close the page.</span></span>
23. <span data-ttu-id="5ac49-139">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="5ac49-139">Click Edit.</span></span>
24. <span data-ttu-id="5ac49-140">Разверните раздел "Платеж".</span><span class="sxs-lookup"><span data-stu-id="5ac49-140">Expand the Payment section.</span></span>
25. <span data-ttu-id="5ac49-141">В поле "Банковский счет" выберите созданный счет.</span><span class="sxs-lookup"><span data-stu-id="5ac49-141">In the Bank  account field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="5ac49-142">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5ac49-142">Click Save.</span></span>
    * <span data-ttu-id="5ac49-143">Адрес может наследоваться от банковской группы, если оно указана, либо его можно добавить здесь.</span><span class="sxs-lookup"><span data-stu-id="5ac49-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  


