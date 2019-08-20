---
title: Производные книги
description: Эта статья содержит обзор функции производной книги.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a649fdbc355b3382bc6c80be03f8b37a06d5226
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840585"
---
# <a name="derived-books"></a><span data-ttu-id="37fa0-103">Производные книги</span><span class="sxs-lookup"><span data-stu-id="37fa0-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37fa0-104">Эта статья содержит обзор функции производной книги.</span><span class="sxs-lookup"><span data-stu-id="37fa0-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="37fa0-105">Целью производных книг является упрощение разноски проводок книги основных средств, которые планируются для регулярных интервалов.</span><span class="sxs-lookup"><span data-stu-id="37fa0-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="37fa0-106">Одну книгу следует выбрать как основную книгу.</span><span class="sxs-lookup"><span data-stu-id="37fa0-106">You choose one book as the primary book.</span></span> <span data-ttu-id="37fa0-107">Обычно это книга, которая используется для бухгалтерской амортизации.</span><span class="sxs-lookup"><span data-stu-id="37fa0-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="37fa0-108">Затем она присоединяется к другим книгам, настроенным для разноски проводок для интервалов, аналогичных интервалам в первичной книге.</span><span class="sxs-lookup"><span data-stu-id="37fa0-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="37fa0-109">Книги налоговой амортизации часто настраиваются как производные книги.</span><span class="sxs-lookup"><span data-stu-id="37fa0-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="37fa0-110">Проводками, для которых наиболее часто выполняется настройка разноски в производных книгах, являются приобретения, корректировки приобретений и выбытия.</span><span class="sxs-lookup"><span data-stu-id="37fa0-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="37fa0-111">Пример</span><span class="sxs-lookup"><span data-stu-id="37fa0-111">Example</span></span>

<span data-ttu-id="37fa0-112">Книги B и C настраиваются как производные книги для книги A для типа проводки "Приобретения".</span><span class="sxs-lookup"><span data-stu-id="37fa0-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="37fa0-113">В книге A введите проводку приобретения для актива 123 на 1500,00.</span><span class="sxs-lookup"><span data-stu-id="37fa0-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="37fa0-114">Когда выполняется разноска проводки, создается проводка приобретения в активе 123 для книги B и в активе 123 для книги C на 1500,00.</span><span class="sxs-lookup"><span data-stu-id="37fa0-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="37fa0-115">При подготовке проводок этой основной книги к разноске в журнал основных средств также можно просмотреть и изменить проводки производных книг.</span><span class="sxs-lookup"><span data-stu-id="37fa0-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="37fa0-116">При подготовке проводок первичной книги в другом журнале проводки производной стоимости не отображаются.</span><span class="sxs-lookup"><span data-stu-id="37fa0-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="37fa0-117">Однако они разносятся на соответствующие счета и уровни разноски, когда выполняется разноска проводок первичной книги.</span><span class="sxs-lookup"><span data-stu-id="37fa0-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="37fa0-118">Книги, которые настраиваются в проводках разноски на интервалах, отличных от интервалов первичной книги, должны присоединяться к основным средствам в качестве отдельных книг, а не в виде производных книг.</span><span class="sxs-lookup"><span data-stu-id="37fa0-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="37fa0-119">Дополнительные сведения см. в разделе [Разноска с производными книгами](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="37fa0-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>



