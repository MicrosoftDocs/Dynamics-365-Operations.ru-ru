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
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 07472188051aea7084142cc417c6d725462cf4f9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205261"
---
# <a name="asset-loans"></a><span data-ttu-id="d134e-103">Предоставление активов в кредит</span><span class="sxs-lookup"><span data-stu-id="d134e-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d134e-104">Если ваша компания получает активы для заданий на ремонт или обслуживание от внутренних местоположений или клиентов, и если вы временно предоставили активы в кредит для этих местопложений местах или клиентов, модуль управления активами может отслеживать предоставление активов в кредит.</span><span class="sxs-lookup"><span data-stu-id="d134e-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="d134e-105">Регистрация кредитных активов в запросе на обслуживание</span><span class="sxs-lookup"><span data-stu-id="d134e-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="d134e-106">Выберите **Управление активами** \> **Общее** \> **Запросы на обслуживание** \> **Все запросы на обслуживание** или **Активные запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="d134e-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="d134e-107">Выберите запрос на обслуживание, чтобы зарегистрировать в нем кредитный актив, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="d134e-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="d134e-108">На странице **Запрос** выберите **Отправить кредитный актив**.</span><span class="sxs-lookup"><span data-stu-id="d134e-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="d134e-109">Выберите актив и введите ожидаемую дату возврата.</span><span class="sxs-lookup"><span data-stu-id="d134e-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="d134e-110">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d134e-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="d134e-111">Вы можете отправить кредитный актив только в том случае, если имеется доступный актив с тем же типом активов.</span><span class="sxs-lookup"><span data-stu-id="d134e-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="d134e-112">Актив, который вы предоставляете в кредит, должен иметь состояние жизненного цикла активов, которое допускает предоставление актива в кредит, например **InStorage** (На хранении).</span><span class="sxs-lookup"><span data-stu-id="d134e-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="d134e-113">Когда предоставление актива в кредит зарегистрировано, состояние жизненного цикла актива автоматически обновляется на, например, **OnLoan** (Передано во временное пользование).</span><span class="sxs-lookup"><span data-stu-id="d134e-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="d134e-114">Чтобы просмотреть список всех активов, которые вы одолжили другим местопложениям или клиентам, выберите **Управление активами** \> **Общее** \> **Предоставление активов в кредит** \> **Все предоставленные в кредит активы**.</span><span class="sxs-lookup"><span data-stu-id="d134e-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="d134e-115">Если для актива установлен флажок **Завершено**, актив был зарегистрирован как возвращенный вашей компании.</span><span class="sxs-lookup"><span data-stu-id="d134e-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Управление запросами на обслуживание](media/06-manage-maintenance-requests.png)

<span data-ttu-id="d134e-117">На странице **Активные предоставления актива в кредит** можно просмотреть список всех кредитных активов, которые еще не возвращены вашей компании.</span><span class="sxs-lookup"><span data-stu-id="d134e-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="d134e-118">Регистрация кредитных активов как возвращенных</span><span class="sxs-lookup"><span data-stu-id="d134e-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="d134e-119">Выберите **Управление активами** \> **Общие** \> **Предоставление активов в кредит** \> **Активные предоставления активов в кредит**.</span><span class="sxs-lookup"><span data-stu-id="d134e-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="d134e-120">Выберите предоставление актива в кредит, чтобы зарегистрироваться в качестве возвращенного, затем выберите **Возврат представленного в кредит актива**.</span><span class="sxs-lookup"><span data-stu-id="d134e-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="d134e-121">В поле **Возвращено** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="d134e-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="d134e-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d134e-122">Select **OK**.</span></span>
5. <span data-ttu-id="d134e-123">Обновите страницу списка **Активные предоставления активов в кредит** и обратите внимание, что кредитный актив больше не отображается в списке.</span><span class="sxs-lookup"><span data-stu-id="d134e-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
