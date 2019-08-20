---
title: Обзор расширенной банковской выверки
description: Эта статья описывает поток для предварительного процесса банковской выверки. Функция расширенной банковской выверки позволяет импортировать банковские выписки, которые можно автоматически выверять из банковских проводок.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c76b38e957c1c76a80c76782f45405573b7f191
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842625"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="91c14-104">Обзор расширенной банковской выверки</span><span class="sxs-lookup"><span data-stu-id="91c14-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91c14-105">Эта статья описывает поток для предварительного процесса банковской выверки.</span><span class="sxs-lookup"><span data-stu-id="91c14-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="91c14-106">Функция расширенной банковской выверки позволяет импортировать банковские выписки, которые можно автоматически выверять из банковских проводок.</span><span class="sxs-lookup"><span data-stu-id="91c14-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="91c14-107">Функция расширенной банковской выверки позволяет вам импортировать банковские выписки.</span><span class="sxs-lookup"><span data-stu-id="91c14-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="91c14-108">Импортированную банковскую выписку можно после этого автоматически выверить их банковских проводок.</span><span class="sxs-lookup"><span data-stu-id="91c14-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="91c14-109">Вот шаги процесса расширенной банковской выверки.</span><span class="sxs-lookup"><span data-stu-id="91c14-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="91c14-110">Настройка импорта банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="91c14-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="91c14-111">Импортируйте банковские выписки через структуру информационного объекта.</span><span class="sxs-lookup"><span data-stu-id="91c14-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="91c14-112">Встроены три типичных формата банковской выписки: ISO20022, BAI2 и MT940.</span><span class="sxs-lookup"><span data-stu-id="91c14-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="91c14-113">Функциональность можно расширить до любого формата.</span><span class="sxs-lookup"><span data-stu-id="91c14-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="91c14-114">Настройте номерную серию для использования для расширенной банковской выверки, и определите правила сопоставления банковской выверки.</span><span class="sxs-lookup"><span data-stu-id="91c14-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="91c14-115">Правило сопоставления выверки — это набор критериев, используемых при фильтрации строк банковской выписки и строк банковской проводки Microsoft Dynamics 365 for Finance and Operations во время процесса выверки.</span><span class="sxs-lookup"><span data-stu-id="91c14-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="91c14-116">В зависимости от вашей методики ведения бизнеса можно настроить более одного правила сопоставления, чтобы автоматизировать и оптимизировать процесс сверки.</span><span class="sxs-lookup"><span data-stu-id="91c14-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="91c14-117">Выверите банковские выписки с банковскими проводками Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="91c14-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="91c14-118">Выполните автоматические сопоставление и создание журналов выверки.</span><span class="sxs-lookup"><span data-stu-id="91c14-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="91c14-119">Просмотр банковских выписок с банковскими проводками Finance and Operations друг рядом с другом.</span><span class="sxs-lookup"><span data-stu-id="91c14-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="91c14-120">Автоматическая разноска банковских проводок Finance and Operations, если они появляются в банковской выписке, но не появились в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="91c14-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="91c14-121">Создать выписку выверки.</span><span class="sxs-lookup"><span data-stu-id="91c14-121">Generate a reconciliation statement.</span></span>





