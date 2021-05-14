---
title: Добавление полей данных в налоговые конфигурации
description: В этой теме объясняется, как настроить налоговые конфигурации путем добавления полей данных.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 197a2d1605dd39188841aba02a71d228c7138c54
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921197"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="cb551-103">Добавление полей данных в налоговые конфигурации</span><span class="sxs-lookup"><span data-stu-id="cb551-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb551-104">В этой теме объясняется, как настроить налоговые конфигурации с помощью [полей данных, которые добавляются в налоговую интеграцию](tax-service-add-data-fields-tax-integration-by-extension.md).</span><span class="sxs-lookup"><span data-stu-id="cb551-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="cb551-105">Настройка модели налоговых данных</span><span class="sxs-lookup"><span data-stu-id="cb551-105">Customize the tax data model</span></span>

1. <span data-ttu-id="cb551-106">В Microsoft Dynamics 365 Finance перейдите в раздел **Электронная отчетность** \> **Конфигурации налогов**.</span><span class="sxs-lookup"><span data-stu-id="cb551-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="cb551-107">В дереве конфигурации выберите **Модель налоговых данных — Европа**.</span><span class="sxs-lookup"><span data-stu-id="cb551-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="cb551-108">Затем на панели операций выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="cb551-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="cb551-109">В раскрывающемся диалоговом окне выберите параметр **Модель налогооблагаемого документа, производная от имени: модель налоговых данных — Европа, Microsoft**, введите имя для новой модели налоговой данных, затем выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="cb551-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="cb551-110">Выберите только что созданную модель налоговых данных, затем в области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="cb551-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="cb551-111">Разверните дерево модели данных, выберите **Строки**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="cb551-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="cb551-112">В диалоговом окне **Создание узла** введите имя, укажите тип элемента, а затем нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="cb551-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="cb551-113">Добавьте необходимые столбцы.</span><span class="sxs-lookup"><span data-stu-id="cb551-113">Add any required columns.</span></span>
8. <span data-ttu-id="cb551-114">На панели операций выберите **Сохранить**, затем выберите **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="cb551-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="cb551-115">Закройте страницу и просмотрите завершенную версию модели налоговых данных.</span><span class="sxs-lookup"><span data-stu-id="cb551-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="cb551-116">Настройка конфигурации налогов</span><span class="sxs-lookup"><span data-stu-id="cb551-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="cb551-117">В Finance перейдите в раздел **Электронная отчетность** \> **Конфигурации налогов**.</span><span class="sxs-lookup"><span data-stu-id="cb551-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="cb551-118">В дереве конфигурации выберите **Конфигурация налогов — Европа**.</span><span class="sxs-lookup"><span data-stu-id="cb551-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="cb551-119">Затем на панели операций выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="cb551-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="cb551-120">В раскрывающемся диалоговом окне выберите параметр **Конфигурация налоговой службы, производная от имени: Конфигурация налогов — Европа, Microsoft**, введите имя для новой конфигурации налогов, затем выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="cb551-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="cb551-121">Выберите только что созданную конфигурацию налогов, затем в области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="cb551-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="cb551-122">В разделе **Свойства** в поле **Модель данных** выберите ранее созданную настроенную модель налоговых данных.</span><span class="sxs-lookup"><span data-stu-id="cb551-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="cb551-123">В поле **Версия модели данных** выберите завершенную версию модели налоговых данных.</span><span class="sxs-lookup"><span data-stu-id="cb551-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="cb551-124">Выберите **Добавить** и добавьте требуемые налоговые меры.</span><span class="sxs-lookup"><span data-stu-id="cb551-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="cb551-125">На панели операций выберите **Сохранить**, затем выберите **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="cb551-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="cb551-126">Закройте страницу и просмотрите завершенную версию конфигурации налогов.</span><span class="sxs-lookup"><span data-stu-id="cb551-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="cb551-127">Реализация налоговых функций в настраиваемой конфигурации налогов</span><span class="sxs-lookup"><span data-stu-id="cb551-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="cb551-128">В Regulatory Configuration Services (RCS) перейдите в раздел **Функции глобализации** \> **Налог**.</span><span class="sxs-lookup"><span data-stu-id="cb551-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="cb551-129">Выберите **Добавить**, введите сведения о новой функции, затем выберите **Создать функцию**.</span><span class="sxs-lookup"><span data-stu-id="cb551-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="cb551-130">На вкладке **Версии** выберите функцию, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="cb551-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="cb551-131">На вкладке **Общие** в поле **Версия конфигурации** выберите настраиваемую конфигурацию и версию налога.</span><span class="sxs-lookup"><span data-stu-id="cb551-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="cb551-132">В диалоговом окне **Управление столбцами** выберите заголовок и столбцы строк, которые необходимо включить в настраиваемую налоговую меру, затем выберите кнопку со стрелкой вправо, чтобы добавить их в список **Выбранные столбцы**.</span><span class="sxs-lookup"><span data-stu-id="cb551-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>
