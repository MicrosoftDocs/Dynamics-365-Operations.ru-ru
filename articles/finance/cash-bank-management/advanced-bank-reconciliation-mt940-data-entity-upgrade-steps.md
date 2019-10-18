---
title: Импорт расширенной банковской выверки MT940 — обновление составного информационного объекта
description: Порядковый номер должен быть добавлен в объект импорта банковской выписки для поддержки формата MT940.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: 88eb5b3c408d36620ab550b29d2e5a3278d25d8a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188472"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="feb97-103">Импорт расширенной банковской выверки MT940 — обновление составного информационного объекта</span><span class="sxs-lookup"><span data-stu-id="feb97-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="feb97-104">Порядковый номер должен быть добавлен в объект импорта банковской выписки для поддержки формата MT940.</span><span class="sxs-lookup"><span data-stu-id="feb97-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="feb97-105">Следующие шаги используются для добавления объекта импорта банковской выписки для поддержки формата MT940.</span><span class="sxs-lookup"><span data-stu-id="feb97-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="feb97-106">Выполните компиляцию и синхронизацию следующего:</span><span class="sxs-lookup"><span data-stu-id="feb97-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="feb97-107">Составной объект\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="feb97-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="feb97-108">Объект\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="feb97-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="feb97-109">Объект\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="feb97-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="feb97-110">Объект\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="feb97-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="feb97-111">Объект\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="feb97-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="feb97-112">Таблицы\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="feb97-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="feb97-113">Управление данными\\проекты данных.</span><span class="sxs-lookup"><span data-stu-id="feb97-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="feb97-114">Загрузка проектов импорта MT940</span><span class="sxs-lookup"><span data-stu-id="feb97-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="feb97-115">Измените XSLT.</span><span class="sxs-lookup"><span data-stu-id="feb97-115">Change XSLT.</span></span>
            -   <span data-ttu-id="feb97-116">Щелкните **Просмотр карты**.</span><span class="sxs-lookup"><span data-stu-id="feb97-116">Click **View map**.</span></span>
            -   <span data-ttu-id="feb97-117">Щелкните **Просмотр карты** на документе банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="feb97-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="feb97-118">Щелкните **Преобразования**</span><span class="sxs-lookup"><span data-stu-id="feb97-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="feb97-119">Удалите файл BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="feb97-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="feb97-120">Добавьте новую версию файла BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="feb97-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="feb97-121">Выведите **Порядковый номер** в макете **Исходные данные**.</span><span class="sxs-lookup"><span data-stu-id="feb97-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="feb97-122">Формат исходных данных = XML-элемент.</span><span class="sxs-lookup"><span data-stu-id="feb97-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="feb97-123">Имя объекта = Банковские выписки.</span><span class="sxs-lookup"><span data-stu-id="feb97-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="feb97-124">Отправите файл данных = новая версия SampleBankCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="feb97-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="feb97-125">Нажмите кнопку **Да**, чтобы перезаписать существующий файл.</span><span class="sxs-lookup"><span data-stu-id="feb97-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="feb97-126">Нажмите **Да** для создания нового сопоставления.</span><span class="sxs-lookup"><span data-stu-id="feb97-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="feb97-127">Убедитесь, что **SequenceNumber** сопоставлен.</span><span class="sxs-lookup"><span data-stu-id="feb97-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="feb97-128">Щелкните **Просмотр карты** на объекте выписки.</span><span class="sxs-lookup"><span data-stu-id="feb97-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="feb97-129">Убедитесь, что **SequenceNumber** составлен с "Источник" на "Промежуточное хранение".</span><span class="sxs-lookup"><span data-stu-id="feb97-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="feb97-130">Импортируйте новую выписку.</span><span class="sxs-lookup"><span data-stu-id="feb97-130">Import the new statement.</span></span>




