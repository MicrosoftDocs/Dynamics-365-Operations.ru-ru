---
title: Начало работы с администрированием службы надстройки "Электронное выставление счетов"
description: В этой теме объясняется, как начать работать с надстройкой электронного выставления накладных.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592534"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="3dd05-103">Начало работы с администрированием службы надстройки "Электронное выставление счетов"</span><span class="sxs-lookup"><span data-stu-id="3dd05-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="3dd05-104">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="3dd05-104">Prerequisites</span></span>

<span data-ttu-id="3dd05-105">Перед выполнением процедур из данной темы необходимо выполнить следующие предварительные требования:</span><span class="sxs-lookup"><span data-stu-id="3dd05-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="3dd05-106">Необходимо иметь доступ к учетной записи Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3dd05-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="3dd05-107">Необходим проект LCS, включающий версию 10.0.17 или более позднюю версию Microsoft Dynamics 365 Finance и Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3dd05-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3dd05-108">Кроме того, эти приложения должны быть развернуты в одном из следующих географических регионов Azure:</span><span class="sxs-lookup"><span data-stu-id="3dd05-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="3dd05-109">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="3dd05-109">East US</span></span>
    - <span data-ttu-id="3dd05-110">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="3dd05-110">West US</span></span>
    - <span data-ttu-id="3dd05-111">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="3dd05-111">North EU</span></span>
    - <span data-ttu-id="3dd05-112">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="3dd05-112">West EU</span></span>

