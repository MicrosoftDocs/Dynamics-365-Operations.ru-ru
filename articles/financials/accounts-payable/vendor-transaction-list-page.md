---
title: "Страница списка \"Проводка по поставщику\""
description: "В этой теме приведена информация о странице списка \"Проводка по поставщику\" в Microsoft Dynamics 365 for Finance and Operations."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: ru-ru
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-transaction-list-page"></a><span data-ttu-id="98d30-103">Страница списка "Проводка по поставщику"</span><span class="sxs-lookup"><span data-stu-id="98d30-103">Vendor transaction list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="98d30-104">Просмотр сопоставлений</span><span class="sxs-lookup"><span data-stu-id="98d30-104">View settlements</span></span>

<span data-ttu-id="98d30-105">Вкладка **Просмотр сопоставлений** в области действий обеспечивает быстрый доступ к истории сопоставления и дополнительной информации о проводке сопоставления в целом.</span><span class="sxs-lookup"><span data-stu-id="98d30-105">The **View settlements** tab on the action pane provides quick access to settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="98d30-106">Также можно отображать дополнительные проводки, связанные с выбранной проводкой — либо потому что они входят в то же сопоставление, либо потому что они представляют собой платежи, созданные в том же журнале платежей.</span><span class="sxs-lookup"><span data-stu-id="98d30-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="98d30-107">Выберите **Расчеты с поставщиками \> Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="98d30-107">Select **Accounts payable \> All vendors**.</span></span>
2. <span data-ttu-id="98d30-108">Выберите поставщика, по которому есть проводки, а затем выберите **Поставщик \> Проводки**.</span><span class="sxs-lookup"><span data-stu-id="98d30-108">Select a vendor that has transactions, and then select **Vendor \> Transactions**.</span></span>
3. <span data-ttu-id="98d30-109">Выберите проводку, которую вы хотите изучить.</span><span class="sxs-lookup"><span data-stu-id="98d30-109">Select a transaction to research.</span></span>
4. <span data-ttu-id="98d30-110">Выберите вкладку **Просмотр сопоставлений** в области действий.</span><span class="sxs-lookup"><span data-stu-id="98d30-110">Select the **View settlements** tab on the action pane.</span></span>

    <span data-ttu-id="98d30-111">Откроется диалоговое окно **Просмотр сопоставлений** с выбранной проводкой и всеми документами, которые с ней сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="98d30-111">The **View settlements** dialog box opens and shows the selected transaction and all documents that are settled against it.</span></span> <span data-ttu-id="98d30-112">Это диалоговое окно напоминает представление истории сопоставления, однако включает в себя все связанные документы.</span><span class="sxs-lookup"><span data-stu-id="98d30-112">This dialog box resembles the settlement history view, but it includes all related documents.</span></span>

5. <span data-ttu-id="98d30-113">В этом диалоговом окне можно выполнять различные задачи.</span><span class="sxs-lookup"><span data-stu-id="98d30-113">You can perform various tasks from this dialog box.</span></span> <span data-ttu-id="98d30-114">Выберите один или несколько ваучеров, а затем выберите один из следующих пунктов меню:</span><span class="sxs-lookup"><span data-stu-id="98d30-114">Select one or more vouchers, and then select one of the following menus:</span></span>

   - <span data-ttu-id="98d30-115">**Просмотр учета** — отображаются все ваучеры, связанные с выбранными документами.</span><span class="sxs-lookup"><span data-stu-id="98d30-115">**View accounting** – All vouchers that are related to the selected documents appear.</span></span> <span data-ttu-id="98d30-116">Выберите **Закрыть**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="98d30-116">Select **Close** to close the dialog box.</span></span>
   - <span data-ttu-id="98d30-117">**Экспорт** — экспорт выбранных ваучеров в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="98d30-117">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
   - <span data-ttu-id="98d30-118">**Просмотр связанных платежей** — отображаются все проводки журнала платежей, созданные в журнале платежей, связанном с выбранным документом.</span><span class="sxs-lookup"><span data-stu-id="98d30-118">**View related payments** – All the payment journal transactions that were created in the payment journal that is related to the selected document appear.</span></span> <span data-ttu-id="98d30-119">Кроме того, отображаются все сопоставления, связанные с этими платежами.</span><span class="sxs-lookup"><span data-stu-id="98d30-119">In addition, all the settlements that are related to those payments appear.</span></span> <span data-ttu-id="98d30-120">Метка этого пункта меню также меняется на **Просмотр сопоставлений**.</span><span class="sxs-lookup"><span data-stu-id="98d30-120">The label of this menu also changes to **View settlements**.</span></span> <span data-ttu-id="98d30-121">Выберите **Просмотр сопоставлений**, чтобы отобразить только те проводки, которые отображались при первом открытии диалогового окна **Просмотр сопоставлений**.</span><span class="sxs-lookup"><span data-stu-id="98d30-121">Select **View settlements** to show only the transactions that were shown when you first opened the  **View settlements** dialog box.</span></span>
    - <span data-ttu-id="98d30-122">**Сопоставление проводок** — этот пункт меню отображается, если исходный выбранный документ не был полностью сопоставлен.</span><span class="sxs-lookup"><span data-stu-id="98d30-122">**Settle transactions** – This menu appears if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="98d30-123">Если выбрать его, появится диалоговое окно **Сопоставление проводок**, где можно выбрать проводки для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="98d30-123">When you select it, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="98d30-124">**Отменить сопоставление** — этот пункт меню отображается, если исходный выбранный документ был полностью сопоставлен.</span><span class="sxs-lookup"><span data-stu-id="98d30-124">**Undo settlements** – This menu appears if the original document that was selected was fully settled.</span></span> <span data-ttu-id="98d30-125">Если выбрать его, появится диалоговое окно **Отменить сопоставление**, где можно отменить сопоставления, сделанные для этого документа.</span><span class="sxs-lookup"><span data-stu-id="98d30-125">When you select it, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>

