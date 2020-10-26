---
title: Определение гипотезы и определение метрик для эксперимента
description: В этом разделе описывается, как определить гипотезу и метрики успешности для эксперимента, который будет выполняться на веб-сайте электронной коммерции в Dynamics 365 Commerce.
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
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930274"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="f8f60-103">Определение гипотезы и определение метрики успеха для эксперимента</span><span class="sxs-lookup"><span data-stu-id="f8f60-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="f8f60-104">Первый этап жизненного цикла эксперимента включает в себя определение гипотезы для эксперимента и определение метрик, которые вы будете отслеживать для оценки успеха.</span><span class="sxs-lookup"><span data-stu-id="f8f60-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="f8f60-105">На следующей схеме показаны все шаги [настройки и запуска эксперимента](experimentation-overview.md) на веб-сайте электронной коммерции в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8f60-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f8f60-106">Дополнительные шаги описаны в отдельных разделах.</span><span class="sxs-lookup"><span data-stu-id="f8f60-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="f8f60-107">[ ![Путь взаимодействия пользователя с экспериментами — определение](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f8f60-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="f8f60-108">Гипотеза — это утверждение, в которой прогнозируется результат эксперимента.</span><span class="sxs-lookup"><span data-stu-id="f8f60-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="f8f60-109">Многие факторы влияют на определение гипотезы, например, исследование поведения пользователей и данные веб-сайта, которые вы собираете.</span><span class="sxs-lookup"><span data-stu-id="f8f60-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="f8f60-110">С гипотезой вы определяете допущение или теорию, которые вы хотите проверить с помощью эксперимента.</span><span class="sxs-lookup"><span data-stu-id="f8f60-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="f8f60-111">Примером гипотезы для эксперимента может быть *изображение белой футболки на домашней странице будет способствовать повышению коэффициента перехода по ссылкам по сравнению с изображением морского свитера в летние месяцы, так как летом люди хотят носить что-то более легкое и светлое".*</span><span class="sxs-lookup"><span data-stu-id="f8f60-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="f8f60-112">В этом случае вы создаете вариации, которые включают белую футболку и морской свитер, и публикуете их одновременно.</span><span class="sxs-lookup"><span data-stu-id="f8f60-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="f8f60-113">Чтобы проверить гипотезу, успех или неудачу в эксперименте следует напрямую связать с действиями пользователя; например, нажмет ли пользователь веб-сайта ссылку или кнопку.</span><span class="sxs-lookup"><span data-stu-id="f8f60-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks a link or button.</span></span> <span data-ttu-id="f8f60-114">Эти действия должны соответствовать событиям, которые будут отправлены в стороннюю службу, отслеживающую эксперимент.</span><span class="sxs-lookup"><span data-stu-id="f8f60-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="f8f60-115">Со временем процент пользователей, которые выполняют это действие, будет регистрироваться как показатель, который можно использовать для создания отчетов и проведения анализа.</span><span class="sxs-lookup"><span data-stu-id="f8f60-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="f8f60-116">Ознакомьтесь с разделом [События компонента Commerce для диагностики и устранения неполадок](dev-itpro/retail-component-events-diagnostics-troubleshooting.md), чтобы просмотреть все доступные события и атрибуты.</span><span class="sxs-lookup"><span data-stu-id="f8f60-116">Refer to the [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) topic to review all of the available events and attributes.</span></span>

## <a name="previous-step"></a><span data-ttu-id="f8f60-117">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="f8f60-117">Previous step</span></span>
[<span data-ttu-id="f8f60-118">Эксперименты в Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f8f60-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="f8f60-119">Далее</span><span class="sxs-lookup"><span data-stu-id="f8f60-119">Next step</span></span>
[<span data-ttu-id="f8f60-120">Настройка эксперимента</span><span class="sxs-lookup"><span data-stu-id="f8f60-120">Set up an experiment</span></span>](experimentation-setup.md)
