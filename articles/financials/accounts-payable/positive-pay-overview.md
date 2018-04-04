---
title: "Обзор положительного платежа"
description: "В этой статье приводятся сведения о положительном плате, используемом для формирования электронного списка чеков, которые можно предоставить банку."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 13a7a842e7b4522b508a34fdf86bb3bf58a0845f
ms.contentlocale: ru-ru
ms.lasthandoff: 03/26/2018

---

# <a name="positive-pay-overview"></a><span data-ttu-id="d2d49-103">Обзор положительного платежа</span><span class="sxs-lookup"><span data-stu-id="d2d49-103">Positive pay overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d2d49-104">В этой статье приводятся сведения о положительном плате, используемом для формирования электронного списка чеков, которые можно предоставить банку.</span><span class="sxs-lookup"><span data-stu-id="d2d49-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="d2d49-105">Положительный платеж используется для формирования электронного списка чеков, которые можно предоставить банку.</span><span class="sxs-lookup"><span data-stu-id="d2d49-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="d2d49-106">Файлы положительных платежей помогут помочь банкам предотвратить мошенничество с чеками.</span><span class="sxs-lookup"><span data-stu-id="d2d49-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="d2d49-107">Можно настроить положительный платеж для формирования электронного списка чеков при каждой печати чеков.</span><span class="sxs-lookup"><span data-stu-id="d2d49-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="d2d49-108">Затем, когда чек передается в банк, банк сравнивает чек со списком чеков, представленным ранее.</span><span class="sxs-lookup"><span data-stu-id="d2d49-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="d2d49-109">Если чек соответствует чеку в списке, банк производит клиринг чека.</span><span class="sxs-lookup"><span data-stu-id="d2d49-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="d2d49-110">Если чек не соответствует чеку в списке, банк отправляет чек на рассмотрение.</span><span class="sxs-lookup"><span data-stu-id="d2d49-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="d2d49-111">Положительная оплата также называется SafePay.</span><span class="sxs-lookup"><span data-stu-id="d2d49-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="d2d49-112">Файлы положительных платежей могут содержать конфиденциальные сведения о получателях и суммах чеков.</span><span class="sxs-lookup"><span data-stu-id="d2d49-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="d2d49-113">Поэтому убедитесь, что вы используете соответствующие меры безопасности со времени создания файлов и до получения файлов банком.</span><span class="sxs-lookup"><span data-stu-id="d2d49-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="d2d49-114">Файлы положительных платежей загружаются согласно инструкциям по загрузке для веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="d2d49-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="d2d49-115">Файлы положительных платежей создаются с помощью записей данных.</span><span class="sxs-lookup"><span data-stu-id="d2d49-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="d2d49-116">Перед созданием файла положительного платежа необходимо настроить форматы преобразования для XML, который переводит данные в формат, который банк может использовать.</span><span class="sxs-lookup"><span data-stu-id="d2d49-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="d2d49-117">Для каждого банковского счета, для которого требуется создать информацию о положительных платежах, необходимо назначить формат положительных платежей.</span><span class="sxs-lookup"><span data-stu-id="d2d49-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="d2d49-118">После создания платежей можно создать файл положительных платежей для одного юридического лица и одного банковского счета.</span><span class="sxs-lookup"><span data-stu-id="d2d49-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="d2d49-119">Можно также одновременно создать файлы положительных платежей для нескольких юридических лиц и банковских счетов.</span><span class="sxs-lookup"><span data-stu-id="d2d49-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="d2d49-120">После оплаты чеков, перечисленных в файле положительных платежей, вы получаете номер подтверждения из банка.</span><span class="sxs-lookup"><span data-stu-id="d2d49-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="d2d49-121">Затем можно подтвердить файл положительных платежей в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d2d49-121">You can then confirm the positive pay file in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="d2d49-122">Если необходимо изменить файл положительных платежей, можно отозвать его.</span><span class="sxs-lookup"><span data-stu-id="d2d49-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="d2d49-123">Затем для каждого чека в файле положительных платежей сбрасывается поле, которое указывает, что чек включен в файл положительных платежей.</span><span class="sxs-lookup"><span data-stu-id="d2d49-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="d2d49-124">Дополнительные сведения см. в разделе [Настройка и создание файлов положительных платежей](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="d2d49-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>




