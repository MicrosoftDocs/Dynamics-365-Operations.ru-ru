---
title: Создание и обновление политик возврата и возмещения для канала
description: В этой теме объясняется, как настроить политику возврата и возмещения для канала.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 89e8fe78414e73053317ebe19e3afcc89231d440
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979729"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="70372-103">Создание и обновление политик возврата и возмещения для канала</span><span class="sxs-lookup"><span data-stu-id="70372-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="70372-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="70372-104">Overview</span></span>

<span data-ttu-id="70372-105">Политика возврата канала в Dynamics 365 Commerce позволяет компаниям устанавливать ограничения на то, какие платежные средства могут быть разрешены для обработки возврата на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="70372-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="70372-106">В этой теме описываются шаги, как настроить политику возврата товаров и возврата денег для канала.</span><span class="sxs-lookup"><span data-stu-id="70372-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="70372-107">Область политики в настоящее время ограничена настройкой предложений платежа, которые могут быть разрешены для канала.</span><span class="sxs-lookup"><span data-stu-id="70372-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="70372-108">Список "разрешено" основан на способах оплаты, используемых для совершения покупки.</span><span class="sxs-lookup"><span data-stu-id="70372-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="70372-109">Пример:</span><span class="sxs-lookup"><span data-stu-id="70372-109">For example:</span></span>

- <span data-ttu-id="70372-110">Если покупка была сделана с помощью подарочного сертификата, политика магазина заключается только в обработке возвратов в виде нового подарочного сертификата или предоставления кредита от магазина.</span><span class="sxs-lookup"><span data-stu-id="70372-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="70372-111">Если продажа осуществляется с помощью наличных денег, разрешенными вариантами для возврата денег являются наличные деньги, подарочный сертификат и счет клиента, но не кредитные карты.</span><span class="sxs-lookup"><span data-stu-id="70372-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="70372-112">Включить политику возврата</span><span class="sxs-lookup"><span data-stu-id="70372-112">Enable return policy</span></span>

<span data-ttu-id="70372-113">Чтобы включить функцию политики возврата канала, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="70372-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="70372-114">Откройте рабочую область **Управление функциями** в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="70372-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="70372-115">В списке имен найдите функцию **Включить политики возврата канала**.</span><span class="sxs-lookup"><span data-stu-id="70372-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="70372-116">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="70372-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="70372-117">Настройка политики возврата</span><span class="sxs-lookup"><span data-stu-id="70372-117">Configure return policy</span></span>

