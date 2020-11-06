---
title: Отмена работы склада для обработки исключений
description: В этом разделе описывается функция отмены работы, которая позволяет супервизорам склада обрабатывать заблокированные работы.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: daa8f0d19de75e6c126fe7a5fe312bca24c89bdc
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016249"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="da055-103">Отмена работы склада для обработки исключений</span><span class="sxs-lookup"><span data-stu-id="da055-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da055-104">Функция "Отмена работы" в Microsoft Dynamics 365 Supply Chain Management позволяет пользователю "Администратор" отменять отдельную работу склада, которая в данный момент выполняется, но которая заблокирована системой или не может быть завершена из-за исключительных обстоятельств.</span><span class="sxs-lookup"><span data-stu-id="da055-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="da055-105">Эта функция является привлекательной и безопасной альтернативой корректирующим сценариям SQL, которые исправляют несогласованные данные.</span><span class="sxs-lookup"><span data-stu-id="da055-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="da055-106">Однако, в то время как эти сценарии обычно запрашиваются ИТ-специалистами, функция отмены работы может использоваться пользователями компании, имеющими права администратора.</span><span class="sxs-lookup"><span data-stu-id="da055-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="da055-107">Вы можете получить доступ к функции отмены работы на странице **Управление складом** \> **периодические задачи** \> **Очистка \> Отмена работы**.</span><span class="sxs-lookup"><span data-stu-id="da055-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="da055-108">В диалоговом окне **Отмена работы** укажите код работы для отмены и затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="da055-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="da055-109">Складские работы, которые могут быть отменены</span><span class="sxs-lookup"><span data-stu-id="da055-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="da055-110">Во время операций комплектации склада работник может столкнуться с ситуациями, когда они регистрировали количества как скомплектованные из местоположения хранения в местоположение пользователя, но затем они не могут зарегистрировать операцию размещения.</span><span class="sxs-lookup"><span data-stu-id="da055-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="da055-111">Несогласованные данные склада часто, но не всегда, являются причина блокирования работы.</span><span class="sxs-lookup"><span data-stu-id="da055-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="da055-112">В отличие от обычных функций отмены, к которым можно получить доступ с помощью кнопки **Отмена** в заголовке работы, функция отмены работы не требует, чтобы последняя строка выполненных работ была строкой работы типа **Размещение**.</span><span class="sxs-lookup"><span data-stu-id="da055-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="da055-113">Другими словами, для функции отмены работы можно выполнить логику отмены, даже если количество номенклатуры в строке работ находится в местоположении пользователя.</span><span class="sxs-lookup"><span data-stu-id="da055-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="da055-114">Для работы, которая должна быть отменена в операционную причину, пользователи склада должны продолжать использовать функцию обычной отмены на странице работ.</span><span class="sxs-lookup"><span data-stu-id="da055-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="da055-115">С помощью функции отмены можно отменить только работы типа **Продажи** , **Выдача на перемещение** , **Комплектация сырья** , **Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="da055-115">Only work of the **Sales** , **Transfer issue** , **Raw material picking** , or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="da055-116">Логика отмены не будет выполняться для заблокированных работ по комплектации сырья или работ, которые могут быть отменены с помощью обычной функции отмены (см. предыдущую заметку).</span><span class="sxs-lookup"><span data-stu-id="da055-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="da055-117">Чтобы разблокировать работу, система отменяет все оставшиеся строки работ и исправляет данные склада, связанные с кодом работ, указанным пользователем.</span><span class="sxs-lookup"><span data-stu-id="da055-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="da055-118">Любые обычные операции обработки склада, включающие затронутое количество номенклатуры, могут быть возобновлены.</span><span class="sxs-lookup"><span data-stu-id="da055-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="da055-119">Чтобы разместить затронутую номенклатуру в конкретное местоположение после отмены работы, пользователь должен использовать операцию перемещения запасов или корректировку количества на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="da055-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
