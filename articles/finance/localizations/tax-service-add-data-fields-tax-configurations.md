---
title: Добавление полей данных в налоговые конфигурации
description: В этой теме объясняется, как настроить налоговые конфигурации путем добавления полей данных.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ebb186a4cb9ca61399909625233b579acd2c0ec5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022795"
---
# <a name="add-data-fields-in-tax-configurations"></a>Добавление полей данных в налоговые конфигурации

[!include [banner](../includes/banner.md)]

В этой теме объясняется, как настроить налоговые конфигурации с помощью [полей данных, которые добавляются в налоговую интеграцию](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Настройка модели налоговых данных

1. В Microsoft Dynamics 365 Finance перейдите в раздел **Электронная отчетность** \> **Конфигурации налогов**.
2. В дереве конфигурации выберите **Модель налоговых данных — Европа**. Затем на панели операций выберите **Создать конфигурацию**.
3. В раскрывающемся диалоговом окне выберите параметр **Модель налогооблагаемого документа, производная от имени: модель налоговых данных — Европа, Microsoft**, введите имя для новой модели налоговой данных, затем выберите **Создать конфигурацию**.
4. Выберите только что созданную модель налоговых данных, затем в области действий выберите **Конструктор**.
5. Разверните дерево модели данных, выберите **Строки**, затем выберите **Создать**.
6. В диалоговом окне **Создание узла** введите имя, укажите тип элемента, а затем нажмите кнопку **Добавить**.
7. Добавьте необходимые столбцы.
8. На панели операций выберите **Сохранить**, затем выберите **Завершить**.
9. Закройте страницу и просмотрите завершенную версию модели налоговых данных.

## <a name="customize-the-tax-configuration"></a>Настройка конфигурации налогов

1. В Finance перейдите в раздел **Электронная отчетность** \> **Конфигурации налогов**.
2. В дереве конфигурации выберите **Конфигурация налогов — Европа**. Затем на панели операций выберите **Создать конфигурацию**.
3. В раскрывающемся диалоговом окне выберите параметр **Конфигурация налоговой службы, производная от имени: Конфигурация налогов — Европа, Microsoft**, введите имя для новой конфигурации налогов, затем выберите **Создать конфигурацию**.
4. Выберите только что созданную конфигурацию налогов, затем в области действий выберите **Конструктор**.
5. В разделе **Свойства** в поле **Модель данных** выберите ранее созданную настроенную модель налоговых данных.
6. В поле **Версия модели данных** выберите завершенную версию модели налоговых данных.
7. Выберите **Добавить** и добавьте требуемые налоговые меры.
8. На панели операций выберите **Сохранить**, затем выберите **Завершить**.
9. Закройте страницу и просмотрите завершенную версию конфигурации налогов.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Реализация налоговых функций в настраиваемой конфигурации налогов

1. В Regulatory Configuration Services (RCS) перейдите в раздел **Функции глобализации** \> **Налог**.
2. Выберите **Добавить**, введите сведения о новой функции, затем выберите **Создать функцию**.
3. На вкладке **Версии** выберите функцию, затем выберите **Изменить**.
4. На вкладке **Общие** в поле **Версия конфигурации** выберите настраиваемую конфигурацию и версию налога.
5. В диалоговом окне **Управление столбцами** выберите заголовок и столбцы строк, которые необходимо включить в настраиваемую налоговую меру, затем выберите кнопку со стрелкой вправо, чтобы добавить их в список **Выбранные столбцы**.
