---
title: Предоставление активов в кредит
description: В этом разделе описывается, как зарегистрировать предоставленные в кредит активы в управлении активами.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 355e3d3e0e952db14a03810145528f9701804ca2
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022340"
---
# <a name="asset-loans"></a><span data-ttu-id="95b3a-103">Предоставление активов в кредит</span><span class="sxs-lookup"><span data-stu-id="95b3a-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="95b3a-104">Если ваша компания получает активы для заданий на ремонт или обслуживание от внутренних местоположений или клиентов, и если вы временно предоставили активы в кредит для этих местопложений местах или клиентов, модуль управления активами может отслеживать предоставление активов в кредит.</span><span class="sxs-lookup"><span data-stu-id="95b3a-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="95b3a-105">Регистрация кредитных активов в запросе на обслуживание</span><span class="sxs-lookup"><span data-stu-id="95b3a-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="95b3a-106">Выберите **Управление активами** \> **Общее** \> **Запросы на обслуживание** \> **Все запросы на обслуживание** или **Активные запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="95b3a-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="95b3a-107">Выберите запрос на обслуживание, чтобы зарегистрировать в нем кредитный актив, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="95b3a-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="95b3a-108">На странице **Запрос** выберите **Отправить кредитный актив**.</span><span class="sxs-lookup"><span data-stu-id="95b3a-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="95b3a-109">Выберите актив и введите ожидаемую дату возврата.</span><span class="sxs-lookup"><span data-stu-id="95b3a-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="95b3a-110">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="95b3a-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="95b3a-111">Вы можете отправить кредитный актив только в том случае, если имеется доступный актив с тем же типом активов.</span><span class="sxs-lookup"><span data-stu-id="95b3a-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="95b3a-112">Актив, который вы предоставляете в кредит, должен иметь состояние жизненного цикла активов, которое допускает предоставление актива в кредит, например **InStorage** (На хранении).</span><span class="sxs-lookup"><span data-stu-id="95b3a-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="95b3a-113">Когда предоставление актива в кредит зарегистрировано, состояние жизненного цикла актива автоматически обновляется на, например, **OnLoan** (Передано во временное пользование).</span><span class="sxs-lookup"><span data-stu-id="95b3a-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="95b3a-114">Чтобы просмотреть список всех активов, которые вы одолжили другим местопложениям или клиентам, выберите **Управление активами** \> **Общее** \> **Предоставление активов в кредит** \> **Все предоставленные в кредит активы**.</span><span class="sxs-lookup"><span data-stu-id="95b3a-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="95b3a-115">Если для актива установлен флажок **Завершено**, актив был зарегистрирован как возвращенный вашей компании.</span><span class="sxs-lookup"><span data-stu-id="95b3a-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Управление запросами на обслуживание](media/06-manage-maintenance-requests.png)

<span data-ttu-id="95b3a-117">На странице **Активные предоставления актива в кредит** можно просмотреть список всех кредитных активов, которые еще не возвращены вашей компании.</span><span class="sxs-lookup"><span data-stu-id="95b3a-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="95b3a-118">Регистрация кредитных активов как возвращенных</span><span class="sxs-lookup"><span data-stu-id="95b3a-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="95b3a-119">Выберите **Управление активами** \> **Общие** \> **Предоставление активов в кредит** \> **Активные предоставления активов в кредит**.</span><span class="sxs-lookup"><span data-stu-id="95b3a-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="95b3a-120">Выберите предоставление актива в кредит, чтобы зарегистрироваться в качестве возвращенного, затем выберите **Возврат представленного в кредит актива**.</span><span class="sxs-lookup"><span data-stu-id="95b3a-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="95b3a-121">В поле **Возвращено** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="95b3a-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="95b3a-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="95b3a-122">Select **OK**.</span></span>
5. <span data-ttu-id="95b3a-123">Обновите страницу списка **Активные предоставления активов в кредит** и обратите внимание, что кредитный актив больше не отображается в списке.</span><span class="sxs-lookup"><span data-stu-id="95b3a-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
