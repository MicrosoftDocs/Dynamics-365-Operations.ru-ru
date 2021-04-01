---
title: Копирование формулы
description: Эта процедура заключается в создании формулы, содержащей те же компоненты, что и существующая формула, но с небольшими отличиями.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdeeb760ab6bb00cefc6b358e53996dd652e5bc6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255333"
---
# <a name="copy-a-formula"></a><span data-ttu-id="adc16-103">Копирование формулы</span><span class="sxs-lookup"><span data-stu-id="adc16-103">Copy a formula</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="adc16-104">Эта процедура заключается в создании формулы, содержащей те же компоненты, что и существующая формула, но с небольшими отличиями.</span><span class="sxs-lookup"><span data-stu-id="adc16-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="adc16-105">Чтобы создать строки формулы, можно воспользоваться функцией Копировать для копирования существующей формулы, содержащей большинство необходимых компонентов.</span><span class="sxs-lookup"><span data-stu-id="adc16-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="adc16-106">Затем можно внести любые необходимые изменения в отдельные строки в новой версии.</span><span class="sxs-lookup"><span data-stu-id="adc16-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="adc16-107">При использовании функции Копировать нет необходимости создавать несколько формул, которые почти не отличаются друг от друга.</span><span class="sxs-lookup"><span data-stu-id="adc16-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="adc16-108">В качестве компании с демонстрационными данными для создания этой задачи используется USP2.</span><span class="sxs-lookup"><span data-stu-id="adc16-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="adc16-109">Создание формулы</span><span class="sxs-lookup"><span data-stu-id="adc16-109">Create a formula</span></span>
1. <span data-ttu-id="adc16-110">Перейдите в раздел "Управление сведениями о продукте" > "Спецификации и формулы" > "Формулы".</span><span class="sxs-lookup"><span data-stu-id="adc16-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="adc16-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="adc16-111">Click New.</span></span>
3. <span data-ttu-id="adc16-112">В поле "Формула" введите значение.</span><span class="sxs-lookup"><span data-stu-id="adc16-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="adc16-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="adc16-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="adc16-114">Введите информативное имя для формулы.</span><span class="sxs-lookup"><span data-stu-id="adc16-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="adc16-115">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="adc16-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="adc16-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="adc16-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="adc16-117">В поле "Номенклатурная группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="adc16-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="adc16-118">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="adc16-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="adc16-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="adc16-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="adc16-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="adc16-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="adc16-121">Копирование строк формулы</span><span class="sxs-lookup"><span data-stu-id="adc16-121">Copy formula lines</span></span>
1. <span data-ttu-id="adc16-122">В области действий щелкните "Формула".</span><span class="sxs-lookup"><span data-stu-id="adc16-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="adc16-123">Щелкните Копировать.</span><span class="sxs-lookup"><span data-stu-id="adc16-123">Click Copy.</span></span>
3. <span data-ttu-id="adc16-124">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="adc16-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="adc16-125">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="adc16-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="adc16-126">В поле "Версия формулы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="adc16-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="adc16-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="adc16-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="adc16-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="adc16-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="adc16-129">Корректировка скопированных строк формулы</span><span class="sxs-lookup"><span data-stu-id="adc16-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="adc16-130">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="adc16-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="adc16-131">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="adc16-131">Click Delete.</span></span>
3. <span data-ttu-id="adc16-132">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="adc16-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="adc16-133">Утвердить формулу</span><span class="sxs-lookup"><span data-stu-id="adc16-133">Approve formula</span></span>
1. <span data-ttu-id="adc16-134">В области действий щелкните "Формула".</span><span class="sxs-lookup"><span data-stu-id="adc16-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="adc16-135">Щелкните Утвердить формулу.</span><span class="sxs-lookup"><span data-stu-id="adc16-135">Click Approve formula.</span></span>
3. <span data-ttu-id="adc16-136">В поле "Кем утверждено" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="adc16-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="adc16-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="adc16-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="adc16-138">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="adc16-138">Click Select.</span></span>
6. <span data-ttu-id="adc16-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="adc16-139">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]