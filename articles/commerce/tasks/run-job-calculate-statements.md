---
title: Настройка и выполнение задания для расчета отчетов
description: Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для создания и расчета журналов операций для выбранного магазина или группы магазинов.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8366bfff16bac8ef8f7b15cb97417d474b52f59c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232769"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="5784a-103">Настройка и выполнение задания для расчета отчетов</span><span class="sxs-lookup"><span data-stu-id="5784a-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5784a-104">Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для создания и расчета журналов операций для выбранного магазина или группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="5784a-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="5784a-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="5784a-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="5784a-106">Перейдите "Все рабочие области > Финансовая информация магазина".</span><span class="sxs-lookup"><span data-stu-id="5784a-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="5784a-107">Щелкните "Создать строки журнала операций".</span><span class="sxs-lookup"><span data-stu-id="5784a-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="5784a-108">Выберите конкретный магазин или узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="5784a-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="5784a-109">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="5784a-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="5784a-110">Щелкните вкладку "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="5784a-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="5784a-111">В поле "Пакетная обработка" выберите "Да".</span><span class="sxs-lookup"><span data-stu-id="5784a-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="5784a-112">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="5784a-112">Click Recurrence.</span></span>
6. <span data-ttu-id="5784a-113">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="5784a-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="5784a-114">В поле "Время начала" введите время.</span><span class="sxs-lookup"><span data-stu-id="5784a-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="5784a-115">Выберите параметр "Дата завершения не указана".</span><span class="sxs-lookup"><span data-stu-id="5784a-115">Select the No end date option.</span></span>
9. <span data-ttu-id="5784a-116">В поле PatternUnit введите "Дни".</span><span class="sxs-lookup"><span data-stu-id="5784a-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="5784a-117">В поле "На" введите число.</span><span class="sxs-lookup"><span data-stu-id="5784a-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="5784a-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5784a-118">Click OK.</span></span>
12. <span data-ttu-id="5784a-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5784a-119">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]