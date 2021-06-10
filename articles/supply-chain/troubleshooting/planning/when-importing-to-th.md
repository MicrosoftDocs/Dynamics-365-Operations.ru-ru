---
title: Вам предлагается сохранить параметры покрытия номенклатуры даже в том случае, если изменения не были внесены
description: Вам предлагается сохранить параметры покрытия номенклатуры даже в том случае, если изменения не были внесены.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049486"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="e9606-103">Вам предлагается сохранить параметры покрытия номенклатуры даже в том случае, если изменения не были внесены</span><span class="sxs-lookup"><span data-stu-id="e9606-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="e9606-104">Номер статьи базы знаний: 4615588</span><span class="sxs-lookup"><span data-stu-id="e9606-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="e9606-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="e9606-105">Symptoms</span></span>

<span data-ttu-id="e9606-106">В некоторых сценариях при открытии страницы **Покрытие номенклатуры** после импорта номенклатур через сущность *Покрытие номенклатуры v2* может появиться следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="e9606-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="e9606-107">Сохранить изменения перед закрытием?</span><span class="sxs-lookup"><span data-stu-id="e9606-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="e9606-108">Это сообщение появляется даже в том случае, если изменения не внесены.</span><span class="sxs-lookup"><span data-stu-id="e9606-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="e9606-109">Решение</span><span class="sxs-lookup"><span data-stu-id="e9606-109">Resolution</span></span>

<span data-ttu-id="e9606-110">Страница **Покрытие номенклатуры** содержит сложную логику по умолчанию, которая может привести к показу сообщения после того, как в базе данных недавно были сделаны прямые изменения, например, через импорт сущностей.</span><span class="sxs-lookup"><span data-stu-id="e9606-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="e9606-111">Например, поле сущности `AREGENERALSETTINGSOVERRIDDEN` имеет значение *Нет*, но вы импортируете файл, предоставляющий новые или измененные значения полей, таких как `PRODUCTCOVERAGEGROUPID` и/или `VENDORACCOUNTNUMBER`.</span><span class="sxs-lookup"><span data-stu-id="e9606-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="e9606-112">В этом случае, поскольку в поле `AREGENERALSETTINGSOVERRIDDEN` установлено значение *Нет*, эти значения автоматически очищаются из полей при открытии страницы **Покрытие номенклатуры** в первый раз после импорта.</span><span class="sxs-lookup"><span data-stu-id="e9606-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="e9606-113">Если сохранить изменения, как предлагается в окне сообщения, они сохраняются в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e9606-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="e9606-114">В противном случае это же сообщение будет получено при следующем открытии страницы.</span><span class="sxs-lookup"><span data-stu-id="e9606-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="e9606-115">Чтобы не допустить такого поведения, но также включить значения для полей, таких как `PRODUCTCOVERAGEGROUPID`, через импорт сущностей, установите в поле `AREGENERALSETTINGSOVERRIDDEN` значение *Да* при импорте.</span><span class="sxs-lookup"><span data-stu-id="e9606-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
