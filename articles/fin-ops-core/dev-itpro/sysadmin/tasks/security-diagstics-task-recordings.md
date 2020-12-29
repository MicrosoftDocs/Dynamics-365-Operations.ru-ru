---
title: Диагностика безопасности для записей задач
description: В этом разделе содержатся сведения о том, как выполнять анализ и управление требованиями к разрешениям безопасности на основе записи задач.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 88eb90b35f1a9754cc4daa01d8f40cdf712db4f8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679798"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="96384-103">Диагностика безопасности для записей задач</span><span class="sxs-lookup"><span data-stu-id="96384-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="96384-104">Перед началом</span><span class="sxs-lookup"><span data-stu-id="96384-104">Before you begin</span></span>

<span data-ttu-id="96384-105">В этом разделе содержатся сведения о том, как выполнять анализ и управление требованиями к разрешениям безопасности на основе записи задач.</span><span class="sxs-lookup"><span data-stu-id="96384-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="96384-106">Перед выполнением шагов, описанных в этом разделе, необходимо провести запись задач бизнес-процесса, который требуется проанализировать.</span><span class="sxs-lookup"><span data-stu-id="96384-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="96384-107">Для записи бизнес-процесса см. раздел [Ресурсы регистратора задач](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="96384-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="96384-108">Управление безопасностью записи задач</span><span class="sxs-lookup"><span data-stu-id="96384-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="96384-109">Выберите **Администрирование системы** > **Безопасность** > **Диагностика безопасности для записи задач**.</span><span class="sxs-lookup"><span data-stu-id="96384-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="96384-110">Откройте запись задачи из нужного местоположения.</span><span class="sxs-lookup"><span data-stu-id="96384-110">Open the task recording from its location.</span></span> <span data-ttu-id="96384-111">Выберите **Открыть с этого компьютера** или **Открыть из Lifecycle Services**, а затем нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="96384-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="96384-112">Откроется страница **Сведения о пункте меню Безопасность**, на которой перечислены необходимые для процесса объекты безопасности.</span><span class="sxs-lookup"><span data-stu-id="96384-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="96384-113">Пункты меню **Действие** и **Вывод** не включаются в список.</span><span class="sxs-lookup"><span data-stu-id="96384-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="96384-114">В поле **ИД пользователя** выберите пользователя.</span><span class="sxs-lookup"><span data-stu-id="96384-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="96384-115">Если у пользователя отсутствуют разрешения на доступ к некоторым пунктам меню, поле **Отсутствующие разрешения** будет обновлено на **Да**.</span><span class="sxs-lookup"><span data-stu-id="96384-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Страница сведения о пункте меню "Безопасность"](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="96384-117">Выберите **Добавить ссылку**, чтобы просмотреть список объектов безопасности, включая роли, обязанности и привилегии, которые предоставляют отсутствующее разрешение.</span><span class="sxs-lookup"><span data-stu-id="96384-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="96384-118">Выберите объект безопасности из списка.</span><span class="sxs-lookup"><span data-stu-id="96384-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="96384-119">Если выбрана **Роль**, выберите **Добавить роль для пользователя**.</span><span class="sxs-lookup"><span data-stu-id="96384-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="96384-120">Откроется страница **Назначить пользователей ролям**.</span><span class="sxs-lookup"><span data-stu-id="96384-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="96384-121">Дополнительные сведения см. в разделе [Назначение пользователей для ролей безопасности](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="96384-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="96384-122">Если выбрано **Полномочие**, выберите **Добавить полномочие для роли**, выберите роли, к которым следует добавить полномочие, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="96384-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="96384-123">Если выбрана **Привилегия**, выберите **Добавить привилегию для полномочий**, выберите роли, к которым следует добавить полномочие, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="96384-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>
