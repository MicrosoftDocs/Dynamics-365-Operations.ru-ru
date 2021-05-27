---
title: Запишите номера сертификатов на предоставление налоговых льгот TDS
description: В этой теме объясняется, как записать номера сертификатов на предоставление налоговых льгот для налога, удержанного в источнике (TDS), выданные поставщикам.
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
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023526"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="67205-103">Запишите номера сертификатов на предоставление налоговых льгот TDS</span><span class="sxs-lookup"><span data-stu-id="67205-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67205-104">В этой теме объясняется, как записать номера сертификатов на предоставление налоговых льгот для налога, удержанного в источнике (TDS), выданные поставщикам.</span><span class="sxs-lookup"><span data-stu-id="67205-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="67205-105">Перейдите в раздел **Налог \> Косвенные налоги \> Подоходный налог \> Концессии подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="67205-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="67205-106">В поле **Тип налога** выберите **TDS** для записи сертификатов на предоставление налоговых льгот для типа налога TDS.</span><span class="sxs-lookup"><span data-stu-id="67205-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="67205-107">На вкладке **Обзор** нажмите сочетание клавиш **ALT+N**, чтобы создать строку.</span><span class="sxs-lookup"><span data-stu-id="67205-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="67205-108">[![Заголовок новой строки](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="67205-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="67205-109">В поле **Код подоходного налога** выберите налоговый код TDS, для которого выпущены сертификаты на предоставление налоговых льгот для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="67205-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="67205-110">В поле **Имя подоходного налога** показано имя кода налога TDS.</span><span class="sxs-lookup"><span data-stu-id="67205-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="67205-111">В полях **Начальная дата** и **Конечная дата** укажите период действия для сертификата на предоставление налоговых льгот, который использует налоговый код TDS для расчета TDS для поставщика на основе концессии.</span><span class="sxs-lookup"><span data-stu-id="67205-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="67205-112">В поле **Примечания** введите любые замечания.</span><span class="sxs-lookup"><span data-stu-id="67205-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="67205-113">В поле **Раздел** введите код юридического раздела, к которому относится сертификат на предоставление налоговых льгот TDS.</span><span class="sxs-lookup"><span data-stu-id="67205-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="67205-114">Если кодом раздела является 197, значение "A" появляется в обоих полях "Причина для невычета/меньшего вычета" в форме формы 26Q и в столбце "Причина невычета/уменьшение вычета/валовое исчисление (если имеется)" в форме 27Q.</span><span class="sxs-lookup"><span data-stu-id="67205-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="67205-115">Если код раздела — 197A, в обоих местах появится значение "B".</span><span class="sxs-lookup"><span data-stu-id="67205-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="67205-116">Откройте экспресс-вкладку **Сертификат**, чтобы записать номера сертификатов на предоставление налоговых льгот TDS для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="67205-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="67205-117">В поле **Счет поставщика** выберите номер счета поставщика, для которого выпускается сертификат на предоставление налоговых льгот TDS.</span><span class="sxs-lookup"><span data-stu-id="67205-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="67205-118">В полях **Начальная дата** и **Конечная дата** укажите период действия для сертификата на предоставление налоговых льгот TDS.</span><span class="sxs-lookup"><span data-stu-id="67205-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="67205-119">Расчет TDS на основе концессий основан на периоде создания сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="67205-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="67205-120">В поле **Сертификат** введите номер сертификата на предоставление налоговых льгот TDS.</span><span class="sxs-lookup"><span data-stu-id="67205-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="67205-121">[![Экспресс-вкладка сертификатов](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="67205-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="67205-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="67205-122">Close the page.</span></span>
