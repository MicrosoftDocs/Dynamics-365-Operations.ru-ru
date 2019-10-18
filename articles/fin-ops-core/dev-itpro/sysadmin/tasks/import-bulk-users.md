---
title: Импорт пользователей в пакетном режиме
description: Эта процедура используется системными администраторами для импорта большого числа пользователей из Azure Active Directory.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2c316465f8c6964a562e92ce0a2233b37d38fe
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180906"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="e12ee-103">Импорт пользователей в пакетном режиме</span><span class="sxs-lookup"><span data-stu-id="e12ee-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e12ee-104">Эта процедура используется системными администраторами для импорта большого числа пользователей из Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e12ee-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="e12ee-105">Выполнить пакетное задание</span><span class="sxs-lookup"><span data-stu-id="e12ee-105">Run as a batch job</span></span>
1. <span data-ttu-id="e12ee-106">Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="e12ee-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="e12ee-107">Щелкните "Пакетный импорт".</span><span class="sxs-lookup"><span data-stu-id="e12ee-107">Click Batch import.</span></span>
3. <span data-ttu-id="e12ee-108">Разверните раздел "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="e12ee-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="e12ee-109">Выберите значение "Да" в поле "Пакетная обработка".</span><span class="sxs-lookup"><span data-stu-id="e12ee-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="e12ee-110">В поле "Описание задачи" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e12ee-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="e12ee-111">В поле "Группа партий" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e12ee-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="e12ee-112">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="e12ee-112">This is an optional step.</span></span>  
7. <span data-ttu-id="e12ee-113">Выберите "Да" в поле "Частный".</span><span class="sxs-lookup"><span data-stu-id="e12ee-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="e12ee-114">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="e12ee-114">This is an optional step.</span></span>  
8. <span data-ttu-id="e12ee-115">Выберите "Да" в поле "Критическое задание".</span><span class="sxs-lookup"><span data-stu-id="e12ee-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="e12ee-116">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="e12ee-116">This is an optional step.</span></span>  
9. <span data-ttu-id="e12ee-117">В поле "Категория мониторинга" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="e12ee-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="e12ee-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e12ee-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="e12ee-119">Запуск в песочнице</span><span class="sxs-lookup"><span data-stu-id="e12ee-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="e12ee-120">Щелкните "Пакетный импорт".</span><span class="sxs-lookup"><span data-stu-id="e12ee-120">Click Batch import.</span></span>
2. <span data-ttu-id="e12ee-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e12ee-121">Click OK.</span></span>

