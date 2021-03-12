---
title: Подтверждение графиков оплаты аренды активов в пакетном режиме
description: В этой теме объясняется, как подтвердить несколько графиков оплаты в пакетном режиме.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9c680ea16e9f64107fde081c7e7763697356dcc1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971386"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="e6a0d-103">Подтверждение графиков оплаты аренды активов в пакетном режиме</span><span class="sxs-lookup"><span data-stu-id="e6a0d-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6a0d-104">В этой теме объясняется, как подтвердить несколько графиков оплаты в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="e6a0d-105">Графики оплаты подтверждаются либо на поарендной основе, либо с помощью процесса пакетной обработки подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="e6a0d-106">Запись журнала может быть разнесена только по аренде, которая имеет подтвержденный график оплаты.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="e6a0d-107">Подтверждение графика оплаты служит окончательным утверждением финансовой информации для аренды.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="e6a0d-108">Все будущие изменения финансовой информации для аренды, такие как платежи и срок аренды, составляют корректировку аренды и должны обрабатываться таким образом.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="e6a0d-109">Чтобы подтвердить несколько графиков оплаты, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="e6a0d-110">Перейдите в раздел **Аренда активов \> Периодические задачи \> Пакетное подтверждение**.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="e6a0d-111">На странице **Пакетное подтверждение** выберите **Пакетное подтверждение**.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="e6a0d-112">В появившемся диалоговом окне отфильтруйте книги, которые требуется подтвердить.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="e6a0d-113">Чтобы подтвердить все книги в конкретной группе аренды, выберите группу в поле **Группа аренды**.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="e6a0d-114">Чтобы подтвердить отдельные книги, выберите книги в поле **Код книги**.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="e6a0d-115">Чтобы подтвердить все книги, включите параметр **Для всех книг**.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="e6a0d-116">Сведения для вновь подтвержденных книг отображаются на странице **Подтвержденные книги**.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="e6a0d-117">После подтверждения графиков оплаты записи журнала начального признания могут быть разнесены по арендам.</span><span class="sxs-lookup"><span data-stu-id="e6a0d-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>
