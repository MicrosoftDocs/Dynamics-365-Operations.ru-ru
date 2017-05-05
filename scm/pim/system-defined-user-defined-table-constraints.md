---
title: "Системные и пользовательские ограничения таблиц"
description: "В этой статье рассматриваются два типа ограничений таблицы для компонентов в модели конфигурации продукта — определяемые пользователем и определяемые системой. Ограничения таблицы представляют собой матрицы разрешенных комбинаций атрибутов, где каждая строка определяет один набор возможных значений атрибутов."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 510ee819e6bc69b72df767f6cfd284230baba729
ms.lasthandoff: 03/31/2017


---

# <a name="system-defined-and-user-defined-table-constraints"></a>Системные и пользовательские ограничения таблиц

[!include[banner](../includes/banner.md)]


В этой статье рассматриваются два типа ограничений таблицы для компонентов в модели конфигурации продукта — определяемые пользователем и определяемые системой. Ограничения таблицы представляют собой матрицы разрешенных комбинаций атрибутов, где каждая строка определяет один набор возможных значений атрибутов.

Ограничения таблиц представляют собой матрицы сочетаний атрибутов, который разрешены для компонентов в модели конфигурации продукта. Каждая строка в таблице определяет один комплект возможных значений атрибутов. В модели конфигурации продукта можно объявить два типа ограничений:

-   **Ограничение для выражения** — создайте выражение, которое определяет отношения между атрибутами, чтобы при конфигурации продукта можно была выбрать только совместимые значения.
-   **Ограничение таблицы** — создание таблицы, которая определяет все комбинации, разрешенные для определенного набора атрибутов. Два Типа ограничений таблицы доступны: пользовательские ограничения таблицы и системные ограничения таблицы.

В этой статье описываются ограничения таблицы, которые пользователями и системой определены для компонентов в модели конфигурации продукта.

## <a name="user-defined-table-constraints"></a>Пользовательские ограничения таблицы
Пользовательские ограничения таблицы — это тип матрицы, который может использоваться для описания комбинаций для значений атрибутов, которые определяются типами атрибута. Например, если вы делаете динамики, можно включить столбцы для отделки корпуса и передней решетки в пользовательское ограничение таблицы. Тип атрибута для отделки корпуса имеет четыре значения, и тип атрибута для передней решетки имеет три значения. Поэтому если ограничения не используются, возможно 4 × 3 = 12 комбинаций. Однако в этом примере допускается только шесть комбинаций, как показано в следующей таблице. Эта информация отображается на вкладке **Разрешенные комбинации** на странице **Изменить ограничение таблицы**.

| Отделка корпуса | Передняя решетка |
|----------------|-------------|
| Черный          | Черный       |
| Черный          | Металл       |
| Дуб            | Черный       |
| Палисандр       | Белый       |
| Белый          | Черный       |
| Белый          | Белый       |

Пользовательские ограничения таблицы определяются статическим вводов в таблицу, который действует так же, как ограничение выражения. При использовании пользовательских ограничений таблицы, преимущество в том, что таблицы часто бывает проще создать, понимать и поддерживать, чем длинные ограничения выражения.

## <a name="system-defined-table-constraints"></a>Определенные системой ограничения таблицы
Системой определенное ограничение таблицы создает динамическое сопоставление между типом атрибута и полем в таблице. Когда определенное системой ограничение таблицы включено в модель конфигурации продукта, сопоставление гарантирует, что данные в таблице отображаются вместо значений типа атрибута. Результатом является динамическое ограничение, поскольку содержимое таблицы может быть изменено (например, другими модулями).  

При создании системой определенного ограничения таблицы, вы выбираете таблицу, при желании определяет запрос, который необходимо использовать, а затем связываете типы атрибутов с полями в выбранной таблице. Типы полей должны соответствовать типам типов атрибута.  

Прежде чем ограничение таблицы может начать действовать в модели конфигурации продукта, ограничение таблицы необходимо включить в ограничение на одном из компонентов модели. Процедура заключается в том, чтобы создать новое ограничение, выбрать тип ограничения таблицы, затем выбрать определение ограничения таблицы для использования. В заключение все поля в ограничении таблицы необходимо составить атрибутам в модели конфигурации продукта.

<a name="see-also"></a>См. также
--------

[Основные понятия моделей конфигурации продукта](product-configuration-models.md)



