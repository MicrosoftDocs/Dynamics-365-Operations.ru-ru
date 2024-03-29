---
title: Отчет об ошибках разноски вследствие недоступности запасов или конфликтов обновления
description: В этой статье приводятся возможные способы обхода проблем, связанных с запасами, при разноске выписок в Microsoft Dynamics 365 Commerce.
author: Shajain
ms.date: 12/19/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: cebb890b42def6e9b002b01be63266b88bfc35a4
ms.sourcegitcommit: 4ad87483ba0bfea3e04fdb7e578d8abc34e607a4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2022
ms.locfileid: "9887634"
---
# <a name="statement-posting-errors-due-to-unavailable-inventory-or-update-conflicts"></a>Отчет об ошибках разноски вследствие недоступности запасов или конфликтов обновления

[!include [banner](../../includes/banner.md)]

В этой статье приводятся возможные способы обхода проблем, связанных с запасами, при разноске выписок в Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Наименование

Во время разноски проводок в Commerce могут быть выведены сообщения об ошибках, связанных с проблемами запасов или конфликтами обновления.

### <a name="inventory-issues-error-message"></a>Сообщение об ошибке с проблемами запасов

При возникновении проблем с запасами полученное сообщение об ошибке будет выглядеть так, как в этом примере:

> хх не может быть скомплектовано, поскольку в запасах имеется только yy

### <a name="update-conflict-error-messages"></a>Сообщения об ошибках конфликтов обновления

Проблема конфликта обновления могут происходить, когда методом оценки запасов является или *стандартная себестоимость*, или *скользящее среднее*. Так как оба этих метода являются бессрочными методами учета затрат, окончательные затраты определяются во время разноски.

При использовании метода *скользящего среднего* сообщение об ошибке конфликта обновления, которые вы получите, будет похоже на этот пример:

> Значение запасов xx,xx после пропорционального расчета расходов не ожидается

При использовании метода *стандартной себестоимости* сообщение об ошибке конфликта обновления, которые вы получите, будет похоже на этот пример:

> В результате обновления стандартные затраты не соответствуют финансовой величине запасов. Значение = xx,xx, Кол-во = yy,yy, Стандартная себестоимость = zz,zz

## <a name="resolutions"></a>Разрешения

### <a name="workaround-for-the-inventory-error"></a>Обходное решение для ошибки запасов

Устранение ошибки запасов можно выполнить либо путем обновления запасов для номенклатуры вручную, либо путем включения физического отрицательного запаса для группы номенклатурных моделей, связанной с номенклатурой в Commerce Headquarters.

Для согласованного интерфейса разноски Microsoft рекомендует включить отрицательные физические запасы для группы моделей номенклатуры. В некоторых сценариях выписки может быть невозможно разнести, если не включить отрицательные физические запасы.

Например, нет доступных запасов для номенклатуры, но кассир возвращает номенклатуру, а затем добавляет ее к той же проводке с уменьшенной ценой, чтобы имитировать сопоставление цены. В этом случае проводка возврата и проводка по продажам будут подаваться в одну и ту же выписку для одного заказа клиента. Однако, поскольку не существует гарантии, что строка возврата (которая увеличивает запасы) будет разнесена до строки продажи (которая сокращает запасы), могут возникать ошибки запасов. Если физический отрицательный запас включен в этом сценарии, разноска проводок не затрагивается, и система будет правильно отражать запасы.

#### <a name="enable-negative-physical-inventory-for-an-item-model-group"></a>Включение отрицательных физических запасов для группы номенклатурных моделей

Чтобы включить отрицательные физические запасы для группы номенклатурных моделей в Commerce headquarters, выполните следующие действия.

1. Перейдите в **Управление запасами \> Настройка \> Запасы**.
1. В области переходов слева выберите группу моделей номенклатуры.
1. В разделе **Политики запасов** в разделе **Отрицательные запасы** установите флажок **Физические отрицательные запасы**.

![Физический отрицательный запас включен.](./media/Physical_Negative_Inventory.png)

### <a name="workaround-for-the-update-conflict-error"></a>Обходное решение для ошибки конфликта обновления

Возможные обходные решения для исправления ошибки конфликта обновления см. в разделе [Конфликт обновления, когда методом оценки запасов является или стандартная себестоимость, или скользящее среднее](/troubleshoot/dynamics-365/supply-chain/costing/update-conflict-standard-cost-moving-average-inventory-valuation)

> [!NOTE]
> Для ошибки конфликта обновления не нужно удалять заказы клиентов, созданные с использованием этапа агрегирования при разноске. После реализации предлагаемых обходных решений журнал операций должен разноситься, если повторно попытаться выполнить разноску журнала операций.