<span data-ttu-id="70372-118">Выполните следующие действия, чтобы настроить политику возврата для розничного магазина или канала интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="70372-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="70372-119">Перейдите **Retail и Commerce** \> **Настройка канала** \> **Возвраты** \> **Политика возврата канала**.</span><span class="sxs-lookup"><span data-stu-id="70372-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="70372-120">Выберите **Создать** для создания нового шаблона политики возврата.</span><span class="sxs-lookup"><span data-stu-id="70372-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="70372-121">Для использования существующего шаблона выберите шаблон в левой области.</span><span class="sxs-lookup"><span data-stu-id="70372-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="70372-122">Для новых шаблонов добавьте имя и описание, которые помогут определить политику и ее применение к каналу.</span><span class="sxs-lookup"><span data-stu-id="70372-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="70372-123">![Добавление новой политики возврата](media/Return-policy-page1.png "Добавление новой политики возврата")</span><span class="sxs-lookup"><span data-stu-id="70372-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="70372-124">В разделе **Разрешенные способы оплаты возвратов** задайте предложения платежа по возврату как **Разрешить** для каждого способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="70372-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="70372-125">![Добавление способов оплаты](media/Return-policy-page2.PNG "Задание разрешенных способов оплаты для каждого типа платежа")</span><span class="sxs-lookup"><span data-stu-id="70372-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="70372-126">Способы оплаты заимствуются из способов оплаты, установленных для организации.</span><span class="sxs-lookup"><span data-stu-id="70372-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="70372-127">Добавление разрешенного типа предложения по возврату для каждого указанного способа оплаты обеспечит возможность возврата согласно разрешенному типу предложения возврата.</span><span class="sxs-lookup"><span data-stu-id="70372-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="70372-128">Свяжите шаблон политики возвратов с магазинами, в которых он будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="70372-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="70372-129">Выберите **Добавить** на вкладке **Каналы розничной торговли** и свяжите доступные каналы.</span><span class="sxs-lookup"><span data-stu-id="70372-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="70372-130">В диалоговом окне **Выбор узлов организации** выберите магазины, регионы и организации, с которыми должен быть связан шаблон.</span><span class="sxs-lookup"><span data-stu-id="70372-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="70372-131">С каждым магазином можно связать только один шаблон политики возвратов.</span><span class="sxs-lookup"><span data-stu-id="70372-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="70372-132">С помощью кнопок со стрелками выберите магазины, регионы или организации.</span><span class="sxs-lookup"><span data-stu-id="70372-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="70372-133">Дата вступления в силу политики будет датой, когда политики применяются к каналам и выполняются задания канала.</span><span class="sxs-lookup"><span data-stu-id="70372-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="70372-134">![Диалоговое окно выборы узлов организации](media/Return-policy-page3.PNG "Диалоговое окно выборы узлов организации")</span><span class="sxs-lookup"><span data-stu-id="70372-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="70372-135">На странице **График распределения** выполните задание **1070**, чтобы сделать политику возврата канала доступной для POS.</span><span class="sxs-lookup"><span data-stu-id="70372-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="70372-136">Предварительный просмотр политики возвратов канала в POS-терминале</span><span class="sxs-lookup"><span data-stu-id="70372-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="70372-137">Выполните шаги из одного из следующих примеров, чтобы просмотреть разрешенные типы предложений возврата в POS.</span><span class="sxs-lookup"><span data-stu-id="70372-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="70372-138">Выполните вход в POS-терминал в качестве кассира или менеджера.</span><span class="sxs-lookup"><span data-stu-id="70372-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="70372-139">В области **Смена и денежный ящик** выберите **Показать журнал**.</span><span class="sxs-lookup"><span data-stu-id="70372-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="70372-140">Выберите проводку, которая является частью возврата.</span><span class="sxs-lookup"><span data-stu-id="70372-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="70372-141">Выберите номенклатуры для возмещения и выберите способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="70372-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="70372-142">Если выбранное предложение платежа относится к списку разрешенных предложения платежа, кассир может выполнить проводку.</span><span class="sxs-lookup"><span data-stu-id="70372-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="70372-143">Если выбранное предложение платежа не разрешено, будет выведено сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="70372-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="70372-144">Выберите **Сумма к оплате**, чтобы открыть список всех допустимых типов предложений платежа по возврату.</span><span class="sxs-lookup"><span data-stu-id="70372-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="70372-145">–или–</span><span class="sxs-lookup"><span data-stu-id="70372-145">-or-</span></span>

1. <span data-ttu-id="70372-146">Выполните вход в POS-терминал в качестве кассира или менеджера.</span><span class="sxs-lookup"><span data-stu-id="70372-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="70372-147">Выберите **Проводка возврата** и введите код чека, используя сканер штрих-кода или запись вручную.</span><span class="sxs-lookup"><span data-stu-id="70372-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="70372-148">Выберите проводку, которая является частью возврата.</span><span class="sxs-lookup"><span data-stu-id="70372-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="70372-149">Выберите номенклатуры для возмещения и выберите способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="70372-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="70372-150">Если выбранное предложение платежа относится к списку разрешенных предложения платежа, кассир может выполнить проводку.</span><span class="sxs-lookup"><span data-stu-id="70372-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="70372-151">Если выбранное предложение платежа не разрешено, будет выведено сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="70372-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="70372-152">Выберите **Сумма к оплате**, чтобы открыть список всех допустимых типов предложений платежа по возврату.</span><span class="sxs-lookup"><span data-stu-id="70372-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="70372-153">![Возмещение не разрешено](media/Return-policy-page6.png "Тип возврата запрещен")</span><span class="sxs-lookup"><span data-stu-id="70372-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="70372-154">![Список способов оплаты](media/Return-policy-page5.PNG "Тип возврата разрешен")</span><span class="sxs-lookup"><span data-stu-id="70372-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
