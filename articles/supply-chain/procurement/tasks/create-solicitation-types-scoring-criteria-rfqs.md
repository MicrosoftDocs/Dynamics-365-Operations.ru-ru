---
title: Создание типов обращений и критериев оценки для запросов предложений
description: В этом руководстве показано, как создать тип обращения и связать его с методом оценки.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57abbab21a20278d77001a39e226af11994230be
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149649"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="d82ab-103">Создание типов обращений и критериев оценки для запросов предложений</span><span class="sxs-lookup"><span data-stu-id="d82ab-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d82ab-104">В этом руководстве показано, как создать тип обращения и связать его с методом оценки.</span><span class="sxs-lookup"><span data-stu-id="d82ab-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="d82ab-105">В нем также показано, как использовать тип обращения в запросе предложения, который задает метод оценки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d82ab-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="d82ab-106">Эти задачи обычно выполняются менеджером по закупкам.</span><span class="sxs-lookup"><span data-stu-id="d82ab-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="d82ab-107">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="d82ab-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d82ab-108">Необходимо иметь доступный метод оценки перед началом работы.</span><span class="sxs-lookup"><span data-stu-id="d82ab-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="d82ab-109">Создание типа обращения</span><span class="sxs-lookup"><span data-stu-id="d82ab-109">Create a solicitation type</span></span>
1. <span data-ttu-id="d82ab-110">Перейдите в раздел "Закупки и источники" > "Настройка" > "Запрос предложения" > "Тип обращения".</span><span class="sxs-lookup"><span data-stu-id="d82ab-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="d82ab-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d82ab-111">Click New.</span></span>
3. <span data-ttu-id="d82ab-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d82ab-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d82ab-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d82ab-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d82ab-114">В поле "Метод оценки" выберите метод оценки, который требуется использовать для этого типа обращения.</span><span class="sxs-lookup"><span data-stu-id="d82ab-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="d82ab-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d82ab-115">Click Save.</span></span>
7. <span data-ttu-id="d82ab-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d82ab-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="d82ab-117">Использование типа обращения</span><span class="sxs-lookup"><span data-stu-id="d82ab-117">Use the solicitation type</span></span>
1. <span data-ttu-id="d82ab-118">Перейдите в раздел "Закупки и источники" > "Запросы предложений" > "Все запросы предложений".</span><span class="sxs-lookup"><span data-stu-id="d82ab-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="d82ab-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d82ab-119">Click New.</span></span>
3. <span data-ttu-id="d82ab-120">В поле "Тип обращения" выберите созданный тип обращения.</span><span class="sxs-lookup"><span data-stu-id="d82ab-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="d82ab-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d82ab-121">Click OK.</span></span>
5. <span data-ttu-id="d82ab-122">Щелкните "Критерии оценки".</span><span class="sxs-lookup"><span data-stu-id="d82ab-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="d82ab-123">Отображаемые критерии оценки — это критерии из метода оценки, связанного с типом обращения.</span><span class="sxs-lookup"><span data-stu-id="d82ab-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="d82ab-124">Можно добавить или удалить критерии на этой странице.</span><span class="sxs-lookup"><span data-stu-id="d82ab-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="d82ab-125">Также можно добавить новый критерий, скопировав его из других методов оценки.</span><span class="sxs-lookup"><span data-stu-id="d82ab-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="d82ab-126">Щелкните "Копировать критерии".</span><span class="sxs-lookup"><span data-stu-id="d82ab-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="d82ab-127">В поле "Метод оценки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d82ab-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="d82ab-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d82ab-128">Click OK.</span></span>
9. <span data-ttu-id="d82ab-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d82ab-129">Close the page.</span></span>

