---
title: Новый пользовательский интерфейс для документов в управлении бизнес-документами
description: В этой теме приводятся сведения об использовании нового пользовательского интерфейса документа в средстве управления бизнес-документами в структуре электронной отчетности.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2cb6e0da4af07b9b8486bf1e5bda29523cbd08e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681360"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="1ef09-103">Новый пользовательский интерфейс для документов в управлении бизнес-документами</span><span class="sxs-lookup"><span data-stu-id="1ef09-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ef09-104">Управление бизнес-документами позволяет бизнес-пользователям редактировать шаблоны деловых документов с помощью службы Microsoft 365 или соответствующего классического приложения Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="1ef09-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="1ef09-105">Правки могут включать изменения структуры или новые развертывания, или пользователи могут добавлять заполнители для включения дополнительных данных без изменения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="1ef09-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="1ef09-106">Дополнительные сведения о работе с системой управления бизнес-документами см. в разделе [Обзор управления бизнес-документами](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="1ef09-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="1ef09-107">Новый пользовательский интерфейс документа является более четким и более удобным для использования.</span><span class="sxs-lookup"><span data-stu-id="1ef09-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="1ef09-108">В области **Бизнес-документ** отображаются только шаблоны, доступные для текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="1ef09-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="1ef09-109">Кнопка **Создать документ** позволяет пользователям создавать и изменять шаблоны в конфигурации формата электронной отчетности, предоставляемой другим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="1ef09-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="1ef09-110">В примере данного раздела поставщиком является Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1ef09-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="1ef09-111">Предоставление доступа для нового пользовательского интерфейса документа в управлении бизнес-документами</span><span class="sxs-lookup"><span data-stu-id="1ef09-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="1ef09-112">Чтобы начать пользоваться новым пользовательским интерфейсом документа в управлении бизнес-документами, необходимо включить функцию **Взаимодействие с пользовательским интерфейсом по типу Office для управления бизнес-документами** в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="1ef09-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="1ef09-113">Чтобы включить эту функцию для всех юридических лиц, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1ef09-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="1ef09-114">В рабочей области **Управление функциями** на вкладке **Создать** в списке выберите функцию **Взаимодействие с пользовательским интерфейсов по типу Office для управления бизнес-документами**.</span><span class="sxs-lookup"><span data-stu-id="1ef09-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="1ef09-115">Чтобы включить выбранный компонент, установите флажок **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="1ef09-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="1ef09-116">Обновите страницу, чтобы получить доступ к новому компоненту.</span><span class="sxs-lookup"><span data-stu-id="1ef09-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="1ef09-117">Редактирование шаблонов, принадлежащих другим поставщикам</span><span class="sxs-lookup"><span data-stu-id="1ef09-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="1ef09-118">В рабочей области **Управление бизнес-документами** выберите **Создать документ**.</span><span class="sxs-lookup"><span data-stu-id="1ef09-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![Рабочая область управления бизнес-документами](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="1ef09-120">В диалоговом окне выберите документ для используемого шаблона и выберите **Создать документ**.</span><span class="sxs-lookup"><span data-stu-id="1ef09-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![Диалоговое окно бизнес-документов](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="1ef09-122">В новом диалоговом окне в поле **Заголовок** измените заголовок нужным образом.</span><span class="sxs-lookup"><span data-stu-id="1ef09-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="1ef09-123">Этот текст заголовка будет использоваться для имени новой конфигурации формата ER, которая создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="1ef09-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="1ef09-124">Черновая версия этой конфигурации (**Копия отчета FTI клиента (GER)**), которая будет содержать отредактированный шаблон, будет автоматически помечена для запуска этого формата ER для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="1ef09-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="1ef09-125">Для запуска этого формата ER для любого другого пользователя будет использоваться исходный шаблон из базовой конфигурации формата ER.</span><span class="sxs-lookup"><span data-stu-id="1ef09-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="1ef09-126">В поле **Имя** измените имя первой редакции редактируемого шаблона, которая будет создана автоматически.</span><span class="sxs-lookup"><span data-stu-id="1ef09-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="1ef09-127">В поле **Комментарий** обновите примечания для редакции редактируемого шаблона, которая будет создана автоматически.</span><span class="sxs-lookup"><span data-stu-id="1ef09-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="1ef09-128">Выберите **ОК**, чтобы подтвердить начало процесса редактирования.</span><span class="sxs-lookup"><span data-stu-id="1ef09-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Диалоговое окно создания документа](./media/BDM_overview_new_template3.png)

<span data-ttu-id="1ef09-130">Кнопка **Создать документ** позволяет создавать и изменять шаблоны в конфигурации формата электронной отчетности, предоставляемой другим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="1ef09-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="1ef09-131">В этом примере поставщиком является Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1ef09-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="1ef09-132">При выборе **Создать документ** отображаются все шаблоны, принадлежащие текущим и другим поставщикам.</span><span class="sxs-lookup"><span data-stu-id="1ef09-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="1ef09-133">После выбора шаблона он будет открыт для редактирования.</span><span class="sxs-lookup"><span data-stu-id="1ef09-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="1ef09-134">Измененный шаблон будет затем сохранен в новой конфигурации формата ER, которая создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="1ef09-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="1ef09-135">Дополнительные сведения см. в разделе [Обзор управления бизнес-документами](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="1ef09-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>
