--- 
title: "Импорт пользователей в пакетном режиме"
description: "Эта процедура используется системными администраторами для импорта большого числа пользователей из Azure Active Directory."
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 54af656c040486f7de718ce589973a6ebe005850
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="import-users-in-bulk"></a><span data-ttu-id="a9e1e-103">Импорт пользователей в пакетном режиме</span><span class="sxs-lookup"><span data-stu-id="a9e1e-103">Import users in bulk</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9e1e-104">Эта процедура используется системными администраторами для импорта большого числа пользователей из Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a9e1e-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="a9e1e-105">Выполнить пакетное задание</span><span class="sxs-lookup"><span data-stu-id="a9e1e-105">Run as a batch job</span></span>
1. <span data-ttu-id="a9e1e-106">Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="a9e1e-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="a9e1e-107">Щелкните "Пакетный импорт".</span><span class="sxs-lookup"><span data-stu-id="a9e1e-107">Click Batch import.</span></span>
3. <span data-ttu-id="a9e1e-108">Разверните раздел "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="a9e1e-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="a9e1e-109">Выберите значение "Да" в поле "Пакетная обработка".</span><span class="sxs-lookup"><span data-stu-id="a9e1e-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="a9e1e-110">В поле "Описание задачи" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a9e1e-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="a9e1e-111">В поле "Группа партий" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a9e1e-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="a9e1e-112">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="a9e1e-112">This is an optional step.</span></span>  
7. <span data-ttu-id="a9e1e-113">Выберите "Да" в поле "Частный".</span><span class="sxs-lookup"><span data-stu-id="a9e1e-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="a9e1e-114">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="a9e1e-114">This is an optional step.</span></span>  
8. <span data-ttu-id="a9e1e-115">Выберите "Да" в поле "Критическое задание".</span><span class="sxs-lookup"><span data-stu-id="a9e1e-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="a9e1e-116">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="a9e1e-116">This is an optional step.</span></span>  
9. <span data-ttu-id="a9e1e-117">В поле "Категория мониторинга" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="a9e1e-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="a9e1e-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9e1e-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="a9e1e-119">Запуск в песочнице</span><span class="sxs-lookup"><span data-stu-id="a9e1e-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="a9e1e-120">Щелкните "Пакетный импорт".</span><span class="sxs-lookup"><span data-stu-id="a9e1e-120">Click Batch import.</span></span>
2. <span data-ttu-id="a9e1e-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9e1e-121">Click OK.</span></span>


