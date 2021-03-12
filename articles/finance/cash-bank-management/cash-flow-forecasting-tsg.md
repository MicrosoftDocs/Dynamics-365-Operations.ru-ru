---
title: Устранение неполадок настройки прогноза движения денежных средств
description: Эта тема содержит ответы на вопросы, которые могут возникнуть при настройке прогноза движения денежных средств. В нем приводиться ответы на часто задаваемые вопросы о настройке движения денежных средств, обновления движения денежных средств и движения денежных средств в Power BI.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985295"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="43fcf-104">Устранение неполадок настройки прогноза движения денежных средств</span><span class="sxs-lookup"><span data-stu-id="43fcf-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43fcf-105">Эта тема содержит ответы на вопросы, которые могут возникнуть при настройке прогноза движения денежных средств.</span><span class="sxs-lookup"><span data-stu-id="43fcf-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="43fcf-106">В нем приводиться ответы на часто задаваемые вопросы о настройке движения денежных средств, обновления движения денежных средств и движения денежных средств в Power BI.</span><span class="sxs-lookup"><span data-stu-id="43fcf-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="43fcf-107">Почему движение денежных средств отображается только для одного юридического лица?</span><span class="sxs-lookup"><span data-stu-id="43fcf-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="43fcf-108">Прогноз движения денежных средств настраивается и рассчитывается для каждого юридического лица.</span><span class="sxs-lookup"><span data-stu-id="43fcf-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="43fcf-109">Power BI сообщает, а возможность прогнозов движения денежных средств в Finance Insights показывает результаты.</span><span class="sxs-lookup"><span data-stu-id="43fcf-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="43fcf-110">Прогнозирование движения денежных средств должно быть настроено для каждого юридического лица, для которого требуется просмотреть прогноз.</span><span class="sxs-lookup"><span data-stu-id="43fcf-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="43fcf-111">Проверьте настройку прогноза движения денежных средств во всех юридических лицах.</span><span class="sxs-lookup"><span data-stu-id="43fcf-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="43fcf-112">В качестве альтернативы проверьте конфигурацию всех юридических лиц для прогноза движения денежных средств и убедитесь, что они настроены так, как вы хотели.</span><span class="sxs-lookup"><span data-stu-id="43fcf-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="43fcf-113">Почему в Power BI не отображаются все данные о движении денежных средств?</span><span class="sxs-lookup"><span data-stu-id="43fcf-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="43fcf-114">Перед тем как прогнозы движения денежных средств могут отображаться в представлениях Power BI, необходимо выполнить несколько шагов.</span><span class="sxs-lookup"><span data-stu-id="43fcf-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="43fcf-115">Просмотрите следующий контрольный список и убедитесь, что все этапы завершены:</span><span class="sxs-lookup"><span data-stu-id="43fcf-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="43fcf-116">Настройте движение денежных средств для каждого юридического лица.</span><span class="sxs-lookup"><span data-stu-id="43fcf-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="43fcf-117">В параметрах главной книги настройте валюту системы и тип валютного курса системы.</span><span class="sxs-lookup"><span data-stu-id="43fcf-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="43fcf-118">Настройте валюту учета ГК и тип валютного курса.</span><span class="sxs-lookup"><span data-stu-id="43fcf-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="43fcf-119">Введите валютные курсы между валютой проводки и валютой учета.</span><span class="sxs-lookup"><span data-stu-id="43fcf-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="43fcf-120">Введите валютные курсы между валютой учета и валютой системы.</span><span class="sxs-lookup"><span data-stu-id="43fcf-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="43fcf-121">Введите валютные курсы между валютой учета и каждой из банковских валют.</span><span class="sxs-lookup"><span data-stu-id="43fcf-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="43fcf-122">Почему в предыдущих версиях движение денежных средств Power BI работает, но теперь оно пусто?</span><span class="sxs-lookup"><span data-stu-id="43fcf-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="43fcf-123">Убедитесь, что в хранилище сущностей настроены измерения "Измерение движения денежных средств V2" и "LedgerCovLiquidityMeasurement".</span><span class="sxs-lookup"><span data-stu-id="43fcf-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="43fcf-124">Дополнительные сведения о работе с данными в хранилище сущностей см. в разделе [Интеграция Power BI с хранилищем сущностей](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Убедитесь, что выполнены все шаги, необходимые для просмотра содержимого Power BI.</span><span class="sxs-lookup"><span data-stu-id="43fcf-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="43fcf-125">Дополнительные сведения см. в разделе [Содержимое Power BI "Обзор кассы"](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="43fcf-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="43fcf-126">Были ли сущности хранилища сущностей обновлены?</span><span class="sxs-lookup"><span data-stu-id="43fcf-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="43fcf-127">Необходимо периодически обновлять сущности, чтобы гарантировать актуальность и точность данных.</span><span class="sxs-lookup"><span data-stu-id="43fcf-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="43fcf-128">Чтобы вручную обновить конкретную сущность, перейдите в раздел **Администрирование системы \> Настройка \> Хранилище сущностей**, выберите сущность, затем выберите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="43fcf-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="43fcf-129">Данные также могут быть обновлены автоматически.</span><span class="sxs-lookup"><span data-stu-id="43fcf-129">The data can also be updated automatically.</span></span> <span data-ttu-id="43fcf-130">На странице **Хранилище сущностей** задайте для параметра **Автоматическое обновление включено** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="43fcf-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>
