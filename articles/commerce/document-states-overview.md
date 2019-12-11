---
title: Состояния и жизненный цикл документа
description: В этом разделе рассматриваются различные состояния документов элементов страницы в Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a34d10edbf84ac1814afdc7107727aea68a303e0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770443"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="27ae4-103">Состояния и жизненный цикл документа</span><span class="sxs-lookup"><span data-stu-id="27ae4-103">Document states and lifecycle</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="27ae4-104">В этом разделе рассматриваются различные состояния документов элементов страницы в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="27ae4-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="27ae4-105">Описания состояния документа</span><span class="sxs-lookup"><span data-stu-id="27ae4-105">Document state descriptions</span></span>

<span data-ttu-id="27ae4-106">В разделе [Элементы страницы](page-elements-overview.md) перечислены различные типы документов в системе управления контентом (CMS).</span><span class="sxs-lookup"><span data-stu-id="27ae4-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="27ae4-107">Эти типы документов могут иметь несколько состояний в инструменте разработки.</span><span class="sxs-lookup"><span data-stu-id="27ae4-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="27ae4-108">Состояния документов помогают предотвратить конфликты данных и обеспечивать управление версиями.</span><span class="sxs-lookup"><span data-stu-id="27ae4-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="27ae4-109">Они определяют, кто может изменять документы, когда документы могут быть изменены и когда изменения могут просматриваться другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="27ae4-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="27ae4-110">В следующей таблице показаны возможные состояния документов элементов страницы в Commerce.</span><span class="sxs-lookup"><span data-stu-id="27ae4-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="27ae4-111">Состояние документа</span><span class="sxs-lookup"><span data-stu-id="27ae4-111">Document state</span></span> | <span data-ttu-id="27ae4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="27ae4-112">Description</span></span> |
|---|---|
| <span data-ttu-id="27ae4-113">Извлеченные</span><span class="sxs-lookup"><span data-stu-id="27ae4-113">Checked out</span></span> | <span data-ttu-id="27ae4-114">Когда элемент CMS извлечен для вас, он не может быть изменен никаким другим пользователем системы, прошедшим проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="27ae4-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="27ae4-115">Любые изменения, внесенные в элемент, будут видны только вам.</span><span class="sxs-lookup"><span data-stu-id="27ae4-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="27ae4-116">Возвращенные</span><span class="sxs-lookup"><span data-stu-id="27ae4-116">Checked in</span></span> | <span data-ttu-id="27ae4-117">Когда элемент CMS возвращен, все изменения видны другим пользователям системы, прошедших проверку подлинности, и эти пользователи могут затем извлечь элемент и редактировать его.</span><span class="sxs-lookup"><span data-stu-id="27ae4-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="27ae4-118">Каждый возврат создает запись версии документа в истории элемента.</span><span class="sxs-lookup"><span data-stu-id="27ae4-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="27ae4-119">Опубликованные</span><span class="sxs-lookup"><span data-stu-id="27ae4-119">Published</span></span> | <span data-ttu-id="27ae4-120">Когда элемент CMS опубликован, он перемещается на активный сайт и становится видимым в Интернете для внешних пользователей, не прошедших проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="27ae4-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="27ae4-121">Элементы могут быть опубликованы только в том случае, если они возвращены.</span><span class="sxs-lookup"><span data-stu-id="27ae4-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="27ae4-122">Сохранено</span><span class="sxs-lookup"><span data-stu-id="27ae4-122">Saved</span></span> | <span data-ttu-id="27ae4-123">Изменения, внесенные в извлеченный элемент CMS, могут быть сохранены в CMS до того, как элемент будет возвращен или опубликован.</span><span class="sxs-lookup"><span data-stu-id="27ae4-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="27ae4-124">Эти сохраненные изменения не видны другим пользователям системы, прошедшим проверку подлинности, до тех пор, пока элемент не будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="27ae4-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="27ae4-125">Они не видны внешним пользователям до тех пор, пока элемент не будет опубликован.</span><span class="sxs-lookup"><span data-stu-id="27ae4-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="27ae4-126">Отменено извлечение</span><span class="sxs-lookup"><span data-stu-id="27ae4-126">Discarded check out</span></span> | <span data-ttu-id="27ae4-127">Когда извлеченный элемент CMS отменяется, все сохраненные изменения удаляются, и элемент восстанавливается до последней возвращенной версии.</span><span class="sxs-lookup"><span data-stu-id="27ae4-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="27ae4-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="27ae4-128">Additional resources</span></span>

[<span data-ttu-id="27ae4-129">Способы добавления содержимого</span><span class="sxs-lookup"><span data-stu-id="27ae4-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="27ae4-130">Глоссарий модели страниц</span><span class="sxs-lookup"><span data-stu-id="27ae4-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="27ae4-131">Работа с модулями</span><span class="sxs-lookup"><span data-stu-id="27ae4-131">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="27ae4-132">Работа с фрагментами</span><span class="sxs-lookup"><span data-stu-id="27ae4-132">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="27ae4-133">Обзор шаблонов и макетов</span><span class="sxs-lookup"><span data-stu-id="27ae4-133">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="27ae4-134">Настройка навигации по сайту</span><span class="sxs-lookup"><span data-stu-id="27ae4-134">Customize site navigation</span></span>](customize-site-navigation.md)
