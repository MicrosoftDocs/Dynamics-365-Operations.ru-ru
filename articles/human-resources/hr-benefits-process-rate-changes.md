---
title: Обработка изменений ставок
description: Процесс изменения ставок льгот в Microsoft Dynamics 365 Human Resources, когда для нового или существующего плана льгот есть изменения параметров правил допустимости.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 850709480326f6a0871f19ea1bb287631cd58b42
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229955"
---
# <a name="process-rate-changes"></a><span data-ttu-id="1e9ed-103">Обработка изменений ставок</span><span class="sxs-lookup"><span data-stu-id="1e9ed-103">Process rate changes</span></span>

<span data-ttu-id="1e9ed-104">Процесс изменения ставок льгот в Microsoft Dynamics 365 Human Resources, когда для нового или существующего плана льгот есть изменения параметров правил допустимости.</span><span class="sxs-lookup"><span data-stu-id="1e9ed-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="1e9ed-105">Если новое правило допустимости создано и назначено плану, система рекомендует снова выполнить проверку допустимости для проверки того, имеют ли работники право на план на основе новых параметров допустимости.</span><span class="sxs-lookup"><span data-stu-id="1e9ed-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="1e9ed-106">В рабочей области **Управление льготами** в **Обработка** выберите **Обработка обновления изменения ставки**.</span><span class="sxs-lookup"><span data-stu-id="1e9ed-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="1e9ed-107">В диалоговом окне **Выполнение обработки обновления изменения ставки** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="1e9ed-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="1e9ed-108">Поле</span><span class="sxs-lookup"><span data-stu-id="1e9ed-108">Field</span></span> | <span data-ttu-id="1e9ed-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1e9ed-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1e9ed-110">**Период регистрации**</span><span class="sxs-lookup"><span data-stu-id="1e9ed-110">**Enrollment period**</span></span> | <span data-ttu-id="1e9ed-111">Период регистрации, для которого необходимо обработать изменения ставки.</span><span class="sxs-lookup"><span data-stu-id="1e9ed-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="1e9ed-112">Если необходимо выполнить процесс в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1e9ed-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="1e9ed-113">Введите сведения для процесса.</span><span class="sxs-lookup"><span data-stu-id="1e9ed-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="1e9ed-114">Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1e9ed-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="1e9ed-115">Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1e9ed-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="1e9ed-116">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1e9ed-116">Select **OK**.</span></span> <span data-ttu-id="1e9ed-117">Процесс будет выполнен с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="1e9ed-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="1e9ed-118">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1e9ed-118">Select **OK**.</span></span>
