--- 
title: "Разноска интернет-продаж и платежей"
description: "Эта процедура содержите инструкции по настройке и запуску регулярного пакетного задания для создания заказов на продажу и платежей для проводок интернета-магазина."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 463a68e73e04990a99323f9f77d9936f586a575c
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="ec50c-103">Разноска интернет-продаж и платежей</span><span class="sxs-lookup"><span data-stu-id="ec50c-103">Post online sales and payments</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ec50c-104">Эта процедура содержите инструкции по настройке и запуску регулярного пакетного задания для создания заказов на продажу и платежей для проводок интернета-магазина.</span><span class="sxs-lookup"><span data-stu-id="ec50c-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="ec50c-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="ec50c-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ec50c-106">Перейдите в раздел "Все рабочие области" > "Финансовая информация розничного магазина".</span><span class="sxs-lookup"><span data-stu-id="ec50c-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="ec50c-107">Щелкните "Синхронизация заказов".</span><span class="sxs-lookup"><span data-stu-id="ec50c-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="ec50c-108">В поле "Организационная иерархия" выберите "Розничные магазины по регионам".</span><span class="sxs-lookup"><span data-stu-id="ec50c-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="ec50c-109">Выберите конкретный интернет-магазин или узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="ec50c-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="ec50c-110">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="ec50c-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="ec50c-111">Щелкните вкладку "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="ec50c-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="ec50c-112">Установите или снимите флажок "Пакетная обработка".</span><span class="sxs-lookup"><span data-stu-id="ec50c-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="ec50c-113">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="ec50c-113">Click Recurrence.</span></span>
7. <span data-ttu-id="ec50c-114">Выберите параметр "Дата завершения не указана".</span><span class="sxs-lookup"><span data-stu-id="ec50c-114">Select the No end date option.</span></span>
8. <span data-ttu-id="ec50c-115">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="ec50c-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="ec50c-116">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ec50c-116">Click OK.</span></span>
10. <span data-ttu-id="ec50c-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ec50c-117">Click OK.</span></span>


