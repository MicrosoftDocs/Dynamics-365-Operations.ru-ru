---
title: Настройка налоговых органов по подоходному налогу для налогов типа TDS
description: В этой теме объясняется, как настроить налоговые органы для налога, который удерживается в источнике (TDS).
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023530"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="1f925-103">Настройка налоговых органов по подоходному налогу для налогов типа TDS</span><span class="sxs-lookup"><span data-stu-id="1f925-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f925-104">В этой теме объясняется, как настроить налоговые органы для налога, который удерживается в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="1f925-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="1f925-105">Перейдите в раздел **Налог \> Косвенные налоги \> Налоговые органы по подоходному налогу**.</span><span class="sxs-lookup"><span data-stu-id="1f925-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="1f925-106">[![Страница "Налоговые органы по подоходному налогу"](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="1f925-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="1f925-107">В поле **Тип налога** выберите **TDS**, чтобы настроить налоговые органы по подоходному налогу для типа налога TDS.</span><span class="sxs-lookup"><span data-stu-id="1f925-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="1f925-108">На панели операций выберите **Создать** для создания строки.</span><span class="sxs-lookup"><span data-stu-id="1f925-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="1f925-109">В поле **Налоговый орган по подоходному налогу** введите имя налогового органа TDS.</span><span class="sxs-lookup"><span data-stu-id="1f925-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="1f925-110">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="1f925-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="1f925-111">На экспресс-вкладке **Общее** в поле **Счет поставщика** выберите счет поставщика для налогового органы TDS.</span><span class="sxs-lookup"><span data-stu-id="1f925-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1f925-112">Необходимо определить название банка, в котором будут депонироваться средства, начисленные в качестве задолженности поставщику органа TDS.</span><span class="sxs-lookup"><span data-stu-id="1f925-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="1f925-113">Название банка определяется на странице **Банковские счета** (**Расчеты с поставщиками \> Все поставщики \> Поставщик \> Настройка \> Банковские счета**).</span><span class="sxs-lookup"><span data-stu-id="1f925-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="1f925-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1f925-114">Close the page.</span></span>
