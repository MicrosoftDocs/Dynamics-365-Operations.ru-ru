---
title: Группы счетов консолидации и дополнительные счета консолидации
description: В этом разделе представлены сведения о группах счетов консолидации и дополнительных счетах консолидации и объясняется, как они используются в Microsoft Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8db7a60656434aafd8114b08c2c0e9493140f27b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179626"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="bc1ea-103">Группы счетов консолидации и дополнительные счета консолидации</span><span class="sxs-lookup"><span data-stu-id="bc1ea-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc1ea-104">В этом разделе представлены сведения о группах счетов консолидации и дополнительных счетах консолидации и объясняется, как они используются в Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 Finance.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="bc1ea-105">Группы счетов консолидации</span><span class="sxs-lookup"><span data-stu-id="bc1ea-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="bc1ea-106">Группы счетов консолидации позволяют создавать группы счетов, которые требуется использовать для консолидации данных.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="bc1ea-107">Чаще всего группа счетов консолидации представляет утвержденный органами власти план счетов или сопоставляет счета с группой, которая определена центральным офисом компании.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="bc1ea-108">Группы счетов консолидации можно найти в области **Настройка** модуля **Консолидации**.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="bc1ea-109">При добавлении новой группы вводится уникальный идентификатор для группы счетов и имя.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="bc1ea-110">Дополнительные счета консолидации</span><span class="sxs-lookup"><span data-stu-id="bc1ea-110">Additional consolidation accounts</span></span>
<span data-ttu-id="bc1ea-111">Дополнительные счета консолидации позволяют назначить счет из существующего плана счетов для группы счетов консолидации.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="bc1ea-112">Затем можно указать значение и имя счета консолидации.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="bc1ea-113">Дополнительные счета консолидации можно найти в области **Настройка** модуля **Консолидации**.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="bc1ea-114">При создании нового счета консолидации необходимо указать следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="bc1ea-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="bc1ea-115">**Счет ГК** — это поле является полем поиска, которое показывает все счета ГК, основанные на плане счетов, выбранном на странице.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="bc1ea-116">При выборе счета его имя автоматически вводится в поле **Наименование счета ГК**.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="bc1ea-117">**Группы счетов консолидации** — это поле используется для указания группы, которой будет назначен счет.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="bc1ea-118">При консолидации двумя разными способами необходимо добавить один и тот же счет во все четыре группы счетов консолидации.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="bc1ea-119">**Счет консолидации** — введите значение счета консолидации.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="bc1ea-120">Это значение не обязательно должен быть счетом из плана счетов.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="bc1ea-121">Это может быть любое требуемое вам значение.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="bc1ea-122">**Имя счета консолидации** — введите имя счета, которое должно отображаться в запросах и отчетах.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="bc1ea-123">**Уровень SAT** — это поле используется для передачи отчета по выпискам по счетам налоговым органам Мексики.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="bc1ea-124">После завершения создания групп счетов консолидации и дополнительных счетов консолидации можно выбрать эту группу в процессе интерактивной консолидации.</span><span class="sxs-lookup"><span data-stu-id="bc1ea-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="bc1ea-125">Дополнительные сведения см. в разделе [Создание групп консолидации и дополнительных счетов консолидации](../general-ledger/tasks/create-consolidation-groups.md).</span><span class="sxs-lookup"><span data-stu-id="bc1ea-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 



