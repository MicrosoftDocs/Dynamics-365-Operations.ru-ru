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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e46b419ab613425ae2d758f80105ac94f1ec5cc2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565980"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="9b506-103">Сопоставление датированного будущим числом чека для поставщика</span><span class="sxs-lookup"><span data-stu-id="9b506-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b506-104">Сопоставьте датированный будущим числом чек, выдаваемый поставщику, когда банк осуществляет клиринг проводки по чеку, после того как чек стал просроченным и был подвергнут клирингу в банке.</span><span class="sxs-lookup"><span data-stu-id="9b506-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="9b506-105">Перед тем как начинать эту процедуру, необходимо выполнить следующие процедуры.</span><span class="sxs-lookup"><span data-stu-id="9b506-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="9b506-106">Настройка датированных будущим числом чеков</span><span class="sxs-lookup"><span data-stu-id="9b506-106">Set up postdated checks</span></span>

2) <span data-ttu-id="9b506-107">Регистрация и разноска датированного будущим числом чека для поставщика</span><span class="sxs-lookup"><span data-stu-id="9b506-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="9b506-108">Роль для выполнения этой процедуры — казначей.</span><span class="sxs-lookup"><span data-stu-id="9b506-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="9b506-109">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="9b506-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="9b506-110">Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Чеки для поставщика, датированные будущим числом".</span><span class="sxs-lookup"><span data-stu-id="9b506-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="9b506-111">Щелкните "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="9b506-111">Click Settle.</span></span>
3. <span data-ttu-id="9b506-112">Щелкните "Сопоставление записей клиринга".</span><span class="sxs-lookup"><span data-stu-id="9b506-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="9b506-113">Сопоставьте счет поставщика для проводки чека.</span><span class="sxs-lookup"><span data-stu-id="9b506-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="9b506-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9b506-114">Close the page.</span></span>
5. <span data-ttu-id="9b506-115">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="9b506-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="9b506-116">В поле "Показать" выберите "Все".</span><span class="sxs-lookup"><span data-stu-id="9b506-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="9b506-117">Установите или снимите флажок "Показать только созданное пользователем".</span><span class="sxs-lookup"><span data-stu-id="9b506-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="9b506-118">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9b506-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9b506-119">Выберите Строки.</span><span class="sxs-lookup"><span data-stu-id="9b506-119">Click Lines.</span></span>
10. <span data-ttu-id="9b506-120">Щелкните "Операция".</span><span class="sxs-lookup"><span data-stu-id="9b506-120">Click Voucher.</span></span>
11. <span data-ttu-id="9b506-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9b506-121">Close the page.</span></span>

