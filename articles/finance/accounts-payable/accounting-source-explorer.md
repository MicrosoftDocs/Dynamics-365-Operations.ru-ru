---
title: Анализатор источника учета
description: Эта статья представляет информацию об Анализаторе источника учета, который можно использовать для подробного анализа сведений об источнике за учетными записями ГК.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: roschlom
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4624a740538493c247b6c3a0f051ed6208c52504
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820939"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="a13b1-103">Анализатор источника учета</span><span class="sxs-lookup"><span data-stu-id="a13b1-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a13b1-104">Эта статья представляет информацию об Анализаторе источника учета, который можно использовать для подробного анализа сведений об источнике за учетными записями ГК.</span><span class="sxs-lookup"><span data-stu-id="a13b1-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="a13b1-105">Анализатор источника учета — это новая страница, на которой представлены сведения об источнике.</span><span class="sxs-lookup"><span data-stu-id="a13b1-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="a13b1-106">Анализатор источника учета можно использовать как отдельное средство или для анализа сведений записей учета ГК.</span><span class="sxs-lookup"><span data-stu-id="a13b1-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="a13b1-107">Например, анализатор источника учета можно использовать для получения самых подробных сведений об источнике для сальдо в пробном балансе или для проводки по ваучеру.</span><span class="sxs-lookup"><span data-stu-id="a13b1-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="a13b1-108">Затем можно использовать функцию "Экспорт в MS Excel" для дальнейшего анализа сведений в Microsoft Excel (например, в сводной таблице или сводном отчете).</span><span class="sxs-lookup"><span data-stu-id="a13b1-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="a13b1-109">Анализатор источника учета всегда показывает ту же итоговую сумму на счет ГК, что и в ГК (например, в пробном балансе).</span><span class="sxs-lookup"><span data-stu-id="a13b1-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="a13b1-110">Как и в пробном балансе, можно отобразить сегменты в отдельных столбцах.</span><span class="sxs-lookup"><span data-stu-id="a13b1-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="a13b1-111">Достаточно выбрать соответствующий набора финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="a13b1-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="a13b1-112">Можно использовать параметры для определения интервала дат для анализа.</span><span class="sxs-lookup"><span data-stu-id="a13b1-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="a13b1-113">Эта функциональность также напоминает функциональность в пробном балансе.</span><span class="sxs-lookup"><span data-stu-id="a13b1-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="a13b1-114">Для всех документов, которые используют платформу документа-источника, анализатор источника учета показывает дополнительные сведения на основании распределений по бухгалтерским счетам и, если это применимо, распределений по бухгалтерским счетам проекта.</span><span class="sxs-lookup"><span data-stu-id="a13b1-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="a13b1-115">Эти сведения включают тип денежных сумм, проект, мероприятие, категорию и свойство строки.</span><span class="sxs-lookup"><span data-stu-id="a13b1-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="a13b1-116">Вот несколько примеров анализа, который можно выполнить:</span><span class="sxs-lookup"><span data-stu-id="a13b1-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="a13b1-117">Отклонения между заказами на покупку и накладными поставщика, поскольку каждое отклонение представлено типом денежной суммы, например отклонение по накладным расходам.</span><span class="sxs-lookup"><span data-stu-id="a13b1-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="a13b1-118">Оплачиваемые и неоплачиваемые часы и расходы по проекту, бизнес-единице и счету ГК.</span><span class="sxs-lookup"><span data-stu-id="a13b1-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="a13b1-119">Для документов-источников, которые используют понятие удостоверений ссылок документа-источника, анализатор источника учета показывает еще больше сведений, таких как клиент, поставщик, работник, продукт, количество, текст единиц измерений и описания.</span><span class="sxs-lookup"><span data-stu-id="a13b1-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="a13b1-120">Вот несколько примеров анализа, который можно выполнить:</span><span class="sxs-lookup"><span data-stu-id="a13b1-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="a13b1-121">Гостиничные расходы на бизнес-единицу и бренд гостиницы за финансовый период на основании отчетов по расходам.</span><span class="sxs-lookup"><span data-stu-id="a13b1-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="a13b1-122">Скидки по поставщику, продукту и подразделению.</span><span class="sxs-lookup"><span data-stu-id="a13b1-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="a13b1-123">В случае этих документов также можно перейти к фактическому документу-источнику из анализатора источника учета.</span><span class="sxs-lookup"><span data-stu-id="a13b1-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]