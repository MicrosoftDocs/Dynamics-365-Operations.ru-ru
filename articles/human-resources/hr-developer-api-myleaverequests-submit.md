---
title: Отправка запроса на отпуск в workflow-процесс
description: В Microsoft Dynamics 365 Human Resources можно воспользоваться API MyLeaveRequests submit(), чтобы отправить запрос на отпуск в workflow-процесс.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9b3151cb042012a167854a1e69b55b36981dab19
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054580"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="6e32f-103">Отправка запроса на отпуск в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="6e32f-103">Submit a leave request to workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6e32f-104">В Microsoft Dynamics 365 Human Resources можно воспользоваться API MyLeaveRequests submit(), чтобы отправить запрос на отпуск в workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="6e32f-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="6e32f-105">Этот API представляется как действие для объекта OData MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="6e32f-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6e32f-106">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="6e32f-106">Prerequisites</span></span>

<span data-ttu-id="6e32f-107">Запрос на отпуск должен быть сохранен в базе данных и должен быть доступен для извлечения с помощью объекта MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="6e32f-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="6e32f-108">Права доступа</span><span class="sxs-lookup"><span data-stu-id="6e32f-108">Permissions</span></span>

<span data-ttu-id="6e32f-109">Для вызова этого API требуется одно из следующих разрешений.</span><span class="sxs-lookup"><span data-stu-id="6e32f-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="6e32f-110">Дополнительные сведения о разрешениях и как их выбрать см. в [Аутентификация](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="6e32f-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="6e32f-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="6e32f-111">Permission type</span></span>                    | <span data-ttu-id="6e32f-112">Разрешения (от минимальных до максимальных привилегий)</span><span class="sxs-lookup"><span data-stu-id="6e32f-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="6e32f-113">Делегировано (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6e32f-113">Delegated (work or school account)</span></span> | <span data-ttu-id="6e32f-114">user\_impersonation</span><span class="sxs-lookup"><span data-stu-id="6e32f-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="6e32f-115">HTTPS-запрос</span><span class="sxs-lookup"><span data-stu-id="6e32f-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="6e32f-116">Запрос соответствует стандартам OData.</span><span class="sxs-lookup"><span data-stu-id="6e32f-116">The request conforms to OData standards.</span></span> <span data-ttu-id="6e32f-117">Параметры {requestId}, {leaveType}, {leaveDate} и {dataArea} относятся к полям, составляющим составной естественный ключ для объекта MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="6e32f-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="6e32f-118">Хотя поля для объекта MyLeaveRequests ссылаются на отдельную строку в запросе отпуска, при вызове API будет отправлен весь запрос отпуска (все строки) в workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="6e32f-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="6e32f-119">Заголовки запроса</span><span class="sxs-lookup"><span data-stu-id="6e32f-119">Request headers</span></span>

| <span data-ttu-id="6e32f-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6e32f-120">Header</span></span>         | <span data-ttu-id="6e32f-121">Value</span><span class="sxs-lookup"><span data-stu-id="6e32f-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="6e32f-122">Санкционирование</span><span class="sxs-lookup"><span data-stu-id="6e32f-122">Authorization</span></span>  | <span data-ttu-id="6e32f-123">Носитель {token} (обязательно)</span><span class="sxs-lookup"><span data-stu-id="6e32f-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="6e32f-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6e32f-124">Content-Type</span></span>   | <span data-ttu-id="6e32f-125">application/json</span><span class="sxs-lookup"><span data-stu-id="6e32f-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="6e32f-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="6e32f-126">Request body</span></span>

<span data-ttu-id="6e32f-127">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="6e32f-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="6e32f-128">Отклик</span><span class="sxs-lookup"><span data-stu-id="6e32f-128">Response</span></span>

<span data-ttu-id="6e32f-129">Успешный ответ — всегда ответ **204 No Content**.</span><span class="sxs-lookup"><span data-stu-id="6e32f-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="6e32f-130">Неавторизованные вызывающие объекты получат ответ **401 Unauthorized** или **403 Forbidden**.</span><span class="sxs-lookup"><span data-stu-id="6e32f-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="6e32f-131">Если отправка завершилась неудачей (например, из-за проверки), ответ будет **500 Server Error**, а текст ответа будет содержать объект JSON с дополнительной информацией.</span><span class="sxs-lookup"><span data-stu-id="6e32f-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="6e32f-132">Пример</span><span class="sxs-lookup"><span data-stu-id="6e32f-132">Example</span></span>

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a><span data-ttu-id="6e32f-133">Сообщения о проверке и ошибках</span><span class="sxs-lookup"><span data-stu-id="6e32f-133">Validation and error messages</span></span>

<span data-ttu-id="6e32f-134">В ходе вызова для отправки API платформа Human Resources выполняет проверку бизнес-логики перед отправкой, чтобы запрос отпуска находится в допустимом состоянии для отправки.</span><span class="sxs-lookup"><span data-stu-id="6e32f-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="6e32f-135">Возможные сообщения об ошибках, которые могут появиться в ответе в случае сбоя проверок:</span><span class="sxs-lookup"><span data-stu-id="6e32f-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="6e32f-136">В результате этого запроса сальдо '{LeaveTypeId}' будет ниже допустимого минимального сальдо на {date}.</span><span class="sxs-lookup"><span data-stu-id="6e32f-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="6e32f-137">Невозможно отправить запрос времени отсутствия в завершенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="6e32f-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="6e32f-138">Не удалось отправить или сохранить запрос, поскольку изменения не выполнены.</span><span class="sxs-lookup"><span data-stu-id="6e32f-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="6e32f-139">Добавьте или обновите сумму или тип отпуска и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="6e32f-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="6e32f-140">Введенный запрос о времени отсутствия содержит один или несколько дней с одинаковой датой и типом отпуска как существующий ожидающий запрос.</span><span class="sxs-lookup"><span data-stu-id="6e32f-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="6e32f-141">Отзовите существующий запрос для внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="6e32f-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="6e32f-142">Код основания '{ReasonCodeId}' не применяется ни к одному из типов отпуска в запросе.</span><span class="sxs-lookup"><span data-stu-id="6e32f-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="6e32f-143">Для типа отпуска {LeaveTypeId} требуется код причины.</span><span class="sxs-lookup"><span data-stu-id="6e32f-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="6e32f-144">Выберите соответствующий тип и код причины.</span><span class="sxs-lookup"><span data-stu-id="6e32f-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="6e32f-145">Время отсутствия не было отправлен успешно.</span><span class="sxs-lookup"><span data-stu-id="6e32f-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="6e32f-146">Время отсутствия сохранено как черновик запроса.</span><span class="sxs-lookup"><span data-stu-id="6e32f-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e32f-147">См. также</span><span class="sxs-lookup"><span data-stu-id="6e32f-147">See also</span></span>

- [<span data-ttu-id="6e32f-148">Обзор MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="6e32f-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="6e32f-149">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="6e32f-149">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]