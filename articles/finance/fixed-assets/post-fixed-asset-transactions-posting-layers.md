---
title: Разноска проводок ОС по слоям разноски
description: Эта статья содержит обзор функции слоя разноски для проводок основных средств.
author: moaamer
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d1c66df39c9712a5d4d26ba4eaa1ce079719c31
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833002"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="d9832-103">Разноска проводок ОС по слоям разноски</span><span class="sxs-lookup"><span data-stu-id="d9832-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9832-104">Эта статья содержит обзор функции слоя разноски для проводок основных средств.</span><span class="sxs-lookup"><span data-stu-id="d9832-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="d9832-105">Основные средства часто амортизируются различными способами для различных целей.</span><span class="sxs-lookup"><span data-stu-id="d9832-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="d9832-106">Амортизация для целей налогообложения рассчитывается с использованием текущего принципа налогообложения, чтобы достигнуть самой высокой возможной амортизации перед выплатой налогов, но амортизация для целей отчетности вычисляется в соответствии с законами и стандартами учета.</span><span class="sxs-lookup"><span data-stu-id="d9832-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="d9832-107">Различные виды амортизации вычисляются и записываются отдельно в слоях разноски.</span><span class="sxs-lookup"><span data-stu-id="d9832-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="d9832-108">Каждая книга, которая присоединяется к основным средствам, настраивается для определенного слоя разноски, имеющего общее задание на амортизацию.</span><span class="sxs-lookup"><span data-stu-id="d9832-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="d9832-109">Предусмотрено десять слоев разноски: Текущий, Операции, Налоги и семь настраиваемых слоев.</span><span class="sxs-lookup"><span data-stu-id="d9832-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="d9832-110">Можно также отключить разноску в главную книгу для этой книги, установив в поле Разносить в главную книгу значение Нет.</span><span class="sxs-lookup"><span data-stu-id="d9832-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="d9832-111">В поле Слой разноски затем автоматически задается значение Нет.</span><span class="sxs-lookup"><span data-stu-id="d9832-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="d9832-112">Обычно книги, которые не разносятся в главную книгу, используются для целей налоговой отчетности.</span><span class="sxs-lookup"><span data-stu-id="d9832-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="d9832-113">Такой подход дает дополнительную гибкость для удаления исторических проводок из модели стоимости ОС, поскольку они не были зафиксированы в главной книге.</span><span class="sxs-lookup"><span data-stu-id="d9832-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="d9832-114">Журналы основных средств определяются с помощью страницы Наименования журналов по пути Главная книга > Настройка журнала > Наименования журналов.</span><span class="sxs-lookup"><span data-stu-id="d9832-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="d9832-115">Каждый журнал, в котором можно разнести амортизацию, определяется своим наименованием журнала только для одного слоя разноски.</span><span class="sxs-lookup"><span data-stu-id="d9832-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="d9832-116">Слой разноски в журнале не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="d9832-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="d9832-117">Это ограничение помогает гарантировать разделение проводок для каждого слоя разноски.</span><span class="sxs-lookup"><span data-stu-id="d9832-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="d9832-118">Для каждого слоя разноски должно быть создано по крайней мере одно имя журнала.</span><span class="sxs-lookup"><span data-stu-id="d9832-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="d9832-119">При использовании книг, которые не разносятся в главную книгу, необходимо также создать журнал, в котором для слоя разноски задано значение "Нет".</span><span class="sxs-lookup"><span data-stu-id="d9832-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="d9832-120">Можно назначить счета ГК для проводок основных средств на странице Профили разноски основных средств.</span><span class="sxs-lookup"><span data-stu-id="d9832-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="d9832-121">Для каждого профиля разноски необходимо выбрать соответствующий тип проводки и книгу, а затем назначить счета учета.</span><span class="sxs-lookup"><span data-stu-id="d9832-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="d9832-122">Настройте запись профиля разноски для каждой книги, которая будет разноситься в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="d9832-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

<span data-ttu-id="d9832-123">Основное средство может быть введено в документы, которые поддерживают только **Текущий** слой разноски, например **Заказ на покупку**, **Накладная поставщика**, **Заказ на продажу** или **Накладная с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="d9832-123">The fixed asset can be entered in documents that only support the **Current** posting layer, like **Purchase order**, **Pending vendor invoice**, **Sales order**, or **Free text invoice**.</span></span> <span data-ttu-id="d9832-124">При выборе кода ОС в любом из этих документов журнал активов фильтруется в книгу с уровнем разноски **Текущий** и заполняется автоматически при разноске, когда система проверяет, что слой разноски основных средств является **Текущим**.</span><span class="sxs-lookup"><span data-stu-id="d9832-124">While selecting a fixed asset ID in any of those documents the asset book is filtered to the book with **Current** posting layer, and will be filled in automatically, during posting when the system validates that the fixed asset posting layer is **Current**.</span></span> <span data-ttu-id="d9832-125">Если эту проверку выполнить невозможно, процесс разноски будет остановлен.</span><span class="sxs-lookup"><span data-stu-id="d9832-125">If that validation can't be completed, the posting process will be stopped.</span></span> 

> [!NOTE] 
> <span data-ttu-id="d9832-126">Используя производные книги, можно разносить проводки одновременно по разным слоям разноски.</span><span class="sxs-lookup"><span data-stu-id="d9832-126">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="d9832-127">Проводки исходной книги создаются в журнале или исходном документе, в котором слой разноски соответствует слою разноски книги.</span><span class="sxs-lookup"><span data-stu-id="d9832-127">The transactions of the primary book are created in a journal or source document where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="d9832-128">В процессе разноски проводки производных книг будут разноситься по соответствующим слоям разноски.</span><span class="sxs-lookup"><span data-stu-id="d9832-128">During posting, the derived book transactions will be posted to the appropriate posting layers.</span></span> 


<span data-ttu-id="d9832-129">Дополнительные сведения см. в разделах [Производные книги](derived-books.md) и [Разноска с производными книгами](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="d9832-129">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]