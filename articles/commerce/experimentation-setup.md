---
title: Настройка эксперимента
description: В этом разделе описывается, как настроить эксперимент в сторонней службе.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0f7db0ce009f6ee7603952891aacfdc16fcde016
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930276"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="6a875-103">Настройка эксперимента</span><span class="sxs-lookup"><span data-stu-id="6a875-103">Set up an experiment</span></span>

<span data-ttu-id="6a875-104">После [определения гипотезы и определения, какие метрики успеха требуется использовать](experimentation-identify.md), необходимо настроить эксперимент в сторонней службе.</span><span class="sxs-lookup"><span data-stu-id="6a875-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="6a875-105">На следующей схеме показаны все шаги настройки и запуска эксперимента на веб-сайте электронной коммерции в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a875-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="6a875-106">Дополнительные шаги описаны в отдельных разделах.</span><span class="sxs-lookup"><span data-stu-id="6a875-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="6a875-107">[ ![Путь взаимодействия пользователя с экспериментами — настройка](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="6a875-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="6a875-108">Настройка эксперимента в сторонней службе</span><span class="sxs-lookup"><span data-stu-id="6a875-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="6a875-109">К этому моменту вы должны были выбрать стороннюю службу, чтобы запустить и отслеживать свой эксперимент, и настроить соединитель экспериментирования.</span><span class="sxs-lookup"><span data-stu-id="6a875-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="6a875-110">Эти предварительные условия описаны в разделе [Экспериментирование в Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6a875-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="6a875-111">Выполните шаги, необходимые для создания эксперимента в сторонней службе.</span><span class="sxs-lookup"><span data-stu-id="6a875-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="6a875-112">Если соединитель настроен правильно, полный список экспериментов, которые вы настраиваете в сторонней службе, появится в конструкторе сайтов в течение 5 минут.</span><span class="sxs-lookup"><span data-stu-id="6a875-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will surface in site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="6a875-113">Настройка метрик успешности</span><span class="sxs-lookup"><span data-stu-id="6a875-113">Set up your success metrics</span></span>
<span data-ttu-id="6a875-114">Каждый эксперимент нуждается в метриках для измерения воздействия вариаций и подтверждения гипотезы.</span><span class="sxs-lookup"><span data-stu-id="6a875-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="6a875-115">Выполните приведенные ниже шаги, чтобы разрешить вычисление метрик в сторонней службе с использованием событий телеметрии в режиме реального времени из Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a875-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

1. <span data-ttu-id="6a875-116">В конструкторе сайтов выберите вкладку **Страницы** в левой области переходов, затем выберите страницу, по которой необходимо собрать метрики.</span><span class="sxs-lookup"><span data-stu-id="6a875-116">In site builder, select the **Pages** tab in the left navigation pane and then select the page that you want to collect metrics on.</span></span> 
1. <span data-ttu-id="6a875-117">Перейдите к разделу **Коды событий для отслеживания** в правой области свойств страницы или модуля, которые необходимо отследить.</span><span class="sxs-lookup"><span data-stu-id="6a875-117">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="6a875-118">Выберите **Представление**.</span><span class="sxs-lookup"><span data-stu-id="6a875-118">Select **View**.</span></span> <span data-ttu-id="6a875-119">Отображается список всех кодов событий.</span><span class="sxs-lookup"><span data-stu-id="6a875-119">A list of all event IDs is displayed.</span></span> <span data-ttu-id="6a875-120">Скопируйте событие, которое требуется отслеживать, и вставьте ключ события в указанное место в сторонней службе.</span><span class="sxs-lookup"><span data-stu-id="6a875-120">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="6a875-121">Если требуется более одного события, скопируйте ключи по одному.</span><span class="sxs-lookup"><span data-stu-id="6a875-121">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="6a875-122">Чтобы узнать, как просмотреть все доступные события и атрибуты, включая представления страниц и отслеживание выручки, см. раздел [События компонентов Commerce для диагностики и устранения неполадок](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="6a875-122">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="6a875-123">Выполните все другие шаги для отслеживания метрик в соответствии с требованиями сторонней службы.</span><span class="sxs-lookup"><span data-stu-id="6a875-123">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="6a875-124">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="6a875-124">Previous step</span></span>
[<span data-ttu-id="6a875-125">Определение гипотезы и определение метрик для эксперимента</span><span class="sxs-lookup"><span data-stu-id="6a875-125">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="6a875-126">Далее</span><span class="sxs-lookup"><span data-stu-id="6a875-126">Next step</span></span>
[<span data-ttu-id="6a875-127">Подключение и редактирование эксперимента</span><span class="sxs-lookup"><span data-stu-id="6a875-127">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
