---
title: Отправка запроса на отпуск в workflow-процесс
description: В Microsoft Dynamics 365 Human Resources можно воспользоваться API MyLeaveRequests submit(), чтобы отправить запрос на отпуск в workflow-процесс.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 51be70edbe1439340377fd01b9760d49d3a75348
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115520"
---
# <a name="submit-a-leave-request-to-workflow"></a>Отправка запроса на отпуск в workflow-процесс

В Microsoft Dynamics 365 Human Resources можно воспользоваться API MyLeaveRequests submit(), чтобы отправить запрос на отпуск в workflow-процесс. Этот API представляется как действие для объекта OData MyLeaveRequests.

## <a name="prerequisites"></a>Необходимые условия

Запрос на отпуск должен быть сохранен в базе данных и должен быть доступен для извлечения с помощью объекта MyLeaveRequests.

## <a name="permissions"></a>Права доступа

Для вызова этого API требуется одно из следующих разрешений. Дополнительные сведения о разрешениях и как их выбрать см. в [Аутентификация](hr-developer-api-authentication.md).

| Тип разрешения                    | Разрешения (от минимальных до максимальных привилегий) |
|------------------------------------|--------------------------------------------------------|
| Делегировано (рабочая или учебная учетная запись) | user\_impersonation                                    |

## <a name="https-request"></a>HTTPS-запрос

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

Запрос соответствует стандартам OData. Параметры {requestId}, {leaveType}, {leaveDate} и {dataArea} относятся к полям, составляющим составной естественный ключ для объекта MyLeaveRequests.

> [!NOTE]
> Хотя поля для объекта MyLeaveRequests ссылаются на отдельную строку в запросе отпуска, при вызове API будет отправлен весь запрос отпуска (все строки) в workflow-процесс.

### <a name="request-headers"></a>Заголовки запроса

| Заголовок         | Value                     |
|----------------|---------------------------|
| Санкционирование  | Носитель {token} (обязательно) |
| Content-Type   | application/json          |

### <a name="request-body"></a>Текст запроса

Не указывайте текст запроса для этого метода.

### <a name="response"></a>Отклик

Успешный ответ — всегда ответ **204 No Content**.

Неавторизованные вызывающие объекты получат ответ **401 Unauthorized** или **403 Forbidden**.

Если отправка завершилась неудачей (например, из-за проверки), ответ будет **500 Server Error**, а текст ответа будет содержать объект JSON с дополнительной информацией.

## <a name="example"></a>Пример

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

## <a name="validation-and-error-messages"></a>Сообщения о проверке и ошибках

В ходе вызова для отправки API платформа Human Resources выполняет проверку бизнес-логики перед отправкой, чтобы запрос отпуска находится в допустимом состоянии для отправки. Возможные сообщения об ошибках, которые могут появиться в ответе в случае сбоя проверок:

 - В результате этого запроса сальдо '{LeaveTypeId}' будет ниже допустимого минимального сальдо на {date}.
 - Невозможно отправить запрос времени отсутствия в завершенном состоянии.
 - Не удалось отправить или сохранить запрос, поскольку изменения не выполнены. Добавьте или обновите сумму или тип отпуска и повторите попытку.
 - Введенный запрос о времени отсутствия содержит один или несколько дней с одинаковой датой и типом отпуска как существующий ожидающий запрос. Отзовите существующий запрос для внесения изменений.
 - Код основания '{ReasonCodeId}' не применяется ни к одному из типов отпуска в запросе.
 - Для типа отпуска {LeaveTypeId} требуется код причины. Выберите соответствующий тип и код причины.
 - Время отсутствия не было отправлен успешно. Время отсутствия сохранено как черновик запроса.

## <a name="see-also"></a>См. также

- [Обзор MyLeaveRequests](hr-developer-api-myleaverequests-overview.md)
- [Проверка подлинности](hr-developer-api-authentication.md)