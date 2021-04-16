---
title: Создание учетной записи хранилища в Azure и хранилища ключей
description: В этом разделе объясняется, как создать учетную запись хранилища Azure и хранилище ключей.
author: gionoder
ms.date: 02/12/2021
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
ms.openlocfilehash: b7df4933c1373893e00f48ea3a21bd5af40719a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840228"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="f430e-103">Создание учетной записи хранилища в Azure и хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="f430e-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f430e-104">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="f430e-104">Prerequisites</span></span>

<span data-ttu-id="f430e-105">Перед выполнением шагов из данного раздела необходимо убедиться, что были выполнены следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="f430e-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="f430e-106">Создайте ресурс хранилища ключей в Azure.</span><span class="sxs-lookup"><span data-stu-id="f430e-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="f430e-107">Дополнительные сведения см. в разделе [Об Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="f430e-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="f430e-108">Создайте учетную запись хранилища Azure (хранилище BLOB-объектов).</span><span class="sxs-lookup"><span data-stu-id="f430e-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="f430e-109">Дополнительные сведения см. в разделе [Управление учетной записью хранилища Azure](https://docs.microsoft.com/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="f430e-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="f430e-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="f430e-110">Overview</span></span>

<span data-ttu-id="f430e-111">В этом разделе выполняются два основных шага:</span><span class="sxs-lookup"><span data-stu-id="f430e-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="f430e-112">Настройте учетную запись хранилища Azure, чтобы получить URI учетной записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="f430e-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="f430e-113">Настройте хранилище ключей для хранения URI учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f430e-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="f430e-114">Настройка учетной записи хранилища Azure для получения URI учетной записи хранилища</span><span class="sxs-lookup"><span data-stu-id="f430e-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="f430e-115">Открывает учетную запись хранения, которую планируется использовать в модуле электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="f430e-115">Open the storage account that you plan to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="f430e-116">Перейдите в раздел **Служб BLOB-объектов** \> **Контейнеры** и создайте новый контейнер.</span><span class="sxs-lookup"><span data-stu-id="f430e-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="f430e-117">Введите имя контейнера и задайте для поля **Уровень открытого доступа** значение **Частный (нет анонимного доступа)**.</span><span class="sxs-lookup"><span data-stu-id="f430e-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="f430e-118">Откройте контейнер и перейдите в раздел **Параметры \> Политика доступа**.</span><span class="sxs-lookup"><span data-stu-id="f430e-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="f430e-119">Выберите **Добавить политику**, чтобы добавить сохраненную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="f430e-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="f430e-120">Задайте требуемые значения в полях **Идентификатор** и **Разрешения**.</span><span class="sxs-lookup"><span data-stu-id="f430e-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="f430e-121">В поле **Разрешения** следует выбрать все разрешения.</span><span class="sxs-lookup"><span data-stu-id="f430e-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Предоставление разрешения для хранилища BLOB-объектов](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="f430e-123">Введите даты начала и окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="f430e-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="f430e-124">Дата истечения срока действия должна быть в будущем.</span><span class="sxs-lookup"><span data-stu-id="f430e-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="f430e-125">Выберите **ОК**, чтобы сохранить политику, затем сохраните изменения в контейнере.</span><span class="sxs-lookup"><span data-stu-id="f430e-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="f430e-126">Вернитесь к учетной записи хранения и откройте **Обозреватель службы хранилища (предварительная версия)**.</span><span class="sxs-lookup"><span data-stu-id="f430e-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="f430e-127">Щелкните контейнер правой кнопкой мыши и выберите **Получить подписанный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="f430e-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="f430e-128">В диалоговом окне **Подписанный URL-адрес** скопируйте и сохраните значение в поле **URI**.</span><span class="sxs-lookup"><span data-stu-id="f430e-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="f430e-129">Это значение будет использоваться в следующей процедуре и будет называться *URI подписанного URL-адреса*.</span><span class="sxs-lookup"><span data-stu-id="f430e-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![Выбор и копирование значения URI](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="f430e-131">Настройка хранилища ключей для хранения URI учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="f430e-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="f430e-132">Откройте хранилище ключей, которое планируется использовать в модуле электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="f430e-132">Open the key vault that you intend to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="f430e-133">Перейдите в раздел **Параметры** \> **Секреты** и выберите **Создать/импортировать**, чтобы создать новый секрет.</span><span class="sxs-lookup"><span data-stu-id="f430e-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="f430e-134">На странице **Создание секрета** в поле **Параметры отправки** выберите **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="f430e-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="f430e-135">Введите имя секрета.</span><span class="sxs-lookup"><span data-stu-id="f430e-135">Enter the name of the secret.</span></span> <span data-ttu-id="f430e-136">Это имя будет использоваться во время настройки службы в Regulatory Configuration Service (RCS) и будет называться *имя секрета хранилища ключей*.</span><span class="sxs-lookup"><span data-stu-id="f430e-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="f430e-137">В поле **Значение** выберите **URI подписанного URL-адреса**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f430e-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="f430e-138">Настройте политику доступа, чтобы предоставить модулю электронного выставления накладных уровень безопасного доступа для созданного вами секрета.</span><span class="sxs-lookup"><span data-stu-id="f430e-138">Set up the access policy to grant Electronic invoicing the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="f430e-139">Перейдите в раздел **Параметры \> Политика доступа** и выберите команду **Добавить политику доступа**.</span><span class="sxs-lookup"><span data-stu-id="f430e-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="f430e-140">Задайте разрешения секрета для операций **Получить** и **Список**.</span><span class="sxs-lookup"><span data-stu-id="f430e-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Предоставление доступа к службе](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="f430e-142">Задайте разрешения сертификата для операций **Получить** и **Список**.</span><span class="sxs-lookup"><span data-stu-id="f430e-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Предоставление разрешения сертификата](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="f430e-144">В поле **Выбрать доверителя** выберите **нет выбранных**.</span><span class="sxs-lookup"><span data-stu-id="f430e-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="f430e-145">В диалоговом окне **Субъект** выберите субъект, добавив **Служба электронных накладных**.</span><span class="sxs-lookup"><span data-stu-id="f430e-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="f430e-146">Выберите **Добавить**, затем выберите **Сохранить изменения Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="f430e-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="f430e-147">На странице **Обзор** скопируйте значение **Имя DNS** для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f430e-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="f430e-148">Это значение будет использоваться во время настройки службы в RCS и будет называться *URI хранилища ключей*.</span><span class="sxs-lookup"><span data-stu-id="f430e-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

