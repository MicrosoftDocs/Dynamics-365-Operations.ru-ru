---
title: Настройка ресурсов Azure для аналитики Интернета вещей
description: В этом разделе объясняется, как создать и настроить ресурсы Microsoft Azure, необходимые для работы с аналитики Интернета вещей.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 33c28f8e7982c6ec9b892e975525de69fc637892
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881380"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="98479-103">Настройка ресурсов Azure для аналитики Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="98479-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98479-104">В этом разделе объясняется, как создать и настроить ресурсы Microsoft Azure, необходимые для работы с аналитики Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="98479-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="98479-105">Создание ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="98479-105">Create Azure resources</span></span>

<span data-ttu-id="98479-106">Выполните следующие действия, чтобы создать узел Интернета вещей, кэш Redis и хранилище ключей, доступ к которым можно получить, используя Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="98479-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="98479-107">Убедитесь, что код собственного приложения Microsoft Dynamics ERP Microservices используется в вашем клиенте</span><span class="sxs-lookup"><span data-stu-id="98479-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="98479-108">Чтобы убедиться в том, что код приложения для собственного приложения Microsoft Dynamics ERP Microservices находится в вашем клиенте, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="98479-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="98479-109">Выполните вход на портал Azure по адресу <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="98479-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="98479-110">Перейдите на страницу **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="98479-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="98479-111">Перейдите к **Корпоративные приложения**.</span><span class="sxs-lookup"><span data-stu-id="98479-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="98479-112">В поле **Тип приложения** выберите **приложения Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="98479-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="98479-113">В поле поиска введите **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="98479-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="98479-114">Убедитесь, что **Microsoft Dynamics ERP Microservices** в списке.</span><span class="sxs-lookup"><span data-stu-id="98479-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="98479-115">Другие приложения имеют похожие имена.</span><span class="sxs-lookup"><span data-stu-id="98479-115">Other applications have similar names.</span></span> <span data-ttu-id="98479-116">Поэтому, убедитесь, что вы нашли соответствующее приложение.</span><span class="sxs-lookup"><span data-stu-id="98479-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="98479-117">Код приложения — **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="98479-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="98479-118">Если приложение отсутствует в списке, его необходимо добавить в клиент:</span><span class="sxs-lookup"><span data-stu-id="98479-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="98479-119">На портале Azure на панели инструментов нажмите кнопку, чтобы открыть Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="98479-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="98479-120">Выполните команду **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="98479-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="98479-121">Введите **Y**, чтобы установить модуль.</span><span class="sxs-lookup"><span data-stu-id="98479-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="98479-122">Выполните команду **Get-InstalledModule -Name "AzureAD"**, чтобы убедиться, что модуль установлен.</span><span class="sxs-lookup"><span data-stu-id="98479-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="98479-123">Выполните команду **Connect-AzureAD -Confirm**, чтобы выполнить проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="98479-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="98479-124">Выполните команду **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="98479-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="98479-125">Теперь можно повторить шаги с 1 по 6 для проверки того, что код приложения находится в вашем клиенте.</span><span class="sxs-lookup"><span data-stu-id="98479-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="98479-126">Создание ресурса хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="98479-126">Create a key vault resource</span></span>

<span data-ttu-id="98479-127">Чтобы создать ресурс хранилища ключей, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="98479-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="98479-128">На портале Azure создайте или перейдите к группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98479-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="98479-129">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="98479-129">Select **Add**.</span></span>
3. <span data-ttu-id="98479-130">На странице **Создать** в поле поиска введите **хранилище ключей**.</span><span class="sxs-lookup"><span data-stu-id="98479-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="98479-131">Затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98479-131">Then select **Create**.</span></span>
4. <span data-ttu-id="98479-132">На странице **Создание хранилища ключей** в поле **имя хранилища ключей** введите имя.</span><span class="sxs-lookup"><span data-stu-id="98479-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="98479-133">Просмотрите значения по умолчанию, а затем выберите **Просмотреть + создать**.</span><span class="sxs-lookup"><span data-stu-id="98479-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="98479-134">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98479-134">Select **Create**.</span></span>

<span data-ttu-id="98479-135">Хранилище ключей создается в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="98479-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="98479-136">Создание ресурса узла Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="98479-136">Create an IoT hub resource</span></span>

<span data-ttu-id="98479-137">Чтобы создать ресурс узла Интернета вещей, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="98479-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="98479-138">Создайте или перейдите к группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98479-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="98479-139">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="98479-139">Select **Add**.</span></span>
3. <span data-ttu-id="98479-140">На странице **Создать** в поле поиска введите **узел Интернета вещей**.</span><span class="sxs-lookup"><span data-stu-id="98479-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="98479-141">Затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98479-141">Then select **Create**.</span></span>
4. <span data-ttu-id="98479-142">В поле **Имя узла Интернета вещей** введите имя.</span><span class="sxs-lookup"><span data-stu-id="98479-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="98479-143">Просмотрите значения по умолчанию, а затем выберите **Просмотреть + создать**.</span><span class="sxs-lookup"><span data-stu-id="98479-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="98479-144">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98479-144">Select **Create**.</span></span>

<span data-ttu-id="98479-145">Узел Интернета вещей создается в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="98479-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="98479-146">Рекомендуется создавать только один ресурс узла Интернета вещей для каждой среды.</span><span class="sxs-lookup"><span data-stu-id="98479-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="98479-147">Создание ресурса кэша Redis</span><span class="sxs-lookup"><span data-stu-id="98479-147">Create a Redis cache resource</span></span>

