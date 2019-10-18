---
title: Документы активов
description: В этом разделе описываются документы активов в «Управлении активами».
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5b791fd3e060c4f4ecdb1ca599a6041d421db74
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024545"
---
# <a name="asset-documents"></a><span data-ttu-id="c9ad4-103">Документы активов</span><span class="sxs-lookup"><span data-stu-id="c9ad4-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c9ad4-104">В этом разделе описываются документы активов в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="c9ad4-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="c9ad4-105">В «Управлении активами» можно настроить документы таким образом, чтобы они автоматически были связаны с типами заданий, производителями активов, типами активов или активами, например.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="c9ad4-106">Эта функциональность полезна при выпуске обновленных версий документов.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="c9ad4-107">В этом случае необходимо просто поместить обновленный документ в стандартное местоположение, которое используется для документов Finance and Operations, и прикрепить документ к созданной записи документа актива.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-107">In that case, you just have to put the updated document in the standard location that you use for your Finance and Operations documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="c9ad4-108">Доступ к обновленному документу можно получить через пункты меню **Все активы**, **Активыные активы**, **Мои активные активы**, **Все заказы на работу**, и **Активные задания заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="c9ad4-109">В процессе присоединения документов к записи документа актива используется стандартная система обработки документов.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="c9ad4-110">**Пример 1:** Документ, относящийся к типу задания, может описать процедуру для этого типа задания.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="c9ad4-111">**Пример 2:** Документ, связанный с комбинацией типа активы, производителя и модели, может быть стандартным руководством для выбранной модели производителя активов.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="c9ad4-112">Создать связь документа актива</span><span class="sxs-lookup"><span data-stu-id="c9ad4-112">Create asset document relation</span></span>

1. <span data-ttu-id="c9ad4-113">Выберите **Управление активами** \> **Настройка** \> **Документы активов**.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="c9ad4-114">Выберите **Создать**, чтобы создать запись документа актива.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="c9ad4-115">В зависимости от требуемого уровня конкретности для связи документа, сделайте соответствующие выборы в одном или более полях: **Тип актива**, **Производитель**, **Модель**, **Актив**, **Категория типа задания**, **Тип задания**, **Вариант типа задания**, и **Потребность в задании**.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="c9ad4-116">Параметры, доступные в полях **Вариант типа задания** и **Потребность в задании** зависят от выбора в поле **Тип задания**.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9ad4-117">Когда система ищет документы, которые должны быть связаны с активом или заказом на работу, «Управление активами» просматривает все документы об активах, чтобы проверить на возможное совпадение.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="c9ad4-118">Она всегда проверяет наиболее конкретные комбинации в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="c9ad4-119">Другими словами, «Управление активами» сначала проверяет на совпадение поле **Потребность в задании**.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="c9ad4-120">Если совпадение не найдено, оно проверяет на совпадение поле **Вариант типа задания**.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="c9ad4-121">Если совпадение не найдено, оно проверяет на совпадение поле **Тип задания** и т.д.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="c9ad4-122">Как вы можете видеть в макете страницы **Документы активов**, это поведение означает, что, чтобы найти наиболее конкретную комбинацию, «Управление активами» проверяет каждую запись справа налево на совпадение.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="c9ad4-123">Несколько документов могут быть связаны с активом или заказом на работу.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="c9ad4-124">Вы можете изменить уровень обслуживания по запросу на обслуживание или заказу на работу, по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="c9ad4-125">Выберите **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-125">Select **Attachments**.</span></span> <span data-ttu-id="c9ad4-126">Будет открыта стандартная страница **Обработка документов**.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="c9ad4-127">Настройка документов или примечаний, которые должны быть прикреплены к записи документа актива.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="c9ad4-128">После прикрепления документов поле **Вложения** показывает количество документов, связанных с записью.</span><span class="sxs-lookup"><span data-stu-id="c9ad4-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
