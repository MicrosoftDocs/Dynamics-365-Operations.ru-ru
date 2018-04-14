---
title: "Использование внешних каталогов для внешних eProcurement"
description: "В этой теме поясняется, как использовать внешние каталоги для создания и отправки заявок."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8ccf810d3ecfeb35e86e7b552f7e59fc7660aa01
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a><span data-ttu-id="aa7f3-103">Использование внешних каталогов для внешних eProcurement</span><span class="sxs-lookup"><span data-stu-id="aa7f3-103">Use external catalogs for PunchOut eProcurement</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="aa7f3-104">Использование внешних каталогов для электронного снабжения по схеме PunchOut избавляет от необходимости вести информацию о продуктах ваших поставщиков в ваших собственных справочниках.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="aa7f3-105">Вместо этого корзина для покупок на веб-сайте поставщика преобразуется в строки заявки, содержащих правильную информацию о продуктах.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="aa7f3-106">Желательно избегать ведения описаний и цен продуктов поставщиков в ваших собственных справочниках продуктов.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="aa7f3-107">Вместо этого используйте для электронного снабжения по схеме PunchOut внешние каталоги.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="aa7f3-108">В этом случае при создании заявок сотрудники могут зайти на сайт поставщика с внешним каталогом (иными словами, выйти из вашей системы и перейти на сайт поставщика).</span><span class="sxs-lookup"><span data-stu-id="aa7f3-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="aa7f3-109">Продукты, добавляемые в корзину для покупок на веб-сайте поставщика, затем можно преобразовать в строки заявки.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="aa7f3-110">Таким образом вы получаете правильную информацию о продукте: код продукта, наименование, цену и т.д.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="aa7f3-111">Чтобы использовать внешние каталоги, сотрудник должен создать заявку на странице **Мои заявки на закупку**.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="aa7f3-112">Сотрудник, который создает заявку, называется составителем заявки.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="aa7f3-113">Будучи составителем, можно выполнять следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="aa7f3-114">Использовать действие строки **Внешние каталоги**, чтобы открыть страницу, которая включает в себя все внешние каталоги, доступные для указанного инициатора запроса, юридического лица-покупателя и операционной единицы-получателя.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="aa7f3-115">В зависимости от ваших разрешений изменить инициатора запроса, юридическое лицо-покупателя и операционную единицу-получателя.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="aa7f3-116">Изменения в этих значениях могут привести к изменению списка внешних каталогов, доступных инициатору.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="aa7f3-117">Доступные внешние каталоги зависят от текущих активных политик закупок для юридического лица-покупателя или операционной единицы-получателя.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="aa7f3-118">Эти политики могут разрешать или запрещать доступ к определенным категориям закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="aa7f3-119">Соответственно, можно влиять на список внешних каталогов, сопоставленных этим категориям закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="aa7f3-120">Дополнительные сведения о политиках см. в разделе [Политики закупок](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="aa7f3-120">For more information about policies, see [Purchasing policies](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="aa7f3-121">Чтобы найти внешние каталоги для конкретных категорий закупаемой продукции, введите текст в поле поиска в каталог.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="aa7f3-122">Чтобы добавить продукты из внешнего каталога поставщика на веб-сайте поставщика, щелкните внешний каталог.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="aa7f3-123">Затем добавьте продукты в корзину для покупок и оформите заказ. Строки корзины для покупок будут перенесены в Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="aa7f3-124">При наличии нескольких вариантов для категорий закупаемой продукции выберите необходимую категорию закупаемой продукции, прежде чем добавлять строки в заявку.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="aa7f3-125">После добавления строк в заявку можно добавить дополнительные строки без использования внешних каталогов.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="aa7f3-126">Также можно продолжить пользоваться внешними каталогами для добавления строк.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="aa7f3-127">Когда заявка будет готова, отправьте ее на утверждение с помощью действия **Workflow-процесс** > **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="aa7f3-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

