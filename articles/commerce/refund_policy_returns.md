---
title: Создание и обновление политик возврата и возмещения для канала
description: В этой теме объясняется, как настроить политику возврата и возмещения для канала.
author: ShalabhjainMSFT
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: e23291130d55fdfb5c2e2077b78c221866d72c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792083"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="4af71-103">Создание и обновление политик возврата и возмещения для канала</span><span class="sxs-lookup"><span data-stu-id="4af71-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4af71-104">Политика возврата канала в Dynamics 365 Commerce позволяет компаниям устанавливать ограничения на то, какие платежные средства могут быть разрешены для обработки возврата на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="4af71-104">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="4af71-105">В этой теме описываются шаги, как настроить политику возврата товаров и возврата денег для канала.</span><span class="sxs-lookup"><span data-stu-id="4af71-105">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="4af71-106">Область политики в настоящее время ограничена настройкой предложений платежа, которые могут быть разрешены для канала.</span><span class="sxs-lookup"><span data-stu-id="4af71-106">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="4af71-107">Список "разрешено" основан на способах оплаты, используемых для совершения покупки.</span><span class="sxs-lookup"><span data-stu-id="4af71-107">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="4af71-108">Пример:</span><span class="sxs-lookup"><span data-stu-id="4af71-108">For example:</span></span>

- <span data-ttu-id="4af71-109">Если покупка была сделана с помощью подарочного сертификата, политика магазина заключается только в обработке возвратов в виде нового подарочного сертификата или предоставления кредита от магазина.</span><span class="sxs-lookup"><span data-stu-id="4af71-109">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="4af71-110">Если продажа осуществляется с помощью наличных денег, разрешенными вариантами для возврата денег являются наличные деньги, подарочный сертификат и счет клиента, но не кредитные карты.</span><span class="sxs-lookup"><span data-stu-id="4af71-110">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="4af71-111">Включить политику возврата</span><span class="sxs-lookup"><span data-stu-id="4af71-111">Enable return policy</span></span>

<span data-ttu-id="4af71-112">Чтобы включить функцию политики возврата канала, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4af71-112">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="4af71-113">Откройте рабочую область **Управление функциями** в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4af71-113">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="4af71-114">В списке имен найдите функцию **Включить политики возврата канала**.</span><span class="sxs-lookup"><span data-stu-id="4af71-114">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="4af71-115">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="4af71-115">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="4af71-116">Настройка политики возврата</span><span class="sxs-lookup"><span data-stu-id="4af71-116">Configure return policy</span></span>

