--- 
title: "Создание налогового платежа"
description: "Задание сопоставления и разноски налога сопоставит налоговые сальдо в налоговых счетах и корреспондирует их со счетом сопоставления налогов за определенный период."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b0d72c88d6ba851e96ca07b896630549690e9396
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="9e9ed-103">Создание налогового платежа</span><span class="sxs-lookup"><span data-stu-id="9e9ed-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e9ed-104">Задание сопоставления и разноски налога сопоставит налоговые сальдо в налоговых счетах и корреспондирует их со счетом сопоставления налогов за определенный период.</span><span class="sxs-lookup"><span data-stu-id="9e9ed-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="9e9ed-105">Перейдите в раздел "Налог" > "Объявления" > "Налог" > "Сопоставить и разнести налог".</span><span class="sxs-lookup"><span data-stu-id="9e9ed-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="9e9ed-106">В поле "Период сопоставления" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9e9ed-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9e9ed-107">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9e9ed-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9e9ed-108">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="9e9ed-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="9e9ed-109">Если параметр "Включать коррекции" не выбран на странице "Параметры главной книги", сопоставление может быть обработано для разных версий.</span><span class="sxs-lookup"><span data-stu-id="9e9ed-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="9e9ed-110">Оригинал — это первое сопоставление за интервал периода и может быть обработано только один раз за интервал периода.</span><span class="sxs-lookup"><span data-stu-id="9e9ed-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="9e9ed-111">Последние корректировки сопоставят налоговые проводки, которые были разнесены после создания исходной версии.</span><span class="sxs-lookup"><span data-stu-id="9e9ed-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="9e9ed-112">В поле "Дата проводки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="9e9ed-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="9e9ed-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9e9ed-113">Click OK.</span></span>


