---
title: Периодические задачи управления кредитом
description: В этой теме описываются периодические задачи, которые являются обязательной частью процесса управления кредитными лимитами для клиентов.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a034d563c12c4ba8b99e13b30ea2683555a01276
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254495"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="6a378-103">Периодические задачи по управлению кредитом</span><span class="sxs-lookup"><span data-stu-id="6a378-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a378-104">В этой теме описываются периодические задачи, которые являются обязательной частью процесса управления кредитными лимитами для клиентов.</span><span class="sxs-lookup"><span data-stu-id="6a378-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="6a378-105">Обновить показатели рисков</span><span class="sxs-lookup"><span data-stu-id="6a378-105">Update risk scores</span></span>

<span data-ttu-id="6a378-106">По мере развития бизнеса и изменения возможных кредитных рисков для данного клиента также могут быть внесены изменения.</span><span class="sxs-lookup"><span data-stu-id="6a378-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="6a378-107">Для поддержки соответствующих кредитных лимитов для клиентов необходимо периодически проверять критерии для каждого показателя риска и обновлять результаты для каждого клиента.</span><span class="sxs-lookup"><span data-stu-id="6a378-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="6a378-108">Можно обновить следующие результаты, используя страницу **Обновить оценки риска** (**Кредит и сбор задолженностей \> Периодические задачи \> Управление кредитом \> Обновить оценки риска**).</span><span class="sxs-lookup"><span data-stu-id="6a378-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="6a378-109">Также обрабатываются все определяемые пользователем вычисления.</span><span class="sxs-lookup"><span data-stu-id="6a378-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="6a378-110">**Среднее число дней платежа** — этот показатель является средним количеством дней, которое клиент использует для оплаты накладных.</span><span class="sxs-lookup"><span data-stu-id="6a378-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="6a378-111">**Срок обслуживания клиента** — этот показатель представляет собой количество лет, в течение которых клиент был клиентом вашей организации.</span><span class="sxs-lookup"><span data-stu-id="6a378-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="6a378-112">**Срок нахождения в бизнесе** — этот показатель означает количество лет, в течение которых клиент был в бизнесе.</span><span class="sxs-lookup"><span data-stu-id="6a378-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="6a378-113">В нем используется значение поля **Начало бизнеса** на странице **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="6a378-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="6a378-114">**Период погашения дебиторской задолженности (в днях)** — эта оценка базируется на сальдо по расчетам с клиентами, выручке и количестве дней за предыдущий 12-месячный период.</span><span class="sxs-lookup"><span data-stu-id="6a378-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="6a378-115">**Средний остаток** — этот показатель базируется на сальдо по расчетам с клиентами за предыдущий 12-месячный период.</span><span class="sxs-lookup"><span data-stu-id="6a378-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="6a378-116">**Группа управления кредитом**, **Статус счета** и **Страна** — эти показатели используются для получения информации от клиента.</span><span class="sxs-lookup"><span data-stu-id="6a378-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="6a378-117">Обновление статистики сальдо по клиенту</span><span class="sxs-lookup"><span data-stu-id="6a378-117">Update customer balance statistics</span></span>

<span data-ttu-id="6a378-118">Можно выполнить процесс **Обновить статистику по сальдо клиента** для обновления расчета статистики сальдо, которая отображается на странице **Запрос статистики сальдо**.</span><span class="sxs-lookup"><span data-stu-id="6a378-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="6a378-119">Эти сведения используются для расчета показателей риска и значений, которые отображаются на информационных панелях статистики кредита на странице **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="6a378-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="6a378-120">При выполнении процесса обновляется статистика по сальдо клиента для одного клиента.</span><span class="sxs-lookup"><span data-stu-id="6a378-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="6a378-121">Чтобы настроить пакетное задание для выполнения процесса для нескольких клиентов, можно использовать страницу **Вычислить статистику сальдо** (**Управление кредитом \> Периодические задачи \> Вычислить статистику сальдо**).</span><span class="sxs-lookup"><span data-stu-id="6a378-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]