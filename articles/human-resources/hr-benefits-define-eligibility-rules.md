---
title: Определение правил и политик проверки прав на льготы
description: Эта статья показывает, как создавать правила и политики проверки прав на льготы, а затем назначать правила льготам.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: fa507591fc89eaebf617deedb15b15a0f93f971d
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010403"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Определение правил и политик проверки прав на льготы

Эта статья показывает, как создавать правила и политики проверки прав на льготы, а затем назначать правила льготам.  

В качестве компании с демонстрационными данными для создания этой записи используется USMF.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Создание типа правил политики приемлемости льготы
1. Перейдите в раздел "Управление персоналом" > "Льготы" > "Приемлемость" > "Типы правил политики права на льготу".
2. Щелкните "Создать".
3. В поле "Правило" введите значение.
4. В поле "Описание" введите значение.
5. В поле "Имя запроса" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
6. В списке перейдите по ссылке в выбранной строке.
7. Нажмите кнопку "Сохранить".
8. Закройте страницу.

## <a name="benefit-eligibility-policy"></a>Политика права на льготу
1. Перейдите в раздел "Управление персоналом" > "Льготы" > "Приемлемость" > "Политики приемлемости льготы".
2. Выберите существующую политику права на льготу.
3. В списке перейдите по ссылке в выбранной строке.
4. Переключите развертывание разделов организаций политики.  Здесь можно добавить или удалить организации, которые требуется включить в политику.
5. Разверните или сверните раздел "Правила политики".
6. Найдите в списке ранее созданное правило политики.
7. Щелкните "Создать правило политики".
8. В поле "Действует с" введите дату, когда политика должна вступить в силу.
    * Задание даты вступления в силу и даты окончания позволяет вносить в правила политики изменения, которые должны вступить в силу в будущем, не возвращаясь в политике перед моментом вступления их в силу.  
9. 
    * Например, если требуется, чтобы правило применялось только к менеджерам по продажам, можно создать предложение с условием "Где", например: "Где описание должности равно Менеджер по продажам".  В одном правиле можно объединить несколько операторов "Где" с помощью операторов "И" и "Или".  
10. Нажмите кнопку "OК".
11. Закройте страницу.
12. Закройте страницу.

## <a name="assign-rule-to-benefit"></a>Назначение правила льготе
1. Перейдите в раздел "Управление персоналом" > "Льготы" > "Льготы".
2. В списке найдите и выберите требуемую запись.
3. В списке перейдите по ссылке в выбранной строке.
4. Разверните или сверните раздел "Правила приемлемости".
5. Выберите Изменить.
6. В поле "Приемлемость" выберите из списка "На основе правила".
7. В поле "Тип правила" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
8. Найдите в списке ранее созданное правило и выберите его.
9. В списке перейдите по ссылке в выбранной строке.
10. Нажмите кнопку "Сохранить".
11. Закройте форму.
