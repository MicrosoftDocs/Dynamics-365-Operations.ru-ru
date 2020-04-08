---
title: Настройка способа оплаты для прямого дебетования ISO20022
description: Эта процедура показывает, как настроить метод платежей клиентов для прямого дебетования ISO20022 или любого другого типа платежа с использованием электронной отчетности.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38afbc3a49d9020540a56e58ce51196b53d6a9e1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143440"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="edf04-103">Настройка способа оплаты для прямого дебетования ISO20022</span><span class="sxs-lookup"><span data-stu-id="edf04-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="edf04-104">Эта процедура показывает, как настроить метод платежей клиентов для прямого дебетования ISO20022 или любого другого типа платежа с использованием электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="edf04-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="edf04-105">Прежде чем можно будет выполнить эту задачу, необходимо настроить конфигурации формата экспорта и счета платежей.</span><span class="sxs-lookup"><span data-stu-id="edf04-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="edf04-106">Эта процедура была создана с использованием демонстрационных данных компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="edf04-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="edf04-107">Это третья процедура из пяти, которые демонстрируют процесс платежа клиентов с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="edf04-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="edf04-108">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="edf04-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="edf04-109">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="edf04-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="edf04-110">Например, отфильтруйте поле "Способ оплаты" по значению "ELECTRONIC".</span><span class="sxs-lookup"><span data-stu-id="edf04-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="edf04-111">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="edf04-111">Click Edit.</span></span>
4. <span data-ttu-id="edf04-112">В поле "Счет оплаты" укажите значения "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="edf04-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="edf04-113">Разверните раздел "Форматы файлов".</span><span class="sxs-lookup"><span data-stu-id="edf04-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="edf04-114">В поле "Общая электронная отчетность" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="edf04-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="edf04-115">В поле "Экспорт конфигурации формата" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="edf04-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="edf04-116">В списке выберите "Прямое дебетование ISO20022 (DE)".</span><span class="sxs-lookup"><span data-stu-id="edf04-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="edf04-117">Если список пуст, конфигурация формата экспорта платежей клиента не импортирована и не активна.</span><span class="sxs-lookup"><span data-stu-id="edf04-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="edf04-118">Выберите значение "Да" в поле "Требуется поручение".</span><span class="sxs-lookup"><span data-stu-id="edf04-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="edf04-119">Выберите параметр "Требуется поручение" для форматов платежей клиентов, который требуют включения информации о поручении в сообщение платежа, например прямое дебетование SEPA.</span><span class="sxs-lookup"><span data-stu-id="edf04-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="edf04-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="edf04-120">Click Save.</span></span>

