---
title: Разноска с производными книгами
description: В этой статье описывается использование производных книг.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6556965a1356522de5f4c17ddeab378a128fbe3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833026"
---
# <a name="post-with-derived-books"></a><span data-ttu-id="386d7-103">Разноска с производными книгами</span><span class="sxs-lookup"><span data-stu-id="386d7-103">Post with derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="386d7-104">В этой статье описывается использование производных книг.</span><span class="sxs-lookup"><span data-stu-id="386d7-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="386d7-105">При разноске проводки для книги, содержащей производные книги, проводки журнала производной амортизации автоматически разносятся из журналов, заказов на покупку или накладных с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="386d7-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="386d7-106">Однако если вы готовите проводки основной книги в журнале "Основные средства", можно просматривать и изменять суммы производных проводок перед их разноской.</span><span class="sxs-lookup"><span data-stu-id="386d7-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="386d7-107">Некоторые счета, например счета налогов и клиентов или поставщиков, обновляются только один раз при помощи разносок основной книги.</span><span class="sxs-lookup"><span data-stu-id="386d7-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="386d7-108">Проводки производной книги разносятся по счетам, определенным для производной книги на странице "Профили разноски основных средств".</span><span class="sxs-lookup"><span data-stu-id="386d7-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="386d7-109">Приобретение часто используется в качестве типа проводки для производных книг.</span><span class="sxs-lookup"><span data-stu-id="386d7-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="386d7-110">Это необходимо, когда книга и производная книга должны применяться к ОС с момента ввода ОС в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="386d7-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="386d7-111">Для данного типа проводки могут применяться и другие значения.</span><span class="sxs-lookup"><span data-stu-id="386d7-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="386d7-112">Например, если у основной книги и производных книг одинаковые интервалы продажи или выбытия, все типы проводок ОС доступны для настройки производной модели стоимости.</span><span class="sxs-lookup"><span data-stu-id="386d7-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="386d7-113">Сумма амортизации, разнесенная в производной книге, равна сумме, разнесенной для основной книги.</span><span class="sxs-lookup"><span data-stu-id="386d7-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="386d7-114">Если методы амортизации для различных книг отличаются, не следует создавать проводки амортизации с использованием производного процесса.</span><span class="sxs-lookup"><span data-stu-id="386d7-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="386d7-115">пример</span><span class="sxs-lookup"><span data-stu-id="386d7-115">Example</span></span> 
<span data-ttu-id="386d7-116">Ниже представлены сведения о способах настройки проводок приобретения с функциональностью производной книги.</span><span class="sxs-lookup"><span data-stu-id="386d7-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="386d7-117">Создайте книги на странице "Книги".</span><span class="sxs-lookup"><span data-stu-id="386d7-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="386d7-118">Книга для учета: VM 1, текущий слой разноски</span><span class="sxs-lookup"><span data-stu-id="386d7-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="386d7-119">Книга для налогов: VM 2, слой разноски налога</span><span class="sxs-lookup"><span data-stu-id="386d7-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="386d7-120">В МС 1 щелкните вкладку "Производные книги". Выберите "МС 2" в поле "Книга" и "Приобретение" в поле "Тип проводки".</span><span class="sxs-lookup"><span data-stu-id="386d7-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="386d7-121">Книги могут быть прикреплены к определенным ОС.</span><span class="sxs-lookup"><span data-stu-id="386d7-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="386d7-122">Когда ввод в эксплуатацию разнесен для ОС с книгой МС 1, ввод в эксплуатацию разносится не только в МС 1, но также в производной книге МС 2.</span><span class="sxs-lookup"><span data-stu-id="386d7-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="386d7-123">Статус обеих книг основных средств обновляется на "Открыта".</span><span class="sxs-lookup"><span data-stu-id="386d7-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="386d7-124">Если вы не используете производные книги, необходимо разнести ввод в эксплуатацию ОС для книги МС 1 и книги МС 2.</span><span class="sxs-lookup"><span data-stu-id="386d7-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="386d7-125">Дополнительные сведения см. в разделе [Производные книги](derived-books.md)</span><span class="sxs-lookup"><span data-stu-id="386d7-125">For more information, see [Derived books](derived-books.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]