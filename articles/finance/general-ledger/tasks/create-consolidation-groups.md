---
title: Создание групп консолидации и дополнительных счетов консолидации
description: Эта процедура описывает порядок создания группы счетов консолидации и последующего добавления счетов в группу.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup, MainAccountConsolidateAccount
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a02d6cf5516e63378f4aa356627c069404546e07
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216528"
---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="191b5-103">Создание групп консолидации и дополнительных счетов консолидации</span><span class="sxs-lookup"><span data-stu-id="191b5-103">Create consolidation groups and additional consolidation accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="191b5-104">Эта процедура описывает порядок создания группы счетов консолидации и последующего добавления счетов в группу.</span><span class="sxs-lookup"><span data-stu-id="191b5-104">This procedure shows how to create a consolidation account group and then add accounts to the group.</span></span> <span data-ttu-id="191b5-105">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="191b5-105">This procedure uses the demo data company USMF.</span></span>


## <a name="create-a-consolidation-account-group"></a><span data-ttu-id="191b5-106">Создание группы счетов консолидации</span><span class="sxs-lookup"><span data-stu-id="191b5-106">Create a consolidation account group</span></span>
1. <span data-ttu-id="191b5-107">Перейдите в раздел "Главная книга" > "План счетов" > "Счета" > "Группы счетов консолидации".</span><span class="sxs-lookup"><span data-stu-id="191b5-107">Go to General ledger > Chart of accounts > Accounts > Consolidation account groups.</span></span>
2. <span data-ttu-id="191b5-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="191b5-108">Click New.</span></span>
3. <span data-ttu-id="191b5-109">В поле "Группа счетов консолидации" введите уникальный идентификатор для группы счетов консолидации.</span><span class="sxs-lookup"><span data-stu-id="191b5-109">In the Consolidation account group field, enter a unique identifier for the consolidation account group.</span></span>
4. <span data-ttu-id="191b5-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="191b5-110">In the Name field, type a value.</span></span>

## <a name="add-accounts-to-consolidation-account-group"></a><span data-ttu-id="191b5-111">Добавление счетов в группу счетов консолидации</span><span class="sxs-lookup"><span data-stu-id="191b5-111">Add accounts to consolidation account group</span></span>
1. <span data-ttu-id="191b5-112">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="191b5-112">Close the page.</span></span>
2. <span data-ttu-id="191b5-113">Перейдите в раздел "Главная книга" > "План счетов" > "Счета" > "Дополнительные счета консолидации".</span><span class="sxs-lookup"><span data-stu-id="191b5-113">Go to General ledger > Chart of accounts > Accounts > Additional consolidation accounts.</span></span>
3. <span data-ttu-id="191b5-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="191b5-114">Click New.</span></span>
4. <span data-ttu-id="191b5-115">В поле "Счет ГК" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="191b5-115">In the Main account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="191b5-116">В списке щелкните счет ГК, который вы хотите сопоставить.</span><span class="sxs-lookup"><span data-stu-id="191b5-116">In the list, click the main account that you want to map.</span></span>
6. <span data-ttu-id="191b5-117">В поле "Группы счетов консолидации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="191b5-117">In the Consolidation account group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="191b5-118">В списке щелкните группу счетов консолидации.</span><span class="sxs-lookup"><span data-stu-id="191b5-118">In the list, click the consolidation account group.</span></span>
8. <span data-ttu-id="191b5-119">В поле "Счет консолидации" введите значение.</span><span class="sxs-lookup"><span data-stu-id="191b5-119">In the Consolidation account field, type a value.</span></span>
9. <span data-ttu-id="191b5-120">В поле "Имя счета консолидации" введите значение.</span><span class="sxs-lookup"><span data-stu-id="191b5-120">In the Consolidation account name field, type a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]