---
title: Ведение типов штрих-кодов
description: Эта процедура описывает, как настроить новое определение штрих-кода, которое можно использовать как часть отчета листа подбора.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 112438417e425b8b77dd56f25e0b6e6db21c5148
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244407"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="7619c-103">Ведение типов штрих-кодов</span><span class="sxs-lookup"><span data-stu-id="7619c-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7619c-104">Эта процедура описывает, как настроить новое определение штрих-кода, которое можно использовать как часть отчета листа подбора.</span><span class="sxs-lookup"><span data-stu-id="7619c-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="7619c-105">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="7619c-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="7619c-106">При использовании USMF можно использовать представленные примеры значений.</span><span class="sxs-lookup"><span data-stu-id="7619c-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="7619c-107">Эти задачи обычно выполняются менеджером склада.</span><span class="sxs-lookup"><span data-stu-id="7619c-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="7619c-108">Перейдите штрих-кодам.</span><span class="sxs-lookup"><span data-stu-id="7619c-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="7619c-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7619c-109">Click New.</span></span>
3. <span data-ttu-id="7619c-110">В поле "Настройка штрих-кода" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7619c-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="7619c-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7619c-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7619c-112">В поле "Тип штрих-кода" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="7619c-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="7619c-113">При использовании USMF можно выбрать "Code 39".</span><span class="sxs-lookup"><span data-stu-id="7619c-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="7619c-114">В поле "Размер" введите число.</span><span class="sxs-lookup"><span data-stu-id="7619c-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="7619c-115">В поле "Максимальная длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="7619c-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="7619c-116">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="7619c-116">Click Save.</span></span>
9. <span data-ttu-id="7619c-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7619c-117">Close the page.</span></span>
10. <span data-ttu-id="7619c-118">Перейдите к параметрам модуля "Управление запасами и складами".</span><span class="sxs-lookup"><span data-stu-id="7619c-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="7619c-119">В поле "Настройка штрих-кода" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="7619c-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="7619c-120">Выберите настройку штрих-кода, созданную ранее, но помните, что формат штрих-кода должен соответствовать формату уникального кода для типа записи, используемой в процессе.</span><span class="sxs-lookup"><span data-stu-id="7619c-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="7619c-121">Например, для маршрутов комплектации формат штрих-кода должен соответствовать формату ссылки маршрута комплектации, которая обычно является номерной серией.</span><span class="sxs-lookup"><span data-stu-id="7619c-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="7619c-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="7619c-122">Click Save.</span></span>
13. <span data-ttu-id="7619c-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7619c-123">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]