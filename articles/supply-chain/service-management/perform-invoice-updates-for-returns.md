---
title: Выполнение обновлений накладной для возвратов
description: Эта функция также поддерживает бизнес-процессы компаний, выбравших процедуру одновременного выставления накладных по заказам на возврат и заказам на продажу одним и тем же сотрудником.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec803aaa2f750c43a1865c9536730b275e6ef1d4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202154"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="e50ac-103">Выполнение обновлений накладной для возвратов</span><span class="sxs-lookup"><span data-stu-id="e50ac-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e50ac-104">Заказ на возврат является особым типом заказа на продажу, имеющим маркировку "Возврат".</span><span class="sxs-lookup"><span data-stu-id="e50ac-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="e50ac-105">Поэтому, чтобы создать накладные для заказа на возврат, страница списка **Все заказы на продажу** используется вместо формы **Заказы на возврат**.</span><span class="sxs-lookup"><span data-stu-id="e50ac-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="e50ac-106">Эта функция также поддерживает бизнес-процессы компаний, выбравших процедуру одновременного выставления накладных по заказам на возврат и заказам на продажу одним и тем же сотрудником.</span><span class="sxs-lookup"><span data-stu-id="e50ac-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="e50ac-107">Так как накладная по возвращенным номенклатурам используется для отрицательных сумм, она называется кредит-нотой.</span><span class="sxs-lookup"><span data-stu-id="e50ac-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="e50ac-108">Если была настроена пакетная обработка обновления накладной, заказ на продажу, относящийся к типу **Возвращенный заказ**, должен иметь статус строки возврата **Получено**, указывающий на то, что отборочная накладная этого заказа была обновлена.</span><span class="sxs-lookup"><span data-stu-id="e50ac-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="e50ac-109">Разноска накладной для заказа на возврат</span><span class="sxs-lookup"><span data-stu-id="e50ac-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="e50ac-110">Щелкните **Расчеты с клиентами** \> **Общий** \> **Заказы на продажу** \> **Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="e50ac-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="e50ac-111">Выберите заказ на продажу, для которого **Возвращенный заказ** отображается в поле **Тип заказа**.</span><span class="sxs-lookup"><span data-stu-id="e50ac-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="e50ac-112">В элементе управления "Панель операций" на вкладке **Накладная** в группе **Создать** щелкните **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="e50ac-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="e50ac-113">На вкладке **Параметры** установите флажок **Разноска**.</span><span class="sxs-lookup"><span data-stu-id="e50ac-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="e50ac-114">Проверьте сведения в форме и внесите все необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="e50ac-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="e50ac-115">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e50ac-115">Click **OK**.</span></span> <span data-ttu-id="e50ac-116">Кредит-нота разнесена.</span><span class="sxs-lookup"><span data-stu-id="e50ac-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="e50ac-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e50ac-117">See also</span></span>

[<span data-ttu-id="e50ac-118">Обновления отборочной накладной для возвратов</span><span class="sxs-lookup"><span data-stu-id="e50ac-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


