---
title: Атрибуты партии
description: В этой статье представлена информация об атрибутах партии. Атрибуты партии являются характеристиками сырья и готовых продуктов, которые образуют партии складских запасов. В статье также описывается, как назначать атрибуты партии, и как можно производить по ним поиск при резервировании партий.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e5f5a03df63cf4fa90b5e9e67082a0d60eef9afc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899392"
---
# <a name="batch-attributes"></a>Атрибуты партии

[!include [banner](../includes/banner.md)]

В этой статье представлена информация об атрибутах партии. Атрибуты партии являются характеристиками сырья и готовых продуктов, которые образуют партии складских запасов. В статье также описывается, как назначать атрибуты партии, и как можно производить по ним поиск при резервировании партий.

Атрибуты партии являются характеристиками сырья и готовых продуктов, которые образуют партии складских запасов. Атрибуты партии могут различаться в зависимости от ряда факторов, включающих условия окружающей среды или качество сырья, использованного для создания партии, или выхода готового продукта. Число и типы используемых атрибутов партии сильно отличаются для различных отраслей. Здесь приводятся два примера использования атрибутов партий:

-   При производстве сыра молоко как сырье может характеризоваться такими атрибутами как содержание жира и процентное содержание. Сыр, производимый из молока, может иметь другие атрибуты, например, влажность и срок вызревания.
-   При производстве стали производимое железо может характеризоваться такими атрибутами как содержание магния, содержание серебра и содержание цинка.

Чтобы лучше управлять числом и типами атрибутов, вы можете использовать группы атрибутов партии. Таким образом вам не придется добавлять каждый атрибут индивидуально.

## <a name="assign-batch-attributes"></a>Назначение атрибутов партии
Атрибуты партии можно назначать отдельным продуктам, входящим в партии складских запасов, или можно назначать их продуктам, связанным с конкретными клиентами. Прежде чем атрибут партии можно будет назначить на уровне клиентов, его необходимо назначить на уровне продукта. Продукт должен иметь аналитику партии, установленную в состояние **Активная** в группе аналитик отслеживания. Чтобы назначить атрибут партии отдельному продукту, используйте страницу для определенного продукта. Если атрибут является специфическим для продукта для клиента, используйте форму для определенного клиента. Когда вы добавляете атрибут к продукту, вы также определяете другие параметры. Далее приводятся некоторые примеры.

-   Минимальный и максимальный диапазоны для атрибута типа **Целое число** или **Дробь**.
-   Действия, выполняемые при превышении допуска, для атрибута типа **Целое число** или **Дробь**. Если значение атрибута выходит за пределы минимального и максимального диапазонов, действие может быть или предупреждением, или сообщением об ошибке.
-   Целевое значение для атрибута. Данное значение является оптимальным значением атрибута и применяется к атрибутам всех типов.

Доступ к страницам для продуктов, выбираемых на странице **Запущенные в производство продукты**, предоставляется в разделе "Управление сведениями о продуктах". После того как продукту назначены атрибуты партии, можно затем добавить отдельные значения атрибутам на странице **Атрибуты партии складских запасов**.

## <a name="reserve-batches"></a>Резервирование партий
Вы можете искать по атрибутам партии, когда вы резервируете партию для заказа на продажу, чтобы выполнить заказ клиента, или когда вы комплектуете и резервируете партии для производственного заказа. Поиск помогает найти партию складских запасов, в которой содержится продукт с требуемыми атрибутами партии. После того как партия или партии найдены, можно затем зарезервировать продукт для создаваемой строки складской проводки.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]