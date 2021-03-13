---
title: Начало работы с администрированием службы надстройки "Электронное выставление счетов"
description: В этой теме объясняется, как начать работать с надстройкой электронного выставления накладных.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104428"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="bd141-103">Начало работы с администрированием службы надстройки "Электронное выставление счетов"</span><span class="sxs-lookup"><span data-stu-id="bd141-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="bd141-104">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="bd141-104">Prerequisites</span></span>

<span data-ttu-id="bd141-105">Перед выполнением процедур из данной темы необходимо выполнить следующие предварительные требования:</span><span class="sxs-lookup"><span data-stu-id="bd141-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="bd141-106">Необходимо иметь доступ к учетной записи Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="bd141-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="bd141-107">Необходим проект LCS, включающий версию 10.0.13 или более позднюю версию Microsoft Dynamics 365 Finance и Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bd141-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="bd141-108">Кроме того, эти приложения должны быть развернуты в одном из следующих географических регионов Azure:</span><span class="sxs-lookup"><span data-stu-id="bd141-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="bd141-109">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="bd141-109">East US</span></span>
    - <span data-ttu-id="bd141-110">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="bd141-110">West US</span></span>
    - <span data-ttu-id="bd141-111">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="bd141-111">North EU</span></span>
    - <span data-ttu-id="bd141-112">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="bd141-112">West EU</span></span>

