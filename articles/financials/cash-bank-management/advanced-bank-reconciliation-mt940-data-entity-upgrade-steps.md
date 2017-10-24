---
title: "Импорт расширенной банковской выверки MT940 — обновление составного информационного объекта"
description: "Порядковый номер должен быть добавлен в объект импорта банковской выписки для поддержки формата MT940."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0fb86cd4264d5420c479e14f7eed41e480c88b63
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="02d3e-103">Импорт расширенной банковской выверки MT940 — обновление составного информационного объекта</span><span class="sxs-lookup"><span data-stu-id="02d3e-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="02d3e-104">Порядковый номер должен быть добавлен в объект импорта банковской выписки для поддержки формата MT940.</span><span class="sxs-lookup"><span data-stu-id="02d3e-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="02d3e-105">Следующие шаги используются для добавления объекта импорта банковской выписки для поддержки формата MT940.</span><span class="sxs-lookup"><span data-stu-id="02d3e-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="02d3e-106">Выполните компиляцию и синхронизацию следующего:</span><span class="sxs-lookup"><span data-stu-id="02d3e-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="02d3e-107">Составной объект\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="02d3e-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="02d3e-108">Объект\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="02d3e-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="02d3e-109">Объект\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="02d3e-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="02d3e-110">Объект\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="02d3e-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="02d3e-111">Объект\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="02d3e-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="02d3e-112">Таблицы\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="02d3e-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="02d3e-113">Управление данными\\проекты данных.</span><span class="sxs-lookup"><span data-stu-id="02d3e-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="02d3e-114">Загрузка проектов импорта MT940</span><span class="sxs-lookup"><span data-stu-id="02d3e-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="02d3e-115">Измените XSLT.</span><span class="sxs-lookup"><span data-stu-id="02d3e-115">Change XSLT.</span></span>
            -   <span data-ttu-id="02d3e-116">Щелкните **Просмотр карты**.</span><span class="sxs-lookup"><span data-stu-id="02d3e-116">Click **View map**.</span></span>
            -   <span data-ttu-id="02d3e-117">Щелкните **Просмотр карты** на документе банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="02d3e-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="02d3e-118">Щелкните **Преобразования**</span><span class="sxs-lookup"><span data-stu-id="02d3e-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="02d3e-119">Удалите файл BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="02d3e-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="02d3e-120">Добавьте новую версию файла BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="02d3e-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="02d3e-121">Выведите **Порядковый номер** в макете **Исходные данные**.</span><span class="sxs-lookup"><span data-stu-id="02d3e-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="02d3e-122">Формат исходных данных = XML-элемент.</span><span class="sxs-lookup"><span data-stu-id="02d3e-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="02d3e-123">Имя объекта = Банковские выписки.</span><span class="sxs-lookup"><span data-stu-id="02d3e-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="02d3e-124">Отправите файл данных = новая версия SampleBankCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="02d3e-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="02d3e-125">Нажмите кнопку **Да**, чтобы перезаписать существующий файл.</span><span class="sxs-lookup"><span data-stu-id="02d3e-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="02d3e-126">Нажмите **Да** для создания нового сопоставления.</span><span class="sxs-lookup"><span data-stu-id="02d3e-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="02d3e-127">Убедитесь, что **SequenceNumber** сопоставлен.</span><span class="sxs-lookup"><span data-stu-id="02d3e-127">Verify that S **equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="02d3e-128">Щелкните **Просмотр карты** на объекте выписки.</span><span class="sxs-lookup"><span data-stu-id="02d3e-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="02d3e-129">Убедитесь, что **SequenceNumber** составлен с "Источник" на "Промежуточное хранение".</span><span class="sxs-lookup"><span data-stu-id="02d3e-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="02d3e-130">Импортируйте новую выписку.</span><span class="sxs-lookup"><span data-stu-id="02d3e-130">Import the new statement.</span></span>





