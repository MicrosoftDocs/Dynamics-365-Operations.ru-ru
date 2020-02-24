---
title: Отправка запроса на отпуск в workflow-процесс
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010382"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="6b3c0-102">Отправка запроса на отпуск в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="6b3c0-102">Submit a leave request to workflow</span></span>

<span data-ttu-id="6b3c0-103">В Microsoft Dynamics 365 Human Resources можно воспользоваться API MyLeaveRequests submit(), чтобы отправить запрос на отпуск в workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-103">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="6b3c0-104">Этот API представляется как действие для объекта OData MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-104">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6b3c0-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="6b3c0-105">Prerequisites</span></span>

<span data-ttu-id="6b3c0-106">Запрос на отпуск должен быть сохранен в базе данных и должен быть доступен для извлечения с помощью объекта MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-106">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="6b3c0-107">Права доступа</span><span class="sxs-lookup"><span data-stu-id="6b3c0-107">Permissions</span></span>

<span data-ttu-id="6b3c0-108">Для вызова этого API требуется одно из следующих разрешений.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-108">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="6b3c0-109">Дополнительные сведения о разрешениях и как их выбрать см. в [Аутентификация](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="6b3c0-109">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="6b3c0-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="6b3c0-110">Permission type</span></span>                    | <span data-ttu-id="6b3c0-111">Разрешения (от минимальных до максимальных привилегий)</span><span class="sxs-lookup"><span data-stu-id="6b3c0-111">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="6b3c0-112">Делегировано (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6b3c0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6b3c0-113">user\_impersonation</span><span class="sxs-lookup"><span data-stu-id="6b3c0-113">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="6b3c0-114">HTTPS-запрос</span><span class="sxs-lookup"><span data-stu-id="6b3c0-114">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="6b3c0-115">Запрос соответствует стандартам OData.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-115">The request conforms to OData standards.</span></span> <span data-ttu-id="6b3c0-116">Параметры {requestId}, {leaveType}, {leaveDate} и {dataArea} относятся к полям, составляющим составной естественный ключ для объекта MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-116">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="6b3c0-117">Хотя поля для объекта MyLeaveRequests ссылаются на отдельную строку в запросе отпуска, при вызове API будет отправлен весь запрос отпуска (все строки) в workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-117">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="6b3c0-118">Заголовки запроса</span><span class="sxs-lookup"><span data-stu-id="6b3c0-118">Request headers</span></span>

| <span data-ttu-id="6b3c0-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6b3c0-119">Header</span></span>         | <span data-ttu-id="6b3c0-120">Value</span><span class="sxs-lookup"><span data-stu-id="6b3c0-120">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="6b3c0-121">Санкционирование</span><span class="sxs-lookup"><span data-stu-id="6b3c0-121">Authorization</span></span>  | <span data-ttu-id="6b3c0-122">Носитель {token} (обязательно)</span><span class="sxs-lookup"><span data-stu-id="6b3c0-122">Bearer {token} (required)</span></span> |
| <span data-ttu-id="6b3c0-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6b3c0-123">Content-Type</span></span>   | <span data-ttu-id="6b3c0-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6b3c0-124">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="6b3c0-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="6b3c0-125">Request body</span></span>

<span data-ttu-id="6b3c0-126">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-126">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="6b3c0-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="6b3c0-127">Response</span></span>

<span data-ttu-id="6b3c0-128">Успешный ответ — всегда ответ **204 No Content**.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-128">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="6b3c0-129">Неавторизованные вызывающие объекты получат ответ **401 Unauthorized** или **403 Forbidden**.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-129">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="6b3c0-130">Если отправка завершилась неудачей (например, из-за проверки), ответ будет **500 Server Error**, а текст ответа будет содержать объект JSON с дополнительной информацией.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-130">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="6b3c0-131">Пример</span><span class="sxs-lookup"><span data-stu-id="6b3c0-131">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="6b3c0-132">Сообщения о проверке и ошибках</span><span class="sxs-lookup"><span data-stu-id="6b3c0-132">Validation and error messages</span></span>

<span data-ttu-id="6b3c0-133">В ходе вызова для отправки API платформа Human Resources выполняет проверку бизнес-логики перед отправкой, чтобы запрос отпуска находится в допустимом состоянии для отправки.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-133">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="6b3c0-134">Возможные сообщения об ошибках, которые могут появиться в ответе в случае сбоя проверок:</span><span class="sxs-lookup"><span data-stu-id="6b3c0-134">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="6b3c0-135">В результате этого запроса сальдо '{LeaveTypeId}' будет ниже допустимого минимального сальдо на {date}.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-135">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="6b3c0-136">Невозможно отправить запрос времени отсутствия в завершенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-136">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="6b3c0-137">Не удалось отправить или сохранить запрос, поскольку изменения не выполнены.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-137">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="6b3c0-138">Добавьте или обновите сумму или тип отпуска и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-138">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="6b3c0-139">Введенный запрос о времени отсутствия содержит один или несколько дней с одинаковой датой и типом отпуска как существующий ожидающий запрос.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-139">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="6b3c0-140">Отзовите существующий запрос для внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-140">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="6b3c0-141">Код основания '{ReasonCodeId}' не применяется ни к одному из типов отпуска в запросе.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-141">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="6b3c0-142">Для типа отпуска {LeaveTypeId} требуется код причины.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-142">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="6b3c0-143">Выберите соответствующий тип и код причины.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-143">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="6b3c0-144">Время отсутствия не было отправлен успешно.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-144">The time off was not submitted successfully.</span></span> <span data-ttu-id="6b3c0-145">Время отсутствия сохранено как черновик запроса.</span><span class="sxs-lookup"><span data-stu-id="6b3c0-145">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b3c0-146">См. также</span><span class="sxs-lookup"><span data-stu-id="6b3c0-146">See also</span></span>

- [<span data-ttu-id="6b3c0-147">Обзор MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="6b3c0-147">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="6b3c0-148">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="6b3c0-148">Authentication</span></span>](hr-developer-api-authentication.md)