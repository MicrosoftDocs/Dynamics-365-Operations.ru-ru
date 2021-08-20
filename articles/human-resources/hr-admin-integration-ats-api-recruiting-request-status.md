---
title: Состояние запроса по набору сотрудников
description: В этом разделе описывается набор параметров состояния запроса на набор сотрудников для Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 91360b07915ba10472768ac32b473e6daf7163fa8aed24e6aabaaa91f0ec7154
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723679"
---
# <a name="recruiting-request-status"></a>Состояние запроса по набору сотрудников

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается набор параметров состояния запроса на набор сотрудников для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmrecruitingrequeststatus

Это перечисление предоставляет набор параметров для значений состояния сущности RecruitingRequest.

| значение | Этикетка | описание |
| --- | --- | --- |
| 200000000 | Черновой | Запрос находится в состоянии черновика и не готов к активному набору сотрудников. |
| 200000001 | На рассмотрении | Запрос был отправлен и направляется на утверждение по рабочему процессу. Доступно только в том случае, если включен рабочий процесс. |
| 200000002 | Ожидает | Запрос ожидает действия рабочего процесса. Доступно только в том случае, если включен рабочий процесс. |
| 200000003 | Отменено | Запрос отменен. Доступно только в том случае, если включен рабочий процесс. |
| 200000004 | Отказано | Запрос был отклонен. Доступно только в том случае, если включен рабочий процесс. |
| 200000005 | Активные сотрудники | Все рабочие процессы выполнены и утверждены, и запрос готов к активному набору сотрудников. |
| 200000006 | Закрытые | Запроса на набор сотрудников закрыт. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса для запроса на набор персонала](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]