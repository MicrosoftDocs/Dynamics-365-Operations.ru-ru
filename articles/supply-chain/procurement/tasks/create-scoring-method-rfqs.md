---
title: Создание метода оценки для запросов предложений
description: Следующая процедура используется для создания метода оценки.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6cbbc941b810cd8e5db5ba15a23dc6bd72a29506
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838078"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="538d9-103">Создание метода оценки для запросов предложений</span><span class="sxs-lookup"><span data-stu-id="538d9-103">Create a scoring method for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="538d9-104">Следующая процедура используется для создания метода оценки.</span><span class="sxs-lookup"><span data-stu-id="538d9-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="538d9-105">Метод оценки — это набор критериев, которые можно использовать для сравнения предложений, отправляемых в ответ на запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="538d9-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="538d9-106">Например, может потребоваться оценить поставщика по его производительности в прошлом, оценить, является ли деятельность компании безопасной для окружающей среды и насколько просто с ней сотрудничать, либо сравнить предложения на основе цены.</span><span class="sxs-lookup"><span data-stu-id="538d9-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="538d9-107">Метод оценки можно связать с типом обращения как метод оценки по умолчанию для запросов предложения этого типа.</span><span class="sxs-lookup"><span data-stu-id="538d9-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="538d9-108">Эти задачи обычно выполняются менеджером по закупкам.</span><span class="sxs-lookup"><span data-stu-id="538d9-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="538d9-109">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="538d9-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="538d9-110">Перейдите в раздел "Закупки и источники" > "Настройка" > "Запрос предложения" > "Метод оценки".</span><span class="sxs-lookup"><span data-stu-id="538d9-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="538d9-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="538d9-111">Click New.</span></span>
3. <span data-ttu-id="538d9-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="538d9-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="538d9-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="538d9-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="538d9-114">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="538d9-114">Click Save.</span></span>
6. <span data-ttu-id="538d9-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="538d9-115">Click New.</span></span>
7. <span data-ttu-id="538d9-116">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="538d9-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="538d9-117">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="538d9-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="538d9-118">Это описание отображается вместе с именем метода оценки при выборе метода оценки для запроса предложения.</span><span class="sxs-lookup"><span data-stu-id="538d9-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="538d9-119">В поле "Начало диапазона" введите число.</span><span class="sxs-lookup"><span data-stu-id="538d9-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="538d9-120">Диапазон ограничивает данные, которые специалист по закупкам может ввести как оценку.</span><span class="sxs-lookup"><span data-stu-id="538d9-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="538d9-121">Если в запросе предложения несколько критериев оценки, вводимые оценки складываются, и сумма становится доступна для сравнения предложений.</span><span class="sxs-lookup"><span data-stu-id="538d9-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="538d9-122">В поле "Конец диапазона" введите число.</span><span class="sxs-lookup"><span data-stu-id="538d9-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="538d9-123">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="538d9-123">Click New.</span></span>
12. <span data-ttu-id="538d9-124">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="538d9-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="538d9-125">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="538d9-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="538d9-126">В поле "Начало диапазона" введите число.</span><span class="sxs-lookup"><span data-stu-id="538d9-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="538d9-127">В поле "Конец диапазона" введите число.</span><span class="sxs-lookup"><span data-stu-id="538d9-127">In the Range to field, enter a number.</span></span>

