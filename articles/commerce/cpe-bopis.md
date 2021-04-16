---
title: Настройка BOPIS в ознакомительной среде Dynamics 365 Commerce
description: В этой теме объясняется, как настроить сценарий "купить в интернете, забрать в магазине" (BOPIS) в среде оценки Microsoft Dynamics 365 Commerce после ее подготовки.
author: rubendel
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 219504da62fd4637ed01f9acbab32f873cef81b0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795963"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="02d5e-103">Настройка сценария BOPIS (купить в Интернете, забрать в магазине) в среде оценки Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="02d5e-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="02d5e-104">В этой теме объясняется, как настроить сценарий "купить в интернете, забрать в магазине" (BOPIS) в среде оценки Microsoft Dynamics 365 Commerce после подготовки этой среды.</span><span class="sxs-lookup"><span data-stu-id="02d5e-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="02d5e-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="02d5e-105">Prerequisite</span></span>

<span data-ttu-id="02d5e-106">Выполните процедуры в этой теме только после того, как ваша ознакомительная среда Commerce была создана и настроена.</span><span class="sxs-lookup"><span data-stu-id="02d5e-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="02d5e-107">Для получения информации о том, как подготовить и настроить среду, см. разделы [Подготовка ознакомительной среды Dynamics 365 Commerce](provisioning-guide.md) и [Настройка ознакомительной среды Dynamics 365 Commerce](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span><span class="sxs-lookup"><span data-stu-id="02d5e-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="02d5e-108">После того как ваша среда Commerce подготовлена и полностью настроена, эту тему можно использовать для включения сценариев BOPIS.</span><span class="sxs-lookup"><span data-stu-id="02d5e-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="02d5e-109">Настройка POS-терминала</span><span class="sxs-lookup"><span data-stu-id="02d5e-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="02d5e-110">Настройка Modern POS</span><span class="sxs-lookup"><span data-stu-id="02d5e-110">Configure Modern POS</span></span>

