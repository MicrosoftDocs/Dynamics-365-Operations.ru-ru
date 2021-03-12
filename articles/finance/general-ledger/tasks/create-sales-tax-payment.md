---
title: Создание налогового платежа
description: Процедура задания сопоставления и разноски налога сопоставит налоговые сальдо в налоговых счетах и корреспондирует их со счетом сопоставления налогов за определенный период.
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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b5e3e26e19bd0a9dbf878626328da267b61964f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968712"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="a26d5-103">Создание налогового платежа</span><span class="sxs-lookup"><span data-stu-id="a26d5-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a26d5-104">Процедура задания сопоставления и разноски налога сопоставит налоговые сальдо в налоговых счетах и корреспондирует их со счетом сопоставления налогов за определенный период.</span><span class="sxs-lookup"><span data-stu-id="a26d5-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="a26d5-105">Перейдите в раздел **Налог > Объявления > Налог > Сопоставить и разнести налог**.</span><span class="sxs-lookup"><span data-stu-id="a26d5-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="a26d5-106">В поле **Период сопоставления** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a26d5-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a26d5-107">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a26d5-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a26d5-108">В поле **Дата начала** введите дату.</span><span class="sxs-lookup"><span data-stu-id="a26d5-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="a26d5-109">Если параметр **Включать коррекции** не выбран на странице **Параметры главной книги**, сопоставление может быть обработано для разных версий.</span><span class="sxs-lookup"><span data-stu-id="a26d5-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="a26d5-110">Оригинал — это первое сопоставление за интервал периода и может быть обработано только один раз за интервал периода.</span><span class="sxs-lookup"><span data-stu-id="a26d5-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="a26d5-111">Последние корректировки сопоставят налоговые проводки, которые были разнесены после создания исходной версии.</span><span class="sxs-lookup"><span data-stu-id="a26d5-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="a26d5-112">В поле **Дата проводки** введите дату.</span><span class="sxs-lookup"><span data-stu-id="a26d5-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="a26d5-113">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26d5-113">Click **OK**.</span></span>

