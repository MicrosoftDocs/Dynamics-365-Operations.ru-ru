---
title: Настройка кодов причин
description: Dynamics 365 Human Resources использует коды причин, чтобы объяснить причину изменения льготы сотрудника.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6fc641233a1bd217de5b9eb6e06560b989f91c7b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056356"
---
# <a name="set-up-reason-codes"></a>Настройка кодов причин

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources использует коды причин, чтобы объяснить причину изменения льготы сотрудника.

> [!NOTE]
> По состоянию на январь 2021 года коды причин переходят в рабочую область **Управление персоналом** вместо рабочей области **Управление льготами**. Дополнительные сведения см. в разделе [Миграция кодов причин в управление персоналом вручную](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Создание кодов причины

1. В рабочей области **Управление персоналом** (или в рабочей области **Управление льготами**, если коды причин еще не перенесены), выберите **Ссылки**, затем выберите **Коды причин**.

2. Выберите **Создать**.

3. Укажите значения для следующих полей:

   | Поле | Описание |
   | --- | --- |
   | **Код основания** | Уникальное имя, определяющее причину, по которой у сотрудника изменится регистрация плана льгот. |
   | **Описание** | Описание кода причины. |

4. В области **Применимые сценарии** задайте для параметра **Управление льготами** значение **Да**. (Не применяется, если коды причин еще не перенесены в рабочую область **Управление персоналом**.)

5. Нажмите **Сохранить**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Миграция кодов причин в управление персоналом вручную

В январе 2021 года коды причин переходят в рабочую область **Управление персоналом** вместо рабочей области **Управление льготами**. Большая часть данных кодов причин будет автоматически перенесена в вашей среде. По некоторым причинам данные кодов причин могут быть не перенесены. Например, коды причин теперь имеют максимальное значение в 15 знаков, поэтому все коды причин, длина которых превышает 15 символов, не переносятся автоматически.

Вы увидите баннер на странице **Ссылки** в рабочей области **Управление льготами**, которая информирует вас о миграции и о том, были ли перенесены коды причин.

1. Выберите **Коды причин** для получения сведений о статусе миграции.

   [![Коды оснований](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Выберите код причины, для которого не удалось выполнить миграцию.

   [![Статус миграции кода причины](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. Выберите **Перенести код причины**.

   [![Мигрировать код основания](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. В области **Миграция кода причины льготы** имеются два параметра для сопоставления с кодом причины управления персоналом:

   - Чтобы использовать существующий код причины в модуле управления персоналом, выберите его в раскрывающемся списке **Использовать существующий код причины**.
     > [!NOTE]
     > Можно использовать существующий код причины в модуле "Управление персоналом" только в том случае, если еще не выполнена миграция другого кода причины модуля управления льготами.
   - Чтобы создать новый код причины в модуле "Управление персоналом", введите новое значение в поле **Создать код причины**, затем введите описание в поле **Создать описание**.

   [![Сопоставление с кодом причины в модуле "Управление персоналом"](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

После того как коды причин переносятся в модуль "Управление персоналом", параметр использования их в модуле "Управление льготами" автоматически устанавливается значение **Да**.

[![Использование кода причин в управлении льготами](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]