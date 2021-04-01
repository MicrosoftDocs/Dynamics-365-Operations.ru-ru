---
title: Настройка типов расходов
description: В этом разделе объясняется, как настраивать типы расходов в аренде активов.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1538826f140393eec59be9ff4df5242d5ced9d8f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249757"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="64a52-103">Настройка типов расходов</span><span class="sxs-lookup"><span data-stu-id="64a52-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64a52-104">В этом разделе объясняется, как настраивать типы расходов в аренде активов.</span><span class="sxs-lookup"><span data-stu-id="64a52-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="64a52-105">Затраты, не представленные графиком оплаты, называются *расходными затратами*.</span><span class="sxs-lookup"><span data-stu-id="64a52-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="64a52-106">Примерами таких затрат являются налоги на собственность, затраты на общее мест общего пользования и страховые расходы.</span><span class="sxs-lookup"><span data-stu-id="64a52-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="64a52-107">Добавление типа административных расходов</span><span class="sxs-lookup"><span data-stu-id="64a52-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="64a52-108">Перейдите в раздел **Аренда активов \> Настройка \> Типы расходов**.</span><span class="sxs-lookup"><span data-stu-id="64a52-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="64a52-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="64a52-109">Select **New**.</span></span>
3. <span data-ttu-id="64a52-110">В соответствующих полях введите новый тип расходов и описание.</span><span class="sxs-lookup"><span data-stu-id="64a52-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="64a52-111">Назначение счетов для административных затрат</span><span class="sxs-lookup"><span data-stu-id="64a52-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="64a52-112">Далее следует связать счета с типами расходов.</span><span class="sxs-lookup"><span data-stu-id="64a52-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="64a52-113">Эти счета будут дебетоваться при разноске записей графика расходов.</span><span class="sxs-lookup"><span data-stu-id="64a52-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="64a52-114">Корр. счет указывается в строках **График платежей по затратам на осуществление аренды** в каждой аренде.</span><span class="sxs-lookup"><span data-stu-id="64a52-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="64a52-115">Перейдите в раздел **Аренда активов \> Настройка \> Параметры аренды активов**.</span><span class="sxs-lookup"><span data-stu-id="64a52-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="64a52-116">На вкладке **Счета** на экспресс-вкладке **Затраты на осуществление аренды** в поле **Тип расходов** выберите тип расходов.</span><span class="sxs-lookup"><span data-stu-id="64a52-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="64a52-117">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="64a52-117">Select **Add**.</span></span>
4. <span data-ttu-id="64a52-118">В поле **Тип книги** выберите тип книги для связи с административными затратами.</span><span class="sxs-lookup"><span data-stu-id="64a52-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="64a52-119">Несколько типов книг могут быть привязаны к одному и тому же счету расходов.</span><span class="sxs-lookup"><span data-stu-id="64a52-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="64a52-120">В поле **Код счета** укажите аренды, к которым должна применяться данная книга:</span><span class="sxs-lookup"><span data-stu-id="64a52-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="64a52-121">**Все** — книга применяется ко всем арендам.</span><span class="sxs-lookup"><span data-stu-id="64a52-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="64a52-122">**Группа** — применение книги к конкретной группе аренд.</span><span class="sxs-lookup"><span data-stu-id="64a52-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="64a52-123">**Таблица** — книга применяется к конкретным арендам.</span><span class="sxs-lookup"><span data-stu-id="64a52-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="64a52-124">Если вы выбрали **Группа** или **Таблица** в поле **Код счета**, выберите номер счета или номер группы в поле **Номер счета или группы**.</span><span class="sxs-lookup"><span data-stu-id="64a52-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="64a52-125">В соответствующих полях выберите счет ГК для финансовой аренды и счет ГК для операционной аренды.</span><span class="sxs-lookup"><span data-stu-id="64a52-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="64a52-126">После выполнения этих шагов можно добавлять расходы с помощью строк **График оплаты затрат на осуществление аренды** на странице **Сведения об аренде** для выбранной аренды.</span><span class="sxs-lookup"><span data-stu-id="64a52-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="64a52-127">Кроме того, можно добавлять расходы при создании новой аренды.</span><span class="sxs-lookup"><span data-stu-id="64a52-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]