---
title: Создание транспортной накладной
description: В этом разделе описывается создание транспортной накладной при использовании процессов управления складом.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b001ef8936e7e35db89163683c023211f79b24c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996482"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="b31ad-103">Создание транспортной накладной</span><span class="sxs-lookup"><span data-stu-id="b31ad-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b31ad-104">В этом разделе описывается создание транспортной накладной при использовании процессов управления складом.</span><span class="sxs-lookup"><span data-stu-id="b31ad-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="b31ad-105">Транспортная накладная — юридический документ между компанией, которая отгружает номенклатуры, и перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="b31ad-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="b31ad-106">Документ сопровождает отгруженные номенклатуры и служит как подтверждение получения отгрузки, когда номенклатуры доставляются по месту назначения.</span><span class="sxs-lookup"><span data-stu-id="b31ad-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="b31ad-107">Если вы используете управление складом, существует два способа создания транспортной накладной:</span><span class="sxs-lookup"><span data-stu-id="b31ad-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="b31ad-108">Создайте отчет вручную, используя страницу **Транспортная накладная**.</span><span class="sxs-lookup"><span data-stu-id="b31ad-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="b31ad-109">Создайте отчет в разделе **Рабочее место планирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="b31ad-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="b31ad-110">При создании транспортной накладной в разделе **Рабочее место планирования загрузки** статус загрузки должен быть **Отгружено.**</span><span class="sxs-lookup"><span data-stu-id="b31ad-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="b31ad-111">Если имеется более одной отгрузки в загрузке, транспортная накладная создается для каждой отгрузки.</span><span class="sxs-lookup"><span data-stu-id="b31ad-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="b31ad-112">После создания транспортной накладной можно вносить в нее изменения на странице **Транспортная накладная**.</span><span class="sxs-lookup"><span data-stu-id="b31ad-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="b31ad-113">Сводная транспортная накладная</span><span class="sxs-lookup"><span data-stu-id="b31ad-113">Master bill of lading</span></span>
<span data-ttu-id="b31ad-114">При наличии нескольких отгрузок в загрузке можно создать сводную транспортную накладную.</span><span class="sxs-lookup"><span data-stu-id="b31ad-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="b31ad-115">Она имеет тот же макет и сведения как и транспортная накладная, но содержит сводное содержимое по всем отгрузкам.</span><span class="sxs-lookup"><span data-stu-id="b31ad-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="b31ad-116">Если для параметра **Создание сводной транспортной накладной при наличии нескольких отгрузок для загрузки** задано значение **Да** на странице **Параметры управления транспортировкой**, сводная транспортная накладная создается автоматически при создании транспортной накладной в разделе **Рабочее место планирования загрузки** и имеется несколько отгрузок.</span><span class="sxs-lookup"><span data-stu-id="b31ad-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="b31ad-117">Можно также получить список транспортных накладных, щелкнув **Связанные сведения** &gt; **Транспортная накладная**.</span><span class="sxs-lookup"><span data-stu-id="b31ad-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="b31ad-118">При создании транспортной накладной вручную можно создать сводную транспортную накладную на странице **Транспортная накладная**.</span><span class="sxs-lookup"><span data-stu-id="b31ad-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>



