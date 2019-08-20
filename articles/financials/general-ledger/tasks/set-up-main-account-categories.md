---
title: Настройка категорий счетов ГК
description: Категории счетов ГК используются для отчетов по умолчанию в финансовой отчетности и в Power BI.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: e33df434b6a4361872bad10250fe3547d7c4affa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834814"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="05f80-103">Настройка категорий счетов ГК</span><span class="sxs-lookup"><span data-stu-id="05f80-103">Set up main account categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05f80-104">Категории счетов ГК используются для отчетов по умолчанию в финансовой отчетности и в Power BI.</span><span class="sxs-lookup"><span data-stu-id="05f80-104">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="05f80-105">Категории счетов ГК, созданные по умолчанию, могут быть переименованы, но не могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="05f80-105">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="05f80-106">Дополнительные категории счетов можно создавать и использовать для отчетности и анализа.</span><span class="sxs-lookup"><span data-stu-id="05f80-106">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="05f80-107">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="05f80-107">This task uses the USMF demo company.</span></span>


## <a name="create-a-main-account-category"></a><span data-ttu-id="05f80-108">Создание категории счета ГК</span><span class="sxs-lookup"><span data-stu-id="05f80-108">Create a main account category</span></span>
1. <span data-ttu-id="05f80-109">Перейдите в раздел "Главная книга" > "План счетов" > "Счета" > "Категории счета ГК".</span><span class="sxs-lookup"><span data-stu-id="05f80-109">Go to General ledger > Chart of accounts > Accounts > Main account categories.</span></span>
2. <span data-ttu-id="05f80-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="05f80-110">Click New.</span></span>
3. <span data-ttu-id="05f80-111">В поле "Категория счета ГК" введите уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="05f80-111">In the Main account category field, enter a unique name.</span></span>
4. <span data-ttu-id="05f80-112">В поле "Описание" введите описание категории счета ГК.</span><span class="sxs-lookup"><span data-stu-id="05f80-112">In the Description field, enter a description for the main account category.</span></span>
5. <span data-ttu-id="05f80-113">В поле "Тип счета ГК" выберите тип счета ГК, который будет связан с категорией.</span><span class="sxs-lookup"><span data-stu-id="05f80-113">In the Main account type field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="05f80-114">Связывание счетов ГК с категорией счета</span><span class="sxs-lookup"><span data-stu-id="05f80-114">Link main accounts to account category</span></span>
1. <span data-ttu-id="05f80-115">Щелкните "Связать счета ГК".</span><span class="sxs-lookup"><span data-stu-id="05f80-115">Click Link main accounts.</span></span>
2. <span data-ttu-id="05f80-116">В списке выберите счета ГК для назначения для категории счетов ГК.</span><span class="sxs-lookup"><span data-stu-id="05f80-116">In the list, select the main accounts to assign to the main account category.</span></span>
    * <span data-ttu-id="05f80-117">При назначении счетов ГК для категории счета ГК суммируются сальдо счетов, когда эта категория используется для финансовой отчетности и анализа.</span><span class="sxs-lookup"><span data-stu-id="05f80-117">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="05f80-118">Выберите или отмените выбор параметра "Связано", чтобы выбрать счета ГК.</span><span class="sxs-lookup"><span data-stu-id="05f80-118">Select or clear the Linked option to choose the main accounts.</span></span>
4. <span data-ttu-id="05f80-119">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="05f80-119">Click OK.</span></span>
5. <span data-ttu-id="05f80-120">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="05f80-120">Click Yes.</span></span>

