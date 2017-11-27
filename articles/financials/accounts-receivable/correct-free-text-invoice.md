---
title: "Корректировка накладной с произвольным текстом"
description: "Эта статья описывает порядок коррекции накладной с произвольным текстом, которая была разнесена, и повторно выпуск ее как исправленной накладной."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cbae4c444db29a8dc7f3040aa78e45c0da092efd
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="aeb74-103">Корректировка накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="aeb74-103">Correct a free text invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="aeb74-104">Эта статья описывает порядок коррекции накладной с произвольным текстом, которая была разнесена, и повторно выпуск ее как исправленной накладной.</span><span class="sxs-lookup"><span data-stu-id="aeb74-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="aeb74-105">Чтобы исправить накладную с произвольным текстом, которая уже была разнесена, откройте разнесенную накладную с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="aeb74-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="aeb74-106">На странице **Накладная** выберите **Отмена**, затем выберите **Исправить накладную**.</span><span class="sxs-lookup"><span data-stu-id="aeb74-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="aeb74-107">Выберите код причины, добавьте комментарии и выберите дату для новой исправленной накладной.</span><span class="sxs-lookup"><span data-stu-id="aeb74-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="aeb74-108">Исправленную накладную можно изменить и разнести.</span><span class="sxs-lookup"><span data-stu-id="aeb74-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="aeb74-109">При разноске исправленной накладной отменяющая накладная создается для суммы кредита, равной сумме исходной накладной.</span><span class="sxs-lookup"><span data-stu-id="aeb74-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="aeb74-110">Таким образом, объединенное сальдо исходной и отменяющей накладной равно 0.</span><span class="sxs-lookup"><span data-stu-id="aeb74-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="aeb74-111">Отменяющая накладная сопоставляется с исходной накладной.</span><span class="sxs-lookup"><span data-stu-id="aeb74-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="aeb74-112">После разноски исправленной накладной будет доступно три накладных:</span><span class="sxs-lookup"><span data-stu-id="aeb74-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="aeb74-113">**Исходная накладная** — накладная, включающая сведения, которые исправляются.</span><span class="sxs-lookup"><span data-stu-id="aeb74-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="aeb74-114">**Отменяющая накладная** — создаваемая системой накладная, служащая для отмены исправляемой накладной.</span><span class="sxs-lookup"><span data-stu-id="aeb74-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="aeb74-115">**Исправленная накладная** — накладная, которая содержит исправленные данные.</span><span class="sxs-lookup"><span data-stu-id="aeb74-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="aeb74-116">Вы можете определить отменяющую и корректирующую накладные двумя способами:</span><span class="sxs-lookup"><span data-stu-id="aeb74-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="aeb74-117">На странице **Все накладные с произвольным текстом** есть столбец **Корректировка**, где можно просмотреть, какие накладные являются отменяющими, а какие корректирующими.</span><span class="sxs-lookup"><span data-stu-id="aeb74-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="aeb74-118">В заголовке накладной с произвольным текстом отображается статус **Отменяющая накладная "\[номер накладной\]"** или **Исправленная накладная "\[номер накладной\]"**.</span><span class="sxs-lookup"><span data-stu-id="aeb74-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="aeb74-119">Эта функция доступна, только если выбран конфигурационный ключ **Исправление накладной с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="aeb74-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span>




