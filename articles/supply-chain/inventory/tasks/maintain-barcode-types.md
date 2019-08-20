---
title: Ведение типов штрих-кодов
description: Эта процедура описывает, как настроить новое определение штрих-кода, которое можно использовать как часть отчета листа подбора.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0551784ff55f5dc05fbe92ee354316eb04d755cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845470"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="46f97-103">Ведение типов штрих-кодов</span><span class="sxs-lookup"><span data-stu-id="46f97-103">Maintain barcode types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46f97-104">Эта процедура описывает, как настроить новое определение штрих-кода, которое можно использовать как часть отчета листа подбора.</span><span class="sxs-lookup"><span data-stu-id="46f97-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="46f97-105">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="46f97-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="46f97-106">При использовании USMF можно использовать представленные примеры значений.</span><span class="sxs-lookup"><span data-stu-id="46f97-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="46f97-107">Эти задачи обычно выполняются менеджером склада.</span><span class="sxs-lookup"><span data-stu-id="46f97-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="46f97-108">Перейдите штрих-кодам.</span><span class="sxs-lookup"><span data-stu-id="46f97-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="46f97-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="46f97-109">Click New.</span></span>
3. <span data-ttu-id="46f97-110">В поле "Настройка штрих-кода" введите значение.</span><span class="sxs-lookup"><span data-stu-id="46f97-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="46f97-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="46f97-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="46f97-112">В поле "Тип штрих-кода" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="46f97-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="46f97-113">При использовании USMF можно выбрать "Code 39".</span><span class="sxs-lookup"><span data-stu-id="46f97-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="46f97-114">В поле "Размер" введите число.</span><span class="sxs-lookup"><span data-stu-id="46f97-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="46f97-115">В поле "Максимальная длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="46f97-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="46f97-116">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="46f97-116">Click Save.</span></span>
9. <span data-ttu-id="46f97-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="46f97-117">Close the page.</span></span>
10. <span data-ttu-id="46f97-118">Перейдите к параметрам модуля "Управление запасами и складами".</span><span class="sxs-lookup"><span data-stu-id="46f97-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="46f97-119">В поле "Настройка штрих-кода" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="46f97-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="46f97-120">Выберите настройку штрих-кода, созданную ранее, но помните, что формат штрих-кода должен соответствовать формату уникального кода для типа записи, используемой в процессе.</span><span class="sxs-lookup"><span data-stu-id="46f97-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="46f97-121">Например, для маршрутов комплектации формат штрих-кода должен соответствовать формату ссылки маршрута комплектации, которая обычно является номерной серией.</span><span class="sxs-lookup"><span data-stu-id="46f97-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="46f97-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="46f97-122">Click Save.</span></span>
13. <span data-ttu-id="46f97-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="46f97-123">Close the page.</span></span>