<span data-ttu-id="4af71-117">Выполните следующие действия, чтобы настроить политику возврата для розничного магазина или канала интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="4af71-117">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="4af71-118">Перейдите **Retail и Commerce** \> **Настройка канала** \> **Возвраты** \> **Политика возврата канала**.</span><span class="sxs-lookup"><span data-stu-id="4af71-118">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="4af71-119">Выберите **Создать** для создания нового шаблона политики возврата.</span><span class="sxs-lookup"><span data-stu-id="4af71-119">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="4af71-120">Для использования существующего шаблона выберите шаблон в левой области.</span><span class="sxs-lookup"><span data-stu-id="4af71-120">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="4af71-121">Для новых шаблонов добавьте имя и описание, которые помогут определить политику и ее применение к каналу.</span><span class="sxs-lookup"><span data-stu-id="4af71-121">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="4af71-122">![Добавление новой политики возврата](media/Return-policy-page1.png "Добавление новой политики возврата")</span><span class="sxs-lookup"><span data-stu-id="4af71-122">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="4af71-123">В разделе **Разрешенные способы оплаты возвратов** задайте предложения платежа по возврату как **Разрешить** для каждого способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="4af71-123">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="4af71-124">![Добавление способов оплаты](media/Return-policy-page2.PNG "Задание разрешенных способов оплаты для каждого типа платежа")</span><span class="sxs-lookup"><span data-stu-id="4af71-124">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="4af71-125">Способы оплаты заимствуются из способов оплаты, установленных для организации.</span><span class="sxs-lookup"><span data-stu-id="4af71-125">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="4af71-126">Добавление разрешенного типа предложения по возврату для каждого указанного способа оплаты обеспечит возможность возврата согласно разрешенному типу предложения возврата.</span><span class="sxs-lookup"><span data-stu-id="4af71-126">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="4af71-127">Свяжите шаблон политики возвратов с магазинами, в которых он будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="4af71-127">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="4af71-128">Выберите **Добавить** на вкладке **Каналы розничной торговли** и свяжите доступные каналы.</span><span class="sxs-lookup"><span data-stu-id="4af71-128">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="4af71-129">В диалоговом окне **Выбор узлов организации** выберите магазины, регионы и организации, с которыми должен быть связан шаблон.</span><span class="sxs-lookup"><span data-stu-id="4af71-129">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="4af71-130">С каждым магазином можно связать только один шаблон политики возвратов.</span><span class="sxs-lookup"><span data-stu-id="4af71-130">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="4af71-131">С помощью кнопок со стрелками выберите магазины, регионы или организации.</span><span class="sxs-lookup"><span data-stu-id="4af71-131">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="4af71-132">Дата вступления в силу политики будет датой, когда политики применяются к каналам и выполняются задания канала.</span><span class="sxs-lookup"><span data-stu-id="4af71-132">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="4af71-133">![Диалоговое окно выборы узлов организации](media/Return-policy-page3.PNG "Диалоговое окно выборы узлов организации")</span><span class="sxs-lookup"><span data-stu-id="4af71-133">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="4af71-134">На странице **График распределения** выполните задание **1070**, чтобы сделать политику возврата канала доступной для POS.</span><span class="sxs-lookup"><span data-stu-id="4af71-134">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="4af71-135">Предварительный просмотр политики возвратов канала в POS-терминале</span><span class="sxs-lookup"><span data-stu-id="4af71-135">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="4af71-136">Выполните шаги из одного из следующих примеров, чтобы просмотреть разрешенные типы предложений возврата в POS.</span><span class="sxs-lookup"><span data-stu-id="4af71-136">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="4af71-137">Выполните вход в POS-терминал в качестве кассира или менеджера.</span><span class="sxs-lookup"><span data-stu-id="4af71-137">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="4af71-138">В области **Смена и денежный ящик** выберите **Показать журнал**.</span><span class="sxs-lookup"><span data-stu-id="4af71-138">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="4af71-139">Выберите проводку, которая является частью возврата.</span><span class="sxs-lookup"><span data-stu-id="4af71-139">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="4af71-140">Выберите номенклатуры для возмещения и выберите способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="4af71-140">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="4af71-141">Если выбранное предложение платежа относится к списку разрешенных предложения платежа, кассир может выполнить проводку.</span><span class="sxs-lookup"><span data-stu-id="4af71-141">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="4af71-142">Если выбранное предложение платежа не разрешено, будет выведено сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4af71-142">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="4af71-143">Выберите **Сумма к оплате**, чтобы открыть список всех допустимых типов предложений платежа по возврату.</span><span class="sxs-lookup"><span data-stu-id="4af71-143">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="4af71-144">–или–</span><span class="sxs-lookup"><span data-stu-id="4af71-144">-or-</span></span>

1. <span data-ttu-id="4af71-145">Выполните вход в POS-терминал в качестве кассира или менеджера.</span><span class="sxs-lookup"><span data-stu-id="4af71-145">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="4af71-146">Выберите **Проводка возврата** и введите код чека, используя сканер штрих-кода или запись вручную.</span><span class="sxs-lookup"><span data-stu-id="4af71-146">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="4af71-147">Выберите проводку, которая является частью возврата.</span><span class="sxs-lookup"><span data-stu-id="4af71-147">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="4af71-148">Выберите номенклатуры для возмещения и выберите способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="4af71-148">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="4af71-149">Если выбранное предложение платежа относится к списку разрешенных предложения платежа, кассир может выполнить проводку.</span><span class="sxs-lookup"><span data-stu-id="4af71-149">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="4af71-150">Если выбранное предложение платежа не разрешено, будет выведено сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4af71-150">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="4af71-151">Выберите **Сумма к оплате**, чтобы открыть список всех допустимых типов предложений платежа по возврату.</span><span class="sxs-lookup"><span data-stu-id="4af71-151">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="4af71-152">![Возмещение не разрешено](media/Return-policy-page6.png "Тип возврата запрещен")</span><span class="sxs-lookup"><span data-stu-id="4af71-152">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="4af71-153">![Список способов оплаты](media/Return-policy-page5.PNG "Тип возврата разрешен")</span><span class="sxs-lookup"><span data-stu-id="4af71-153">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
