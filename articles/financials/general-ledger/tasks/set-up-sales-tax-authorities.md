--- 
title: "Настройка налоговых органов"
description: "Налоговые органы — это юридические лица, которым отправляются налоговые отчеты и выплачиваются налоги."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: b1ebd65bcf3950c0f2a91d198fec22b92209de48
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="355cd-103">Настройка налоговых органов</span><span class="sxs-lookup"><span data-stu-id="355cd-103">Set up sales tax authorities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="355cd-104">Налоговые органы — это юридические лица, которым отправляются налоговые отчеты и выплачиваются налоги.</span><span class="sxs-lookup"><span data-stu-id="355cd-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="355cd-105">Вы можете платить налоги непосредственно налоговому органу или через счет поставщика, который создается для налогового органа.</span><span class="sxs-lookup"><span data-stu-id="355cd-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="355cd-106">Если это сделать, компания может использовать свои обычные платежные процедуры для своевременных платежей налоговому органу.</span><span class="sxs-lookup"><span data-stu-id="355cd-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="355cd-107">Если не настроить налоговый орган в качестве поставщика, кто-то должен будет готовить платежи налоговому органу в соответствующий срок.</span><span class="sxs-lookup"><span data-stu-id="355cd-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="355cd-108">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="355cd-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="355cd-109">Перейдите в раздел "Налог" > "Косвенные налоги" > "Налог" > "Налоговые органы".</span><span class="sxs-lookup"><span data-stu-id="355cd-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="355cd-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="355cd-110">Click New.</span></span>
3. <span data-ttu-id="355cd-111">В поле "Налоговый орган" введите значение.</span><span class="sxs-lookup"><span data-stu-id="355cd-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="355cd-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="355cd-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="355cd-113">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="355cd-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="355cd-114">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="355cd-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="355cd-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="355cd-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="355cd-116">Выберите макет отчета для своей страны или региона, если он имеется.</span><span class="sxs-lookup"><span data-stu-id="355cd-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="355cd-117">Если макеты отчетов не соответствуют требованиям налогового органа, используйте макет по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="355cd-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="355cd-118">Введите значения в форму "Округление" и поля "Округление", чтобы указать, как должна округляться выплачиваемая общая сумма налога.</span><span class="sxs-lookup"><span data-stu-id="355cd-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="355cd-119">Все расхождения при округлении будут разнесены в счета для автоматических проводок, настроенные в главной книге.</span><span class="sxs-lookup"><span data-stu-id="355cd-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="355cd-120">В поле "Округление" введите число.</span><span class="sxs-lookup"><span data-stu-id="355cd-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="355cd-121">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="355cd-121">Click Save.</span></span>


