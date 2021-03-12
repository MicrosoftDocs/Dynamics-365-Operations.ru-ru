---
title: Обзор электронных подписей
description: В этой статье представлен обзор электронных подписей и описан порядок их возможного использования.
author: maertenm
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 051bb023d3456dae0be30de3897b282c2d50c5af
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797636"
---
# <a name="electronic-signatures-overview"></a><span data-ttu-id="19643-103">Обзор электронных подписей</span><span class="sxs-lookup"><span data-stu-id="19643-103">Electronic signatures overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19643-104">В этой статье представлен обзор электронных подписей и описан порядок их возможного использования.</span><span class="sxs-lookup"><span data-stu-id="19643-104">This article provides an overview of electronic signatures and describes how they can be used.</span></span>

## <a name="what-is-an-electronic-signature"></a><span data-ttu-id="19643-105">Что такое электронная подпись?</span><span class="sxs-lookup"><span data-stu-id="19643-105">What is an electronic signature?</span></span>

<span data-ttu-id="19643-106">Электронная подпись подтверждает личность человека, который намеревается запустить или утвердить процесс обработки данных.</span><span class="sxs-lookup"><span data-stu-id="19643-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="19643-107">В некоторых отраслях промышленности электронная подпись имеет одинаковую юридическую силу с рукописной подписью.</span><span class="sxs-lookup"><span data-stu-id="19643-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span>

<span data-ttu-id="19643-108">Электронные подписи являются обязательным требованием в некоторых строго регламентируемых отраслях, таких как фармацевтика, продукты и напитки, аэрокосмическая и оборонная.</span><span class="sxs-lookup"><span data-stu-id="19643-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="19643-109">Они также необходимы для соответствия требованиям 21 CFR, часть 11, Управление по контролю за продуктами и лекарствами США (FDA).</span><span class="sxs-lookup"><span data-stu-id="19643-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span>

> [!NOTE]
> <span data-ttu-id="19643-110">Электронная подпись по своей сути не идентична цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="19643-110">An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="19643-111">Электронная подпись является обычной заменой рукописной подписи, в то время как цифровая подпись обеспечивает дополнительные меры безопасности.</span><span class="sxs-lookup"><span data-stu-id="19643-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="19643-112">Цифровая подпись может оказать помощь при идентификации признаков несанкционированных действий в отношении данных со стороны другого пользователя или процесса.</span><span class="sxs-lookup"><span data-stu-id="19643-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="19643-113">Цифровую подпись также можно проверить, и эта проверка не может быть отвергнута владельцем сертификата, использованного для подписания данных.</span><span class="sxs-lookup"><span data-stu-id="19643-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="19643-114">Как описано ниже, электронные подписи имеют встроенную функциональность цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="19643-114">As described below, electronic signatures have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures"></a><span data-ttu-id="19643-115">Электронные подписи</span><span class="sxs-lookup"><span data-stu-id="19643-115">Electronic signatures</span></span>

<span data-ttu-id="19643-116">Можно использовать электронные подписи для критически важных бизнес-процессов.</span><span class="sxs-lookup"><span data-stu-id="19643-116">You can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="19643-117">Для некоторых процессов предусмотрены встроенные возможности использования электронных подписей.</span><span class="sxs-lookup"><span data-stu-id="19643-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="19643-118">Можно также создать пользовательские требования к электронным подписям для любой таблицы и поля базы данных.</span><span class="sxs-lookup"><span data-stu-id="19643-118">You can also create custom signature requirements for any database table and field.</span></span>

<span data-ttu-id="19643-119">Для электронных подписей предусмотрены соответствующие функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="19643-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="19643-120">Каждый пользователь, подписывающий документы, должен получить действительный сертификат шифрования.</span><span class="sxs-lookup"><span data-stu-id="19643-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="19643-121">При подписании документа проверяется закрытый ключ, который связан с этим сертификатом.</span><span class="sxs-lookup"><span data-stu-id="19643-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="19643-122">Сведения об электронной подписи записываются в журнал, чтобы создать аудиторский след.</span><span class="sxs-lookup"><span data-stu-id="19643-122">Electronic signature information is recorded in a log to provide an audit trail.</span></span> <span data-ttu-id="19643-123">Для настройки электронных подписей см. раздел [Настройка электронных подписей](tasks/set-up-electronic-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="19643-123">To set up electronic signatures, see [Set up electronic signatures](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="19643-124">Пользователи, которым требуется доступ к электронным подписям</span><span class="sxs-lookup"><span data-stu-id="19643-124">Users who require access to electronic signatures</span></span>

