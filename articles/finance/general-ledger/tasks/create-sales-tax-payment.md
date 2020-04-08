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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99059a8e5d6f4bf125266ad2a98cb73751529e6b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139936"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="31982-103">Создание налогового платежа</span><span class="sxs-lookup"><span data-stu-id="31982-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31982-104">Задание сопоставления и разноски налога сопоставит налоговые сальдо в налоговых счетах и корреспондирует их со счетом сопоставления налогов за определенный период.</span><span class="sxs-lookup"><span data-stu-id="31982-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="31982-105">Перейдите в раздел "Налог" > "Объявления" > "Налог" > "Сопоставить и разнести налог".</span><span class="sxs-lookup"><span data-stu-id="31982-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="31982-106">В поле "Период сопоставления" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="31982-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="31982-107">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="31982-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="31982-108">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="31982-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="31982-109">Если параметр "Включать коррекции" не выбран на странице "Параметры главной книги", сопоставление может быть обработано для разных версий.</span><span class="sxs-lookup"><span data-stu-id="31982-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="31982-110">Оригинал — это первое сопоставление за интервал периода и может быть обработано только один раз за интервал периода.</span><span class="sxs-lookup"><span data-stu-id="31982-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="31982-111">Последние корректировки сопоставят налоговые проводки, которые были разнесены после создания исходной версии.</span><span class="sxs-lookup"><span data-stu-id="31982-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="31982-112">В поле "Дата проводки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="31982-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="31982-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="31982-113">Click OK.</span></span>

