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
ms.openlocfilehash: 7834745923bf5ec05018ff5829ddaa0b75df5db7
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145599"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="75637-103">Ведение типов штрих-кодов</span><span class="sxs-lookup"><span data-stu-id="75637-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75637-104">Эта процедура описывает, как настроить новое определение штрих-кода, которое можно использовать как часть отчета листа подбора.</span><span class="sxs-lookup"><span data-stu-id="75637-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="75637-105">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="75637-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="75637-106">При использовании USMF можно использовать представленные примеры значений.</span><span class="sxs-lookup"><span data-stu-id="75637-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="75637-107">Эти задачи обычно выполняются менеджером склада.</span><span class="sxs-lookup"><span data-stu-id="75637-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="75637-108">Перейдите штрих-кодам.</span><span class="sxs-lookup"><span data-stu-id="75637-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="75637-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="75637-109">Click New.</span></span>
3. <span data-ttu-id="75637-110">В поле "Настройка штрих-кода" введите значение.</span><span class="sxs-lookup"><span data-stu-id="75637-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="75637-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="75637-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="75637-112">В поле "Тип штрих-кода" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="75637-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="75637-113">При использовании USMF можно выбрать "Code 39".</span><span class="sxs-lookup"><span data-stu-id="75637-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="75637-114">В поле "Размер" введите число.</span><span class="sxs-lookup"><span data-stu-id="75637-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="75637-115">В поле "Максимальная длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="75637-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="75637-116">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="75637-116">Click Save.</span></span>
9. <span data-ttu-id="75637-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="75637-117">Close the page.</span></span>
10. <span data-ttu-id="75637-118">Перейдите к параметрам модуля "Управление запасами и складами".</span><span class="sxs-lookup"><span data-stu-id="75637-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="75637-119">В поле "Настройка штрих-кода" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="75637-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="75637-120">Выберите настройку штрих-кода, созданную ранее, но помните, что формат штрих-кода должен соответствовать формату уникального кода для типа записи, используемой в процессе.</span><span class="sxs-lookup"><span data-stu-id="75637-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="75637-121">Например, для маршрутов комплектации формат штрих-кода должен соответствовать формату ссылки маршрута комплектации, которая обычно является номерной серией.</span><span class="sxs-lookup"><span data-stu-id="75637-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="75637-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="75637-122">Click Save.</span></span>
13. <span data-ttu-id="75637-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="75637-123">Close the page.</span></span>

