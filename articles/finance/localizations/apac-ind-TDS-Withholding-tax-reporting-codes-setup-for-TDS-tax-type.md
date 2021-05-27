---
title: Настройка кодов налоговой отчетности по подоходному налогу для налогов типа TDS
description: Коды налоговой отчетности подоходного налога используются для создания отчетов по формам 26Q и 27Q для налога, вычитаемого в источнике (TDS). В этой теме объясняется, как настроить шаги кодов налоговой отчетности подоходного налога, чтобы можно было настроить коды налоговой отчетности TDS.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023548"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="9e571-104">Настройка кодов налоговой отчетности по подоходному налогу для налогов типа TDS</span><span class="sxs-lookup"><span data-stu-id="9e571-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e571-105">Коды налоговой отчетности подоходного налога используются для создания отчетов по формам 26Q и 27Q для налога, вычитаемого в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="9e571-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="9e571-106">В этой теме объясняется, как настроить шаги кодов налоговой отчетности подоходного налога, чтобы можно было настроить коды налоговой отчетности TDS.</span><span class="sxs-lookup"><span data-stu-id="9e571-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="9e571-107">Перейдите **Налог \> Настройка \> Подоходный налог \> Коды налоговой отчетности подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="9e571-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="9e571-108">[![Страница "Коды налоговой отчетности подоходного налога"](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="9e571-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="9e571-109">В поле **Тип налога** выберите **TDS**, чтобы задать коды налоговой отчетности по подоходному налогу для типа налога TDS.</span><span class="sxs-lookup"><span data-stu-id="9e571-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="9e571-110">В поле **Компонент подоходного налога** выберите компонент TDS, для которого определяется код налоговой отчетности подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="9e571-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="9e571-111">В поле **Группа компонентов подоходного налога** отображается группа компонентов TDS, которая была задана для определяемого компонента TDS.</span><span class="sxs-lookup"><span data-stu-id="9e571-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="9e571-112">В поле **Код раздела** на экспресс-вкладке **Общие** отображается код раздела, прикрепленный к группе компонентов TDS.</span><span class="sxs-lookup"><span data-stu-id="9e571-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="9e571-113">На экспресс-вкладке **Общее** в поле **Код налоговой отчетности** выберите код налоговой отчетности TDS:</span><span class="sxs-lookup"><span data-stu-id="9e571-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="9e571-114">TDS</span><span class="sxs-lookup"><span data-stu-id="9e571-114">TDS</span></span>
    - <span data-ttu-id="9e571-115">TCS</span><span class="sxs-lookup"><span data-stu-id="9e571-115">TCS</span></span>
    - <span data-ttu-id="9e571-116">Доплата</span><span class="sxs-lookup"><span data-stu-id="9e571-116">Surcharge</span></span>
    - <span data-ttu-id="9e571-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="9e571-117">PE\_Cess</span></span>
    - <span data-ttu-id="9e571-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="9e571-118">SHE\_Cess</span></span>

5. <span data-ttu-id="9e571-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9e571-119">Close the page.</span></span>
