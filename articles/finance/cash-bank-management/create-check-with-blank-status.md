---
title: Создание чеков, имеющих пустой статус
description: В этом разделе объясняется, как создать пустые чеки для банковского счета на странице "Чеки".
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: af79dd4831f2e7fc71c296922d73a9e42f7955b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176067"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="48d8f-103">Создание чеков, имеющих пустой статус</span><span class="sxs-lookup"><span data-stu-id="48d8f-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="48d8f-104">В этом разделе объясняется, как создавать пустые чеки.</span><span class="sxs-lookup"><span data-stu-id="48d8f-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="48d8f-105">Например, можно создать пустой чек для учета чека, который был поврежден и не может использоваться для оплаты.</span><span class="sxs-lookup"><span data-stu-id="48d8f-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="48d8f-106">На странице **Чеки** выполняются задачи обслуживания для чеков.</span><span class="sxs-lookup"><span data-stu-id="48d8f-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="48d8f-107">Например, можно создать новые номера чеков и удалить чеки.</span><span class="sxs-lookup"><span data-stu-id="48d8f-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="48d8f-108">Можно также создать чеки со статусом **Пустой**.</span><span class="sxs-lookup"><span data-stu-id="48d8f-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="48d8f-109">После создания пустых чеков они не могут быть удалены или повторно использованы в системе.</span><span class="sxs-lookup"><span data-stu-id="48d8f-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="48d8f-110">Эта функция доступна на странице **Чеки** только в том случае, если вы включите функцию **Создать чеки с пустым статусом на странице "Чеки"** на странице **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="48d8f-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="48d8f-111">Если эта функция не включена, чеки, имеющие статус **Пустой**, могут быть созданы только из диалогового окна **Платеж чеком** в процессе создания платежа в модуле "Расчеты с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="48d8f-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="48d8f-112">Чтобы открыть страницу **Чеки**, перейдите в раздел **Управление банком и кассовыми операциями \> Банковские счета \> Банковские счета**, а затем на панели операций на вкладке **Управление платежами** в группе **Связанные сведения** выберите **Чеки**.</span><span class="sxs-lookup"><span data-stu-id="48d8f-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="48d8f-113">Также можно перейти в раздел **Управление банком и кассовыми операциями \> Запросы и отчеты \> Чеки**.</span><span class="sxs-lookup"><span data-stu-id="48d8f-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="48d8f-114">Затем, чтобы создать чеки с **пустым** статусом, в панели операций выберите **Создать пустые чеки**.</span><span class="sxs-lookup"><span data-stu-id="48d8f-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="48d8f-115">Когда система создает пустые чеки, соответствующий банковский счет временно деактивируется.</span><span class="sxs-lookup"><span data-stu-id="48d8f-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="48d8f-116">Это поведение снижает риск создания платежей одновременно с созданием пустых чеков.</span><span class="sxs-lookup"><span data-stu-id="48d8f-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="48d8f-117">После завершения обработки соответствующий банковский счет повторно активируется.</span><span class="sxs-lookup"><span data-stu-id="48d8f-117">When the processing is completed, the associated bank account is reactivated.</span></span>