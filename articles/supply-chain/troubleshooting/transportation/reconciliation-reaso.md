---
title: В целях выверки можно добавить только счет ГК в качестве кредитного счета
description: При настройке причины выверки в модуле управления транспортировкой в качестве кредитного счета можно добавить только счет ГК.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026833"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="94780-103">В целях выверки можно добавить только счет ГК в качестве кредитного счета</span><span class="sxs-lookup"><span data-stu-id="94780-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="94780-104">Номер статьи базы знаний: 4603538</span><span class="sxs-lookup"><span data-stu-id="94780-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="94780-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="94780-105">Symptoms</span></span>

<span data-ttu-id="94780-106">При настройке причины выверки в модуле управления транспортировкой в качестве кредитного счета можно добавить только счет ГК.</span><span class="sxs-lookup"><span data-stu-id="94780-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="94780-107">Нельзя добавить место возникновения затрат или любую другую аналитику в качестве кредитового счета.</span><span class="sxs-lookup"><span data-stu-id="94780-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="94780-108">Однако дебетовый счет позволяет выбрать другие аналитики.</span><span class="sxs-lookup"><span data-stu-id="94780-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="94780-109">Приказ</span><span class="sxs-lookup"><span data-stu-id="94780-109">Resolution</span></span>

<span data-ttu-id="94780-110">Если выверка не выполнена для оплаты поставщику, но для кредитования определенного счета ГК, система не позволяет выбрать финансовую аналитику для кредитового счета при настройке причины выверки.</span><span class="sxs-lookup"><span data-stu-id="94780-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="94780-111">Если для структуры счета требуется конкретное значение финансовой аналитики для кредитного счета ГК, журнал итогового поставщика нельзя разнести автоматически, поскольку значение финансовой аналитики отсутствует.</span><span class="sxs-lookup"><span data-stu-id="94780-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="94780-112">Таким образом, необходимо сначала указать счет кредита вручную, используя страницу **Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="94780-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="94780-113">Поскольку значение аналитики требуется для счета кредита, разноска журнала накладных поставщика автоматически невозможна.</span><span class="sxs-lookup"><span data-stu-id="94780-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="94780-114">Необходимо вручную разнести его после добавления значения аналитики к счету ГК для строки кредита.</span><span class="sxs-lookup"><span data-stu-id="94780-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
