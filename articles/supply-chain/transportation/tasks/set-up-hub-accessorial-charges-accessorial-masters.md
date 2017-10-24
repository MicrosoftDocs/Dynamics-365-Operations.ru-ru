--- 
title: "Настройка дополнительных расходов и справочников дополнений для узла"
description: "В этой процедуре показано, как создать справочник дополнений для узла и, используя этот справочник, создать дополнительные расходы для узла."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6381416640ffacf0a9d96d7da96bc33612ca7137
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="ac697-103">Настройка дополнительных расходов и справочников дополнений для узла</span><span class="sxs-lookup"><span data-stu-id="ac697-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac697-104">В этой процедуре показано, как создать справочник дополнений для узла и, используя этот справочник, создать дополнительные расходы для узла.</span><span class="sxs-lookup"><span data-stu-id="ac697-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="ac697-105">В процедуре используется набор данных USMF.</span><span class="sxs-lookup"><span data-stu-id="ac697-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="ac697-106">Обычно это настраивается координатором транспортировки.</span><span class="sxs-lookup"><span data-stu-id="ac697-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="ac697-107">Настройка шаблона узла</span><span class="sxs-lookup"><span data-stu-id="ac697-107">Set up a hub master</span></span>
1. <span data-ttu-id="ac697-108">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Расчет ставок" > "Шаблоны дополнения".</span><span class="sxs-lookup"><span data-stu-id="ac697-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="ac697-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ac697-109">Click New.</span></span>
3. <span data-ttu-id="ac697-110">В поле "Шаблон дополнения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ac697-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="ac697-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ac697-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ac697-112">В поле "Тип дополнения" выберите "Узел".</span><span class="sxs-lookup"><span data-stu-id="ac697-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="ac697-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ac697-113">Click Save.</span></span>
7. <span data-ttu-id="ac697-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ac697-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="ac697-115">Настройка дополнительных расходов для узла</span><span class="sxs-lookup"><span data-stu-id="ac697-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="ac697-116">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Расчет ставок" > "Дополнительные расходы узла".</span><span class="sxs-lookup"><span data-stu-id="ac697-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="ac697-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ac697-117">Click New.</span></span>
3. <span data-ttu-id="ac697-118">В поле "Код дополнительного узла" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ac697-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="ac697-119">В поле "Узел" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="ac697-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ac697-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ac697-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="ac697-121">В поле "Позиция узла" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="ac697-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="ac697-122">Расходы можно создавать как вывоз или разгрузку.</span><span class="sxs-lookup"><span data-stu-id="ac697-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="ac697-123">В зависимости от выбранного варианта расходы будут применяться к соответствующему сегменту транспортировки на маршруте.</span><span class="sxs-lookup"><span data-stu-id="ac697-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="ac697-124">В поле "Шаблон дополнения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="ac697-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ac697-125">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ac697-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ac697-126">Выберите только что созданный справочник.</span><span class="sxs-lookup"><span data-stu-id="ac697-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="ac697-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ac697-127">Click Save.</span></span>
10. <span data-ttu-id="ac697-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ac697-128">Close the page.</span></span>