<span data-ttu-id="98479-148">Чтобы создать ресурс кэша Redis, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="98479-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="98479-149">Создайте или перейдите к группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98479-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="98479-150">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="98479-150">Select **Add**.</span></span>
3. <span data-ttu-id="98479-151">На странице **Создать** в поле поиска введите **Кэш Azure для Redis**.</span><span class="sxs-lookup"><span data-stu-id="98479-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="98479-152">Затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98479-152">Then select **Create**.</span></span>
4. <span data-ttu-id="98479-153">В поле **Имя DNS** введите имя.</span><span class="sxs-lookup"><span data-stu-id="98479-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="98479-154">Просмотрите значения по умолчанию, а затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98479-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="98479-155">Кэш Redis создается в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="98479-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="98479-156">Рекомендуется создавать только один кэш Redis для каждой среды.</span><span class="sxs-lookup"><span data-stu-id="98479-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="98479-157">Все ресурсы будут созданы.</span><span class="sxs-lookup"><span data-stu-id="98479-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="98479-158">Настройка ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="98479-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="98479-159">Настройка узла Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="98479-159">Configure the IoT hub</span></span>

<span data-ttu-id="98479-160">Выполните следующие действия, чтобы настроить узел Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="98479-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="98479-161">В ресурсах выберите ресурс узла Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="98479-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="98479-162">В левой области навигации выберите **встроенные конечные точки**.</span><span class="sxs-lookup"><span data-stu-id="98479-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="98479-163">В **группы потребителей** вставьте следующие группы потребителей.</span><span class="sxs-lookup"><span data-stu-id="98479-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="98479-164">Эти группы потребителей соответствуют готовым сценариям.</span><span class="sxs-lookup"><span data-stu-id="98479-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="98479-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="98479-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="98479-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="98479-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="98479-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="98479-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="98479-168">Настройка хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="98479-168">Configure the key vault</span></span>

<span data-ttu-id="98479-169">Чтобы настроить хранилище ключей, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="98479-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="98479-170">В ресурсах выберите ресурс хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="98479-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="98479-171">В левой области переходов выберите **политики доступа**.</span><span class="sxs-lookup"><span data-stu-id="98479-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="98479-172">Выберите **Добавить политику доступа**.</span><span class="sxs-lookup"><span data-stu-id="98479-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="98479-173">На странице **Добавить политику доступа** в поле **секретные разрешения** выберите значение **получить** и **список**.</span><span class="sxs-lookup"><span data-stu-id="98479-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="98479-174">Щелкните **Выбрать доверителя**.</span><span class="sxs-lookup"><span data-stu-id="98479-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="98479-175">В диалоговом окне **Доверитель** выполните поиск и выберите **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="98479-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="98479-176">Затем выберите **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="98479-176">Then select **Select**.</span></span>
7. <span data-ttu-id="98479-177">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="98479-177">Select **Add**.</span></span>
8. <span data-ttu-id="98479-178">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="98479-178">Select **Save**.</span></span>

<span data-ttu-id="98479-179">У приложения есть доступ к секретам в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="98479-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="98479-180">Сохраните секрет для строки подключения к узлу Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="98479-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="98479-181">Чтобы сохранить секрет для строки подключения к узлу Интернета вещей, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="98479-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="98479-182">В ресурсах выберите ресурс узла Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="98479-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="98479-183">В левой области навигации выберите **встроенные конечные точки**.</span><span class="sxs-lookup"><span data-stu-id="98479-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="98479-184">Скопируйте значение в поле **Конечная точка, совместимая с центром событий**.</span><span class="sxs-lookup"><span data-stu-id="98479-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="98479-185">Перейдите к ресурсу хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="98479-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="98479-186">В левой области переходов выберите **Секреты**.</span><span class="sxs-lookup"><span data-stu-id="98479-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="98479-187">Выберите **Создать/Импортировать**.</span><span class="sxs-lookup"><span data-stu-id="98479-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="98479-188">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="98479-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="98479-189">В поле **значение** вставьте ранее скопированное значение конечной точки.</span><span class="sxs-lookup"><span data-stu-id="98479-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="98479-190">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98479-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="98479-191">Сохраните секрет для строки подключения к кэшу Redis</span><span class="sxs-lookup"><span data-stu-id="98479-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="98479-192">Чтобы сохранить секрет для строки подключения к кэшу Redis, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="98479-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="98479-193">В ресурсах выберите ресурс кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="98479-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="98479-194">Выбор **ключей доступа**.</span><span class="sxs-lookup"><span data-stu-id="98479-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="98479-195">Скопируйте значение в поле **первичная строка подключения**.</span><span class="sxs-lookup"><span data-stu-id="98479-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="98479-196">Перейдите к ресурсу хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="98479-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="98479-197">В левой области переходов выберите **Секреты**.</span><span class="sxs-lookup"><span data-stu-id="98479-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="98479-198">Выберите **Создать/Импортировать**.</span><span class="sxs-lookup"><span data-stu-id="98479-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="98479-199">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="98479-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="98479-200">В поле **значение** вставьте ранее скопированное строку подключения.</span><span class="sxs-lookup"><span data-stu-id="98479-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="98479-201">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98479-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="98479-202">Когда обновляется одна из строк подключения, необходимо также обновить значения секрета.</span><span class="sxs-lookup"><span data-stu-id="98479-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="98479-203">Теперь подготовка необходимых ресурсов Azure завершена.</span><span class="sxs-lookup"><span data-stu-id="98479-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="98479-204">Следующий шаг состоит в [установке надстройки аналитики Интернета вещей в Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="98479-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
