---
title: Создание типов планов
description: Тип плана в Microsoft Dynamics 365 Human Resources является высокоуровневой группировкой различных типов льгот. Каждый тип плана имеет код типа плана, который определяет правила для данного типа плана.
author: andreabichsel
ms.date: 04/06/2020
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
ms.openlocfilehash: eb4746425c2faa3c0b1bd3940bf2e03cf7f9595c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057870"
---
# <a name="create-plan-types"></a>Создание типов планов

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Тип плана в Microsoft Dynamics 365 Human Resources является высокоуровневой группировкой различных типов льгот. Каждый тип плана имеет код типа плана, который определяет правила для данного типа плана. Например, тип плана "основное страхование жизни" будет иметь код типа плана "жизненный", так как это вид плана страхования жизни, и должен соответствовать правилам, установленным для кода типа плана "жизнь". Другой тип плана может быть "дополнительное страхование жизни", также кодом типа плана "жизнь".

Каждый тип плана указывает, может ли сотрудник регистрироваться в одном или нескольких планах его типа. Например, сотрудник, скорее всего, сможет регистрироваться для полисов "базового страхования жизни" и "дополнительного страхования жизни" типа плана "жизнь". Вероятно, сотруднику разрешается регистрировать только в одном полисе типа "медицина".

Если тип плана включает контакты, тип плана указывает, являются ли контакты бенефициарами или иждивенцами. Например, у типа плана "основная жизнь" могут быть бенефициары, в то время как у типа плана "основной медицинский" будут иждивенцы. В некоторых случаях в плане могут отсутствовать личные контакты. Например, план сбережений на случай непредвиденных расходов или премии за парковку.

Для типа плана можно определить параметры покрытия. Параметры покрытия определяются в форме параметров покрытия. В параметре покрытия можно указать сумму льготы или контакты, которые могут быть допустимыми для типа плана. Например, если тип контакта — "бенефициар", параметр покрытия должен определять условия того, что бенефициар имеет право получить, когда используется льгота. Если тип контакта — "Иждивенец", параметр покрытия должен определять связь между иждивенцем и сотрудником. 

1. В рабочей области **Управление льготами** в разделе **Настройка** выберите **Типы планов**.

2. Выберите **Создать**.

3. Укажите значения для следующих полей:

   | Поле | Описание |
   | --- | --- |
   | **Тип плана** | Уникальное имя, идентифицирующее тип плана. |
   | **Описание** | Описание типа плана. |
   | **Код типа плана** | Выберите код типа плана из раскрывающегося списка значений. В списке код типа плана отображаются все типы планов, поддерживаемые в текущей версии. |
   | **Одновременная регистрация** | Указывает, может ли сотрудник регистрироваться в нескольких планах льгот того же типа плана или только в одном плане льготы для каждого типа плана. |
   | **Тип контакта** | Задает роль личного контакта. Значения пусты, иждивенец и бенефициар. Можно оставить поле **Тип контакта** пустым, если тип плана не требует наличия иждивенца или бенефициара на основе параметра покрытия. |

4. Чтобы настроить параметры жизненного события, выберите **Действия**, а затем выберите **Параметры жизненных событий**. Укажите значения для следующих полей:

   | Поле | Описание |
   | --- | --- |
   | **Тип плана** | Тип плана, для которого настраиваются параметры жизненного события. |
   | **Идентификатор типа жизненного события** | Код типа жизненного события. |
   | **Разрешить отмену** | Указывает, может ли сотрудник отменять план льгот во время жизненного события. |
   | **Изменить параметр покрытия** | Указывает, может ли сотрудник изменять параметры покрытия во время жизненного события. |
   | **Изменить на новый план** | Указывает, может ли сотрудник изменять планы во время жизненного события. |
   | **Автоматическая отмена плана** | Указывает, следует ли автоматически отменять план в течение жизненного события. |
   | **Автоматически повторно открыть проверку допустимости** | Указывает, следует ли автоматически повторно открывать проверку допустимости регистрации льгот в ходе жизненного события. |
   | **Окно отчетности** | Указывает окно отчетности в днях для жизненного события. **Примечание**. Если не ввести сумму, система предполагает, что окно отчетности равно нулю и не будет обрабатывать жизненное событие. |

5. Нажмите **Сохранить**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]