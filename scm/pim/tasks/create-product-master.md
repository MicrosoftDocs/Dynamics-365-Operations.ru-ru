--- 
title: "Создание шаблона продукта"
description: "Создайте шаблон продукта для предопределенных вариантов."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b783c41459163ab5a0644a1ff5c39b6933bcdb1b
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-master"></a>Создание шаблона продукта

[!include[task guide banner](../../includes/task-guide-banner.md)]

Создайте шаблон продукта для предопределенных вариантов. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF. Эта процедура предназначена для конструктора продуктов.


## <a name="create-a-new-product-master"></a>Создание нового шаблона продукта
1. Перейдите в раздел "Управление сведениями о продукте" > "Продукты" > "Шаблоны продукта".
2. Щелкните "Создать".
3. В поле "Номер продукта" введите значение.
    * Номер должен быть уникальным. Для поля "Номер продукта" можно задать номерную серию. В этом случае пользователю необязательно вводить значение.  
4. В поле "Имя продукта" введите значение.
    * Введите описательное наименование продукта. По умолчанию это значение совпадает с кратким наименованием, однако пользователь может его изменить.  
5. В поле "Группа аналитик продуктов" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
    * Группа аналитик продукта определяет, какую из четырех аналитик продукта можно использовать для создания вариантов продукта. В этом примере используется группа с цветом и размером.  
6. В списке найдите и выберите требуемую запись.
7. В списке перейдите по ссылке в выбранной строке.
    * Технология конфигурации по умолчанию — "Предопределенный вариант". Она и будет использоваться в этом примере.  
8. Нажмите кнопку "OК".

## <a name="select-product-dimension-groups"></a>Выбор групп аналитик продукта
1. В поле "Группа цветов" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
2. Поиск и выбор требуемой записи в списке.
3. В списке перейдите по ссылке в выбранной строке.
4. В поле "Группа размеров" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
5. В списке найдите и выберите требуемую запись.
6. В списке перейдите по ссылке в выбранной строке.

## <a name="add-dimension-groups"></a>Добавление групп аналитики
1. В области действий щелкните "Продукт".
2. Щелкните "Группы аналитики", чтобы открыть ниспадающее диалоговое окно.
3. В поле "Группа аналитик хранения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
    * С помощью аналитик хранения можно управлять хранением и извлечением номенклатур из запасов. Например, аналитика хранения может включать параметры "Сайт" и "Склад".  
4. В списке найдите и выберите требуемую запись.
5. В списке перейдите по ссылке в выбранной строке.
6. В поле "Группа аналитик отслеживания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
    * Группа аналитик отслеживания определяет, какие аналитики отслеживания можно добавить к продукту. Например, номер партии и серийный номер используются для отслеживания складских номенклатур.  
7. В списке найдите и выберите требуемую запись.
8. В списке перейдите по ссылке в выбранной строке.
9. Нажмите кнопку OK.
10. Нажмите кнопку "Сохранить".
11. Закройте страницу.

