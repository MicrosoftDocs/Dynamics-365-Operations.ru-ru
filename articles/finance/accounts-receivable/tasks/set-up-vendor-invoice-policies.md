---
title: Настройка политик накладных поставщиков
description: В этом разделе описывается, как настроить политики накладных поставщика.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72f017294c976dcd1b7ddda01ac9e39252f036d6
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250287"
---
# <a name="set-up-vendor-invoice-policies"></a>Настройка политик накладных поставщиков

[!include [task guide banner](../../includes/task-guide-banner.md)]

В этом разделе описывается, как настроить политики накладных поставщика. Политики накладных поставщиков применяются при разноске накладной поставщика с помощью страницы "Накладная поставщика" и при открытии страницы "Нарушения политики" накладной поставщика. Вы также можете настроить workflow-процесс накладной поставщика для выполнения политик накладных поставщиков при каждом отправлении накладной в workflow-процесс. 

- Политики накладных поставщиков не применяются к накладным, созданным в реестре или журнале накладных.  
- При проверке сопоставления накладных не используются политики накладных поставщиков, проверка настраивается на странице "Параметры модуля расчетов с поставщиками".  
- В данной записи используется демонстрационная компания USMF. Эти шаги выполняются ролями менеджера по расчету с поставщиками или главного бухгалтера. Перед началом работы убедитесь, что выбран конфигурационный ключ "Сопоставление накладных".


## <a name="prepare-to-create-vendor-invoice-policies"></a>Подготовка к созданию политики накладных поставщиков
1. Выберите **Область перехода > Модули > Расчеты с поставщиками > Настройка > Параметры расчетов с поставщиками**.
2. Выберите вкладку **Проверка накладной**.
3. Установите или снимите флажок **Автоматически обновлять статус заголовка накладной**.
4. Нажмите **ОК**.
5. В поле **Разнести накладную с несоответствиями** выберите параметр.
6. Закройте страницу.
7. Перейдите к **Область перехода > Модули > Расчеты с поставщиками > Настройка политики > Политики накладных поставщика**.
8. Выберите **Параметры**.
9. Выберите **Добавить**.
10. Закройте страницу и вернитесь на домашнюю страницу.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Создание типов правил политики для накладных поставщика
1. Перейдите к **Область перехода > Модули > Расчеты с поставщиками > Настройка политики > Типы правил политики для накладных поставщика**.
2. Выберите **Создать**.
3. Введите значения в поля **Имя правила** и **Описание**.
4. В поле **Имя запроса** нажмите кнопку раскрывающегося списка, чтобы открыть поиск, а затем выберите желаемую запись.
5. Нажмите **Сохранить**.
6. Закройте страницу и вернитесь на домашнюю страницу.

## <a name="define-a-vendor-invoice-policy"></a>Определение политики накладных поставщиков
1. Перейдите к **Область перехода > Модули > Расчеты с поставщиками > Настройка политики > Политики накладных поставщика**.
2. Выберите **Создать**.
3. Введите значения в поля **Имя** и **Описание**.
4. Разверните или сверните раздел **Организации политики**.
5. В дереве выберите **Contoso Entertainment System USA**.
6. Выберите **Добавить**.
7. Разверните или сверните раздел **Правила политики**.
8. Выберите **Создать правило политики**.
9. В поле **Описание правила политики** введите значение.
10. Выберите **Фильтр**.
11. Выберите **Добавить**. Выберите требуемую запись.
12. В полях **Таблица**, **Производная таблица** и **Поле** выберите или введите параметры из выпадающих меню.
13. Закройте страницу.
14. В поле **Критерии** введите значение.
15. Нажмите **ОК**.
16. Нажмите **ОК**.
17. Закройте страницы и вернитесь на домашнюю страницу.
