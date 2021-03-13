---
title: Использование внешних каталогов для электронных закупок с внешними заказами
description: В этой теме поясняется, как использовать внешние каталоги для создания и отправки заявок.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests, CatExternalCatalogBasketWizard, CatExternalCatalogPunchoutDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74b49e32684571f622b25dcdd179eeeed9b35365
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018761"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a><span data-ttu-id="f47a2-103">Использование внешних каталогов для электронных закупок с внешними заказами</span><span class="sxs-lookup"><span data-stu-id="f47a2-103">Use external catalogs for PunchOut e-procurement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f47a2-104">Использование внешних каталогов для электронного снабжения по схеме PunchOut избавляет от необходимости вести информацию о продуктах ваших поставщиков в ваших собственных справочниках.</span><span class="sxs-lookup"><span data-stu-id="f47a2-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="f47a2-105">Вместо этого корзина для покупок на веб-сайте поставщика преобразуется в строки заявки, содержащих правильную информацию о продуктах.</span><span class="sxs-lookup"><span data-stu-id="f47a2-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="f47a2-106">Желательно избегать ведения описаний и цен продуктов поставщиков в ваших собственных справочниках продуктов.</span><span class="sxs-lookup"><span data-stu-id="f47a2-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="f47a2-107">Вместо этого используйте для электронного снабжения по схеме PunchOut внешние каталоги.</span><span class="sxs-lookup"><span data-stu-id="f47a2-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="f47a2-108">В этом случае при создании заявок сотрудники могут зайти на сайт поставщика с внешним каталогом (иными словами, выйти из вашей системы и перейти на сайт поставщика).</span><span class="sxs-lookup"><span data-stu-id="f47a2-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="f47a2-109">Продукты, добавляемые в корзину для покупок на веб-сайте поставщика, затем можно преобразовать в строки заявки.</span><span class="sxs-lookup"><span data-stu-id="f47a2-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="f47a2-110">Таким образом вы получаете правильную информацию о продукте: код продукта, наименование, цену и т.д.</span><span class="sxs-lookup"><span data-stu-id="f47a2-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="f47a2-111">Чтобы использовать внешние каталоги, сотрудник должен создать заявку на странице **Мои заявки на закупку**.</span><span class="sxs-lookup"><span data-stu-id="f47a2-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="f47a2-112">Сотрудник, который создает заявку, называется составителем заявки.</span><span class="sxs-lookup"><span data-stu-id="f47a2-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="f47a2-113">Будучи составителем, можно выполнять следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="f47a2-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="f47a2-114">Использовать действие строки **Внешние каталоги**, чтобы открыть страницу, которая включает в себя все внешние каталоги, доступные для указанного инициатора запроса, юридического лица-покупателя и операционной единицы-получателя.</span><span class="sxs-lookup"><span data-stu-id="f47a2-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="f47a2-115">В зависимости от ваших разрешений изменить инициатора запроса, юридическое лицо-покупателя и операционную единицу-получателя.</span><span class="sxs-lookup"><span data-stu-id="f47a2-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="f47a2-116">Изменения в этих значениях могут привести к изменению списка внешних каталогов, доступных инициатору.</span><span class="sxs-lookup"><span data-stu-id="f47a2-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="f47a2-117">Доступные внешние каталоги зависят от текущих активных политик закупок для юридического лица-покупателя или операционной единицы-получателя.</span><span class="sxs-lookup"><span data-stu-id="f47a2-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="f47a2-118">Эти политики могут разрешать или запрещать доступ к определенным категориям закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="f47a2-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="f47a2-119">Соответственно, можно влиять на список внешних каталогов, сопоставленных этим категориям закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="f47a2-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="f47a2-120">Дополнительные сведения о политиках см. в разделе [Обзор политик закупок](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="f47a2-120">For more information about policies, see [Purchasing policies overview](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="f47a2-121">Чтобы найти внешние каталоги для конкретных категорий закупаемой продукции, введите текст в поле поиска в каталог.</span><span class="sxs-lookup"><span data-stu-id="f47a2-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="f47a2-122">Чтобы добавить продукты из внешнего каталога поставщика на веб-сайте поставщика, щелкните внешний каталог.</span><span class="sxs-lookup"><span data-stu-id="f47a2-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="f47a2-123">Затем добавьте продукты в корзину для покупок и оформите заказ. Строки корзины для покупок будут перенесены в Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f47a2-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="f47a2-124">При наличии нескольких вариантов для категорий закупаемой продукции выберите необходимую категорию закупаемой продукции, прежде чем добавлять строки в заявку.</span><span class="sxs-lookup"><span data-stu-id="f47a2-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="f47a2-125">После добавления строк в заявку можно добавить дополнительные строки без использования внешних каталогов.</span><span class="sxs-lookup"><span data-stu-id="f47a2-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="f47a2-126">Также можно продолжить пользоваться внешними каталогами для добавления строк.</span><span class="sxs-lookup"><span data-stu-id="f47a2-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="f47a2-127">Когда заявка будет готова, отправьте ее на утверждение с помощью действия **Workflow-процесс** > **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="f47a2-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="f47a2-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f47a2-128">Additional resources</span></span>

- [<span data-ttu-id="f47a2-129">Настройка внешнего каталога для электронных закупок с внешними заказами</span><span class="sxs-lookup"><span data-stu-id="f47a2-129">Set up an external catalog for PunchOut e-procurement</span></span>](set-up-external-catalog-for-punchout.md)
- [<span data-ttu-id="f47a2-130">Улучшения cXML покупки</span><span class="sxs-lookup"><span data-stu-id="f47a2-130">Purchasing cXML enhancements</span></span>](purchasing-cxml-enhancements.md)