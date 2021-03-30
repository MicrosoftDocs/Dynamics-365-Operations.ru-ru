---
title: Настройка глобального подоходного налога
description: В этом разделе перечислены этапы настройки глобального подоходного налога для продаж и покупок.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 00c472e90f4926c52ffe9b19661e68cbfa6bd493
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204841"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="5ae36-103">Настройка глобального подоходного налога</span><span class="sxs-lookup"><span data-stu-id="5ae36-103">Set up global withholding tax</span></span>

<span data-ttu-id="5ae36-104">В этом разделе перечислены этапы настройки глобального подоходного налога для продаж и покупок.</span><span class="sxs-lookup"><span data-stu-id="5ae36-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="5ae36-105">Настройте налоговые органы для подоходного налога на странице **Налоговые органы по подоходному налогу**.</span><span class="sxs-lookup"><span data-stu-id="5ae36-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="5ae36-106">Настройте периоды сопоставления налогов на странице **Периоды сопоставления подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="5ae36-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="5ae36-107">Настройте группы разноски ГК для удержания налога на странице **Подоходный налог > Группа разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="5ae36-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="5ae36-108">Счету **Подоходный налог** будет назначен счет ГК с параметером **Тип разноски** со значением подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="5ae36-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="5ae36-109">Счету **Корреспондирующий подоходного налога** также будет назначен счет ГК с параметером **Тип разноски** со значением "Корреспондирующий подоходного налога".</span><span class="sxs-lookup"><span data-stu-id="5ae36-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="5ae36-110">Перейдите в раздел **Главная книга > План счетов > Счета > Счета ГК**, настройте **Тип разноски** во вложенной форме **Проверка разноски** для счетов ГК.</span><span class="sxs-lookup"><span data-stu-id="5ae36-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="5ae36-111">Настройте коды подоходного налога на странице **Коды подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="5ae36-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="5ae36-112">Настройте группы подоходного налога на странице **Группы подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="5ae36-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="5ae36-113">Настройте типы выручки подоходного налога на странице **Типы** **выручки по подоходному налогу**.</span><span class="sxs-lookup"><span data-stu-id="5ae36-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="5ae36-114">Настройте группы подоходного налога на странице **Группы подоходного налога для номенклатуры** для номенклатуры или услуги.</span><span class="sxs-lookup"><span data-stu-id="5ae36-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="5ae36-115">Настройте параметр **Минимальная сумма накладной** на странице **Параметры главной книги > Подоходный налог**.</span><span class="sxs-lookup"><span data-stu-id="5ae36-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]