<span data-ttu-id="19643-125">Обычно права доступа к электронным подписям через систему безопасности требуются трем группам пользователей: администраторы электронных подписей, подписывающие лица и аудиторы электронных подписей.</span><span class="sxs-lookup"><span data-stu-id="19643-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="19643-126">Администратор электронной подписи</span><span class="sxs-lookup"><span data-stu-id="19643-126">Electronic signature administrator</span></span>

<span data-ttu-id="19643-127">Администратор электронной подписи настраивает требования к подписи, общие параметры и утверждающих лиц и получает оповещения в случае ошибки при проверке подписи.</span><span class="sxs-lookup"><span data-stu-id="19643-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="19643-128">По умолчанию разрешение на администрирование электронных подписей имеет пользователь с ролью безопасности **Менеджер по информационным технологиям**.</span><span class="sxs-lookup"><span data-stu-id="19643-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="19643-129">Подписавшее лицо</span><span class="sxs-lookup"><span data-stu-id="19643-129">Signer</span></span>

<span data-ttu-id="19643-130">Подписывающее лицо ставит электронные подписи для документов и процессов, которым требуются электронные подписи.</span><span class="sxs-lookup"><span data-stu-id="19643-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="19643-131">По умолчанию разрешение на подписывание документов с помощью электронных подписей имеет пользователь с ролью безопасности **Пользователь системы**.</span><span class="sxs-lookup"><span data-stu-id="19643-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span>

> [!NOTE]
> <span data-ttu-id="19643-132">Подписывающему лицу могут потребоваться дополнительные разрешения на доступ к данным, связанным с подписываемым документом или процессом.</span><span class="sxs-lookup"><span data-stu-id="19643-132">The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="19643-133">Пользователи, которые вносят изменения в данные и затем подписывают эти изменения, должны иметь разрешения на изменение данных.</span><span class="sxs-lookup"><span data-stu-id="19643-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="19643-134">Пользователю, выполняющему подписание от имени другого пользователя, доступ к данным может не потребоваться.</span><span class="sxs-lookup"><span data-stu-id="19643-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="19643-135">Примером пользователя такого типа является супервизор, подписывающий внесенные сотрудником изменения.</span><span class="sxs-lookup"><span data-stu-id="19643-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="19643-136">Аудитор электронной подписи</span><span class="sxs-lookup"><span data-stu-id="19643-136">Electronic signature auditor</span></span>

<span data-ttu-id="19643-137">Аудиторы электронной подписи проверяют журнал базы данных и журнал проверки подписи, который доступен из журнала базы данных.</span><span class="sxs-lookup"><span data-stu-id="19643-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="19643-138">По умолчанию разрешение на аудит электронных подписей имеет пользователь с ролью безопасности **Менеджер по информационным технологиям**.</span><span class="sxs-lookup"><span data-stu-id="19643-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span>

<span data-ttu-id="19643-139">При использовании роли, отличной от **Менеджер по информационным технологиям**, необходимо убедиться, что ей назначены следующие привилегии.</span><span class="sxs-lookup"><span data-stu-id="19643-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

- <span data-ttu-id="19643-140">Просмотр ошибок электронной подписи</span><span class="sxs-lookup"><span data-stu-id="19643-140">View electronic signature failures</span></span>
- <span data-ttu-id="19643-141">Просмотр журнала базы данных</span><span class="sxs-lookup"><span data-stu-id="19643-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="19643-142">Подписание документов электронным способом</span><span class="sxs-lookup"><span data-stu-id="19643-142">Signing documents electronically</span></span>

### <a name="get-a-certificate"></a><span data-ttu-id="19643-143">Получение сертификата</span><span class="sxs-lookup"><span data-stu-id="19643-143">Get a certificate</span></span>

<span data-ttu-id="19643-144">Перед подписанием документов электронным способом необходимо запросить сертификат.</span><span class="sxs-lookup"><span data-stu-id="19643-144">Before you sign documents electronically, you must request a certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="19643-145">Для создания сертификатов и активации электронной подписи используются возможности Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="19643-145">Microsoft SQL Server features are used to create certificates and enable electronic signing.</span></span> <span data-ttu-id="19643-146">Никакая дополнительная инфраструктура сертификатов или открытые ключи не требуются.</span><span class="sxs-lookup"><span data-stu-id="19643-146">No additional certificate or public key infrastructure (PKI) is required.</span></span>

<span data-ttu-id="19643-147">При запросе сертификата создается открытый ключ и закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="19643-147">When you request a certificate, a public key and a private key are created for you.</span></span> <span data-ttu-id="19643-148">Закрытый ключ зашифрован с использованием пароля, который известен только пользователю.</span><span class="sxs-lookup"><span data-stu-id="19643-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="19643-149">Во время подписания документа электронным способом идентификация личности производится после ввода пароля.</span><span class="sxs-lookup"><span data-stu-id="19643-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span>

