---
title: Создание налогового платежа
description: Задание сопоставления и разноски налога сопоставит налоговые сальдо в налоговых счетах и корреспондирует их со счетом сопоставления налогов за определенный период.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d72c88d6ba851e96ca07b896630549690e9396
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "321762"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="435d6-103">Создание налогового платежа</span><span class="sxs-lookup"><span data-stu-id="435d6-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="435d6-104">Задание сопоставления и разноски налога сопоставит налоговые сальдо в налоговых счетах и корреспондирует их со счетом сопоставления налогов за определенный период.</span><span class="sxs-lookup"><span data-stu-id="435d6-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="435d6-105">Перейдите в раздел "Налог" > "Объявления" > "Налог" > "Сопоставить и разнести налог".</span><span class="sxs-lookup"><span data-stu-id="435d6-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="435d6-106">В поле "Период сопоставления" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="435d6-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="435d6-107">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="435d6-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="435d6-108">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="435d6-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="435d6-109">Если параметр "Включать коррекции" не выбран на странице "Параметры главной книги", сопоставление может быть обработано для разных версий.</span><span class="sxs-lookup"><span data-stu-id="435d6-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="435d6-110">Оригинал — это первое сопоставление за интервал периода и может быть обработано только один раз за интервал периода.</span><span class="sxs-lookup"><span data-stu-id="435d6-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="435d6-111">Последние корректировки сопоставят налоговые проводки, которые были разнесены после создания исходной версии.</span><span class="sxs-lookup"><span data-stu-id="435d6-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="435d6-112">В поле "Дата проводки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="435d6-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="435d6-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="435d6-113">Click OK.</span></span>

