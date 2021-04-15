---
title: Настройка электронных подписей
description: Эта процедура используется для настройки электронных подписей.
author: maertenm
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d78ecd0606f3b1d5d7b5f3cd470beecfcdd5077
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747353"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="821de-103">Настройка электронных подписей</span><span class="sxs-lookup"><span data-stu-id="821de-103">Set up electronic signatures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="821de-104">Эта процедура используется для настройки электронных подписей.</span><span class="sxs-lookup"><span data-stu-id="821de-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="821de-105">Электронная подпись подтверждает личность человека, который намеревается запустить или утвердить процесс обработки данных.</span><span class="sxs-lookup"><span data-stu-id="821de-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="821de-106">В качестве компании с демонстрационными данными для создания этой процедуры используется DAT.</span><span class="sxs-lookup"><span data-stu-id="821de-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="821de-107">Включение конфигурационного ключа "Электронная подпись"</span><span class="sxs-lookup"><span data-stu-id="821de-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="821de-108">Перейдите в раздел "Администрирование системы" > "Настройка" > "Конфигурация лицензии".</span><span class="sxs-lookup"><span data-stu-id="821de-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="821de-109">В дереве разверните узел "Администрирование".</span><span class="sxs-lookup"><span data-stu-id="821de-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="821de-110">Убедитесь, что флажок "Электронная подпись" установлен.</span><span class="sxs-lookup"><span data-stu-id="821de-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="821de-111">Если флажок "Электронная подпись" не установлен, необходимо включить режим обслуживания.</span><span class="sxs-lookup"><span data-stu-id="821de-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="821de-112">Режим обслуживания в этой среде может быть включен путем запуска задания обслуживания из Lifecycle Services или путем локального использования средства Deployment.Setup.</span><span class="sxs-lookup"><span data-stu-id="821de-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="821de-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="821de-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="821de-114">Настройка параметров электронной подписи</span><span class="sxs-lookup"><span data-stu-id="821de-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="821de-115">Перейдите в раздел "Управление организацией" > "Настройка" > "Электронная подпись" > "Параметры электронной подписи".</span><span class="sxs-lookup"><span data-stu-id="821de-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="821de-116">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="821de-116">Click Edit.</span></span>
3. <span data-ttu-id="821de-117">В поле "Объявление" введите значение.</span><span class="sxs-lookup"><span data-stu-id="821de-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="821de-118">Введите текст уведомления, которое подписывающие лица получат при запросе подписи.</span><span class="sxs-lookup"><span data-stu-id="821de-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="821de-119">Можно ввести любой текст.</span><span class="sxs-lookup"><span data-stu-id="821de-119">You can enter any text.</span></span> <span data-ttu-id="821de-120">Обычно в этом тексте для пользователя раскрывается значение электронной подписи документа.</span><span class="sxs-lookup"><span data-stu-id="821de-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="821de-121">Если вы хотите ввести текст уведомления на дополнительных языках, нажмите кнопку "Переводы".</span><span class="sxs-lookup"><span data-stu-id="821de-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="821de-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="821de-122">Click Save.</span></span>
5. <span data-ttu-id="821de-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="821de-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="821de-124">Настройка кодов причин для электронных подписей</span><span class="sxs-lookup"><span data-stu-id="821de-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="821de-125">Перейдите в раздел "Управление организацией" > "Настройка" > "Электронная подпись" > "Коды оснований электронной подписи".</span><span class="sxs-lookup"><span data-stu-id="821de-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="821de-126">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="821de-126">Click New.</span></span>
    * <span data-ttu-id="821de-127">Перед использованием электронных подписей необходимо настроить коды причин.</span><span class="sxs-lookup"><span data-stu-id="821de-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="821de-128">Действительный код причины необходимо указать при подписании документа.</span><span class="sxs-lookup"><span data-stu-id="821de-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="821de-129">Подписавшее лицо выбирает код причины, чтобы указать цель электронной подписи.</span><span class="sxs-lookup"><span data-stu-id="821de-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="821de-130">Например, коды причин могут использоваться, чтобы указать на утверждение юристом.</span><span class="sxs-lookup"><span data-stu-id="821de-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="821de-131">В поле "Код основания" введите значение.</span><span class="sxs-lookup"><span data-stu-id="821de-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="821de-132">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="821de-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="821de-133">При необходимости введите дополнительные коды оснований.</span><span class="sxs-lookup"><span data-stu-id="821de-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="821de-134">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="821de-134">Click Save.</span></span>
6. <span data-ttu-id="821de-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="821de-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="821de-136">Требование к электронным подписям для существующих процессов</span><span class="sxs-lookup"><span data-stu-id="821de-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="821de-137">Перейдите в раздел "Управление организацией" > "Настройка" > "Электронная подпись" > "Требования к электронной подписи".</span><span class="sxs-lookup"><span data-stu-id="821de-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="821de-138">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="821de-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="821de-139">Выберите процесс, для которого требуются электронные подписи.</span><span class="sxs-lookup"><span data-stu-id="821de-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="821de-140">Установите или снимите флажок "Необходима подпись".</span><span class="sxs-lookup"><span data-stu-id="821de-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="821de-141">Повторите эти шаги для каждого процесса, требующего электронной подписи.</span><span class="sxs-lookup"><span data-stu-id="821de-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="821de-142">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="821de-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="821de-143">Создание пользовательского требования к электронном подписям</span><span class="sxs-lookup"><span data-stu-id="821de-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="821de-144">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="821de-144">Click New.</span></span>
2. <span data-ttu-id="821de-145">Установите или снимите флажок "Необходима подпись".</span><span class="sxs-lookup"><span data-stu-id="821de-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="821de-146">В поле "Имя" введите имя процесса, для которого требуется электронная подпись.</span><span class="sxs-lookup"><span data-stu-id="821de-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="821de-147">В поле "Имя таблицы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="821de-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="821de-148">Найдите и выберите в списке таблицу, где хранятся данные, которые необходимо подписать.</span><span class="sxs-lookup"><span data-stu-id="821de-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="821de-149">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="821de-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="821de-150">В поле "Имя поля" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="821de-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="821de-151">Найдите и выберите в списке поле таблицы, которое необходимо контролировать.</span><span class="sxs-lookup"><span data-stu-id="821de-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="821de-152">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="821de-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="821de-153">Укажите, когда требуется подпись.</span><span class="sxs-lookup"><span data-stu-id="821de-153">Specify when a signature is required.</span></span>     <span data-ttu-id="821de-154">Выберите "Всегда", если подпись требуется при изменении данных в поле.</span><span class="sxs-lookup"><span data-stu-id="821de-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="821de-155">Выберите "Только", если подпись требуется только при определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="821de-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="821de-156">При выборе варианта "Только" также необходимо выбрать один из следующих вариантов: "При вставке записи", "При обновлении записи" или "При удалении записи".</span><span class="sxs-lookup"><span data-stu-id="821de-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="821de-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="821de-157">Click Save.</span></span>
11. <span data-ttu-id="821de-158">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="821de-158">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]