- <span data-ttu-id="bd141-113">Необходимо иметь доступ к учетной записи службы Dynamics 365 Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="bd141-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="bd141-114">Необходимо активировать функцию глобализации для вашей учетной записи RCS в управлении функциями.</span><span class="sxs-lookup"><span data-stu-id="bd141-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="bd141-115">Дополнительные сведения см. в разделе [Regulatory Configuration Services (RCS) — функции глобализации](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="bd141-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="bd141-116">Необходимо создать Key Vault и учетную запись хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="bd141-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="bd141-117">Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="bd141-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="bd141-118">Установка надстройки для микрослужб в Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="bd141-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="bd141-119">Войдите в учетную запись LCS.</span><span class="sxs-lookup"><span data-stu-id="bd141-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="bd141-120">Выберите плитку **Управление предварительными версиями функций**.</span><span class="sxs-lookup"><span data-stu-id="bd141-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="bd141-121">В разделе **Общедоступные предварительные версии функций** выберите **Служба электронного выставления накладных**.</span><span class="sxs-lookup"><span data-stu-id="bd141-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="bd141-122">Убедитесь, что для параметра **Предварительная версия функции включена** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="bd141-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="bd141-123">Настройка параметров для интеграции RCS с надстройкой электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="bd141-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="bd141-124">Войдите в учетную запись RCS.</span><span class="sxs-lookup"><span data-stu-id="bd141-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="bd141-125">В рабочей области **Электронная отчетность** в разделе **Связанные ссылки** выберите **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="bd141-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="bd141-126">На вкладке **Служба электронного выставления накладных** в поле **URI конечной точки службы** введите соответствующую конечную точку службы для своего географического расположения Azure, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bd141-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="bd141-127">География центра обработки данных Azure</span><span class="sxs-lookup"><span data-stu-id="bd141-127">Datacenter Azure geography</span></span> | <span data-ttu-id="bd141-128">Универсальный код ресурса (URI) конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="bd141-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="bd141-129">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="bd141-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="bd141-130">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="bd141-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="bd141-131">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="bd141-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="bd141-132">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="bd141-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="bd141-133">Убедитесь, что в поле **Код приложения** установлено значение **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="bd141-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="bd141-134">Это значение является фиксированным значением.</span><span class="sxs-lookup"><span data-stu-id="bd141-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="bd141-135">В поле **Код среды LCS** введите идентификатор вашей учетной записи подписки LCS.</span><span class="sxs-lookup"><span data-stu-id="bd141-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="bd141-136">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd141-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="bd141-137">Создание секрета Key Vault</span><span class="sxs-lookup"><span data-stu-id="bd141-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="bd141-138">Войдите в учетную запись RCS.</span><span class="sxs-lookup"><span data-stu-id="bd141-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="bd141-139">В рабочей области **Функция глобализации** в разделе **Среда** выберите плитку **Электронные накладные**.</span><span class="sxs-lookup"><span data-stu-id="bd141-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="bd141-140">На странице **Настройки среды** на панели действий выберите **Среда службы**, затем выберите **Параметры Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="bd141-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="bd141-141">Выберите **Создать**, чтобы создать секрет Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bd141-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="bd141-142">В поле **Имя** введите имя секрета Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bd141-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="bd141-143">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="bd141-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="bd141-144">В поле **URI Key Vault** вставьте секрет из Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bd141-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="bd141-145">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="bd141-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="bd141-146">Создание секрета учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bd141-146">Create Storage account secret</span></span>

1. <span data-ttu-id="bd141-147">На странице **Параметры Key Vault** в разделе **Сертификаты** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="bd141-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="bd141-148">В поле **Имя** введите имя секрета учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bd141-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="bd141-149">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="bd141-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="bd141-150">В поле **Тип** выберите **Сертификат**.</span><span class="sxs-lookup"><span data-stu-id="bd141-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="bd141-151">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd141-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="bd141-152">Создание среды надстройки электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="bd141-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="bd141-153">Войдите в учетную запись RCS.</span><span class="sxs-lookup"><span data-stu-id="bd141-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="bd141-154">В рабочей области **Функция глобализации** в разделе **Среда** выберите плитку **Электронные накладные**.</span><span class="sxs-lookup"><span data-stu-id="bd141-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="bd141-155">Создание среды службы</span><span class="sxs-lookup"><span data-stu-id="bd141-155">Create a service environment</span></span>

1. <span data-ttu-id="bd141-156">На странице **Настройки среды** на панели действий выберите **Среда службы**.</span><span class="sxs-lookup"><span data-stu-id="bd141-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="bd141-157">Выберите **Создать** для создания новой среды службы.</span><span class="sxs-lookup"><span data-stu-id="bd141-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="bd141-158">В поле **Имя** введите имя среды электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="bd141-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="bd141-159">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="bd141-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="bd141-160">В поле **Секрет маркера SAS хранилища** выберите имя сертификата, который должен использоваться для проверки подлинности доступа к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bd141-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="bd141-161">В разделе **Пользователи** выберите **Добавить**, чтобы добавить пользователя, которому разрешено отправлять электронные накладные через среду, а также подключиться к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bd141-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="bd141-162">В поле **Код пользователя** введите псевдоним пользователя.</span><span class="sxs-lookup"><span data-stu-id="bd141-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="bd141-163">В поле **Электронная почта** введите адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="bd141-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="bd141-164">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="bd141-164">Select **Save**.</span></span>
8. <span data-ttu-id="bd141-165">Если в накладных для конкретной страны/региона требуется цепочка сертификатов для применения цифровых подписей, на панели действий выберите **Параметры Key Vault**, затем выберите **Цепочка сертификатов** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bd141-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="bd141-166">Для создания цепочки сертификатов выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="bd141-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="bd141-167">В поле **Имя** введите имя цепочки сертификатов.</span><span class="sxs-lookup"><span data-stu-id="bd141-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="bd141-168">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="bd141-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="bd141-169">В разделе **Сертификаты** выберите **Добавить**, чтобы добавить сертификат в цепочку.</span><span class="sxs-lookup"><span data-stu-id="bd141-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="bd141-170">Используйте кнопки **Вверх** или **Вниз**, чтобы изменить положение сертификата в цепочке.</span><span class="sxs-lookup"><span data-stu-id="bd141-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="bd141-171">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd141-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="bd141-172">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd141-172">Close the page.</span></span>
9. <span data-ttu-id="bd141-173">На странице **Среда службы** в области действий выберите **Опубликовать** для публикации среды в облаке.</span><span class="sxs-lookup"><span data-stu-id="bd141-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="bd141-174">Значение в поле **Статус** изменяется на **Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="bd141-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="bd141-175">Создание подключенного приложения</span><span class="sxs-lookup"><span data-stu-id="bd141-175">Create a connected application</span></span>

1. <span data-ttu-id="bd141-176">На странице **Настройки среды** на панели действий выберите **Подключенные приложения**.</span><span class="sxs-lookup"><span data-stu-id="bd141-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="bd141-177">Выберите **Создать** для создания подключенного приложения.</span><span class="sxs-lookup"><span data-stu-id="bd141-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="bd141-178">В поле **Имя** введите имя подключаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="bd141-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="bd141-179">В поле **Приложение** введите URL-адрес среды Finance и Supply Chain Management для подключения.</span><span class="sxs-lookup"><span data-stu-id="bd141-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="bd141-180">В поле **Клиент** укажите клиент среды Finance и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bd141-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="bd141-181">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="bd141-181">Select **Save**.</span></span>
6. <span data-ttu-id="bd141-182">В области действий выберите **Проверить подключение** для проверки подключения к среде.</span><span class="sxs-lookup"><span data-stu-id="bd141-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="bd141-183">Затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd141-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="bd141-184">Связывание подключенных приложений со средами</span><span class="sxs-lookup"><span data-stu-id="bd141-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="bd141-185">На странице **Настройки среды** выберите **Создать**, чтобы назначить подключенное приложение среде.</span><span class="sxs-lookup"><span data-stu-id="bd141-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="bd141-186">В поле **Подключенное приложение** выберите подключенное приложение.</span><span class="sxs-lookup"><span data-stu-id="bd141-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="bd141-187">В поле **Среда службы** выберите среду службы.</span><span class="sxs-lookup"><span data-stu-id="bd141-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="bd141-188">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd141-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="bd141-189">Настройка интеграции надстройки электронного выставления накладных в Finance и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="bd141-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="bd141-190">Включение функции интеграции дополнения электронных накладных</span><span class="sxs-lookup"><span data-stu-id="bd141-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="bd141-191">Войдите в свой экземпляр Finance или Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bd141-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="bd141-192">В рабочей области **Управление функциями** выполните поиск функции **Интеграция надстройки электронного выставления накладных**.</span><span class="sxs-lookup"><span data-stu-id="bd141-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="bd141-193">Если эта функция не отображается на странице, выберите **Проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="bd141-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="bd141-194">Выберите эту функцию, затем выберите **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="bd141-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="bd141-195">Настройка URL-адреса конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="bd141-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="bd141-196">Перейдите в раздел **Администрирование организации \> Настройка \> Параметры электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="bd141-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="bd141-197">На вкладке **Служба отправки** в поле **URL конечной точки службы** введите соответствующую конечную точку службы для своего географического расположения Azure, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bd141-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="bd141-198">География центра обработки данных Azure</span><span class="sxs-lookup"><span data-stu-id="bd141-198">Datacenter Azure geography</span></span> | <span data-ttu-id="bd141-199">URL-адрес конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="bd141-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="bd141-200">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="bd141-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="bd141-201">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="bd141-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="bd141-202">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="bd141-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="bd141-203">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="bd141-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="bd141-204">В поле **Среда** введите имя среды надстройки электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="bd141-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="bd141-205">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd141-205">Select **Save**, and then close the page.</span></span>
