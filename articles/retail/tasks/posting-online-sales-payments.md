--- 
title: "Разноска интерактивных продаж и платежей"
description: "Эта процедура содержите инструкции по настройке и запуску регулярного пакетного задания для создания заказов на продажу и платежей для проводок интернета-магазина."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="54b2d-103">Разноска интерактивных продаж и платежей</span><span class="sxs-lookup"><span data-stu-id="54b2d-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="54b2d-104">Эта процедура содержите инструкции по настройке и запуску регулярного пакетного задания для создания заказов на продажу и платежей для проводок интернета-магазина.</span><span class="sxs-lookup"><span data-stu-id="54b2d-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="54b2d-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="54b2d-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="54b2d-106">Перейдите в раздел "Все рабочие области" > "Финансовая информация розничного магазина".</span><span class="sxs-lookup"><span data-stu-id="54b2d-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="54b2d-107">Щелкните "Синхронизация заказов".</span><span class="sxs-lookup"><span data-stu-id="54b2d-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="54b2d-108">В поле "Организационная иерархия" выберите "Розничные магазины по регионам".</span><span class="sxs-lookup"><span data-stu-id="54b2d-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="54b2d-109">Выберите конкретный интернет-магазин или узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="54b2d-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="54b2d-110">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="54b2d-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="54b2d-111">Щелкните вкладку "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="54b2d-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="54b2d-112">Установите или снимите флажок "Пакетная обработка".</span><span class="sxs-lookup"><span data-stu-id="54b2d-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="54b2d-113">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="54b2d-113">Click Recurrence.</span></span>
7. <span data-ttu-id="54b2d-114">Выберите параметр "Дата завершения не указана".</span><span class="sxs-lookup"><span data-stu-id="54b2d-114">Select the No end date option.</span></span>
8. <span data-ttu-id="54b2d-115">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="54b2d-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="54b2d-116">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="54b2d-116">Click OK.</span></span>
10. <span data-ttu-id="54b2d-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="54b2d-117">Click OK.</span></span>


