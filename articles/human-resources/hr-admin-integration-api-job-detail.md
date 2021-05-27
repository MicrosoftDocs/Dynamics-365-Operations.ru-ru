---
title: API Сведения о должности
description: В этом разделе представлены сведения и пример запроса для сущности сведений о должности в Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c92b0636fbd68c6ee7eded90a8cb5bcd0cda7ca3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018370"
---
# <a name="job-detail-api"></a><span data-ttu-id="8cf6e-103">API Сведения о должности</span><span class="sxs-lookup"><span data-stu-id="8cf6e-103">Job detail API</span></span>

<span data-ttu-id="8cf6e-104">В этом разделе представлены сведения и пример запроса для сущности сведений о должности в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-104">This topic provides details and an example query for the Job detail entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="8cf6e-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="8cf6e-105">Properties</span></span>

| <span data-ttu-id="8cf6e-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="8cf6e-106">Property</span></span><br><span data-ttu-id="8cf6e-107">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="8cf6e-107">**Physical name**</span></span><br><span data-ttu-id="8cf6e-108">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="8cf6e-108">**_Type_**</span></span> | <span data-ttu-id="8cf6e-109">Использование</span><span class="sxs-lookup"><span data-stu-id="8cf6e-109">Use</span></span> | <span data-ttu-id="8cf6e-110">описание</span><span class="sxs-lookup"><span data-stu-id="8cf6e-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8cf6e-111">**Код задания**</span><span class="sxs-lookup"><span data-stu-id="8cf6e-111">**Job ID**</span></span><br><span data-ttu-id="8cf6e-112">mshr_jobid</span><span class="sxs-lookup"><span data-stu-id="8cf6e-112">mshr_jobid</span></span><br><span data-ttu-id="8cf6e-113">*Строка*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-113">*String*</span></span> | <span data-ttu-id="8cf6e-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8cf6e-114">Read-only</span></span><br><span data-ttu-id="8cf6e-115">Требуется</span><span class="sxs-lookup"><span data-stu-id="8cf6e-115">Required</span></span> | <span data-ttu-id="8cf6e-116">Уникальный код задания.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-116">Unique ID for a job.</span></span> |
| <span data-ttu-id="8cf6e-117">**Нижний порог рыночной цены**</span><span class="sxs-lookup"><span data-stu-id="8cf6e-117">**Market price low threshold**</span></span><br><span data-ttu-id="8cf6e-118">mshr_marketpricelowthreshold</span><span class="sxs-lookup"><span data-stu-id="8cf6e-118">mshr_marketpricelowthreshold</span></span><br><span data-ttu-id="8cf6e-119">*Десятичн.*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-119">*Decimal*</span></span> | | <span data-ttu-id="8cf6e-120">Создаваемое системой значение GUID для уникальной идентификации должности.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-120">A system-generated GUID value to uniquely identify the position.</span></span>  |
