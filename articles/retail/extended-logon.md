---
title: "Настройка функции расширенного входа для Cloud POS и MPOS"
description: "В этом разделе описываются параметры настройки расширенного входа для Cloud POS и Retail Modern POS (MPOS)."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8075abccdcdde21df967dcc9948a738895f35cef
ms.openlocfilehash: d369b760047a18c82dd89f3452d94b9c62ba8841
ms.contentlocale: ru-ru
ms.lasthandoff: 01/25/2018

---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a><span data-ttu-id="adfc3-103">Настройка функции расширенного входа для Cloud POS и MPOS</span><span class="sxs-lookup"><span data-stu-id="adfc3-103">Set up extended logon functionality for Cloud POS and MPOS</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="adfc3-104">В этом разделе описываются параметры настройки расширенного входа для Cloud POS и Retail Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="adfc3-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

## <a name="setting-up-extended-logon"></a><span data-ttu-id="adfc3-105">Настройка расширенного входа</span><span class="sxs-lookup"><span data-stu-id="adfc3-105">Setting up extended logon</span></span>

<span data-ttu-id="adfc3-106">Можно найти настройку для масок штрих-кода в разделе **Розница** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **Профили POS** &gt; **Профили функциональности**.</span><span class="sxs-lookup"><span data-stu-id="adfc3-106">You can find the setup for bar code masks at **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="adfc3-107">Экспресс-вкладка **Функции** включает следующие параметры, связанные с расширенным входом.</span><span class="sxs-lookup"><span data-stu-id="adfc3-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="adfc3-108">Вход персонала по штрих-коду</span><span class="sxs-lookup"><span data-stu-id="adfc3-108">Staff bar code logon</span></span>

<span data-ttu-id="adfc3-109">Если включен параметр **Вход персонала по штрих-коду**, сотрудники, учетным данным POS которых назначен расширенный вход, могут входить с использованием штрихкода.</span><span class="sxs-lookup"><span data-stu-id="adfc3-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="adfc3-110">Для входа со штрих-кодом требуется пароль</span><span class="sxs-lookup"><span data-stu-id="adfc3-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="adfc3-111">Если включен параметр **Для входа со штрих-кодом требуется пароль**, при входе персонала по штрихкоду выбирается только работник, назначенный представленному расширенному входу.</span><span class="sxs-lookup"><span data-stu-id="adfc3-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="adfc3-112">Если этот параметр включен, работники обязаны вводить пароль.</span><span class="sxs-lookup"><span data-stu-id="adfc3-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="adfc3-113">Вход персонала по карточке</span><span class="sxs-lookup"><span data-stu-id="adfc3-113">Staff card logon</span></span>

<span data-ttu-id="adfc3-114">Если включен параметр **Вход персонала по карте**, сотрудники, учетным данным POS которых назначен расширенный вход, могут входить с использованием магнитной ленты.</span><span class="sxs-lookup"><span data-stu-id="adfc3-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="adfc3-115">Для входа по карте персонала требуется пароль</span><span class="sxs-lookup"><span data-stu-id="adfc3-115">Staff card logon requires password</span></span>

<span data-ttu-id="adfc3-116">Если включен параметр **Для входа с картой требуется пароль**, при входе персонала по карте выбирается только работник, назначенный представленному расширенному входу.</span><span class="sxs-lookup"><span data-stu-id="adfc3-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="adfc3-117">Если этот параметр включен, работники обязаны вводить пароль.</span><span class="sxs-lookup"><span data-stu-id="adfc3-117">Workers must still enter their password when this option is enabled.</span></span>

## <a name="assigning-an-extended-logon"></a><span data-ttu-id="adfc3-118">Назначение расширенного входа</span><span class="sxs-lookup"><span data-stu-id="adfc3-118">Assigning an extended logon</span></span>

<span data-ttu-id="adfc3-119">По умолчанию только менеджеры могут назначать работникам расширенный вход.</span><span class="sxs-lookup"><span data-stu-id="adfc3-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="adfc3-120">Чтобы назначить расширенный вход, перейдите в раздел **Расширенный вход** в POS.</span><span class="sxs-lookup"><span data-stu-id="adfc3-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="adfc3-121">Затем выполните поиск работника, введя его код оператора в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="adfc3-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="adfc3-122">Выберите работника, а затем выберите **Назначить**.</span><span class="sxs-lookup"><span data-stu-id="adfc3-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="adfc3-123">На следующей странице проведите пальцем по расширенному входу или сканируйте его, чтобы назначить работнику.</span><span class="sxs-lookup"><span data-stu-id="adfc3-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="adfc3-124">Если проведение пальцем или сканирование прочитано удачно, становится доступной кнопка **ОК**.</span><span class="sxs-lookup"><span data-stu-id="adfc3-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="adfc3-125">Нажмите кнопку **ОК**, чтобы сохранить расширенный вход для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="adfc3-125">Click **OK** to save the extended logon for that worker.</span></span>

## <a name="deleting-an-extended-logon"></a><span data-ttu-id="adfc3-126">Удаление расширенного входа</span><span class="sxs-lookup"><span data-stu-id="adfc3-126">Deleting an extended logon</span></span>

<span data-ttu-id="adfc3-127">Чтобы удалить расширенный вход, назначенный работнику, найдите работника с помощью операции **Расширенный вход**.</span><span class="sxs-lookup"><span data-stu-id="adfc3-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="adfc3-128">Выберите работника, а затем выберите **Отменить**.</span><span class="sxs-lookup"><span data-stu-id="adfc3-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="adfc3-129">Все учетные данные расширенного входа, связанные с этим работником, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="adfc3-129">All extended logon credentials that are associated with that worker are removed.</span></span>

## <a name="extending-extended-logon"></a><span data-ttu-id="adfc3-130">Расширение расширенного входа</span><span class="sxs-lookup"><span data-stu-id="adfc3-130">Extending extended logon</span></span>

<span data-ttu-id="adfc3-131">Услугу входа в систему можно расширить, чтобы обеспечить поддержку дополнительных устройств расширенного входа, например сканеров ладони.</span><span class="sxs-lookup"><span data-stu-id="adfc3-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="adfc3-132">Дополнительные сведения см. в документации по расширяемости POS.</span><span class="sxs-lookup"><span data-stu-id="adfc3-132">For more information, see the POS extensibility documentation.</span></span>

## <a name="using-extended-logon"></a><span data-ttu-id="adfc3-133">Использование расширенного входа</span><span class="sxs-lookup"><span data-stu-id="adfc3-133">Using extended logon</span></span>

<span data-ttu-id="adfc3-134">Если настроен расширенный вход и работнику назначен штрихкод или магнитная лента, работнику достаточно провести картой или сканировать ее, когда отображается страница входа POS.</span><span class="sxs-lookup"><span data-stu-id="adfc3-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="adfc3-135">Если пароль также требуется перед страницей входа, работнику предложат ввести пароль.</span><span class="sxs-lookup"><span data-stu-id="adfc3-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>




