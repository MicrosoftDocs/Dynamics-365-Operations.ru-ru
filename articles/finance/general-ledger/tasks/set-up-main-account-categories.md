---
title: Настройка категорий счетов ГК
description: В этой теме описывается, как настроить категории счетов ГК в Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0a015283064af2287013bccc065b4467a308c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447127"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="d47ab-103">Настройка категорий счетов ГК</span><span class="sxs-lookup"><span data-stu-id="d47ab-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d47ab-104">В этой теме описывается, как настроить категории счетов ГК.</span><span class="sxs-lookup"><span data-stu-id="d47ab-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="d47ab-105">Категории счетов ГК используются для отчетов по умолчанию в финансовой отчетности и в Power BI.</span><span class="sxs-lookup"><span data-stu-id="d47ab-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="d47ab-106">Категории счетов ГК, созданные по умолчанию, могут быть переименованы, но не могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="d47ab-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="d47ab-107">Дополнительные категории счетов можно создавать и использовать для отчетности и анализа.</span><span class="sxs-lookup"><span data-stu-id="d47ab-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="d47ab-108">В этой теме используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="d47ab-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="d47ab-109">Создание категории счета ГК</span><span class="sxs-lookup"><span data-stu-id="d47ab-109">Create a main account category</span></span>
1. <span data-ttu-id="d47ab-110">В области перехода выберите **Модули > Главная книга > План счетов > Счета > Категории счета ГК**.</span><span class="sxs-lookup"><span data-stu-id="d47ab-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="d47ab-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d47ab-111">Select **New**.</span></span>
3. <span data-ttu-id="d47ab-112">В поле **Категория счета ГК** введите уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="d47ab-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="d47ab-113">В поле **Описание** введите описание категории счета ГК.</span><span class="sxs-lookup"><span data-stu-id="d47ab-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="d47ab-114">В поле **Тип счета ГК** выберите тип счета ГК, который будет связан с категорией.</span><span class="sxs-lookup"><span data-stu-id="d47ab-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="d47ab-115">Связывание счетов ГК с категорией счета</span><span class="sxs-lookup"><span data-stu-id="d47ab-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="d47ab-116">Щелкните **Связать счета ГК**.</span><span class="sxs-lookup"><span data-stu-id="d47ab-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="d47ab-117">В списке выберите счета ГК для назначения категории счетов ГК, установив флажки в столбце **Связано**.</span><span class="sxs-lookup"><span data-stu-id="d47ab-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="d47ab-118">При назначении счетов ГК для категории счета ГК суммируются сальдо счетов, когда эта категория используется для финансовой отчетности и анализа.</span><span class="sxs-lookup"><span data-stu-id="d47ab-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="d47ab-119">Выберите или отмените выбор параметра **Связано**, чтобы выбрать счета ГК.</span><span class="sxs-lookup"><span data-stu-id="d47ab-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="d47ab-120">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d47ab-120">Select **OK**.</span></span>
5. <span data-ttu-id="d47ab-121">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="d47ab-121">Select **Yes**.</span></span>
