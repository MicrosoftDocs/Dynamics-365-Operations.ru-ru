---
title: Настройка параметров TDS
description: В этой теме объясняется, как настроить параметры для активации функции налога, удерживаемого в источнике (TDS), в указанных проводках. Это обязательный шаг для использования налога, удержанного в источнике (TDS).
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023536"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="5d46a-104">Настройка параметров TDS</span><span class="sxs-lookup"><span data-stu-id="5d46a-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d46a-105">В этой теме объясняется, как настроить параметры для активации функции налога, удерживаемого в источнике (TDS), в указанных проводках.</span><span class="sxs-lookup"><span data-stu-id="5d46a-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="5d46a-106">Это обязательный шаг для использования налога, удержанного в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="5d46a-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="5d46a-107">Перейдите в раздел **Главная книга \> Настройка главной книги \> Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="5d46a-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="5d46a-108">На вкладке **Прямые налоги** в поле **Налог, удерживаемый в источнике**, установите для параметра **Активировать TDS** значение **Да**, чтобы активировать функции TDS, а также используемые для него страницы и поля.</span><span class="sxs-lookup"><span data-stu-id="5d46a-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="5d46a-109">Установите для параметра **Накладная** значение **Да**, чтобы активировать поля, используемые для расчета и вычета TDS на уровне накладных.</span><span class="sxs-lookup"><span data-stu-id="5d46a-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="5d46a-110">Установите для параметра **Платеж** значение **Да**, чтобы активировать поля, используемые для расчета и вычета TDS на уровне платежей.</span><span class="sxs-lookup"><span data-stu-id="5d46a-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="5d46a-111">[![Вкладка "Прямые налоги"](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="5d46a-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="5d46a-112">На вкладке **Номерные серии** найдите строку, в которой поле **Ссылка** задано как **Платеж подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="5d46a-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="5d46a-113">В поле **Код номерной серии** для строки выберите код номерной серии.</span><span class="sxs-lookup"><span data-stu-id="5d46a-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="5d46a-114">Код номерной серии используется для создания кодов ваучеров для периодического процесса сопоставления TDS.</span><span class="sxs-lookup"><span data-stu-id="5d46a-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5d46a-115">Чтобы выполнить периодическое сопоставление TDS, перейдите **Налог \> Декларации \> Подоходный налог \> Платеж подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="5d46a-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="5d46a-116">[![Вкладка "Номерные серии"](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="5d46a-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="5d46a-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5d46a-117">Close the page.</span></span>
