---
title: Импорт пользователей из Azure Active Directory
description: Эта процедура используется системными администраторами для импорта вручную выбранных пользователей или для импорта большого числа пользователей из Azure Active Directory.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b6666310309817ff30ccb3902721880b829ee0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679822"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="18ab5-103">Импорт пользователей из Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="18ab5-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="18ab5-104">Импорт выбранных пользователей</span><span class="sxs-lookup"><span data-stu-id="18ab5-104">Import select users</span></span>

<span data-ttu-id="18ab5-105">Эта процедура используется системными администраторами для импорта выбранных пользователей из Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="18ab5-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="18ab5-106">Пользователь будет импортирован с компанией текущего сеанса в качестве компании по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="18ab5-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="18ab5-107">Измените текущую компанию, если это применимо, прежде чем импортировать пользователей.</span><span class="sxs-lookup"><span data-stu-id="18ab5-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="18ab5-108">Перейдите в раздел **Администрирование системы > Пользователи > Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="18ab5-109">Щелкните **Импорт пользователей**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-109">Click **Import users**.</span></span>
4. <span data-ttu-id="18ab5-110">Выберите пользователей, которых необходимо импортировать, и выберите **Импорт пользователей**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="18ab5-111">После завершения импорта потребуется назначить роли пользователям.</span><span class="sxs-lookup"><span data-stu-id="18ab5-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="18ab5-112">Импорт пользователей в пакетном режиме</span><span class="sxs-lookup"><span data-stu-id="18ab5-112">Import users in bulk</span></span>

<span data-ttu-id="18ab5-113">Эта процедура используется системными администраторами для импорта большого числа пользователей из Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="18ab5-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="18ab5-114">Обратите внимание, что при использовании параметра пакетного импорта выбирать пользователей невозможно.</span><span class="sxs-lookup"><span data-stu-id="18ab5-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="18ab5-115">Запуск импорта в качестве пакетной задачи</span><span class="sxs-lookup"><span data-stu-id="18ab5-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="18ab5-116">Пользователь будет импортирован с компанией текущего сеанса в качестве компании по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="18ab5-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="18ab5-117">Измените текущую компанию, если это применимо, прежде чем импортировать пользователей.</span><span class="sxs-lookup"><span data-stu-id="18ab5-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="18ab5-118">Перейдите в раздел **Администрирование системы > Пользователи > Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="18ab5-119">Выберите **Пакетный импорт**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="18ab5-120">Разверните раздел **Выполнять в фоновом режиме**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="18ab5-121">Выберите значение **Да** в поле **Пакетная обработка**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-121">Select \*\*Yes in the **Batch processing** field.</span></span>
6. <span data-ttu-id="18ab5-122">В поле **Группа пакетной обработке** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="18ab5-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="18ab5-123">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="18ab5-123">This is an optional step.</span></span>  
7. <span data-ttu-id="18ab5-124">Выберите **Да** в поле **Частный**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="18ab5-125">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="18ab5-125">This is an optional step.</span></span>  
8. <span data-ttu-id="18ab5-126">Выберите **Да** в поле **Критическое задание**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="18ab5-127">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="18ab5-127">bThis is an optional step.</span></span>  
9. <span data-ttu-id="18ab5-128">В поле **Категория мониторинга** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="18ab5-128">In the \*\*Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="18ab5-129">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-129">Click **OK**.</span></span>

<span data-ttu-id="18ab5-130">После завершения импорта потребуется назначить роли пользователям.</span><span class="sxs-lookup"><span data-stu-id="18ab5-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="18ab5-131">Запуск в песочнице</span><span class="sxs-lookup"><span data-stu-id="18ab5-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="18ab5-132">Выберите **Пакетный импорт**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="18ab5-133">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="18ab5-133">Select **OK**.</span></span>
