---
title: Удаленные или устаревшие функции Platform
description: В этом разделе описываются возможности, который удалены или которые планируется удалить в обновлениях платформы приложений Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087891"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="73407-103">Удаленные или устаревшие функции Platform</span><span class="sxs-lookup"><span data-stu-id="73407-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73407-104">В этом разделе описываются возможности, который удалены или которые планируется удалить в обновлениях платформы приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="73407-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="73407-105">*Удаленная* функция больше недоступна в продукте.</span><span class="sxs-lookup"><span data-stu-id="73407-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="73407-106">*Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.</span><span class="sxs-lookup"><span data-stu-id="73407-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="73407-107">Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании.</span><span class="sxs-lookup"><span data-stu-id="73407-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="73407-108">Подробные сведения об объектах в приложениях Finance and Operations можно найти в документе [Технический справочник по отчетам](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="73407-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="73407-109">Можно сравнить различные версии этих отчетов, чтобы получить сведения об объектах, которые были изменены или были исключены в каждой версии приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="73407-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="73407-110">Обновление платформы update 32</span><span class="sxs-lookup"><span data-stu-id="73407-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="73407-111">Диалоговое окно "запрос на изменение бизнес-правила" больше не включает раскрывающийся список выбора пользователя</span><span class="sxs-lookup"><span data-stu-id="73407-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="73407-112">**Причина устаревания/удаления**</span><span class="sxs-lookup"><span data-stu-id="73407-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="73407-113">Это связано с безопасностью, поскольку запрос на изменение может быть отправлен непредусмотренному пользователю.</span><span class="sxs-lookup"><span data-stu-id="73407-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="73407-114">Это также проблема для удобства использования, поскольку требует от пользователя определить, кто был инициатор workflow-процесса, и вручную выбрать их.</span><span class="sxs-lookup"><span data-stu-id="73407-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="73407-115">**Заменена другой функцией?**</span><span class="sxs-lookup"><span data-stu-id="73407-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="73407-116">Нет</span><span class="sxs-lookup"><span data-stu-id="73407-116">No</span></span> |
| <span data-ttu-id="73407-117">**Затрагиваемые области продукта**</span><span class="sxs-lookup"><span data-stu-id="73407-117">**Product areas affected**</span></span>         | <span data-ttu-id="73407-118">Рабочий процесс</span><span class="sxs-lookup"><span data-stu-id="73407-118">Workflow</span></span> |
| <span data-ttu-id="73407-119">**Вариант развертывания**</span><span class="sxs-lookup"><span data-stu-id="73407-119">**Deployment option**</span></span>              | <span data-ttu-id="73407-120">Все</span><span class="sxs-lookup"><span data-stu-id="73407-120">All</span></span> |
| <span data-ttu-id="73407-121">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="73407-121">**Status**</span></span>                         | <span data-ttu-id="73407-122">Раскрывающийся список выбора пользователя был удален из диалогового окна запроса на изменение в обновлении платформы 32.</span><span class="sxs-lookup"><span data-stu-id="73407-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="73407-123">Запросы на изменение запроса будут автоматически отправлены инициатору по назначению.</span><span class="sxs-lookup"><span data-stu-id="73407-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="73407-124">Дополнительные сведения об этих функциях см. в разделе [Действия в процессах утверждения workflow-процесса](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="73407-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="73407-125">Предыдущие объявления об удаленных или устаревших функциях</span><span class="sxs-lookup"><span data-stu-id="73407-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="73407-126">Для получения дополнительных сведений о функциях, которые были удалены или устарели в предыдущих выпусках, см [Удаленные или устаревшие функции в предыдущих выпусках](../migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="73407-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

