---
title: Обновление составного объекта журнала банка
description: Следующие шаги требуются, чтобы добавить дополнительное поле BankTransactionType в составной объект BankJournalEntity.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 70db65dca4cfadd1ed8769386b4b437cecc217a2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565934"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="1125c-103">Обновление составного объекта журнала банка</span><span class="sxs-lookup"><span data-stu-id="1125c-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1125c-104">Следующие шаги требуются, чтобы добавить дополнительное поле BankTransactionType в составной объект BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="1125c-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="1125c-105">Используйте следующие шаги, чтобы добавить дополнительное поле BankTransactionType в составной объект BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="1125c-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="1125c-106">Скомпилируйте и синхронизируйте следующие составные объекты, объекты и промежуточные таблицы журнала банка:</span><span class="sxs-lookup"><span data-stu-id="1125c-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="1125c-107">Составной объект\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="1125c-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="1125c-108">Объект\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="1125c-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="1125c-109">Объект\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="1125c-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="1125c-110">Таблица\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="1125c-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="1125c-111">Таблица\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="1125c-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="1125c-112">Управление данными\\проекты данных</span><span class="sxs-lookup"><span data-stu-id="1125c-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="1125c-113">Сделайте доступным тип **Банковская проводка** в макете **Исходные данные**.</span><span class="sxs-lookup"><span data-stu-id="1125c-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="1125c-114">Формат исходных данных = XML-элемент</span><span class="sxs-lookup"><span data-stu-id="1125c-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="1125c-115">Имя объекта = Банковский журнал</span><span class="sxs-lookup"><span data-stu-id="1125c-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="1125c-116">Отправьте файл данных = новая версия SampleBankJournalCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="1125c-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="1125c-117">Нажмите кнопку **Да**, чтобы перезаписать существующий файл.</span><span class="sxs-lookup"><span data-stu-id="1125c-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="1125c-118">Нажмите **Да** для создания сопоставления с самого начала.</span><span class="sxs-lookup"><span data-stu-id="1125c-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="1125c-119">Убедитесь, что тип "Банковская проводка" сопоставлен.</span><span class="sxs-lookup"><span data-stu-id="1125c-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="1125c-120">Щелкните **Просмотр карты** на объекте "Строка".</span><span class="sxs-lookup"><span data-stu-id="1125c-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="1125c-121">Убедитесь, что тип "Банковская проводка" составлен с "Источник" на "Промежуточное хранение".</span><span class="sxs-lookup"><span data-stu-id="1125c-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="1125c-122">Импортируйте новую выписку.</span><span class="sxs-lookup"><span data-stu-id="1125c-122">Import the new statement.</span></span>