<span data-ttu-id="02d5e-111">Сценарии BOPIS, в которых участвует платеж по кредитной карте, требуют наличия станции оборудования.</span><span class="sxs-lookup"><span data-stu-id="02d5e-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="02d5e-112">Станция оборудования встроена в клиенты Modern POS для Windows и Android.</span><span class="sxs-lookup"><span data-stu-id="02d5e-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="02d5e-113">Если вы используете Cloud POS или Modern POS для iOS, клиент POS должен составлять пару с общей аппаратной станцией.</span><span class="sxs-lookup"><span data-stu-id="02d5e-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="02d5e-114">В этой теме объясняется, как настроить BOPIS для клиентов Windows и Android.</span><span class="sxs-lookup"><span data-stu-id="02d5e-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="02d5e-115">Сведения о том, как настроить общую станцию оборудования, см. в разделе [Настройка и установка Retail Hardware Station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="02d5e-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="02d5e-116">Перейдите в раздел **Розничная торговля и коммерция \> Настройка канала \> Настройка POS \> Регистры**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="02d5e-117">Выберите регистр **SANFRAN-5**, затем выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="02d5e-118">Измените значение поля **Профиль оборудования** с **HW002** на **HW001**, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="02d5e-119">Чтобы синхронизировать изменения, выберите **Розничная торговля и коммерция \> ИТ розничной торговли и коммерции \> График распределения**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="02d5e-120">Выберите план распределения **1090**, затем, на панели действий, выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="02d5e-121">Выберите **Да**, затем **OK**, чтобы начать синхронизацию данных.</span><span class="sxs-lookup"><span data-stu-id="02d5e-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="02d5e-122">Установка Modern POS</span><span class="sxs-lookup"><span data-stu-id="02d5e-122">Install Modern POS</span></span>

1. <span data-ttu-id="02d5e-123">Перейдите в раздел **Розничная торговля и коммерция \> Настройка канала \> Настройка POS \> Устройства**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="02d5e-124">Выберите устройство **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="02d5e-125">На панели операций выберите **Загрузить**, затем выберите **Файл конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="02d5e-126">Выберите **Загрузить**, затем выберите **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="02d5e-127">После завершения загрузки файла **ModernPOSSetup.exe** выберите **Открыть файл**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Открыть файл](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="02d5e-129">Выберите **Далее**, чтобы пройти процесс установки.</span><span class="sxs-lookup"><span data-stu-id="02d5e-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="02d5e-130">После завершения установки выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="02d5e-131">Активация Modern POS</span><span class="sxs-lookup"><span data-stu-id="02d5e-131">Activate Modern POS</span></span>

1. <span data-ttu-id="02d5e-132">На рабочем столе Windows нажмите кнопку **Пуск** и введите **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="02d5e-133">Выберите приложение **Retail Modern POS**, для которого начать активацию.</span><span class="sxs-lookup"><span data-stu-id="02d5e-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="02d5e-134">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-134">Select **Next**.</span></span> <span data-ttu-id="02d5e-135">Поля **URL-адрес сервера**, **ИД устройства** и **Номер регистра** должны быть предварительно установлены с использованием сведений из файла конфигурации, загруженного в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="02d5e-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="02d5e-136">Выберите **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-136">Select **Activate**.</span></span>
5. <span data-ttu-id="02d5e-137">Появляется диалоговое окно проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="02d5e-137">An authentication dialog box appears.</span></span> <span data-ttu-id="02d5e-138">Выберите счет, который использует адрес электронной почты, который ранее был связан с сотрудником **000713 — Эндрю Коллетт**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="02d5e-139">Если сотрудник еще не сопоставлен с вашим удостоверением, активация будет неудачной.</span><span class="sxs-lookup"><span data-stu-id="02d5e-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="02d5e-140">В этом случае выполните действия, указанные в разделе "Связывание работника с вашим удостоверением" в теме [Настройка ознакомительной среды Dynamics 365 Commerce](cpe-post-provisioning.md#associate-a-worker-with-your-identity).</span><span class="sxs-lookup"><span data-stu-id="02d5e-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="02d5e-141">Когда появится приглашение, предлагающее разрешить вашей организации управление устройством, выберите **Только это приложение**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="02d5e-142">После завершения активации выберите **Начать работу**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="02d5e-143">Включение BOPIS в Modern POS</span><span class="sxs-lookup"><span data-stu-id="02d5e-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="02d5e-144">Войдите в Modern POS, используя **000713** в качестве идентификатора оператора и **123** в качестве пароля.</span><span class="sxs-lookup"><span data-stu-id="02d5e-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="02d5e-145">В процессе воспроизведения видео с вводным пошаговым руководством установите два флажка в нижнем левом углу диалогового окна, затем закройте это диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="02d5e-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="02d5e-146">Если не выводится запрос на закрытие смены, перейдите вправо на странице **Добро пожаловать**, выберите **Закрыть смену**, затем снова выполните вход в POS-терминал.</span><span class="sxs-lookup"><span data-stu-id="02d5e-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="02d5e-147">После входа в ответ на запрос выберите **Выполнение операций, не связанных с кассовым лотком**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="02d5e-148">На странице **Добро пожаловать** прокрутите вправо и выберите операцию **Выбрать станцию оборудования**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="02d5e-149">Выберите **Управление**, установите для параметра **Использовать станцию оборудование** значение **Вкл.**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="02d5e-150">Выйдите из POS, затем снова войдите в нее.</span><span class="sxs-lookup"><span data-stu-id="02d5e-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="02d5e-151">После входа выберите **Открыть новую смену**, затем выберите **Ящик**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="02d5e-152">Завершение сценария BOPIS</span><span class="sxs-lookup"><span data-stu-id="02d5e-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="02d5e-153">Создание заказа в магазине для получения в магазине</span><span class="sxs-lookup"><span data-stu-id="02d5e-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="02d5e-154">Перейдите по URL-адресу, указанному на этапе [Инициализация электронной коммерции](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) во время конфигурации среды.</span><span class="sxs-lookup"><span data-stu-id="02d5e-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="02d5e-155">Выберите номенклатуру и выберите **Добавить в корзину**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="02d5e-156">На странице корзины выберите пункт **Забрать это** для строки заказа, которая была только что добавлена.</span><span class="sxs-lookup"><span data-stu-id="02d5e-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="02d5e-157">В диалоговом окне **Выбор магазина** введите **Сан-Франциско**, затем выберите кнопку **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="02d5e-158">В списке результатов найдите магазин в Сан-Франциско и выберите **Забрать здесь**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="02d5e-159">На странице корзины выберите **Оформить как гость**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="02d5e-160">Чтобы продолжить оформление, необходимо принять оповещение о файлах cookie.</span><span class="sxs-lookup"><span data-stu-id="02d5e-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="02d5e-161">Это уведомление появляется в виде баннера в верхней части страницы оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="02d5e-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="02d5e-162">Для метода платежа кредитной картой введите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="02d5e-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="02d5e-163">**Имя владельца карты:** введите любое имя.</span><span class="sxs-lookup"><span data-stu-id="02d5e-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="02d5e-164">**Номер карты:** введите **4111-1111-1111-1111**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="02d5e-165">**Срок действия:** введите **10/20**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="02d5e-166">**Контрольный код карты (CVV):** введите **737**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="02d5e-167">Никогда не следует пытаться использовать фактические сведения кредитной карты на тестовых сайтах при любых обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="02d5e-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="02d5e-168">Продолжите оформление, введя подробные данные об адресе для выставления счета, затем выберите **Сохранить и продолжить**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="02d5e-169">Когда заказ готов к размещению, выберите **Оформить**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="02d5e-170">Синхронизация интернет-заказов с бек-офисом</span><span class="sxs-lookup"><span data-stu-id="02d5e-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="02d5e-171">Сведения о синхронизации интернет-заказов см. в разделе [Разноска продаж и платежей через Интернет](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span><span class="sxs-lookup"><span data-stu-id="02d5e-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="02d5e-172">Получение заказа в магазине</span><span class="sxs-lookup"><span data-stu-id="02d5e-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="02d5e-173">Войдите в POS.</span><span class="sxs-lookup"><span data-stu-id="02d5e-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="02d5e-174">На экране **Добро пожаловать** выберите **Выполнение заказа**</span><span class="sxs-lookup"><span data-stu-id="02d5e-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="02d5e-175">В списке номенклатур для получения выберите строку из заказа, который был размещен через Интернет.</span><span class="sxs-lookup"><span data-stu-id="02d5e-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="02d5e-176">Когда выбрана строка заказа, выберите **Скомплектовать**.</span><span class="sxs-lookup"><span data-stu-id="02d5e-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="02d5e-177">Номенклатура строки добавляется на экран проводки, и сумма **$0,00** отображается в качестве сальдо, которое должно быть оплачено.</span><span class="sxs-lookup"><span data-stu-id="02d5e-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="02d5e-178">Выберите подлежащее оплате сальдо **$0,00** или выберите любой метод платежа для завершения проводки.</span><span class="sxs-lookup"><span data-stu-id="02d5e-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="02d5e-179">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="02d5e-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="02d5e-180">Интернет-заказы, извлеченные в POS, имеют ненулевое дебетовое сальдо</span><span class="sxs-lookup"><span data-stu-id="02d5e-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="02d5e-181">Когда заказ извлекается для получения в магазине, если дебетовое сальдо не равно 0 (нулю), убедитесь, что используется Modern POS и что станция оборудования активна.</span><span class="sxs-lookup"><span data-stu-id="02d5e-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="02d5e-182">Если используется Cloud POS или Modern POS для iOS, убедитесь, что активна общая станция оборудования.</span><span class="sxs-lookup"><span data-stu-id="02d5e-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="02d5e-183">Для получения платежей, которые были сделаны в Интернете, требуется какая-то активная станция оборудования.</span><span class="sxs-lookup"><span data-stu-id="02d5e-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="02d5e-184">Общие проблемы при записи платежа</span><span class="sxs-lookup"><span data-stu-id="02d5e-184">General issues with payment capture</span></span>

<span data-ttu-id="02d5e-185">Для всех общих вопросов сначала следует всегда обращаться к журналам событий Modern POS или станции оборудования IIS Hardware Station.</span><span class="sxs-lookup"><span data-stu-id="02d5e-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="02d5e-186">Эти журналы можно найти в следующих узлах журнала событий Windows:</span><span class="sxs-lookup"><span data-stu-id="02d5e-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="02d5e-187">Журналы приложений и служб \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="02d5e-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="02d5e-188">Журналы приложений и служб \> Microsoft \> Dynamics \> Commerce-Hardware Station</span><span class="sxs-lookup"><span data-stu-id="02d5e-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="02d5e-189">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="02d5e-189">Additional resources</span></span>

[<span data-ttu-id="02d5e-190">Обзор ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="02d5e-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="02d5e-191">Подготовка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="02d5e-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="02d5e-192">Настройка дополнительных функций ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="02d5e-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="02d5e-193">Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="02d5e-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="02d5e-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="02d5e-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="02d5e-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="02d5e-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="02d5e-196">Портал Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="02d5e-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="02d5e-197">Веб-сайт Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="02d5e-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="02d5e-198">Соединитель платежей Adyen</span><span class="sxs-lookup"><span data-stu-id="02d5e-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="02d5e-199">Сохранение интерактивных платежных инструментов с помощью соединителя Adyen</span><span class="sxs-lookup"><span data-stu-id="02d5e-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="02d5e-200">Обзор многоканальных платежей</span><span class="sxs-lookup"><span data-stu-id="02d5e-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)


[!INCLUDE[footer-include](../includes/footer-banner.md)]