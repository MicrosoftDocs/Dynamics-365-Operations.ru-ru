---
title: Начало работы с администрированием службы электронного выставления накладных
description: В этой теме объясняется, как начать работать с модулем электронного выставления накладных.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840156"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="3c616-103">Начало работы с администрированием службы электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="3c616-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="3c616-104">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="3c616-104">Prerequisites</span></span>

<span data-ttu-id="3c616-105">Перед выполнением процедур из данной темы необходимо выполнить следующие предварительные требования:</span><span class="sxs-lookup"><span data-stu-id="3c616-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="3c616-106">Необходимо иметь доступ к учетной записи Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3c616-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="3c616-107">Необходим проект LCS, включающий версию 10.0.17 или более позднюю версию Microsoft Dynamics 365 Finance и Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3c616-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3c616-108">Кроме того, эти приложения должны быть развернуты в одном из следующих географических регионов Azure:</span><span class="sxs-lookup"><span data-stu-id="3c616-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="3c616-109">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="3c616-109">East US</span></span>
    - <span data-ttu-id="3c616-110">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="3c616-110">West US</span></span>
    - <span data-ttu-id="3c616-111">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="3c616-111">North EU</span></span>
    - <span data-ttu-id="3c616-112">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="3c616-112">West EU</span></span>

- <span data-ttu-id="3c616-113">Необходимо иметь доступ к учетной записи службы Dynamics 365 Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="3c616-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="3c616-114">Необходимо активировать функцию глобализации для вашей учетной записи RCS в управлении функциями.</span><span class="sxs-lookup"><span data-stu-id="3c616-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="3c616-115">Дополнительные сведения см. в разделе [Regulatory Configuration Services (RCS) — функции глобализации](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="3c616-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="3c616-116">Необходимо создать Key Vault и учетную запись хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="3c616-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="3c616-117">Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="3c616-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="3c616-118">Установка надстройки для микрослужб в Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="3c616-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="3c616-119">Войдите в учетную запись LCS.</span><span class="sxs-lookup"><span data-stu-id="3c616-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="3c616-120">Выберите плитку **Управление предварительными версиями функций**.</span><span class="sxs-lookup"><span data-stu-id="3c616-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="3c616-121">В разделе **Общедоступные предварительные версии функций** выберите **Служба электронного выставления накладных**.</span><span class="sxs-lookup"><span data-stu-id="3c616-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="3c616-122">Убедитесь, что для параметра **Предварительная версия функции включена** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="3c616-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="3c616-123">На панели мониторинга LCS выберите проект развертывания LCS.</span><span class="sxs-lookup"><span data-stu-id="3c616-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="3c616-124">Должен быть выполнен проект LCS.</span><span class="sxs-lookup"><span data-stu-id="3c616-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="3c616-125">На вкладке **Надстройки сред** выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="3c616-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="3c616-126">Выберите **Службы электронного выставления накладных**.</span><span class="sxs-lookup"><span data-stu-id="3c616-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="3c616-127">В поле **Код приложения AAD** введите **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="3c616-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="3c616-128">Это фиксированное значение.</span><span class="sxs-lookup"><span data-stu-id="3c616-128">This is a fixed value.</span></span>
10. <span data-ttu-id="3c616-129">В поле **Код клиента AAD** введите код клиента вашей учетной записи подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="3c616-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="3c616-130">Ознакомьтесь с условиями и установите флажок.</span><span class="sxs-lookup"><span data-stu-id="3c616-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="3c616-131">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="3c616-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="3c616-132">Настройка параметров для интеграции RCS с модулем электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="3c616-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="3c616-133">Войдите в учетную запись RCS.</span><span class="sxs-lookup"><span data-stu-id="3c616-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="3c616-134">В рабочей области **Электронная отчетность** в разделе **Связанные ссылки** выберите **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="3c616-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="3c616-135">На вкладке **Служба электронного выставления накладных** в поле **URI конечной точки службы** введите соответствующую конечную точку службы для своего географического расположения Azure, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3c616-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="3c616-136">География центра обработки данных Azure</span><span class="sxs-lookup"><span data-stu-id="3c616-136">Datacenter Azure geography</span></span> | <span data-ttu-id="3c616-137">Универсальный код ресурса (URI) конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="3c616-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="3c616-138">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="3c616-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3c616-139">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="3c616-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3c616-140">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="3c616-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3c616-141">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="3c616-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="3c616-142">Убедитесь, что в поле **Код приложения** установлено значение **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="3c616-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="3c616-143">Это значение является фиксированным значением.</span><span class="sxs-lookup"><span data-stu-id="3c616-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="3c616-144">В поле **Код среды LCS** введите идентификатор вашей среды LCS.</span><span class="sxs-lookup"><span data-stu-id="3c616-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="3c616-145">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3c616-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="3c616-146">Создание ссылок Key Vault</span><span class="sxs-lookup"><span data-stu-id="3c616-146">Create Key Vault references</span></span>

1. <span data-ttu-id="3c616-147">Войдите в учетную запись RCS.</span><span class="sxs-lookup"><span data-stu-id="3c616-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="3c616-148">В рабочей области **Функция глобализации** в разделе **Среда** выберите плитку **Электронное выставление накладных**.</span><span class="sxs-lookup"><span data-stu-id="3c616-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="3c616-149">На странице **Настройки среды** на панели действий выберите **Среда службы**, затем выберите **Параметры Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="3c616-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="3c616-150">Выберите **Создать**, чтобы создать ссылку Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3c616-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="3c616-151">В поле **Имя** введите имя ссылки Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3c616-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="3c616-152">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="3c616-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="3c616-153">В поле **URI Key Vault** вставьте секрет хранилища ключей из Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3c616-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="3c616-154">Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="3c616-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="3c616-155">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3c616-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="3c616-156">Создание секрета учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="3c616-156">Create Storage account secret</span></span>

1. <span data-ttu-id="3c616-157">На странице **Настройки среды** на панели действий выберите **Среда службы** > **Параметры Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="3c616-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="3c616-158">Выберите пункт **Ссылка Key Vault** и в разделе **Сертификаты** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="3c616-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="3c616-159">В поле **Имя** введите имя секрета учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3c616-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="3c616-160">Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="3c616-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="3c616-161">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="3c616-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="3c616-162">В поле **Тип** выберите **Секрет**.</span><span class="sxs-lookup"><span data-stu-id="3c616-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="3c616-163">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3c616-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="3c616-164">Создайте секрет для цифрового сертификата</span><span class="sxs-lookup"><span data-stu-id="3c616-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="3c616-165">На странице **Настройки среды** на панели действий выберите **Среда службы**, затем выберите **Параметры Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="3c616-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="3c616-166">Выберите пункт **Ссылка Key Vault**, затем в разделе **Сертификаты** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="3c616-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="3c616-167">В поле **Имя** введите имя секрета цифрового сертификата.</span><span class="sxs-lookup"><span data-stu-id="3c616-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="3c616-168">Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="3c616-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="3c616-169">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="3c616-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="3c616-170">В поле **Тип** выберите **Сертификат**.</span><span class="sxs-lookup"><span data-stu-id="3c616-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="3c616-171">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3c616-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="3c616-172">Создание среды службы</span><span class="sxs-lookup"><span data-stu-id="3c616-172">Create a service environment</span></span>

1. <span data-ttu-id="3c616-173">Войдите в учетную запись RCS.</span><span class="sxs-lookup"><span data-stu-id="3c616-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="3c616-174">В рабочей области **Функция глобализации** в разделе **Среда** выберите плитку **Электронное выставление накладных**.</span><span class="sxs-lookup"><span data-stu-id="3c616-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="3c616-175">На странице **Настройки среды** на панели действий выберите **Среда службы**.</span><span class="sxs-lookup"><span data-stu-id="3c616-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="3c616-176">Выберите **Создать** для создания новой среды службы.</span><span class="sxs-lookup"><span data-stu-id="3c616-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="3c616-177">В поле **Имя** введите имя среды электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3c616-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="3c616-178">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="3c616-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="3c616-179">В поле **Секрет маркера SAS хранилища** выберите имя секрета учетной записи хранения, который должен использоваться для проверки подлинности доступа к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3c616-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="3c616-180">В разделе **Пользователи** выберите **Добавить**, чтобы добавить пользователя, которому разрешено отправлять электронные накладные через среду, а также подключиться к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3c616-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="3c616-181">В поле **Код пользователя** введите псевдоним пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c616-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="3c616-182">В поле **Электронная почта** введите адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c616-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="3c616-183">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3c616-183">Select **Save**.</span></span>
10. <span data-ttu-id="3c616-184">Если в накладных для конкретной страны/региона требуется цепочка сертификатов для применения цифровых подписей, на панели действий выберите **Параметры Key Vault**, затем выберите **Цепочка сертификатов** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3c616-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="3c616-185">Для создания цепочки сертификатов выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3c616-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="3c616-186">В поле **Имя** введите имя цепочки сертификатов.</span><span class="sxs-lookup"><span data-stu-id="3c616-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="3c616-187">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="3c616-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="3c616-188">В разделе **Сертификаты** выберите **Добавить**, чтобы добавить сертификат в цепочку.</span><span class="sxs-lookup"><span data-stu-id="3c616-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="3c616-189">Используйте кнопки **Вверх** или **Вниз**, чтобы изменить положение сертификата в цепочке.</span><span class="sxs-lookup"><span data-stu-id="3c616-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="3c616-190">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3c616-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="3c616-191">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3c616-191">Close the page.</span></span>
11. <span data-ttu-id="3c616-192">На странице **Среда службы** в области действий выберите **Опубликовать** для публикации среды в облаке.</span><span class="sxs-lookup"><span data-stu-id="3c616-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="3c616-193">Значение в поле **Статус** изменяется на **Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="3c616-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="3c616-194">Создание подключенного приложения</span><span class="sxs-lookup"><span data-stu-id="3c616-194">Create a connected application</span></span>

1. <span data-ttu-id="3c616-195">На странице **Настройки среды** на панели действий выберите **Подключенные приложения**.</span><span class="sxs-lookup"><span data-stu-id="3c616-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="3c616-196">Выберите **Создать** для создания подключенного приложения.</span><span class="sxs-lookup"><span data-stu-id="3c616-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="3c616-197">В поле **Имя** введите имя подключаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="3c616-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="3c616-198">В поле **Приложение** введите URL-адрес среды Finance и Supply Chain Management для подключения.</span><span class="sxs-lookup"><span data-stu-id="3c616-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="3c616-199">В поле **Клиент** укажите клиент среды Finance и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3c616-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="3c616-200">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3c616-200">Select **Save**.</span></span>
6. <span data-ttu-id="3c616-201">В области действий выберите **Проверить подключение** для проверки подключения к среде.</span><span class="sxs-lookup"><span data-stu-id="3c616-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="3c616-202">Затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3c616-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="3c616-203">Связывание подключенных приложений со средами</span><span class="sxs-lookup"><span data-stu-id="3c616-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="3c616-204">На странице **Настройки среды** выберите **Создать**, чтобы назначить подключенное приложение среде.</span><span class="sxs-lookup"><span data-stu-id="3c616-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="3c616-205">В поле **Подключенное приложение** выберите подключенное приложение.</span><span class="sxs-lookup"><span data-stu-id="3c616-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="3c616-206">В поле **Среда службы** выберите среду службы.</span><span class="sxs-lookup"><span data-stu-id="3c616-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="3c616-207">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3c616-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="3c616-208">Настройка интеграции электронного выставления накладных в Finance и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3c616-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="3c616-209">Включение функции интеграции электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="3c616-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="3c616-210">Войдите в свой экземпляр Finance или Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3c616-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="3c616-211">В рабочей области **Управление функциями** выполните поиск функции **Интеграция электронного выставления накладных**.</span><span class="sxs-lookup"><span data-stu-id="3c616-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="3c616-212">Если эта функция не отображается на странице, выберите **Проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="3c616-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="3c616-213">Выберите эту функцию, затем выберите **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="3c616-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="3c616-214">Настройка URL-адреса конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="3c616-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="3c616-215">Перейдите в раздел **Администрирование организации \> Настройка \> Параметры электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="3c616-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="3c616-216">На вкладке **Служба отправки** в поле **URL конечной точки службы** введите соответствующую конечную точку службы для своего географического расположения Azure, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3c616-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="3c616-217">География центра обработки данных Azure</span><span class="sxs-lookup"><span data-stu-id="3c616-217">Datacenter Azure geography</span></span> | <span data-ttu-id="3c616-218">URL-адрес конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="3c616-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="3c616-219">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="3c616-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3c616-220">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="3c616-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3c616-221">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="3c616-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="3c616-222">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="3c616-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="3c616-223">В поле **Среда** введите имя среды службы, опубликованной в модуле электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3c616-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="3c616-224">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3c616-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="3c616-225">Включение ключей фокус-тестирования</span><span class="sxs-lookup"><span data-stu-id="3c616-225">Enable Flighting keys</span></span>

<span data-ttu-id="3c616-226">Включите ключи фокус-тестирования для Microsoft Dynamics 365 Finance или Microsoft Dynamics 365 Supply Chain Management версии 10.0.17 или более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="3c616-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="3c616-227">Выполните следующую команду SQL:</span><span class="sxs-lookup"><span data-stu-id="3c616-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="3c616-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="3c616-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="3c616-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="3c616-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="3c616-230">Выполните команду IISreset для всех серверов AOS.</span><span class="sxs-lookup"><span data-stu-id="3c616-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
