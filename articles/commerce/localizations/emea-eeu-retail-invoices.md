---
title: Накладные клиента и возвратные заказы на продажу для Commerce в странах Восточной Европы
description: В этом разделе описывается, как настроить сведения по накладным клиентов и заказы на возврат продаж в странах Восточной Европы.
author: epopov
manager: annbe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a00a960142b0e3955c80d75f7963f4827209bf75
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408515"
---
# <a name="customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a><span data-ttu-id="ebed3-103">Накладные клиента и возвратные заказы на продажу для Commerce в странах Восточной Европы</span><span class="sxs-lookup"><span data-stu-id="ebed3-103">Customer invoices and return sales orders in Eastern European countries</span></span>


[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ebed3-104">В этом разделе описывается, как настроить сведения по накладным клиентов и заказы на возврат продаж в странах Восточной Европы.</span><span class="sxs-lookup"><span data-stu-id="ebed3-104">This topic describes how to set up information for customer invoices and return sales orders in Eastern European countries.</span></span>

<span data-ttu-id="ebed3-105">Можно настроить следующие сведения для накладных клиентов и заказов на продажу с возвратом, созданных в Retail POS.</span><span class="sxs-lookup"><span data-stu-id="ebed3-105">You can set up the following information for customer invoices and return sales orders that are generated in Retail point of sale (POS).</span></span>

- <span data-ttu-id="ebed3-106">Можно использовать налоговые группы для обработки возвратов с помощью заказов на продажу с возвратом.</span><span class="sxs-lookup"><span data-stu-id="ebed3-106">You can use sales tax groups to process returns by using return sales orders.</span></span> <span data-ttu-id="ebed3-107">Перейдите в раздел **Retail и Commerce \> Настройка центрального офиса \> Параметры \> Параметры Commerce**.</span><span class="sxs-lookup"><span data-stu-id="ebed3-107">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="ebed3-108">Откройте вкладку **Разноска \> Накладная**, затем задайте для параметра **Использовать налоговую группу для возвратов** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ebed3-108">Open the **Posting \> Invoice** tab, and then set **Use sales tax group for returns** to **Yes**.</span></span>

    * <span data-ttu-id="ebed3-109">Чтобы определить налоговую группу для возвратов, сделанных клиентом, на странице **Клиенты** на экспресс-вкладке **Commerce** в поле **Налоговая группа для возвратов** выберите налоговую группу.</span><span class="sxs-lookup"><span data-stu-id="ebed3-109">To specify the sales tax group for returns that are made by a customer, on the **Customers** page, on the **Commerce** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="ebed3-110">При разноске заказа на продажу с возвратом для клиента в строке заказа на продажу с возвратом обновляется налоговая группа для возвратов, указанная в форме **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="ebed3-110">When you post a return sales order for a customer, the return sales order line is updated with the sales tax group for returns that is specified in the **Customers** form.</span></span>
    * <span data-ttu-id="ebed3-111">Чтобы определить налоговую группу для возвратов, сделанных клиентом в Retail POS, на странице **Магазины** на экспресс-вкладке **Общие** в поле **Налоговая группа для возвратов** выберите налоговую группу.</span><span class="sxs-lookup"><span data-stu-id="ebed3-111">To specify a sales tax group for returns that are made at a retail POS by a customer, on the **Stores** page, on the **General** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="ebed3-112">При разноске заказа на продажу с возвратом для клиента магазина в строке заказа на продажу с возвратом обновляется налоговая группа для возвратов, указанная на странице **Магазины**.</span><span class="sxs-lookup"><span data-stu-id="ebed3-112">When you post a return sales order for a customer of a  store, the return sales order line is updated with the sales tax group for returns that are specified on the **Stores** page.</span></span>

- <span data-ttu-id="ebed3-113">Можно использовать дату разноски накладной клиента или заказа на продажу с возвратом в качестве даты накладной или возврата, если накладная или возврат не имеют дату продажи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ebed3-113">You can use the posting date of a customer invoice or a return sales order as the sales date of the invoice or return if the invoice or return does not have a default sales date.</span></span> <span data-ttu-id="ebed3-114">Перейдите в раздел **Retail и Commerce \> Настройка центрального офиса \> Параметры \> Параметры Commerce**.</span><span class="sxs-lookup"><span data-stu-id="ebed3-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="ebed3-115">Откройте вкладку **Разноска \> Накладная**, затем задайте для параметра **Использовать дату разноски как дату продажи** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ebed3-115">Open the **Posting \> Invoice** tab, and then set **Use posting date as sales date** to **Yes**.</span></span>
- <span data-ttu-id="ebed3-116">Можно использовать диапазон номеров, предоставленный налоговыми органами для нумерации латышских и литовских накладных клиентов и заказов на продажу с возвратом.</span><span class="sxs-lookup"><span data-stu-id="ebed3-116">You can use the number range that is provided by the tax authorities to number Latvian and Lithuanian customer invoices and return sales orders.</span></span>

    * <span data-ttu-id="ebed3-117">Перейдите в раздел **Управление организацией \> Номерные серии \> Управление счетчиками**.</span><span class="sxs-lookup"><span data-stu-id="ebed3-117">Go to **Organization administration \> Number sequences \> Counters management**.</span></span> <span data-ttu-id="ebed3-118">Должна существовать запись, в которой **Модуль** = **Продажи** и **Типа** = **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="ebed3-118">There should be a record where **Module** = **Sales** and **Type** = **Invoice**.</span></span>
    * <span data-ttu-id="ebed3-119">Перейдите в раздел **Управление организацией \> Номерные серии \> Настройка нумерации накладных**.</span><span class="sxs-lookup"><span data-stu-id="ebed3-119">Go to **Organization administration \> Number sequences \> Invoice numbering setup**.</span></span> <span data-ttu-id="ebed3-120">Установите флажок **Commerce** для строки номерной серии, которая используется для нумерации накладных клиентов.</span><span class="sxs-lookup"><span data-stu-id="ebed3-120">Select the **Commerce** check box for the number sequence line that is used to number the customer invoices.</span></span>
