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
# <a name="removed-or-deprecated-platform-features"></a>Удаленные или устаревшие функции Platform

[!include [banner](../includes/banner.md)]

В этом разделе описываются возможности, который удалены или которые планируется удалить в обновлениях платформы приложений Finance and Operations.

- *Удаленная* функция больше недоступна в продукте.
- *Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.

Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании. 

> [!NOTE]
> Подробные сведения об объектах в приложениях Finance and Operations можно найти в документе [Технический справочник по отчетам](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Можно сравнить различные версии этих отчетов, чтобы получить сведения об объектах, которые были изменены или были исключены в каждой версии приложений Finance and Operations.

## <a name="platform-update-32"></a>Обновление платформы update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Диалоговое окно "запрос на изменение бизнес-правила" больше не включает раскрывающийся список выбора пользователя
|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Это связано с безопасностью, поскольку запрос на изменение может быть отправлен непредусмотренному пользователю. Это также проблема для удобства использования, поскольку требует от пользователя определить, кто был инициатор workflow-процесса, и вручную выбрать их.  |
| **Заменена другой функцией?**   | Нет |
| **Затрагиваемые области продукта**         | Рабочий процесс |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Раскрывающийся список выбора пользователя был удален из диалогового окна запроса на изменение в обновлении платформы 32. Запросы на изменение запроса будут автоматически отправлены инициатору по назначению. Дополнительные сведения об этих функциях см. в разделе [Действия в процессах утверждения workflow-процесса](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Предыдущие объявления об удаленных или устаревших функциях
Для получения дополнительных сведений о функциях, которые были удалены или устарели в предыдущих выпусках, см [Удаленные или устаревшие функции в предыдущих выпусках](../migration-upgrade/deprecated-features.md).

