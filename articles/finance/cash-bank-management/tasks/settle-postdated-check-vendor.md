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
ms.openlocfilehash: ee66bdb93d1252486efc7be25adeb6ee7cc6ce05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447264"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="32317-103">Сопоставление датированного будущим числом чека для поставщика</span><span class="sxs-lookup"><span data-stu-id="32317-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32317-104">Сопоставьте датированный будущим числом чек, выдаваемый поставщику, когда банк осуществляет клиринг проводки по чеку, после того как чек стал просроченным и был подвергнут клирингу в банке.</span><span class="sxs-lookup"><span data-stu-id="32317-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="32317-105">Перед тем как начинать эту процедуру, необходимо выполнить следующие процедуры.</span><span class="sxs-lookup"><span data-stu-id="32317-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="32317-106">Настройка датированных будущим числом чеков</span><span class="sxs-lookup"><span data-stu-id="32317-106">Set up postdated checks</span></span>

2) <span data-ttu-id="32317-107">Регистрация и разноска датированного будущим числом чека для поставщика</span><span class="sxs-lookup"><span data-stu-id="32317-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="32317-108">Роль для выполнения этой процедуры — казначей.</span><span class="sxs-lookup"><span data-stu-id="32317-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="32317-109">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="32317-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="32317-110">Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Чеки для поставщика, датированные будущим числом".</span><span class="sxs-lookup"><span data-stu-id="32317-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="32317-111">Щелкните "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="32317-111">Click Settle.</span></span>
3. <span data-ttu-id="32317-112">Щелкните "Сопоставление записей клиринга".</span><span class="sxs-lookup"><span data-stu-id="32317-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="32317-113">Сопоставьте счет поставщика для проводки чека.</span><span class="sxs-lookup"><span data-stu-id="32317-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="32317-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="32317-114">Close the page.</span></span>
5. <span data-ttu-id="32317-115">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="32317-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="32317-116">В поле "Показать" выберите "Все".</span><span class="sxs-lookup"><span data-stu-id="32317-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="32317-117">Установите или снимите флажок "Показать только созданное пользователем".</span><span class="sxs-lookup"><span data-stu-id="32317-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="32317-118">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="32317-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="32317-119">Выберите Строки.</span><span class="sxs-lookup"><span data-stu-id="32317-119">Click Lines.</span></span>
10. <span data-ttu-id="32317-120">Щелкните "Операция".</span><span class="sxs-lookup"><span data-stu-id="32317-120">Click Voucher.</span></span>
11. <span data-ttu-id="32317-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="32317-121">Close the page.</span></span>