- <span data-ttu-id="3dd05-113">Необходимо иметь доступ к учетной записи службы Dynamics 365 Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="3dd05-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="3dd05-114">Необходимо активировать функцию глобализации для вашей учетной записи RCS в управлении функциями.</span><span class="sxs-lookup"><span data-stu-id="3dd05-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="3dd05-115">Дополнительные сведения см. в разделе [Regulatory Configuration Services (RCS) — функции глобализации](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="3dd05-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="3dd05-116">Необходимо создать Key Vault и учетную запись хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd05-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="3dd05-117">Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="3dd05-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="3dd05-118">Установка надстройки для микрослужб в Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="3dd05-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="3dd05-119">Войдите в учетную запись LCS.</span><span class="sxs-lookup"><span data-stu-id="3dd05-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="3dd05-120">Выберите плитку **Управление предварительными версиями функций**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="3dd05-121">В разделе **Общедоступные предварительные версии функций** выберите **Служба электронного выставления накладных**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="3dd05-122">Убедитесь, что для параметра **Предварительная версия функции включена** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="3dd05-123">На панели мониторинга LCS выберите проект развертывания LCS.</span><span class="sxs-lookup"><span data-stu-id="3dd05-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="3dd05-124">Должен быть выполнен проект LCS.</span><span class="sxs-lookup"><span data-stu-id="3dd05-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="3dd05-125">На вкладке **Надстройки сред** выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="3dd05-126">Выберите **Службы электронного выставления накладных** и в поле **Код приложения AAD** введите **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="3dd05-127">Это фиксированное значение.</span><span class="sxs-lookup"><span data-stu-id="3dd05-127">This is a fixed value.</span></span>
10. <span data-ttu-id="3dd05-128">В поле **Код клиента AAD** введите код клиента вашей учетной записи подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd05-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="3dd05-129">Ознакомьтесь с условиями и установите флажок.</span><span class="sxs-lookup"><span data-stu-id="3dd05-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="3dd05-130">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="3dd05-131">Настройка параметров для интеграции RCS с надстройкой электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="3dd05-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="3dd05-132">Войдите в учетную запись RCS.</span><span class="sxs-lookup"><span data-stu-id="3dd05-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="3dd05-133">В рабочей области **Электронная отчетность** в разделе **Связанные ссылки** выберите **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="3dd05-134">На вкладке **Служба электронного выставления накладных** в поле **URI конечной точки службы** введите соответствующую конечную точку службы для своего географического расположения Azure, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3dd05-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="3dd05-135">География центра обработки данных Azure</span><span class="sxs-lookup"><span data-stu-id="3dd05-135">Datacenter Azure geography</span></span> | <span data-ttu-id="3dd05-136">Универсальный код ресурса (URI) конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="3dd05-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="3dd05-137">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="3dd05-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3dd05-138">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="3dd05-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3dd05-139">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="3dd05-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3dd05-140">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="3dd05-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="3dd05-141">Убедитесь, что в поле **Код приложения** установлено значение **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="3dd05-142">Это значение является фиксированным значением.</span><span class="sxs-lookup"><span data-stu-id="3dd05-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="3dd05-143">В поле **Код среды LCS** введите идентификатор вашей учетной записи подписки LCS.</span><span class="sxs-lookup"><span data-stu-id="3dd05-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="3dd05-144">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3dd05-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="3dd05-145">Создание секрета Key Vault</span><span class="sxs-lookup"><span data-stu-id="3dd05-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="3dd05-146">Войдите в учетную запись RCS.</span><span class="sxs-lookup"><span data-stu-id="3dd05-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="3dd05-147">В рабочей области **Функция глобализации** в разделе **Среда** выберите плитку **Дополнение электронных накладных**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="3dd05-148">На странице **Настройки среды** на панели действий выберите **Среда службы**, затем выберите **Параметры Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="3dd05-149">Выберите **Создать**, чтобы создать секрет Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3dd05-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="3dd05-150">В поле **Имя** введите имя секрета Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3dd05-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="3dd05-151">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="3dd05-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="3dd05-152">В поле **URI Key Vault** вставьте секрет из Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3dd05-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="3dd05-153">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="3dd05-154">Создание секрета учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="3dd05-154">Create Storage account secret</span></span>

1. <span data-ttu-id="3dd05-155">Перейдите в раздел **Администрирование системы** > **Настройка** > **Параметры Key Vault** и выберите секрет Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3dd05-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="3dd05-156">В разделе **Сертификаты** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="3dd05-157">В поле **имя** введите имя секрета учетной записи хранения, а в поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="3dd05-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="3dd05-158">В поле **Тип** выберите **Сертификат**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="3dd05-159">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3dd05-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="3dd05-160">Создайте секрет для цифрового сертификата</span><span class="sxs-lookup"><span data-stu-id="3dd05-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="3dd05-161">Перейдите в раздел **Администрирование системы** > **Настройка** > **Параметры Key Vault** и выберите секрет Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3dd05-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="3dd05-162">В разделе **Сертификаты** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="3dd05-163">В поле **имя** введите имя секрета для цифрового сертификата, а в поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="3dd05-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="3dd05-164">В поле **Тип** выберите **Сертификат**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="3dd05-165">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3dd05-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="3dd05-166">Создание среды надстройки электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="3dd05-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="3dd05-167">Войдите в учетную запись RCS.</span><span class="sxs-lookup"><span data-stu-id="3dd05-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="3dd05-168">В рабочей области **Функция глобализации** в разделе **Среда** выберите плитку **Дополнение электронных накладных**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="3dd05-169">Создание среды службы</span><span class="sxs-lookup"><span data-stu-id="3dd05-169">Create a service environment</span></span>

1. <span data-ttu-id="3dd05-170">На странице **Настройки среды** на панели действий выберите **Среда службы**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="3dd05-171">Выберите **Создать** для создания новой среды службы.</span><span class="sxs-lookup"><span data-stu-id="3dd05-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="3dd05-172">В поле **Имя** введите имя среды электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3dd05-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="3dd05-173">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="3dd05-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="3dd05-174">В поле **Секрет маркера SAS хранилища** выберите имя секрета учетной записи хранения, который должен использоваться для проверки подлинности доступа к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3dd05-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="3dd05-175">В разделе **Пользователи** выберите **Добавить**, чтобы добавить пользователя, которому разрешено отправлять электронные накладные через среду, а также подключиться к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3dd05-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="3dd05-176">В поле **Код пользователя** введите псевдоним пользователя.</span><span class="sxs-lookup"><span data-stu-id="3dd05-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="3dd05-177">В поле **Электронная почта** введите адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="3dd05-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="3dd05-178">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-178">Select **Save**.</span></span>
8. <span data-ttu-id="3dd05-179">Если в накладных для конкретной страны/региона требуется цепочка сертификатов для применения цифровых подписей, на панели действий выберите **Параметры Key Vault**, затем выберите **Цепочка сертификатов** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3dd05-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="3dd05-180">Для создания цепочки сертификатов выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="3dd05-181">В поле **Имя** введите имя цепочки сертификатов.</span><span class="sxs-lookup"><span data-stu-id="3dd05-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="3dd05-182">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="3dd05-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="3dd05-183">В разделе **Сертификаты** выберите **Добавить**, чтобы добавить сертификат в цепочку.</span><span class="sxs-lookup"><span data-stu-id="3dd05-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="3dd05-184">Используйте кнопки **Вверх** или **Вниз**, чтобы изменить положение сертификата в цепочке.</span><span class="sxs-lookup"><span data-stu-id="3dd05-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="3dd05-185">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3dd05-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="3dd05-186">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3dd05-186">Close the page.</span></span>
9. <span data-ttu-id="3dd05-187">На странице **Среда службы** в области действий выберите **Опубликовать** для публикации среды в облаке.</span><span class="sxs-lookup"><span data-stu-id="3dd05-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="3dd05-188">Значение в поле **Статус** изменяется на **Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="3dd05-189">Создание подключенного приложения</span><span class="sxs-lookup"><span data-stu-id="3dd05-189">Create a connected application</span></span>

1. <span data-ttu-id="3dd05-190">На странице **Настройки среды** на панели действий выберите **Подключенные приложения**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="3dd05-191">Выберите **Создать** для создания подключенного приложения.</span><span class="sxs-lookup"><span data-stu-id="3dd05-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="3dd05-192">В поле **Имя** введите имя подключаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="3dd05-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="3dd05-193">В поле **Приложение** введите URL-адрес среды Finance и Supply Chain Management для подключения.</span><span class="sxs-lookup"><span data-stu-id="3dd05-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="3dd05-194">В поле **Клиент** укажите клиент среды Finance и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3dd05-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="3dd05-195">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-195">Select **Save**.</span></span>
6. <span data-ttu-id="3dd05-196">В области действий выберите **Проверить подключение** для проверки подключения к среде.</span><span class="sxs-lookup"><span data-stu-id="3dd05-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="3dd05-197">Затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3dd05-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="3dd05-198">Связывание подключенных приложений со средами</span><span class="sxs-lookup"><span data-stu-id="3dd05-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="3dd05-199">На странице **Настройки среды** выберите **Создать**, чтобы назначить подключенное приложение среде.</span><span class="sxs-lookup"><span data-stu-id="3dd05-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="3dd05-200">В поле **Подключенное приложение** выберите подключенное приложение.</span><span class="sxs-lookup"><span data-stu-id="3dd05-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="3dd05-201">В поле **Среда службы** выберите среду службы.</span><span class="sxs-lookup"><span data-stu-id="3dd05-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="3dd05-202">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3dd05-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="3dd05-203">Настройка интеграции надстройки электронного выставления накладных в Finance и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3dd05-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="3dd05-204">Включение функции интеграции дополнения электронных накладных</span><span class="sxs-lookup"><span data-stu-id="3dd05-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="3dd05-205">Войдите в свой экземпляр Finance или Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3dd05-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="3dd05-206">В рабочей области **Управление функциями** выполните поиск функции **Интеграция надстройки электронного выставления накладных**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="3dd05-207">Если эта функция не отображается на странице, выберите **Проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="3dd05-208">Выберите эту функцию, затем выберите **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="3dd05-209">Настройка URL-адреса конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="3dd05-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="3dd05-210">Перейдите в раздел **Администрирование организации \> Настройка \> Параметры электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="3dd05-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="3dd05-211">На вкладке **Служба отправки** в поле **URL конечной точки службы** введите соответствующую конечную точку службы для своего географического расположения Azure, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3dd05-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="3dd05-212">География центра обработки данных Azure</span><span class="sxs-lookup"><span data-stu-id="3dd05-212">Datacenter Azure geography</span></span> | <span data-ttu-id="3dd05-213">URL-адрес конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="3dd05-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="3dd05-214">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="3dd05-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3dd05-215">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="3dd05-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3dd05-216">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="3dd05-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3dd05-217">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="3dd05-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="3dd05-218">В поле **Среда** введите имя среды надстройки электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3dd05-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="3dd05-219">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3dd05-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
