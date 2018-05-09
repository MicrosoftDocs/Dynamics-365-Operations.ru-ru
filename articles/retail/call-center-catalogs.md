---
title: "Каталоги центра обработки вызовов"
description: "Эта статья содержит описание функций специально для центра обработки вызовов по каталогам в Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 99f66e975cf5875f357af095ead66529b9784eff
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="call-center-catalogs"></a><span data-ttu-id="7fc29-103">Каталоги центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="7fc29-103">Call center catalogs</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7fc29-104">Эта статья содержит описание функций специально для центра обработки вызовов по каталогам в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="7fc29-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="7fc29-105">В центре обработки вызовов каталоги продуктов используются для определения продуктов, которые требуется предложить клиентам.</span><span class="sxs-lookup"><span data-stu-id="7fc29-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="7fc29-106">В центрах обработки вызовов обычно используются печатные каталоги.</span><span class="sxs-lookup"><span data-stu-id="7fc29-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="7fc29-107">Разработка и производство печатного каталога выполняются вне Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="7fc29-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="7fc29-108">Однако вы можете создать и сохранить цифровую форму каталога, используя те же страницы, что и при настройке интернет-каталогов розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="7fc29-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="7fc29-109">Перед созданием каталога необходимо настроить ассортименты продуктов и назначить ассортименты центру обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="7fc29-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="7fc29-110">После этого следует добавить продукты в каталог, выбрав продукты из этих ассортиментов.</span><span class="sxs-lookup"><span data-stu-id="7fc29-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="7fc29-111">После добавления продуктов в каталог и завершения составления каталога необходимо утвердить каталог для проверки данных.</span><span class="sxs-lookup"><span data-stu-id="7fc29-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="7fc29-112">Затем следует отправить каталог на просмотр и утверждение.</span><span class="sxs-lookup"><span data-stu-id="7fc29-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="7fc29-113">После утверждения каталога, он может быть опубликован.</span><span class="sxs-lookup"><span data-stu-id="7fc29-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="7fc29-114">После создания каталога центра обработки вызовов можно сделать снимок данных каталога в момент публикации каталога.</span><span class="sxs-lookup"><span data-stu-id="7fc29-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="7fc29-115">Благодаря этой функции снимка можно получить доступ к определенной версии каталога, даже если каталог изменяется и обновляется впоследствии.</span><span class="sxs-lookup"><span data-stu-id="7fc29-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="7fc29-116">Кроме того, каталоги центра обработки вызовов можно настроить для включения следующих дополнительных возможностей.</span><span class="sxs-lookup"><span data-stu-id="7fc29-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="7fc29-117">**Коды источников** — коды источников, которые используются для отслеживания реакции клиентов на определенные рассылки каталогов.</span><span class="sxs-lookup"><span data-stu-id="7fc29-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="7fc29-118">**Бесплатные продукты** — продукты могут быть включены в заказ клиента без дополнительной платы.</span><span class="sxs-lookup"><span data-stu-id="7fc29-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="7fc29-119">Эти продукты автоматически добавляются в заказ, когда код источника каталога вводится в заказ.</span><span class="sxs-lookup"><span data-stu-id="7fc29-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="7fc29-120">**Сценарии** — сценарии — это тексты, которые работник центра обработки вызовов читает клиенту при создании заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="7fc29-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="7fc29-121">Сценарии могут включать приветствия или предложения покупки.</span><span class="sxs-lookup"><span data-stu-id="7fc29-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="7fc29-122">**Макет страницы** — Макет страницы захватывает положение страницы продуктов в напечатанном каталоге.</span><span class="sxs-lookup"><span data-stu-id="7fc29-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="7fc29-123">Эта информация использована для отчета анализа области каталога.</span><span class="sxs-lookup"><span data-stu-id="7fc29-123">This information is used for the catalog area analysis report.</span></span>





