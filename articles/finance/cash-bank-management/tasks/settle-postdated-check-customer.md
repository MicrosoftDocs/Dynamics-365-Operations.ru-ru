---
title: Сопоставление датированного будущим числом чека от клиента
description: Можно сопоставить чек, датированный задним числом, после того как банком был выполнен клиринг чека.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f714e41f47a31bce16424de18878d2f5acb5028d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834557"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="29738-103">Сопоставление датированного будущим числом чека от клиента</span><span class="sxs-lookup"><span data-stu-id="29738-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29738-104">Можно сопоставить чек, датированный задним числом, после того как банком был выполнен клиринг чека.</span><span class="sxs-lookup"><span data-stu-id="29738-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="29738-105">Эта финансовая проводка также приведет к очистке проводки на промежуточный счет для чека, датированного задним числом.</span><span class="sxs-lookup"><span data-stu-id="29738-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="29738-106">Перед тем как начинать эту задачу, необходимо выполнить следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="29738-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="29738-107">Настройка датированных будущим числом чеков</span><span class="sxs-lookup"><span data-stu-id="29738-107">Set up postdated checks</span></span>

2) <span data-ttu-id="29738-108">Регистрация и разноска датированного будущим числом чека для клиента</span><span class="sxs-lookup"><span data-stu-id="29738-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="29738-109">Роль для выполнения этого руководства по задачам — казначей.</span><span class="sxs-lookup"><span data-stu-id="29738-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="29738-110">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="29738-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="29738-111">Перейдите в раздел "Кредит и коллекции" > "Запросы и отчеты" > "Платежи" > "Чеки клиента, датированные будущим числом".</span><span class="sxs-lookup"><span data-stu-id="29738-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="29738-112">Щелкните "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="29738-112">Click Settle.</span></span>
3. <span data-ttu-id="29738-113">Щелкните "Сопоставление записей клиринга".</span><span class="sxs-lookup"><span data-stu-id="29738-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="29738-114">Сопоставьте счет клиента для проводки чека.</span><span class="sxs-lookup"><span data-stu-id="29738-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="29738-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="29738-115">Close the page.</span></span>
5. <span data-ttu-id="29738-116">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="29738-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="29738-117">В поле "Показать" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="29738-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="29738-118">Установите или снимите флажок "Показать только созданное пользователем".</span><span class="sxs-lookup"><span data-stu-id="29738-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="29738-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="29738-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="29738-120">Выберите Строки.</span><span class="sxs-lookup"><span data-stu-id="29738-120">Click Lines.</span></span>
10. <span data-ttu-id="29738-121">Щелкните "Операция".</span><span class="sxs-lookup"><span data-stu-id="29738-121">Click Voucher.</span></span>
11. <span data-ttu-id="29738-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="29738-122">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]