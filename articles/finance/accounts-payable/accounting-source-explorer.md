---
title: Анализатор источника учета
description: Эта статья представляет информацию об Анализаторе источника учета, который можно использовать для подробного анализа сведений об источнике за учетными записями ГК.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7f92781a8e1400206f91f91c46c319b928e0010c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250730"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="bf910-103">Анализатор источника учета</span><span class="sxs-lookup"><span data-stu-id="bf910-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf910-104">Эта статья представляет информацию об Анализаторе источника учета, который можно использовать для подробного анализа сведений об источнике за учетными записями ГК.</span><span class="sxs-lookup"><span data-stu-id="bf910-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="bf910-105">Анализатор источника учета — это новая страница, на которой представлены сведения об источнике.</span><span class="sxs-lookup"><span data-stu-id="bf910-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="bf910-106">Анализатор источника учета можно использовать как отдельное средство или для анализа сведений записей учета ГК.</span><span class="sxs-lookup"><span data-stu-id="bf910-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="bf910-107">Например, анализатор источника учета можно использовать для получения самых подробных сведений об источнике для сальдо в пробном балансе или для проводки по ваучеру.</span><span class="sxs-lookup"><span data-stu-id="bf910-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="bf910-108">Затем можно использовать функцию "Экспорт в MS Excel" для дальнейшего анализа сведений в Microsoft Excel (например, в сводной таблице или сводном отчете).</span><span class="sxs-lookup"><span data-stu-id="bf910-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="bf910-109">Анализатор источника учета всегда показывает ту же итоговую сумму на счет ГК, что и в ГК (например, в пробном балансе).</span><span class="sxs-lookup"><span data-stu-id="bf910-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="bf910-110">Как и в пробном балансе, можно отобразить сегменты в отдельных столбцах.</span><span class="sxs-lookup"><span data-stu-id="bf910-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="bf910-111">Достаточно выбрать соответствующий набора финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="bf910-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="bf910-112">Можно использовать параметры для определения интервала дат для анализа.</span><span class="sxs-lookup"><span data-stu-id="bf910-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="bf910-113">Эта функциональность также напоминает функциональность в пробном балансе.</span><span class="sxs-lookup"><span data-stu-id="bf910-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="bf910-114">Для всех документов, которые используют платформу документа-источника, анализатор источника учета показывает дополнительные сведения на основании распределений по бухгалтерским счетам и, если это применимо, распределений по бухгалтерским счетам проекта.</span><span class="sxs-lookup"><span data-stu-id="bf910-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="bf910-115">Эти сведения включают тип денежных сумм, проект, мероприятие, категорию и свойство строки.</span><span class="sxs-lookup"><span data-stu-id="bf910-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="bf910-116">Вот несколько примеров анализа, который можно выполнить:</span><span class="sxs-lookup"><span data-stu-id="bf910-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="bf910-117">Отклонения между заказами на покупку и накладными поставщика, поскольку каждое отклонение представлено типом денежной суммы, например отклонение по накладным расходам.</span><span class="sxs-lookup"><span data-stu-id="bf910-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="bf910-118">Оплачиваемые и неоплачиваемые часы и расходы по проекту, бизнес-единице и счету ГК.</span><span class="sxs-lookup"><span data-stu-id="bf910-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="bf910-119">Для документов-источников, которые используют понятие удостоверений ссылок документа-источника, анализатор источника учета показывает еще больше сведений, таких как клиент, поставщик, работник, продукт, количество, текст единиц измерений и описания.</span><span class="sxs-lookup"><span data-stu-id="bf910-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="bf910-120">Вот несколько примеров анализа, который можно выполнить:</span><span class="sxs-lookup"><span data-stu-id="bf910-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="bf910-121">Гостиничные расходы на бизнес-единицу и бренд гостиницы за финансовый период на основании отчетов по расходам.</span><span class="sxs-lookup"><span data-stu-id="bf910-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="bf910-122">Скидки по поставщику, продукту и подразделению.</span><span class="sxs-lookup"><span data-stu-id="bf910-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="bf910-123">В случае этих документов также можно перейти к фактическому документу-источнику из анализатора источника учета.</span><span class="sxs-lookup"><span data-stu-id="bf910-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]