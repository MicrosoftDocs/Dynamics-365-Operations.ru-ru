---
title: Разноска проводок ОС по слоям разноски
description: Эта статья содержит обзор функции слоя разноски для проводок основных средств.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22feb15a1891c57576a5809f4ff3f4d089c6dfa4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "323349"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="94cd3-103">Разноска проводок ОС по слоям разноски</span><span class="sxs-lookup"><span data-stu-id="94cd3-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94cd3-104">Эта статья содержит обзор функции слоя разноски для проводок основных средств.</span><span class="sxs-lookup"><span data-stu-id="94cd3-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="94cd3-105">Основные средства часто амортизируются различными способами для различных целей.</span><span class="sxs-lookup"><span data-stu-id="94cd3-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="94cd3-106">Амортизация для целей налогообложения рассчитывается с использованием текущего принципа налогообложения, чтобы достигнуть самой высокой возможной амортизации перед выплатой налогов, но амортизация для целей отчетности вычисляется в соответствии с законами и стандартами учета.</span><span class="sxs-lookup"><span data-stu-id="94cd3-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="94cd3-107">Различные виды амортизации вычисляются и записываются отдельно в слоях разноски.</span><span class="sxs-lookup"><span data-stu-id="94cd3-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="94cd3-108">Каждая книга, которая присоединяется к основным средствам, настраивается для определенного слоя разноски, имеющего общее задание на амортизацию.</span><span class="sxs-lookup"><span data-stu-id="94cd3-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="94cd3-109">Предусмотрено десять слоев разноски: Текущий, Операции, Налоги и семь настраиваемых слоев.</span><span class="sxs-lookup"><span data-stu-id="94cd3-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="94cd3-110">Можно также отключить разноску в главную книгу для этой книги, установив в поле Разносить в главную книгу значение Нет.</span><span class="sxs-lookup"><span data-stu-id="94cd3-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="94cd3-111">В поле Слой разноски затем автоматически задается значение Нет.</span><span class="sxs-lookup"><span data-stu-id="94cd3-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="94cd3-112">Обычно книги, которые не разносятся в главную книгу, используются для целей налоговой отчетности.</span><span class="sxs-lookup"><span data-stu-id="94cd3-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="94cd3-113">Такой подход дает дополнительную гибкость для удаления исторических проводок из модели стоимости ОС, поскольку они не были зафиксированы в главной книге.</span><span class="sxs-lookup"><span data-stu-id="94cd3-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="94cd3-114">Журналы основных средств определяются с помощью страницы Наименования журналов по пути Главная книга > Настройка журнала > Наименования журналов.</span><span class="sxs-lookup"><span data-stu-id="94cd3-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="94cd3-115">Каждый журнал, в котором можно разнести амортизацию, определяется своим наименованием журнала только для одного слоя разноски.</span><span class="sxs-lookup"><span data-stu-id="94cd3-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="94cd3-116">Слой разноски в журнале не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="94cd3-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="94cd3-117">Это ограничение помогает гарантировать разделение проводок для каждого слоя разноски.</span><span class="sxs-lookup"><span data-stu-id="94cd3-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="94cd3-118">Для каждого слоя разноски должно быть создано по крайней мере одно имя журнала.</span><span class="sxs-lookup"><span data-stu-id="94cd3-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="94cd3-119">При использовании книг, которые не разносятся в главную книгу, необходимо также создать журнал, в котором для слоя разноски задано значение "Нет".</span><span class="sxs-lookup"><span data-stu-id="94cd3-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="94cd3-120">Можно назначить счета ГК для проводок основных средств на странице Профили разноски основных средств.</span><span class="sxs-lookup"><span data-stu-id="94cd3-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="94cd3-121">Для каждого профиля разноски необходимо выбрать соответствующий тип проводки и книгу, а затем назначить счета учета.</span><span class="sxs-lookup"><span data-stu-id="94cd3-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="94cd3-122">Настройте запись профиля разноски для каждой книги, которая будет разноситься в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="94cd3-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="94cd3-123">Используя производные книги, можно разносить проводки одновременно по разным слоям разноски.</span><span class="sxs-lookup"><span data-stu-id="94cd3-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="94cd3-124">Вами создаются проводки исходной книги в журнал, в котором слой разноски соответствует слою разноски книги.</span><span class="sxs-lookup"><span data-stu-id="94cd3-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="94cd3-125">В процессе разноски проводки производных книг разносятся по соответствующим слоям разноски.</span><span class="sxs-lookup"><span data-stu-id="94cd3-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="94cd3-126">Дополнительные сведения см. в разделах [Производные книги](derived-books.md) и [Разноска с производными книгами](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="94cd3-126">For more information see, [Derived books](derived-books.md) and [Posting with derived books](post-derived-value-models.md).</span></span>



