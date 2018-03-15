---
title: "Импорт данных из шаблонов информационных объектов Excel с несколькими листами"
description: "В этом разделе описывается, как импортировать данные с помощью шаблонов информационных объектов Excel в Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: b314a649829dd14a525923802e19b847dc5a115e
ms.contentlocale: ru-ru
ms.lasthandoff: 02/27/2018

---

# <a name="excel-templates-with-multiple-worksheets"></a><span data-ttu-id="3de72-103">Шаблоны Excel с несколькими листами</span><span class="sxs-lookup"><span data-stu-id="3de72-103">Excel templates with multiple worksheets</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3de72-104">Управление данными в Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition поддерживает шаблоны на основе Microsoft Excel для информационных объектов.</span><span class="sxs-lookup"><span data-stu-id="3de72-104">Data management in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="3de72-105">Эти шаблоны могут содержать один или несколько листов.</span><span class="sxs-lookup"><span data-stu-id="3de72-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="3de72-106">Шаблоны с несколькими листами часто используются, когда удобно управлять данными в одном файле и импортировать их в несколько информационных объектов.</span><span class="sxs-lookup"><span data-stu-id="3de72-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="3de72-107">Примерами могут служить сайты и склады.</span><span class="sxs-lookup"><span data-stu-id="3de72-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="3de72-108">Отправка файла один раз и сопоставление его всем объектам</span><span class="sxs-lookup"><span data-stu-id="3de72-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="3de72-109">Рассмотрим пример, где имеется один файл Excel с листами, которые называются **Сайты** и **Склады**.</span><span class="sxs-lookup"><span data-stu-id="3de72-109">Let’s take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="3de72-110">Чтобы настроить проект импорта данных, следует добавить первый информационный объект, **Сайты**, затем отправить файл.</span><span class="sxs-lookup"><span data-stu-id="3de72-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="3de72-111">Можно будет выбрать **Сайты** в качестве листа, используемого для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="3de72-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="3de72-112">Если вы добавите второй объект **Склады**, не выходя из формы **Добавить файл**, поле подстановки листа позволит выбрать лист **Склады** без необходимости повторной отправки файла.</span><span class="sxs-lookup"><span data-stu-id="3de72-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="3de72-113">Единственная причина отправить новый файл существовала бы, если бы данные **Склады** были в другом файле.</span><span class="sxs-lookup"><span data-stu-id="3de72-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![Несколько листов](./media/AddFileMultipleWorkSheets.png) 

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="3de72-115">Исправление сопоставления листов и объектов</span><span class="sxs-lookup"><span data-stu-id="3de72-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="3de72-116">Сопоставление листа с информационным объектом в задании импорта можно исправить из сетки.</span><span class="sxs-lookup"><span data-stu-id="3de72-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="3de72-117">Столбец **Лист** в сетке отображает листы из файла, которые были сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="3de72-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="3de72-118">В раскрывающемся меню можно выбрать другой лист.</span><span class="sxs-lookup"><span data-stu-id="3de72-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="3de72-119">Если выбранный лист уже сопоставлен объекту в проекте данных, система запрашивает подтверждение изменения.</span><span class="sxs-lookup"><span data-stu-id="3de72-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="3de72-120">Рекомендуется исправить все сопоставления в сетке.</span><span class="sxs-lookup"><span data-stu-id="3de72-120">We recommend that you fix all mappings in the grid.</span></span>

![Обновление сопоставления листов](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="3de72-122">Изменение сопоставления на новый файл</span><span class="sxs-lookup"><span data-stu-id="3de72-122">Re-map to a new file</span></span>

<span data-ttu-id="3de72-123">В случаях, когда новая версия того же файла или совершенно новый файл должен быть отправлен для существующих объектов в проекте данных, необходимо использовать процесс **Добавить файл** и снова добавить объекты, как если бы они добавлялись в первый раз.</span><span class="sxs-lookup"><span data-stu-id="3de72-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="3de72-124">Перед продолжением система запросит подтверждение, что вы хотите перезаписать существующие объекты в проекте данные.</span><span class="sxs-lookup"><span data-stu-id="3de72-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="3de72-125">Объекты, которые не были добавлены повторно (или перезаписаны) сохранят предыдущие сопоставления из предыдущего файла.</span><span class="sxs-lookup"><span data-stu-id="3de72-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="3de72-126">Отправка файла с помощью команды "Выполнить проект"</span><span class="sxs-lookup"><span data-stu-id="3de72-126">Upload a file using Run project</span></span>

<span data-ttu-id="3de72-127">Можно отправить файл Excel при использовании параметра **Выполнить проект** для выполнения проекта импорта.</span><span class="sxs-lookup"><span data-stu-id="3de72-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="3de72-128">Будьте внимательны, чтобы отправить только файлы, имеющие те же листы, что и существующие сопоставления для информационных объектов в проекте данных.</span><span class="sxs-lookup"><span data-stu-id="3de72-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="3de72-129">Если лист отсутствует в новом отправленном файле, система выводит сообщение об ошибке и останавливает импорт.</span><span class="sxs-lookup"><span data-stu-id="3de72-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="3de72-130">Если сопоставление с листом должно быть изменено для объекта, сначала необходимо обновить сопоставления в проекте данных из проекта данных, прежде чем использовать этот файл в процессе **Выполнить проект**.</span><span class="sxs-lookup"><span data-stu-id="3de72-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>