<span data-ttu-id="19643-150">Для запроса сертификата на странице **Параметры** на вкладке **Учетные записи** щелкните **Получить сертификат**.</span><span class="sxs-lookup"><span data-stu-id="19643-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span>

<span data-ttu-id="19643-151">Введите и подтвердите пароль, который используется для подписания.</span><span class="sxs-lookup"><span data-stu-id="19643-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="19643-152">Пароль необходим для защиты закрытого ключа и авторизации использования данного сертификата.</span><span class="sxs-lookup"><span data-stu-id="19643-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="19643-153">Этот пароль не хранится в базе данных и недоступен никому, в том числе администратору.</span><span class="sxs-lookup"><span data-stu-id="19643-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the administrator.</span></span>

<span data-ttu-id="19643-154">Если забыт пароль, связанный с данным сертификатом, то сертификат необходимо сбросить.</span><span class="sxs-lookup"><span data-stu-id="19643-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="19643-155">Сброс сертификата не влияет на документы, которые были ранее подписаны с помощью предыдущего сертификата.</span><span class="sxs-lookup"><span data-stu-id="19643-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="19643-156">Чтобы сбросить сертификат, на странице **Параметры** щелкните **Сбросить сертификат**.</span><span class="sxs-lookup"><span data-stu-id="19643-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="19643-157">Подписание документа электронным способом</span><span class="sxs-lookup"><span data-stu-id="19643-157">Sign a document electronically</span></span>

<span data-ttu-id="19643-158">Страница **Подписание документа** отображается при внесении изменения, требующего электронной подписи.</span><span class="sxs-lookup"><span data-stu-id="19643-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1. <span data-ttu-id="19643-159">На странице **Подписание документа** перейдите на вкладку **Документ**, чтобы проверить внесенные в документ изменения.</span><span class="sxs-lookup"><span data-stu-id="19643-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2. <span data-ttu-id="19643-160">На вкладке **Подпись** выберите код причины.</span><span class="sxs-lookup"><span data-stu-id="19643-160">On the **Signature** tab, select a reason code.</span></span>
3. <span data-ttu-id="19643-161">Введите комментарий, если он требуется.</span><span class="sxs-lookup"><span data-stu-id="19643-161">Enter a comment, if a comment is required.</span></span>
4. <span data-ttu-id="19643-162">Если соответствующий идентификатор пользователя не отображается в поле **Подписавший**, выберите его из списка.</span><span class="sxs-lookup"><span data-stu-id="19643-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5. <span data-ttu-id="19643-163">Введите свое местоположение, если эта информация является обязательной.</span><span class="sxs-lookup"><span data-stu-id="19643-163">Enter your location, if this information is required.</span></span>
6. <span data-ttu-id="19643-164">Нажмите кнопку **OК**.</span><span class="sxs-lookup"><span data-stu-id="19643-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="19643-165">Подписание изменений, внесенных другим пользователем</span><span class="sxs-lookup"><span data-stu-id="19643-165">Sign for another user's changes</span></span>

<span data-ttu-id="19643-166">Время от времени может возникнуть необходимость, чтобы один пользователь подписал изменения, внесенные другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="19643-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="19643-167">Например, может потребоваться, чтобы руководитель подписал изменения, внесенные в спецификацию сотрудником.</span><span class="sxs-lookup"><span data-stu-id="19643-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="19643-168">Эта процедура используется для назначения одного пользователя в качестве лица, подписывающего изменения за другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="19643-168">Use this procedure to designate a user as a signer for another user.</span></span>

> [!NOTE]
> <span data-ttu-id="19643-169">Когда один пользователь подписывает изменения, внесенные другим пользователем, необходимо, чтобы на рабочую станцию пользователя, который внес изменения, была предоставлена подпись.</span><span class="sxs-lookup"><span data-stu-id="19643-169">When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="19643-170">Пользователю не удастся сохранить изменение до тех пор, пока не будет предоставлена подпись.</span><span class="sxs-lookup"><span data-stu-id="19643-170">The user can't save the change until the signature has been provided.</span></span>

<span data-ttu-id="19643-171">Чтобы назначить утверждающих, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="19643-171">To designate approvers, follow these steps.</span></span>

1. <span data-ttu-id="19643-172">На странице **Параметры** на вкладке **Учетные записи** щелкните **Назначить утверждающего**.</span><span class="sxs-lookup"><span data-stu-id="19643-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2. <span data-ttu-id="19643-173">В поле **Код утверждающего пользователя** выберите идентификатор пользователя, который должен подписать изменения, внесенные другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="19643-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3. <span data-ttu-id="19643-174">В поле **Код пользователя для подписи** выберите идентификатор пользователя, чьи изменения будут подписаны.</span><span class="sxs-lookup"><span data-stu-id="19643-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>
