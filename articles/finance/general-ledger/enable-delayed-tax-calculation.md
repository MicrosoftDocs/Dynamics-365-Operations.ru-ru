---
title: Включение отсроченного расчета налога для журналов
description: В этом разделе объясняется, как включить функцию Отсроченный расчет налога, чтобы повысить производительность расчетов налога, когда число строк журнала является огромным.
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
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d4ce0343ac766b30d532be0866a381dc520fd462
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447304"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="34513-103">Включение отсроченного расчета налога для журналов</span><span class="sxs-lookup"><span data-stu-id="34513-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="34513-104">В этом разделе объясняется, как можно отложить расчет налога по журналам.</span><span class="sxs-lookup"><span data-stu-id="34513-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="34513-105">Эта возможность позволяет улучшить производительность налоговых расчетов, если имеется много строк журнала.</span><span class="sxs-lookup"><span data-stu-id="34513-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="34513-106">По умолчанию суммы налога в строках журнала рассчитываются каждый раз, когда обновляются поля, соответствующие налогам.</span><span class="sxs-lookup"><span data-stu-id="34513-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="34513-107">В эти поля включаются поля для налоговых групп и налоговых групп номенклатур.</span><span class="sxs-lookup"><span data-stu-id="34513-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="34513-108">Любое обновление строки журнала приводит к пересчету налоговых сумм для всех строк журнала.</span><span class="sxs-lookup"><span data-stu-id="34513-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="34513-109">Хотя это позволяет пользователю видеть суммы налога, рассчитанные в реальном времени, это также может повлиять на производительность, если количество строк журнала очень велико.</span><span class="sxs-lookup"><span data-stu-id="34513-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="34513-110">Функция отсроченного расчета налога позволяет отложить расчет налогов по журналам и, таким образом, помочь в устранении проблем с производительностью.</span><span class="sxs-lookup"><span data-stu-id="34513-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="34513-111">Когда эта функция включена, суммы налога будут вычисляться только тогда, когда пользователь выбирает команду **Налог** или разносит журнал.</span><span class="sxs-lookup"><span data-stu-id="34513-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="34513-112">Можно отложить расчет налогов на трех уровнях:</span><span class="sxs-lookup"><span data-stu-id="34513-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="34513-113">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="34513-113">Legal entity</span></span>
- <span data-ttu-id="34513-114">Наименование журнала</span><span class="sxs-lookup"><span data-stu-id="34513-114">Journal name</span></span>
- <span data-ttu-id="34513-115">Заголовок журнала</span><span class="sxs-lookup"><span data-stu-id="34513-115">Journal header</span></span>

<span data-ttu-id="34513-116">Система назначает приоритет параметру для заголовка журнала.</span><span class="sxs-lookup"><span data-stu-id="34513-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="34513-117">По умолчанию этот параметр берется из наименования журнала.</span><span class="sxs-lookup"><span data-stu-id="34513-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="34513-118">По умолчанию значение для наименования журнала берется из настройки на странице **Параметры главной книги** при создании наименования журнала.</span><span class="sxs-lookup"><span data-stu-id="34513-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="34513-119">В следующих разделах объясняется, как включить Отсроченный расчет налога для юридических лиц, наименований журналов и заголовков журналов.</span><span class="sxs-lookup"><span data-stu-id="34513-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="34513-120">Включите Отсроченный расчет налога на уровне юридических лиц</span><span class="sxs-lookup"><span data-stu-id="34513-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="34513-121">Перейдите в раздел **Главная книга \> Настройка главной книги \> Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="34513-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="34513-122">На вкладке **Налог** на экспресс-вкладке **Общие** задайте для параметра **Отсроченный расчет налога** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="34513-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Изображение параметров главной книги](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="34513-124">Включите Отсроченный расчет налога на уровне наименование журнала</span><span class="sxs-lookup"><span data-stu-id="34513-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="34513-125">Перейдите в раздел **Главная книга \> Настройка журнала \> Наименования журналов**.</span><span class="sxs-lookup"><span data-stu-id="34513-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="34513-126">На экспресс-вкладке **Общее** в разделе **Налог** задайте для параметра **Отсроченный расчет налога** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="34513-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Изображение наименований журналов](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="34513-128">Включите Отсроченный расчет налога на уровне заголовка журнала</span><span class="sxs-lookup"><span data-stu-id="34513-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="34513-129">Перейдите к **Главная книга \> Записи в журнале \> Общие журналы**.</span><span class="sxs-lookup"><span data-stu-id="34513-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="34513-130">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="34513-130">Select **New**.</span></span>
3. <span data-ttu-id="34513-131">Выберите название журнала.</span><span class="sxs-lookup"><span data-stu-id="34513-131">Select a journal name.</span></span>
4. <span data-ttu-id="34513-132">На вкладке **Настройка** установите для параметра **Отсроченный расчет налога** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="34513-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Изображение страницы общего журнала](media/delayed-tax-calculation-journal-header.png)
