--- 
title: "Настройка метода оплаты для безакцептного списания ISO20022"
description: "Эта процедура показывает, как настроить метод платежей клиентов для прямого дебетования ISO20022 или любого другого типа платежа с использованием электронной отчетности."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d18a72b511d51cbeb69f5b417defe0974112a67d
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="3c7ec-103">Настройка метода оплаты для безакцептного списания ISO20022</span><span class="sxs-lookup"><span data-stu-id="3c7ec-103">Set up method of payment for ISO20022 direct debit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3c7ec-104">Эта процедура показывает, как настроить метод платежей клиентов для прямого дебетования ISO20022 или любого другого типа платежа с использованием электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="3c7ec-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="3c7ec-105">Прежде чем можно будет выполнить эту задачу, необходимо настроить конфигурации формата экспорта и счета платежей.</span><span class="sxs-lookup"><span data-stu-id="3c7ec-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="3c7ec-106">Эта процедура была создана с использованием демонстрационных данных компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="3c7ec-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="3c7ec-107">Это третья процедура из пяти, которые демонстрируют процесс платежа клиентов с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="3c7ec-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="3c7ec-108">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="3c7ec-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="3c7ec-109">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="3c7ec-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3c7ec-110">Например, отфильтруйте поле "Способ оплаты" по значению "ELECTRONIC".</span><span class="sxs-lookup"><span data-stu-id="3c7ec-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="3c7ec-111">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="3c7ec-111">Click Edit.</span></span>
4. <span data-ttu-id="3c7ec-112">В поле "Счет оплаты" укажите значения "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="3c7ec-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="3c7ec-113">Разверните раздел "Форматы файлов".</span><span class="sxs-lookup"><span data-stu-id="3c7ec-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="3c7ec-114">В поле "Общая электронная отчетность" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="3c7ec-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="3c7ec-115">В поле "Экспорт конфигурации формата" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3c7ec-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="3c7ec-116">В списке выберите "Прямое дебетование ISO20022 (DE)".</span><span class="sxs-lookup"><span data-stu-id="3c7ec-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="3c7ec-117">Если список пуст, конфигурация формата экспорта платежей клиента не импортирована и не активна.</span><span class="sxs-lookup"><span data-stu-id="3c7ec-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="3c7ec-118">Выберите значение "Да" в поле "Требуется поручение".</span><span class="sxs-lookup"><span data-stu-id="3c7ec-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="3c7ec-119">Выберите параметр "Требуется поручение" для форматов платежей клиентов, который требуют включения информации о поручении в сообщение платежа, например прямое дебетование SEPA.</span><span class="sxs-lookup"><span data-stu-id="3c7ec-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="3c7ec-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3c7ec-120">Click Save.</span></span>


