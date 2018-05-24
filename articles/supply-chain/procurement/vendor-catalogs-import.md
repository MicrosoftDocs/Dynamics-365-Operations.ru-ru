---
title: "Импорт каталогов поставщиков"
description: "В этом разделе описывается процедура импорта данных каталогов поставщиков."
author: mkirknel
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: 
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: ac7754bd6361ad74f7ab4d564ae3114dd4b9f165
ms.openlocfilehash: caf801ea27ade63c24bb0907313e7f8294c50702
ms.contentlocale: ru-ru
ms.lasthandoff: 04/26/2018

---

# <a name="import-vendor-catalogs"></a><span data-ttu-id="6fe57-103">Импорт каталогов поставщиков</span><span class="sxs-lookup"><span data-stu-id="6fe57-103">Import vendor catalogs</span></span>
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="6fe57-104">Импорт каталогов поставщиков</span><span class="sxs-lookup"><span data-stu-id="6fe57-104">Vendor catalogs import</span></span>

<span data-ttu-id="6fe57-105">В Microsoft Dynamics 365 for Finance and Operations специалисты по закупкам могут создавать и вести каталоги, которые сотрудники компании, в свою очередь, могут использовать для заказа товаров и услуг для внутреннего пользования.</span><span class="sxs-lookup"><span data-stu-id="6fe57-105">In Microsoft Dynamics 365 for Finance and Operations, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="6fe57-106">Для создания каталога закупаемой продукции номенклатуры и услуги, которые требуется сделать доступными для сотрудников, можно добавить либо путем импорта данных каталога продуктов, либо путем ручного добавления данных из каталогов продуктов в основной список товаров.</span><span class="sxs-lookup"><span data-stu-id="6fe57-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="6fe57-107">Данные каталога, предоставленные поставщиком, можно отправить из клиента Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6fe57-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="6fe57-108">Данные о продукции, передаваемые вам поставщиком в виде файла обновления каталога, должны быть в формате XML-файла.</span><span class="sxs-lookup"><span data-stu-id="6fe57-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="6fe57-109">Файл обновления каталога должен содержать сведения о продукции, которую поставщик поставляет вашей компании.</span><span class="sxs-lookup"><span data-stu-id="6fe57-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="6fe57-110">Импорт данных каталога поставщика</span><span class="sxs-lookup"><span data-stu-id="6fe57-110">Import vendor catalog data</span></span>

<span data-ttu-id="6fe57-111">Чтобы импортировать данные каталога поставщика, необходимо выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="6fe57-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1.  <span data-ttu-id="6fe57-112">Настройте проект в рабочей области управления данными, где определены правила сопоставления данных.</span><span class="sxs-lookup"><span data-stu-id="6fe57-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="6fe57-113">Выберите **Управление данными**, затем выберите **Настройка ролей для проектов данных**.</span><span class="sxs-lookup"><span data-stu-id="6fe57-113">Select **Data management** and then select **Set up roles for data projects**.</span></span> 

2.  <span data-ttu-id="6fe57-114">Настроить иерархию категорий закупаемой продукции и назначить имеющихся поставщиков категориям закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="6fe57-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="6fe57-115">Если используются товарные коды, необходимо добавить товарные коды в категории закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="6fe57-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="6fe57-116">Сведения о настройке иерархии категорий закупаемой продукции см. в разделе [Настройка иерархии категорий закупаемой продукции](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="6fe57-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3.  <span data-ttu-id="6fe57-117">Настроить поставщика для импорта каталога.</span><span class="sxs-lookup"><span data-stu-id="6fe57-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="6fe57-118">Выберите поставщика, затем выберите **Закупки** > **Настройка** > **Настроить поставщика для импорта каталога**.</span><span class="sxs-lookup"><span data-stu-id="6fe57-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4.  <span data-ttu-id="6fe57-119">Настроить workflow-процесс для импорта каталогов.</span><span class="sxs-lookup"><span data-stu-id="6fe57-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="6fe57-120">Создайте шаблон файла CMR и предоставьте его поставщику.</span><span class="sxs-lookup"><span data-stu-id="6fe57-120">Create a CMR file template and share this with your vendor.</span></span>

5.  <span data-ttu-id="6fe57-121">Выберите **Закупки и источники** \> **Общее** \> **Каталоги** \> **Каталоги поставщиков** для создания каталога поставщика.</span><span class="sxs-lookup"><span data-stu-id="6fe57-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="6fe57-122">В этом каталоге группируются файлы обновления каталога, получаемые от поставщика.</span><span class="sxs-lookup"><span data-stu-id="6fe57-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6.  <span data-ttu-id="6fe57-123">Отправить файл обновления каталога в систему.</span><span class="sxs-lookup"><span data-stu-id="6fe57-123">Upload the CMR file.</span></span>

7.  <span data-ttu-id="6fe57-124">Просмотреть, утвердить или отклонить продукты в каталоге поставщика.</span><span class="sxs-lookup"><span data-stu-id="6fe57-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="6fe57-125">Продукты автоматически сопоставляются с категориями закупок в Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6fe57-125">The products are automatically mapped to the procurement categories in Dynamics 365 for Finance and Operations.</span></span> 
    
<span data-ttu-id="6fe57-126">Утвержденные продукты добавляются в основной список товаров и становятся доступными выбранным юридическим лицам.</span><span class="sxs-lookup"><span data-stu-id="6fe57-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="6fe57-127">Добавить в каталог закупаемой продукции можно только утвержденные продукты.</span><span class="sxs-lookup"><span data-stu-id="6fe57-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="6fe57-128">Создание шаблона файла импорта каталога</span><span class="sxs-lookup"><span data-stu-id="6fe57-128">Generate a catalog import file template</span></span>

<span data-ttu-id="6fe57-129">Шаблон файла импорта каталога является XSD-файлом, который используется для создания файла CMR для продуктов поставщика.</span><span class="sxs-lookup"><span data-stu-id="6fe57-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor’s products.</span></span> <span data-ttu-id="6fe57-130">Можно использовать файл CMR для создания нового каталога, замены существующего каталога и изменения существующего каталога.</span><span class="sxs-lookup"><span data-stu-id="6fe57-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1.  <span data-ttu-id="6fe57-131">Выберите **Закупки и источники** \> **Каталоги** \> **Каталоги поставщиков** и дважды щелкните каталог, с которым требуется работать.</span><span class="sxs-lookup"><span data-stu-id="6fe57-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor catalogs** and double-click the catalog that you want to work with.</span></span>

2.  <span data-ttu-id="6fe57-132">Загрузите шаблон импорта текущего каталога (XSD-файл).</span><span class="sxs-lookup"><span data-stu-id="6fe57-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="6fe57-133">На странице **Обновить каталог** в области **Панель операций** на вкладке **Каталоги** в группе **Связанные сведения** щелкните **Создать шаблон каталога** и выберите **Категория закупаемой продукции**.</span><span class="sxs-lookup"><span data-stu-id="6fe57-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    -   <span data-ttu-id="6fe57-134">С помощью варианта **Категория закупаемой продукции** можно создать шаблон каталога, который содержит категории закупаемой продукции, которую поставщик уполномочен поставлять.</span><span class="sxs-lookup"><span data-stu-id="6fe57-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="6fe57-135">В диалоговом окне **Сохранить как** выберите расположение, в котором следует сохранить файл шаблона каталога, и сохраните файл.</span><span class="sxs-lookup"><span data-stu-id="6fe57-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="6fe57-136">Дополнительные сведения и примеры см. в этой записи блога: [Каталоги поставщиков в Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="6fe57-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>

