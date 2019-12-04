---
title: Импорт расширенной банковской выверки MT940 — обновление составного информационного объекта
description: Порядковый номер должен быть добавлен в объект импорта банковской выписки для поддержки формата MT940.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 91100c3e3c33462e5b19ca239a784cdb720210ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772015"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="2884b-103">Импорт расширенной банковской выверки MT940 — обновление составного информационного объекта</span><span class="sxs-lookup"><span data-stu-id="2884b-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2884b-104">Порядковый номер должен быть добавлен в объект импорта банковской выписки для поддержки формата MT940.</span><span class="sxs-lookup"><span data-stu-id="2884b-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="2884b-105">Следующие шаги используются для добавления объекта импорта банковской выписки для поддержки формата MT940.</span><span class="sxs-lookup"><span data-stu-id="2884b-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="2884b-106">Выполните компиляцию и синхронизацию следующего:</span><span class="sxs-lookup"><span data-stu-id="2884b-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="2884b-107">Составной объект\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="2884b-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="2884b-108">Объект\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="2884b-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="2884b-109">Объект\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="2884b-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="2884b-110">Объект\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="2884b-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="2884b-111">Объект\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="2884b-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="2884b-112">Таблицы\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="2884b-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="2884b-113">Управление данными\\проекты данных.</span><span class="sxs-lookup"><span data-stu-id="2884b-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="2884b-114">Загрузка проектов импорта MT940</span><span class="sxs-lookup"><span data-stu-id="2884b-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="2884b-115">Измените XSLT.</span><span class="sxs-lookup"><span data-stu-id="2884b-115">Change XSLT.</span></span>
            -   <span data-ttu-id="2884b-116">Щелкните **Просмотр карты**.</span><span class="sxs-lookup"><span data-stu-id="2884b-116">Click **View map**.</span></span>
            -   <span data-ttu-id="2884b-117">Щелкните **Просмотр карты** на документе банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="2884b-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="2884b-118">Щелкните **Преобразования**</span><span class="sxs-lookup"><span data-stu-id="2884b-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="2884b-119">Удалите файл BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="2884b-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="2884b-120">Добавьте новую версию файла BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="2884b-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="2884b-121">Выведите **Порядковый номер** в макете **Исходные данные**.</span><span class="sxs-lookup"><span data-stu-id="2884b-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="2884b-122">Формат исходных данных = XML-элемент.</span><span class="sxs-lookup"><span data-stu-id="2884b-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="2884b-123">Имя объекта = Банковские выписки.</span><span class="sxs-lookup"><span data-stu-id="2884b-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="2884b-124">Отправите файл данных = новая версия SampleBankCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="2884b-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="2884b-125">Нажмите кнопку **Да**, чтобы перезаписать существующий файл.</span><span class="sxs-lookup"><span data-stu-id="2884b-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="2884b-126">Нажмите **Да** для создания нового сопоставления.</span><span class="sxs-lookup"><span data-stu-id="2884b-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="2884b-127">Убедитесь, что **SequenceNumber** сопоставлен.</span><span class="sxs-lookup"><span data-stu-id="2884b-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="2884b-128">Щелкните **Просмотр карты** на объекте выписки.</span><span class="sxs-lookup"><span data-stu-id="2884b-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="2884b-129">Убедитесь, что **SequenceNumber** составлен с "Источник" на "Промежуточное хранение".</span><span class="sxs-lookup"><span data-stu-id="2884b-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="2884b-130">Импортируйте новую выписку.</span><span class="sxs-lookup"><span data-stu-id="2884b-130">Import the new statement.</span></span>




