---
title: Покупка и продажа отпуска
description: В Dynamics 365 Human Resources можно отправлять запросы на покупку и продажу отпуска, используя политики покупки и продажи отпуска, настроенные вашей компанией.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271501"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="99502-103">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="99502-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="99502-104">В Dynamics 365 Human Resources можно отправлять запросы на покупку и продажу отпуска, используя политики покупки и продажи отпуска, настроенные вашей компанией.</span><span class="sxs-lookup"><span data-stu-id="99502-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="99502-105">Запрос на покупку отпуска</span><span class="sxs-lookup"><span data-stu-id="99502-105">Request to buy leave</span></span>

1. <span data-ttu-id="99502-106">В рабочей области **Самообслуживания сотрудников** выберите **Запрос на покупку отпуска** на плитке **Время отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="99502-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="99502-107">Добавьте **Тип отпуска** и введите **Сумма** для суммы отпуска, которую вы хотите купить.</span><span class="sxs-lookup"><span data-stu-id="99502-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="99502-108">Выберите **Отправить**, когда будете готовы отправить запрос.</span><span class="sxs-lookup"><span data-stu-id="99502-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="99502-109">Ваши балансы будут автоматически обновляться или проходить через процесс утверждения перед обновлением.</span><span class="sxs-lookup"><span data-stu-id="99502-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="99502-110">Это зависит от настройки политики покупки.</span><span class="sxs-lookup"><span data-stu-id="99502-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="99502-111">Запрос на продажу отпуска</span><span class="sxs-lookup"><span data-stu-id="99502-111">Request to sell leave</span></span>

1. <span data-ttu-id="99502-112">В рабочей области **Самообслуживания сотрудников** выберите **Запрос на продажу отпуска** на плитке **Время отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="99502-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="99502-113">Добавьте **Тип отпуска** и введите **Сумма** для суммы отпуска, которую вы хотите продать.</span><span class="sxs-lookup"><span data-stu-id="99502-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="99502-114">Выберите **Отправить**, когда будете готовы отправить запрос.</span><span class="sxs-lookup"><span data-stu-id="99502-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="99502-115">Ваши балансы будут автоматически обновляться или проходить через процесс утверждения перед обновлением.</span><span class="sxs-lookup"><span data-stu-id="99502-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="99502-116">Это зависит от настройки политики покупки.</span><span class="sxs-lookup"><span data-stu-id="99502-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="99502-117">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="99502-117">Troubleshooting</span></span> 

<span data-ttu-id="99502-118">Если рабочий процесс в запросе на покупку или продажу заканчивается неудачей, пользователи с привилегией **EssLeaveBuySellRequestApprover** могут проверить журнал сообщений для всех запросов на покупку и продажу.</span><span class="sxs-lookup"><span data-stu-id="99502-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="99502-119">Для этого перейдите к пункту **Отпуск и отсутствие > Ссылка > Запросы на покупку и продажу отпуска > Журнал сообщений** (в верхнем левом углу).</span><span class="sxs-lookup"><span data-stu-id="99502-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="99502-120">**Журнал сообщений** показывает пользователям, как были обработаны проводки, и связанную историю workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="99502-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="99502-121">См. также</span><span class="sxs-lookup"><span data-stu-id="99502-121">See also</span></span>

[<span data-ttu-id="99502-122">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="99502-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="99502-123">Управление политиками покупки и продажи отпусков</span><span class="sxs-lookup"><span data-stu-id="99502-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
