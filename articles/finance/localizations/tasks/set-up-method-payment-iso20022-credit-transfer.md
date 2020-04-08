---
title: Настройка способов оплаты для кредитового перевода ISO20022
description: Эта процедура показывает, как настроить метод платежа поставщику для переноса кредита ISO20022 или любого другого типа платежа с использованием электронной отчетности для создания файла.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d60502cd7f749b71cf39cc38d8a39dcbb7b108
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140125"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="40edf-103">Настройка способов оплаты для кредитового перевода ISO20022</span><span class="sxs-lookup"><span data-stu-id="40edf-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="40edf-104">Эта процедура показывает, как настроить метод платежа поставщику для переноса кредита ISO20022 или любого другого типа платежа с использованием электронной отчетности для создания файла.</span><span class="sxs-lookup"><span data-stu-id="40edf-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="40edf-105">Прежде чем можно будет выполнить эту задачу, необходимо экспортировать конфигурации формата и настроить счета платежей.</span><span class="sxs-lookup"><span data-stu-id="40edf-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="40edf-106">Эта задача была создана с использованием компании с демонстрационными данными DEMF.</span><span class="sxs-lookup"><span data-stu-id="40edf-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="40edf-107">Это третья процедура из пяти, которые иллюстрируют процесс платежа поставщикам с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="40edf-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="40edf-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="40edf-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="40edf-109">Перейдите в раздел "Расчеты с поставщиками" > "Настройка платежей" > "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="40edf-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="40edf-110">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="40edf-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="40edf-111">Например, отфильтруйте поле "Способ оплаты" по значению "SEPA CT".</span><span class="sxs-lookup"><span data-stu-id="40edf-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="40edf-112">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="40edf-112">Click Edit.</span></span>
4. <span data-ttu-id="40edf-113">В поле "Период" выберите "Итого".</span><span class="sxs-lookup"><span data-stu-id="40edf-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="40edf-114">В поле "Тип платежа" выберите "Электронный платеж".</span><span class="sxs-lookup"><span data-stu-id="40edf-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="40edf-115">Разверните раздел "Форматы файлов".</span><span class="sxs-lookup"><span data-stu-id="40edf-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="40edf-116">В поле "Общая электронная отчетность" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="40edf-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="40edf-117">В поле "Экспорт конфигурации формата" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="40edf-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="40edf-118">В списке выберите значение "Перемещение кредита ISO20022 (DE)".</span><span class="sxs-lookup"><span data-stu-id="40edf-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="40edf-119">Если список пуст, конфигурация формата экспорта платежа поставщику не импортирована и не активна.</span><span class="sxs-lookup"><span data-stu-id="40edf-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="40edf-120">В поле "Тип счета" выберите "Банк".</span><span class="sxs-lookup"><span data-stu-id="40edf-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="40edf-121">В поле "Счет оплаты" укажите значения "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="40edf-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="40edf-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="40edf-122">Click Save.</span></span>

