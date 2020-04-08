---
title: Настройка подоходного налога
description: В этом разделе описывается, как настроить подоходный налог.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 135cca434a1689bf22ee468894dcf8746071e7ca
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144705"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="395c4-103">Настройка подоходного налога</span><span class="sxs-lookup"><span data-stu-id="395c4-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="395c4-104">В этом разделе описывается, как настроить подоходный налог.</span><span class="sxs-lookup"><span data-stu-id="395c4-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="395c4-105">*Подоходный налог* — это налог на поставщиков, который не приводит к созданию налоговых проводок.</span><span class="sxs-lookup"><span data-stu-id="395c4-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="395c4-106">Подоходный налог, рассчитываемый по платежам поставщиков, является задолженностью.</span><span class="sxs-lookup"><span data-stu-id="395c4-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="395c4-107">Поэтому действительными счетами для разноски подоходного налога являются только балансовые счета или счета задолженности.</span><span class="sxs-lookup"><span data-stu-id="395c4-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="395c4-108">В этом руководстве по задаче показано, как настроить подоходный налог.</span><span class="sxs-lookup"><span data-stu-id="395c4-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="395c4-109">Перейдите к **Область перехода> Мдули > > Налог > Косвенные налоги > Подоходный налог > Коды подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="395c4-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="395c4-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="395c4-110">Select **New**.</span></span>
3. <span data-ttu-id="395c4-111">В поле **Код подоходного налога** введите значение.</span><span class="sxs-lookup"><span data-stu-id="395c4-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="395c4-112">В поле **Имя подоходного налога** введите имя кода подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="395c4-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="395c4-113">В поле **Счет ГК** выберите счет ГК для разноски налоговых обязательств по подоходному налогу.</span><span class="sxs-lookup"><span data-stu-id="395c4-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="395c4-114">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="395c4-114">Select **Save**.</span></span>
7. <span data-ttu-id="395c4-115">Выберите **Значения** и пометьте требуемую запись в списке.</span><span class="sxs-lookup"><span data-stu-id="395c4-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="395c4-116">В поле **Значение** введите процент, используемый для расчета подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="395c4-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="395c4-117">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="395c4-117">Select **Save**.</span></span>
10. <span data-ttu-id="395c4-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="395c4-118">Close the page.</span></span>
11. <span data-ttu-id="395c4-119">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="395c4-119">Select **Save**.</span></span>
12. <span data-ttu-id="395c4-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="395c4-120">Close the page.</span></span>
13. <span data-ttu-id="395c4-121">Перейдите к **Область перехода> Мдули > > Налог > Косвенные налоги > Подоходный налог > Группы подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="395c4-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="395c4-122">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="395c4-122">Select **New**.</span></span>
15. <span data-ttu-id="395c4-123">В поле **Группа подоходного налога** введите код группы подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="395c4-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="395c4-124">В поле **Описание** введите имя группы подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="395c4-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="395c4-125">В поле **Код подоходного налога** выберите код подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="395c4-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="395c4-126">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="395c4-126">Select **Save**.</span></span>
19. <span data-ttu-id="395c4-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="395c4-127">Close the page.</span></span>

