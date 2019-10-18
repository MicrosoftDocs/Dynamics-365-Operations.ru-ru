---
title: Включение отсроченного расчета налога для журнала
description: В этой теме объясняется, как использовать функцию **Включить отсроченный расчет налога для журнала**, чтобы повысить производительность расчета налога, когда объем строк журнала является огромным.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179554"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="7428f-103">Включение отсроченного расчета налога для журнала</span><span class="sxs-lookup"><span data-stu-id="7428f-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="7428f-104">В этой теме объясняется, как использовать функцию **Включить отсроченный расчет налога для журнала**, чтобы повысить производительность расчета налога, когда объем строк журнала является огромным.</span><span class="sxs-lookup"><span data-stu-id="7428f-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="7428f-105">Текущее поведение расчета налога в журнале запускается в режиме реального времени, когда пользователь обновляет поля, соответствующие налогам, например, налоговая группа/налоговая группа номенклатур.</span><span class="sxs-lookup"><span data-stu-id="7428f-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="7428f-106">Любое обновление на уровне строки журнала приводит к пересчету суммы налога во всех строках журнала.</span><span class="sxs-lookup"><span data-stu-id="7428f-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="7428f-107">Он позволяет пользователю просмотреть сумму рассчитанного налога в реальном времени, но может также привести к снижению производительности, если объем строк журнала является огромным.</span><span class="sxs-lookup"><span data-stu-id="7428f-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="7428f-108">Эта функция предоставляет возможность отложенного расчета налогов для решения проблем с производительностью.</span><span class="sxs-lookup"><span data-stu-id="7428f-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="7428f-109">Если эта функция включена, сумма налога будет вычисляться только тогда, когда пользователь нажимает команду "Налог" или разносит журнал.</span><span class="sxs-lookup"><span data-stu-id="7428f-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="7428f-110">Пользователь может включить/отключить параметр на трех уровнях:</span><span class="sxs-lookup"><span data-stu-id="7428f-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="7428f-111">По юридическому лицу</span><span class="sxs-lookup"><span data-stu-id="7428f-111">By legal entity</span></span>
- <span data-ttu-id="7428f-112">По наименованию журнала</span><span class="sxs-lookup"><span data-stu-id="7428f-112">By journal name</span></span>
- <span data-ttu-id="7428f-113">По заголовку журнала</span><span class="sxs-lookup"><span data-stu-id="7428f-113">By journal header</span></span>

<span data-ttu-id="7428f-114">Система принимает значение параметра в заголовке журнала как окончательное.</span><span class="sxs-lookup"><span data-stu-id="7428f-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="7428f-115">Значение параметра в заголовке журнала по умолчанию используется из наименования журнала.</span><span class="sxs-lookup"><span data-stu-id="7428f-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="7428f-116">При создании наименования журнала значение параметра для наименования журнала по умолчанию берется из параметра главной книги.</span><span class="sxs-lookup"><span data-stu-id="7428f-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="7428f-117">Поля "Фактическая сумма налога" и "Рассчитанная сумма налога" в журнале будут скрыты, если этот параметр включен.</span><span class="sxs-lookup"><span data-stu-id="7428f-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="7428f-118">Это сделано, чтобы не путать пользователя, поскольку значение этих двух полей всегда будет показывать 0, пока расчет налога не будет запущен пользователем.</span><span class="sxs-lookup"><span data-stu-id="7428f-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="7428f-119">Включение отсроченного расчета налога по юридическим лицам</span><span class="sxs-lookup"><span data-stu-id="7428f-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="7428f-120">Перейдите в раздел **Главная книга > Настройка главной книги > Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="7428f-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="7428f-121">Откройте вкладку **Налог**</span><span class="sxs-lookup"><span data-stu-id="7428f-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="7428f-122">На экспресс-вкладке **Общие** найдите параметр **Отсроченный расчет налога**, включите или выключите его</span><span class="sxs-lookup"><span data-stu-id="7428f-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="7428f-123">Включение отсроченного расчета налога по наименованию журнала</span><span class="sxs-lookup"><span data-stu-id="7428f-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="7428f-124">Перейдите в раздел **Главная книга > Настройка журнала > Наименования журналов**.</span><span class="sxs-lookup"><span data-stu-id="7428f-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="7428f-125">На экспресс-вкладке **Общие** найдите параметр **Отсроченный расчет налога**, включите или выключите его</span><span class="sxs-lookup"><span data-stu-id="7428f-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="7428f-126">Включение отсроченного расчета налога по журналам</span><span class="sxs-lookup"><span data-stu-id="7428f-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="7428f-127">Перейдите в раздел **Главная книга > Записи в журнале > Общие журналы**</span><span class="sxs-lookup"><span data-stu-id="7428f-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="7428f-128">Щелкните **Создать**</span><span class="sxs-lookup"><span data-stu-id="7428f-128">Click **New**</span></span>
3. <span data-ttu-id="7428f-129">Выберите название журнала</span><span class="sxs-lookup"><span data-stu-id="7428f-129">Select a journal name</span></span>
4. <span data-ttu-id="7428f-130">Щелкните **Настройка**</span><span class="sxs-lookup"><span data-stu-id="7428f-130">Click **Setup**</span></span>
5. <span data-ttu-id="7428f-131">Найдите параметр **Отсроченный расчет налога**, включите или выключите его</span><span class="sxs-lookup"><span data-stu-id="7428f-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
