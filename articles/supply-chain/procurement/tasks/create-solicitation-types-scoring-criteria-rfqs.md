---
title: Создание типов обращений и критериев оценки для запросов предложений
description: В этом руководстве показано, как создать тип обращения и связать его с методом оценки.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b3876238a191cbbacc4e8c435bb798232e6fd6f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204685"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="898c6-103">Создание типов обращений и критериев оценки для запросов предложений</span><span class="sxs-lookup"><span data-stu-id="898c6-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="898c6-104">В этом руководстве показано, как создать тип обращения и связать его с методом оценки.</span><span class="sxs-lookup"><span data-stu-id="898c6-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="898c6-105">В нем также показано, как использовать тип обращения в запросе предложения, который задает метод оценки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="898c6-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="898c6-106">Эти задачи обычно выполняются менеджером по закупкам.</span><span class="sxs-lookup"><span data-stu-id="898c6-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="898c6-107">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="898c6-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="898c6-108">Необходимо иметь доступный метод оценки перед началом работы.</span><span class="sxs-lookup"><span data-stu-id="898c6-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="898c6-109">Создание типа обращения</span><span class="sxs-lookup"><span data-stu-id="898c6-109">Create a solicitation type</span></span>
1. <span data-ttu-id="898c6-110">Перейдите в раздел "Закупки и источники" > "Настройка" > "Запрос предложения" > "Тип обращения".</span><span class="sxs-lookup"><span data-stu-id="898c6-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="898c6-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="898c6-111">Click New.</span></span>
3. <span data-ttu-id="898c6-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="898c6-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="898c6-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="898c6-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="898c6-114">В поле "Метод оценки" выберите метод оценки, который требуется использовать для этого типа обращения.</span><span class="sxs-lookup"><span data-stu-id="898c6-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="898c6-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="898c6-115">Click Save.</span></span>
7. <span data-ttu-id="898c6-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="898c6-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="898c6-117">Использование типа обращения</span><span class="sxs-lookup"><span data-stu-id="898c6-117">Use the solicitation type</span></span>
1. <span data-ttu-id="898c6-118">Перейдите в раздел "Закупки и источники" > "Запросы предложений" > "Все запросы предложений".</span><span class="sxs-lookup"><span data-stu-id="898c6-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="898c6-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="898c6-119">Click New.</span></span>
3. <span data-ttu-id="898c6-120">В поле "Тип обращения" выберите созданный тип обращения.</span><span class="sxs-lookup"><span data-stu-id="898c6-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="898c6-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="898c6-121">Click OK.</span></span>
5. <span data-ttu-id="898c6-122">Щелкните "Критерии оценки".</span><span class="sxs-lookup"><span data-stu-id="898c6-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="898c6-123">Отображаемые критерии оценки — это критерии из метода оценки, связанного с типом обращения.</span><span class="sxs-lookup"><span data-stu-id="898c6-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="898c6-124">Можно добавить или удалить критерии на этой странице.</span><span class="sxs-lookup"><span data-stu-id="898c6-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="898c6-125">Также можно добавить новый критерий, скопировав его из других методов оценки.</span><span class="sxs-lookup"><span data-stu-id="898c6-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="898c6-126">Щелкните "Копировать критерии".</span><span class="sxs-lookup"><span data-stu-id="898c6-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="898c6-127">В поле "Метод оценки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="898c6-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="898c6-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="898c6-128">Click OK.</span></span>
9. <span data-ttu-id="898c6-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="898c6-129">Close the page.</span></span>

