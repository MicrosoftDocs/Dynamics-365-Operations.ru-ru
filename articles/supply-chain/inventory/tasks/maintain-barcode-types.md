---
title: "Ведение типов штрихкодов"
description: "Эта процедура описывает, как настроить новое определение штрих-кода, которое можно использовать как часть отчета листа подбора."
author: perlynne
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: bcaba4b56f665acb97a74982053dfd14d241344d
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="maintain-bar-code-types"></a><span data-ttu-id="01e1f-103">Ведение типов штрихкодов</span><span class="sxs-lookup"><span data-stu-id="01e1f-103">Maintain bar code types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01e1f-104">Эта процедура описывает, как настроить новое определение штрих-кода, которое можно использовать как часть отчета листа подбора.</span><span class="sxs-lookup"><span data-stu-id="01e1f-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="01e1f-105">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="01e1f-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="01e1f-106">При использовании USMF можно использовать представленные примеры значений.</span><span class="sxs-lookup"><span data-stu-id="01e1f-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="01e1f-107">Эти задачи обычно выполняются менеджером склада.</span><span class="sxs-lookup"><span data-stu-id="01e1f-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="01e1f-108">Перейдите штрих-кодам.</span><span class="sxs-lookup"><span data-stu-id="01e1f-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="01e1f-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="01e1f-109">Click New.</span></span>
3. <span data-ttu-id="01e1f-110">В поле "Настройка штрих-кода" введите значение.</span><span class="sxs-lookup"><span data-stu-id="01e1f-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="01e1f-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="01e1f-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="01e1f-112">В поле "Тип штрих-кода" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="01e1f-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="01e1f-113">При использовании USMF можно выбрать "Code 39".</span><span class="sxs-lookup"><span data-stu-id="01e1f-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="01e1f-114">В поле "Размер" введите число.</span><span class="sxs-lookup"><span data-stu-id="01e1f-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="01e1f-115">В поле "Максимальная длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="01e1f-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="01e1f-116">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="01e1f-116">Click Save.</span></span>
9. <span data-ttu-id="01e1f-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01e1f-117">Close the page.</span></span>
10. <span data-ttu-id="01e1f-118">Перейдите к параметрам модуля "Управление запасами и складами".</span><span class="sxs-lookup"><span data-stu-id="01e1f-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="01e1f-119">В поле "Настройка штрих-кода" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01e1f-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="01e1f-120">Выберите настройку штрих-кода, созданную ранее, но помните, что формат штрих-кода должен соответствовать формату уникального кода для типа записи, используемой в процессе.</span><span class="sxs-lookup"><span data-stu-id="01e1f-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="01e1f-121">Например, для маршрутов комплектации формат штрих-кода должен соответствовать формату ссылки маршрута комплектации, которая обычно является номерной серией.</span><span class="sxs-lookup"><span data-stu-id="01e1f-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="01e1f-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="01e1f-122">Click Save.</span></span>
13. <span data-ttu-id="01e1f-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01e1f-123">Close the page.</span></span>

