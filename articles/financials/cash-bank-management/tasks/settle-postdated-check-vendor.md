---
title: Сопоставление датированного будущим числом чека для поставщика
description: Сопоставьте датированный будущим числом чек, выдаваемый поставщику, когда банк осуществляет клиринг проводки по чеку, после того как чек стал просроченным и был подвергнут клирингу в банке.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d935ec24d97ca76a088cbe41d57c12c6e8a6689
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841833"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="76822-103">Сопоставление датированного будущим числом чека для поставщика</span><span class="sxs-lookup"><span data-stu-id="76822-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76822-104">Сопоставьте датированный будущим числом чек, выдаваемый поставщику, когда банк осуществляет клиринг проводки по чеку, после того как чек стал просроченным и был подвергнут клирингу в банке.</span><span class="sxs-lookup"><span data-stu-id="76822-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="76822-105">Перед тем как начинать эту процедуру, необходимо выполнить следующие процедуры.</span><span class="sxs-lookup"><span data-stu-id="76822-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="76822-106">Настройка датированных будущим числом чеков</span><span class="sxs-lookup"><span data-stu-id="76822-106">Set up postdated checks</span></span>

2) <span data-ttu-id="76822-107">Регистрация и разноска датированного будущим числом чека для поставщика</span><span class="sxs-lookup"><span data-stu-id="76822-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="76822-108">Роль для выполнения этой процедуры — казначей.</span><span class="sxs-lookup"><span data-stu-id="76822-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="76822-109">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="76822-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="76822-110">Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Чеки для поставщика, датированные будущим числом".</span><span class="sxs-lookup"><span data-stu-id="76822-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="76822-111">Щелкните "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="76822-111">Click Settle.</span></span>
3. <span data-ttu-id="76822-112">Щелкните "Сопоставление записей клиринга".</span><span class="sxs-lookup"><span data-stu-id="76822-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="76822-113">Сопоставьте счет поставщика для проводки чека.</span><span class="sxs-lookup"><span data-stu-id="76822-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="76822-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="76822-114">Close the page.</span></span>
5. <span data-ttu-id="76822-115">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="76822-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="76822-116">В поле "Показать" выберите "Все".</span><span class="sxs-lookup"><span data-stu-id="76822-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="76822-117">Установите или снимите флажок "Показать только созданное пользователем".</span><span class="sxs-lookup"><span data-stu-id="76822-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="76822-118">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="76822-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="76822-119">Выберите Строки.</span><span class="sxs-lookup"><span data-stu-id="76822-119">Click Lines.</span></span>
10. <span data-ttu-id="76822-120">Щелкните "Операция".</span><span class="sxs-lookup"><span data-stu-id="76822-120">Click Voucher.</span></span>
11. <span data-ttu-id="76822-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="76822-121">Close the page.</span></span>

