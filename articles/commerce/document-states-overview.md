---
title: Состояния и жизненный цикл документа
description: В этом разделе рассматриваются различные состояния документов элементов страницы в Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e3334e4284df681907d879ca2eab5cd12e764c99
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792831"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="c33b8-103">Состояния и жизненный цикл документа</span><span class="sxs-lookup"><span data-stu-id="c33b8-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c33b8-104">В этом разделе рассматриваются различные состояния документов элементов страницы в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c33b8-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="c33b8-105">Описания состояния документа</span><span class="sxs-lookup"><span data-stu-id="c33b8-105">Document state descriptions</span></span>

<span data-ttu-id="c33b8-106">В разделе [Элементы страницы](page-elements-overview.md) перечислены различные типы документов в системе управления контентом (CMS).</span><span class="sxs-lookup"><span data-stu-id="c33b8-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="c33b8-107">Эти типы документов могут иметь несколько состояний в инструменте разработки.</span><span class="sxs-lookup"><span data-stu-id="c33b8-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="c33b8-108">Состояния документов помогают предотвратить конфликты данных и обеспечивать управление версиями.</span><span class="sxs-lookup"><span data-stu-id="c33b8-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="c33b8-109">Они определяют, кто может изменять документы, когда документы могут быть изменены и когда изменения могут просматриваться другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="c33b8-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="c33b8-110">В следующей таблице показаны возможные состояния документов элементов страницы в Commerce.</span><span class="sxs-lookup"><span data-stu-id="c33b8-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="c33b8-111">Состояние документа</span><span class="sxs-lookup"><span data-stu-id="c33b8-111">Document state</span></span>      | <span data-ttu-id="c33b8-112">Действие конструктора сайтов</span><span class="sxs-lookup"><span data-stu-id="c33b8-112">Site builder action</span></span>        | <span data-ttu-id="c33b8-113">описание</span><span class="sxs-lookup"><span data-stu-id="c33b8-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="c33b8-114">Оформленные</span><span class="sxs-lookup"><span data-stu-id="c33b8-114">Checked out</span></span>         | <span data-ttu-id="c33b8-115">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="c33b8-115">Select **Edit**.</span></span>           | <span data-ttu-id="c33b8-116">Соответствующий документ извлечен вами.</span><span class="sxs-lookup"><span data-stu-id="c33b8-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="c33b8-117">Если документ находится в этом состоянии, он не может быть изменен другими пользователями системы, прошедшими проверку подлинности, и любые изменения, внесенные в документ, будут видны только вам.</span><span class="sxs-lookup"><span data-stu-id="c33b8-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="c33b8-118">Сохранено</span><span class="sxs-lookup"><span data-stu-id="c33b8-118">Saved</span></span>               | <span data-ttu-id="c33b8-119">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c33b8-119">Select **Save**.</span></span>           | <span data-ttu-id="c33b8-120">Изменения, внесенные в извлеченный документ, сохраняются в базе данных, но документ еще не был зарегистрирован или опубликован.</span><span class="sxs-lookup"><span data-stu-id="c33b8-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="c33b8-121">Сохраненные изменения не видны другим пользователям системы, прошедшим проверку подлинности, до тех пор, пока автор не выберет **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="c33b8-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="c33b8-122">Они не видны внешним пользователям до тех пор, пока элемент не будет опубликован.</span><span class="sxs-lookup"><span data-stu-id="c33b8-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="c33b8-123">Отменено извлечение</span><span class="sxs-lookup"><span data-stu-id="c33b8-123">Discarded check out</span></span> | <span data-ttu-id="c33b8-124">Выберите **Отменить изменения**.</span><span class="sxs-lookup"><span data-stu-id="c33b8-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="c33b8-125">Все изменения в извлеченном документе отбрасываются, и элемент восстанавливается до последней возвращенной версии.</span><span class="sxs-lookup"><span data-stu-id="c33b8-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="c33b8-126">Возвращенные</span><span class="sxs-lookup"><span data-stu-id="c33b8-126">Checked in</span></span>          | <span data-ttu-id="c33b8-127">Выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="c33b8-127">Select **Finish editing**.</span></span> | <span data-ttu-id="c33b8-128">Измененный документ возвращен.</span><span class="sxs-lookup"><span data-stu-id="c33b8-128">The edited document is checked in.</span></span> <span data-ttu-id="c33b8-129">Все изменения видны другим пользователям системы, прошедшим проверку подлинности, и эти пользователи могут затем редактировать документ.</span><span class="sxs-lookup"><span data-stu-id="c33b8-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="c33b8-130">Каждый возврат создает запись версии документа в истории элемента.</span><span class="sxs-lookup"><span data-stu-id="c33b8-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="c33b8-131">Опубликованные</span><span class="sxs-lookup"><span data-stu-id="c33b8-131">Published</span></span>           | <span data-ttu-id="c33b8-132">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="c33b8-132">Select **Publish**.</span></span>        | <span data-ttu-id="c33b8-133">Документ публикуется, и изменения отправляются на ваш активный сайт и становятся видимыми внешним пользователям.</span><span class="sxs-lookup"><span data-stu-id="c33b8-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="c33b8-134">Элементы могут быть опубликованы только в том случае, если они сначала были возвращены путем выбора команды **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="c33b8-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="c33b8-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c33b8-135">Additional resources</span></span>

[<span data-ttu-id="c33b8-136">Способы добавления содержимого</span><span class="sxs-lookup"><span data-stu-id="c33b8-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="c33b8-137">Глоссарий по модели страниц</span><span class="sxs-lookup"><span data-stu-id="c33b8-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="c33b8-138">Работа с группами публикаций</span><span class="sxs-lookup"><span data-stu-id="c33b8-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="c33b8-139">Включение и использование межканального совместного использования</span><span class="sxs-lookup"><span data-stu-id="c33b8-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="c33b8-140">Работа с модулями</span><span class="sxs-lookup"><span data-stu-id="c33b8-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="c33b8-141">Работа с фрагментами</span><span class="sxs-lookup"><span data-stu-id="c33b8-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="c33b8-142">Обзор шаблонов и макетов</span><span class="sxs-lookup"><span data-stu-id="c33b8-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="c33b8-143">Настройка навигации по сайту</span><span class="sxs-lookup"><span data-stu-id="c33b8-143">Customize site navigation</span></span>](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]